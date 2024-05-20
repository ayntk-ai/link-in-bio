<script setup>
import LocationIcon from './icons/LocationIcon.vue'
import SocialLinks from './SocialLinks.vue'
import From from './Form.vue'
defineProps({
    ProfileName: {
        type: String,
        required: false
    },
    ProfileDescription: {
        type: String,
        required: false
    },
    Location: {
        type: String,
        required: false
    },
    ProfilePicture: {
        type: String,
        required: false
    }
})
</script>

<template>
    <div class="profile">
        <img class="profile__picture" :src="ProfilePicture" alt="Description of image">
        <div class="profile__content">
            <h2 class="profile__name"> {{ ProfileName }}</h2>
            <div class="profile_location-container">
                <LocationIcon class="profile__location-icon"> </LocationIcon>
                <span class="profile__location"> {{ Location }} </span>
            </div>
            <div class="profile__social-links">
                <SocialLinks socialIcon="src/assets/images/instagram.png" socialLink="https://instagram.com/"
                    socialName="Facebook" />
                <SocialLinks socialIcon="src/assets/images/x.png" socialLink="https://x.com/" socialName="X" />
                <SocialLinks socialIcon="src/assets/images/linkedin.png" socialLink="https://www.linkedin.com/"
                    socialName="LinkedIn" />
            </div>
            <p class="profile__descripiton"> {{ ProfileDescription }}</p>
            <From class="profile__form"></From>
        </div>
    </div>
</template>

<style scoped>
.profile {
    display: flex;
    flex-direction: row;
    align-items: center;
    padding: var(--lb-space-s);
    padding-left: var(--lb-space-2xl);
    max-width: 90%;
}

.profile__picture,
.fit-cover {
    border-radius: 30px;
    width: 150px;
    height: 150px;
    margin-right: var(--lb-space-l);
    object-fit: cover;
}

.profile__content {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}

.profile__name {
    font-size: var(--lb-text-l);
    font-weight: var(--lb-font-700);
    color: var(--lb-text);
    margin: 0;
}

.profile_location-container {
    display: flex;
    align-items: center;
    margin: var(--lb-space-xs) 0;
    gap: var(--lb-space-3xs);
    color: var(--lb-text);
}

.profile__social-links {
    display: flex;
    justify-content: flex-start;
    margin: var(--lb-space-xs) 0;
}

.profile__descripiton {
    font-size: var(--lb-text-s);
    color: var(--lb-text);
    margin-bottom: var(--lb-space-l);
}

.profile__form {
    width: 100%;
    border-top: 1px solid var(--lb-bg-body-d-1);
    padding-top: var(--lb-space-xs);
}
</style>