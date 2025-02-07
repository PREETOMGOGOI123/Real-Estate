<script>
    // Dummy property listings
    const availableProperties = [
      {
        id: "L001",
        name: "Prime Land in Zoo Road",
        image: "https://images.unsplash.com/photo-1500382017468-9049fed747ef",
        price: "95 L",
        type: "Plot",
        status: "For Sale",
        location: "Zoo Road, Guwahati",
        size: "4000 sq ft",
        features: ["Corner Plot", "Road Facing", "Residential Zone", "Ready to Construct"]
      },
      {
        id: "L002",
        name: "Commercial Plot in Six Mile",
        image: "https://images.unsplash.com/photo-1500076656116-558758c991c1",
        price: "1.2 Cr",
        type: "Plot",
        status: "For Sale",
        location: "Six Mile, Guwahati",
        size: "5000 sq ft",
        features: ["Commercial Zone", "Main Road", "All Utilities", "High ROI"]
      },
      {
        id: "L003",
        name: "Development Land in GS Road",
        image: "https://images.unsplash.com/photo-1500382017468-9049fed747ef",
        price: "2.5 Cr",
        type: "Plot",
        status: "For Sale",
        location: "GS Road, Guwahati",
        size: "8000 sq ft",
        features: ["Prime Location", "Mixed Use Zone", "Wide Road", "Clear Title"]
      },
      {
        id: "L004",
        name: "Residential Plot in Rukminigaon",
        image: "https://images.unsplash.com/photo-1500382017468-9049fed747ef",
        price: "75 L",
        type: "Plot",
        status: "For Sale",
        location: "Rukminigaon, Guwahati",
        size: "2400 sq ft",
        features: ["Residential Area", "Gated Community", "All Papers Clear", "Ready for Construction"]
      }
    ];
  </script>
  
  <!-- Navbar -->
  <div class="navbar bg-base-100 sticky top-0 z-50 shadow-lg">
    <div class="navbar-start">
      <a class="btn btn-ghost normal-case text-xl">🏠 PropertyDeals</a>
    </div>
    <div class="navbar-center hidden lg:flex">
      <ul class="menu menu-horizontal px-1">
        <li><a href="#properties">Properties</a></li>
        <li><a href="#how-it-works">How It Works</a></li>
        <li><a href="#list-property">List Property</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </div>
    <div class="navbar-end">
      <a href="YOUR_GOOGLE_FORM_LINK_FOR_BUYING" class="btn btn-primary">Enquire Now</a>
    </div>
  </div>
  
  <!-- Hero Section -->
  <div class="hero min-h-[70vh] relative" style="background-image: url('https://images.pexels.com/photos/5472526/pexels-photo-5472526.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1'); background-size: cover; background-position: center;">
    <div class="hero-overlay bg-opacity-60"></div>
    <div class="hero-content text-center text-neutral-content">
      <div class="max-w-md">
        <h1 class="text-5xl font-bold text-white mb-8">Find Your Dream Property</h1>
        <p class="py-6 text-white text-lg">Discover premium properties in Aruncahal. Buy or sell with confidence.</p>
        <div class="flex gap-4 justify-center">
          <a href="#properties" class="btn btn-primary btn-lg">View Properties</a>
          <a href="YOUR_GOOGLE_FORM_LINK_FOR_SELLING" class="btn btn-secondary btn-lg">List Property</a>
        </div>
      </div>
    </div>
  </div>
  
  <!-- Property Listings Section -->
  <section id="properties" class="py-16 bg-base-100">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl font-bold text-center mb-12">Featured Properties</h2>
      
      <!-- Property Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        {#each availableProperties as property}
          <div class="card bg-base-100 shadow-xl hover:shadow-2xl transition-shadow duration-300">
            <figure class="relative h-64">
              <img src={property.image} alt={property.name} class="w-full h-full object-cover" />
              <div class="absolute top-4 right-4">
                <span class="badge badge-primary">{property.status}</span>
              </div>
            </figure>
            <div class="card-body">
              <h3 class="card-title">
                {property.name}
                <div class="badge badge-secondary">{property.type}</div>
              </h3>
              <div class="space-y-2">
                <p class="text-primary font-bold text-xl">₹{property.price}</p>
                <p class="text-sm">📍 {property.location}</p>
                <p class="text-sm">📐 {property.size}</p>
                <div class="flex flex-wrap gap-2 mt-2">
                  {#each property.features as feature}
                    <span class="badge badge-outline">{feature}</span>
                  {/each}
                </div>
              </div>
              <div class="card-actions justify-end mt-4">
                <a href="YOUR_GOOGLE_FORM_LINK_FOR_BUYING" class="btn btn-primary">Enquire Now</a>
              </div>
            </div>
          </div>
        {/each}
      </div>
    </div>
  </section>
  
  <!-- How It Works Section -->
  <section id="how-it-works" class="py-16 bg-base-200">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl font-bold text-center mb-12">How It Works</h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8 text-center">
        <div class="card bg-base-100 shadow-xl">
          <div class="card-body">
            <div class="text-4xl mb-4">🏠</div>
            <h3 class="text-xl font-bold mb-4">1. Choose Property</h3>
            <p>Browse our curated collection of premium properties in Arunachal.</p>
          </div>
        </div>
        <div class="card bg-base-100 shadow-xl">
          <div class="card-body">
            <div class="text-4xl mb-4">📝</div>
            <h3 class="text-xl font-bold mb-4">2. Schedule Visit</h3>
            <p>Submit an enquiry and schedule a visit to your chosen property.</p>
          </div>
        </div>
        <div class="card bg-base-100 shadow-xl">
          <div class="card-body">
            <div class="text-4xl mb-4">🤝</div>
            <h3 class="text-xl font-bold mb-4">3. Close the Deal</h3>
            <p>Get assistance with documentation and complete your purchase.</p>
          </div>
        </div>
      </div>
    </div>
  </section>
  
  <!-- List Your Property Section -->
  <section id="list-property" class="py-16 bg-base-100" style="background-image: url('https://images.unsplash.com/photo-1560518883-ce09059eeffa'); background-size: cover; background-position: center;">
    <div class="bg-opacity-90 bg-base-100 py-16">
      <div class="container mx-auto px-4 text-center">
        <h2 class="text-3xl font-bold mb-6">Want to Sell Your Property?</h2>
        <p class="mb-8 text-lg">List your property with us and reach genuine buyers.</p>
        <div class="space-y-4">
          <a href="YOUR_GOOGLE_FORM_LINK_FOR_SELLING" class="btn btn-primary btn-lg">List Your Property</a>
          <p class="text-sm opacity-75">* Verified buyers and hassle-free process</p>
        </div>
      </div>
    </div>
  </section>
  
  <!-- Why Choose Us Section -->
  <section class="py-16 bg-base-200">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl font-bold text-center mb-12">Why Choose Us</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
        <div class="card bg-base-100 shadow-xl">
          <div class="card-body">
            <h3 class="font-bold mb-2">Verified Properties</h3>
            <p>All listings are thoroughly verified</p>
          </div>
        </div>
        <div class="card bg-base-100 shadow-xl">
          <div class="card-body">
            <h3 class="font-bold mb-2">Expert Guidance</h3>
            <p>Professional support throughout the process</p>
          </div>
        </div>
        <div class="card bg-base-100 shadow-xl">
          <div class="card-body">
            <h3 class="font-bold mb-2">Legal Assistance</h3>
            <p>Complete documentation support</p>
          </div>
        </div>
        <div class="card bg-base-100 shadow-xl">
          <div class="card-body">
            <h3 class="font-bold mb-2">Best Deals</h3>
            <p>Competitive prices and transparent process</p>
          </div>
        </div>
      </div>
    </div>
  </section>
  
  <!-- Contact Section -->
  <section id="contact" class="py-16 bg-base-100">
    <div class="container mx-auto px-4 text-center">
      <h2 class="text-3xl font-bold mb-8">Contact Us</h2>
      <div class="max-w-md mx-auto">
        <div class="card bg-base-200 shadow-xl">
          <div class="card-body">
            <p class="mb-4">📞 Call/WhatsApp: +91 XXXXXXXXXX</p>
            <p class="mb-4">📧 Email: contact@propertydeals.com</p>
            <p>📍 Office: Ziro Valley, Aruncahal Pradesh</p>
          </div>
        </div>
      </div>
    </div>
  </section>
  
  <!-- Footer -->
  <footer class="footer footer-center p-10 bg-base-200 text-base-content">
    <div>
      <p class="font-bold">
        PropertyDeals <br/>Your Trusted Real Estate Partner
      </p> 
      <p>© 2024 PropertyDeals - All rights reserved</p>
    </div> 
  </footer>
  
  <style>
    .navbar {
      backdrop-filter: blur(10px);
      background-color: rgba(255, 255, 255, 0.9);
    }
  </style>