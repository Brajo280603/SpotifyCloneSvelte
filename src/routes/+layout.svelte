<script>
	import '../app.postcss';
	let current ;
	$: {
		current = "home";
	}

	import { LightSwitch } from '@skeletonlabs/skeleton';
	import BasicLibraryCards from '../lib/basic_library_cards.svelte';
</script>

<div class="flex h-screen font-sans ">
	
	<div class="sideBar basis-1/5 my-2 mx-2 flex flex-col ">
		
		<div class="sideBarOptions sub-bg mb-2 rounded-lg flex flex-col font-bold  text-xs">
			<div class="OptionsHome pt-3 pb-2 px-5">
				<a class="flex h-5 gap-4 align-center hover:brightness-200 transition duration-500 {current == "home" ? "brightness-100" : "brightness-50" }" href="/" on:click={()=>{current = "home"}}>
					<img class="dark:invert" src="/home-icon.png" alt=""><p class=" ">Home</p>
				</a>
			</div>
			
			<div class="OptionsSearch pb-3 pt-2 px-5">
				<a class="flex h-5 gap-4 hover:brightness-200 transition duration-500 {current == "search" ? "brightness-100" : "brightness-50" }" href="/search" on:click={()=>{current = "search"}}>
					<img class="dark:invert" src="/search-icon.png" alt=""><p class="">Search</p>
				</a>
			</div>

		</div>

		<div class="sideBarLibrary sub-bg grow rounded-lg  p-1 text-xs leading-6 flex flex-col justify-between"> <!--py-3 ps-5 pe-3-->
			
			<div class="LibraryHeading flex h-6  gap-4  w-100 font-bold my-2 ms-4 me-2 ">
				<div class="flex w-full ">
					<div class="brightness-50 h-full flex hover:brightness-200 transition duration-500 gap-4 cursor-pointer">
						<img src="/collection-icon.png" alt="" class="dark:invert "><p class="">Library</p>
					</div>
					<div class="grow flex justify-end">
						<button class="h-full rounded-full hover:bg-surface-700/[0.5] p-1 brightness-50 hover:brightness-200 transition duration-500" >
							<img src="/add-icon.png" alt="" class="h-full dark:invert">
						</button>
					</div>
					
				</div>
			</div>

			<div class="LibraryFiles grow mx-1">
				
				<BasicLibraryCards title="Create your first playlist" text="it's easy, we'll help you" btnText="Create playlist"></BasicLibraryCards>
				<BasicLibraryCards title="Let's find some podcasts to follow" text="We'll keep you updated on new episodes" btnText="Browse podcasts"></BasicLibraryCards>
			</div>
			
			<div class="LibraryFooter mx-3 mb-2">
				<div class=" dark:font-normal font-bold tracking-widest antialiased" style="font-size: 0.45rem;">
					<div class="flex gap-2">
						<span>Legal</span>
						<span>Privacy Center</span>
						<span>Privacy Policy</span>
						<span>Cookies</span>
						<span>About Ads</span>
					</div>
	
					<div>
						Accessibility
					</div>
	
					<div>
						Cookies
					</div>
				</div>

				<div class="py-3 flex justify-between mt-3">
					
					<button class="border border-current rounded-full px-3 flex items-center gap-1">
						<img src="/web-icon.png" alt="" class="h-4 dark:invert"><span>English</span>
					</button>

					<LightSwitch></LightSwitch>
				</div>

				
			</div>

		</div>

	</div>
	
	<slot class="basis-2/3"/> 

</div>


