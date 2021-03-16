```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>test</title>
<script src="https://cdn.staticfile.org/vue/2.4.2/vue.min.js"></script>
</head>
<body>
<div id = "app">
	<p>input hour for test </p>
	<input v-model="hour" placeholder="input...">
	<p>{{ say }}</p>
</div>
<script type = "text/javascript">
 var now  = new Date();
 var hour = now.getHours();
 var Client = new Vue({
    el: '#app',
    data: {
       hour: hour
    },
    computed: {
       say:function(){
          if(this.hour < 12){ return "Good morning"} 
          else if (this.hour < 18){return "Good afternoon"}  
          else if (this.hour >18 && this.hour < 24){return "Good evening"} 
       }
  }
 });

</script>
</body>
</html>
```	
