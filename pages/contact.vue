<script setup>
</script>

<template>
    <div class="h-full">
        <Header />
        <div class="project grid grid-cols-2 w-10/12 mx-auto">
            
            <div class="project-image flex justify-center py-4">
                <img src="@/assets/img/contact2.avif" class="max-h-[480px]" alt="">
            </div>

            <div class="flex flex-col py-4">
                <h1 class="text-5xl font-extrabold mb-10">CONTACT ME</h1>

                <div>
                    <label for="username" class="block text-sm font-medium leading-6 text-gray-900">Your Name</label>
                    <div class="mt-2">
                        <div class="flex pl-2 rounded-md shadow-sm ring-1 ring-inset ring-gray-300 focus-within:ring-indigo-600">
                        <input type="text" name="username" id="username" autocomplete="username" class="block flex-1 border-0 bg-transparent py-1.5 pl-1 text-gray-900 placeholder:text-gray-400 focus:ring-0" placeholder="Your Name...">
                        </div>
                    </div>
                </div>
                <div>
                    <label for="username" class="block text-sm font-medium leading-6 text-gray-900">Enter your Email Address</label>
                    <div class="mt-2">
                        <div class="flex pl-2 rounded-md shadow-sm ring-1 ring-inset ring-gray-300 focus-within:ring-indigo-600">
                        <input type="text" name="username" id="username" autocomplete="username" class="block flex-1 border-0 bg-transparent py-1.5 pl-1 text-gray-900 placeholder:text-gray-400 focus:ring-0" placeholder="username...">
                        </div>
                    </div>
                </div>
                <div class="mt-2">
                    <textarea id="about" name="about" rows="3" class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-indigo-600">Pls write down your problem here...</textarea>
                </div>

                <div class="w-1/3 bg-slate-50 my-2">
                    <!-- <span class="border inline-block flex-none p-1 bg-blue-400 m-0">
                    </span> -->
                    <button class="px-6 py-2 bg-blue-200 text-lg w-full">Submit</button>
                </div>
            </div>
        </div>

        <Footer />
    </div>
</template>

<style lang="css">
</style>