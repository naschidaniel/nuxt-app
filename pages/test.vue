<template>
    <div>
        <div>
            <NuxtLink to="/">index</NuxtLink><br />
            <NuxtLink to="/test">test</NuxtLink>
        </div>
        <input ref="input" />
    </div>
</template>

<script setup>
import { ref, watchEffect } from 'vue'

// declare a ref to hold the element reference
// the name must match template ref value
const input = ref(null)

watchEffect(() => {
    if (input.value) {
        console.log(input.value)
        console.log(input.value?.clientWidth)
    }
})
</script>
