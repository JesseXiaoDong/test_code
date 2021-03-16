<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>test</title>
<script src="https://cdn.staticfile.org/vue/2.4.2/vue.min.js"></script>
</head>
<body>
<div id = "app">
	<p style = "font-size:25px;">{{ say }}</p>
</div>
<script type = "text/javascript">
 var Client = new Vue({
    el: '#app',
    data: {
       now: new Date()
    },
	computed: {
       hour: function () {
          return this.now.getHours();
       },
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
