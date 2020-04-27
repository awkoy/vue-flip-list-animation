<template>
    <transition-group name="flip" class="flip-list" tag="div" :style="{ '--total': listData.length }" appear>
        <div class="flip-list__item" v-for="(el, i) in listData" :key="el.id" :style="{'--i': i}">
            <FlipItem :item="el" />
        </div>
    </transition-group>
</template>

<script>
import FlipItem from './FlipItem.vue'

export default {
  name: 'FlipList',
  data: function(){
      return {
          listData: [
              {
                  id: 'jkgfdskl',
                  imgSrc: "http://lorempixel.com/200/200",
                  content: "This is back part 1"
              },
              {
                  id: 'jkgfdskl2',
                  imgSrc: "http://lorempixel.com/200/200",
                  content: "This is back part 2"
              },
              {
                  id: 'jkgfds3kl',
                  imgSrc: "http://lorempixel.com/200/200",
                  content: "This is back part 3"
              },
              {
                  id: 'jkg4fdskl',
                  imgSrc: "http://lorempixel.com/200/200",
                  content: "This is back part 4"
              },
              {
                  id: 'jkgf5dskl',
                  imgSrc: "http://lorempixel.com/200/200",
                  content: "This is back part 5"
              },
              {
                  id: 'jkgf6dskl',
                  imgSrc: "http://lorempixel.com/200/200",
                  content: "This is back part 6"
              }
          ]
      }
  },
  components: {
    FlipItem
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.flip-list {
    display: flex;
    flex-wrap: wrap;
}
.flip-list__item {
    display: flex;
    align-self: center;
    justify-content: center;
    text-transform: uppercase;
    font-weight: bold;
    margin: 30px;
}
</style>
