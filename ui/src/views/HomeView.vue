<template>
    <div class="home">
        <img alt="Dominion Shirt" src="../assets/base_shirt.png" />
    </div>
</template>

<script>
export default {
    name: "HomeView"
};
</script>

<style lang="scss">
.home {
    width: 100vw;
    height: calc(100vh - 58px - 20px);

    display: grid;
    align-items: center;
    justify-items: center;

    img {
        display: block;
        max-width: 100%;
        max-height: 100%;
        width: auto;
        height: auto;
    }
}
</style>
