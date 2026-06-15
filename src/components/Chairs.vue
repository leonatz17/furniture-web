<script>
import Chaircart from './Chaircart.vue';
export default{
    components:{
        Chaircart
    },
    data (){
        return{
             chairs: [
                {
                    id: 1,
                    img: 'https://img5.su-cdn.com/cdn-cgi/image/width=750,height=750/mall/file/2024/01/11/cfa30498d3104dd5024ccb33b0cc3e20.jpg',
                    price: '₱2,000',
                    name: ' Mid-Century Dining Chair',
                    description: 'A grand, heirloom-quality centerpiece for family feasts'
                },
                {
                    id: 2,
                    img: 'https://www.thebrick.com/cdn/shop/products/78617_my_brick_home21323_1500x.jpg?v=1751053851',
                    price: '₱6,500',
                    name: 'Velvet Accent Chair',
                    description: 'Cozy and compact, ideal for small living spaces.'
                },
                {
                    id: 3,
                    img: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSZpHqmOSVaGenzmntD5xaehPvjc65XOLOkJA&s',
                    price: '₱5,500 ',
                    name: 'Ergonomic Office Chair',
                    description: 'The centerpiece of your living room; built for family gatherings.'
                },
                {
                    id: 4,
                    img: 'https://i5.walmartimages.com/seo/Top-Leather-Lounge-Chair-with-Ottoman-Mid-Century-Recline-Accent-Chair-Upholstered-for-Living-Room_f1a6be0e-de9a-4efb-8bd9-2ff8cec701b2.54cb79ab87c6d1bc5cfe7dee59847a60.jpeg',
                    price: '₱10,000',
                    name: ' Leather Lounge Chair',
                    description: 'Designed for lounging; perfect for movie nights and hosting.'
                },
                {
                    id: 5,
                    img: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSaS3JKY7YuLFYm4RjKrmPeSo-U30xVPzT3vA&s',
                    price: '₱5,500',
                    name: ' Scandinavian Armchair',
                    description: 'Seamlessly converts from a stylish sofa to a comfy guest bed.'
                },
                {
                    id: 6,
                    img: 'https://m.media-amazon.com/images/I/81Xpi50p1aL._AC_UF1000,1000_QL80_.jpg',
                    price: '₱5,600',
                    name: 'Wingback Chair',
                    description: 'A versatile, space-saving essential for modern studios.'
                },
                {
                    id: 7,
                    img: 'https://thronekingdom.com/cdn/shop/files/Clover_Chair_02_45f3524e-9834-4764-ac77-9d4d0a728181.jpg?v=1729014288&width=807',
                    price: '₱5,000',
                    name: 'Rattan Accent Chair',
                    description: 'Timeless, hand-tufted elegance for a sophisticated home.'
                },
                {
                    id: 8,
                    img: 'https://www.designstory.com.ph/cdn/shop/files/AA599-A2191_Hee_Bar_Stool_low_black_64203fda-24a1-4305-902a-c131a2c9684c_650x.jpg?v=1714118512',
                    price: '₱2,000',
                    name: 'Bar Stool',
                    description: 'Ultimate relaxation with adjustable support for your back.'
                },
                {
                    id: 9,
                    img: 'https://m.media-amazon.com/images/I/41Wvz3BGiSL._AC_US1000_.jpg',
                    price: '₱3,000',
                    name: 'Folding Guest Chair',
                    description: 'Luxury comfort where every seat is the best in the house.'
                },
                {
                    id: 10,
                    img: 'https://woodentwist.com/cdn/shop/products/honey.jpg?v=1743268855',
                    price: '₱4,000',
                    name: 'Rocking Chair',
                    description: 'Clean lines and iconic style for the design-conscious.'
                },
                {
                    id: 11,
                    img: 'https://images.thdstatic.com/productImages/0df83a30-57d3-4453-adfc-8bf2a005fbfd/svn/light-grey-and-walnut-brown-baxton-studio-ottomans-233-13323-hd-31_600.jpg',
                    price: '₱2,000',
                    name: 'Ottoman/Pouffe',
                    description: 'Defined by soft, loose cushions for laid-back comfort.'
                },
                {
                    id: 12,
                    img: 'https://afhomeph.com/cdn/shop/files/IdaBoothBench-IdaBoothBenchLightGray3-20230503-114832.jpg?v=1750304699&width=1214',
                    price: '₱17,000',
                    name: 'Bench Seat',
                    description: 'Elegant and slim-profile seating that fits any corner.'
                },
            ],
            chairproducts:false,
            chairitems : true,
            currentIndex: 0
        }
    },
    methods:{
        buyChairs(index){
            this.currentIndex = index;
            this.chairproducts = true;
            this.chairitems = false

        },
        addCart(chairs) {
            this.$emit('addtableCart', { ...chairs })
        },
    }
}
</script>
<template>
    <div v-if="chairitems" class="bg-stone-600/90">
        <section class="container mx-auto p-10 md:py-12 px-0 md:p-8 md:px-0">
            <div class="h-30 w-full">
            </div>
            <div class="h-10 w-full px-10">
                <h1 class="text-2xl font-['Poppins'] font-bold text-amber-950">> Chairs Collection</h1>
            </div>
            <section
                class="p-5 md:p-0 grid grid-cols-1 sm:grid-cols-1 md:grid-cols-2 xl:grid-cols-3 2xl:grid-cols-4 gap-10 items-start "
                >
                <section v-for="(chair,index) in chairs" :key="chair.id"
                    class="p-5 py-10  text-center transform duration-500 hover:-translate-y-2 cursor-pointer hover:bg-stone-300" @click="buyChairs(index)">
                    <img class="w-full h-60" :src="chair.img" alt="">
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
                    <h1 class="text-xl font-bold text-amber-950 font-['Poppins'] my-3">{{ chair.name }}</h1>

                    <h2 class=" text-xl font-bold text-amber-950 font-['Poppins'] my-3">{{ chair.price }}.00</h2>
                    <button class="p-2 px-6 bg-amber-800 text-white rounded-md hover:bg-[#c09858] cursor-pointer"
                        @click="buyChairs(index)">Add To
                        Cart</button>
                </section>
            </section>
        </section>
    </div>
    <Chaircart v-if="chairproducts" :selectedChairitems="chairs[currentIndex]" />
</template>