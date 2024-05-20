<script setup>
import Profile from './components/Profile.vue'
import Tab from './components/Tab.vue'
</script>

<template>
  <main>
    <div class="profile">
      <Profile ProfileName="Max Mustermann"
        ProfileDescription="Officia irure fugiat duis ad. Consectetur velit exercitation do occaecat cillum culpa. Eiusmod occaecat id laborum laboris. Voluptate anim ullamco nisi enim"
        Location="Berlin" ProfilePicture="./images/profile-image.jpg" />
    </div>

    <div class="services">
      <Tab></Tab>
    </div>
  </main>
</template>

<style scoped>
.profile,
.services {
  max-width: 1140px;
  margin: 0 auto;
}
</style>
