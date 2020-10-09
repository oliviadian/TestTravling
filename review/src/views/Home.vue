<template>
  <div class="home">
    <Navbar />
    <div class="container" style="margin-top: 25px;">
      <!-- <Stars /> -->
      <Form />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
// import Stars from "@/components/Stars.vue";
import Form from "@/components/Form.vue";

export default {
  name: "Home",
  components: {
    Navbar,
    // Stars,
    Form,
  },
};
</script>

<style></style>
