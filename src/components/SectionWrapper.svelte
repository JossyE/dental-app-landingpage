<script>
	let { children, id } = $props();
</script>

<section id={id} class={"min-h-screen flex flex-col px-4 w-full"}>
    <div class="flex flex-col flex-1 max-w-350 mx-auto w-full">
        {@render children()}
    </div>
</section>