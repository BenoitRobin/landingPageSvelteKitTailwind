<script>
	import logo from '../assets/RocketLogo.svg';
	import menu from '../assets/menu.svg';

    import { fade } from 'svelte/transition';

	let isVisible = true ;

	const toogleMenu = () => {
		isVisible = !isVisible;
	};
</script>

<nav
	class="fixed top-0 z-20 bg-gray-50 p-4 w-full grid grid-cols-none shadow-md md:max-w-7x1 md:grid-cols-menu md:shadow-none md:relative md:mx-auto md:bg-transparent"
>
	<div class="flex justify-between items-center md:justify-center">
		<a href="#accueil" class="w-12">
			<img src={logo} alt="logo" />
		</a>
		<button on:click={toogleMenu} class="toogle-menu bg-white rounded-md p-2 ring-1 ring-black ring-opacity-20 md:hidden">
			<img src={menu} alt="icon menu" class="h-6 w-6" />
		</button>
	</div>
	<ul
		class="px-1 pt-6 bg-gray-50 flex flex-col md:flex md:bg-transparent md:pt-0 md:flex-row md:space-x-10 md:w-auto md:items-center md:justify-center
        {isVisible ? "hidden" : ""}
        "
	>
		<li class="py-2 text-center border-t border-gray-200 md:border-0">
			<a on:click={toogleMenu} href="#accueil" class="font-medium text-lg text-zinc-800 hover:text-gray-900"> Accueil </a>
		</li>

		<li class="py-2 text-center border-t border-gray-200 md:border-0">
			<a on:click={toogleMenu} href="#services" class="font-medium text-lg text-zinc-800 hover:text-gray-900">
				Services
			</a>
		</li>

		<li class="py-2 text-center border-t border-gray-200 md:border-0">
			<a on:click={toogleMenu} href="#tarifs" class="font-medium text-lg text-zinc-800 hover:text-gray-900">
				Nos tarifs
			</a>
		</li>

		<li class="py-2 text-center border-t border-b border-gray-200 md:border-0">
			<a on:click={toogleMenu} href="#contact" class="font-medium text-lg text-zinc-800 hover:text-gray-900"> Contact </a>
		</li>
	</ul>

	<div
		class="{isVisible ? "hidden" : ""} flex justify-center items-center mt-6 md:mt-0 md:justify-end md:flex"
	>
		<a
			href="/"
			class="shadow-md px-6 py-2 border font-medium rounded-md text-indigo-600 bg-white hover:bg-gray-50 text-center w-40"
			>Log in</a
		>
	</div>
</nav>
