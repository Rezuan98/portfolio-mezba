<template>
  <div>
    <!-- Hero Section -->
    <section id="hero" class="relative min-h-screen flex items-center justify-center overflow-hidden bg-gradient-to-br from-blue-50 via-indigo-100 to-purple-200 dark:from-gray-900 dark:via-indigo-950 dark:to-purple-950">
      <canvas ref="heroCanvas" class="absolute inset-0 w-full h-full opacity-40 dark:opacity-60"></canvas>
      
      <!-- Floating Elements Background -->
      <div class="absolute inset-0 overflow-hidden pointer-events-none">
        <div class="floating-element absolute top-20 left-10 w-20 h-20 bg-gradient-to-br from-blue-400 to-cyan-400 rounded-full opacity-20 animate-float-slow"></div>
        <div class="floating-element absolute top-40 right-20 w-16 h-16 bg-gradient-to-br from-purple-400 to-pink-400 rounded-full opacity-20 animate-float-medium"></div>
        <div class="floating-element absolute bottom-40 left-20 w-24 h-24 bg-gradient-to-br from-yellow-400 to-orange-400 rounded-full opacity-20 animate-float-fast"></div>
        <div class="floating-element absolute bottom-20 right-10 w-12 h-12 bg-gradient-to-br from-green-400 to-emerald-400 rounded-full opacity-20 animate-float-slow"></div>
      </div>
      
      <div class="relative z-10 max-w-7xl mx-auto px-4 pt-16 sm:px-6 lg:px-8 w-full">
        <!-- Mobile Layout: Image First -->
        <div class="flex flex-col lg:hidden items-center text-center space-y-8">
          <!-- Mobile Image -->
          <div class="w-72 h-72 sm:w-80 sm:h-80 rounded-full overflow-hidden shadow-2xl border-4 border-white dark:border-gray-700 bg-gradient-to-br from-blue-400 via-purple-500 to-pink-500 p-1 animate-pulse-glow">
            <div class="w-full h-full rounded-full overflow-hidden">
              <img 
                src="/public/mezba.jpg" 
                alt="MD Sharif Hossain" 
                class="w-full h-full object-cover hover:scale-110 transition-transform duration-700"
              />
            </div>
          </div>
          
          <!-- Mobile Content -->
          <div class="space-y-6">
            <h1 class="text-4xl sm:text-5xl md:text-6xl font-bold  text-white animate-gradient-x">
              MD Sharif Hossain
            </h1>
            <p class="text-xl sm:text-2xl font-semibold bg-gradient-to-r from-blue-600 via-purple-600 to-pink-600 dark:from-blue-400 dark:via-purple-400 dark:to-pink-400 bg-clip-text text-transparent">
              Award-Winning Digital Marketing Strategist
            </p>
            <p class="text-lg leading-relaxed text-gray-700 dark:text-gray-300 max-w-2xl">
              Delivering data-driven campaigns that drive measurable sales impact for brands like Unilever, Bata, Bkash, and Castrol. First-ever Bangladesh wins at major global marketing award competitions.
            </p>
          </div>
        </div>

        <!-- Desktop Layout: Side by Side -->
        <div class="hidden lg:grid lg:grid-cols-2 gap-16 items-center">
          <!-- Left Content -->
          <div class="text-center lg:text-left space-y-8">
            <h1 class="text-4xl xl:text-6xl font-bold  text-white animate-gradient-x leading-tight">
              MD Sharif Hossain
            </h1>
            <p class="text-2xl xl:text-3xl font-semibold bg-gradient-to-r from-blue-600 via-purple-600 to-pink-600 dark:from-blue-400 dark:via-purple-400 dark:to-pink-400 bg-clip-text text-transparent">
              Award-Winning Digital Marketing Strategist
            </p>
            <p class="text-lg xl:text-xl leading-relaxed text-gray-700 dark:text-gray-300">
              Delivering data-driven campaigns that drive measurable sales impact for brands like Unilever, Bata, Bkash, and Castrol. First-ever Bangladesh wins at major global marketing award competitions.
            </p>
            
            <div class="flex flex-wrap justify-center lg:justify-start gap-3">
              <span class="skill-badge bg-gradient-to-r from-blue-500 to-cyan-500 text-white">
                Planning Strategist
              </span>
              <span class="skill-badge bg-gradient-to-r from-purple-500 to-pink-500 text-white">
                Campaign Expert
              </span>
              <span class="skill-badge bg-gradient-to-r from-green-500 to-emerald-500 text-white">
                Award Winner
              </span>
            </div>
            
            <div class="flex flex-col sm:flex-row gap-4 justify-center lg:justify-start">
              <a href="#achievements" class="btn-primary">
                View Achievements
              </a>
              <a href="#contact" class="btn-secondary">
                Contact Me
              </a>
            </div>
          </div>

          <!-- Right Image -->
          <div class="flex justify-center lg:justify-end">
            <div class="w-80 h-80 xl:w-96 xl:h-96 rounded-full overflow-hidden shadow-2xl border-4 border-white dark:border-gray-700 bg-gradient-to-br from-blue-400 via-purple-500 to-pink-500 p-1 animate-pulse-glow">
              <div class="w-full h-full rounded-full overflow-hidden">
                <img 
                  src="/public/mezba.jpg" 
                  alt="MD Sharif Hossain" 
                  class="w-full h-full object-cover hover:scale-110 transition-transform duration-700"
                />
              </div>
            </div>
          </div>
        </div>

        <!-- Common Action Buttons for Mobile -->
        <div class="lg:hidden flex flex-col sm:flex-row gap-4 justify-center mt-8">
          <a href="#achievements" class="btn-primary">
            View Achievements
          </a>
          <a href="#contact" class="btn-secondary">
            Contact Me
          </a>
        </div>

        <!-- Tags for Mobile -->
        <div class="lg:hidden flex flex-wrap justify-center gap-3 mt-8">
          <span class="skill-badge bg-gradient-to-r from-blue-500 to-cyan-500 text-white">
            Planning Strategist
          </span>
          <span class="skill-badge bg-gradient-to-r from-purple-500 to-pink-500 text-white">
            Campaign Expert
          </span>
          <span class="skill-badge bg-gradient-to-r from-green-500 to-emerald-500 text-white">
            Award Winner
          </span>
        </div>
      </div>

      <!-- Scroll Indicator -->
      <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 animate-bounce">
        <div class="w-6 h-10 border-2 border-gray-400 dark:border-gray-500 rounded-full flex justify-center">
          <div class="w-1 h-3 bg-gradient-to-b from-blue-500 to-purple-500 rounded-full mt-2 animate-scroll"></div>
        </div>
      </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-20 px-4 sm:px-6 lg:px-8 bg-gradient-to-br from-slate-50 via-blue-50 to-indigo-100 dark:from-gray-800 dark:via-slate-800 dark:to-indigo-900">
      <div class="max-w-7xl mx-auto">
        <h2 class="section-title">
          About Me
        </h2>
        <div class="grid lg:grid-cols-2 gap-12 xl:gap-16 items-center">
          <div class="space-y-6">
            <p class="text-lg leading-relaxed text-gray-700 dark:text-gray-300">
              I'm an award-winning Digital Marketing Strategist with proven expertise delivering data-driven campaigns 
              that drive measurable sales impact across industries from FMCG to tech and finance. Currently at 
              Mindshare Bangladesh, I work with major brands including Unilever, Bata, Bkash, and Castrol.
            </p>
            <p class="text-lg leading-relaxed text-gray-700 dark:text-gray-300">
              My executional expertise across Meta Ads, Google Ads, TikTok, DV360, and GA4 enables me to build 
              performance-focused, personalized campaigns. I've led work that earned Bangladesh its first-ever 
              wins at major global marketing award competitions.
            </p>
            <div class="flex flex-wrap gap-3">
              <span class="badge bg-gradient-to-r from-blue-100 to-cyan-100 dark:from-blue-900/30 dark:to-cyan-900/30 text-blue-700 dark:text-cyan-300 border border-blue-200 dark:border-cyan-700">IELTS Score: 8</span>
              <span class="badge bg-gradient-to-r from-purple-100 to-pink-100 dark:from-purple-900/30 dark:to-pink-900/30 text-purple-700 dark:text-pink-300 border border-purple-200 dark:border-pink-700">Multiple Global Awards</span>
              <span class="badge bg-gradient-to-r from-green-100 to-emerald-100 dark:from-green-900/30 dark:to-emerald-900/30 text-green-700 dark:text-emerald-300 border border-green-200 dark:border-emerald-700">Campaign Innovation</span>
            </div>
          </div>
          <div class="stats-card">
            <h3 class="text-2xl font-bold mb-8 bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">Quick Stats</h3>
            <div class="space-y-6">
              <div class="stat-item">
                <span class="text-gray-700 dark:text-gray-300">Current Role</span>
                <span class="font-bold bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">Digital Operations Specialist</span>
              </div>
              <div class="stat-item">
                <span class="text-gray-700 dark:text-gray-300">Global Awards</span>
                <span class="font-bold bg-gradient-to-r from-yellow-600 to-orange-600 bg-clip-text text-transparent">5+ Gold/Silver</span>
              </div>
              <div class="stat-item">
                <span class="text-gray-700 dark:text-gray-300">Campaign Platform</span>
                <span class="font-bold bg-gradient-to-r from-green-600 to-emerald-600 bg-clip-text text-transparent">10+ Platforms</span>
              </div>
              <div class="stat-item">
                <span class="text-gray-700 dark:text-gray-300">Education</span>
                <span class="font-bold bg-gradient-to-r from-pink-600 to-red-600 bg-clip-text text-transparent">B.Sc. Engineering</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Experience Section -->
    <!-- ExperienceSection.vue - Updated with new Unilever role -->

  <section id="experience" class="py-20 px-4 bg-gray-950">
    <div class="max-w-6xl mx-auto">
      <h2 class="text-4xl font-bold text-center mb-16 bg-gradient-to-r from-blue-400 to-blue-500 bg-clip-text text-transparent">
        Professional Experience
      </h2>
      
      <div class="max-w-3xl mx-auto">
        <div class="relative">
          <!-- Timeline line -->
          <div class="absolute left-8 top-0 bottom-0 w-0.5 bg-gradient-to-b from-blue-500 to-blue-600"></div>
          
          <!-- Current Role - Unilever -->
          <div class="relative pl-20 pb-12">
            <div class="absolute left-6 top-0 w-4 h-4 bg-green-500 rounded-full border-4 border-black animate-pulse"></div>
            <div class="bg-gradient-to-br from-black to-gray-900 p-6 rounded-2xl border border-green-800/50 shadow-lg shadow-green-500/10">
              <div class="flex items-center gap-2 mb-2">
                <h3 class="text-xl font-semibold text-green-400">Digital Operations Specialist</h3>
                <span class="px-2 py-1 bg-green-500/20 text-green-300 rounded-full text-xs font-medium">Current</span>
              </div>
              <p class="text-gray-400 mb-3">Unilever Bangladesh • August 2025 - Present</p>
              <div class="space-y-3 mb-4">
                <p class="text-gray-300 leading-relaxed">
                  Managing end-to-end DDM platforms (Gigya, Dataiku, Adobe Audience Manager, Adobe Analytics, Campaign Wizard) 
                  for consumer data acquisition, segmentation and remarketing as the sole Unilever employee authorized to handle consumer data.
                </p>
                <p class="text-gray-300 leading-relaxed">
                  Creating audience segments aligned with data strategy and JTBDs, championing DDM marketing and personalized content 
                  to drive superior digital performance across brands and categories.
                </p>
                <p class="text-gray-300 leading-relaxed">
                  Bridging brands, IT and legal teams for data governance, risk mitigation, and ensuring legally compliant data collection 
                  while supporting performance marketing campaigns and e-commerce partnerships.
                </p>
              </div>
              <div class="flex flex-wrap gap-2">
                <span class="px-3 py-1 bg-green-500/20 text-green-300 rounded-full text-sm">Data Analytics</span>
                <span class="px-3 py-1 bg-green-500/20 text-green-300 rounded-full text-sm">Adobe Suite</span>
                <span class="px-3 py-1 bg-green-500/20 text-green-300 rounded-full text-sm">Consumer Segmentation</span>
                <span class="px-3 py-1 bg-green-500/20 text-green-300 rounded-full text-sm">Data Governance</span>
                <span class="px-3 py-1 bg-green-500/20 text-green-300 rounded-full text-sm">Performance Marketing</span>
              </div>
            </div>
          </div>

          <!-- Previous Role - Asiatic Mindshare -->
          <div class="relative pl-20 pb-12">
            <div class="absolute left-6 top-0 w-4 h-4 bg-blue-500 rounded-full border-4 border-black"></div>
            <div class="bg-gradient-to-br from-black to-gray-900 p-6 rounded-2xl border border-gray-800">
              <h3 class="text-xl font-semibold mb-2 text-blue-400">Planning Strategist (Digital Marketing)</h3>
              <p class="text-gray-400 mb-3">Asiatic Mindshare Ltd. • July 2023 - August 2025</p>
              <div class="space-y-3 mb-4">
                <p class="text-gray-300 leading-relaxed">
                  Led strategy, planning, and execution of digital campaigns for major brands including Unilever 
                  (Pureit, Rin, Surf Excel, Wheel, Horlicks), Bata, Bkash, and Castrol.
                </p>
                <p class="text-gray-300 leading-relaxed">
                  Delivered award-winning campaigns across Meta, Google, DV360, and TikTok platforms. Executed innovative 
                  campaigns like "AR Shoe Trial" for BATA and "Rin Beep Call" - first of its kind in Bangladesh.
                </p>
              </div>
              <div class="flex flex-wrap gap-2">
                <span class="px-3 py-1 bg-blue-500/20 text-blue-300 rounded-full text-sm">Strategy Planning</span>
                <span class="px-3 py-1 bg-blue-500/20 text-blue-300 rounded-full text-sm">Campaign Execution</span>
                <span class="px-3 py-1 bg-blue-500/20 text-blue-300 rounded-full text-sm">Multi-Platform</span>
                <span class="px-3 py-1 bg-blue-500/20 text-blue-300 rounded-full text-sm">Award-Winning</span>
                <span class="px-3 py-1 bg-blue-500/20 text-blue-300 rounded-full text-sm">Innovation</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>




    <!-- Skills Section -->
    <section id="skills" class="py-20 px-4 sm:px-6 lg:px-8 bg-gradient-to-br from-slate-50 via-blue-50 to-indigo-100 dark:from-gray-800 dark:via-slate-800 dark:to-indigo-900">
      <div class="max-w-7xl mx-auto">
        <h2 class="section-title">
          Technical Expertise
        </h2>
        
        <div class="grid md:grid-cols-2 xl:grid-cols-3 gap-8">
          <!-- Digital Marketing -->
          <div class="skill-card group hover:scale-105">
            <h3 class="text-xl xl:text-2xl font-bold mb-6 bg-gradient-to-r from-blue-600 to-cyan-600 bg-clip-text text-transparent">Digital Marketing</h3>
            <div class="space-y-4">
              <div v-for="skill in skills.digital" :key="skill" class="skill-progress-item">
                <span class="text-sm font-medium text-gray-700 dark:text-gray-300">{{ skill }}</span>
                <div class="skill-progress-bar">
                  <div class="skill-progress-fill bg-gradient-to-r from-blue-500 to-cyan-500" :style="{width: `${85 + Math.random() * 15}%`}"></div>
                </div>
              </div>
            </div>
          </div>

          <!-- Technical Skills -->
          <div class="skill-card group hover:scale-105">
            <h3 class="text-xl xl:text-2xl font-bold mb-6 bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent">Technical Skills</h3>
            <div class="space-y-4">
              <div v-for="skill in skills.technical" :key="skill" class="skill-progress-item">
                <span class="text-sm font-medium text-gray-700 dark:text-gray-300">{{ skill }}</span>
                <div class="skill-progress-bar">
                  <div class="skill-progress-fill bg-gradient-to-r from-purple-500 to-pink-500" :style="{width: `${75 + Math.random() * 20}%`}"></div>
                </div>
              </div>
            </div>
          </div>

          <!-- Certifications -->
          <div class="skill-card group hover:scale-105 md:col-span-2 xl:col-span-1">
            <h3 class="text-xl xl:text-2xl font-bold mb-6 bg-gradient-to-r from-green-600 to-emerald-600 bg-clip-text text-transparent">Certifications</h3>
            <div class="space-y-4">
              <div v-for="cert in skills.certifications" :key="cert" class="certification-item">
                <span class="text-sm font-medium text-gray-800 dark:text-gray-200">{{ cert }}</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Achievements Section -->
  <section id="achievements" class="py-20 px-4 bg-gray-950">
    <div class="max-w-6xl mx-auto">
      <h2 class="text-4xl font-bold text-center mb-16 bg-gradient-to-r from-yellow-400 to-orange-500 bg-clip-text text-transparent">
        Awards & Achievements
      </h2>
      
      <!-- Achievement Gallery Header -->
      <div class="mb-12">
        <h3 class="text-2xl font-bold mb-8 text-center bg-gradient-to-r from-yellow-600 to-orange-600 bg-clip-text text-transparent">
          Prize Ceremony Gallery
        </h3>
        
        <!-- Add this to your template - replace the existing gallery section -->
