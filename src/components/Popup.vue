<template>
    <div>
        <h2>This is the popup</h2>
        <button @click="$emit('close')">Closed Popup</button>
    </div>
</template>

<script>
export default {
    name: 'Popup',
    emits: ['close']
}
</script>

<style scoped></style>