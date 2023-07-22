<template>
    <div  
    class="items"  
    v-for="item in items" 
    v-bind:key="item.id" 
    >
      <div class="item-container">
      <input
      v-model="item.action"
      type="checkbox" 
      class="item"
      >
      <p>{{ item.title }}</p>
      </div>
      <div class="value-container">
      <input 
      type="number"
      class="value-item"
      v-model="item.value"
      >
      <input 
      type="color" 
      class="color-item"
      v-model="item.color"
      >
      </div>
    </div>
</template>

<script>
  export default {
    props:{
      items: {
        type: Array,
        required: true
      },
      Active: {
        type: Object,
        required: true
      }
    },
    data() {
      return {
        itemValue: 0,
        itemColor: "#ff0000",
      }
    },
    computed: {
    allSelected() {
      return this.items.every(item => item.action);
    }
  },
  methods: {
    selectAll() {
      let all_s = this.allSelected;
      this.items.forEach( item => item.action = !all_s );
      this.$emit("selectAll")
    },
  }
}
</script>

<style>


.item {
  margin: 0 15px 0 0 ;
}

.item-container {
  display: flex;
}

.items {
  z-index: -10;
  margin: 10px 0 10px 50px;
  display: flex;
  align-items: center;
  align-content: center;
  justify-content: space-between;
}

.value-container {
  display: flex;
  align-items: center;
}

.value-item {
  border: none;
  width: 20%;
  margin: 0;
  padding: 0;
}

.color-item {
  width: 21px;
  height: 23px;
  border: none;
  margin: 0;
  padding: 0;
}

</style>