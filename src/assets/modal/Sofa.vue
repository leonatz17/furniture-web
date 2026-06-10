<script>
import Cart from './Cart.vue';
export default {
    components: {
        Cart
    },
    data() {
        return {
            sofa: [
                {
                    id: 1,
                    img: 'https://image.made-in-china.com/202f0j00rCcqAQUKfHkF/Italian-Luxury-Modern-Design-1-Seater-Sofa-Lazy-Arm-Chair-Lounge-Living-Room-Wing-Accent-Chair.jpg',
                    price: '₱3,500',
                    name: '1-Seater / Armchair',
                    description: 'The perfect "me-time" spot for reading or coffee.'
                },
                {
                    id: 2,
                    img: 'https://ak1.ostkcdn.com/images/products/is/images/direct/82f0794456f723b6a445d6628df587e981010846/2-Seater-Loveseat-Sofa-with-Wood-Frame-for-Small-Spaces%2C-Versatile-Sofa-Settee-Upholstered-Sofa-with-2-Pillows.jpg?imwidth=714&impolicy=medium&carousel=true',
                    price: '₱8,500',
                    name: '2-Seater (Loveseat)',
                    description: 'Cozy and compact, ideal for small living spaces.'
                },
                {
                    id: 3,
                    img: 'https://www.furnituresourcephils.com/wp-content/uploads/2023/05/040426139-min.jpg',
                    price: '₱15,000',
                    name: '3-Seater Sofa',
                    description: 'The centerpiece of your living room; built for family gatherings.'
                },
                {
                    id: 4,
                    img: 'https://afhomeph.com/cdn/shop/files/gino_2_2.png?v=1749447563&width=1214',
                    price: '₱18,000',
                    name: 'L-Shape Sectional Sofa',
                    description: 'Designed for lounging; perfect for movie nights and hosting.'
                },
                {
                    id: 5,
                    img: 'https://www.furnituresourcephils.com/wp-content/uploads/2019/10/BrinkoffDG1.jpg',
                    price: '₱19,000',
                    name: 'Pull-Out Sofa Bed',
                    description: 'Seamlessly converts from a stylish sofa to a comfy guest bed.'
                },
                {
                    id: 6,
                    img: 'https://www.meubles.ie/images/products/standard/23200_3823216.jpg',
                    price: '₱3,000',
                    name: 'Futon Sofa Bed',
                    description: 'A versatile, space-saving essential for modern studios.'
                },
                {
                    id: 7,
                    img: 'https://dantefurniture.co.uk/cdn/shop/files/dante_furniture_chesterfield_blue_3_seater_sofa.png?v=1772538153&width=2156',
                    price: '₱30,000',
                    name: 'Chesterfield Sofa',
                    description: 'Timeless, hand-tufted elegance for a sophisticated home.'
                },
                {
                    id: 8,
                    img: 'https://m.media-amazon.com/images/I/61BdXjWZLiL._AC_UF894,1000_QL80_.jpg',
                    price: '₱12,000',
                    name: 'Reclining Sofa (Single)',
                    description: 'Ultimate relaxation with adjustable support for your back.'
                },
                {
                    id: 9,
                    img: 'https://www.nilkamalhomes.com/cdn/shop/files/DERIK_3STR_RCL_LS2_02c38fda-0229-48c4-9e18-ece6212b6ed3.jpg?v=1725355507&width=1214',
                    price: '₱35,000',
                    name: '3-Seater Reclining Sofa',
                    description: 'Luxury comfort where every seat is the best in the house.'
                },
                {
                    id: 10,
                    img: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSWtemqmjy8477eObf76-C3nTbpJZT1dhzFBA&s',
                    price: '₱15,000',
                    name: 'Mid-Century Modern Sofa',
                    description: 'Clean lines and iconic style for the design-conscious.'
                },
                {
                    id: 11,
                    img: 'https://homeu.ph/cdn/shop/products/lawson8_1d178b3c-b4d9-4c06-a390-e16baecca614.jpg?v=1620960669',
                    price: '₱12,000',
                    name: 'Lawson Sofa',
                    description: 'Defined by soft, loose cushions for laid-back comfort.'
                },
                {
                    id: 12,
                    img: 'https://cdn.arhaus.com/product/images/ZTGFSEE_FN250521.jpg?preset=pdp',
                    price: '₱7,000',
                    name: 'Settee',
                    description: 'Elegant and slim-profile seating that fits any corner.'
                },
            ],
            currentIndex: 0,
            sofaItems: false,
            items:true,
        }

    },
    emits: ['addCart'],
    methods: {
        buySofa(index) {
            this.currentIndex = index;
            this.sofaItems = true
            this.items = false;
        },
        addCart(sofa) {
            this.$emit('addCart', { ...sofa })
            


        }
    }
}
</script>
<template>
    <div v-if="items" class="bg-stone-600/90">
        <section class="container mx-auto p-10 md:py-12 px-0 md:p-8 md:px-0">
            <div class="h-30 w-full">
            </div>
            <div class="h-10 w-full px-10">
                <h1 class="text-2xl font-['Poppins'] font-bold text-amber-950">> Sofa Collection</h1>
            </div>
            <section
                class="p-5 md:p-0 grid grid-cols-1 sm:grid-cols-1 md:grid-cols-2 xl:grid-cols-3 2xl:grid-cols-4 gap-10 items-start "
                @click="buySofa(index)">
                <section v-for="(sofas, index) in sofa" :key="sofas.id"
                    class="p-5 py-10  text-center transform duration-500 hover:-translate-y-2 cursor-pointer hover:bg-stone-300">
                    <img class="w-full h-60" :src="sofas.img" alt="">
                    <div class="space-x-1 flex justify-center mt-10">
                        <svg class="w-4 h-4 mx-px fill-current text-orange-600" xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 14 14">
                            <path
                                d="M6.43 12l-2.36 1.64a1 1 0 0 1-1.53-1.11l.83-2.75a1 1 0 0 0-.35-1.09L.73 6.96a1 1 0 0 1 .59-1.8l2.87-.06a1 1 0 0 0 .92-.67l.95-2.71a1 1 0 0 1 1.88 0l.95 2.71c.13.4.5.66.92.67l2.87.06a1 1 0 0 1 .59 1.8l-2.3 1.73a1 1 0 0 0-.34 1.09l.83 2.75a1 1 0 0 1-1.53 1.1L7.57 12a1 1 0 0 0-1.14 0z">
                            </path>
                        </svg>
                        <svg class="w-4 h-4 mx-px fill-current text-orange-600" xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 14 14">
                            <path
                                d="M6.43 12l-2.36 1.64a1 1 0 0 1-1.53-1.11l.83-2.75a1 1 0 0 0-.35-1.09L.73 6.96a1 1 0 0 1 .59-1.8l2.87-.06a1 1 0 0 0 .92-.67l.95-2.71a1 1 0 0 1 1.88 0l.95 2.71c.13.4.5.66.92.67l2.87.06a1 1 0 0 1 .59 1.8l-2.3 1.73a1 1 0 0 0-.34 1.09l.83 2.75a1 1 0 0 1-1.53 1.1L7.57 12a1 1 0 0 0-1.14 0z">
                            </path>
                        </svg>
                        <svg class="w-4 h-4 mx-px fill-current text-orange-600" xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 14 14">
                            <path
                                d="M6.43 12l-2.36 1.64a1 1 0 0 1-1.53-1.11l.83-2.75a1 1 0 0 0-.35-1.09L.73 6.96a1 1 0 0 1 .59-1.8l2.87-.06a1 1 0 0 0 .92-.67l.95-2.71a1 1 0 0 1 1.88 0l.95 2.71c.13.4.5.66.92.67l2.87.06a1 1 0 0 1 .59 1.8l-2.3 1.73a1 1 0 0 0-.34 1.09l.83 2.75a1 1 0 0 1-1.53 1.1L7.57 12a1 1 0 0 0-1.14 0z">
                            </path>
                        </svg>
                        <svg class="w-4 h-4 mx-px fill-current text-orange-600" xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 14 14">
                            <path
                                d="M6.43 12l-2.36 1.64a1 1 0 0 1-1.53-1.11l.83-2.75a1 1 0 0 0-.35-1.09L.73 6.96a1 1 0 0 1 .59-1.8l2.87-.06a1 1 0 0 0 .92-.67l.95-2.71a1 1 0 0 1 1.88 0l.95 2.71c.13.4.5.66.92.67l2.87.06a1 1 0 0 1 .59 1.8l-2.3 1.73a1 1 0 0 0-.34 1.09l.83 2.75a1 1 0 0 1-1.53 1.1L7.57 12a1 1 0 0 0-1.14 0z">
                            </path>
                        </svg>
                        <svg class="w-4 h-4 mx-px fill-current text-gray-300" xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 14 14">
                            <path
                                d="M6.43 12l-2.36 1.64a1 1 0 0 1-1.53-1.11l.83-2.75a1 1 0 0 0-.35-1.09L.73 6.96a1 1 0 0 1 .59-1.8l2.87-.06a1 1 0 0 0 .92-.67l.95-2.71a1 1 0 0 1 1.88 0l.95 2.71c.13.4.5.66.92.67l2.87.06a1 1 0 0 1 .59 1.8l-2.3 1.73a1 1 0 0 0-.34 1.09l.83 2.75a1 1 0 0 1-1.53 1.1L7.57 12a1 1 0 0 0-1.14 0z">
                            </path>
                        </svg>
                    </div>
                    <h1 class="text-xl font-bold text-amber-950 font-['Poppins'] my-3">{{ sofas.name }}</h1>

                    <h2 class=" text-xl font-bold text-amber-950 font-['Poppins'] my-3">{{ sofas.price }}.00</h2>
                    <button class="p-2 px-6 bg-amber-800 text-white rounded-md hover:bg-[#c09858] cursor-pointer"
                        @click="buySofa(index)">Add To
                        Cart</button>
                </section>
            </section>
        </section>
    </div>
    <Cart v-if="sofaItems" :selecteditems="sofa[currentIndex]"/>
</template>