<template>
  <div class="home">
  <!-- <p v-if="'path ===/'">You are on Home Page</p>
  <p v-else>You're on {{ path }}</p> -->

  <p><span :title="message">Hover & see the dynamic title</span></p>
  <p :class="{red:isRed}" @click="toggleRed">This should be red....But click me to toggle</p>
  <p :style="{color}" @click="toggleColor">This will change color when clicking</p>
  </div>
</template>

<script>
// // @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

// export default {
//   name: 'HomeView',
//   components: {
//     HelloWorld
//   }
// }
export default
 {data()
   {return{message: 'Hello World', isRed: true, color: 'green'}},
   methods: {
  toggleRed(){this.isRed = !this.isRed},
  toggleColor(){this.color = this.color ==='green' ? 'blue' : 'green'}
}
}
// data:{path: Location.pathname}


</script>
<style>
.red{color: red;}</style>