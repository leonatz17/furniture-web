<script>
import Tablecart from './Tablecart.vue';
export default{
    components:{
        Tablecart

    },
    data (){
        return{
            table: [
                {
                    id: 1,
                    img: 'https://gulnatural.com/cdn/shop/collections/solid-wood-dining-tables.jpg?v=1708699881',
                    price: '₱20,000',
                    name: 'Solid Wood Dining Table',
                    description: 'A grand, heirloom-quality centerpiece for family feasts'
                },
                {
                    id: 2,
                    img: 'https://cdn11.bigcommerce.com/s-2c1axsxmlw/images/stencil/500x659/products/3229/11307/Screenshot_2025-02-11_at_2.44.24PM__89757.1739313998.png?c=2',
                    price: '₱8,500',
                    name: 'Glass-Top Coffee Table',
                    description: 'Cozy and compact, ideal for small living spaces.'
                },
                {
                    id: 3,
                    img: 'https://www.simpli-home.com/cdn/shop/products/AXCWAG-04-N-front_v5-copy.jpg?v=1677181227',
                    price: '₱4,500 ',
                    name: 'Marble Side Table',
                    description: 'The centerpiece of your living room; built for family gatherings.'
                },
                {
                    id: 4,
                    img: 'https://ourhome.ph/cdn/shop/files/OURHOME_SPRINGTABLE_4.jpg?v=1707872163',
                    price: '₱18,000',
                    name: 'Extendable Dining Table',
                    description: 'Designed for lounging; perfect for movie nights and hosting.'
                },
                {
                    id: 5,
                    img: 'https://eurekaergonomic.com/cdn/shop/files/1-2_58628ab3-f551-4c52-9efc-177ef7e04b11.jpg?v=1767860679&width=1946',
                    price: '₱19,000',
                    name: ' Minimalist Work Desk',
                    description: 'Seamlessly converts from a stylish sofa to a comfy guest bed.'
                },
                {
                    id: 6,
                    img: 'https://rustandoak.co.uk/cdn/shop/products/SHOPIFY4Xcon20boxlegangleview1.jpg?v=1756127367',
                    price: '₱3,000',
                    name: 'Rustic Console Table',
                    description: 'A versatile, space-saving essential for modern studios.'
                },
                {
                    id: 7,
                    img: 'https://cooperandco.com.au/cdn/shop/files/TB-ACT646-NA_1.jpg?v=1716506144&width=2000',
                    price: '₱30,000',
                    name: 'Nested Coffee Table',
                    description: 'Timeless, hand-tufted elegance for a sophisticated home.'
                },
                {
                    id: 8,
                    img: 'https://ak1.ostkcdn.com/images/products/is/images/direct/0b5cca5bfa746606a10d80312b895ac20eebc04b/Furniture-of-America-Harold-Modern-54-inch-Round-Espresso-Pedestal-Dining-Table.jpg',
                    price: '₱12,000',
                    name: 'Pedestal Bistro Table',
                    description: 'Ultimate relaxation with adjustable support for your back.'
                },
                {
                    id: 9,
                    img: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSlp3AT6fXX-a1ifZ1GLn8a1QxEvC6vq1N57w&s',
                    price: '₱5,000',
                    name: 'Industrial Iron-Frame Table',
                    description: 'Luxury comfort where every seat is the best in the house.'
                },
                {
                    id: 10,
                    img: 'https://ak1.ostkcdn.com/images/products/is/images/direct/23a3b92671cb0c9819af5cefc5b732864b6d3a16/Small-Vanity-Desk-with-Mirror-and-Light%2C-Dressing-Table-with-Charging-Station-%26-Fold-up-Panel%2C-Vanity-Set-with-Hidden-Stool.jpg?impolicy=medium',
                    price: '₱15,000',
                    name: 'Vanity/Dressing Table',
                    description: 'Clean lines and iconic style for the design-conscious.'
                },
                {
                    id: 11,
                    img: 'https://media.bunnings.com.au/api/public/content/e968adf37806492f8dc44eedea2e0b69?v=4a9f684c&t=w700dpr1',
                    price: '₱2,000',
                    name: 'Foldable Balcony Table',
                    description: 'Defined by soft, loose cushions for laid-back comfort.'
                },
                {
                    id: 12,
                    img: 'https://m.media-amazon.com/images/I/71eI24eHGwL._AC_UF894,1000_QL80_.jpg',
                    price: '₱7,000',
                    name: 'Nightstand / Bedside Table',
                    description: 'Elegant and slim-profile seating that fits any corner.'
                },
            ],
            currentIndex: 0,
            tableproducts: false,
            tableitems: true,
        }
        
    },
    methods:{
        buyTable(index){
            this.currentIndex = index;
            this.tableproducts = true;
            this.tableitems = false

        },
        addCart(table) {
            this.$emit('addtableCart', { ...table })
        },
    }
}
</script>
<template>
     <div v-if="tableitems" class="bg-stone-600/90">
        <section class="container mx-auto p-10 md:py-12 px-0 md:p-8 md:px-0">
            <div class="h-30 w-full">
            </div>
            <div class="h-10 w-full px-10">
                <h1 class="text-2xl font-['Poppins'] font-bold text-amber-950">> Table Collection</h1>
            </div>
            <section
                class="p-5 md:p-0 grid grid-cols-1 sm:grid-cols-1 md:grid-cols-2 xl:grid-cols-3 2xl:grid-cols-4 gap-10 items-start "
                >
                <section v-for="(tables,index) in table" :key="tables.id"
                    class="p-5 py-10  text-center transform duration-500 hover:-translate-y-2 cursor-pointer hover:bg-stone-300" @click="buyTable(index)">
                    <img class="w-full h-60" :src="tables.img" alt="">
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
                    <h1 class="text-xl font-bold text-amber-950 font-['Poppins'] my-3">{{ tables.name }}</h1>

                    <h2 class=" text-xl font-bold text-amber-950 font-['Poppins'] my-3" @click="buyTable(index)">{{ tables.price }}.00</h2>
                    <button class="p-2 px-6 bg-amber-800 text-white rounded-md hover:bg-[#c09858] cursor-pointer"
                        >Add To
                        Cart</button>
                </section>
            </section>
        </section>
    </div>
    <Tablecart v-if="tableproducts" :selectedTableitems="table[currentIndex]"/>
</template>