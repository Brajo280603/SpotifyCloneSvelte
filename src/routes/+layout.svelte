<script>
	import '../app.postcss';
</script>

<div class="flex h-screen font-sans font-bold">
	
	<div class="sideBar basis-1/4 my-2 mx-2 flex flex-col ">
		
		<div class="sideBarOptions bg-surface-700 basis-1/6 mb-2 rounded-lg flex flex-col">
			sidebar Options
			<div class="p-2">
				<a class="flex h-5 gap-4" href="">
					<img class="dark:invert" src="/home-icon.png" alt=""><p class="font-1">Home</p>
				</a>
			</div>
			<div>
				Search
			</div>

		</div>

		<div class="sideBarLibrary bg-surface-700 basis-5/6 rounded-lg">
			sidebar Library
		</div>

	</div>
	
	<slot class="basis-2/3"/> 

</div>
