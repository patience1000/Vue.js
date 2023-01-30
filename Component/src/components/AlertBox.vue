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
    <div class="card">
        <slot>box-content</slot>
    </div>
  <div class="container">
   <header>
    <h1>Here might be a page title</h1>
  </header>
  <main>
    <p>A paragraph for the main content.</p>
    <p>And another one.</p>
  </main>
  <footer>
    <p>Here's some contact info</p>
  </footer>
 </div>

</template>

<style scoped>
.card {
  color: #666;
  border: 1px solid red;
  border-radius: 4px;
  padding: 20px;
  background-color: #f8f8f8;
}
  
strong {
	color: red;    
}
</style>