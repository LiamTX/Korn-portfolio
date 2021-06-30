<template>
  <v-container>
    <v-card :loading="loading" class="mx-auto my-12" max-width="374">
      <template slot="progress">
        <v-progress-linear
          color="deep-purple"
          height="10"
          indeterminate
        ></v-progress-linear>
      </template>

      <v-img height="250" :src="album.img"></v-img>

      <v-card-title>
        <strong>{{ album.title }}</strong>
      </v-card-title>

      <v-card-text>
        <div>
          <p>
            {{ album.about }}
          </p>
        </div>
      </v-card-text>

      <v-divider class="mx-4"></v-divider>

      <v-card-text> </v-card-text>
    </v-card>
  </v-container>
</template>

<script>
export default {
  props: ["data"],

  data: () => ({
    album: {
      img: "",
      title: "",
      about: "",
    },
  }),

  created() {
    this.album.img = this.data.img;
    this.album.title = this.data.title;
    this.album.about = this.data.about;
  },
};
</script>