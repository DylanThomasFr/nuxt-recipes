<template>
    <header>
        <nav>
            <ul>
                <li><nuxt-link to="/">Starting page</nuxt-link></li>
                <li><nuxt-link to="/recipes">Recipes</nuxt-link></li>
                <li><nuxt-link to="/about">About</nuxt-link></li>
            </ul>
        </nav>
    </header>
</template>

<script>
export default {
    name: "Header.vue"
}
</script>

<style scoped>
header {
    width: 100%;
    height: 30px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #521751;
}

ul {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;
}
li{
    margin: 0 10px;
}
a{
    text-decoration: none;
    color: #fff;
}
</style>
