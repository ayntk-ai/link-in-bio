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
            <a class="service-card__link" v-bind:href="ServiceLink" target="_blank" rel="noopener">URL</a>
        </div>
    </div>
</template>

<style scoped>
.service-card {
    background: var(--lb-bg-body);
    border-radius: var(--lb-radius-s);
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    display: flex;
    flex-direction: column;
    max-width: 450px;
    padding: var(--lb-space-s);
    margin-top: var(--lb-space-m);
    margin-bottom: var(--lb-space-m);
    align-items: flex-start;
}

@media (prefers-color-scheme: dark) {
    .service-card {
        background: var(--lb-bg-body-d-4);
        border-radius: var(--lb-radius-s);
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
        display: flex;
        flex-direction: column;
        max-width: 450px;
        padding: var(--lb-space-s);
        margin-top: var(--lb-space-m);
        margin-bottom: var(--lb-space-m);
        align-items: flex-start;
    }
}

.service-card__heading {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    margin-bottom: var(--lb-space-s);
    color: var(--lb-text);
}

.service-card__image {
    border-radius: 50%;
    width: 50px;
    height: 50px;
    margin-right: var(--lb-space-2xs);
}

.service-card__name-container {
    display: flex;
    flex-direction: column;
}

.service-card__service-name {
    font-size: var(--lb-text-l);
    font-weight: var(--lb-font-700);
    color: var(--lb-text);
}

.service-card__name-container-year {
    display: flex;
    align-items: left;
    flex-direction: row;
    width: 100%;
}

.service-card__service-start-year,
.service-card__service-end-year {
    font-size: var(--lb-text-xs);
    color: var(--lb-text);
}

.service-card__service-end-year {
    margin-left: var(--lb-space-4xs);
}

.service-card__service-status {
    background-color: var(--lb-accent);
    color: var(--lb-bg-body-d);
    border-radius: var(--lb-radius-xl);
    padding: var(--lb-space-4xs) var(--lb-space-2xs);
    font-size: var(--lb-text-xs);
    display: flex;
    align-items: center;
}

.service-card__content {
    margin-bottom: var(--lb-space-l);
}

.service-card__role {
    font-size: var(--lb-text-m);
    font-weight: var(--lb-font-700);
    color: var(--lb-text);
    margin-bottom: var(--lb-space-4xs);
}

.service-card__description {
    font-size: var(--lb-text-s);
    color: var(--lb-text);
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
    color: var(--lb-text);
    font-size: var(--lb-text-l);
    font-weight: var(--lb-font-700);
    margin-right: var(--lb-space-4xs);
}

.service-card__revenue {
    font-size: var(--lb-text-l);
    font-weight: var(--lb-font-700);
    color: var(--lb-text);
    display: flex;
    align-items: center;
}

.service-card__revenue-text {
    font-size: var(--lb-text-l);
    color: var(--lb-bg-body-d-6);
    margin-left: var(--lb-space-4xs);
    color: var(--lb-text);
}

.service-card__link {
    background-color: var(--lb-bg-body-d-1);
    color: var(--lb-text);
    text-decoration: none;
    text-align: center;
    font-size: var(--lb-text-s);
    padding: var(--lb-space-4xs) var(--lb-space-2xs);
    border-radius: var(--lb-radius-xl);
    display: flex;
    align-items: center;
    justify-content: center;
}
</style>