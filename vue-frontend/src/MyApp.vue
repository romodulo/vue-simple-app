<script setup>
import { ref } from 'vue'

const variableOne = ref("text-input")

const functionDefinition = () => {return variableOne.value = ""}

</script>

<template>
    <div class="definedFlex">
        <h1>{{ variableOne }}</h1>
        <input class="definedInputElement"v-model="variableOne">
        <button class="definedInputElement buttonElement" v-on:click="functionDefinition">Submit</button>
    </div>
</template>

<style scoped>
.definedFlex {
    display: flex;
    flex-direction: column;
}
.definedInputElement {
    /* display: block; */
    height: 48px;
    margin-top: 3px;
}
.buttonElement {
    margin-top: 7px;
}
</style>