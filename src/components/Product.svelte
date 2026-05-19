<script>
    import ProductCard from "./ProductCard.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";
    let productFeatures = [
        {
            featureList: [
                'Pediatric Dentistry',
                'Dental Check-ups',
                'Dental Sealants',
                'Dental X-rays',
                'Gum Disease Treatments'
            ],
            description: 'Care focused on preventing dental problems, maintaining long-term oral health, and early diagnosis for patients of all ages.',
            imageUrl: ' assets/den1.jpg'
        },
        {
            featureList: [
                'Cosmetic Dentistry',
                'Teeth Whitening',
                'Orthodontics',
                'Restorative Services',
                'Dental Implants'
            ],
            description: 'Services that improve the appearance, function, and overall structure of your smile through aesthetic and restorative solutions.',
            imageUrl: 'assets/den2.jpg'
        },
        {
            featureList: [
                'Oral Surgery',
                'Tooth Extractions',
                'Gum Surgery',
                'TMJ Treatments',
                'Endodontic Treatments'
            ],
            description: 'Advanced treatments for complex dental conditions, pain management, infections, and oral function restoration.',
            imageUrl: 'assets/den3.jpg'
        },
    ]

</script>
<SectionWrapper id='products'>
    <div class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14 mt-10">
        <div class="flex flex-col gap-2">
            <p class="opacity-60 text-base sm:text-lg text-orange-400 md:text-xl text-center">
                Smile Services
            </p>
            <h3 class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center">
                Our Dental Offerings
            </h3>
        </div>
        
            {#each productFeatures as productFeature, index}
                <ProductCard productFeature={productFeature} index={index}>
                    {#if index === 0}
                    <span class="text-orange-400">Preventive,</span> Family & Diagnostic Dentistry
                    {:else if index === 1}
                    Cosmetic & <span class="text-orange-400">Restorative </span> Dentistry
                    {:else}
                    Surgical, <span class="text-orange-400">Specialized</span> & Therapeutic Care
                    {/if}
                </ProductCard>
            {/each}
    </div>
</SectionWrapper> 