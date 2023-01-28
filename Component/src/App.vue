<script>
  import props from './components/props.vue'
  import AlertBox from './components/AlertBox.vue'
  import vmodel from './components/vmodel.vue'
  export default{
    components: {
      vmodel
      // props,
      // AlertBox
    },
    data(){
      return{
        message: 'hello'
      }
    }
  }
  //   data(){
  //     return{
  //       posts:[
  //             {id: '1', title: 'How I started'},
  //             {id:'2', title:'Vue in View'},
  //             {id:'3', title:'How its going'}
  //       ],
  //       postFontSize: 1,
  //     }
  //   }
  // }
</script>
 
  <template>
 <vmodel v-model="message"/> {{ message }}

    <!-- <AlertBox>
      Something bad happened
    </AlertBox> -->
    <!-- <div :style="{ fontSize: postFontSize + 'em'}">
    <props 
    v-for="post in posts" 
    :key="post.id" 
    :title="post.title"
    @enlarge-text="postFontSize += 0.1">
   </props> -->
   <!-- </div> -->
  </template>

