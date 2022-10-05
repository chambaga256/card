<!-- <script setup>
import AddIcon from './icons/AddIcon.vue';
</script> -->
<script>
  import Modal from "./Model.vue";
  import { ref } from "vue";
  export default {
    name: "App",
    components: {
      Modal,
    },
    setup() {
      const modalActive = ref(false);
      const toggleModal = () => {
        modalActive.value = !modalActive.value;
      };
      return { modalActive, toggleModal };
    },
  };
  </script>

<template>
    <div class="">
  

<div class=" lg:flex  space-x-11  ml-[180px] pb-[50px] ">
  <Modal @close="toggleModal" :modalActive="modalActive" />
    <button  @click="toggleModal" class="h-15 px-11 m-2 sm:w-10 bg-[#f7faff] flex  transition-colors duration-150 bg-grey border-2  text-black focus:shadow-outline hover:bg-grey"> <span class="text-[#2c7ce7] text-base">
      %</span> Add Tax</button>
    <p class="w-[80px]">Currency <span class="text-[#911c26]">*</span></p>
    <div class="inline-block relative w-64">
  <select class="block appearance-none w-full bg-[#f7faff]  border border-gray-400 hover:border-gray-500 px-4 py-2 pr-8 rounded shadow leading-tight focus:outline-none focus:shadow-outline">
    <option>USA Dollars</option>
    <option>USH</option>
    <option>KSH</option>
  </select>
  <div class="pointer-events-none absolute inset-y-0 right-0 flex items-center px-2 text-gray-700">
    
  </div>
</div>

<div claas=" px-5 ">
    <button class=" w-30 h-30 inset-0 bg-[#f7faff]  hover:bg-gray-100 text-gray-800 font-semibold py-2 px-4 border border-gray-400 rounded shadow">
<span  class="text-[#2c7ce7]">246</span> Number Format
</button>


</div>
<button class=" pb-2 bg-[#f7faff] w-30 h-30 hover:bg-gray-100 text-gray-800 font-semibold py-2  border border-gray-700 ">
Rename/Add Fields
</button>
  </div>
  <!-- button low -->
  <div class="ml-[180px]  mr-[150px]  sm:pt-50 pb-5 sm:items-center justify-content-center relative w-[1000px] h-10 sm:object-fill  sm:h- bg-[#2c7ce7]  space-y-4 text-white border-rounded items-center place-items-center ">
    <div class="lg:flex  gap-x-[200px]" >
        <p class=""> Item</p>
      
        <p  class ="">Quantiy</p>
     
        <p>
        Rate
        </p>
        <p>
            Amount 
        </p>

    

    </div>
     <div>
        <button class=" pb-50 pt-50 w-full h-12 space-y-7 px-6 text-[#911c26] transition-colors duration-150 bg-[#f7faff] rounded-lg border-dashed border-2 border-[#e5e7eb] focus:shadow-outline hover:bg-[#f7faff]">
            
            <AddIcon class="w-4 h-4 px-[50px] fill-current" />
            <span>  Add New Line </span> </button> 
     </div>

  </div>
   <div class="ml-[880px] pt-20  space-y-7  ">
    <div>
      <div claas=" px-5 ">
    <button class=" w-30 h-30 inset-0 bg-[#f7faff]  hover:bg-gray-100 text-gray-800 font-semibold py-2 px-4  rounded shadow">  
       Give Item wise Discount
</button>


</div>

      
    </div>
    <div>
      <div claas=" px-5 pt-50 ">
    <button class=" w-30 h-30 inset-0 bg-[#f7faff]  hover:bg-gray-100 text-gray-800 font-semibold py-2 px-4 rounded shadow">  
      Give Discount on Total
</button>


</div>
   
    </div>
    <div>
      <div claas=" px-5 space-y-10 pt-10">
    <button class="  w-30 h-30 inset-0 bg-[#f7faff]  hover:bg-gray-100 text-gray-800 font-semibold py-2 px-4 rounded shadow">  
      Add Additional Charges
      </button>

</div>
      
    </div>
    <div class="border border-gray-300 w-[400px] px-30">

    </div>
   
    <div claas=" px-5 space-y-10 pt-10">
    <button class="  w-30 h-30 inset-0   hover:bg-gray-100 text-black  text-[40px] font-semibold py-2 px-4 rounded shadow">  
      Total
 
        (USD)
      </button>

