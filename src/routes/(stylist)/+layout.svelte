<script lang="ts">
	import Sidebar from '$lib/components/layouts/stylist/Sidebar.svelte';
	import TopNavigation from '$lib/components/layouts/stylist/TopNavigation.svelte';
	import Separator from '$lib/components/pages/profile/Separator.svelte';
	import PageTransition from '$lib/components/ui/PageTransition.svelte';

    export let data
</script>
<svelte:head>
    <title>Stylist Area</title>
</svelte:head>

<TopNavigation user={data.user} />
<section class="flex h-full min-h-[calc(100svh-200px)] max-h-full">
    <div class="flex flex-row w-full h-full">

        <div class="hidden md:flex">
              
            <Sidebar />
            <Separator />

        </div>

        <section id="content" class="overflow-x-hidden w-full h-full">
            <PageTransition pathname={data.pathname}>
                <slot />
            </PageTransition>
        </section>

    </div>
</section>