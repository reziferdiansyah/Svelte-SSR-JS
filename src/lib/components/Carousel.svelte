<script>
    import { ChevronRightIcon, ChevronLeftIcon } from "svelte-feather-icons";
    let current = 0;
    const slides = [
        { id: 1, img: "/images/slide1.jpg", title: "Welcome to MySite" },
        { id: 2, img: "/images/slide2.jpg", title: "Discover Our Services" },
        { id: 3, img: "/images/slide3.jpg", title: "Contact Us Anytime" },
    ];
    const next = () => (current = (current + 1) % slides.length);
    const prev = () =>
        (current = (current - 1 + slides.length) % slides.length);
    // Auto-slide every 5 seconds
    import { onMount } from "svelte";
    onMount(() => {
        const interval = setInterval(next, 5000);
        return () => clearInterval(interval);
    });
</script>

<div class="relative w-full overflow-hidden">
    <!-- Slides -->
    <div
        class="flex transition-transform duration-500 ease-in-out"
        style="transform: translateX(-{current * 100}%)"
    >
        {#each slides as slide (slide.id)}
            <div class="w-full flex-shrink-0">
                <img
                    src={slide.img}
                    alt={slide.title}
                    class="w-full h-64 object-cover md:h-[500px]"
                />
                <div
                    class="absolute inset-0 bg-black bg-opacity-30 flex items-center justify-center"
                >
                </div>
            </div>
        {/each}
    </div>
    <!-- Prev/Next Buttons -->
    <button
        on:click={prev}
        class="absolute top-1/2 left-2 transform -translate-y-1/2 bg-blue-500 bg-opacity-70 hover:bg-opacity-90 p-2 rounded-full"
    >
        <ChevronLeftIcon size="1.5x" />
    </button>
    <button
        on:click={next}
        class="absolute top-1/2 right-2 transform -translate-y-1/2 bg-blue-500 bg-opacity-70 hover:bg-opacity-90 p-2 rounded-full"
    >
        <ChevronRightIcon size="1.5x" />
    </button>
    <!-- Indicators -->
    <div
        class="absolute bottom-4 left-1/2 transform -translate-x-1/2 flex gap-2"
    >
        {#each slides as _, i}
            <span
                class="w-3 h-3 rounded-full"
                class:bg-white={current === i}
                class:bg-gray-400={current !== i}
                on:click={() => (current = i)}
            >
            </span>
        {/each}
    </div>
</div>
