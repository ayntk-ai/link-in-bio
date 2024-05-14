<script setup>
import Profile from './components/Profile.vue'
import Tab from './components/Tab.vue'
// import Header from './components/Header.vue'
// import Footer from './components/Footer.vue'
</script>

<template>
  <header></header>

  <main>
    <div class="profile">
      <Profile ProfileName="This is a Test Profile!" ProfileDescription="Discription" Location="Location" ProfilePicture="imageSrc"/>
    </div>
    
    <div class="services"> 
      <Tab></Tab>
    </div>
  </main>
</template>

<style scoped>
  main {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
.app {
  width: 1140px;
}

</style>
