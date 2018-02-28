<template id="nav">
	<div>
		{{title}}
	</div>

</template>

<script>
	Vue.component('navhead',{
			template: '#nav',
			props:['title']
	});

</script>