<template>
    <div class="bg-gray-900 text-gray-100 py-4 px-6 shadow 
    justify-between md:flex items-center">


    <div class="flex items-center cursor-pointer">
      <span class="text-green-500 text-xl mr-2">
        <i class="bi bi-messenger"></i>
    </span>
    <h1 class="text-xl">Designer</h1>
    </div>

    <span @click="MenuOpen()" class="absolute md:hidden right-6 top-1.5 cursor-pointer text-4xl">
        <i :class="[open ? 'bi bi-x' : 'bi bi-filter-left']"></i>
    </span>

    <ul class="md:flex md:items-center md:px-0 px-10 md:pb-0 pb-10 md:static absolute bg-gray-900
    md:w-auto w-full top-14 duration-700 ease-in"
    :class="[open ? 'left-0' : 'left-[-100]']">
        <li class="md:mx-4 md:my-0 my-6" v-for="link in Links">
            <a :href="link.link" class="text-xl hover:text-gray-500">{{link.name}}</a>
        </li>
    </ul>
    </div>
</template>

<script>
import { ref } from '@vue/reactivity'
export default {
    setup() {
        let open = ref(false)
        let Links = [
        { name: "Home", link: "#"},
        { name: "Services", link: "#"},
        { name: "About", link: "#"},
        { name: "Blog's", link: "#"},
        { name: "Contact", link: "#"},

        ]

        function MenuOpen(){
            open.value = !open.value
        }

        return{Links,open,MenuOpen}
        
    }
}

</script>