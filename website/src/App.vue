<script setup>
import Profile from './components/Profile.vue'
import Tab from './components/Tab.vue'
</script>

<template>
  <header></header>

  <main>
    <div class="profile">
      <Profile ProfileName="This is a Test Profile!"
        ProfileDescription="Officia irure fugiat duis ad. Consectetur velit exercitation do occaecat cillum culpa. Eiusmod occaecat id laborum laboris. Voluptate anim ullamco nisi enim"
        Location="Location" ProfilePicture="imageSrc" />
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
  width: 100%;
}

.profile,
.services {
  width: 1140px;
  margin: 0 auto;
}
</style>
