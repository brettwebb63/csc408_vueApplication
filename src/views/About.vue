<template>
  <div class="about">
    <h2>The Yellow Bucket App</h2>
    <p>Yellow Bucket is the next wave in movie rental technology.  The App is a strategic
    piece of making rentals available anywhere you have a phone or tablet. The app is in its early
    stages and provides administrative functions.</p>
    <p id="td1"> {{greetings}} </p>
  </div>
</template>
<script>
    var today = new Date()
    var curHr = today.getHours()
    
    new Vue({
        el: '#td1' ,
        data: ()=>({
            greeting : 'Test'
        }),
        methods: {
            greetings(){
                if (curHr < 12) {
                    console.log('good morning')
                } else if (curHr < 18) {
                    console.log('good afternoon')
                } else {
                    console.log('good evening');
                }
            }
        }
    });
</script>
<style>

</style>