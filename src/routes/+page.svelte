<script lang="ts">
	import { onMount } from 'svelte';

	onMount(async () => {
		const EditorJS = (await import('@editorjs/editorjs')).default;
		const Header = (await import('@editorjs/header')).default;

		const editor = new EditorJS({
			holder: 'editor',
			placeholder: "Let's write an awesome story",

			tools: {
				header: Header
			}
		});
	});
</script>

<div id="editor" />
