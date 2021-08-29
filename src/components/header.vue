<template>
  <header>
    <h1>{{ title }}</h1>
    <Button
      @btn-click="$emit('shownewTask')"
      :text="showbutton ? 'Close' : 'add task'"
      :color="showbutton ? 'red' : 'green'"
    />
  </header>
</template>

<script>
import Button from "./Button.vue";
export default {
  name: "Header",
  props: {
    title: String,
    showbutton: Boolean,
  },
  components: {
    Button,
  },
  // computed: {
  //   homePage() {
  //     if (this.$route.path === '/') {
  //       return true;
  //     } else {
  //       return false;
  //     }
  //   },
  // },
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>