<template>
    <section class="recipes">
        <recipe
            v-for="recipe in recipes"
            :key="recipe.id"
            :id="recipe.id"
            :thumbnail="recipe.thumbnail"
            :title="recipe.title"
            :preview="recipe.preview" />
    </section>
</template>

<script>
import Recipe from "@/components/Recipe";
export default {
    name: "Recipes.vue",
    components: {
        Recipe
    },
    asyncData() {
        return new Promise((resolve,reject) => {
            resolve({
                recipes: [
                    {
                        id: 1,
                        thumbnail: 'https://upload.wikimedia.org/wikipedia/commons/6/6d/Good_Food_Display_-_NCI_Visuals_Online.jpg',
                        title: 'Delicious pot au feu',
                        preview: 'Jelly beans soufflé fruitcake cupcake brownie liquorice. Macaroon halvah bonbon topping topping shortbread donut pudding.'
                    },
                    {
                        id: 2,
                        thumbnail: 'https://eatforum.org/content/uploads/2018/05/table_with_food_top_view_900x700.jpg',
                        title: 'Delicious pizza',
                        preview: 'Icing chocolate cake fruitcake fruitcake macaroon. Toffee fruitcake apple pie candy halvah macaroon powder jujubes lollipop.'
                    },
                ]
            })
        })
    }
}
</script>

<style scoped>
.recipes {
    display: flex;
    flex-flow: row;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
}
</style>