<!-- Replace your gallery section with this -->
<div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-4 xl:grid-cols-6 gap-4">
  <div v-for="i in 22" :key="i" class="relative group cursor-pointer overflow-hidden rounded-lg" @click="openModal(`/aw${i}.jpg`, `Award ceremony photo ${i}`)">
    <img 
      :src="`/aw${i}.jpg`" 
      :alt="`Award ceremony photo ${i}`"
      class="w-full h-auto transition-transform duration-300 group-hover:scale-110 pointer-events-none"
      loading="lazy"
    />
    <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-transparent to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end justify-center pb-2">
      <p class="text-xs text-white font-medium">Click to view</p>
    </div>
  </div>
</div>

<!-- Fullscreen Modal -->
<div 
  v-if="modalOpen" 
  class="fixed inset-0 z-50 flex items-center justify-center bg-black bg-opacity-90 backdrop-blur-sm"
  @click="closeModal"
>
  <div class="relative max-w-7xl max-h-screen p-4 w-full h-full flex items-center justify-center">
    <!-- Close Button -->
    <button 
      @click="closeModal"
      class="absolute top-4 right-4 z-10 w-12 h-12 bg-black bg-opacity-50 hover:bg-opacity-70 rounded-full flex items-center justify-center text-white text-2xl transition-all duration-300 hover:scale-110"
    >
      ×
    </button>
    
    <!-- Image -->
    <img 
      :src="modalImage" 
      :alt="modalAlt"
      class="max-w-full max-h-full object-contain rounded-lg shadow-2xl"
      @click.stop
    />
    
    <!-- Image Title -->
    <div class="absolute bottom-4 left-1/2 transform -translate-x-1/2 bg-black bg-opacity-70 px-4 py-2 rounded-full">
      <p class="text-white text-sm font-medium">{{ modalAlt }}</p>
    </div>
  </div>
