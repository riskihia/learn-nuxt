<script setup>
const data = [
{
    "name" : "Project BNI LIFE",
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


const route = useRoute();
let id = route.params.id;
// console.log(id);

const project = data[id];
// console.log(project);

</script>

<template>
    <Header />

    <div class="project grid grid-cols-2 w-10/12 mx-auto mb-10">
        <template v-if="project.imagePosition === 'right'">
            <div class="desc pr-10 flex flex-col">
                <div>
                    <h1 class="text-center text-2xl font-bold py-2">
                        <a href="/projects/0">{{project.name}}</a>
                    </h1>
                    <div v-html="project.desc" class="py-1 text-base text-justify"></div>
                </div>
                <div class="flex flex-wrap pt-10">
                    <span v-for="(color, tech) in project.tectList" :key="tech" class="rounded-full px-6 py-2 mr-4" :style="{ backgroundColor: color, color: 'white' }">{{ tech }}</span>
                </div>
            </div>
            <div class="project-image grid grid-cols-2">
                <img v-for="(image, index) in project.images" :key="index" :src="`/assets/img/${image}`" class="p-4 max-h-[240px] w-full scale-90 hover:scale-100 transition" alt="">
            </div>
        </template>
        <template v-else>
            <div class="project-image grid grid-cols-2">
                <img v-for="(image, index) in project.images" :key="index" :src="`/assets/img/${image}`" class="p-4 max-h-[240px] w-full scale-90 hover:scale-100 transition" alt="">
            </div>
            <div class="desc pr-10 flex flex-col">
                <div>
                    <h1 class="text-center text-2xl font-bold py-2">
                        <a href="/projects/1">{{project.name}}</a>
                    </h1>
                    <p class="py-1 text-base text-justify">{{ project.desc }}</p>
                </div>
                <div class="flex flex-wrap pt-10">
                    <span v-for="(color, tech) in project.tectList" :key="tech" class="rounded-full px-6 py-2 mr-4" :style="{ backgroundColor: color, color: 'white' }">{{ tech }}</span>
                </div>
            </div>
        </template>
    </div>

    <Footer />
</template>

<style lang="css">
</style>