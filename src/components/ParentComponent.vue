<template>
  <div class="parent">
    <h1>Item List</h1>
    <ChildComponent
      v-for="item in itemList"
      :key="item.id"
      :item="item"
      @show-detail="showDetail" />
    <DetailComponent v-if="selectedItem" :item="selectedItem" />
  </div>
</template>

<script>
import ChildComponent from './ChildComponent.vue';
import DetailComponent from './DetailComponent.vue';

export default {
  components: {
    ChildComponent,
    DetailComponent
  },
  data() {
    return {
      itemList: [
        { id: 1, name: 'Item 1', description: 'Description of Item 1' },
        { id: 2, name: 'Item 2', description: 'Description of Item 2' },
        { id: 3, name: 'Item 3', description: 'Description of Item 3' }
      ],
      selectedItem: null
    };
  },
  methods: {
    showDetail(item) {
      this.selectedItem = item;
    }
  }
};
</script>

<style scoped>
.parent {
  padding: 20px;
  background-color: #090a55;
  border-radius: 10px;
}
</style>
