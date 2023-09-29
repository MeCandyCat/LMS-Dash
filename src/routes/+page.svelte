<script>
	import FeatureCard from '$lib/FeatureCard.svelte';
	import links from '$lib/links';
	import { base } from '$app/paths';
</script>

<div class="bg-grid">
	<!-- section container  -->
	<div class="overflow-x-hidden">
		<!-- shapes  -->
		<div>
			<div class="absolute right-0 top-0 -z-10 aspect-square w-[55%] rounded-full bg-blue-700 opacity-50 mix-blend-soft-light blur-3xl filter" />
			<div class="absolute -bottom-72 left-0 -z-10 aspect-square w-[60%] rounded-full bg-purple-900 opacity-20 blur-3xl filter" />
		</div>
		<!-- first section  -->
		<section class="relative flex-col h-screen gap-10 p-16 text-5xl font-bold leading-normal text-center center-everything pt-28">
			<h1 class="bg-gradient-to-br from-sky-400 from-40% to-purple-700 to-80% bg-clip-text text-transparent">
				Learning Management System<br />in Discord.
			</h1>
			<a
				href={links.inviteLink} target="_blank"
				class="p-2 px-4 text-4xl transition-all duration-500 border-4 rounded-full border-sky-500 text-sky-300 hover:border-purple-500 hover:text-purple-300"
				>Invite</a
			>
		</section>
		<svg class="fill-slate-950" viewBox="0 0 1440 320"
			><path
				fill-opacity="1"
				d="M0,192L80,202.7C160,213,320,235,480,224C640,213,800,171,960,176C1120,181,1280,235,1360,261.3L1440,288L1440,320L1360,320C1280,320,1120,320,960,320C800,320,640,320,480,320C320,320,160,320,80,320L0,320Z"
			/></svg
		>

		<!-- section divider  -->

		<!-- Features section  -->
		<section class="relative flex-col gap-10 p-16 pb-48 center-everything bg-slate-950">
			<h1 class="text-5xl font-bold text-center text-purple-500">Features</h1>

			<div class="grid justify-center grid-cols-1 gap-10 lg:grid-cols-2">
				<FeatureCard
					image="https://cdn-icons-png.flaticon.com/128/2641/2641257.png"
					title="Host Classes"
					description="You can host private classes on discord only for your students."
					color="via-green-500"
				/>
				<FeatureCard
					image="https://cdn-icons-png.flaticon.com/128/2641/2641289.png"
					title="View Satistics"
					description="View useful information about your class within a month."
					color="via-blue-600"
				/>
				<FeatureCard
					image="https://cdn-icons-png.flaticon.com/128/2641/2641478.png"
					title="Assignments"
					description="Send assignments as a teacher and submit answers as a student."
					color="via-orange-500"
				/>
				<FeatureCard
					image="https://cdn-icons-png.flaticon.com/128/2641/2641483.png"
					title="Attendance"
					description="Mark attendance of students in a VC."
					color="via-yellow-300"
				/>
				<FeatureCard
					image="https://cdn-icons-png.flaticon.com/128/2641/2641269.png "
					title="Dashboard"
					description="A clean dashboard to manage our bot."
				/>
			</div>
		</section>

		<svg class="bg-slate-900 fill-slate-950" viewBox="0 0 1200 120" preserveAspectRatio="none">
			<path
				d="M321.39,56.44c58-10.79,114.16-30.13,172-41.86,82.39-16.72,168.19-17.73,250.45-.39C823.78,31,906.67,72,985.66,92.83c70.05,18.48,146.53,26.09,214.34,3V0H0V27.35A600.21,600.21,0,0,0,321.39,56.44Z"
				class="shape-fill"
			/>
		</svg>

		<!-- about section  -->
		<section class="relative z-10 flex-col h-full text-justify center-everything min-h-64 bg-slate-900">
			<h1 class="m-5 mt-16 text-5xl font-bold text-purple-500">About LMS</h1>
			<p class="m-16 mt-5 lg:mx-48 xl:mx-96">
				Introducing LMS Discord Bot, your ultimate companion for creating and managing a Learning Management System on Discord! This versatile bot is
				designed to streamline the process of setting up an educational platform, making it a breeze for Educators, Admins and students alike. With
				LMS you can automate the process of creating classes, sending assignments, scheduling classes + much more. Join us and elevate your learning
				experience today!
			</p>
		</section>

		<svg class="bg-slate-900 fill-slate-950" viewBox="0 0 1440 320">
			<path
				d="M0,96L80,106.7C160,117,320,139,480,176C640,213,800,267,960,282.7C1120,299,1280,277,1360,266.7L1440,256L1440,320L1360,320C1280,320,1120,320,960,320C800,320,640,320,480,320C320,320,160,320,80,320L0,320Z"
			/>
		</svg>

		<footer class="relative flex flex-col items-center justify-around gap-10 p-16 text-lg font-bold bg-slate-950 md:flex-row">
			<div class="text-center">
				<h1 class="text-8xl">LMS</h1>
				<p>&copy LMS Developer Team</p>
			</div>
			<div class="flex gap-10 underline-offset-2">
				<a class="hover:underline" href={links.docsLink}>Docs</a>
				<a class="hover:underline" href={links.supportLink} target="_blank">Support</a>
				<a class="hover:underline" href={links.inviteLink} target="_blank">Invite</a>
				<a class="hover:underline" href="/dash">Dashboard</a>
				<a class="hover:underline" href="/terms">Terms</a>
				<a class="hover:underline" href="/privacy">Privacy</a>
			</div>
		</footer>
	</div>
</div>
