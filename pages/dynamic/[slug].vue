<template>
    <PageWrapper>
    <div>
        <p>Im dynamic</p>
        <p>{{ data.title }}</p>
        <p v-if="error">{{ error }}</p>
    </div>
</PageWrapper>
</template>

<script setup>

const route = useRoute()
const { data } = await useAsyncData(route.name, () => queryContent(route.fullPath).findOne())

    if (!data.value.title) {
        throw createError({ statusCode: 404, statusMessage: 'Page Not Found' })
    }

</script>