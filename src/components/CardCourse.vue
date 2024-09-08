<script setup>
import { Card, CardContent, CardDescription, CardFooter, CardHeader, CardTitle } from "@/components/ui/card";

defineProps({
    course: {
        type: Object,
        required: true,
    },
});
</script>

<template>
    <Card>
        <CardHeader>
            <CardTitle>{{ course.fullname }}</CardTitle>
            <CardDescription>Course ID: {{ course.id }}</CardDescription>
        </CardHeader>
        <CardContent>
            <p>Start Date: {{ new Date(course.startdate * 1000).toLocaleDateString() }}</p>
            <p>Progress: {{ course.progress }}%</p>
        </CardContent>
        <CardFooter>
            <a :href="course.viewurl" target="_blank">View Course</a>
        </CardFooter>
    </Card>
</template>
