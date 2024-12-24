

 <template>
  <div class=" grid gap-4 justify-center items-center"> 
          <h1 class="text-7xl text-red-600 font-bold underline">
        Count 
        </h1>

        <span class="mt-5  p-4 text-center bg-green-500 rounded-md text-3xl text-white" > {{ count }}
         </span>
        <button @click="increment" class="mt-5 px-7 py-4 bg-green-500 rounded-md text-3xl text-white" > increment </button>
        <button @click="decrement"
                      :disabled="count===0"
                      :class="count===0 ? 'bg-green-100'
                                         : 'bg-green-800' "
         class="mt-5 px-7 py-4 bg-green-500 rounded-md text-3xl text-white" > increment </button>
 

  <Checkbox />
  </div>
</template>


  <script setup>
  import { ref } from 'vue'
  import Checkbox from './Checkbox.vue'
  const count = ref(0);

  const increment = () => {
    count.value++;
  }
  const decrement = () => {
    if(count.value >0){count.value--;}
  }
  
  </script>
