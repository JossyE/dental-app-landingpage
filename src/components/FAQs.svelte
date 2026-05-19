<script>
    import SectionWrapper from "./SectionWrapper.svelte";
    let faqs = [
        {
            question: "What dental services do you offer?",
            ans: "We offer a comprehensive range of dental services including preventive care, cosmetic dentistry, orthodontics, restorative treatments, oral surgery, and specialized therapies to meet all your dental needs."
        },
        {
            question: "How can I book an appointment?",
            ans: "You can easily book an appointment by calling our clinic directly, using our online booking system on our website, or through our mobile app for added convenience."
        },
        {
            question: "Do you accept dental insurance?",
            ans: "Yes, we accept a wide range of dental insurance plans. Please contact our office to verify if we accept your specific insurance provider and to understand the coverage details."
        },
        {
            question: "What should I expect during my first visit?",
            ans: "During your first visit, you can expect a thorough dental examination, including X-rays if necessary. Our team will discuss your dental history, address any concerns you may have, and create a personalized treatment plan tailored to your needs."
        },
        {
            question: "How do I maintain good oral hygiene at home?",
            ans: "Maintaining good oral hygiene involves brushing your teeth at least twice a day with fluoride toothpaste, flossing daily to remove plaque between teeth, using mouthwash for added protection, and scheduling regular dental check-ups for professional cleanings and early detection of any issues."
        }
    ]
</script>


<SectionWrapper id='faqs'>
<div class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center">
    <div class="flex flex-col gap-2">
        <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">For all your dental questions</p>
        <h3 class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] w-full mx-auto font-semibold text-center">
            Frequently Asked Questions
        </h3>
    </div>
    <div class="flex flex-col gap-8 sm:gap-10 md:gap-14 w-full">
        {#each faqs as faq}
        <div class="flex flex-col gap-2 text-left max-w-[800px] w-full mx-auto relative p-4 px-6">
            <div class="absolute top-0 left-0 w-1/3 h-[1px] bg-slate-950 -translate-x-4"></div>
            <div class="absolute top-0 left-0 w-[1px] h-2/3 bg-slate-950 -translate-y-4"></div>
            <h4 class="text-lg sm:text-xl md:text-2xl pt-2">{faq.question}</h4>
            <p class="pl-2">{faq.ans}</p>
        </div>
        {/each}
    </div>
</div>
</SectionWrapper>