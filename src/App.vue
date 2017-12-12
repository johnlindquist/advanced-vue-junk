<template>
  <div>
    <h1>Above</h1>
    {{renderButton()}}
    <h1>Below</h1>
  </div>
</template>
<script>
import Vue from "vue"
import Component from "vue-class-component"
import Toggle from "./Toggle"
import MyButton from "./MyButton"

@Component({
  components: {
    Toggle,
    MyButton
  }
})
export default class App extends Vue {
  mounted() {
    console.log(this.render)
  }
}
</script>