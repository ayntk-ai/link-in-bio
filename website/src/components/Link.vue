<script setup>
defineProps({
    LinkName: {
        type: String,
        required: false
    },
    LinkImage: {
        type: Image,
        required: false
    },
    
    LinkDescription: {
        type: String,
        required: false
    },
    LinkText: {
        type: String,
        required: false
    },
    LinkURL: {
        type: URL,
        required: false
    },
})
</script>

<template>
    <div class="link-card">
        <div class="link-card__heading">
            <img class="link-card__image" v-bind:src="LinkImage" alt="Service Image">
            <div class="link-card__name-container">
                <h2 class="link-card__service-name"> {{ LinkName }}</h2>
            </div>
        </div>
        <div class="link-card__content">
            <p class="link-card__description"> {{ LinkDescription }}</p>
        </div>
        <div class="link-card__footer">
            <a class="link-card__link" v-bind:href="LinkURL" target="_blank" rel="noopener">{{ LinkText }}</a>
        </div>
    </div>
</template>

<style scoped>
.link-card {
    background: #FFFFFF;
    border-radius: 4px;
    box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.1);
    display: flex;
    flex-direction: column;
    max-width: 100%;
    padding: 16px;
    margin-top: 16px;
    margin-bottom: 16px;
    font-family: 'Arial', sans-serif;
}

.link-card__heading {
    display: flex;
    align-items: center;
    margin-bottom: 16px;
}

.link-card__image {
    border-radius: 50%;
    width: 40px;
    height: 40px;
    margin-right: 8px;
}

.link-card__name-container {
    display: flex;
    flex-direction: column;
}

.link-card__service-name {
    font-size: 1em;
    font-weight: bold;
    color: #333;
}

.link-card__content {
    margin-bottom: 16px;
}

.link-card__description {
    font-size: 0.8em;
    color: #666;
}

.link-card__footer {
    display: flex;
    justify-content: flex-end;
    width: 100%;
}

.link-card__link {
    color: #007bff;
    text-decoration: none;
    font-size: 0.8em;
    padding: 4px 8px; 
    border: 1px solid #007bff;
    border-radius: 4px;
    display: inline-block;
}
</style>