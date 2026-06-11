<script>
import Sofa from '../assets/modal/Sofa.vue';
import Contact from '../assets/modal/Contact.vue';

export default {
    components: {
        Sofa,
        Contact
       
    },
    data() {
        return {
            sofaproduct: false,
            Homepage: true,
            cart: [],
            contactUs:false
           
            
            
            

        }
    },
    emits:['addCart'],
    methods: {
        sofaProduct() {
            this.sofaproduct = true;
            this.Homepage = false;
        },
        handleCart(sofa) {
        this.$emit('addCart', {...sofa});
        this.cart.push(sofa)
        
    },
    contact(){
        this.contactUs = true;
        this.Homepage = false; 
    }
        

    }
}
</script>

<template>
    <div v-if="Homepage" class="bg-stone-600/90">
        <div class="w-full h-30">
        </div>
        <div class="relative w-full h-[320px]" id="home">
            <div class="absolute inset-0 opacity-70 h-100">
                <img src="https://essentialhome.eu/room-by-room/wp-content/uploads/2024/10/MCG_0724-Living-brubeck-miles-russel-fitzgerald-metamorphosis-matheny-craig-shirley-martin-1-2-scaled.jpg"
                    alt="Background Image" class="object-cover object-center w-full h-full" />

            </div>
            <div class="absolute inset-9 flex flex-col md:flex-row items-center justify-between">
                <div class="md:w-1/2 mb-4 md:mb-0">
                    <h1 class="text-white font-['Poppins'] font-extrabold text-5xl md:text-5xl leading-tight mb-2">Rest
                        like
                        Royalty.</h1>
                    <p class="font-regular text-xl mb-8 mt-4 text-white font-['Poppins']">Luxury Furniture, Curated for
                        the Filipino Home
                    </p>
                    <h1 
                        class=" px-6 w-fit py-3 bg-[#c8a876] text-white font-medium rounded-full hover:bg-[#c09858]  transition duration-200" @click="contact">Contact
                        Us</h1>
                </div>
            </div>
        </div>


        <!-- our collection section -->
        <section class="py-30 px-10" id="services">
            <div class="container mx-auto px-3">
                <h2 class="text-3xl font-bold text-[#c09858] mb-8 text-center font-['Poppins']">Our Collection</h2>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8 ">
                    <div class=" rounded-lg shadow-md overflow-hidden hover:bg-stone-300 cursor-pointer"
                        @click="sofaProduct">
                        <img src="https://m.media-amazon.com/images/I/91GILvhd-rL._AC_UF894,1000_QL80_.jpg"
                            alt="wheat flour grinding" class="w-full h-110 object-cover">
                        <div class="p-6 text-center flex justify-between">
                            <h3 class="text-xl font-bold text-amber-950 mb-2 font-['Poppins']" @click="sofaProduct">Sofa Collection</h3>
                            <button class="text-lg font-bold text-white mb-2 font-['Poppins'] bg-amber-900 p-2 hover:bg-[#c09858]" @click="sofaProduct">See all Collection➜ </button>

                        </div>
                    </div>
                    <div class=" rounded-lg shadow-md overflow-hidden hover:bg-stone-300 cursor-pointer"
                        @click="sofaProduct">
                        <img src="https://cdn.thewirecutter.com/wp-content/media/2026/03/BEST-COFFEE-TABLES-SUB-02025-1.jpg?width=2048&quality=60&crop=2048:1365&auto=webp"
                            alt="Coffee" class="w-full h-110 object-cover">
                        <div class="p-6 text-center flex justify-between">
                            <h3 class="text-xl font-medium text-amber-950 mb-2" @click="sofaProduct">Table Collection
                            </h3>
                            <button class="text-lg font-bold text-white mb-2 font-['Poppins'] bg-amber-900 p-2 hover:bg-[#c09858]" @click="sofaProduct">See all Collection➜ </button>

                        </div>
                    </div>
                    <div class=" rounded-lg shadow-md overflow-hidden hover:bg-stone-300 cursor-pointer" @click="sofaProduct">
                        <img src="https://assets.sohohome.com/cdn-cgi/image/fit=crop%2Cformat=auto%2Cquality=75%2Cwidth=1100%2Cheight=1222%2Ctrim=388%3B0%3B389%3B0/images/original/271871-78124283-hoverjpg.jpg"
                            alt="Coffee" class="w-full h-110 object-cover">
                        <div class="p-6 text-center flex justify-between">
                            <h3 class="text-xl font-medium text-amber-950 mb-2 " @click="sofaProduct" >Chairs Collection</h3>
                            <button class="text-lg font-bold text-white mb-2 font-['Poppins'] bg-amber-900 p-2 hover:bg-[#c09858]" @click="sofaProduct">See all Collection➜ </button>
                        </div>
                    </div>
                    <div class=" rounded-lg shadow-md overflow-hidden hover:bg-stone-300 cursor-pointer" @click="sofaProduct">
                        <img src="https://www.nitori.com.ph/cdn/shop/files/4714424-471752001_415x415.jpg?v=1709949604g"
                            alt="Coffee" class="w-full h-110 object-cover">
                        <div class="p-6 text-center flex justify-between">
                            <h3 class="text-xl font-medium text-amber-950 mb-2 " @click="sofaProduct">Kitchen Furniture Collection</h3>
                            <button class="text-lg font-bold text-white mb-2 font-['Poppins'] bg-amber-900 p-2 hover:bg-[#c09858]" @click="sofaProduct">See all Collection➜ </button>
                        </div>
                    </div>
                    <div class=" rounded-lg shadow-md overflow-hidden hover:bg-stone-300 cursor-pointer" @click="sofaProduct">
                        <img src="https://ouchcart.com/cdn/shop/files/Berne_Upholstered_Bed_Frame_37275ae1-c586-4335-81ee-2e85927ac1e8.webp?v=1721393639&width=800"
                            alt="Coffee" class="w-full h-110 object-cover">
                        <div class="p-6 text-center flex justify-between">
                            <h3 class="text-xl font-medium text-amber-950 mb-2 " @click="sofaProduct">Bedroom Furniture Collection</h3>
                            <button class="text-lg font-bold text-white mb-2 font-['Poppins'] bg-amber-900 p-2 hover:bg-[#c09858]" @click="sofaProduct">See all Collection➜ </button>
                        </div>

                    </div>
                    <div class=" rounded-lg shadow-md overflow-hidden hover:bg-stone-300 cursor-pointer" @click="sofaProduct">
                        <img src="https://mandauefoam.ph/cdn/shop/files/PHOTO_2_LIFESTYLE_1_e744151f-ac67-4fd0-91e0-51c45622dcc0.jpg?v=1776483003&width=2048"
                            alt="Coffee" class="w-full h-110 object-cover">
                        <div class="p-6 text-center flex justify-between">
                            <h3 class="text-xl font-medium text-amber-950 mb-2 " @click="sofaProduct">Outdoor Furniture Collection</h3>
                            <button class="text-lg font-bold text-white mb-2 font-['Poppins'] bg-amber-900 p-2 hover:bg-[#c09858]" @click="sofaProduct">See all Collection➜ </button>
                        </div>

                    </div>
                </div>
            </div>
        </section>
    </div>
    <Sofa v-if="sofaproduct" @addCart="handleCart" /> 
    <Contact v-if="contactUs" />
    
</template>