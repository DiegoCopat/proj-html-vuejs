<template>
    <div class="card">
        <img :src="singularProduct.src" alt="singularProduct.titolo">
    </div>
</template>

<script>
export default {
    name: "Card",
    proprs: ["singularProduct"]

}
</script>

<style lang="scss" scope>
    .card {
        width: calc(100% / 3);
        height: 200px;
        img {
            width: 100%; 
        }
    }
</style>