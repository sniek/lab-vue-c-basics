<script setup>
import { ref } from 'vue';

const myObject = ref([{
    title: 'Oppenheimer',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur, laborum. Officiis dicta corporis aperiam asperiores? Ullam, minima. Sapiente ea repellendus tenetur exercitationem, aut pariatur consequatur, atque quos a repudiandae itaque.'
},
{
    title: 'Inception',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur, laborum. Officiis dicta corporis aperiam asperiores? Ullam, minima. Sapiente ea repellendus tenetur exercitationem, aut pariatur consequatur, atque quos a repudiandae itaque.'
},
{
    title: 'Interstellar',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur, laborum. Officiis dicta corporis aperiam asperiores? Ullam, minima. Sapiente ea repellendus tenetur exercitationem, aut pariatur consequatur, atque quos a repudiandae itaque.'
}])

</script>

<template>
    <h2>This is the iteration 4 component</h2>
    <ul>
        <li v-for="(item, index) in myObject">
            {{ index }} 
            - {{ item.title }} 
            - {{ item.description }}
            - {{ item.content }}
        </li>
    </ul>
</template>

<style>
</style>