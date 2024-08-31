<script lang="ts">
  import * as Sheet from "$lib/components/ui/sheet/index";
  let isNavbarOpen = false
</script>

<!-- ========== HEADER ========== -->
<header class="px-4 lg:px-6 h-14 flex items-center">
  <a href="/" class="flex items-center justify-center">
    <span class="sr-only text-xl">Barber's Delight</span>
  </a>
  <nav class="ml-auto flex gap-4 sm:gap-6">

    
    <div class="hidden sm:block">
      <slot />
    </div>

  </nav>
</header>
<!-- ========== END HEADER ========== -->

<Sheet.Root open={isNavbarOpen} onOpenChange={() => isNavbarOpen = !isNavbarOpen }>
<Sheet.Content side="top" class="bg-gray-900 text-sm">
  <slot />
   
</Sheet.Content>
</Sheet.Root>