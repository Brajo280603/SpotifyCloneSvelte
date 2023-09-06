<script>
	import '../app.postcss';
</script>

<div class="flex h-screen">
	
	<div class="sideBar basis-1/3 my-2 mx-2 flex flex-col h-full">
		
		<div class="sideBarOptions bg-surface-700 basis-1/6 mb-2">
			sidebar Options
		</div>

		<div class="sideBarLibrary bg-surface-700 basis-5/6">
			sidebar Library
		</div>

	</div>
	
	<slot class="basis-2/3"/> 

</div>
