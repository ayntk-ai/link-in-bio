<script setup>
defineProps({
    ServiceName: {
        type: String,
        required: false
    },
    ServiceImage: {
        type: Image,
        required: false
    },
    ServiceStartYear: {
        type: Date,
        required: false
    },
    ServiceEndYear: {
        type: Date,
        required: false
    },
    PersonalServiceRole: {
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
    ServiceRevenue: {
        type: Number,
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
        <div class="service-card__heading">
            <img class="service-card__image" v-bind:src="ServiceImage" alt="Service Image">
            <div class="service-card__name-container">
                <h2 class="service-card__service-name"> {{ ServiceName }}</h2>
                <div class="service-card__name-container-year">
                    <span class="service-card__service-start-year"> {{ ServiceStartYear }} - </span>
                    <span class="service-card__service-end-year"> {{ ServiceEndYear }}</span>
                </div>
            </div>
            <span class="service-card__service-status"> {{ ServiceStatus }}</span>
        </div>
        <div class="service-card__content">
            <p class="service-card__role"> {{ PersonalServiceRole }}</p>
            <p class="service-card__description"> {{ ServiceDescription }}</p>
        </div>
        <div class="service-card__footer">
            <div class="service-card__footer-revenue">
                <span class="service-card__revenue-icon"> $ </span>
                <p class="service-card__revenue"> {{ ServiceRevenue }}</p>
                <span class="service-card__revenue-text"> MRR </span>
            </div>
            <a class="service-card__link" v-bind:href="ServiceLink" target="_blank" rel="noopener">Link Text</a>
        </div>
    </div>
</template>

<style scoped>
.main {
    width: 100%;
}

.service-card {
    background: #FFFFFF;
    border-radius: 10px;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    display: flex;
    flex-direction: column;
    max-width: 350px;
    padding: 20px;
    margin-top: 40px;
    margin-bottom: 40px;
    font-family: 'Arial', sans-serif;
    align-items: flex-start;
}

.service-card__heading {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    margin-bottom: 20px;
}

.service-card__image {
    border-radius: 50%;
    width: 50px;
    height: 50px;
    margin-right: 10px;
}

.service-card__name-container {
    display: flex;
    flex-direction: column;
}

.service-card__service-name {
    font-size: 1.2em;
    font-weight: bold;
    color: #333;
}

.service-card__name-container-year {
    display: flex;
    align-items: left;
    flex-direction: row;
    width: 100%;
}

.service-card__service-start-year,
.service-card__service-end-year {
    font-size: 0.9em;
    color: #666;
}

.service-card__service-end-year {
    margin-left: 5px;
}

.service-card__service-status {
    background-color: #007bff;
    color: white;
    border-radius: 15px;
    padding: 5px 10px;
    font-size: 0.8em;
    display: flex;
    align-items: center;
}

.service-card__content {
    margin-bottom: 20px;
}

.service-card__role {
    font-size: 1em;
    font-weight: bold;
    color: #333;
    margin-bottom: 5px;
}

.service-card__description {
    font-size: 0.9em;
    color: #666;
}

.service-card__footer {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
}

.service-card__footer-revenue {
    display: flex;
    align-items: left;
}

.service-card__revenue-icon {
    color: #333;
    font-size: 1.2em;
    font-weight: bold;
    margin-right: 5px;
}

.service-card__revenue {
    font-size: 1.2em;
    font-weight: bold;
    color: #333;
    display: flex;
    align-items: center;
}

.service-card__revenue-text {
    font-size: 1.2em;
    color: #666;
    margin-left: 5px;
}

.service-card__link {
    color: black;
    text-decoration: none;
    font-size: 0.9em;
    padding: 5px 10px;
    border-radius: 15px;
    display: flex;
    align-items: center;
    justify-content: center;
}

.service-card__link::after {
    content: url('./icons/LocationIcon.vue');
    margin-left: 5px;
}
</style>