</div>
      </div>

      <!-- Achievements Grid -->
      <div class="grid sm:grid-cols-2 lg:grid-cols-3 gap-6 xl:gap-8 mb-16">
        <div v-for="(achievement, index) in achievements" :key="index" 
             class="bg-gradient-to-br from-black to-gray-900 p-6 rounded-2xl border border-gray-800 hover:border-yellow-500/50 transition-all duration-300 group">
          <div class="flex items-start justify-between mb-4">
            <div class="w-12 h-12 bg-gradient-to-r from-yellow-500 to-orange-500 rounded-full flex items-center justify-center">
              <span class="text-white font-bold text-lg">🏆</span>
            </div>
            <span class="px-3 py-1 bg-yellow-500/20 text-yellow-300 rounded-full text-sm font-medium">
              {{ achievement.year }}
            </span>
          </div>
          <h3 class="text-lg font-bold mb-3 bg-gradient-to-r from-yellow-600 to-orange-600 bg-clip-text text-transparent">
            {{ achievement.title }}
          </h3>
          <p class="text-sm text-gray-400 leading-relaxed">
            {{ achievement.event }}
          </p>
        </div>
      </div>

      <!-- Call to Action -->
      <div class="text-center">
        <p class="text-lg sm:text-xl lg:text-2xl font-bold mb-6 bg-gradient-to-r from-yellow-600 via-orange-500 to-red-500 bg-clip-text text-transparent">
          First-ever Bangladesh wins at major global marketing competitions
        </p>
        <a href="#contact" 
           class="inline-block px-8 py-3 text-base font-semibold text-white bg-gradient-to-r from-red-600 to-red-700 rounded-full shadow-lg hover:shadow-red-500/25 hover:scale-105 transition-all duration-300">
          Let's Create Award-Winning Campaigns
        </a>
      </div>
    </div>
  </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20 px-4 sm:px-6 lg:px-8 bg-gradient-to-br from-slate-50 via-blue-50 to-indigo-100 dark:from-gray-800 dark:via-slate-800 dark:to-indigo-900">
      <div class="max-w-5xl mx-auto text-center">
        <h2 class="section-title">
          Let's Drive Results Together
        </h2>
        <p class="text-xl xl:text-2xl mb-16 text-gray-700 dark:text-gray-300 leading-relaxed max-w-3xl mx-auto">
          Ready to create award-winning campaigns that deliver measurable impact? 
          Let's discuss how we can accelerate your brand's growth.
        </p>
        
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6 xl:gap-8 mb-16">
          <div class="contact-card group">
            <div class="contact-icon bg-gradient-to-br from-blue-500 to-cyan-500">
              <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
              </svg>
            </div>
            <h3 class="text-lg font-bold mb-2">Email</h3>
            <p class="text-sm text-gray-600 dark:text-gray-400 break-all">sharifhossainmezba@gmail.com</p>
          </div>
          
          <div class="contact-card group">
            <div class="contact-icon bg-gradient-to-br from-purple-500 to-pink-500">
              <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"></path>
              </svg>
            </div>
            <h3 class="text-lg font-bold mb-2">Phone</h3>
            <p class="text-sm text-gray-600 dark:text-gray-400">+880 1764815056</p>
          </div>
          
          <div class="contact-card group">
            <div class="contact-icon bg-gradient-to-br from-green-500 to-emerald-500">
              <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"></path>
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"></path>
              </svg>
            </div>
            <h3 class="text-lg font-bold mb-2">Location</h3>
            <p class="text-sm text-gray-600 dark:text-gray-400">TB Gate,Mohakhali,Dhaka, Bangladesh</p>
          </div>

         <!-- LinkedIn -->
