<template>
  <div id="editor">
    <textarea :value="input" @input="update"></textarea>
    <div v-html="compiledMarkdown"></div>
  </div>
</template>

<script>
import marked from 'marked'
import _ from 'lodash'

export default {
  name: 'bob-editor',
  data () {
    return {
      input: ''
    }
  },
  computed: {
    compiledMarkdown: function () {
      return marked(this.input, { sanitize: true })
    }
  },
  methods: {
    update: _.debounce(function (e) {
      this.input = e.target.value
    }, 300)
  }
}
</script>

<style scoped>
textarea, #editor div {
  display: inline-block;
  width: 49%;
  height: 95vh;
  vertical-align: top;
  box-sizing: border-box;
  padding: 0 20px;
  line-height: 1.2em;
}

textarea {
  border: none;
  resize: none;
  outline: none;
  background-color: #f6f6f6;
  font-size: 14px;
  padding: 10px;
}

</style>
