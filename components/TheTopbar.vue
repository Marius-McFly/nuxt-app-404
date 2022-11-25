<template>
<div class="topbar">
    <div class="flex">
        <p>I'm the topbar</p>
        <a href="/">home</a>
        <a href="/about">about</a>
    </div>
</div>
</template>

<style>
.topbar {
    background-color: grey;
    text-align: center;
    height: 80px;
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