<script lang="ts">
	import Navigation from '$lib/components/layouts/guests/Navigation.svelte';
	import NavigationItems from '$lib/components/layouts/guests/NavigationItems.svelte';
	import Features from '$lib/components/pages/home/Features.svelte';
	import Footer from '$lib/components/pages/home/Footer.svelte';
	import Hero from '$lib/components/pages/home/Hero.svelte';
	import Team from '$lib/components/pages/home/Team.svelte';
    export let data
</script>
<div class="flex flex-col min-h-[100dvh] w-full">

    <Navigation>
        <NavigationItems user={data.user} authenticated={data.isAuthenticatedUser} hasCustomerSession={data.hasCustomerSession} />
    </Navigation>
    <main class="flex-1">
        <Hero />
        <Features />
        <Team />
    </main>
    <Footer />

</div>