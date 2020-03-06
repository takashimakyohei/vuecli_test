<template>
  <div>
    <myheader></myheader>
    <p v-if="message.length > 0">
      {{message}}
    </p>
    <p v-else>
      no text
    </p>
    <input type="text" v-model="message">
    <button @click="clear()">clear</button>
  </div>
</template>

<script>
import myheader from '/Users/takashimakyouhei/workspace/sample/src/components/myheader'

export default {
  components: {
    myheader
  },
  data () {
    return {
      message: 'Hello World!'
    }
  },
  methods: {
    clear () {
      this.message = ''
    }
  }
}
</script>