<script>
  export let mobileMenuOpen = false;
</script>

<nav class="flex items-center justify-between px-6 py-5 md:px-10 max-w-[1600px] mx-auto">
  <div class="flex items-center gap-1 cursor-pointer">
    <a href="/" class="font-bold text-xl tracking-tight flex items-center">
      <span class="mr-0.5">II</span>Alago
    </a>
  </div>

  <!-- Navigation Links (Desktop) -->
  <div class="hidden lg:flex items-center gap-8 text-[15px] font-medium text-gray-800">
    <a href="#features" class="hover:text-black transition-colors">Meeting Assistant</a>
    <a href="#protocol" class="hover:text-black transition-colors">Protocol Designer</a>
    <a href="#integrations" class="hover:text-black transition-colors">Integrations</a>
    <a href="#case-studies" class="hover:text-black transition-colors">Case Studies</a>
    <a href="#construction" class="hover:text-black transition-colors">Construction Firms</a>
    <a href="#pricing" class="hover:text-black transition-colors">Pricing</a>
  </div>

  <!-- Auth Buttons -->
  <div class="flex items-center gap-3">
    <a href="/login" class="px-5 py-2 rounded-full border border-gray-200 text-[15px] font-medium hover:bg-gray-50 transition-colors">Log in</a>
    <a href="/signup" class="px-5 py-2 rounded-full bg-black text-white text-[15px] font-medium hover:bg-gray-800 transition-colors">Sign up</a>
  </div>
</nav>
