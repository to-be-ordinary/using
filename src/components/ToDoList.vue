<template>
    <li @click="clickHandle">{{item}}</li>
</template>
<script>
export default {
  props: [
    'item',
    'index'
  ],
  methods: {
    clickHandle: function () {
      this.$emit('delete', this.index)
    }
  }
}
</script>
