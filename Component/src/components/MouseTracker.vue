<script>
    export default{
    data(){
        return{
        x:0,
        y:0
        }
    },
    methods:{
        update(e){
        this.x = e.pagex,
        this.y = e.pagey
        }
    },
    mounted() {
        window.addEventListener('mousemove', this.update)
    },
    unmounted() {
        window.removeEventListener('mousemove', this.update)
    }
    }
    
</script>
<template>
  <slot :x='x' :y="y"/>
  <p>{{ x }}</p>
</template>