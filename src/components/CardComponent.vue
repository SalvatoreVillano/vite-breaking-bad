<template>
    <div class="character text-center">
        <img :src="character.img" :alt="character.name">
        <p>{{ character.name }}</p>
        <p>{{ character.category }}</p>
        <p>{{ character.status }}</p>
    </div>
</template>

<script>
export default {
    props: {
        character: Object
    },
    name: 'CardComponent',
}
</script>

<style lang="scss" scoped>
.character {
    img {
        max-height: 250px;
        max-width: 250px;
    }
}
</style>