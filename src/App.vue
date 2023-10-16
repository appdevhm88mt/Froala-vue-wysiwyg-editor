<template>
  <img alt="Vue logo" src="./assets/logo.png" />
    <froala
    id="edit"
    :tag="'textarea'"
    :config="config"
    v-model:value="model"
  ></froala>
  <h3>Content Preview</h3>
  <froalaView v-model:value="model"></froalaView>
</template>
<script>
export default {
  name: "App",
  data() {
    return {
      config: {
        //editor Options
        heightMin: 100,
        key:
          "YNB3fH3A7B7B7E5E3F2C-8zE2A5jqdE5ixnA3oD-16e1mD6F5F4G4E1A9D7C3B4E4==",

        //editor Events
        events: {
          initialized: function () {
            console.log("initialized");
          },
        },
      },
      //editor content
      model: "<i>Edit Your Content Here!</i>",
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
