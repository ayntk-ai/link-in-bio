<script setup>
import LocationIcon from './icons/LocationIcon.vue'
import SocialLinks from './SocialLinks.vue'
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
        <h2 class="profile__name"> {{ ProfileName }}</h2>
        <p class="profile__descripiton"> {{ ProfileDescription }}</p>
        <LocationIcon class="profile__location-icon"> </LocationIcon>
        <div>
            <SocialLinks socialIcon="#" socialLink="#" socialName="Facebook" />
            <SocialLinks socialIcon="#" socialLink="#" socialName="Twitter" />
            <SocialLinks socialIcon="#" socialLink="#" socialName="LinkedIn" />
        </div>
        <span class="profile__location"> {{ Location }} </span>
        <img class="profile__picture" s:src="ProfilePicture" alt="Description of image">
    </div>
</template>

<style scoped>
.profile {
    display: flex;
    width: 100%;
    flex-direction: column;
    align-items: center;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
    margin: 20px;
}
.profile__name {
    font-size: 24px;
    margin: 10px 0;
}
.profile__descripiton {
    margin: 10px 0;
}
.profile__location {
    margin: 10px 0;
}
.profile__location-icon {
    margin: 10px 0;
}
.profile__picture {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    margin: 10px 0;
}
</style>