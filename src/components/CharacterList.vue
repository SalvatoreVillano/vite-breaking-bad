<template>
    <div class="container">
        <div v-if="loading">
            Sto Caricando i dati
        </div>
        <div class="row" v-if="!loading">
            <div v-for="(item, index) in characters" :key="item.id" class="col-sm-6 col-md-4 col-lg-3">
                <CardComponent :character='item' />
            </div>
        </div>
    </div>
</template>

<script>
import CardComponent from './CardComponent.vue';

export default {
    name: "CharacterList",
    props: ["characters", "loading"],
    components: { CardComponent }
}
</script>

<style lang="scss" scoped>

</style>