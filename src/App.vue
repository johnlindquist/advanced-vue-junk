<template>
  <div>
    <h1>{{message}} 😎</h1>
  </div>
</template>

<script>
import Vue from "vue"
import Component from "vue-class-component"

@Component({})
export default class App extends Vue {
  message = "Hello world"
}
</script>