
<template>
  <div class="math-label" v-html="renderedMath"></div>
</template>

<script setup>
import { computed } from 'vue'
import katex from 'katex'
import 'katex/dist/katex.min.css'

const props = defineProps({
  expr: {
    type: String,
    required: true,
  },
})

const renderedMath = computed(() =>
  katex.renderToString(props.expr, {
    throwOnError: false,
    displayMode: false,
  })
)
</script>

<style>
.math-label {
  font-size: 16px;
  text-align: center;
  line-height: 1.5;
}
</style>

