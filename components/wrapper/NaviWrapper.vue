<template>
    <div class="absolute z-10 top-0 w-screen h-22">
        <div class="flex justify-between w-screen h-full py-6 px-8 bg-black bg-opacity-25" v-if='!show'>
            <div class='h-full w-32'>
                <img :srcset="imgURL" class="h-full w-full"/>
            </div>
            <div>
                <button type="button" class="focus:outline-none active:outline:none" @click='toggleMenu'>
                    <svg class="h-8 w-8" fill="#000000" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" ><path id='cross' d="M 0 2 L 0 4 L 24 4 L 24 2 Z M 0 11 L 0 13 L 24 13 L 24 11 Z M 0 20 L 0 22 L 24 22 L 24 20 Z"/></svg>
                </button>
            </div>
        </div>
        <div class='flex h-screen w-full bg-black bg-opacity-75' v-else>
            <div class="flex flex-col m-auto z-20 items-center">
                <div class='text-white text-4xl upppercase font-sans font-semibold tracking-wide my-4'>
                    <a href="#home" @click="toggleMenu">HOME</a>
                    </div>
                <div class='text-white text-4xl upppercase font-sans font-semibold tracking-wide my-4'>
                    <a href="#about" @click="toggleMenu">ABOUT</a>
                </div>
                <div class="flex items-center">
                    <div class='text-white text-4xl upppercase font-sans font-semibold tracking-wide my-4'>
                        <a href="#service" @click="toggleMenu">SERVICE</a>
                    </div>
                    <div class="flex items-center">
                        <button type="button" class="focus:outline-none active:outline-none" @click='toggleMenu'>
                            <svg class="h-8 w-8 ml-5 -mr-12" version="1.1" id="Capa_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
                                viewBox="0 0 512.001 512.001" style="enable-background:new 0 0 512.001 512.001;" xml:space="preserve">
                                <g><g><path id='cross' d="M284.286,256.002L506.143,34.144c7.811-7.811,7.811-20.475,0-28.285c-7.811-7.81-20.475-7.811-28.285,0L256,227.717
                                        L34.143,5.859c-7.811-7.811-20.475-7.811-28.285,0c-7.81,7.811-7.811,20.475,0,28.285l221.857,221.857L5.858,477.859
                                        c-7.811,7.811-7.811,20.475,0,28.285c3.905,3.905,9.024,5.857,14.143,5.857c5.119,0,10.237-1.952,14.143-5.857L256,284.287
                                        l221.857,221.857c3.905,3.905,9.024,5.857,14.143,5.857s10.237-1.952,14.143-5.857c7.811-7.811,7.811-20.475,0-28.285
                                        L284.286,256.002z"/></g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g>
                            </svg>
                        </button>
                    </div>
                </div>
                <div class='text-white text-4xl upppercase font-sans font-semibold tracking-wide my-4'>
                    <a href="#portfolio" @click="toggleMenu">PORTFOLIO</a>
                </div>
                <div class='text-white text-4xl upppercase font-sans font-semibold tracking-wide my-4'>
                    <a href="#contact" @click="toggleMenu">CONTACT</a>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    props:{
        imgURL: {
            type: String,
            default: '/img/lead-white-logo.png'
        }
    },
    data : function(){
        return {
            show: false
        }
    },
    methods: {
        toggleMenu() {
            this.show = !this.show
        }
    }
}
</script>
<style >
    #cross{
        fill: white;
    }
</style>