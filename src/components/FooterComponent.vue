<template>
  <v-footer class="bg-grey-lighten-1">
    <v-row justify="center" no-gutters>
      <v-btn
        v-for="link in links"
        :key="link"
        color="white"
        variant="text"
        class="mx-2"
        rounded="xl"
      >
        {{ link }}
      </v-btn>
      <v-col class="text-center mt-4" cols="12">
        {{ new Date().getFullYear() }} — <strong>Groupomania</strong>
      </v-col>
    </v-row>
  </v-footer>
</template>

<script>
export default {
  name: "FooterComponent",
  data: () => ({
    links: ["Home", "About Us", "Team", "Services", "Blog", "Contact Us"],
  }),
};
</script>

<style scoped>
.v-footer {
  color: white;
  background-color: #212121 !important;
  padding: 0 0 0 0;
  margin: 0 0 0 0;
  height: 250px;
  width: 100%;
  position: static;
  bottom: 0;
  left: 0;
  right: 0;
  z-index: 1;
}
@media (max-width: 768px) {
  v-footer {
    height: 260px;
  }
}
</style>
