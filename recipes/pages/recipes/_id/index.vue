<template>
    <section class="single-recipe">
        <h1>{{ recipe.title }}</h1>
        <div>
            <img class="recipe-image" src="recipe.thumbnail" alt="recipe.title">
        </div>
        <p>{{ recipe.descriptionText }}</p>
        <p>{{ recipe.contactText }}</p>
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
                          title: "Delicious f00d",
                          previewText: "Healthy f00d",
                          descriptionText: "What a tasty meal!",
                          thumbnail: "https://www.incimages.com/uploaded_files/image/970x450/getty_855098134_353411.jpg",
                          contactText: "habin@hotmail.co.uk"
                      },
                      {
                          id: "2",
                          title: "Even Healthier f00d",
                          previewText: "Super Healthy f00d",
                          descriptionText: "What a tasty meal!",
                          thumbnail: "https://www.incimages.com/uploaded_files/image/970x450/getty_855098134_353411.jpg",
                          contactText: "habin@hotmail.co.uk"
                      }
                  ].find(el => el.id === context.params.id)
              }, 1500)
          })
    })
  }
}
</script>


<style>
.single-recipe {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    flex-flow: column;
}

.recipe-image {
    width: 100%;
}
</style>

