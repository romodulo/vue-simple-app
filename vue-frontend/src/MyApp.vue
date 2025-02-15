<script setup>
import { ref } from 'vue'
import TaskList from './components/TaskList.vue'


const variableOne = ref("text-input")
// deprecated
// const functionDefinition = () => {return variableOne.value = ""}
const superList = ref([])
const addTaskToList = () => {superList.value.push(variableOne.value); variableOne.value = "";}

</script>

<template>
    <div>
        <TaskList :propList = "superList" />
        <h1 class="custom-self-flex _temp-self-scoped">{{ variableOne }}</h1>
        <div class="definedFlex" v-on:keyup.enter="addTaskToList">
            <input class="definedInputElement"v-model="variableOne">
            <button class="definedInputElement buttonElement" v-on:click="addTaskToList">Submit</button>
        </div>
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