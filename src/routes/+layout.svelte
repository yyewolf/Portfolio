<script lang="ts">
	// The ordering of these imports is critical to your app working properly
	import '@skeletonlabs/skeleton/themes/theme-skeleton.css';
	// If you have source.organizeImports set to true in VSCode, then it will auto change this ordering
	import '@skeletonlabs/skeleton/styles/all.css';
	// Most of your app wide CSS should be put in this file
	import '../app.postcss';
	import '../app.css';
	import { Avatar, AppShell, AppBar } from '@skeletonlabs/skeleton';
	import { Motion } from 'svelte-motion';

	import { Toast, toastStore } from '@skeletonlabs/skeleton';
</script>



<Toast position="b" />

<!-- App Shell -->
<!-- svelte-ignore a11y-invalid-attribute -->
<AppShell>
	<svelte:fragment slot="header">
		<!-- App Bar -->
		<AppBar>
			<svelte:fragment slot="lead">
				<Avatar src="logo.png" class="w-9"  />
				<Motion whileHover={{ scale: 1.2, rotate: 0.8 }} initial={{ borderRadius: 25 }} let:motion>
					<a use:motion class="ml-5 text-3xl uppercase text-orange-200" href="#">#Yewolf</a>
				</Motion>
			</svelte:fragment>
			<svelte:fragment slot="trail">
				<Motion whileHover={{ scale: 1.5, rotate: 5 }} initial={{ borderRadius: 25 }} let:motion>
					<a  use:motion
						class="btn btn-sm variant-ghost-surface"
						href="https://www.linkedin.com/in/tristan-smagghe-70178a24b/"
						target="_blank"
						rel="noreferrer"
					>
						LinkedIn
					</a>
				</Motion>
				<Motion whileHover={{ scale: 1.5, rotate: -5 }} initial={{ borderRadius: 25 }} let:motion>
					<a  use:motion
						class="btn btn-sm variant-ghost-surface"
						href="https://github.com/yyewolf"
						target="_blank"
						rel="noreferrer"
					>
						GitHub
					</a>
				</Motion>
				<Motion whileHover={{ scale: 1.5, rotate: 5 }} initial={{ borderRadius: 25 }} let:motion>
					<a  use:motion
						class="btn btn-sm variant-ghost-surface"
						href="mailto:tristan.smagghe@telecomnancy.net"
						target="_blank"
						rel="noreferrer"
					>
						Mail
					</a>
				</Motion>
				<Motion whileHover={{ scale: 1.5, rotate: -5 }} initial={{ borderRadius: 25 }} let:motion>
					<a  use:motion
						class="btn btn-sm variant-ghost-surface"
						href="#contact"
						rel="noreferrer"
					>
						Contact
					</a>
				</Motion>
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
	<!-- Page Route Content -->
	<slot />
</AppShell>