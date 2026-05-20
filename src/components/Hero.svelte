<script>
    import CTAs from "./CTAs.svelte";
    import Header from "./Header.svelte";
    import Stars from "./Stars.svelte";
</script>

<section
    class="min-h-screen w-full flex flex-col items-start justify-end bg-[url('/assets/dental.jpg')] bg-cover bg-center relative after:content-[''] after:absolute after:inset-0 after:bg-black/50"
>
    <div class="flex flex-col flex-1 w-full relative z-10 pb-10 md:pb-14">
        <Header />
        <div class="flex md:flex-row flex-col gap-6 justify-between items-end flex-1 w-full px-4">

            <div
                class="flex flex-col gap-8 flex-1 text-white items-end justify-end px-4"
            >
                <h2
                    class="text-5xl sm:text-6xl md:text-7xl lg:text-8xl max-w-300 mx-auto w-full text-left font-semibold"
                >
                    Your <span class="text-orange-400">Journey </span> To A <br />
                    <span class="text-orange-400">Radiant Smile</span> Starts Here
                </h2>
                <p
                    class="text-md sm:text-xl md:text-2xl max-w-300 mx-auto text-white w-full text-left"
                >Discover the joy of a healthy,<br/> beautiful smile with our <span
                        class="italic"
                        >expert
                    </span> dental care.
                </p>
            </div>
            <div class="flex flex-col items-start gap-10">
                <CTAs  />
                <Stars />
            </div>
        </div>
    </div>
</section>
