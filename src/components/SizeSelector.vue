<script lang="ts" setup>
    const possibleSize = ['XS','S','M','L','XL'];


// javaScript
// const props = defineProps({
// selectedSize: { type: String, required: true }
// });

// const emits = defineEmits({
//  onChangeSize: String
//});


// TypeScript
const props = defineProps<{
    selectedSize: String
}>();

const emits = defineEmits<{
    ( event: 'onChangeSize' , value: String): void,
}>();

</script>

<template>

    <button 
        v-for="size in possibleSize"
        :class="{ 'active': props.selectedSize === size }"
        @click="emits('onChangeSize', size )"
        >
        {{size}}
    </button>

</template>