<script>
    import ReviewCard from "./ReviewCard.svelte";

    let lim = true;

    let reviewsList = [

        {
            name: "Sabri El Gharbi",
            review: "I had the pleasure to be Pascal's manager and Lead Developer for more than two years at GSG, and I can confidently say he is an exceptional frontend developer. His expertise in JavaScript and React has consistently driven our Gift Card with Cashback project to success, navigating challenges with skill and determination.Beyond his technical prowess, Pascal stands out for his remarkable character. He is a compassionate team player, always ready to lend an ear and offer support. His dedication to the team's well-being and collaboration is truly commendable.I highly recommend Pascal for any frontend development role. He is a valuable asset to any team.",
            features: [
                "Global Savings Group",
                "Team Manager",
                "Lead Developer",
            ],
        },
        {
            name: "Helen Mameri",
            review: "I worked with Pascal for over two years at iGraal (GSG) and I can highly recommend him to anyone looking for a very good developer. His expertise in front-end development is now accompanied by strong Shopify skills that will allow you to put a personalized and efficient application online for your store. Pascal is a person who is committed to doing things correctly, according to best practices and who communicates and collaborates perfectly with the members of his team. It is a pleasure to work with such a pleasant and competent person.",
            features: [
                "iGraal France",
                "Full-stack Developer",
            ],
        },
        {
            name: "Farouk Younsi",
            review: "Pascal is dedicated to the team's efforts and success. He is a team player who is always willing to help and support his colleagues. His positive attitude and willingness to learn make him a valuable asset to any team.",
            features: [
                "OpenClassrooms",
                "Mentor",
            ],
        },
    ];
</script>

<section id="reviews">
     <div
        class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center"
    >
        <div class="flex flex-col md:flex-row gap-8 w-fit mx-auto">
            <div class="flex flex-col gap-8">
                {#each lim ? reviewsList.slice(0, 1) : reviewsList as reviewItem, index}
                    <ReviewCard {reviewItem} left={true} {index} />
                {/each}
            </div>
            <div class="w-[1px] bg-slate-950 hidden md:flex"></div>
            <div class="flex flex-col gap-8">
                {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
                    <ReviewCard {reviewItem} {index} />
                {/each}
            </div>
        </div>
        <button on:click={() => (lim = !lim)} class="specialBtn">
            <p>{lim ? "Show More" : "Show Less"}</p>
        </button>
    </div>
</section>