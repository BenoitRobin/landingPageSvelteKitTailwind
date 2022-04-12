<script>
	import Checked from '../assets/checked.svg';

	const offers = [
		{
			id: 0,
			name: 'Basic',
			desc: 'Fill your basic needs',
			price: 12,
			option: [
				'Lorem Ipsum is simply dummy',
				'It is a long established fact.',
				'Many desktop publishing.'
			]
		},
		{
			id: 1,
			name: 'Freelance',
			desc: 'Go to the next level',
			price: 29,
			option: [
				'Contrary to popular belief.',
				'There are many variations of passages.',
				'It is a long established fact.',
				'Lorem Ipsum is simply dummy.'
			]
		},
		{
			id: 2,
			name: 'Professionnal',
			desc: 'Enter the pro world',
			price: 99,
			option: [
				'It is a long established fact.',
				'Lorem Ipsum is simply dummy.',
				'There are many variations.',
				'Many desktop publishing.',
				'Potenti felis, in cras at.'
			]
		}
	];

</script>

{#each offers as item}
	<div
		class="w-72 h-[450px] m-auto mb-5 shadow-lg shadow-slate-300 rounded-xl ring-2 ring-gray-300 px-5 bg-transparent flex flex-col justify-around"
	>
		<div class="flex flex-col ">
			<h3 class="text-2xl font-bold">{item.name}</h3>
			<p class="pb-5">{item.desc}</p>
			<p class="font-bold"><span class="text-4xl">{item.price}€</span>/month</p>
			<p class="pb-5 text-sm">INCLUDED :</p>

			<ul class="text-sm">

				<li class="flex mb-4">
					<img src={Checked} alt="icone checked" class="w-5 mr-3" />Lorem Ipsum is simply dummy
				</li>
				<li class="flex mb-4">
					<img src={Checked} alt="icone checked" class="w-5 mr-3" /> Polentisfelis, in cras at.
				</li>
				<li class="flex mb-4">
					<img src={Checked} alt="icone checked" class="w-5 mr-3" /> Polentisfelis, in cras at.
				</li>
			</ul>
		</div>

		<a
			href="#"
			class="w-full text-center py-3 bg-slate-800 text-white text-sm font-medium rounded-md"
		>
			Subscribe to this plan
		</a>
	</div>
{/each}
