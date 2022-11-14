<template>
    <div>
        Sono la lista dei personaggi
        <CardComponent />
    </div>
</template>

<script>
import CardComponent from './CardComponent.vue';

export default {
    name: "CharacterList",
    components: { CardComponent }
}
</script>

<style lang="scss" scoped>

</style>