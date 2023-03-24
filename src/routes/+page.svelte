<script>
	// @ts-nocheck

	import { Motion } from 'svelte-motion';
	import Typewriter from 'svelte-typewriter';
	import emailjs from '@emailjs/browser';
	/**
	 * @param {{ target: string | HTMLFormElement; }} e
	 */
	function sendEmail(e) {
		emailjs.sendForm('service_wehsins', 'template_4bpdsb9', e.target, 'cfiuVCzmLcrYWf-9N').then(
			(result) => {
				console.log('SUCCESS!', result.text);
			},
			(error) => {
				console.log('FAILED...', error.text);
			}
		);
	}

	const variants = {
		visible: { opacity: 1, x: 0 },
		hidden: { opacity: 0, x: -500 }
	};
	let i = 1;
	$: t = [0, 360][i];
	$: v = ['hidden', 'visible'][i];

	// I need HTML5, CSS3, JS, Vue, K3S, Tailwind, Git, Docker, Go, Python, Java, C, V, PSQL, MySQL and EdgeDB
	var logos = [
		{
			alt: 'HTML5',
			src: 'https://cdn.svgporn.com/logos/html-5.svg',
			link: 'https://www.w3schools.com/html/'
		},
		{
			alt: 'CSS3',
			src: 'https://cdn.svgporn.com/logos/css-3.svg',
			link: 'https://www.w3schools.com/css/'
		},
		{
			alt: 'JavaScript',
			src: 'https://cdn.svgporn.com/logos/javascript.svg',
			link: 'https://www.w3schools.com/js/'
		},
		{
			alt: 'Vue',
			src: 'https://cdn.svgporn.com/logos/vue.svg',
			link: 'https://vuejs.org/'
		},
		{
			alt: 'K3S',
			src: 'https://cdn.svgporn.com/logos/kubernetes.svg',
			link: 'https://k3s.io/'
		},
		{
			alt: 'Tailwind',
			src: 'https://cdn.svgporn.com/logos/tailwindcss-icon.svg',
			link: 'https://tailwindcss.com/'
		},
		{
			alt: 'Git',
			src: 'https://cdn.svgporn.com/logos/git-icon.svg',
			link: 'https://git-scm.com/'
		},
		{
			alt: 'Docker',
			src: 'https://cdn.svgporn.com/logos/docker-icon.svg',
			link: 'https://www.docker.com/'
		},
		{
			alt: 'Go',
			src: 'https://cdn.svgporn.com/logos/go.svg',
			link: 'https://go.dev/'
		},
		{
			alt: 'Python',
			src: 'https://cdn.svgporn.com/logos/python.svg',
			link: 'https://www.python.org/'
		},
		{
			alt: 'Java',
			src: 'https://cdn.svgporn.com/logos/java.svg',
			link: 'https://www.java.com/'
		},
		{
			alt: 'C',
			src: 'https://cdn.svgporn.com/logos/c.svg',
			link: 'https://www.cprogramming.com/'
		},
		{
			alt: 'V',
			src: 'https://vlang.io/img/v-logo.png',
			link: 'https://vlang.io/'
		},
		{
			alt: 'PostgreSQL',
			src: 'https://cdn.svgporn.com/logos/postgresql.svg',
			link: 'https://www.postgresql.org/'
		},
		{
			alt: 'MySQL',
			src: 'https://cdn.svgporn.com/logos/mysql.svg',
			link: 'https://www.mysql.com/'
		}
	];
</script>

<!-- This is the hero/home -->
<section
	id="home"
	class="h-screen w-full bg-brand bg-center bg-no-repeat bg-[length:105%_105%] flex py-28 justify-center items-center transition-all duration-75 sticky top-0"
>
	<div class="space-y-10 text-center">
		<h2 class="font-bold">Hi, I'm Yewolf.</h2>
		<!-- Animated Logo -->
		<figure>
			<section class="img-bg" />
			<Motion initial="hidden" animate={v} {variants} let:motion>
				<img use:motion src="logo.png" alt="Skeleton Logo" />
			</Motion>
		</figure>
		<!-- / -->
		<div class="flex justify-center space-x-2 bottom-0 heartbeat">
			<!-- Scroll buttons with arrows -->
			<a href="#about" class="btn btn-sm variant-ghost-surface h-12 w-12">
				<div class="flex flex-col items-center">
					<svg
						xmlns="http://www.w3.org/2000/svg"
						class="h-8 w-8"
						fill="none"
						viewBox="0 0 24 24"
						stroke="currentColor"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M19 14l-7 7m0 0l-7-7m7 7V3"
						/>
					</svg>
				</div>
			</a>
		</div>
	</div>
