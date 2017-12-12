<template>
  <div>
    <input v-model="msg">
    <p>prop: {{propMessage}}</p>
    <p>msg: {{msg}}</p>
    <p>helloMsg: {{helloMsg}}</p>
    <p>computed msg: {{computedMsg}}</p>
    <button @click="greet">Greet</button>
  </div>
</template>

<script>
import Vue from "vue"
import Component from "vue-class-component"

export default Component({
  props: {
    propMessage: String
  }
})(
  class NoDec extends Vue {
    msg = 123
    helloMsg = "Hello, " + this.propMessage

    mounted() {
      this.greet()
    }

    get computedMsg() {
      return "computed " + this.msg
    }

    greet() {
      console.log("greeting: " + this.msg)
    }
  }
)
</script>
