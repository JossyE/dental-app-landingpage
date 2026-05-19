<script>
    import ReviewsCard from "./ReviewsCard.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";
    import Stars from "./Stars.svelte";
    let limit = $state(true);
    let reviewsList = [
  {
    "name": "Amina K.",
    "review": "The clinic was very professional and made my child feel comfortable during the entire visit. The check-up and cleaning were handled smoothly, and the staff explained everything clearly.",
    "features": ["Pediatric Dentistry", "Dental Check-ups", "Dental X-rays"]
  },
  {
    "name": "David O.",
    "review": "I went in for teeth whitening and I’m really happy with the results. The process was quick, and the improvement in my smile confidence is noticeable.",
    "features": ["Teeth Whitening", "Cosmetic Dentistry"]
  },
  {
    "name": "Grace M.",
    "review": "I had braces treatment here and also received restorative work on a damaged tooth. The team was very patient and guided me through each stage of treatment.",
    "features": ["Orthodontics", "Restorative Services", "Dental Check-ups"]
  },
  {
    "name": "Tunde A.",
    "review": "I came in for a dental implant and extraction. The procedure was well explained and the recovery support was excellent. I felt well taken care of throughout.",
    "features": ["Dental Implants", "Tooth Extractions", "Oral Surgery"]
  },
  {
    "name": "Chika E.",
    "review": "I had issues with jaw pain and gum infection. The treatment helped a lot and I can now eat comfortably again. The staff were very professional.",
    "features": ["TMJ Treatments", "Gum Disease Treatments", "Endodontic Treatments"]
  },
  {
    "name": "Michael S.",
    "review": "I needed a root canal and follow-up care. The procedure was painless and the dentist explained every step clearly, which helped reduce my anxiety.",
    "features": ["Root Canal Therapy", "Endodontic Treatments", "Dental X-rays"]
  }
]
</script>
<SectionWrapper id='reviews'>
<div class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center">
    <div class="flex flex-col gap-2">
        <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">Don't just take our word for it</p>
        <h3 class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] w-full mx-auto font-semibold text-center">
            See What <span class="text-orange-400">Others</span> Have To Say
        </h3>
    </div>
    <div class="flex flex-col md:flex-row gap-8 w-fit mx-auto">
        <div class="flex flex-col gap-8">
            {#each limit ? reviewsList.slice(0,4) : reviewsList as reviewItem, index }
                <ReviewsCard reviewItem={reviewItem} left={true} {index} />
            {/each}
        </div>
        <div class="w-[1px] bg-slate-950 hidden md:flex"></div>
         <div class="flex flex-col gap-8">
            {#each limit ? reviewsList.slice(0,4) : reviewsList as reviewItem, index }
                <ReviewsCard {reviewItem} {index} />
            {/each}
        </div>
    </div>
    <button on:click={() => limit = !limit} class="specialBtn">
        <p>{limit ? "Show More" : "Show Less"}</p>
    </button>
    <div class="flex flex-col gap-10">
        <p class="mx-auto textlg sm:text-xl md:text-2xl font-semibold">
            Trusted by 1400+ Happy Patients and Counting
        </p>
        <Stars />
    </div>
</div>
</SectionWrapper>