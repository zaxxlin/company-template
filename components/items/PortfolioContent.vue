<template>
    <div class="flex w-screen py-32" id="portfolio">
        <div class="flex flex-col m-auto">
            <div class='text-4xl font-sans tracking-wide pl-10 uppercase text-gray-700 my-8'>
                Portfolio
            </div>
            <div class='flex grid grid-cols-1 md:grid-cols-4 text-gray-700'>
                <slot name='portfolio'></slot>
            </div>
        </div>
    </div>
</template>