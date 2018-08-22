<template>
    <section class="recipes">
        <Recipe thumbnail="https://www.incimages.com/uploaded_files/image/970x450/getty_855098134_353411.jpg"
                title="Delicious f00d"
                id="1"
                previewText="Healthy f00d"/>
        <Recipe thumbnail="https://www.incimages.com/uploaded_files/image/970x450/getty_855098134_353411.jpg"
                title="Even Healthier f00d"
                id="2"
                previewText="Super Healthy f00d"/>
    </section>
</template>

<script>
import Recipe from '@/components/Recipe'

export default {
    components: {
        Recipe
    }
}
</script>
