<script setup>
import { ref } from 'vue'

const variableOne = ref("test-variable")

</script>

<template>
    <h1>{{ variableOne }}</h1>
</template>