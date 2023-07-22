<template>
    <div class="block-view" v-for="(list, index) in lists"  v-bind:key="index">
        <div class="top-title">
            <p>{{list.title }}</p>
            <button
            v-on:click="shuffle"
            >Перемешать</button>
        </div>
        <div class="">
            <div    
            v-for="item in list.items" 
            v-bind:key="item.id" 
            >
                <div class="container-color" >
                    <div 
                        v-for="(j,index) in item.value"
                        v-bind:key="index"
                        class="color-block"
                        :class="{activeColor: item.action}"
                        :style="{background: item.color}"
                    >
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    props: {
        lists:{
            type: Array,
            required: true
        },
        items: {
                type: Array,
                required: true
        },
    },
    data() {
        return {
            shuffledNumbers: null
        }
    },
    methods: {
    shuffle() {
    }
  },
  mounted() {
    this.shuffle();
    }

}
</script>

<style>
.block-view {
    margin: 5px;
    border: 1px solid #000
}

.top-title {
    margin: 2px;
    display: flex;
    justify-content: space-between
}

.color-block {
    margin: 2px 2px 5px 2px;
    width: 10px;
    height: 10px;
    background: #000;
    display: none;
}

.container-color {
    display: flex;
    flex-wrap: wrap;
}

.activeColor {
 display: block;
}
</style>