<div class="contact-card group">
  <div class="contact-icon bg-gradient-to-br from-cyan-500 to-blue-500">
    <svg class="w-6 h-6 text-white" fill="currentColor" viewBox="0 0 24 24">
      <path
        d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
    </svg>
  </div>
  <h3 class="text-lg font-bold mb-2">LinkedIn</h3>
  <a href="https://www.linkedin.com/in/sharif-mezba"
     target="_blank"
     rel="noopener noreferrer"
     class="text-sm text-blue-600 dark:text-blue-400 underline hover:text-blue-800 dark:hover:text-blue-300">
    sharif-mezba
  </a>
</div>

<!-- Location -->
<!-- <div class="contact-card group">
  <div class="contact-icon bg-gradient-to-br from-green-500 to-emerald-500">
    <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
        d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
        d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
    </svg>
  </div>
  <h3 class="text-lg font-bold mb-4">Location</h3>
  <iframe 
    src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3651.1049815915276!2d90.40648857479282!3d23.77927568766818!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3755c709957ed997%3A0x242bac45778271fc!2sMohakhali%20TB%20Gate%20Mosque!5e0!3m2!1sen!2sbd!4v1755202457228!5m2!1sen!2sbd" 
    width="100%" 
    height="250" 
    style="border:0;" 
    allowfullscreen="" 
    loading="lazy" 
    referrerpolicy="no-referrer-when-downgrade">
  </iframe>
