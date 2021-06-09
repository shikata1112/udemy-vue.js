<template>
  <div>
    <p>いいね ({{ totalNumber / 2 }})</p>
    <button @click="increment">UP</button>
  </div>
</template>

<script>
  export default {
    props: {
      totalNumber: {
        type: Number,
        required: true,
      },
    },
    methods: {
      increment() {
        this.$emit("my-click", this.totalNumber + 1);
      }
    }
  }
</script>
