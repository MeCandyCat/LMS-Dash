<script>
	import FeatureCard from '$lib/FeatureCard.svelte';
	import { base } from '$app/paths'

</script>

<!-- nav bar  -->
<nav class="p-2 sm:p-10 h-10 flex justify-between items-center w-full text-lg sm:text-2xl font-bold gap-5">
	<a class="text-transparent bg-gradient-to-br bg-clip-text from-indigo-500 from-50% to-sky-500 to-70%" href="{base}">LMS</a>
	<div class="gap-5 flex">
		<a href="https://mecandycat.github.io/LMS-Docs/">Docs</a>
		<a href="{base}">Support</a>
	</div>
	<a href="{base}">Login</a>
</nav>

<!-- section container  -->
<div class="overflow-x-hidden">
	<!-- first section  -->
	<section class="h-5/6 mt-28 md:32 text-center leading-normal p-16 text-5xl font-bold center-everything flex-col gap-10 overflow-y-clip">
		<div class="absolute top-0 right-0 bg-blue-700 opacity-70 rounded-full w-1/3 aspect-square filter blur-3xl mix-blend-soft-light" />
		<div class="absolute bottom-0 left-0 bg-purple-900 opacity-50 rounded-full w-1/4 aspect-square filter blur-3xl" />

		<h1 class="bg-gradient-to-br bg-clip-text text-transparent from-sky-400 from-40% to-purple-700 to-90%">
			Learning Management System<br />in Discord.
		</h1>
		<button class="text-4xl p-2 px-4 border-4 transition-all duration-500 border-purple-500 hover:border-sky-500 hover:text-sky-300 rounded-full"
			>Invite</button
		>
	</section>

	<!-- section divider  -->
	<svg class="relative fill-slate-950" viewBox="0 0 1440 320"
		><path
			fill-opacity="1"
			d="M0,192L80,202.7C160,213,320,235,480,224C640,213,800,171,960,176C1120,181,1280,235,1360,261.3L1440,288L1440,320L1360,320C1280,320,1120,320,960,320C800,320,640,320,480,320C320,320,160,320,80,320L0,320Z"
		/></svg
	>

	<!-- Features section  -->
	<section class="relative p-16 flex-col center-everything gap-10 bg-slate-950">
		<h1 class="text-5xl font-bold">Features</h1>

		<div class="flex flex-wrap gap-10 justify-center text-left text-sm font-normal">
			<FeatureCard
				image="https://images-ext-2.discordapp.net/external/2r8e9QV2hma4BspoSm6X7kW6pyqsMhsZqvDfsARRDt8/https/cdn.discordapp.com/avatars/725721249652670555/781224f90c3b841ba5b40678e032f74a.webp"
				title="Host Classes"
				description="You can host private classes on discord only for your students."
			/>
			<FeatureCard
				image="https://images-ext-2.discordapp.net/external/2r8e9QV2hma4BspoSm6X7kW6pyqsMhsZqvDfsARRDt8/https/cdn.discordapp.com/avatars/725721249652670555/781224f90c3b841ba5b40678e032f74a.webp"
				title="View Satistics"
				description="View useful information about your class within a month."
			/>
			<FeatureCard
				image="https://images-ext-2.discordapp.net/external/2r8e9QV2hma4BspoSm6X7kW6pyqsMhsZqvDfsARRDt8/https/cdn.discordapp.com/avatars/725721249652670555/781224f90c3b841ba5b40678e032f74a.webp"
				title="Assignments"
				description="Method to send assignments as a teacher and submit answers back to teacher as a student."
			/>
			<FeatureCard
				image="https://images-ext-2.discordapp.net/external/2r8e9QV2hma4BspoSm6X7kW6pyqsMhsZqvDfsARRDt8/https/cdn.discordapp.com/avatars/725721249652670555/781224f90c3b841ba5b40678e032f74a.webp"
				title="Attendance"
				description="Mark attendance of students in a VC."
			/>
			<FeatureCard
				image="https://images-ext-2.discordapp.net/external/2r8e9QV2hma4BspoSm6X7kW6pyqsMhsZqvDfsARRDt8/https/cdn.discordapp.com/avatars/725721249652670555/781224f90c3b841ba5b40678e032f74a.webp"
				title="Dashboard"
				description="A clean dashboard to manage our bot."
			/>
		</div>
	</section>

	<svg class="fill-slate-950" viewBox="0 0 1200 120" preserveAspectRatio="none">
		<path
			d="M321.39,56.44c58-10.79,114.16-30.13,172-41.86,82.39-16.72,168.19-17.73,250.45-.39C823.78,31,906.67,72,985.66,92.83c70.05,18.48,146.53,26.09,214.34,3V0H0V27.35A600.21,600.21,0,0,0,321.39,56.44Z"
			class="shape-fill"
		/>
	</svg>

	<!-- about section  -->
	<section class="relative z-10 center-everything min-h-64 bg-slate-900 flex-col h-full text-justify mb-12">
		<h1 class="text-5xl font-bold m-5 mt-16 text-purple-500">About LMS</h1>
		<p class="m-16 mt-5 lg:mx-96">
			Introducing LMS Discord Bot, your ultimate companion for creating and managing a Learning Management System on Discord! This versatile bot is
			designed to streamline the process of setting up an educational platform, making it a breeze for Educators, Admins and students alike. With LMS
			you can automate the process of creating classes, sending assignments, scheduling classes + much more. Join us and elevate your learning
			experience today!
		</p>
	</section>

	<svg class="fill-slate-950" viewBox="0 0 1440 320">
		<path
			d="M0,96L80,106.7C160,117,320,139,480,176C640,213,800,267,960,282.7C1120,299,1280,277,1360,266.7L1440,256L1440,320L1360,320C1280,320,1120,320,960,320C800,320,640,320,480,320C320,320,160,320,80,320L0,320Z"
		/>
	</svg>

	<footer class="relative flex items-center justify-around gap-10 p-16 flex-col md:flex-row font-bold text-lg bg-slate-950">
		<div class="text-center">
			<h1 class="text-8xl">LMS</h1>
			<p>&copy LMS Developer Team</p>
		</div>
		<div class="flex gap-10 underline-offset-2">
			<a class="hover:underline" href="{base}">Docs</a>
			<a class="hover:underline" href="{base}">Support</a>
			<a class="hover:underline" href="{base}">Invite</a>
			<a class="hover:underline" href="{base}">Dashboard</a>
		</div>
	</footer>
</div>
