<script>
import props from './props.vue'

export default{
    components: {
        props
    },
    data (){
        return{
            posts: [
                        {id:'1', title:'Welcome back'},
                        {id: '2', title: 'First time'},
                        {id:'3',title: 'Vue in view'}
                   ]
                    
        }
    },  
}
</script> 
<template>
    <props v-for="post in post" :key='post.id' :title='post.title'/>
</template>