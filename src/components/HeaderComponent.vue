<template>
    <header>
        <h1 class="text-center">{{ title }}</h1>
    </header>
</template>

<script>
export default {
    name: 'HeaderComponent',
    props: {
        title: String
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

h1 {
    font-weight: 700;
    color: $white;
}
</style>