</div> -->

        </div>
      </div>
    </section>
  </div>
</template>

<script>
import { ref, onMounted, onBeforeUnmount, inject } from 'vue'
import * as THREE from 'three'

export default {
  name: 'Home',
  setup() {
    const heroCanvas = ref(null)
    const animationId = ref(null)
    const darkMode = inject('darkMode')

    // Modal variables
    const modalOpen = ref(false)
    const modalImage = ref('')
    const modalAlt = ref('')

    // Modal functions
    const openModal = (imageSrc, imageAlt) => {
      modalImage.value = imageSrc
      modalAlt.value = imageAlt
      modalOpen.value = true
      document.body.style.overflow = 'hidden'
    }

    const closeModal = () => {
      modalOpen.value = false
      modalImage.value = ''
      modalAlt.value = ''
      document.body.style.overflow = 'unset'
    }

    const handleKeydown = (event) => {
      if (event.key === 'Escape' && modalOpen.value) {
        closeModal()
      }
    }

    const skills = {
      digital: [
        "Google Analytics (GA4)", "Meta Ads", "DV360", "Google Ads", "TikTok Ads", 
        "Adobe Audience Manager", "Power BI", "Looker Studio", "Shopify Analytics", "SEMRush"
      ],
      technical: [
        "NodeJS", "JavaScript", "HTML/CSS", "Flutter", "Python", "TensorFlow", 
        "Git", "N8N", "Adobe Illustrator", "Canva"
      ],
      certifications: [
        "Media Buying Professional - Meta Blueprint",
        "Google Video Ads Certification",
        "TikTok Ads Expert - Digital Ad Expert by Aleph",
        "IELTS Score: Overall 8"
      ]
    }

    const achievements = [
      {
        title: "Gold - Best Use of Mobile",
        event: "Festival of Media Global 2025",
        year: "2025"
      },
      {
        title: "Gold - Best Use of Mobile", 
        event: "Festival of Media APEC 2025",
        year: "2025"
      },
      {
        title: "Original Media Innovation of the Year",
        event: "Mindshare Global Awards 2025",
        year: "2025"
      },
      {
        title: "GOLD - Most Effective Use of Media Campaign",
        event: "Commward 2024",
        year: "2024"
      },
      {
        title: "SILVER - Best Use of Mobile Category",
        event: "Digital Marketing Awards (DMA) 2024",
        year: "2024"
      },
      {
        title: "Best Creative Talent of the Year (Science)",
        event: "Government of Bangladesh",
        year: "2016"
      }
    ]

    const initAdvancedThreeJS = () => {
      if (!heroCanvas.value) return

      const scene = new THREE.Scene()
      const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000)
      const renderer = new THREE.WebGLRenderer({ 
        canvas: heroCanvas.value,
        alpha: true,
        antialias: true
      })
      
      renderer.setSize(window.innerWidth, window.innerHeight)
      renderer.setClearColor(0x000000, 0)

      // Enhanced particle system
      const particleCount = 200
      const particles = new THREE.BufferGeometry()
      const positions = new Float32Array(particleCount * 3)
      const colors = new Float32Array(particleCount * 3)
      const sizes = new Float32Array(particleCount)

      // Color palettes for light and dark modes
      const lightColors = [
        new THREE.Color(0x3B82F6), // Blue
        new THREE.Color(0x8B5CF6), // Purple
        new THREE.Color(0xF59E0B), // Yellow
        new THREE.Color(0xEF4444), // Red
        new THREE.Color(0x10B981), // Green
        new THREE.Color(0xF97316), // Orange
      ]

      const darkColors = [
        new THREE.Color(0x60A5FA), // Light Blue
        new THREE.Color(0xA78BFA), // Light Purple
        new THREE.Color(0xFBBF24), // Light Yellow
        new THREE.Color(0xF87171), // Light Red
        new THREE.Color(0x34D399), // Light Green
        new THREE.Color(0xFB923C), // Light Orange
      ]

      const currentColors = darkMode.value ? darkColors : lightColors

      for (let i = 0; i < particleCount; i++) {
        // Positions
        positions[i * 3] = (Math.random() - 0.5) * 20
        positions[i * 3 + 1] = (Math.random() - 0.5) * 20
        positions[i * 3 + 2] = (Math.random() - 0.5) * 20

        // Colors
        const color = currentColors[Math.floor(Math.random() * currentColors.length)]
        colors[i * 3] = color.r
        colors[i * 3 + 1] = color.g
        colors[i * 3 + 2] = color.b

        // Sizes
        sizes[i] = Math.random() * 4 + 1
      }

      particles.setAttribute('position', new THREE.BufferAttribute(positions, 3))
      particles.setAttribute('color', new THREE.BufferAttribute(colors, 3))
      particles.setAttribute('size', new THREE.BufferAttribute(sizes, 1))

      const particleMaterial = new THREE.ShaderMaterial({
        uniforms: {
          time: { value: 0 }
        },
        vertexShader: `
          attribute float size;
          attribute vec3 color;
          varying vec3 vColor;
          uniform float time;
          
          void main() {
            vColor = color;
            vec3 pos = position;
            
            // Add wave motion
            pos.y += sin(time * 0.001 + position.x * 0.1) * 2.0;
            pos.x += cos(time * 0.001 + position.z * 0.1) * 1.0;
            
            vec4 mvPosition = modelViewMatrix * vec4(pos, 1.0);
            gl_PointSize = size * (300.0 / -mvPosition.z);
            gl_Position = projectionMatrix * mvPosition;
          }
        `,
        fragmentShader: `
          varying vec3 vColor;
          
          void main() {
            float distanceToCenter = distance(gl_PointCoord, vec2(0.5));
            float alpha = 1.0 - smoothstep(0.0, 0.5, distanceToCenter);
            gl_FragColor = vec4(vColor, alpha * 0.8);
          }
        `,
        transparent: true,
        vertexColors: true,
        blending: THREE.AdditiveBlending
      })

      const particleSystem = new THREE.Points(particles, particleMaterial)
      scene.add(particleSystem)

      // Connection lines with dynamic behavior
      const connectionMaterial = new THREE.ShaderMaterial({
        uniforms: {
          time: { value: 0 },
          color1: { value: new THREE.Color(darkMode.value ? 0x60A5FA : 0x3B82F6) },
          color2: { value: new THREE.Color(darkMode.value ? 0xA78BFA : 0x8B5CF6) }
        },
        vertexShader: `
          uniform float time;
          varying float vAlpha;
          
          void main() {
            vAlpha = sin(time * 0.002 + position.x * 0.1) * 0.5 + 0.5;
            gl_Position = projectionMatrix * modelViewMatrix * vec4(position, 1.0);
          }
        `,
        fragmentShader: `
          uniform vec3 color1;
          uniform vec3 color2;
          varying float vAlpha;
          
          void main() {
            vec3 color = mix(color1, color2, vAlpha);
            gl_FragColor = vec4(color, vAlpha * 0.3);
          }
        `,
        transparent: true,
        blending: THREE.AdditiveBlending
      })

      // Create dynamic connections
      const connections = []
      for (let i = 0; i < 80; i++) {
        const points = []
        const p1 = new THREE.Vector3(
          (Math.random() - 0.5) * 15,
          (Math.random() - 0.5) * 15,
          (Math.random() - 0.5) * 15
        )
        const p2 = new THREE.Vector3(
          (Math.random() - 0.5) * 15,
          (Math.random() - 0.5) * 15,
          (Math.random() - 0.5) * 15
        )
        
        points.push(p1, p2)
        
        const geometry = new THREE.BufferGeometry().setFromPoints(points)
        const line = new THREE.Line(geometry, connectionMaterial)
        connections.push(line)
        scene.add(line)
      }

      // Floating geometric shapes
      const shapes = []
      const shapeGeometries = [
        new THREE.OctahedronGeometry(0.3),
        new THREE.TetrahedronGeometry(0.4),
        new THREE.IcosahedronGeometry(0.25),
        new THREE.DodecahedronGeometry(0.3)
      ]

      for (let i = 0; i < 15; i++) {
        const geometry = shapeGeometries[Math.floor(Math.random() * shapeGeometries.length)]
        const material = new THREE.MeshBasicMaterial({
          color: currentColors[Math.floor(Math.random() * currentColors.length)],
          transparent: true,
          opacity: 0.4,
          wireframe: Math.random() > 0.5
        })
        
        const shape = new THREE.Mesh(geometry, material)
        shape.position.set(
          (Math.random() - 0.5) * 18,
          (Math.random() - 0.5) * 18,
          (Math.random() - 0.5) * 18
        )
        shape.rotation.set(
          Math.random() * Math.PI,
          Math.random() * Math.PI,
          Math.random() * Math.PI
        )
        
        shapes.push(shape)
        scene.add(shape)
      }

      camera.position.z = 8

      let mouseX = 0
      let mouseY = 0

      const handleMouseMove = (event) => {
        mouseX = (event.clientX / window.innerWidth) * 2 - 1
        mouseY = -(event.clientY / window.innerHeight) * 2 + 1
      }

      window.addEventListener('mousemove', handleMouseMove)

      const animate = () => {
        animationId.value = requestAnimationFrame(animate)
        
        const time = Date.now()

        // Update particle system
        particleMaterial.uniforms.time.value = time
        connectionMaterial.uniforms.time.value = time

        // Rotate particle system
        particleSystem.rotation.x += 0.0005
        particleSystem.rotation.y += 0.001

        // Animate shapes
        shapes.forEach((shape, index) => {
          shape.rotation.x += 0.01 + index * 0.001
          shape.rotation.y += 0.008 + index * 0.0008
          shape.position.y += Math.sin(time * 0.001 + index) * 0.002
        })

        // Mouse interaction
        camera.position.x += (mouseX * 2 - camera.position.x) * 0.02
        camera.position.y += (mouseY * 2 - camera.position.y) * 0.02

        // Gentle camera movement
        camera.position.x += Math.sin(time * 0.0003) * 0.3
        camera.position.y += Math.cos(time * 0.0002) * 0.2

        renderer.render(scene, camera)
      }

      animate()

      const handleResize = () => {
        camera.aspect = window.innerWidth / window.innerHeight
        camera.updateProjectionMatrix()
        renderer.setSize(window.innerWidth, window.innerHeight)
      }

      window.addEventListener('resize', handleResize)

      return () => {
        window.removeEventListener('resize', handleResize)
        window.removeEventListener('mousemove', handleMouseMove)
        if (animationId.value) {
          cancelAnimationFrame(animationId.value)
        }
        renderer.dispose()
      }
    }

    const setupSmoothScrolling = () => {
      document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
          e.preventDefault()
          const target = document.querySelector(this.getAttribute('href'))
          if (target) {
            target.scrollIntoView({
              behavior: 'smooth',
              block: 'start'
            })
          }
        })
      })
    }

    onMounted(() => {
      // Add keyboard listener for modal
      window.addEventListener('keydown', handleKeydown)
      
      const cleanup = initAdvancedThreeJS()
      setupSmoothScrolling()
    })

    onBeforeUnmount(() => {
      window.removeEventListener('keydown', handleKeydown)
      if (animationId.value) {
        cancelAnimationFrame(animationId.value)
      }
    })

    return {
      heroCanvas,
      skills,
      achievements,
      modalOpen,
      modalImage,
      modalAlt,
      openModal,
      closeModal
    }
  }
}
</script>

