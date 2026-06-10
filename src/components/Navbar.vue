<script>
export default {
    data() {
        return {

        }
    },
    emits: ['switchpages'],
    methods: {
        navigate(page) {
            this.$emit('switchpages', page)
        }
    }
}
</script>
<template>
    <nav class="flex flex-wrap items-center justify-between p-3 bg-stone-300/90 h-30 fixed top-0 w-full px-10 z-1000">
        <div class="text-xl font-['Poppins'] hover:text-amber-950">
            <img class="h-30 w-50 object-cover" src="../assets/images/home.png" alt="">
        </div>
        <div class="flex md:hidden">
            <button id="hamburger">
                <img class="toggle block" src="https://img.icons8.com/fluent-systems-regular/2x/menu-squared-2.png"
                    width="40" height="40" />
                <img class="toggle hidden" src="https://img.icons8.com/fluent-systems-regular/2x/close-window.png"
                    width="40" height="40" />
            </button>
        </div>
        <div
            class=" toggle hidden w-full md:w-auto md:flex text-right text-bold mt-5 md:mt-0 md:border-none cursor-pointer">
            <h1 class="block md:inline-block hover:text-amber-950 px-3 py-3 md:border-none text-xl"
                @click="navigate('Home')">Home
            </h1>

            <h1 class="block md:inline-block hover:text-amber-950 px-3 py-3 md:border-none text-xl"
                @click="navigate('About')">About us
            </h1>
            <h1 class="block md:inline-block hover:text-amber-950 px-3 py-3 md:border-none text-xl"
                @click="navigate('Collect')">Gallery
            </h1>
            <h1 class="block md:inline-block hover:text-amber-950 px-3 py-3 md:border-none text-xl"
                @click="navigate('Visit')">Visit Us
            </h1>
        </div>



        <div class="toggle w-full text-end hidden md:flex md:w-auto px-2 py-2 md:rounded gap-2">
            <div class="flex items-center h-10 w-10 rounded-md bg-[#c8a876] text-white font-medium p-2 ">
                <svg class="w-6 h-6 text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                    width="24" height="24" fill="none" viewBox="0 0 24 24" @click="navigate('Cart')">
                    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M5 4h1.5L9 16m0 0h8m-8 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4Zm8 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4Zm-8.5-3h9.25L19 7h-1M8 7h-.688M13 5v4m-2-2h4" />
                </svg>


            </div>

            <div class="flex justify-end">
                <div class="flex items-center h-10 w-30 rounded-md bg-[#c8a876] text-white font-medium p-2">
                    <!-- Heroicon name: phone -->
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                        stroke="currentColor" class="w-6 h-6">
                        <path stroke-linecap="round" stroke-linejoin="round"
                            d="M2.25 6.75c0 8.284 6.716 15 15 15h2.25a2.25 2.25 0 002.25-2.25v-1.372c0-.516-.351-.966-.852-1.091l-4.423-1.106c-.44-.11-.902.055-1.173.417l-.97 1.293c-.282.376-.769.542-1.21.38a12.035 12.035 0 01-7.143-7.143c-.162-.441.004-.928.38-1.21l1.293-.97c.363-.271.527-.734.417-1.173L6.963 3.102a1.125 1.125 0 00-1.091-.852H4.5A2.25 2.25 0 002.25 4.5v2.25z" />
                    </svg>
                    Call now
                </div>
            </div>
        </div>
    </nav>
</template>