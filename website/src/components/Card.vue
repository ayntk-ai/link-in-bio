<script setup>
defineProps({
    ServiceName: {
        type: String,
        required: false
    },
    ServiceDescription: {
        type: String,
        required: false
    },
    ServiceStatus: {
        type: String,
        required: false
    },
    ServiceLink: {
        type: URL,
        required: false
    },
})
</script>

<template>
    <div class="service-card">
        <h2 class="service-card__heading"> {{ ServiceName }}</h2>  
        <p class="servic-card__descripiton"> {{ ServiceDescription }}</p>
        <span class="service-card__status"> {{ ServiceStatus }}</span>
        <a class="service-card__link" v-bind:href="ServiceLink" target="_blank" rel="noopener">Link Text</a>
    </div>
</template>

<style scoped>
.service-card {
    background-color: #f9f9f9;
    border-radius: 10px;
    padding: 20px;
    margin: 10px;
}
.service-card__heading{
    font-size: 1.5rem;
    margin-bottom: 10px;
}
.service-card__description{
    font-size: 1rem;
    margin-bottom: 10px;
}
.service-card__status{
    font-size: 1rem;
    margin-bottom: 10px;
}
.service-card__link{
    font-size: 1rem;
    margin-bottom: 10px;
}
</style>