<style scoped>
/* Enhanced animations */
@keyframes gradient-x {
  0%, 100% {
    background-size: 200% 200%;
    background-position: left center;
  }
  50% {
    background-size: 200% 200%;
    background-position: right center;
  }
}

@keyframes pulse-glow {
  0%, 100% {
    box-shadow: 0 0 30px rgba(59, 130, 246, 0.3);
  }
  50% {
    box-shadow: 0 0 50px rgba(139, 92, 246, 0.5);
  }
}

@keyframes float-slow {
  0%, 100% { transform: translateY(0px) rotate(0deg); }
  50% { transform: translateY(-20px) rotate(180deg); }
}

@keyframes float-medium {
  0%, 100% { transform: translateY(0px) rotate(0deg); }
  50% { transform: translateY(-15px) rotate(90deg); }
}

@keyframes float-fast {
  0%, 100% { transform: translateY(0px) rotate(0deg); }
  50% { transform: translateY(-25px) rotate(270deg); }
}

@keyframes scroll {
  0% { transform: translateY(0); opacity: 1; }
  100% { transform: translateY(10px); opacity: 0; }
}

.animate-gradient-x {
  animation: gradient-x 3s ease infinite;
}

.animate-pulse-glow {
  animation: pulse-glow 3s ease-in-out infinite;
}

