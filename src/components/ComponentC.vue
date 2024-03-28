<template>
    <div>
        <h2>Component C</h2>
        <ComponentE />
    </div>
</template>

<script>
import ComponentE from './components/ComponentE';
export default {
    name:'ComponentC',
    components:{
        ComponentE
    }

}
</script>

<style scoped></style>