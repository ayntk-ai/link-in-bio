<script setup>
import Card from './Card.vue'
import Link from './Link.vue'
</script>

<template>
    <div>
        <div class="tabs">
            <button @click="activeTab = 'services'" :class="{ 'active': activeTab === 'services' }">Services</button>
            <button @click="activeTab = 'links'" :class="{ 'active': activeTab === 'links' }">Links</button>
        </div>

        <div v-if="activeTab === 'services'">
            <div class="services">
                <Card ServiceName="This is a Test Service!" ServiceImage="path/to/image.jpg" ServiceStartYear="2022"
                    ServiceEndYear="2023" PersonalServiceRole="Developer" ServiceDescription="Officia irure fugiat duis ad. Consectetur velit exercitation do occaecat cillum culpa. Eiusmod occaecat id laborum laboris. Voluptate anim ullamco nisi enim. Commodo do velit excepteur fugiat. Officia enim aute reprehenderit enim irure. Eu tempor et pariatur anim voluptate dolore eiusmod enim commodo.
" ServiceStatus="Development" ServiceRevenue="1000" ServiceLink="https://example.com" />
                <Card ServiceName="This is a Test Service!" ServiceImage="path/to/image.jpg" ServiceStartYear="2022"
                    ServiceEndYear="2023" PersonalServiceRole="Developer" ServiceDescription="Officia irure fugiat duis ad. Consectetur velit exercitation do occaecat cillum culpa. Eiusmod occaecat id laborum laboris. Voluptate anim ullamco nisi enim. Commodo do velit excepteur fugiat. Officia enim aute reprehenderit enim irure. Eu tempor et pariatur anim voluptate dolore eiusmod enim commodo.
" ServiceStatus="Development" ServiceRevenue="1000" ServiceLink="https://example.com" />
            </div>
        </div>

        <div v-if="activeTab === 'links'">
            <Link class="links"
  LinkName="Bloomberg"
  LinkImage="https://path-to-bloomberg-logo.com/logo.png"
  LinkDescription="An article about how I built Aviator and eventually sold it."
  LinkText="Read More"
  LinkURL="https://www.bloomberg.com"
/>

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
main {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 50%;
}

.app {
    max-width: 1140px;
    margin: 0 auto;
}

.profile,
.services {
    width: 100%;
    max-width: 1140px;
    margin: 0 auto;
}

.tabs {
    display: flex;
    justify-content: center;
    padding: 1rem;
    gap: 1rem;
}

.tabs button {
    flex: 1;
    padding: 0.5rem 1rem;
    border: none;
    background-color: #f1f1f1;
    cursor: pointer;
    border-radius: 20px;
}

.tabs button.active {
    background-color: #ffffff;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.tab-content {
    width: 100%;
    max-width: 1140px;
    margin: 0 auto;
}

.links{
    display: flex;
    flex-direction: row;
    align-items: center;
    padding: 20px;
    padding-left: 200px;
    max-width: 80%;
}
</style>