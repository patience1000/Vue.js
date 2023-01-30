<script>
  import props from './components/props.vue'
  import AlertBox from './components/AlertBox.vue'
  import vmodel from './components/vmodel.vue'
  export default{
    components: {
      // vmodel
      // props,
      AlertBox
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
  <AlertBox>
    <template #header>
    <h1>Here might be a page title</h1>
  </template>

  <!-- implicit default slot -->
  <p>A paragraph for the main content.</p>
  <p>And another one.</p>

  <template #footer>
    <p>Here's some contact info</p>
  </template>

  </AlertBox>
  <!-- <AlertBox> box1</AlertBox> -->
  <!-- <vmodel v-model="message"/> {{ message }} -->

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

