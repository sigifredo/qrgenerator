<template>
    <div class="container">
        <h1>QR Generator</h1>
        <div class="form">
            <input type="text" v-model="value2generate" placeholder="URL or Text to generate" />
            <button @click="generate">Generate</button>
            <p v-if="errorMessage" class="alert alert-danger" role="alert">{{ errorMessage }}</p>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const errorMessage = ref('');
const value2generate = ref('');

const generate = () => {
    if (value2generate.value.trim() === '') {
        errorMessage.value = `El campo de texto no puede estar vacío.`;
    } else {
        // generar QR
    }
};
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300..800;1,300..800&display=swap');

body,
html {
    margin: 0;
    padding: 0;
    font-family: 'Open Sans', sans-serif;
}
*,
*::before,
*::after {
    box-sizing: border-box;
}
input {
    font-size: 1.1em;
    padding: 0.5em 1em;
}
.alert {
    border: 1px solid transparent;
    border-radius: 0.25rem;
    margin-bottom: 1rem;
    padding: 0.75rem 1.25rem;
    position: relative;

    &.alert-danger {
        background-color: #f8d7da;
        border-color: #f5c6cb;
        color: #721c24;
    }
}
.container {
    margin-left: auto;
    margin-right: auto;
    padding-left: 15px;
    padding-right: 15px;
    width: 100%;

    @media (min-width: 576px) {
        max-width: 540px;
    }
    @media (min-width: 768px) {
        max-width: 720px;
    }
    @media (min-width: 992px) {
        max-width: 960px;
    }
    @media (min-width: 1200px) {
        max-width: 1140px;
    }
}
.form {
    align-items: center;
    display: flex;
    flex-direction: column;
    gap: 1em;
}
</style>
