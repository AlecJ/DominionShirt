<template>
    <div id="navContainer">
        <nav>
            <router-link class="tab" to="/">Home</router-link>
            <router-link class="tab" to="/champ">Champ</router-link>
            <a
                class="tab"
                href="https://www.teepublic.com/t-shirt/23352146-lucky7"
                >Store</a
            >
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
        a {
            font-weight: bold;
            color: #2c3e50;

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