</section>
<!-- About me section -->
<section
	id="about"
	class="w-full flex items-center bg-neutrals-900 py-28 relative z-10 xl:min-h-[900px] flex-col md:flex-row bg-slate-900"
	aria-label="About"
>
	<div class="flex justify-center space-x-2 absolute bottom-10 heartbeat w-full z-10">
		<!-- Scroll buttons with arrows -->
		<a href="#tech" class="btn btn-sm variant-ghost-surface h-12 w-12">
			<div class="flex flex-col items-center">
				<svg
					xmlns="http://www.w3.org/2000/svg"
					class="h-8 w-8"
					fill="none"
					viewBox="0 0 24 24"
					stroke="currentColor"
				>
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="M19 14l-7 7m0 0l-7-7m7 7V3"
					/>
				</svg>
			</div>
		</a>
	</div>
	<img
		class="object-cover object-center w-full max-h-screen relative md:top-0 -top-28 right-0 md:w-1/2 md:h-full md:pr-10 xl:pr-0 md:absolute"
		loading="lazy"
		src="wp1.jpg"
		width="756"
		alt="placeholder"
		height="1008"
	/>
	<div class="mx-auto w-10/12 2xl:w-[80%] h-full">
		<div class="flex flex-col md:flex-row h-full w-full">
			<div class="basis-1/2 md:self-center">
				<div
					class="font-display font-bold text-brand lg:text-xl text-xl uppercase text-purple-400 mb-4"
				>
					About
				</div>
				<Typewriter mode="loop" interval={100}>
					<span class="text-4xl font-mono uppercase">Developer</span>
					<span class="text-4xl font-mono uppercase">Problem Solver</span>
					<span class="text-4xl font-mono uppercase">Explorer</span>
					<span class="text-4xl font-mono uppercase">Fast learner</span>
				</Typewriter>
				<p class="text-neutrals-50/60 leading-relaxed max-w-prose mt-4 text-slate-400">
					Hi, I'm Yewolf, a passionate developer who loves crafting beautiful and efficient
					software. With years of experience in coding and a solid understanding of different
					programming languages and frameworks, I'm always eager to take on new challenges and learn
					from them. Whether I'm working on a complex backend architecture or a sleek frontend
					interface, my goal is to deliver top-notch solutions that exceed expectations. When I'm
					not coding, you can find me playing my favorite video games or playing table tennis. Let's
					connect and bring your ideas to life!
				</p>
			</div>
		</div>
	</div>
</section>
<!-- Spacer -->
<section class="w-full z-10 relative h-2 py-28 bg-slate-100">
	<div class="mx-auto w-10/12 2xl:w-[80%] text-center">
		<div
			class="font-display font-bold text-brand lg:text-xl text-xl uppercase text-purple-800 mb-4"
		>
			Technologies used
		</div>
		<div class="font-display font-bold text-neutral-900 text-4xl md:text-4xl mb-8">What I use</div>
	</div>
</section>
<!-- Technologies section -->
<section
	id="tech"
	class="w-full flex items-center bg-neutrals-900 relative z-10 xl:min-h-[900px] min-h-[500px] flex-col md:flex-row bg-slate-900"
	aria-label="Technologies"
