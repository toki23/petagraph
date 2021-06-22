<template>
<div>
    <h1>データを入れてください</h1>
    <input v-model="message" placeholder="edit me">
    <p>Message is: {{ message }}</p>
</div>
</template>

<script>
export default {
 data () {
   return {
     message: ''
   }
 },
 }
</script>