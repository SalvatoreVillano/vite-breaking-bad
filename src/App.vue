<template>
  <HeaderComponent title="Breaking Bad API" />
  <main class="container">
    <SearchBar />
    <CharacterList />
  </main>
</template>

<script>
import axios from 'axios';
import HeaderComponent from './components/HeaderComponent.vue';
import SearchBar from './components/SearchBar.vue';
import CharacterList from './components/CharacterList.vue';
export default {
  components: {
    HeaderComponent,
    SearchBar,
    CharacterList,
  },
  data() {
    return {
      apiURL: 'https://www.breakingbadapi.com/api/characters',
      CharacterList: [],
      loading: false
    }
  },
  methods: {
    getCharacters() {
      this.loading = true;
      axios.get(this.apiURL).then(
        (res) => {
          this.CharacterList = [...res.data];
          console.log(this.CharacterList)
          this.loading = false;
        },
      )
        .catch((error) => {
          console.log(error)
        })
    }
  },
  created() {
    this.getCharacters();
  }
}

</script>

<style lang="scss" scoped>

</style>