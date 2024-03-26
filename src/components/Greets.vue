<template>
    <div>
        <h2>Hello {{ name }}-{{ heroName }}</h2>
    </div>
</template>

<script>
export default {
    name: "Ahmad",
    props: ['name','heroName'],
    
}
</script>

<style scoped></style>