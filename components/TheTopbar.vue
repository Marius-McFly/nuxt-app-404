<template>
<div class="topbar">
    <div class="flex">
        <p>I'm the topbar</p>
        <a href="/">home</a>
        <a href="/about">about</a>
        <a href="/dynamic">dynamic</a>
        <a v-for="item in data" :href="item._path">{{ item._path }}</a>
    </div>
    
</div>
</template>

<script setup>
const route = useRoute()
const { data } = await useAsyncData(route.name, () => queryContent('/').find())
</script>

<style>
.topbar {
    background-color: grey;
    text-align: center;
    width: 100%;
    display: flex;
    justify-items: center;
    align-items: center;
}

p {
    margin-right: 40px;
    font-size: 32px;
}

.flex {
    display: flex;
    justify-items: center;
    width: 100%;
}

a {
    margin-right: 20px;
    font-size: 24px;
}
</style>