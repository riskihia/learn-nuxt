<script setup lang="ts">
    // const {sayHello} = useUtils();
    // sayHello();

    const { $sayHello } = useNuxtApp();
    $sayHello("RISKI");
</script>

<template>
    <div>
        <Alert />
        <Profile />

        <img src="@/assets/img/avatar1.png" />
    </div>
</template>