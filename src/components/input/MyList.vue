<template>
  <div v-for="(list) in lists"  v-bind:key="list.id">
    <div  class="list" @click="list.dinamik = !list.dinamik" >
      <h3 
        class="prev"
        :class="{active: list.dinamik}"
      >>
      </h3>
      <input 
        type="checkbox" 
        class="list-input" 
        v-model="list.active"
        @click.stop="allSelected"
        :checked="selectAll"
      >
      <p>{{ list.title }}</p>
    </div>
    <div 
      class="deletItem"
      v-bind:ListAction="ListAction"
      :class="{activeList: list.dinamik}"
    >
      <Item 
      v-bind:items="list.items"
      v-on="selectAll"
      v-bind:Active="list.active"
      />
    </div>
  </div>
</template>

<script>
import Item from "../input/MyItem.vue";

export default {
  props: {
    lists:{
      type: Array,
      required: true
    }
  },
  components: {
    Item
  },
  data() {
    return {
      ListAction: false,
      AllItemActive: false
    }
  },
  methods: {
    setActive() {
      this.ListAction == true
    },
  }
}

</script>

<style>
.list {
  z-index: 10;
  background: #FFF;
  display: flex;
  cursor: pointer;
  width: auto;
  align-items: center;
}


.deletItem {
  display: none;
}

.activeList {
  display: block;
}

.active {
  transform: rotate(0.25turn);
  top: 0px;
}

.prev {
  font-size: 16px;
  position: relative;
  top: -1px;
  transition: ease-in .3s;
}

.list-input {
  margin: 10px 10px 10px 10px;
}
</style>