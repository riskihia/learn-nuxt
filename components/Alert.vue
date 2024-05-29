<script setup>
let dataUser = {
    "bg" : "pink-400",
    "px" : "2",
    "py" : "1",
    "mb" : "2",
}

const userValue = Object.entries(dataUser).map(([key, value]) => {
    return `${key === 'bg' ? 'bg' : key}-${value}`;
}).join(' ');

console.log(userValue);

let defaultValue = {
    "bg" : "red-400",
    "px" : "4",
    "py" : "4",
    "mb" : "4",
}

const defaultValueString = Object.entries(defaultValue).map(([key, value]) => {
    return `${key === 'bg' ? 'bg' : key}-${value}`;
}).join(' ');

console.log(defaultValueString);

// Merge dataUser into defaultValue
let mergedStyles = { ...defaultValue };

Object.keys(dataUser).forEach(key => {
    if (dataUser[key]) {
        mergedStyles[key] = dataUser[key];
    }
});

console.log(mergedStyles);

// Convert mergedStyles object to a string
const classValue = Object.entries(mergedStyles).map(([key, value]) => {
    return `${key === 'bg' ? 'bg' : key}-${value}`;
}).join(' ');

console.log(classValue);

</script>

<template>
    <div :class="userValue">
        USER VALUE
    </div>
    <div :class="defaultValueString">
        DEFAULT VALUE
    </div>
    <div :class="classValue">
        MERGED VALUE
    </div>
    <div class="bg-indigo-400 px-2 py-1 mb-2">
        MANUAL CLASS
    </div>
</template>

<style lang="css"></style>
