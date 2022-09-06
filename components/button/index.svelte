<script lang="ts">
    import './style.scss'
    export let label:string ='';
    export let size: "small" | "medium" | "large";
    export let onClick : (value : string) => void;

	let user = { Hello: false };
	function toggle() {
		user.Hello = !user.Hello;
	}
</script>

{#if user.Hello}
	<button on:click={toggle}>
		Hello
	</button>
{:else}
	<button on:click={toggle}>
		Bye Bye
	</button>
{/if}