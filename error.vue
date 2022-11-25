<template>
<div>
    <div 
    class="error"
    v-if="error.statusCode === 404 || '404'"
    >
        <div>Oohhpss lost</div>
        <button @click="handleError">back home c:</button>
        <p>Error {{ error.statusCode }}</p>
    </div>
</div>
</template>

<script lang="ts" setup>
import { defineProps } from 'vue';

defineProps({
	error: {
		type: Object,
		required: true,
	},
});

// clear error and redirect to home page
const handleError = () => clearError({ redirect: '/' });
</script>

<style>
.error {
    background-color: tomato;
    height: 100vh;
    width: 100%;
    font-size: 100px;
}
</style>
