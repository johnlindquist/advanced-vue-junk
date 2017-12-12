<template>
  <div>
    <h1>
      {{renderButton}}
    </h1>
  </div>
</template>
<script>
import Vue from "vue"
import Component from "vue-class-component"

@Component({
  props: {
    renderButton: Function
  }
})
export default class Toggle extends Vue {}
</script>