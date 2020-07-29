<template>
    <div class="flex h-2/3 w-screen py-32" id="about">
        <div class="m-auto">
            <div class="flex grid grid-cols-1 md:grid-cols-2 xl:px-56">
                <div class="xl:h-2/3 xl:w-2/3">
                    <img :srcset="imgURL" class='w-full h-full'/>
                </div>
                <div class="flex flex-col w-full p-2 relative">
                    <div class="text-4xl font-sans tracking-wide text-gray-700">
                        ABOUT <span class="font-semibold text-gray-800">US</span>
                    </div>
                    <div class="font-sans text-lg tracking-wide text-gray-600 mt-2 p-1">
                        <slot name='about'></slot>
                    </div>
                    <div class="mt-10">
                        <a href='#contact' class="
                            transition-all
                            duration-500
                            ease-in-out
                            bg-blue-600
                            py-2
                            px-4
                            text-lg
                            font-sans
                            tracking-wide
                            text-gray-200
                            hover:text-white
                            hover:bg-blue-700
                            focus:outline-none 
                            active:outline-none"> Contact Us </a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    props:{
        imgURL :{
            type: String,
            default: '/img/about.jpg'
        }
    }
}
</script>