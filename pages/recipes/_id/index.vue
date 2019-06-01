<template>
  <section class="single-card-recipe">
    <h1>{{recipe.title}}</h1>
    <div>
      <img class="recipe-image" :src="recipe.thumbnail" :alt="recipe.title">
    </div>
    <p>{{recipe.description}}</p>
  </section>
</template>

<script>
export default {
  asyncData(context) {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          recipe: [
            {
              id: "1",
              title: "Pizza",
              previewText:
                "Pizza vegana cocinada con los mejores ingredientes naturales.",
              description: "una deliciosa comida!",
              thumbnail:
                "https://www.cilantroandcitronella.com/wp-content/uploads/2017/10/vegan-nacho-pizza-photo.jpg"
            },

            {
              id: "2",
              title: "Hamburguesa",
              previewText:
                "Hamburguesa 100% de vacuno preparada por chefs expertos.",
              description: "una deliciosa comida!",
              thumbnail:
                "https://okdiario.com/img/2018/10/26/hamburguesas-de-pollo-y-pimientos-655x368.jpg"
            }
          ].find(el => el.id === context.params.id)
        });
      }, 1500);
    });
  }
};
</script>


<style scoped>
.single-card-recipe {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  flex-flow: column;
  padding: 30px;
}
.recipe-image {
  width: 100%;
}
</style>
