<template>
  <div>
    <h1>{{$route.params.id}}</h1>
    <div v-if="albumExists">
      <div v-for="(album, index) in albumData" :key="index">
        <Card
        :title="album.collectionCensoredName"
        :img="album.artworkUrl100"
        :artistName="album.artistName"
        :url="album.artistViewUrl"
        />
      </div>
    </div>
    <div v-else>
      <h1>Could not find album.</h1>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import Card from '~/components/Card'
export default {
  asyncData({ params }) {
    return axios
      .get(`https://itunes.apple.com/search?term=${params.id}&entity=album`)
      .then(response => {
        return { albumData: response.data.results };
      });
  },
  middleware: "search",
  computed: {
    albumExists() {
      return this.albumData.length > 0;
    }
  },
  components: {
    Card
  },
  methods: {
    picker(index) {
      return index % 2 == 0 ? 'red' : 'blue';
    }
  }
};
</script>

<style>

</style>