.animate-float-slow {
  animation: float-slow 6s ease-in-out infinite;
}

.animate-float-medium {
  animation: float-medium 4s ease-in-out infinite;
}

.animate-float-fast {
  animation: float-fast 3s ease-in-out infinite;
}

.animate-scroll {
  animation: scroll 2s infinite;
}

/* Component styles */
.section-title {
  @apply text-4xl xl:text-5xl font-bold text-center mb-16 bg-gradient-to-r from-blue-600 via-purple-600 to-pink-600 bg-clip-text text-transparent;
}

.skill-badge {
  @apply px-4 py-2 rounded-full font-semibold text-sm shadow-lg hover:shadow-xl transition-all duration-300 transform hover:scale-105;
}

.btn-primary {
  @apply bg-gradient-to-r from-blue-500 via-purple-500 to-pink-500 hover:from-pink-500 hover:via-purple-500 hover:to-blue-500 px-8 py-3 rounded-full font-bold text-white hover:shadow-2xl hover:shadow-purple-500/25 transition-all duration-300 transform hover:scale-105 text-center;
}

.btn-secondary {
  @apply border-2 border-gray-300 dark:border-gray-600 hover:border-purple-500 dark:hover:border-purple-400 px-8 py-3 rounded-full font-semibold hover:bg-gradient-to-r hover:from-blue-50 hover:to-purple-50 dark:hover:from-gray-800 dark:hover:to-purple-900 transition-all duration-300 transform hover:scale-105 text-gray-700 dark:text-white text-center;
}

