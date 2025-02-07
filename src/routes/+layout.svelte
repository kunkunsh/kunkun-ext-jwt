<script>
	import '../app.css';
	import { ModeWatcher } from 'mode-watcher';
	import { ui } from '@kksh/api/ui/custom';
	import { updateTheme } from '@kksh/svelte5';
	import { onMount } from 'svelte';

	onMount(() => {
		ui.registerDragRegion();
		ui.getTheme().then((theme) => {
			updateTheme(theme);
		});
	});
</script>

<ModeWatcher />
<slot></slot>
