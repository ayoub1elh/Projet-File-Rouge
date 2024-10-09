<script setup>
import Card from '../Components/Card.vue';

defineProps({
    listings: Object,
});
</script>

<template>
    <Head title="- Latest Listings"/>

    <div v-if="Object.keys(listings.data).length">
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
            <div v-for="listing in listings.data" :key="listing.id">
                <Card :listing="listing" />
            </div>
        </div>
        <Pagination :data="listings" @onPagination="fetchListings"/>

    </div>
</template>