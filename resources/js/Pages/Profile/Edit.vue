<script setup>
import UpdateInfo from "./Partials/UpdateInfo.vue";
import UpdatePassword from "./Partials/UpdatePassword.vue";

defineProps({
    user: Object,
    status: String,
});
</script>

<template>
    <Head title="- Profile" />
    <UpdateInfo :user="user" :status="status" />
    <UpdatePassword />
</template>