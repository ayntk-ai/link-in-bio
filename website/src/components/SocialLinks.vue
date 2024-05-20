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
    <div class="social-links">
        <a class="social-url" :href="socialLink" target="_blank" rel="noopener noreferrer">
            <img class="social-icon" :src="socialIcon" :alt="socialName" />
            <span class="social-text"> {{ socialName }}</span>
        </a>
    </div>
</template>

<style scoped>
.social-links {
    display: flex;
    align-items: center;
    gap: var(--lb-space-s);
}

.social-url {
    display: flex;
    align-items: center;
    text-decoration: none;
    color: var(--lb-text);
    font-size: var(--lb-text-s);
    margin-right: var(--lb-space-m);
}

.social-icon {
    width: var(--lb-space-4xs);
    height: var(--lb-space-4xs);
    margin-right: var(--lb-space-2xs);
    object-fit: cover;
}

.social-text {
    font-size: var(--lb-text-s);
    color: var(--lb-text);
}
</style>