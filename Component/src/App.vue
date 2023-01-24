<script setup>
import props from './components/props.vue'

export default{
  components: {
    props
  },

  data(){
    return{
      posts:[
            {id: '1', title: 'How I started'},
            {id:'2', title:'Vue in View'},
            {id:'3', title:'How its going'}
      ]
    }
  }
}
</script>

<template>
  <props v-for="post in posts :key="post.id" :title="post.title"></props>
</template>

