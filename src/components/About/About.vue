<template>
  <div class="about">
    <h1>This about page</h1>
    <div>Hi {{theirName}}! Welcome to about page!</div>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Iure asperiores eligendi aliquam. Nemo voluptas laboriosam dignissimos corporis quibusdam error ex eligendi ut aliquid autem, magnam laborum fuga eos nam at!</p>
  </div>
</template>

<script>
export default {
  name: "About",
  data() {
    return {
      theirName: this.$route.params.name
    };
  }
};
</script>