.btn-achievement {
  @apply bg-gradient-to-r from-yellow-500 via-orange-500 to-red-500 hover:from-red-500 hover:via-orange-500 hover:to-yellow-500 px-8 py-4 rounded-full font-bold text-white text-lg hover:shadow-2xl hover:shadow-orange-500/25 transition-all duration-300 transform hover:scale-105;
}

.badge {
  @apply px-4 py-2 rounded-full text-sm font-medium;
}

.stats-card {
  @apply bg-white dark:bg-gray-800 p-8 rounded-3xl border border-gray-200 dark:border-gray-700 shadow-xl hover:shadow-2xl transition-all duration-300 backdrop-blur-sm;
}

.stat-item {
  @apply flex justify-between items-center;
}

.experience-card {
  @apply bg-white dark:bg-gray-800 p-8 rounded-3xl border border-gray-200 dark:border-gray-700 shadow-xl hover:shadow-2xl hover:border-purple-400 dark:hover:border-purple-500/50 transition-all duration-300 backdrop-blur-sm;
}

.skill-card {
  @apply bg-white dark:bg-gray-800 p-8 rounded-3xl border border-gray-200 dark:border-gray-700 shadow-xl hover:shadow-2xl transition-all duration-300 backdrop-blur-sm;
}

.skill-progress-item {
  @apply flex items-center justify-between;
}

.skill-progress-bar {
  @apply w-20 h-2 rounded-full bg-gray-200 dark:bg-gray-700 overflow-hidden;
}

.skill-progress-fill {
  @apply h-full rounded-full transition-all duration-1000;
}

.skill-tag {
  @apply px-3 py-1 rounded-full text-xs font-semibold text-white shadow-lg hover:shadow-xl transition-all duration-300 transform hover:scale-105;
}

.certification-item {
  @apply p-4 rounded-xl bg-gradient-to-r from-gray-50 to-gray-100 dark:from-gray-700/50 dark:to-gray-600/50 border border-gray-200 dark:border-gray-600 hover:border-green-400 dark:hover:border-green-500 transition-all duration-300;
}

.gallery-header {
  @apply bg-white dark:bg-gray-800 p-8 rounded-3xl border border-gray-200 dark:border-gray-700 shadow-xl backdrop-blur-sm;
}

.gallery-placeholder {
  @apply aspect-square rounded-xl border-2 border-dashed border-gray-300 dark:border-gray-600 bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-700/50 dark:to-gray-600/50 flex items-center justify-center hover:border-yellow-400 dark:hover:border-yellow-500 transition-all duration-300 transform hover:scale-105;
}

.gallery-image-container {
  @apply aspect-square rounded-xl overflow-hidden bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-700/50 dark:to-gray-600/50 relative cursor-pointer transition-all duration-300 transform hover:scale-105 shadow-lg hover:shadow-2xl;
}

.gallery-image {
  @apply w-full h-full object-cover transition-all duration-500 group-hover:scale-110;
}

.gallery-overlay {
  @apply absolute inset-0 bg-black/50 flex flex-col items-center justify-center opacity-0 group-hover:opacity-100 transition-all duration-300 backdrop-blur-sm;
}

.achievement-card {
  @apply bg-white dark:bg-gray-800 p-8 rounded-3xl border border-gray-200 dark:border-gray-700 shadow-xl hover:shadow-2xl hover:border-yellow-400 dark:hover:border-yellow-500/50 transition-all duration-300 transform hover:scale-105 backdrop-blur-sm;
}

.achievement-year {
  @apply px-3 py-1 rounded-full text-xs font-bold bg-gradient-to-r from-yellow-100 to-orange-100 dark:from-yellow-500/20 dark:to-orange-500/20 text-yellow-700 dark:text-yellow-300 border border-yellow-200 dark:border-yellow-500/30;
}

.contact-card {
  @apply bg-white dark:bg-gray-800 p-8 rounded-3xl border border-gray-200 dark:border-gray-700 shadow-xl hover:shadow-2xl transition-all duration-300 transform hover:scale-105 backdrop-blur-sm;
}

.contact-icon {
  @apply w-16 h-16 rounded-2xl flex items-center justify-center mx-auto mb-6 shadow-lg group-hover:shadow-xl group-hover:scale-110 transition-all duration-300;
}

/* Responsive improvements */
@media (max-width: 640px) {
  .section-title {
    @apply text-3xl mb-12;
  }
  
  .skill-badge {
    @apply text-xs px-3 py-1.5;
  }
  
  .btn-primary, .btn-secondary {
    @apply px-6 py-2.5 text-sm;
  }
}

/* Custom scrollbar */
::-webkit-scrollbar {
  width: 8px;
}

::-webkit-scrollbar-track {
  background: linear-gradient(to bottom, #f1f5f9, #e2e8f0);
}

.dark ::-webkit-scrollbar-track {
  background: linear-gradient(to bottom, #1e293b, #0f172a);
}

::-webkit-scrollbar-thumb {
  background: linear-gradient(to bottom, #3b82f6, #8b5cf6);
  border-radius: 4px;
}

::-webkit-scrollbar-thumb:hover {
  background: linear-gradient(to bottom, #2563eb, #7c3aed);
}

html {
  scroll-behavior: smooth;
}
</style>