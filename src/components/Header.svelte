<script>
import {openModal} from "../store/index.js";
</script>

<header class="flex flex-col relative z-20">
    <div
        class="max-w-350 mx-auto w-full flex items-center justify-between p-4 py-6"
    >
        <a href="/">
            <h1 class="font-semibold text-orange-400">Molly</h1>
        </a>
        <button
            on:click={() => $openModal = true}
            class="md:hidden grid place-items-center"
            aria-label="Open menu"
        >
            <i class="fa fa-bars" aria-hidden="true"></i>
        </button>
        <nav class="hidden md:flex items-center gap-4 lg:gap-6">
            <a class="duration-200 text-orange-400 cursor-pointer" href="#products">Products</a>
            <a class="duration-200 text-orange-400 cursor-pointer" href="#reviews">Reviews</a>
            <a class="duration-200 text-orange-400 cursor-pointer" href="#faqs">FAQ</a>
            <button class="specialBtn text-orange-400"><p>Start Free Today</p></button>
        </nav>
    </div>
</header>
