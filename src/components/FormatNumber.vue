<template>
  <p>{{ formatted }}</p>
</template>

<script>
export default {
  props: {
    number: 50000,
  },

  computed: {
    formatted() {
      return new Intl.NumberFormat().format(this.number)
    },
  },
}
</script>
