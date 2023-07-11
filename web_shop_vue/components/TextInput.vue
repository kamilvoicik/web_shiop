<template>
  <div></div>
</template>

<script setup>
const emit = defineEmits(["update:input"]);

const props = defineProps([
  "input",
  "placeholder",
  "max",
  "inputType",
  "error",
]);

const { input, placeholder, max, inputType, error } = toRefs(props);
let isFocusd = ref(false);

const inputComputed = computed({
  get: () => input.value,
  set: (value) => emit("update:input", val),
});
</script>

<style lang="scss" scoped></style>
