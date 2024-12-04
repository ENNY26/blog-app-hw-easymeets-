<script>
    // Navbar links
    const links = [
        { name: "Home", href: "/" },
        { name: "About", href: "/About" },
        { name: "Contact", href: "/Contact" },
        { name: "Blogs", href: "/Blogs" },
    ];

    // Track if the menu is open
    let isMenuOpen = false;

    // Toggle menu visibility
    function toggleMenu() {
        isMenuOpen = !isMenuOpen;
    }
</script>

<nav >
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex items-center justify-between h-16">
        <!-- Logo -->
        <div>
           <a href="/"> <img src="/src/Assets/logo2.svg" alt="Logo" class="h-10 cursor-pointer"></a>
        </div>

        <!-- Desktop Links -->
        <div class="hidden md:flex space-x-4">
            {#each links as link}
                <a
                    href={link.href}
                    class="text-gray-700 hover:text-[#1e40d7] 
                    px-3 py-2 rounded-md text-sm font-medium"
                >
                    {link.name}
                </a>
            {/each}
        </div>

        <!--  Menu Buttons  -->
        <button
            class="md:hidden text-gray-700 hover:text-gray-900 
            focus:outline-none focus:ring-2 focus:ring-[#1e40d7]"
            on:click={toggleMenu}
            aria-label="Toggle Navigation"
        >
        {#if isMenuOpen}
            <img src="/src/Assets/close.svg" width="26px" alt="close icon">
            {:else}
            <img src="/src/Assets/menu.svg" width="26px" alt="menu icon">
            {/if}
        </button>
    </div>

    <!-- Mobile Menu -->
    {#if isMenuOpen}
        <div class="md:hidden bg-white shadow-lg">
            <div class="space-y-2 py-4 px-4">
                {#each links as link}
                    <a
                        href={link.href}
                        class="block text-gray-700 hover:text-[#1e40d7] 
                        px-3 py-2 rounded-md text-base font-medium"
                    >
                        {link.name}
                    </a>
                {/each}
            </div>
        </div>
    {/if}
</nav>

<style>
    /*  animations for menu */
    @keyframes slideDown {
        from {
            opacity: 0;
            transform: translateY(-10px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }

    div[aria-hidden="false"] {
        animation: slideDown 0.3s ease-out;
    }
</style>
