<script>
export default {
    props:[ 'title'],
    emits: ['enlarge-text']
}
</script>

<template>
   <h4>{{ title }}</h4> 
   <button @click="$emit('enlarge-text')">Enlarge text</button>
</template>
