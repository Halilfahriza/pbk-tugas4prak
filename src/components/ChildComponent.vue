<template>
  <div class="child" @click="emitDetail">
    <h2>{{ item.name }}</h2>
    <p>{{ item.description }}</p>
  </div>
</template>

<script>
export default {
  props: {
    item: Object
  },
  methods: {
    emitDetail() {
      this.$emit('show-detail', this.item);
    }
  }
};
</script>

<style scoped>
.child {
  border: 1px solid #ccc;
  padding: 10px;
  margin: 10px 0;
  cursor: pointer;
  transition: background-color 0.3s ease;
}
.child:hover {
  background-color: #e0f7fa;
}
</style>
