<template>
  <div>
    <personal-data/>

    <the-about />

    <the-skills/>
  </div>
</template>

<script>
  import PersonalData from '@/components/Home/PersonalData.vue'
  import TheAbout from '@/components/Home/TheAbout.vue'
  import TheSkills from '@/components/Home/TheSkills.vue'

  export default {
    
    name: 'App',
    components: {
      PersonalData,
      TheAbout,
      TheSkills
    }
}
</script>

<style>
  * {
    margin: 0;
    padding: 0;
  }
</style>
