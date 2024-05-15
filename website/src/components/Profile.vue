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
        type: Image,
        required: false
    }
})
</script>

<template>
    <div class="profile">
        <img class="profile__picture" s:src="ProfilePicture" alt="Description of image">
        <div class="profile__content">
            <h2 class="profile__name"> {{ ProfileName }}</h2>
            <div class="profile_location-container">
                <LocationIcon class="profile__location-icon"> </LocationIcon>
                <span class="profile__location"> {{ Location }} </span>
            </div>
            <div class="profile__social-links">
                <SocialLinks socialIcon="#" socialLink="#" socialName="Facebook" />
                <SocialLinks socialIcon="#" socialLink="#" socialName="Twitter" />
                <SocialLinks socialIcon="#" socialLink="#" socialName="LinkedIn" />
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
    padding: 20px;
    padding-left: 200px;
    max-width: 80%;
}

.profile__picture {
    border-radius: 50%;
    width: 150px;
    height: 150px;
    object-fit: cover;
    margin-right: 20px;
}

.profile__content {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}

.profile__name {
    font-size: 24px;
    font-weight: bold;
    color: #333;
    margin: 0;
}

.profile_location-container {
    display: flex;
    align-items: center;
    margin: 10px 0;
}

.profile__social-links {
    display: flex;
    justify-content: flex-start;
    margin: 10px 0;
}

.profile__description {
    font-size: 14px;
    color: #666;
    margin-bottom: 20px;
}

.profile__form {
    width: 100%;
    border-top: 1px solid #eee;
    padding-top: 10px;
}
</style>