<template>
  <div class="containet">
    <div class="main">
      <div class=container-list>
        <MyList :lists="lists"/>
      </div>
    </div>
    <div class="main">
      <div class="">
        <MyView :lists="lists"/>
      </div>
    </div>
  </div>
</template>

<script>
import MyList from './components/input/MyList.vue'
import MyView from './components/view/MyView.vue'

export default {
  components: {
    MyList,
    MyView
  },
  data() {
    return{
      lists:[
        {
          id: 1,
          title: "List 1",
          dinamik: false,
          active: false,
          items:[
          {
            title: "item 1",
            id: 1, 
            value: 2,
            action:false,
            color: "#ff0000"
          },
          {
            title: "item 2",
            id: 2, 
            value: 3, 
            action:false,
            color: "#ff0000"
          },          {
            title: "item 3",
            id: 1, 
            value: 2,
            action:false,
            color: "#ff0000"
          },
          {
            title: "item 4",
            id: 2, 
            value: 3, 
            action:false,
            color: "#ff0000"
          }
        ]
        },
        {
          id: 2,
          title: "List 2",
          dinamik: false,
          active: false,
          items:[
            {
            title: "item 1",
            id: 1, 
            value: 3,
            action:false,
            color: "#ff0000"
          },
          {
            title: "item 2",
            id: 2, 
            value: 5,
            action:false,
            color: "#ff0000"
          },
          {
            title: "item 3",
            id: 3, 
            value: 1,
            action:false,
            color: "#ff0000"
          },
          {
            title: "item 4",
            id: 4, 
            value: 0,
            action:false,
            color: "#000000"
          },
          {
            title: "item 5",
            id: 5, 
            value: 2,
            action:false,
            color: "#fefefe"
          },
          {
            title: "item 6",
            id: 6, 
            value: 10,
            action:false,
            color: "#ff0000"
          },
        ]
        },
        {
          id: 3,
          title: "List 3",
          dinamik: false,
          active: false,
          items:[
            {
            title: "item 1",
            id: 1, 
            value: 3,
            action:false,
            color: "#ff0000"
          },
          {
            title: "item 2",
            id: 2, 
            value: 5,
            action:false,
            color: "#ff0000"
          },
          {
            title: "item 3",
            id: 3, 
            value: 1,
            action:false,
            color: "#ff0000"
          },
          {
            title: "item 4",
            id: 4, 
            value: 0,
            action:false,
            color: "#000000"
          },
          {
            title: "item 5",
            id: 5, 
            value: 2,
            action:false,
            color: "#fefefe"
          },
          {
            title: "item 6",
            id: 6, 
            value: 10,
            action:false,
            color: "#ff0000"
          },
        ]
        },
        {
          id: 4,
          title: "List 4",
          dinamik: false,
          active: false,
          items:[
            {
            title: "item 1",
            id: 1, 
            value: 3,
            action:false,
            color: "#ff0000"
          },
          {
            title: "item 2",
            id: 2, 
            value: 5,
            action:false,
            color: "#ff0000"
          },
          {
            title: "item 3",
            id: 3, 
            value: 1,
            action:false,
            color: "#ff0000"
          },
          {
            title: "item 4",
            id: 4, 
            value: 0,
            action:false,
            color: "#000000"
          },
          {
            title: "item 5",
            id: 5, 
            value: 2,
            action:false,
            color: "#fefefe"
          },
          {
            title: "item 6",
            id: 6, 
            value: 10,
            action:false,
            color: "#ff0000"
          },
        ]
        },
        {
          id: 5,
          title: "List 5",
          dinamik: false,
          active: false,
          items:[
            {
            title: "item 1",
            id: 1, 
            value: 3,
            action:false,
            color: "#ff0000"
          },
          {
            title: "item 2",
            id: 2, 
            value: 5,
            action:false,
            color: "#ff0000"
          },
          {
            title: "item 3",
            id: 3, 
            value: 1,
            action:false,
            color: "#ff0000"
          },
          {
            title: "item 4",
            id: 4, 
            value: 0,
            action:false,
            color: "#000000"
          },
          {
            title: "item 5",
            id: 5, 
            value: 2,
            action:false,
            color: "#fefefe"
          },
          {
            title: "item 6",
            id: 6, 
            value: 10,
            action:false,
            color: "#ff0000"
          },
          {
            title: "item 7",
            id: 3, 
            value: 1,
            action:false,
            color: "#ff0000"
          },
          {
            title: "item 8",
            id: 4, 
            value: 0,
            action:false,
            color: "#000000"
          },
          {
            title: "item 9",
            id: 5, 
            value: 2,
            action:false,
            color: "#fefefe"
          },
          {
            title: "item 10",
            id: 6, 
            value: 10,
            action:false,
            color: "#ff0000"
          },
        ]
        }
      ]
    }
  },
  methods: {
  }
}
</script>

<style>
*{
  font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

.containet {
  padding: 30px;
  display: flex;
  justify-content: space-between;
}

.main{
  padding: 20px;
  border: 1px solid #000;
  min-height: 90vh;
  height: auto;
  width: 60vh;
}

</style>
