<template>
    <section class="recipes">
        <Recipe 
            v-for="recipe in recipes"
            :key="recipe.id"
            :thumbnail="recipe.thumbnail"
            :title="recipe.title"
            :id="recipe.id"
            :previewText="recipe.previewText"
            :contactText="recipe.contactText"
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
                          title: "Delicious f00d",
                          previewText: "Healthy f00d",
                          thumbnail: "https://www.incimages.com/uploaded_files/image/970x450/getty_855098134_353411.jpg",
                          contactText: "habin@hotmail.co.uk"
                      },
                      {
                          id: "2",
                          title: "Even Healthier f00d",
                          previewText: "Super Healthy f00d",
                          thumbnail: "https://www.incimages.com/uploaded_files/image/970x450/getty_855098134_353411.jpg",
                          contactText: "habin@hotmail.co.uk"
                      },
                  ]
              }, 1500)
          })
      })
    }
}
</script>
