<template>
    <div class="flex h-2/3 w-screen py-32" id="service">
        <div class="m-auto">
            <div class="flex grid grid-cols-1 md:grid-cols-4 px-5 text-gray-700">
                <slot name="services"></slot>
            </div>
        </div>
    </div>
</template>