<template>
    <div class="w-screen h-screen relative" id="home">
        <div class="w-screen h-screen bg-fixed" :style="{
            'background-image': `url(${imgURL})`
          }"></div>
        <div class="absolute top-0 w-screen h-screen bg-black bg-opacity-50">
            <div class='flex items-center h-screen'>
                <div class='flex-col m-auto px-10 xl:px-56'>
                    <div class='text-white text-center text-5xl uppercase font-sans tracking-wide font-semibold'>
                        {{header_txt}}
                    </div>
                    <div class='text-white text-center text-3xl uppercase font-sans tracking-wide '>
                        {{second_header}}
                    </div>
                    <div class='text-white text-center text-xl font-sans tracking-wide px-10 lg:px-64'>
                        {{descriptions}}
                    </div>
                </div>
            </div>
        </div>
      </div>
</template>
<script>
export default {
    props: {
        imgURL: {
            type: String,
            default: '/img/slider1.jpeg'
        },
        header_txt: {
            type: String,
            default: ''
        },
        second_header : {
            type: String,
            default : ''
        },
        descriptions : {
            type: String,
            default : ''
        }
    }
}
</script>
