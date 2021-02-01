<template>
    <section class="text-gray-700 body-font">
        <div class="container px-8 py-48 mx-auto lg:px-4">
            <div class="flex flex-col w-full mb-12 sm:justify-center items-center text-left lg:text-center">
                    <jet-authentication-card-logo />

                <h2 class="mb-1 mt-5 text-xs font-semibold tracking-widest text-blue-600 uppercase title-font">
                    ara ara sup weeabu-kun
                   </h2>
                <h1 class="mb-6 text-2xl font-semibold tracking-tighter text-blue-800 sm:text-5xl title-font">
                    Welcome to ManiChan!
                    <br class="md:hidden">
                    Have a nice staying :D !
                </h1>
                <p class="mx-auto text-base font-medium leading-relaxed text-gray-700 lg:w-2/3">
                    This is my personal anime tracking website. It's still super early development, but it aint that bad heey.
                </p>
            </div>
            <div v-if="canLogin" class="flex lg:justify-center">

                <inertia-link
                    :href="route('dashboard')"
                    v-if="$page.props.user"
                    class="inline-flex items-center px-4 py-2 ml-4 font-semibold text-blue-800 transition duration-500 ease-in-out transform bg-white border rounded-lg shadow-xl hover:border-gray-600 hover:bg-gray-600 hover:text-white focus:shadow-outline focus:outline-none">Dashboard</inertia-link>
                <template v-else>
                    <inertia-link
                        :href="route('login')"
                        class="inline-flex px-4 py-2 font-semibold text-white transition duration-500 ease-in-out transform rounded-lg shadow-xl bg-gradient-to-r from-blue-700 hover:from-blue-600 to-blue-600 hover:to-blue-700 focus:shadow-outline focus:outline-none">Login</inertia-link>
                    <inertia-link
                        :href="route('register')"
                        v-if="canRegister"
                        class="inline-flex items-center px-4 py-2 ml-4 font-semibold text-blue-800 transition duration-500 ease-in-out transform bg-white border rounded-lg shadow-xl hover:border-gray-600 hover:bg-gray-600 hover:text-white focus:shadow-outline focus:outline-none">Register</inertia-link>
                </template>
            </div>
        </div>
    </section>



</template>

<style scoped>
    .bg-gray-100 {
        background-color: #f7fafc;
        background-color: rgba(247, 250, 252, var(--tw-bg-opacity));
    }

    .border-gray-200 {
        border-color: #edf2f7;
        border-color: rgba(237, 242, 247, var(--tw-border-opacity));
    }

    .text-gray-400 {
        color: #cbd5e0;
        color: rgba(203, 213, 224, var(--tw-text-opacity));
    }

    .text-gray-500 {
        color: #a0aec0;
        color: rgba(160, 174, 192, var(--tw-text-opacity));
    }

    .text-gray-600 {
        color: #718096;
        color: rgba(113, 128, 150, var(--tw-text-opacity));
    }

    .text-gray-700 {
        color: #4a5568;
        color: rgba(74, 85, 104, var(--tw-text-opacity));
    }

    .text-gray-900 {
        color: #1a202c;
        color: rgba(26, 32, 44, var(--tw-text-opacity));
    }

    @media (prefers-color-scheme: dark) {
        .dark\:bg-gray-800 {
            background-color: #2d3748;
            background-color: rgba(45, 55, 72, var(--tw-bg-opacity));
        }

        .dark\:bg-gray-900 {
            background-color: #1a202c;
            background-color: rgba(26, 32, 44, var(--tw-bg-opacity));
        }

        .dark\:border-gray-700 {
            border-color: #4a5568;
            border-color: rgba(74, 85, 104, var(--tw-border-opacity));
        }

        .dark\:text-white {
            color: #fff;
            color: rgba(255, 255, 255, var(--tw-text-opacity));
        }

        .dark\:text-gray-400 {
            color: #cbd5e0;
            color: rgba(203, 213, 224, var(--tw-text-opacity));
        }
    }
</style>

<script>
import JetAuthenticationCardLogo from '@/Jetstream/AuthenticationCardLogo'
    export default {
        props: {
            canLogin: Boolean,
            canRegister: Boolean,
            laravelVersion: String,
            phpVersion: String,
        },
        components: {
            JetAuthenticationCardLogo
        }
    }

</script>
