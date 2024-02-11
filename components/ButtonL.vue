<template>
    <button class="px-[14px] py-2">{{props.title}}</button>
</template>

<script setup>
    const props = defineProps({
        title :{
            type:String,
            default:'',
        }
    })
</script>