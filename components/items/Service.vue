<template>
    <div class="flex flex-col transition-all duration-500 ease-in-out items-center px-2 py-12 hover:shadow-2xl cursor-pointer">
        <div class="h-22 my-4">
            <img :srcset='imgURL' class="w-full h-full"/>
        </div>
        <div class="font-sans text-lg font-semibold tracking-wide text-center my-2">
            {{title}}
        </div>
        <div class="font-sans tracking-wide text-center">
            <slot name="content"></slot>
        </div>
    </div>
</template>
<script>
export default {
    props:{
        imgURL : {
            type: String,
            default: '/img/icon1.png'
        },
        title : {
            type: String,
            default: 'Title'
        }
    }
}
</script>