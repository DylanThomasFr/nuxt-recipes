<template>
    <section class="single-recipe">
        <h1>{{ recipe.title }}</h1>
        <div>
            <img
                class="recipe-image"
                :src="recipe.thumbnail"
                :alt="recipe.title">
        </div>
        <p>{{ recipe.preview }}</p>
    </section>
</template>

<script>
export default {
    name: "index.vue",
    asyncData(context) {
        return new Promise(resolve => {
            resolve({
                recipe: [
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
                ].find(el => el.id === parseInt(context.params.id)),
            })
        })
    }
}
</script>

<style scoped>
.single-recipe {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    flex-flow: column;
    padding: 30px;
}
.recipe-image {
    width: 100%;
    height: 250px;
}
</style>
