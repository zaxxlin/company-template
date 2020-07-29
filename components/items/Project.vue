<template>
    <div class="relative cursor-pointer">
        <a :href="projectURL" target="_blank" class="hover:outline-none active:outline-none">
        <div class="block overflow-hidden">
            <img :class="{
            'transition':true, 
            'duration-500':true, 
            'ease-in-out':true, 
            'transform':true,
            '-translate-y-1':hover,
            'scale-125':hover,
            'object-cover':true,
            }" :srcset="imgURL" />
        </div>
        <div class="absolute w-full h-full top-0" @mouseover="hover=true" @mouseleave="hover=false">
            <div :class="{
                'flex': true,
                'h-full': true,
                'transition':true, 
                'duration-500':true, 
                'ease-in-out':true, 
                'product-hover': hover
                }">
                <div class="my-auto px-10" v-if="hover">
                    <div class="text-white font-bold text-3xl md:text-xl font-sans tracking-wide">
                        {{name}}
                    </div>
                    <div class="text-white font-light text-md font-sans">
                        {{project}}
                    </div>
                </div>
            </div>
        </div>
        </a>
    </div>
</template>
<script>
export default {
    data: () => {
        return {
            hover: false
        }
    },
    props: {
        imgURL: {
            type: String,
            default : '../img/github.png'
        },
        name: {
            type: String,
            default : 'Project Name'
        },
        project : {
            type: String,
            default : 'Project Type'
        },
        projectURL : {
            type: String,
            default : 'project url'
        }
    }
}
</script>
<style>
.product-hover{
    background-color: rgba(0, 0, 0, 0.452)
}
</style>