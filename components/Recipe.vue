<template>
    <nuxt-link :to="'/recipes/' + id">
        <article class="recipe">
            <div
                :style="{backgroundImage: `url('${thumbnail}')`}"
                class="thumbnail"/>
            <h1 v-text="title" />
            <p v-text="preview" />
        </article>
    </nuxt-link>
</template>

<script>
export default {
    name: "Recipe",
    props: {
        thumbnail: {
            type: String,
            required: true
        },
        title: {
            type: String,
            required:true
        },
        preview: {
            type: String,
            required: true
        },
        id: {
            type: Number,
            required: true
        }

    }
}
</script>

<style scoped>
a {
    text-decoration: none;
    color: black;
}
.recipe {
    box-sizing: border-box;
    width: 280px;
    padding: 8px;
    border: 1px solid #ccc;
    box-shadow: 0 2px 2px #eee;
}
.thumbnail {
    background-position: center;
    background-size: cover;
    width: 100%;
    height: 200px;
}
</style>
