<script setup>

</script>

<template>
    <div class="skill-background">

        <div class="w-10/12 mx-auto py-6">
            <div>
                <h1 class="text-3xl font-bold text-center">Skill</h1>
                <p class="text-lg font-base text-center">Explore my skill. Dont forget to go back and HIRE ME</p>
            </div>
            <div class="flex">
                <SkillCard title="Programming Language" description="Lorem ipsum dolor sit, amet consectetur adipisicing elit. Vero eligendi quaerat tenetur doloremque, ipsum praesentium!" :skills="['PHP', 'Javascript', 'Python', 'Ruby', 'Swift', 'Golang']" />

                <SkillCard title="Backend Framework" description="Lorem ipsum dolor sit, amet consectetur adipisicing elit. Vero eligendi quaerat tenetur doloremque, ipsum praesentium!" :skills="['Spring Boot', 'ASP.NET', 'Node.Js', 'Laravel', 'Flask']" />
                
                <SkillCard title="Backend Framework" description="Lorem ipsum dolor sit, amet consectetur adipisicing elit. Vero eligendi quaerat tenetur doloremque, ipsum praesentium!" :skills="['Bootstrap', 'Nuxt', 'React', 'Vue']" />
            </div>
        </div>
    </div>
</template>

<style leng="css">
    #target:hover{
        background-color: aquamarine;
    }
    .skill-background{
        background: rgb(224,224,224);
background: radial-gradient(circle, rgba(224,224,224,1) 0%, rgba(252,252,252,1) 100%);
    }
</style>