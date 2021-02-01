<template>
    <div class="min-h-screen flex flex-col sm:justify-center items-center pt-6 sm:pt-0 bga-gray-900" style="
    background-image: url('https://cutewallpaper.org/21/hd-gifs-wallpaper/Gifs-Anime-1920x1080-Ryanmartinproductions.com.gif');
    background-repeat: no-repeat;
    background-size: cover;
    ">
        <div>
            <slot name="logo" />
        </div>

        <div class="w-full sm:max-w-md mt-6 px-6 py-4 bg-gray-700 shadow-md overflow-hidden sm:rounded-lg">
            <slot />
        </div>
    </div>
</template>
