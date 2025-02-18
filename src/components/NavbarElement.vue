<template>
    <nav class="w-screen fixed bg-opacity-90 bg-white p-4 lg:px-20 flex justify-between z-50 bg-blue-1000">
		
		<div class="h-full flex flex-row items-start justify-start justify-self-start">
			<img src="../../img/Poste.png" class="w-16 h-16">
			<div class="flex-col items-center ml-4 self-center">
				<p class="tracking-widest font-semibold text-black">La Poste</p>
				<p class="tracking-widest font-light text-black self-start">Tunisienne</p>
			</div>
		</div>

		<button role="menubar" class="md:hidden" @click="navToggle()">
			<i class="fa-solid fa-bars text-2xl"></i>
		</button>

		<div class="absolute left-0 right-0 translate-y-16 bg-opacity-90 bg-white md:bg-none md:bg-opacity-0 shadow hidden md:flex flex-col gap-4 items-center p-4 md:flex-row md:static md:shadow-none md:translate-y-0" role="menu" aria-expanded="false">

			<a href="#" role="menuitem">
				<p class="mx-4 text-black">La Poste</p>
			</a>

			<a href="#historique" role="menuitem">
				<p class="mx-4 text-black">Historique</p>
			</a>

			<a href="#service" role="menuitem">
				<p class="mx-4 text-black">Services</p>
			</a>

			<button class="p-4 rounded-2xl transition-all duration-300 text-black hover:shadow-md bg-[#fbbc35]" role="menuitem">
				<a href="#contact">Contactez-nous</a>
			</button>
		</div>
	</nav>
</template>

<script>

export default {
    methods: {
		// Toogle navbar mode 
        navToggle() {
			let menu = document.querySelector("[role='menu']");
			let isExpanded = menu.getAttribute('aria-expanded');
			menu.setAttribute('aria-expanded', !isExpanded);
			menu.classList.toggle('hidden');
			menu.classList.toggle('flex');
		}
    }
}
</script>

<style>

</style>