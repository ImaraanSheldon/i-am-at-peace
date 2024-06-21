<template>
    <div>
      <h2 class="text-center p-3">Friends List</h2>
      <div v-if="friends.length === 0">Loading spinner...</div>
      <div v-else>
        <CardComp v-for="friend in friends" :key="friend.id" class="card" :style="{ borderColor: friend.gender === 'male' ? 'gold' : 'pink' }">
          <template #cardHeader>
            <h4 class="card-header text-center fw-bold" :style="{color: friend.gender === 'female' ? 'pink': 'gold' }">{{ friend.firstName }} {{ friend.lastName }}</h4>
          </template>
          <template #cardBody>
            <div class="card-body d-flex align-items-center flex-column m-2">
            <img :src="friend.profile" alt="Profile Image">
            <p>Gender: {{ friend.gender }}</p>
            <!-- Add more details as needed -->
          </div>
          </template>
        </CardComp>
      </div>
    </div>
  </template>
  
  <script>
  import CardComp from './CardComp.vue'

  export default {
    name: 'FriendsComp',
    data() {
      return {
        friends: [
          { id: 1, firstName: 'Imaraan', lastName: 'Sheldon', gender: 'male', profile: 'Portrait_Placeholder.png' },
          { id: 2, firstName: 'Ashley', lastName: 'Kiwitz', gender: 'female', profile: 'Portrait_Placeholder.png' }
          // Friends
        ]
      };
    },
    components:{
      CardComp
    }
  };
  </script>
  
  <style>
  .card {
    margin-bottom: 20px;
  }
  img{
    width: 30vw;
  }
  </style>
  