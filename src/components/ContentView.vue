<script setup>
import { ref, onMounted } from "vue";
import axios from "axios";
import CardCourse from "./CardCourse.vue";

const courses = ref([]);

const fetchCourses = async () => {
    try {
        const response = await axios.get("http://localhost:3000/courses", {
            withCredentials: true,
            headers: {
                "Content-Type": "application/json",
            },
        });
        courses.value = response.data;
    } catch (error) {
        console.error("Error fetching courses:", error);
    }
};

onMounted(() => {
    fetchCourses();
});
</script>

<template>
    <div class="grid-cols-1 md:grid-cols-2 grid lg:grid-cols-3 gap-4">
        <CardCourse v-for="course in courses" :key="course.id" :course="course" />
    </div>
</template>
