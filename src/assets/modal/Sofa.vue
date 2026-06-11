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
                {
                    id: 13,
                    img: 'https://img5.su-cdn.com/cdn-cgi/image/width=750,height=750/mall/file/2024/01/11/cfa30498d3104dd5024ccb33b0cc3e20.jpg',
                    price: '₱2,000',
                    name: ' Mid-Century Dining Chair',
                    description: 'A grand, heirloom-quality centerpiece for family feasts'
                },
                {
                    id: 14,
                    img: 'https://www.thebrick.com/cdn/shop/products/78617_my_brick_home21323_1500x.jpg?v=1751053851',
                    price: '₱6,500',
                    name: 'Velvet Accent Chair',
                    description: 'Cozy and compact, ideal for small living spaces.'
                },
                {
                    id: 15,
                    img: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSZpHqmOSVaGenzmntD5xaehPvjc65XOLOkJA&s',
                    price: '₱5,500 ',
                    name: 'Ergonomic Office Chair',
                    description: 'The centerpiece of your living room; built for family gatherings.'
                },
                {
                    id: 16,
                    img: 'https://i5.walmartimages.com/seo/Top-Leather-Lounge-Chair-with-Ottoman-Mid-Century-Recline-Accent-Chair-Upholstered-for-Living-Room_f1a6be0e-de9a-4efb-8bd9-2ff8cec701b2.54cb79ab87c6d1bc5cfe7dee59847a60.jpeg',
                    price: '₱10,000',
                    name: ' Leather Lounge Chair',
                    description: 'Designed for lounging; perfect for movie nights and hosting.'
                },
                {
                    id: 17,
                    img: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSaS3JKY7YuLFYm4RjKrmPeSo-U30xVPzT3vA&s',
                    price: '₱5,500',
                    name: ' Scandinavian Armchair',
                    description: 'Seamlessly converts from a stylish sofa to a comfy guest bed.'
                },
                {
                    id: 18,
                    img: 'https://m.media-amazon.com/images/I/81Xpi50p1aL._AC_UF1000,1000_QL80_.jpg',
                    price: '₱5,600',
                    name: 'Wingback Chair',
                    description: 'A versatile, space-saving essential for modern studios.'
                },
                {
                    id: 19,
                    img: 'https://thronekingdom.com/cdn/shop/files/Clover_Chair_02_45f3524e-9834-4764-ac77-9d4d0a728181.jpg?v=1729014288&width=807',
                    price: '₱5,000',
                    name: 'Rattan Accent Chair',
                    description: 'Timeless, hand-tufted elegance for a sophisticated home.'
                },
                {
                    id: 20,
                    img: 'https://www.designstory.com.ph/cdn/shop/files/AA599-A2191_Hee_Bar_Stool_low_black_64203fda-24a1-4305-902a-c131a2c9684c_650x.jpg?v=1714118512',
                    price: '₱2,000',
                    name: 'Bar Stool',
                    description: 'Ultimate relaxation with adjustable support for your back.'
                },
                {
                    id: 21,
                    img: 'https://m.media-amazon.com/images/I/41Wvz3BGiSL._AC_US1000_.jpg',
                    price: '₱3,000',
                    name: 'Folding Guest Chair',
                    description: 'Luxury comfort where every seat is the best in the house.'
                },
                {
                    id: 22,
                    img: 'https://woodentwist.com/cdn/shop/products/honey.jpg?v=1743268855',
                    price: '₱4,000',
                    name: 'Rocking Chair',
                    description: 'Clean lines and iconic style for the design-conscious.'
                },
                {
                    id: 23,
                    img: 'https://images.thdstatic.com/productImages/0df83a30-57d3-4453-adfc-8bf2a005fbfd/svn/light-grey-and-walnut-brown-baxton-studio-ottomans-233-13323-hd-31_600.jpg',
                    price: '₱2,000',
                    name: 'Ottoman/Pouffe',
                    description: 'Defined by soft, loose cushions for laid-back comfort.'
                },
                {
                    id: 24,
                    img: 'https://afhomeph.com/cdn/shop/files/IdaBoothBench-IdaBoothBenchLightGray3-20230503-114832.jpg?v=1750304699&width=1214',
                    price: '₱17,000',
                    name: 'Bench Seat',
                    description: 'Elegant and slim-profile seating that fits any corner.'
                },
                {
                    id: 25,
                    img: 'https://gulnatural.com/cdn/shop/collections/solid-wood-dining-tables.jpg?v=1708699881',
                    price: '₱20,000',
                    name: 'Solid Wood Dining Table',
                    description: 'A grand, heirloom-quality centerpiece for family feasts'
                },
                {
                    id: 26,
                    img: 'https://cdn11.bigcommerce.com/s-2c1axsxmlw/images/stencil/500x659/products/3229/11307/Screenshot_2025-02-11_at_2.44.24PM__89757.1739313998.png?c=2',
                    price: '₱8,500',
                    name: 'Glass-Top Coffee Table',
                    description: 'Cozy and compact, ideal for small living spaces.'
                },
                {
                    id: 27,
                    img: 'https://www.simpli-home.com/cdn/shop/products/AXCWAG-04-N-front_v5-copy.jpg?v=1677181227',
                    price: '₱4,500 ',
                    name: 'Marble Side Table',
                    description: 'The centerpiece of your living room; built for family gatherings.'
                },
                {
                    id: 28,
                    img: 'https://ourhome.ph/cdn/shop/files/OURHOME_SPRINGTABLE_4.jpg?v=1707872163',
                    price: '₱18,000',
                    name: 'Extendable Dining Table',
                    description: 'Designed for lounging; perfect for movie nights and hosting.'
                },
                {
                    id: 29,
                    img: 'https://eurekaergonomic.com/cdn/shop/files/1-2_58628ab3-f551-4c52-9efc-177ef7e04b11.jpg?v=1767860679&width=1946',
                    price: '₱19,000',
                    name: ' Minimalist Work Desk',
                    description: 'Seamlessly converts from a stylish sofa to a comfy guest bed.'
                },
                {
                    id: 30,
                    img: 'https://rustandoak.co.uk/cdn/shop/products/SHOPIFY4Xcon20boxlegangleview1.jpg?v=1756127367',
                    price: '₱3,000',
                    name: 'Rustic Console Table',
                    description: 'A versatile, space-saving essential for modern studios.'
                },
                {
                    id: 31,
                    img: 'https://cooperandco.com.au/cdn/shop/files/TB-ACT646-NA_1.jpg?v=1716506144&width=2000',
                    price: '₱30,000',
                    name: 'Nested Coffee Table',
                    description: 'Timeless, hand-tufted elegance for a sophisticated home.'
                },
                {
                    id: 32,
                    img: 'https://ak1.ostkcdn.com/images/products/is/images/direct/0b5cca5bfa746606a10d80312b895ac20eebc04b/Furniture-of-America-Harold-Modern-54-inch-Round-Espresso-Pedestal-Dining-Table.jpg',
                    price: '₱12,000',
                    name: 'Pedestal Bistro Table',
                    description: 'Ultimate relaxation with adjustable support for your back.'
                },
                {
                    id: 33,
                    img: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSlp3AT6fXX-a1ifZ1GLn8a1QxEvC6vq1N57w&s',
                    price: '₱5,000',
                    name: 'Industrial Iron-Frame Table',
                    description: 'Luxury comfort where every seat is the best in the house.'
                },
                {
                    id: 34,
                    img: 'https://ak1.ostkcdn.com/images/products/is/images/direct/23a3b92671cb0c9819af5cefc5b732864b6d3a16/Small-Vanity-Desk-with-Mirror-and-Light%2C-Dressing-Table-with-Charging-Station-%26-Fold-up-Panel%2C-Vanity-Set-with-Hidden-Stool.jpg?impolicy=medium',
                    price: '₱15,000',
                    name: 'Vanity/Dressing Table',
                    description: 'Clean lines and iconic style for the design-conscious.'
                },
                {
                    id: 35,
                    img: 'https://media.bunnings.com.au/api/public/content/e968adf37806492f8dc44eedea2e0b69?v=4a9f684c&t=w700dpr1',
                    price: '₱2,000',
                    name: 'Foldable Balcony Table',
                    description: 'Defined by soft, loose cushions for laid-back comfort.'
                },
                {
                    id: 36,
                    img: 'https://m.media-amazon.com/images/I/71eI24eHGwL._AC_UF894,1000_QL80_.jpg',
                    price: '₱7,000',
                    name: 'Nightstand / Bedside Table',
                    description: 'Elegant and slim-profile seating that fits any corner.'
                },
            ],
            currentIndex: 0,
            sofaItems: false,
            items:true,
            cart:[],
        }

    },
    emits: ['addCart'],
    methods: {
        buySofa(index) {
            this.currentIndex = index;
           this.items = false;
            this.sofaItems = true
            
        },
        addCart(index) {
            this.cart.push({...sofa})
            this.currentIndex = index
            

        },
        return(){
            this.sofaItems = true;
        }
    }
}
</script>
<template>
    <div v-if="items" class="bg-stone-600/90">
        <section class="container mx-auto p-10 md:py-12 px-0 md:p-8 md:px-0">
            <div class="h-30 w-full">
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
                    <h1 class="text-2xl font-extrabold text-amber-950 font-['Poppins'] my-4">{{ sofas.name }}</h1>

                    <h2 class=" text-xl font-bold text-amber-950 font-['Poppins'] my-3">{{ sofas.price }}.00</h2>
                    <button class="p-2 px-6 bg-amber-800 text-white rounded-md hover:bg-[#c09858] cursor-pointer"
                        @click="buySofa(index)">Add To
                        Cart</button>
                </section>
            </section>
        </section>
    </div>
    <Cart v-if="sofaItems" :selecteditems="sofa[currentIndex]" @returntoshop="return" @addCart="addCart"/>
</template>