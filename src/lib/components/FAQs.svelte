<script>
    let faqs = [
        {
            question: "What is Pagellis Studio's expertise?",
            ans: "Pixel-perfect integration. We transform the mockups designed for your site into elegant, high-performance web pages that are adapted to all screen sizes.",
        },
        {
            question: "How can we contact you?",
            ans: "Our most effective method is to send us an email at this address: contact [at] pagellis-studio.com",
        },
        {
            question: "I have a question / I would like to know more.",
            ans: "We would be happy to discuss with you, our discovery consultations are free.",
        },

    ];
</script>

<section id="faqs">
    <div
        class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center"
    >
        <div class="flex flex-col gap-8 sm:gap-10 md:gap-14 w-full">
            {#each faqs as faq}
                <div
                    class="flex flex-col gap-2 text-left max-w-[800px] w-full mx-auto relative p-4 px-6"
                >
                    <div
                        class="absolute top-0 left-0 w-1/3 h-[1px] bg-slate-950 -translate-x-4"
                    ></div>
                    <div
                        class="absolute top-0 left-0 h-2/3 w-[1px] bg-slate-950 -translate-y-4"
                    ></div>
                    <h4 class="text-lg sm:text-xl md:text-2xl pt-2">
                        {faq.question}
                    </h4>
                    <p class="pl-2">{faq.ans}</p>
                </div>
            {/each}
        </div>
    </div>
</section>