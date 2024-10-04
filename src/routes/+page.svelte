<script>
  import { onMount } from 'svelte';
  import FAQs from "$lib/components/FAQs.svelte";
  import Reviews from "$lib/components/Reviews.svelte";

  let clientLogos = [
    { name: 'iGraal' },
    { name: 'SeLoger' },
    { name: 'Agence Fidesio' },
  ];

  let features = [
    { title: 'Membership Organisations', description: 'Our membership management software provides full automation of membership renewals and payments' },
    { title: 'National Associations', description: 'Our membership management software provides full automation of membership renewals and payments' },
    { title: 'Clubs And Groups', description: 'Our membership management software provides full automation of membership renewals and payments' },
  ];

  onMount(() => {
    // Vous pouvez ajouter ici toute initialisation côté client si nécessaire
  });
</script>

<svelte:head>
  <title>Pagellis studio | Shopify Expert Agency</title>
  <meta name="description" content="Expert Shopify | Agence web à Paris.">
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
      <h1 class="text-4xl md:text-5xl font-bold mb-4">Lessons and insights <span class="text-green-500">from 8 years</span></h1>
      <p class="text-xl text-gray-600 mb-6">Where to grow your business as a photographer: site or social media?</p>
      <button class="px-6 py-3 bg-green-500 text-white rounded-md hover:bg-green-600">Register</button>
    </div>
    <div class="md:w-1-2">
      <img src="/images/hero-illustration.png" alt="Hero Illustration" class="w-full" />
    </div>
  </div>
</section>

<section class="clients bg-gray-100 py-16">
  <div class="container mx-auto px-4">
    <h2 class="text-2xl font-bold text-center mb-8">Our Clients</h2>
    <div class="grid grid-cols-3 md:grid-cols-6 gap-8">
      {#each clientLogos as client}
        <img src={client.logo} alt={client.name} class="h-12 object-contain mx-auto" />
      {/each}
    </div>
  </div>
</section>

<section class="features py-16">
  <div class="container mx-auto px-4">
    <h2 class="text-3xl font-bold text-center mb-12">Manage your entire community in a single system</h2>
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
      <img src="/images/testimonial-illustration.png" alt="Testimonial Illustration" class="w-full" />
    </div>
    <div class="md:w-1/2 md:pl-12">
      <h2 class="text-3xl font-bold mb-6">The unseen of spending three years at Pixelgrade</h2>
      <p class="text-gray-600 mb-6">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
      <button class="px-6 py-3 bg-green-500 text-white rounded-md hover:bg-green-600">Learn More</button>
    </div>
  </div>
</section>

<section class="pricing py-16">
  <div class="container mx-auto px-4">
    <h2 class="text-3xl font-bold text-center mb-12">What our clients say</h2>
    <div class="grid md:grid-cols-2 gap-8">
      <Reviews/>
    </div>
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
