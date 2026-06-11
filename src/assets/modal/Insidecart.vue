<script>
export default{
    props:{
       cart :{
            type: Array
        }
    },
    data (){
        return{
            shoppingCart: true,
        }
    }

}
</script>
<template>

    <div class="h-30 w-full">

    </div>
   
    <div v-if="shoppingCart" class="bg-stone-600/90 h-screen py-8 px-10">
        <div  class="container mx-auto px-4">
            <h1 class="text-2xl font-semibold mb-4 font-['Poppins'] text-amber-950 ">Shopping Cart</h1>
            <div      class="flex flex-col md:flex-row gap-4">
                <div class="md:w-3/4">
                    <div  class="bg-stone-300 rounded-lg shadow-md p-6 mb-4">
                        <table class="w-full">
                            <thead>
                                <tr>
                                    <th class="text-left font-semibold font-['Poppins'] text-amber-950">Product</th>
                                    <th class="text-left font-semibold font-['Poppins'] text-amber-950">Price</th>
                                    <th class="text-left font-semibold font-['Poppins'] text-amber-950">Quantity</th>
                                    <th class="text-left font-semibold font-['Poppins'] text-amber-950">Total</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr>
                                    <td class="py-4">
                                        <div class="flex items-center">
                                            <img class="h-16 w-16 mr-4" :src="cart.img"
                                                alt="Product image">
                                            <span class="font-semibold">{{ cart.name }}</span>
                                        </div>
                                    </td>
                                    <td class="py-4">{{ cart.price }}</td>
                                    <td class="py-4">
                                        <div class="flex items-center">
                                            <button class="border rounded-md py-2 px-4 mr-2">-</button>
                                            <span class="text-center w-8">1</span>
                                            <button class="border rounded-md py-2 px-4 ml-2">+</button>
                                        </div>
                                    </td>
                                    <td class="py-4">{{ cart.price }}</td>
                                </tr>
                                <!-- More product rows -->
                            </tbody>
                        </table>
                    </div> 
                </div>
                <!-- <div class="md:w-1/4">
                    <div class="bg-white rounded-lg shadow-md p-6">
                        <h2 class="text-lg font-semibold mb-4">Summary</h2>
                        <div class="flex justify-between mb-2">
                            <span>Subtotal</span>
                            <span>$19.99</span>
                        </div>
                        <div class="flex justify-between mb-2">
                            <span>Taxes</span>
                            <span>0.00</span>
                        </div>
                        <div class="flex justify-between mb-2">
                            <span>Shipping</span>
                            <span>0.00</span>
                        </div>
                        <hr class="my-2">
                        <div class="flex justify-between mb-2">
                            <span class="font-semibold">Total</span>
                            <span class="font-semibold">{{ cart.price }}</span>
                        </div>
                        <button class="bg-blue-500 text-white py-2 px-4 rounded-lg mt-4 w-full">Checkout</button>
                    </div>
                </div> -->
            </div>
        </div>
    </div>

</template>