</div>

<div claas=" px-5 space-y-10 pt-10">
    <button class="  w-30 h-30 inset-0  hover:bg-gray-100 text-gray-800 font-semibold py-2 px-4 rounded shadow">  
      Show Total In Words
      </button>

</div>
<div claas=" px-5 space-y-10 pt-10">
    <button class="  w-30 h-30 inset-0  hover:bg-gray-100 text-gray-800 font-semibold py-2 px-4 rounded shadow">  
      Show Total In Words
      </button>

</div>
   </div>
   
   <div class="ml-[155px] pt-5  lg:flex  space-x-4 ">
    <div claas=" px-5 ">
    <button class=" w-30 h-30 inset-0 bg-[#f7faff]  hover:bg-gray-100 text-gray-800 font-semibold py-2 px-4 border border-gray-400 rounded shadow">
<span  class="text-[#2c7ce7]">246</span> Number Format
</button>


</div>
<div claas=" px-5 ">
    <button class=" w-30 h-30 inset-0 bg-[#f7faff]  hover:bg-gray-100 text-gray-800 font-semibold py-2 px-4 border border-gray-400 rounded shadow">
<span  class="text-[#2c7ce7]">246</span> Number Format
</button>


</div>
<div claas=" px-5 ">
    <button class=" w-30 h-30 inset-0 bg-[#f7faff]  hover:bg-gray-100 text-gray-800 font-semibold py-2 px-4 border border-gray-400 rounded shadow">
<span  class="text-[#2c7ce7]">246</span> Number Format
</button>


</div>
<div claas=" px-5 ml-[50px]">
    <button class=" w-30 h-30 inset-0 bg-[#f7faff]  hover:bg-gray-100 text-gray-800 font-semibold py-2 px-4 border border-gray-400 rounded shadow">
<span  class="text-[#2c7ce7]">246</span> Number Format
</button>


</div>
   </div>
   <div class="lg:flex   ml-[155px] space-x-5 pt-10">
    <div claas=" px-5 ml-[50px]">
    <button class=" w-30 h-30 inset-0 bg-[#f7faff]  hover:bg-gray-100 text-gray-800 font-semibold py-2 px-4 border border-gray-400 rounded shadow">
<span  class="text-[#2c7ce7]">246</span> Number Format
</button>


</div>
<div claas=" px-5 ml-[50px]">
    <button class=" w-30 h-30 inset-0 bg-[#f7faff]  hover:bg-gray-100 text-gray-800 font-semibold py-2 px-4 border border-gray-400 rounded shadow">
<span  class="text-[#2c7ce7]">246</span> Number Format
</button>


</div>
   </div>
   <div class="bg-[#e8f0fe]  ml-[150px] p-0 h-[60px] space-y-10 w-[500px] pt-5 lg:flex space-x-10">
    <!-- <div claas=" px-5 ml-[50px]">
    <button class=" w-30 h-30 inset-0 bg-[#f7faff]  hover:bg-gray-100 text-gray-800 font-semibold py-2 px-4 border border-gray-400 rounded shadow">
<span  class="text-[#2c7ce7]">246</span>  This is a recurring invoice.
</button>


</div> -->
    <p class="pb-2 space-y-2">This is a recurring invoice.
    A draft invoice will be created with same details every next period.</p>
   <div claas=" px-5 ml-[50px] h-[10px] absolute">
    <button class=" w-30 h-30 inset-0 bg-[#f7faff]  hover:bg-gray-100 text-gray-800 font-semibold py-2 px-4 border border-gray-400 rounded shadow">
<span  class="text-[#2c7ce7]">246</span>  This is a recurring invoice.
</button>


</div>
  
  
  </div>

    <!-- <div claas=" px-5 ml-[50px]">
    <button class=" w-30 h-30 inset-0 bg-[#f7faff]  hover:bg-gray-100 text-gray-800 font-semibold py-2 px-4 border border-gray-400 rounded shadow">
<span  class="text-[#2c7ce7]">246</span>  This is a recurring invoice.
</button>


</div> -->
 </div>

    
</template>