<script lang="ts">
	import Sidebar from '$lib/components/layouts/stylist/Sidebar.svelte';
	import TopNavigation from '$lib/components/layouts/dashboard/TopNavigation.svelte';
	import Separator from '$lib/components/pages/profile/Separator.svelte';

    export let data
</script>
<svelte:head>
    <title>Stylist Area</title>
</svelte:head>

<TopNavigation user={data.user} />
<section class="flex h-full min-h-[calc(100svh-200px)] max-h-full">
    <div class="flex flex-row overflow-x-hidden w-full h-full">

        <div class="hidden md:flex">
              
            <Sidebar />
            <Separator />

        </div>

        <section id="content" class="w-full">
            <slot />
        </section>

    </div>
</section>