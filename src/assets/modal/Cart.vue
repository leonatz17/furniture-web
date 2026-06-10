<script>
import Payment from './Payment.vue';
export default{
  components:{
    Payment,
  },
  props:{
    selecteditems:{
      type:Object
    }
  },
  data (){
    return{
      itemschecked: false,
      pay: false
    }
  },
  emits:['returntoshop'],
  methods:{
    returnShop(){
      this.$emit('returntoshop')
    },
    paymentTab(){
      this.pay = true;
    }
  }
}
</script>
<template>
  <section class="w-full bg-stone-600/90 py-9 px-12">
    <div class="h-30 w-full">
    </div>
    <h1 class="text-center text-amber-950 font-['Poppins'] text-[32px] font-semibold leading-[38px]">
      My Shopping Cart
    </h1>
    <div class="flex items-start mt-8 gap-6 ">
      <div class="hover:bg-stone-300 border-1 border-amber-600 p-4 w-[800px] rounded-xl">
        <table class="w-full  rounded-xl">
          <thead>
            <tr
              class="text-center border-b border-[#c09858] w-full text-amber-950 text-sm font-medium uppercase leading-[14px] tracking-wide ">
              <th class="text-left px-2 py-2">Product</th>
              <th class="px-2 py-2">price</th>
              <th class="px-2 py-2">Quantity</th>
              <th class="px-2 py-2">Subtotal</th>
              <th class="w-7 px-2 py-2"></th>
            </tr>
          </thead>
          <tbody>
            <tr class="text-center">
              <td class="px-2 py-2 text-left align-top">
                <img :src="selecteditems.img " alt="photo"
                  class="w-[150px] mr-2 inline-block h-[120px]" /><span class="text-amber-950 font-['Poppins'] text-xl">{{ selecteditems.name }}</span>
              </td>
              <td class="px-2 py-2 text-amber-950 font-['Poppins']">{{ selecteditems.price }}.00</td>
              <td class="p-2 mt-9  rounded-[170px] border border-[#c09858] justify-around items-center flex">
                <svg width="14" height="15" class="cursor-pointer" viewBox="0 0 14 15" fill="none"
                  xmlns="http://www.w3.org/2000/svg">
                  <path d="M2.33398 7.5H11.6673" stroke="#666666" stroke-width="1.5" stroke-linecap="round"
                    stroke-linejoin="round"></path>
                </svg><span class="w-10 text-center text-amber-950 font-['Poppins'] text-base font-normal leading-normal">5</span><svg
                  class="cursor-pointer relative" width="14" height="15" viewBox="0 0 14 15" fill="none"
                  xmlns="http://www.w3.org/2000/svg">
                  <path d="M2.33398 7.49998H11.6673M7.00065 2.83331V12.1666V2.83331Z" stroke="#1A1A1A"
                    stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"></path>
                </svg>
              </td>
              <td class="px-2 py-2 text-amber-950 font-['Poppins']">$70.00</td>
              <td class="px-2 py-2">
                <svg width="24" class="cursor-pointer text-[#c09858]" height="25" viewBox="0 0 24 25" fill="none"
                  xmlns="http://www.w3.org/2000/svg">
                  <path
                    d="M12 23.5C18.0748 23.5 23 18.5748 23 12.5C23 6.42525 18.0748 1.5 12 1.5C5.92525 1.5 1 6.42525 1 12.5C1 18.5748 5.92525 23.5 12 23.5Z"
                    stroke="#CCCCCC" stroke-miterlimit="10"></path>
                  <path d="M16 8.5L8 16.5" stroke="#666666" stroke-width="1.5" stroke-linecap="round"
                    stroke-linejoin="round"></path>
                  <path d="M16 16.5L8 8.5" stroke="#666666" stroke-width="1.5" stroke-linecap="round"
                    stroke-linejoin="round"></path>
                </svg>
              </td>
            </tr>
            
            
          </tbody>
          <tfoot>
            <tr class="border-t border-amber-600 ">
              <td class="px-2 py-2" colspan="3">
                <button
                  class="px-8 cursor-pointer py-3.5 bg-amber-800 rounded-[43px] hover:bg-[#c09858] text-sm font-semibold className leading-[16px] text-white font-['Poppins']" @click="returnShop">
                  Return to shop
                </button>
              </td>
              <td class="px-2 py-2" colspan="2">
                <button
                  class="px-8 py-3.5 cursor-pointer bg-amber-800 rounded-[43px] hover:bg-[#c09858] text-sm font-semibold className leading-[16px] text-white font-['Poppins']">
                  Update Cart
                </button>
              </td>
            </tr>
          </tfoot>
        </table>
      </div>
      <div class="w-[424px] bg-stone-300 hover:bg-stone-300 border-1 border-amber-600 rounded-lg p-6">
        <h2 class="text-amber-950 font-['Poppins'] mb-2 text-xl font-medium leading-[30px]">
          Cart Total
        </h2>
        <div class="w-[376px] py-3 justify-between items-center flex">
          <span class="text-amber-950 font-['Poppins'] text-base font-normal leading-normal">Total:</span><span
            class="text-amber-950 font-['Poppins'] text-base font-semibold leading-tight">{{ selecteditems.price }}.00</span>
        </div>
        <div class="w-[376px] py-3 shadow-[0px_1px_0px_0px_rgba(229,229,229,1.00)] justify-between items-center flex">
          <span class="text-amber-950 font-['Poppins'] text-sm font-normal leading-[21px]">Shipping:</span><span
            class="text-amber-950 font-['Poppins'] text-sm font-medium leading-[21px]">Free</span>
        </div>
        <div class="w-[376px] py-3 shadow-[0px_1px_0px_0px_rgba(229,229,229,1.00)] justify-between items-center flex">
          <span class="text-amber-950 font-['Poppins'] text-sm font-normal leading-[21px]">Subtotal:</span><span
            class="text-amber-950 font-['Poppins'] text-sm font-medium leading-[21px]">{{ selecteditems.prize }}.00</span>
        </div>
        <button
          class="w-[376px] text-white mt-5 px-10 py-4 bg-amber-800 hover:bg-[#c09858] rounded-[44px] gap-4 text-base font-semibold leading-tight" @click="paymentTab">
          Proceed to checkout
        </button>
      </div>
    </div>
    <div
      class="mt-6 p-5 w-[800px]  rounded-lg border border-amber-600 justify-start items-center gap-6 inline-flex hover:bg-stone-300">
      <h3 class="text-amber-950 font-['Poppins'] w-1/4 text-xl font-medium className leading-[30px]">
        Coupon Code
      </h3>
      <div class="w-full ">
        <input placeholder="Enter code" type="text"
          class="w-2/3 px-6 py-3.5 outline-none border border-amber-600 rounded-[46px] text-amber-950 font-['Poppins'] text-base font-normal leading-normal" /><button
          class="px-10 py-4 bg-amber-800 font-['Poppins']  rounded-[43px] text-white text-base font-semibold leading-tight">
          Apply Coupon
        </button>
      </div>
    </div>
  </section>
  <Payment v-if="pay" />
</template>