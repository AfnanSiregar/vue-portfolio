<template>
  <nav class="className='shadow-md w-full fixed top-0 left-0 z-[2]">
    <div class='md:flex items-center justify-between bg-slate-800 py-4 md:px-10 px-7 dark:bg-gray-800'>
        <div class="font-semibold text-2xl cursor-pointer flex items-center font-[Poppins] text-gray-200 transition-all duration-500 ease-in">
            <span class="text-white text-center">
                <h1>Afnan Siregar</h1>
            </span>
            <button-view/>
        </div>
        <div @click="(open += 1)" class="text-3xl text-white absolute right-8 top-4 cursor-pointer md:hidden">
            <ion-icon v-if="(open % 2 === 0)" name="menu"></ion-icon>
            <ion-icon v-else name="close-outline" class="hover:animate-spin"></ion-icon>
        </div>
        <ul v-if="(open %2 === 1)" class="md:flex items-center text-white bg-slate-800 md:z-auto z-[-1] left-0 w-full md:w-auto pl-9 transition-all duration-75 ease-in">
            <li class="md:ml-8 text-xl md:my-0 my-7">
                <a href="#home" @click="(open += 1)">HOME</a>
            </li>
            <li class="md:ml-8 text-xl md:my-0 my-7">
                <a href="#services" @click="(open += 1)">SERVICES</a>
            </li>
            <li class="md:ml-8 text-xl md:my-0 my-7">
                <a href="#works" @click="(open += 1)">WORKS</a>
            </li>
            <li class="md:ml-8 text-xl md:my-0 my-7">
                <a href="#about" @click="(open += 1)">ABOUT</a>
            </li>
        </ul>
    </div>
  </nav>
</template>

<script>
import { ref } from 'vue';
import ButtonView from './ButtonView.vue'

export default {
    components: { ButtonView },
    setup(){
        return{
            open: ref(0)
        }
    }
}

</script>