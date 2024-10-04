<script>
    let faqs = [
        {
            question: "Qu'est-ce que Swoley Moley ?",
            ans: "Swoley Moley est une application de fitness amusante conçue pour rendre vos entraînements agréables en incorporant des jeux et des défis interactifs.",
        },
        {
            question: "Comment puis-je télécharger Swoley Moley ?",
            ans: "Vous pouvez télécharger Swoley Moley depuis l'App Store (pour iOS) ou le Google Play Store (pour Android) sur votre appareil mobile.",
        },
        {
            question: "Swoley Moley est-il gratuit ?",
            ans: "Oui, Swoley Moley propose une version gratuite avec des fonctionnalités de base. Il existe également un abonnement premium qui débloque des jeux supplémentaires et un suivi avancé des entraînements.",
        },
        {
            question: "Quels types d'entraînements Swoley Moley propose-t-il ?",
            ans: "Swoley Moley propose une variété d'entraînements, notamment du cardio, du renforcement musculaire et des exercices de flexibilité. Les entraînements sont conçus pour être engageants et divertissants.",
        },
        {
            question: "Puis-je connecter Swoley Moley à mon tracker d'activité ?",
            ans: "Oui, Swoley Moley prend en charge l'intégration avec les trackers d'activité populaires, vous permettant de synchroniser vos données d'entraînement et de suivre vos progrès de manière transparente.",
        },
        {
            question: "Y a-t-il des fonctionnalités multijoueurs dans Swoley Moley ?",
            ans: "Oui, Swoley Moley inclut des défis multijoueurs, vous permettant de rivaliser avec des amis ou de rejoindre des entraînements en groupe pour une expérience plus interactive et sociale.",
        },
        {
            question: "Comment Swoley Moley motive-t-il les utilisateurs à rester actifs ?",
            ans: "Swoley Moley utilise un système de récompenses, où les utilisateurs gagnent des points et des réalisations en complétant des entraînements. Ces récompenses peuvent être utilisées pour débloquer de nouveaux niveaux, défis et contenus dans l'application.",
        },
        {
            question: "Puis-je personnaliser mes entraînements dans Swoley Moley ?",
            ans: "Absolument ! Swoley Moley permet aux utilisateurs de personnaliser leurs entraînements en fonction de leurs préférences personnelles, de leurs objectifs de fitness et de l'équipement disponible.",
        },
        {
            question: "Y a-t-il un mode adapté aux débutants dans Swoley Moley ?",
            ans: "Oui, Swoley Moley propose un mode adapté aux débutants avec des exercices plus faciles et des entraînements moins intenses, le rendant approprié pour les utilisateurs de différents niveaux de forme physique.",
        },
        {
            question: "À quelle fréquence dois-je utiliser Swoley Moley pour des résultats optimaux ?",
            ans: "La fréquence des entraînements Swoley Moley dépend de vos objectifs de fitness. Il est recommandé de participer à au moins 3 à 5 sessions par semaine pour des résultats notables.",
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