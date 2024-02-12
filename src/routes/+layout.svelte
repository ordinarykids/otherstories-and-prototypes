<script>
    import { onMount } from "svelte";
    import "../app.css";
    import "@fontsource/ibm-plex-mono";
    import '@fontsource-variable/hanken-grotesk';



    let menuOpen = false;


   
</script>

<div class="container mx-auto pt-16 lg:w-1/3 m:w-full px-8">
    <div class="grid grid-cols-1 ">
        <div class="relative">
           
            <!-- Hamburger Button -->
            <button
                on:click={() => (menuOpen = !menuOpen)}
                class="hamburger-button block lg:hidden px-3 py-2 border rounded text-gray-700 border-gray-400 hover:text-white hover:border-white"
            >
                <div class="space-y-2">
                    <span class="block w-8 h-0.5 bg-gray-600"></span>
                    <span class="block w-8 h-0.5 bg-gray-600"></span>
                    <span class="block w-8 h-0.5 bg-gray-600"></span>
                </div>
            </button>

            <!-- Menu Items -->
            <nav class="lg:block" class:hidden={menuOpen}>
                <ul 
                    class="flex flex-col lg:flex-row space-y-4 lg:space-y-0 lg:space-x-8 mt-5 lg:mt-0 text-xs py-4"
                >
                    <li>
                        <a href="/" class="text-gray-700 hover:text-gray-900 "
                            ><a href="mailto:jason@ordinarykids.com" class="underline">JASON HERRING </a> - Daily Prototypes
                    </li>
                  
                </ul>
                <ul
                    class="flex flex-col lg:flex-row space-y-4 lg:space-y-0 lg:space-x-8 mt-5 lg:mt-0 text-xs"
                >
                   
                    <li>
                        <a href="/Globe" class="text-gray-700 hover:text-gray-900"
                            >Helix Globe Prototypes</a
                        >
                    </li>
                    <li>
                        <a href="/day3" class="text-gray-700 hover:text-gray-900"
                            >Early StyleGAN</a
                        >
                    </li>
                    <li>
                        <a href="/day1" class="text-gray-700 hover:text-gray-900"
                            >1</a
                        >
                    </li>
                    <li>
                        <a href="/day2" class="text-gray-700 hover:text-gray-900"
                            >2</a
                        >
                    </li>
                    <li>
                        <a href="/day3" class="text-gray-700 hover:text-gray-900"
                            >3</a
                        >
                    </li>
                </ul>
            </nav>
        </div>
    </div>
</div>



<div class="container mx-auto pt-16 lg:w-1/3 m:w-full px-8">
    <div class="grid grid-cols-1">
        <slot />
    </div>
</div>

<style>
    .hamburger-button:focus {
        outline: none;
    }
</style>