>
	<div class="flex justify-center space-x-2 absolute bottom-10 heartbeat w-full z-10">
		<!-- Scroll buttons with arrows -->
		<a href="#projects" class="btn btn-sm variant-ghost-surface h-12 w-12">
			<div class="flex flex-col items-center">
				<svg
					xmlns="http://www.w3.org/2000/svg"
					class="h-8 w-8"
					fill="none"
					viewBox="0 0 24 24"
					stroke="currentColor"
				>
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="M19 14l-7 7m0 0l-7-7m7 7V3"
					/>
				</svg>
			</div>
		</a>
	</div>
	<div class="mx-auto w-10/12 2xl:w-[80%] h-full">
		<div class="flex flex-col md:flex-row h-full w-full justify-center">
			<!-- Add a cloud of technologies -->
			<div class="grid justify-center grid-cols-5">
				{#each logos as tech}
					<Motion whileHover={{ scale: 1.8 }} initial={{ borderRadius: 25 }} let:motion>
						<a
							title={tech.alt}
							use:motion
							href={tech.link}
							target="_blank"
							class="flex flex-col items-center justify-center m-4"
						>
							<img class="h-16 w-16" src={tech.src} alt={tech.alt} />
						</a>
					</Motion>
				{/each}
			</div>
		</div>
	</div>
</section>
<!-- Spacer -->
<section class="w-full z-10 relative h-2 py-28 bg-slate-100">
	<div class="mx-auto w-10/12 2xl:w-[80%] text-center">
		<div
			class="font-display font-bold text-brand lg:text-xl text-xl uppercase text-purple-800 mb-4"
		>
			My projects
		</div>
		<div class="font-display font-bold text-neutral-900 text-4xl md:text-4xl mb-8">
			What I've done
		</div>
	</div>
</section>
<!-- Projects section -->
<section
	id="projects"
	class="w-full flex items-center bg-neutrals-900 pb-28 relative z-10 xl:min-h-[900px] flex-col md:flex-row bg-slate-900"
	aria-label="Projects"
>
	<div class="flex justify-center space-x-2 absolute bottom-10 heartbeat w-full z-10">
		<!-- Scroll buttons with arrows -->
		<a href="#contact" class="btn btn-sm variant-ghost-surface h-12 w-12">
			<div class="flex flex-col items-center">
				<svg
					xmlns="http://www.w3.org/2000/svg"
					class="h-8 w-8"
					fill="none"
					viewBox="0 0 24 24"
					stroke="currentColor"
				>
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="M19 14l-7 7m0 0l-7-7m7 7V3"
					/>
				</svg>
			</div>
		</a>
	</div>

	<div class="logo-cloud grid-cols-1 xl:grid-cols-2 2xl:grid-cols-4 gap-0.5 w-full px-32">
		<label for="modal-place" class="logo-item hover:cursor-pointer hover:bg-slate-800">TN Place</label>
	</div>


	<!-- Put this part before </body> tag -->
	<input type="checkbox" id="modal-place" class="modal-toggle" />
	<div class="modal">
		<div class="modal-box">
			<!-- Image on top to represent the project -->
			<img src="place.png" class="w-full" alt="TN Place" />
			<h3 class="font-bold text-lg">TN Place</h3>
			<p class="py-4">
				A "r/place" clone made with SvelteKit and Golang. It's a real-time collaborative drawing board
				where users can draw pixels on a grid. The project was hosted on Kubernetes.
			</p>
			<div class="modal-action">
				<a class="btn btn-primary" href="https://github.com/yyewolf/tn-place" target="_blank">Github</a>
				<label for="modal-place" class="btn">Close</label>
			</div>
		</div>
	</div>
</section>
<!-- Spacer -->
<section class="w-full z-10 relative h-2 py-28 bg-slate-100">
	<div class="mx-auto w-10/12 2xl:w-[80%] text-center">
		<div
			class="font-display font-bold text-brand lg:text-xl text-xl uppercase text-purple-800 mb-4"
		>
			Contact
		</div>
		<div class="font-display font-bold text-neutral-900 text-4xl md:text-4xl mb-8">
			How to contact me
		</div>
	</div>
</section>
<!-- Projects section -->
<section
	id="contact"
	class="w-full flex items-center bg-neutrals-900 pb-28 relative z-10 xl:min-h-[900px] flex-col md:flex-row bg-slate-900"
	aria-label="contact"
>
	<div class="mx-auto w-10/12 2xl:w-[80%] h-full">
		<div class="flex flex-col md:flex-row h-full w-full justify-center">
			<!-- I want 3 fields: name, email & message -->
			<div class="py-8 lg:py-16 px-4 mx-auto max-w-screen-md w-full">
				<form class="space-y-8" on:submit|preventDefault={sendEmail}>
					<div>
						<label
							for="email"
							class="block mb-2 text-sm font-medium text-gray-900 dark:text-gray-300"
							>Your email</label
						>
						<input
							type="email"
							id="email"
							name="reply_to"
							class="textarea"
							placeholder="email@example.com"
							required
						/>
					</div>
					<div>
						<label
							for="subject"
							class="block mb-2 text-sm font-medium text-gray-900 dark:text-gray-300">Subject</label
						>
						<input
							type="text"
							id="subject"
							name="from_subject"
							class="textarea"
							placeholder="Title of your message"
							required
						/>
					</div>
					<div class="sm:col-span-2">
						<label
							for="message"
							class="block mb-2 text-sm font-medium text-gray-900 dark:text-gray-400"
							>Your message</label
						>
						<textarea
							id="message"
							name="message"
							rows="6"
							class="textarea"
							placeholder="Your message here..."
						/>
					</div>
					<button
						type="submit"
						class="py-3 px-5 text-sm font-medium text-center text-white rounded-lg bg-primary-700 sm:w-fit hover:bg-primary-800 focus:ring-4 focus:outline-none focus:ring-primary-300 dark:bg-primary-600 dark:hover:bg-primary-700 dark:focus:ring-primary-800"
						>Send message</button
					>
				</form>
			</div>
		</div>
	</div>
</section>

<style lang="postcss">
	:root {
		--cursor-color: #fff;
	}

	.heartbeat {
		-webkit-animation: heartbeat 1.5s ease-in-out infinite both;
		animation: heartbeat 1.5s ease-in-out infinite both;
	}
	@-webkit-keyframes heartbeat {
		from {
			-webkit-transform: scale(1);
			transform: scale(1);
			-webkit-transform-origin: center center;
			transform-origin: center center;
			-webkit-animation-timing-function: ease-out;
			animation-timing-function: ease-out;
		}
		10% {
			-webkit-transform: scale(0.91);
			transform: scale(0.91);
			-webkit-animation-timing-function: ease-in;
			animation-timing-function: ease-in;
		}
		17% {
			-webkit-transform: scale(0.98);
			transform: scale(0.98);
			-webkit-animation-timing-function: ease-out;
			animation-timing-function: ease-out;
		}
		33% {
			-webkit-transform: scale(0.87);
			transform: scale(0.87);
			-webkit-animation-timing-function: ease-in;
			animation-timing-function: ease-in;
		}
		45% {
			-webkit-transform: scale(1);
			transform: scale(1);
			-webkit-animation-timing-function: ease-out;
			animation-timing-function: ease-out;
		}
	}
	@keyframes heartbeat {
		from {
			-webkit-transform: scale(1);
			transform: scale(1);
			-webkit-transform-origin: center center;
			transform-origin: center center;
			-webkit-animation-timing-function: ease-out;
			animation-timing-function: ease-out;
		}
		10% {
			-webkit-transform: scale(0.91);
			transform: scale(0.91);
			-webkit-animation-timing-function: ease-in;
			animation-timing-function: ease-in;
		}
		17% {
			-webkit-transform: scale(0.98);
			transform: scale(0.98);
			-webkit-animation-timing-function: ease-out;
			animation-timing-function: ease-out;
		}
		33% {
			-webkit-transform: scale(0.87);
			transform: scale(0.87);
			-webkit-animation-timing-function: ease-in;
			animation-timing-function: ease-in;
		}
		45% {
			-webkit-transform: scale(1);
			transform: scale(1);
			-webkit-animation-timing-function: ease-out;
			animation-timing-function: ease-out;
		}
	}
	figure {
		@apply flex relative flex-col;
	}
	figure svg,
	.img-bg {
		@apply w-64 h-64 md:w-80 md:h-80;
	}
	.img-bg {
		@apply absolute z-[-1] rounded-full blur-[50px] transition-all;
		animation: pulse 5s cubic-bezier(0, 0, 0, 0.5) infinite, glow 5s linear infinite;
	}
	@keyframes glow {
		0% {
			@apply bg-primary-400/50;
		}
		33% {
			@apply bg-secondary-400/50;
		}
		66% {
			@apply bg-tertiary-400/50;
		}
		100% {
			@apply bg-primary-400/50;
		}
	}
	@keyframes pulse {
		50% {
			transform: scale(1.5);
		}
	}
</style>
