<template>
<nuxt-link :to="'/recipes/' + id">
    <article class="recipe">
        <div class="thumbnail" :style="{backgroundImage: 'url(' + thumbnail + ')'}"></div>
        <h1>{{ title }}</h1>
        <p>{{ previewText }}</p>
        <p>{{ contactText }}</p>
    </article>
</nuxt-link>
</template>

<script>
export default {
    props: ['thumbnail', 'title', 'id', 'previewText', 'contactText']
}
</script>


<style scoped>
a {
    text-decoration: none;
    color: black;
}
.recipes {
    display: flex;
    flex-flow: row;
    justify-content: center;
    align-items: center;
}

.recipe {
    box-sizing: border-box;
    width: 280px;
    padding: 8px;
    border: 1px solid lightslategray;
    box-shadow: 0 2px 2px lightcoral;
    margin: 10px;
}

.thumbnail {
    background-position: center;
    background-image: cover;
    width: 100%;
    height: 200px;
}
</style>