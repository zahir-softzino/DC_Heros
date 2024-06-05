<template>
  <div class="w-full flex">
    <div class="m-auto">
      <AppHeader />
      <dcHeros />
    <!-- </div>
    <div class="m-auto"> -->
      <!-- <ul>
        <li class="flex justify-between" v-for="(hero, index) in dcHeros" :key="index">
          <div>
            {{ hero.name }}
          </div>
          <button @click="remove(index)">x</button>
        </li>
      </ul> -->

      <form class="mt-10" @submit.prevent="addHero">
        <input class="border border-gray-800 rounded mr-5" v-model.lazy="newHero" placeholder="New Hero"/>
        <button class="border rounded bg-gradient-to-r from-gray-200 to-gray-500" type="submit">Add hero</button>  
      </form>
    </div>    
    
  </div>
  
</template>

<script>
 
  import AppHeader from "./components/AppHeader.vue"
  import dcHeros from "./components/dcHeros.vue"
export default {
  components: {AppHeader, dcHeros},
  
}
</script>

