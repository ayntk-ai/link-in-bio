<script setup>
defineProps({
    LinkName: {
        type: String,
        required: false
    },
    LinkImage: {
        type: String,
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
    background: white;
    border-radius: var(--lb-radius-s);
    box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.1);
    display: flex;
    flex-direction: column;
    max-width: 100%;
    padding: var(--lb-space-m);
    margin-top: var(--lb-space-m);
    margin-bottom: var(--lb-space-m);
    font-family: 'Arial', sans-serif;
}

@media (prefers-color-scheme: dark) {
    .link-card {
        background: var(--lb-bg-body-d-4);
        border-radius: var(--lb-radius-s);
        box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.1);
        display: flex;
        flex-direction: column;
        max-width: 100%;
        padding: var(--lb-space-m);
        margin-top: var(--lb-space-m);
        margin-bottom: var(--lb-space-m);
        font-family: 'Arial', sans-serif;
    }

}

.link-card__heading {
    display: flex;
    align-items: center;
    margin-bottom: var(--lb-space-m);
    color: var(--lb-text);
}

.link-card__image {
    border-radius: 50%;
    width: 40px;
    height: 40px;
    margin-right: var(--lb-space-xs);
}

.link-card__name-container {
    display: flex;
    flex-direction: column;
}

.link-card__service-name {
    font-size: var(--lb-text-m);
    font-weight: var(--lb-font-700);
    color: var(--lb-text);
}

.link-card__content {
    margin-bottom: var(--lb-space-m);
}

.link-card__description {
    font-size: var(--lb-text-xs);
    color: var(--lb-text);
}

.link-card__footer {
    display: flex;
    justify-content: flex-end;
    width: 100%;
}

.link-card__link {
    color: var(--lb-accent);
    text-decoration: none;
    font-size: var(--lb-text-xs);
    padding: var(--lb-space-4xs) var(--lb-space-2xs);
    border: 1px solid var(--lb-accent);
    border-radius: var(--lb-radius-s);
    display: inline-block;
}
</style>