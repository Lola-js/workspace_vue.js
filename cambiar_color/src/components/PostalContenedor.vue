<template>

    <div class="post-container">
        <PostalCarta />
        <PostalCarta />
        <PostalCarta />
        <PostalCarta />
    </div>
    
    </template>
    
    <script setup>
        import PostalCarta from './PostalCarta.vue'
    </script>
    
    <style>
        .post-container{
            width: 100%;
            display: flex;
            flex-wrap: wrap;
        }
    
    </style>    