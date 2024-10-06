<script>
  import FAQs from "$lib/components/FAQs.svelte";
  import Reviews from "$lib/components/Reviews.svelte";
  import heroIllustration from '$lib/images/illustration@2x.png';
  import testimonialIllustration from '$lib/images/mobileloginrafiki@2x.png';
  
  let clientLogos = [
    { name: 'Global Savings Group', logo:'https://www.womentech.net/sites/default/files/styles/cms_bootstrap_1_2/public/2022-01/2022_01_20_0oa_Kleki.png?itok=b_TDvzb1'},
    { name: 'SeLoger', logo:'https://www.groupeseloger.com/images/logo-seloger-header.png' },
    { name: 'Agence Fidesio', logo:'https://www.drupal.org/files/styles/grid-4-2x/public/LOGO-2017-ROND-ROUGE-RVB.png?itok=Fes-lvOd' },
  ];

  let features = [
    { title: 'SEO Friendly', description: 'We love Google and we want Google to love your websites as well' },
    { title: 'Amazing User experience', description: 'Visit our websites shall remain as great as possible, despite our users use their mobile device or their laptop ' },
    { title: 'Performance at the best', description: 'A website shall be performant in the front row' },
];
</script>

<svelte:head>
  <title>Pagellis studio | Web Agency</title>
  <meta name="description" content=" Web Agency based in Paris and dedicated to Front End beautiful integrations.">
  <script type="application/ld+json">
    {
      "@context": "http://schema.org",
      "@type": "LocalBusiness",
      "name": "Pagellis studio",
      "url": "https://pagellis-studio.com/",
      "image": "https://pagellis-studio.com/public/Pagellis-Studio-Logo-Label.png",
      "telephone": "+33661908251",
      "address": {
        "@type": "PostalAddress",
        "addressLocality": "Paris",
        "addressRegion": "Ile-de-France",
        "postalCode": "75002",
        "streetAddress": "9 rue des Colonnes"
      },
      "description": "Expert Shopify | Agence web à Paris.",
      "openingHours": "Monday-Friday 9:00-18:00",
      "priceRange": "€€",
      "geo": {
        "@type": "GeoCoordinates",
        "latitude": 48.8697089,
        "longitude": 2.3394292
      },
      "sameAs": [
        "https://www.linkedin.com/company/pagellis-studio"
      ],
      "logo": "https://pagellis-studio.com/public/Pagellis-Studio-Logo-Label.png",
      "contactPoint": {
        "@type": "ContactPoint",
        "telephone": "+33661908251",
        "contactType": "customer service"
      },
      "aggregateRating": {
        "@type": "AggregateRating",
        "ratingValue": "4.9",
        "reviewCount": "3"
      }
    }
  </script>
</svelte:head>

<section class="hero container mx-auto px-4 py-16 md:py-24">
  <div class="md:flex items-center">
    <div class="md:w-1/2 mb-8 md:mb-0">
      <h1 class="text-4xl md:text-5xl font-bold mb-4">Lessons and insights <span class="text-green-500">from 7 years</span></h1>
      <p class="text-xl text-gray-600 mb-6">We love to find ways to make your business grow.</p>
      <button class="px-6 py-3 bg-green-500 text-white rounded-md hover:bg-green-600">Want to know more?</button>
    </div>
    <div class="md:w-1-2 mx-auto">
      <img src={heroIllustration} alt="" class="w-full" />
    </div>
  </div>
</section>

<section class="clients bg-gray-100 py-16">
  <div class="container mx-auto px-4">
    <h2 class="text-2xl font-bold text-center mb-8">Our Clients</h2>
    <div class="grid grid-cols-3 gap-8">
      {#each clientLogos as client}
        <img src={client.logo} alt={client.name} class="h-12 object-contain mx-auto client-logo" />
      {/each}
    </div>
  </div>
</section>

<section id="services" class="features py-16">
  <div class="container mx-auto px-4">
    <h2 class="text-3xl font-bold text-center mb-12">Our key values</h2>
    <div class="grid md:grid-cols-3 gap-8">
      {#each features as feature}
        <div class="text-center">
          <h3 class="text-xl font-semibold mb-2">{feature.title}</h3>
          <p class="text-gray-600">{feature.description}</p>
        </div>
      {/each}
    </div>
  </div>
</section>

<section class="testimonial bg-gray-100 py-16">
  <div class="container mx-auto px-4 md:flex items-center">
    <div class="md:w-1/2 mb-8 md:mb-0">
      <img src={testimonialIllustration} alt="Testimonial Illustration" class="w-full" />
    </div>
    <div class="md:w-1/2 md:pl-12">
      <h2 class="text-3xl font-bold mb-6">The unseen of spending 7 years in amazing companies</h2>
      <p class="text-gray-600 mb-6">We are always supportive and reactive. A success is mostly the result of a team's work, whare everyone feels involved and happy to contribute. We are always supportive and reactive.</p>
      <button class="px-6 py-3 bg-green-500 text-white rounded-md hover:bg-green-600">Want to work with us ?</button>
    </div>
  </div>
</section>

<section  id="about" class="pricing py-16">
  <div class="container mx-auto px-4">
    <h2 class="text-3xl font-bold text-center mb-12">What our clients say</h2>
    <Reviews/>
  </div>

</section>


<section class="pricing py-16">
  <div class="container mx-auto px-4">
    <h2 class="text-3xl font-bold text-center mb-12">Frequently asked questions</h2>
    <div class="max-w-3xl mx-auto">
      <FAQs/>
    </div>
  </div>
</section>

<style>
  .client-logo {
    filter: brightness(0);
  }

  .client-logo:first-child {
    width: 150px; 
    height: 60px; 
    object-fit: cover;
    object-position: center;  
    }

  img {
    max-height: 300px;
    object-fit: contain;
  }
</style>