<template>
  <div class="p-3 flex items-center justify-between">
      <div class="flex items-center">
        <button class="rounded-full hover:bg-light p-3 flex items-center justify-center" type="button" name="button">
          <img src="logo.png" alt="logo" class="h-6 w-6">  
        </button>
        <button v-for="(item,index) in tabItems" v-bind:key="index" @click="selectedTab=item.key" :class=" `${selectedTab === item.key ? ' bg-dark text-white':'text-dark hover:bg-light' }` + ' rounded-full py-3 px-4 font-semibold focus:outline-none' " type="button" name="button">
          {{item.name}}
        </button>
      </div>
  </div>  
</template>

<script>


export default {
data(){
    return{
        tabItems:[
          {name: 'Home', key:'home'},
          {name: 'Today', key:'today'}
        ],
        selectedTab: 'home'
    }
}
};


</script>

<style scoped>

</style>



