<template>
  <section class="recipes">
    <Recipe
      v-for="recipe in recipes"
      :key="recipe.id"
      :id="recipe.id"
      :thumbnail="recipe.thumbnail"
      :title="recipe.title"
      :previewText="recipe.previewText"
    />
  </section>
</template>

<script>
import Recipe from "@/components/Recipe";

export default {
  components: {
    Recipe
  },

  asyncData() {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          recipes: [
            {
              id: "1",
              title: "Pizza",
              previewText:
                "Pizza vegana cocinada con los mejores ingredientes naturales.",
              thumbnail:
                "https://www.cilantroandcitronella.com/wp-content/uploads/2017/10/vegan-nacho-pizza-photo.jpg"
            },

            {
              id: "2",
              title: "Hamburguesa",
              previewText:
                "Hamburguesa 100% de vacuno preparada por chefs expertos.",
              thumbnail:
                "https://okdiario.com/img/2018/10/26/hamburguesas-de-pollo-y-pimientos-655x368.jpg"
            }
          ]
        });
      }, 1500);
    });
  }
};
</script>


<style scoped>
.recipes {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items: center;
}
</style>
