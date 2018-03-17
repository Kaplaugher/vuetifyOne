<template>
  <div>
    <div class="card-container">
      <v-card target="_blank" :href="url" :color="color" class="card">
        <v-card-title primary-title>
          <div class="headline">{{title}}</div>
          <div>{{artistName}}</div>
        </v-card-title>
        <v-card-media :src='img' height="100px" contain>
        </v-card-media>
        <v-card-actions>
          <v-btn flat dark>Listen now</v-btn>
        </v-card-actions>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {
  props: ['title', 'img', 'artistName', 'url',]
};
</script>

<style>

.card-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.card {
  height: 150px;
  width: 400px;

}

</style>
