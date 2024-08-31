<script lang="ts">
  import * as Sheet from "$lib/components/ui/sheet/index";
  let isNavbarOpen = false
</script>

<!-- ========== HEADER ========== -->
<header class="h-14 flex items-center bg-black">
  <a href="/" class="flex items-center justify-center">
    <!-- <span class="sr-only text-4 text-white">Barber's Delight</span> -->
  </a>
  <nav class="px-2 lg:px-6 ml-auto flex gap-4 sm:gap-6">
    
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