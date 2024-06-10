<template>
    <div class="container">
        <h1>QR Generator</h1>
        <div class="form">
            <input type="text" placeholder="URL or Text to generate" />
            <button>Generate</button>
        </div>
    </div>
</template>

<script setup></script>

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
</style>
