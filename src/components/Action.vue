<template>
  <b-button v-b-toggle="type" variant="outline-light">
    <b-container>
      <b-row>
        <img
          class="svg-action"
          viewBox="0 0 500 500"
          width="40vw"
          height="40vw"
          v-bind:src="svgURL"
        />
      </b-row>
      <b-row class="action-header">{{ title }}</b-row>
    </b-container>
  </b-button>
</template>
<script>
export default {
  props: { title: String, type: String, svgURL: String }
};
</script>

<style>
.action-header {
  display: block;
  margin-right: auto;
  margin-left: auto;
  color: white;
  cursor: pointer;
  font-size: 2.8vw;
  justify-content: center;
}
.svg-action {
  display: block;
  margin-right: auto;
  margin-left: auto;
  cursor: pointer;
  height: 8vw;
  width: 8vw;

  filter: invert(98%) sepia(0%) saturate(682%) hue-rotate(261deg);
}
</style>
