 

<template>
   <!-- component -->
<div   v-show="modalActive" class="bg-white rounded md:w-1/2 w-1/2 border shadow-lg place-items-center float-right">
    <div v-show="modalActive"  class="rounded-t">
      <div class="relative py-3 px-2 flex">
        <span class="font-semibold text-black md:text-base text-5 items-center justify-center">Choose Taxation </span>
        <div class="absolute right-0 top-0 -mr-2 -mt-2 border cursor-pointer shadow-lg bg-white z-10  rounded-full p-2">
        
        </div>
      </div>
    </div>
    <div class="border-b-2 border-[#e8f0fe]"></div>
    <div class=" md:text-base text-sm border-b p-2 h-24">
        
        
<div class="flex items-center mb-4">
    <input id="default-radio-1" type="radio" value="" name="default-radio" class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600">
    <label for="default-radio-1" class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">Default radio</label>
</div>
<div class="flex items-center">
    <input checked="" id="default-radio-2" type="radio" value="" name="default-radio" class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600">
    <label for="default-radio-2" class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">Checked state</label>
</div>
<!-- swttting pop -->

 <div>
     <div v-for="key in count " :key="key">
        <input type="text"  v-model="values['dynamic-field-'+key]" :id="key " class="   text-grey-700 text-5  border-2 w-30 p-2  dark:placeholder-[#c8c3cf] " placeholder="Field Name" required>
     </div>
 </div>
 <button id="add_more_fields" @click="add"  class="focus:outline-none py-1 px-2 md:py-2 md:px-3 w-24 mr-2 border-2 hover:bg-grey-700 text-black rounded">Add Field</button>
      </div>
      <div class="p-2 flex justify-end rounded-b">
        <button  @click="submit" class="focus:outline-none py-1 px-2 md:py-2 md:px-3 w-24 mr-2 bg-blue-700 hover:bg-blue-600 text-white rounded">save</button>
        <button   @click="close" class="focus:outline-none py-1 px-2 md:py-2 md:px-3 w-24 bg-red-700 hover:bg-red-600 text-white rounded">Cancel</button>
      </div>
  </div>
</template>

<script>
    export default {
      props: ["modalActive"],
      setup(props, { emit }) {
        const close = () => {
          emit("close");
        };
        return { close };
      },
      data: function () { 
        return {
          count: 0,
         values: {}
    
        }
      },
      methods: {
        add: function(){
          this.count++;
        },
        remove: function () {
         this.count--;
         
        },
        
        submit: function(){
         for (var key of Object.keys(this.values)) {
              console.log(key + " -> " + this.values[key])
          }
        }
    
        
      }
       
    };
    </script>