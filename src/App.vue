<template>
  <HeaderComponent />
  <SearchBar />
  <CharacterList />
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import SearchBar from './components/SearchBar.vue';
import CharacterList from './components/CharacterList.vue';
export default {
  components: {
    HeaderComponent, SearchBar, CharacterList
  }
}
</script>

<style lang="scss" scoped>

</style>