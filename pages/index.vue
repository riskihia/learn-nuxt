<script setup>
    const {sayHello} = useUtils();
    sayHello();
</script>

<template>
    <div>
        <Alert />
        <Profile />

        <img src="@/assets/img/avatar1.png" />
    </div>
</template>