<template>
  <div id="app">
    <b-button v-b-tooltip.hover title="Tooltip directive content">Hover Me</b-button>

    <b-button id="tooltip-target-1">Hover Me</b-button>
    <b-tooltip target="tooltip-target-1" triggers="hover">
      I am tooltip
      <b>component</b> content!
    </b-tooltip>
  </div>
</template>

<script lang="ts">
import "./app.scss";
import { Component, Vue } from "vue-property-decorator";
import { BButton, BTooltip, VBTooltip } from "bootstrap-vue";

@Component({
  components: {
    BButton,
    BTooltip
  },
  directives: {
    "b-tooltip": VBTooltip
  }
})
export default class App extends Vue {}
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
