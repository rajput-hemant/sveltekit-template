<script lang="ts">
	import { Clipboard, ClipboardCheck, Github, Twitter } from 'lucide-svelte';

	const packageManagers = { bun: 'bunx', pnpm: 'pnpx', npm: 'npx', yarn: 'yarn dlx' };

	let isCopied = false;
	let showDropdown = false;

	const copyToClipboard = (pm: keyof typeof packageManagers) => {
		showDropdown = false;
		isCopied = true;

		const text = `${packageManagers[pm]} degit rajput-hemant/sveltekit-template <project-name>`;

		try {
			navigator.clipboard.writeText(text);
			isCopied = true;
		} catch (err) {
			console.error('Failed to copy: ', err);
		}
	};
</script>

<svelte:head>
	<title>SvelteKit Starter Template</title>
	<meta
		name="description"
		content="A starter template for SvelteKit w/ TypeScript, TailwindCSS pre-configured with ESLint, Prettier and Husky git hooks."
	/>
</svelte:head>

<main class="layout h-screen w-full bg-black py-12 md:py-24 lg:py-32 xl:py-48">
	<section class="container px-4 md:px-6">
		<img src="/favicon.png" alt="SvelteKit logo" class="mx-auto mb-6 max-w-[100px] md:max-w-full" />

		<div class="grid items-center gap-6">
			<div class="flex flex-col justify-center space-y-4 text-center">
				<div class="mb-6 space-y-2">
					<h1
						class="bg-gradient-to-r from-white to-gray-500 bg-clip-text text-3xl font-bold tracking-tighter text-transparent sm:text-5xl xl:text-6xl/none"
					>
						SvelteKit Starter Template
					</h1>

					<p class="mx-auto max-w-[600px] text-zinc-200 md:text-xl">
						A SvelteKit template with TypeScript, TailwindCSS, Lucide Icons and pre-configured with
						ESLint, Prettier and Husky git hooks.
					</p>
				</div>

				<div
					class="relative mx-auto rounded-xl border border-zinc-800 p-1 text-zinc-200 shadow-md transition-shadow duration-300 hover:border-zinc-700 hover:shadow-white/10"
				>
					<p
						class="flex w-full cursor-pointer items-center gap-2 rounded-md bg-white/10 p-3 font-mono"
					>
						<span class="text-orange-500">$</span>

						<span>
							pnpx degit rajput-hemant/sveltekit-template {'<project-name>'}
						</span>

						<button
							on:click={() => (showDropdown = !showDropdown)}
							class="text-zinc-400 transition-colors duration-300 hover:text-white"
						>
							{#if isCopied}
								<ClipboardCheck class="h-5 w-5" />
							{:else}
								<Clipboard class="h-5 w-5" />
							{/if}
						</button>
					</p>

					{#if showDropdown}
						<div
							class="absolute -right-16 top-8 z-10 rounded-xl border border-zinc-700 p-1 hover:border-zinc-600"
						>
							<ul class="sticky flex flex-col rounded-md bg-zinc-800">
								<button
									on:click={() => copyToClipboard('bun')}
									class="m-0.5 w-20 cursor-pointer rounded-md px-3 py-0.5 hover:bg-zinc-700/50 hover:text-orange-500"
								>
									bun
								</button>

								<button
									on:click={() => copyToClipboard('pnpm')}
									class="m-0.5 w-20 cursor-pointer rounded-md px-3 py-0.5 hover:bg-zinc-700/50 hover:text-orange-500"
								>
									pnpm
								</button>

								<button
									on:click={() => copyToClipboard('npm')}
									class="m-0.5 w-20 cursor-pointer rounded-md px-3 py-0.5 hover:bg-zinc-700/50 hover:text-orange-500"
								>
									npm
								</button>

								<button
									on:click={() => copyToClipboard('yarn')}
									class="m-0.5 w-20 cursor-pointer rounded-md px-3 py-0.5 hover:bg-zinc-700/50 hover:text-orange-500"
								>
									yarn
								</button>
							</ul>
						</div>
					{/if}
				</div>
			</div>
		</div>
	</section>

	<footer
		class="fixed bottom-4 mx-auto flex w-full flex-col text-center font-medium text-zinc-600 dark:text-zinc-400"
	>
		<div class="mx-auto flex">
			<a
				href="https://github.com/rajput-hemant"
				target="_blank"
				rel="noopener noreferrer"
				class="rounded-md border border-transparent p-2 hover:border-zinc-700 hover:bg-white/10"
			>
				<Github class="h-5 w-5" />
			</a>

			<a
				href="https://x.com/rajput_hemant01"
				target="_blank"
				rel="noopener noreferrer"
				class="rounded-md border border-transparent p-2 hover:border-zinc-700 hover:bg-white/10"
			>
				<Twitter class="h-5 w-5" />
			</a>
		</div>

		<span>
			Copyright &copy; {new Date().getFullYear()}

			<a
				href="https://github.com/rajput-hemant"
				target="_blank"
				rel="noopener noreferrer"
				class="bg-gradient-to-r from-white to-gray-500 bg-clip-text underline-offset-4 hover:underline"
			>
				rajput-hemant@github
			</a>
		</span>
	</footer>
</main>

<style>
	/* https://github.com/jvidalv/nextal/blob/main/src/components/organisms/layout/layout.module.css */

	.layout {
		background-image: radial-gradient(hsla(0, 0%, 84%, 0.25) 1px, transparent 0),
			radial-gradient(hsla(0, 0%, 65%, 0.2) 1px, transparent 0);
		background-size: 50px 50px;
		background-position:
			0 0,
			25px 25px;
		-webkit-animation: slide 2s linear infinite;
		animation: slide 4s linear infinite;
	}

	@keyframes slide {
		100% {
			background-position:
				50px 0,
				125px 25px;
		}
	}

	::selection {
		color: hsl(0, 0%, 17%);
		background-color: hsl(0, 0%, 100%);
	}
</style>
