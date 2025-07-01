<script lang="ts">
	import ThemeSwitcher from '$lib/components/self/theme-switcher.svelte';
	import { Button } from '$lib/components/ui/button';
	import Particles from '$lib/components/ui/Particles.svelte';
	import { Facebook, Github, Instagram, Mail, MapPin } from '@lucide/svelte';

	const handleNavigate = (url: string) => {
		window.open(url, '_open');
	};
</script>

<main class="flex min-h-screen flex-col items-center justify-center gap-2">
	<Particles className="absolute h-full w-full -z-10" />
	<div class="absolute top-2 right-2">
		<ThemeSwitcher />
	</div>
	<div class="flex flex-col items-center">
		<h1 class="text-2xl font-semibold">Phat Lorthammakun</h1>
		<div class="flex flex-row items-center gap-1">
			<MapPin size={16} class="text-muted-foreground" />
			<p class="text-muted-foreground">Bangkok, Thailand</p>
		</div>
	</div>
	<div class="flex flex-row gap-2">
		<Button
			variant="outline"
			class="h-8 w-8"
			onclick={() => handleNavigate('https://www.facebook.com/epiccatto/')}
		>
			<Facebook size={32} />
		</Button>
		<Button
			variant="outline"
			class="h-8 w-8"
			onclick={() => handleNavigate('https://www.instagram.com/phat.lor/')}
		>
			<Instagram size={32} />
		</Button>
		<Button
			variant="outline"
			class="h-8 w-8"
			onclick={() => handleNavigate('https://github.com/phat-lor/')}
		>
			<Github size={32} />
		</Button>
		<Button
			variant="outline"
			class="h-8 w-8"
			onclick={() => handleNavigate('mailto:contact@phatlor.me')}
		>
			<Mail size={32} />
		</Button>
	</div>
</main>
