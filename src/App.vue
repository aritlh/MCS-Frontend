<script setup>
import NavigationBar from "./components/NavigationBar.vue";
import ContentView from "./components/ContentView.vue";
</script>

<template>
    <div class="container mx-auto py-20">
        <div class="space-y-20">
            <NavigationBar title="Moodle Course Syncer (MCS)" />
            <ContentView />
        </div>
    </div>
</template>
