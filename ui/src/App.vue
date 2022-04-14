<script>
export default {
    name: "app",
    data() {
        return {
            flipLink: "/scoreboard"
        };
    },
    methods: {
        handleShirtFlip() {
            if (this.flipLink === "/scoreboard") {
                this.flipLink = "/";
            } else {
                this.flipLink = "/scoreboard";
            }
        }
    }
};
</script>

<template>
    <div id="navContainer">
        <nav>
            <router-link class="tab" @click="handleShirtFlip" :to="flipLink"
                ><img
                    class="icon"
                    alt="Flip"
                    src="./assets/icons8-replace-96.png"
            /></router-link>
            <!-- <router-link class="tab" to="/scoreboard">Champ</router-link> -->
            <a
                class="tab"
                href="https://www.teepublic.com/t-shirt/23352146-lucky7"
                ><img
                    class="icon"
                    alt="Store"
                    src="./assets/icons8-shop-100.png"
            /></a>
        </nav>
    </div>
    <router-view />
</template>

<style lang="scss">
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;

    width: 100vw;
    height: 100vh;
    overflow: hidden;
    margin: 0;
    padding: 0;
}

.tab {
    margin: 0 20px 0 20px;
}

#navContainer {
    height: 58px;
    display: grid;
    align-items: center;

    nav {
        .icon {
            max-height: 40px;
        }
        a {
            // font-weight: bold;
            // color: #2c3e50;

            &:hover {
                background-color: #42b9834d;
                transition: all 0.5s;
            }

            &.router-link-exact-active {
                color: #42b983;
            }
        }
    }
}
</style>
