<script lang="ts">
	import Button from "$lib/components/ui/button/button.svelte";
	import type { ActionData } from "../$types";
	import AddPoint from "./AddPoint.svelte";

    let isOpen = false
    export let form: ActionData
</script>
<div class="flex justify-between px-8 pt-4 pb-2 bg-gray-50">
    <div>
        <h3 class="text-lg font-medium">Point List</h3> 
        <p class="text-sm text-muted-foreground">Summary of your application. (Example of a dashboard card stats)</p>
    </div>
    <Button type="button" on:click={() => isOpen = !isOpen}>
        Add New
    </Button>
</div>
<AddPoint {isOpen} onClose={() => isOpen = false} {form} />

