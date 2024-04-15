<script setup lang="ts">
type SideMenuType = {
  name: string
  value: string
}

const icons: Array<SideMenuType> = [
  {
    name: 'HOME',
    value: '/'
  },
  {
    name: 'FromLink',
    value: '/ltt'
  },
  {
    name: 'FromSoundFile',
    value: '/ftt'
  },
  {
    name: 'FromTextFile',
    value: '/tts'
  }
]

</script>

<template>
<!--  navigation bar-->
  <nav class="p-4 flex items-center justify-around">
    <div class="flex items-center">
      <v-icon size="large" icon="midYoutube"></v-icon>
      <h1 class="text-2xl mx-1 font-bold text-white">Y2Text</h1>
    </div>
    <div>
      <input class="h-10 w-96 px-4 bg-dark border border-white rounded-l-full" placeholder="link"/>
      <button type="submit" class="h-10 px-8 ml-0 bg-char border border-white rounded-r-full text-white">
        START
      </button>
    </div>
    <div></div>
  </nav>
  <div class="flex">
<!--    TODO: side menu-->
    <div class="pl-2 pt-4 w-1/12">
      <div class="py-4 w-fit hover:cursor-pointer hover:bg-gray-700 hover:rounded-xl" v-for="icon in icons" :key="icon.name">
        <p class="w-20 text-white truncate text-center text-xs">{{icon.name}}</p>
      </div>

    </div>
<!--    TODO: contents-->
    <div class="p-6 mx-2 w-11/12 min-h-max">

    </div>
  </div>
</template>