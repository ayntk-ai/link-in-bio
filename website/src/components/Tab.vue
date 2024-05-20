<script setup>
import Card from './Card.vue'
import Link from './Link.vue'
</script>

<template>
    <div class="tab-container">
        <div class="tabs">
            <button @click="activeTab = 'services'" :class="{ 'active': activeTab === 'services' }">Services</button>
            <button @click="activeTab = 'links'" :class="{ 'active': activeTab === 'links' }">Links</button>
        </div>

        <div class="services-tab" v-if="activeTab === 'services'">

            <Card class="card" ServiceName="Photo Lens" ServiceImage="public/images/service-1.jpg"
                ServiceStartYear="2018" ServiceEndYear="2020" PersonalServiceRole="Designer" ServiceDescription="Officia irure fugiat duis ad. Consectetur velit exercitation do occaecat cillum culpa. Eiusmod occaecat id laborum laboris. Voluptate anim ullamco nisi enim. Commodo do velit excepteur fugiat. Officia enim aute reprehenderit enim irure. Eu tempor et pariatur anim voluptate dolore eiusmod enim commodo.
" ServiceStatus="Discountinued" ServiceRevenue="10" ServiceLink="https://example.com" />
            <Card ServiceName="Macbook Clean" ServiceImage="public/images/service-2.jpg" ServiceStartYear="2021"
                ServiceEndYear="x" PersonalServiceRole="Developer" ServiceDescription="Officia irure fugiat duis ad. Consectetur velit exercitation do occaecat cillum culpa. Eiusmod occaecat id laborum laboris. Voluptate anim ullamco nisi enim. Commodo do velit excepteur fugiat. Officia enim aute reprehenderit enim irure. Eu tempor et pariatur anim voluptate dolore eiusmod enim commodo.
" ServiceStatus="Growing" ServiceRevenue="1200" ServiceLink="https://example.com" />
            <Card ServiceName="Money Report" ServiceImage="public/images/service-3.jpg" ServiceStartYear="2023"
                ServiceEndYear="2024" PersonalServiceRole="Developer" ServiceDescription="Officia irure fugiat duis ad. Consectetur velit exercitation do occaecat cillum culpa. Eiusmod occaecat id laborum laboris. Voluptate anim ullamco nisi enim. Commodo do velit excepteur fugiat. Officia enim aute reprehenderit enim irure. Eu tempor et pariatur anim voluptate dolore eiusmod enim commodo.
" ServiceStatus="Sold" ServiceRevenue="25000" ServiceLink="https://example.com" />

        </div>

        <div v-if="activeTab === 'links'">
            <div class="links-tab">
                <Link LinkName="Substack" LinkImage="public/images/newsletter.jpg"
                    LinkDescription="My montly Newsletter" LinkText="Read More" LinkURL="https://substack.com" />
                <Link LinkName="Portfolio" LinkImage="public/images/portfolio.jpg" LinkDescription="My Portfolio"
                    LinkText="Read More" LinkURL="https://substack.com" />
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            activeTab: 'services'
        };
    }
};
</script>

<style scoped>
.tab-container {
    width: 100%;
    max-width: 1000px;
    margin: 0 auto;
}

.services-tab {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
    margin: 20px;
}




.tabs {
    display: flex;
    justify-content: center;
    font-size: var(--lb-text-s);
    gap: var(--lb-space-m);
}

.tabs button {
    background-color: var(--lb-bg-body-d-1);
    font-size: var(--lb-text-s);
    color: var(--lb-text);
    padding-top: var(--lb-space-xs);
    padding-bottom: var(--lb-space-xs);
    padding-left: var(--lb-space-2xl);
    padding-right: var(--lb-space-2xl);
    font-size: var(--lb-text-m);
    cursor: pointer;
    border-radius: var(--lb-radius-s);
    transition: background-color 0.3s ease, color 0.3s ease;
}

.tabs button:hover {
    background-color: var(--lb-accent);
    color: var(--lb-text);
}

.tabs button:focus {
    outline: none;
    box-shadow: 0 0 0 1px var(--lb-text);
    border-radius: var(--lb-radius-s);
}


.tabs button.active {
    background-color: var(--lb-accent);
}

.tab-content {
    width: 100%;
    max-width: 1140px;
    margin: 0 auto;
}
</style>