<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<link rel="stylesheet" type="text/css" href="css/my.css">
</head>
<body>
	<div id="nav">
	  <parent :active="active" :navarr="navarr"></parent>
	</div>

	<template id="h">
		<div id="nav">  
	        <ul>  
	            <li v-for="(relation,index) in relations" v-bind:id="relation.id"  v-bind:id="relation.id" v-bind:class="{checked:index==nowIndex}"  v-on:click="relationClick(index)">  
	                <i></i>  
	                <span class="">{{relation.text}}</span>  
	            </li>  
	        </ul>  
	    </div>  
	</template>

</body>


</html>

<script type="text/javascript" src="node_modules/vue/dist/vue.js"></script>
<script type="text/javascript" src="node_modules/vue-resource/dist/vue-resource.js"></script>
  <script type="text/javascript">  
    var nav = new Vue({  
      el:'#nav',  
      data:{  
        relations: [  
          {text:'项目',id:'program'},  
          {text:'人员',id:'person'},  
          {text:'机构',id:'organization'},  
          {text:'技术',id:'tech'},  
          {text:'地区',id:'location'},  
          {text:'国家',id:'country'}  
        ],  
        nowIndex:-1,  
      },  
      methods:{  
        relationClick:function(index){  
          this.nowIndex=index;  
        }  
      }  
    });  
  </script>  