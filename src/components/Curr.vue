<!-- eslint-disable vue/multi-word-component-names -->
<!-- eslint-disable prettier/prettier -->
<template>
    {{ dollar(amt) }}
</template>

<script>
export default {
  props: ['amt'],
  methods: {
    dollar(value) {
      return '$' + Number.parseFloat(value).toFixed(2)
    }
  }
}
</script>

<style></style>
