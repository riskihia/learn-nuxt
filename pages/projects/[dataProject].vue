<script setup>
const data = [
{
    "name" : "Project BMKG",
    "desc" : "<p class='py-1 text-base text-justify'>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Veritatis qui officia mollitia magni quidem deleniti molestias maiores. Debitis eaque quidem inventore! Consequatur, esse amet vel pariatur culpa tempora voluptas fugiat!</p><p class='py-1 text-base text-justify'>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Veritatis qui officia mollitia magni quidem deleniti molestias maiores. Debitis eaque quidem inventore! Consequatur, esse amet vel pariatur culpa tempora voluptas fugiat!</p>",
    "tectList" : {
        "github" : "black",
        "linkedin" : "blue",
        "facebook" : "blue",
        "instagram" : "pink"
    },
    "images" : [
        "bg.avif",
        "bg.avif",
        "bg.avif"
    ],
    "imagePosition" : "right"
},
{
    "name" : "Project BMKG",
    "desc" : "<p class='py-1 text-base text-justify'>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Veritatis qui officia mollitia magni quidem deleniti molestias maiores. Debitis eaque quidem inventore! Consequatur, esse amet vel pariatur culpa tempora voluptas fugiat!</p><p class='py-1 text-base text-justify'>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Veritatis qui officia mollitia magni quidem deleniti molestias maiores. Debitis eaque quidem inventore! Consequatur, esse amet vel pariatur culpa tempora voluptas fugiat!</p>",
    "tectList" : {
        "github" : "black",
        "linkedin" : "blue",
        "facebook" : "blue",
        "instagram" : "pink"
    },
    "images" : [
        "hero.jpg",
        "hero.jpg",
        "hero.jpg"
    ],
    "imagePosition" : "left"
}
]

const project = data[route.params.dataProject];
console.log(project)

</script>

<template>
    <div>data : {{ $route.params.dataProject }}</div>
</template>

<style lang="css">
</style>