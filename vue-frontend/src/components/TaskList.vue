<script setup>
defineProps({
    propList : {
        type: Array,
    },
})
</script>

<template>
    <!-- <h1>{{ propList }}</h1> -->
     <!-- <div class="custom-self-flex _temp-self-scoped"> -->
     <div>
        <ul>
            <li v-for="item in propList" ><h1>{{ item }}</h1></li>
        </ul>
     </div>
</template>

