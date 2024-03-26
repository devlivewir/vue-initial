<template>
    <div>
        <h2>Article Component</h2>
        <h2>{{ title }}</h2>
        <h2>{{ likes }}</h2>
        <h2>is published - {{ isBoolean ? 'Yes' : 'No' }}</h2>
    </div>
</template>

<script>
export default {
    name: 'Artical',
    props: {
        title: {
            type: String,
            required: true,
            default: 'Default title String'
        },
        likes: Number,
        isBoolean: Boolean
    }
}
</script>

<style scoped></style>