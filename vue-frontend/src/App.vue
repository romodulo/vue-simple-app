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
    <div class="custom-self-flex">
        <div class="self_flex-box">
            <div class="self_height-4">
            
            </div>
            <TaskList :propList = "superList" />
            <ul class="self_display-block">
                <h1>{{ variableOne }}</h1>
            </ul>
        </div>
        <div class="definedFlex" v-on:keyup.enter="addTaskToList">
            <input class="definedInputElement"v-model="variableOne">
            <button class="definedInputElement buttonElement" v-on:click="addTaskToList">Submit</button>
            <div class="self_height">
            
            </div>
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