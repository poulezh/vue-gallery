<template>
  <v-container>
    <v-row>
          <Photo v-for="photo in photos" :key="photo.id" :photo="photo"> </Photo>
    </v-row>
  </v-container>
</template>

<script>
import Photo from "@/components/photo/Photo.vue";
export default {
  data: () => ({
    photos: [],
  }),
  components: { Photo },
  mounted() {
    this.fetchTodo()

  },
  methods: {
    fetchTodo(){
      this.axios.get("https://jsonplaceholder.typicode.com/photos?_limit=10")
      .then(response => this.photos = response.data)

    }

  }
};
</script>

<style scoped></style>
