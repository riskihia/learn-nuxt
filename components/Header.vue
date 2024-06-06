<script setup>
const route = useRoute();
const url = route.fullPath;
const parts = url.split('/');

let active = parts[1];

if(active === ""){
    active = "index"
}

console.log(active)
</script>

<template>
    <div class="flex w-10/12 mx-auto border-b-4 p-2">
        <span class="basis-1/6 mr-[60%] font-bold text-5xl text-center cursor-pointer text-blue-400">LOGO</span>
        <ul class="flex flex-auto justify-between">
            <li class="text-xl flex items-center px-3 cursor-pointer hover:bg-slate-200" :class="{'bg-slate-200': active == 'index'}">
                <a href="/">HOME</a>
            </li>
            <li class="text-xl flex items-center px-3 cursor-pointer hover:bg-slate-200" :class="{'bg-slate-200': active == 'projects'}">
                <a href="/projects">PROJECTS</a>
            </li>
            <li class="text-xl flex items-center px-3 cursor-pointer hover:bg-slate-200" :class="{'bg-slate-200': active == 'about'}">
                <a href="/about" >ABOUT</a>
            </li>
            <li class="text-xl flex items-center px-3 cursor-pointer hover:bg-slate-200" :class="{'bg-slate-200': active == 'contact'}">
                
                <a href="/contact">CONTACT</a>
            </li>
        </ul>
    </div>
</template>

<style lang="css"></style>