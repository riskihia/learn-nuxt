<script setup>
import { ref } from 'vue';

// Define a reactive variable to store user input for bg color
const bgColorInput = ref('blue-400');

// Function to update bg color when user changes the input
const updateBgColor = (color) => {
    bgColorInput.value = color;
}

// Function to generate the class value based on user input and default values
const generateClassValue = () => {
    const mergedStyles = { ...defaultValue, bg: bgColorInput.value };
    return Object.entries(mergedStyles).map(([key, value]) => {
        return `${key === 'bg' ? 'bg' : key}-${value}`;
    }).join(' ');
}

// Logging user input
console.log(bgColorInput.value);

// Your default value object
let defaultValue = {
    "bg": "red-400",
    "px": "4",
    "py": "4",
    "mb": "4",
}

// Logging default value
console.log(defaultValue);

// Logging class value
console.log(generateClassValue());

</script>

<template>
    <div>
        <!-- Input field for bg color -->
        <input type="text" class="text-black" v-model="bgColorInput" @input="generateClassValue" placeholder="Enter bg color">
        <IconsBell />
        <!-- Display the generated class value -->
        <div :class="generateClassValue()">
            This is an alert component.
        </div>

        <div>
            <img src="@/assets/img/avatar.jpg"/>
        </div>
    </div>
</template>

<style lang="css"></style>
