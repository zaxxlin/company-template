<template>
    <div class="flex w-screen h-64 bg-gray-800" id="contact">
        <div class="m-auto p-2">
            <div class="flex flex-col items-center">
                <div class="h-full w-40 my-5">
                    <img :srcset="imgURL"  class="w-full h-full"/>
                </div>
                <div class="text-white font-sans text-center">
                    <p>{{address}}</p>
                    <p>{{email}}</p>
                    <p>{{phone}}</p>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    props: {
        address : {
            type: String,
            default: ''
        },
        phone : {
            type: String,
            default: ''
        },
        email : {
            type: String,
            default: ''
        },
        imgURL : {
            type: String,
            default: '/img/lead-white-logo.png'
        }
    }
}
</script>