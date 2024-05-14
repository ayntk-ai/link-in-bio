<script setup>
defineProps({
    socialIcon: {
        type: String,
        required: true
    },
    socialLink: {
        type: String,
        required: true
    },
    socialName: {
        type: String,
        required: true
    }
})
</script>


<template>
    <div>
        <a :href="socialLink" target="_blank">
        <img :src="socialIcon" :alt="socialName" />
        </a>
    </div>
</template>

<style scoped>


</style>