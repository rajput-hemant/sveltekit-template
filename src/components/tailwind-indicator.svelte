<script lang="ts">
	import { dev } from '$app/environment';
</script>

{#if dev}
	<div class="fixed bottom-1 right-1 z-50 text-xs text-black dark:text-white">
		<div class="block sm:hidden">xs</div>
		<div class="hidden sm:block md:hidden">sm</div>
		<div class="hidden md:block lg:hidden">md</div>
		<div class="hidden lg:block xl:hidden">lg</div>
		<div class="hidden xl:block 2xl:hidden">xl</div>
		<div class="hidden 2xl:block">2xl</div>
	</div>
{/if}
