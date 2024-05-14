<script setup>
import Card from './Card.vue'
</script>

<template>
    <div>
        <div class="tabs">
            <button @click="activeTab = 'services'" :class="{ 'active': activeTab === 'services' }">Services</button>
            <button @click="activeTab = 'links'" :class="{ 'active': activeTab === 'links' }">Links</button>
        </div>

        <div v-if="activeTab === 'services'">
            <h2>Services</h2>
            <div class="services">
                <Card ServiceName="This is a Test Service!" ServiceDescription="Discription" ServiceStatus="Developement" ServiceLink="#"/>
                <Card ServiceName="This is a Test Service!" ServiceDescription="Discription" ServiceStatus="Developement" ServiceLink="#"/>
            </div>
        </div>

        <div v-if="activeTab === 'links'">
            <h2>Links</h2>
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

<style>
.tabs {
    display: flex;
}

button {
    padding: 10px;
    margin-right: 10px;
    background-color: #eee;
    border: none;
    cursor: pointer;
}

button.active {
    background-color: #ccc;
}
</style>