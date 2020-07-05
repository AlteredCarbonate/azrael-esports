<template>
	<div id="section" class="second text-center flex">
		<div id="apex" class="w-2/6 my-10">
			<apexglobalseries class="pt-5 sm:pt-10 lg:pt-16 md:pt-12 px-4 w-full h-48 lg:h-56 xl:h-64" color="white"
				detail="#a4adb0" stroke="black" />
		</div>
		<div class="w-4/6 mt-10 text-white">
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Tenetur
			consequatur eos, iste mollitia nulla reiciendis reprehenderit accusantium
			ratione maxime quidem, non harum nostrum dolorem error id beatae, commodi
			laboriosam aliquam.
		</div>
	</div>
</template>

<script>
	import apexglobalseries from "@/components/Logos/apexglobalseries.vue";

	export default {
		name: "secTwo",
		components: {
			apexglobalseries
		}
	};
</script>

<style scoped>
	#section #apex {
		background-image: url("../../../assets/background/red_background3.png");
		background-size: contain;
		background-repeat: no-repeat;
		background-position: top;
	}
</style>