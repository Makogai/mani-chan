<template>
    <div>
        <div class="p-6 sm:px-20 bg-white border-b border-gray-200">
            <div>
                <jet-application-logo class="block h-12 w-auto" />
            </div>

            <div class="mt-8 text-2xl">
                Welcome to your ManiChan App.
            </div>

            <div class="mt-6 text-gray-500">
                This is my personal app for tracking anime. As you can see it's still like just a skeleton, but as time passes by and I put much work into it, it's gonna be super good.
                At least I hope so. at some point in the future I'll probs make it public and available to everyone. My plans for it are huge. So let the time show me the way.
            </div>
        </div>


    </div>
</template>

<script>
    import JetApplicationLogo from '@/Jetstream/ApplicationLogo'

    export default {
        components: {
            JetApplicationLogo,
        },
    }
</script>
