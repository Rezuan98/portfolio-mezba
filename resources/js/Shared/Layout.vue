<template>
  <div :class="[darkMode ? 'dark' : '', 'min-h-screen transition-colors duration-300']">
    <div class="bg-gradient-to-br from-slate-50 via-blue-50 to-indigo-100 dark:from-gray-900 dark:via-slate-900 dark:to-indigo-950 text-gray-900 dark:text-white min-h-screen">
      <!-- Navigation -->
      <nav class="fixed top-0 left-0 right-0 z-50 bg-white/80 dark:bg-gray-900/80 backdrop-blur-md border-b border-gray-200/50 dark:border-gray-700/50 transition-all duration-300 shadow-lg shadow-blue-500/5">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div class="flex items-center justify-between h-16">
            <!-- Logo -->
            <div class="flex items-center">
              <a href="#hero" class="text-xl sm:text-2xl font-bold bg-gradient-to-r from-yellow-600 via-white-600 to-purple-600 bg-clip-text text-transparent hover:from-pink-600 hover:via-purple-600 hover:to-blue-600 transition-all duration-500">
                Sharif Mezba
              </a>
            </div>

            <!-- Desktop Navigation -->
            <div class="hidden md:block">
              <div class="flex items-center space-x-8">
                <a href="#about" class="nav-link">About</a>
                <a href="#experience" class="nav-link">Experience</a>
                <a href="#skills" class="nav-link">Skills</a>
                <a href="#achievements" class="nav-link">Achievements</a>
                <a href="#contact" class="bg-gradient-to-r from-blue-500 via-purple-500 to-pink-500 hover:from-pink-500 hover:via-purple-500 hover:to-blue-500 px-6 py-2.5 rounded-full text-white font-medium hover:shadow-xl hover:shadow-purple-500/25 transition-all duration-300 transform hover:scale-105">
                  Contact
                </a>
                
              </div>
            </div>

            <!-- Mobile menu button -->
            <div class="md:hidden flex items-center space-x-2">
              <button 
                @click="toggleDarkMode"
                class="p-2 rounded-full transition-all duration-300 bg-gradient-to-r from-yellow-400 to-orange-500 dark:from-indigo-500 dark:to-purple-600 text-white hover:shadow-lg"
              >
                <!-- -->
              </button>
              <button @click="toggleMobileMenu" class="text-gray-600 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white transition-colors p-2 rounded-lg hover:bg-gray-100 dark:hover:bg-gray-800">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path v-if="!mobileMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
                  <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
                </svg>
              </button>
            </div>
          </div>

          <!-- Mobile Navigation -->
          <div v-show="mobileMenuOpen" class="md:hidden border-t border-gray-200/50 dark:border-gray-700/50 bg-white/95 dark:bg-gray-900/95 backdrop-blur-md rounded-b-xl mt-1">
            <div class="px-2 pt-2 pb-3 space-y-1">
              <a href="#about" @click="closeMobileMenu" class="mobile-nav-link">About</a>
              <a href="#experience" @click="closeMobileMenu" class="mobile-nav-link">Experience</a>
              <a href="#skills" @click="closeMobileMenu" class="mobile-nav-link">Skills</a>
              <a href="#achievements" @click="closeMobileMenu" class="mobile-nav-link">Achievements</a>
              <a href="#contact" @click="closeMobileMenu" class="mobile-nav-link">Contact</a>
            </div>
          </div>
        </div>
      </nav>

      <!-- Main Content -->
      <main>
        <slot />
      </main>

      <!-- Footer -->
      <footer class="py-12 px-4 border-t border-gray-200/50 dark:border-gray-700/50 bg-gradient-to-r from-blue-50/50 via-purple-50/50 to-pink-50/50 dark:from-gray-900/50 dark:via-slate-900/50 dark:to-indigo-950/50 backdrop-blur-sm">
        <div class="max-w-6xl mx-auto text-center">
          <div class="mb-6">
            <h3 class="text-lg font-semibold bg-gradient-to-r from-blue-600 via-purple-600 to-pink-600 bg-clip-text text-transparent mb-2">
              MD Sharif Hossain
            </h3>
            <p class="text-gray-600 dark:text-gray-400">Award-Winning Digital Marketing Strategist</p>
          </div>
          <!-- <div class="flex justify-center space-x-6 mb-6">
            <a href="#" class="footer-social-link">
              <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
                <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
              </svg>
            </a>
            <a href="#" class="footer-social-link">
              <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
                <path d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z"/>
              </svg>
            </a>
             <a href="#" class="footer-social-link">
              <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
                <path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/>
              </svg>
            </a> 
          </div> -->
          <p class="text-gray-600 dark:text-gray-400 text-sm">
            &copy; 2025 MD Sharif Hossain. All rights reserved. • Building award-winning digital experiences
          </p>
        </div>
      </footer>
    </div>
  </div>
</template>

<script>
import { ref, onMounted, provide, watch } from 'vue'

export default {
  name: 'Layout',
  setup() {
    const mobileMenuOpen = ref(false)
    const darkMode = ref(false)

    const toggleMobileMenu = () => {
      mobileMenuOpen.value = !mobileMenuOpen.value
    }

    const closeMobileMenu = () => {
      mobileMenuOpen.value = false
    }

    const toggleDarkMode = () => {
      darkMode.value = !darkMode.value
      localStorage.setItem('darkMode', darkMode.value)
      
      // Update document class for Tailwind dark mode
      if (darkMode.value) {
        document.documentElement.classList.add('dark')
      } else {
        document.documentElement.classList.remove('dark')
      }
    }

    // Watch for mobile menu clicks outside
    watch(mobileMenuOpen, (newValue) => {
      if (newValue) {
        document.addEventListener('click', handleClickOutside)
      } else {
        document.removeEventListener('click', handleClickOutside)
      }
    })

    const handleClickOutside = (event) => {
      const nav = document.querySelector('nav')
      if (nav && !nav.contains(event.target)) {
        closeMobileMenu()
      }
    }

    onMounted(() => {
      // Load dark mode preference
      const savedDarkMode = localStorage.getItem('darkMode')
      if (savedDarkMode !== null) {
        darkMode.value = savedDarkMode === 'true'
      } else {
        // Default to system preference
        darkMode.value = window.matchMedia('(prefers-color-scheme: dark)').matches
      }
      
      // Apply initial dark mode state
      if (darkMode.value) {
        document.documentElement.classList.add('dark')
      }

      setupScrollEffect()
    })

    const setupScrollEffect = () => {
      // Enhanced scroll effect for navigation
      let lastScrollY = window.scrollY
      const nav = document.querySelector('nav')
      
      window.addEventListener('scroll', () => {
        const currentScrollY = window.scrollY
        
        if (currentScrollY > lastScrollY && currentScrollY > 100) {
          // Scrolling down
          nav.style.transform = 'translateY(-100%)'
          nav.style.opacity = '0.9'
        } else {
          // Scrolling up
          nav.style.transform = 'translateY(0)'
          nav.style.opacity = '1'
        }
        
        // Add blur effect based on scroll
        if (currentScrollY > 50) {
          nav.style.backdropFilter = 'blur(20px)'
          nav.style.background = darkMode.value 
            ? 'rgba(17, 24, 39, 0.85)' 
            : 'rgba(255, 255, 255, 0.85)'
        } else {
          nav.style.backdropFilter = 'blur(8px)'
          nav.style.background = darkMode.value 
            ? 'rgba(17, 24, 39, 0.8)' 
            : 'rgba(255, 255, 255, 0.8)'
        }
        
        lastScrollY = currentScrollY
      })
    }

    // Provide dark mode state to child components
    provide('darkMode', darkMode)

    return {
      mobileMenuOpen,
      darkMode,
      toggleMobileMenu,
      closeMobileMenu,
      toggleDarkMode
    }
  }
}
</script>

<style scoped>
nav {
  transition: transform 0.3s cubic-bezier(0.4, 0, 0.2, 1), 
              opacity 0.3s ease, 
              backdrop-filter 0.3s ease,
              background 0.3s ease;
}

.nav-link {
  @apply text-gray-600 dark:text-gray-300 hover:text-transparent bg-gradient-to-r from-blue-600 to-purple-600 hover:bg-clip-text font-medium transition-all duration-300 relative;
}

.nav-link::after {
  content: '';
  position: absolute;
  width: 0;
  height: 2px;
  bottom: -4px;
  left: 50%;
  background: linear-gradient(to right, #3B82F6, #8B5CF6);
  transition: all 0.3s ease;
  transform: translateX(-50%);
}

.nav-link:hover::after {
  width: 100%;
}

.mobile-nav-link {
  @apply block px-4 py-3 text-gray-600 dark:text-gray-300 hover:text-white hover:bg-gradient-to-r hover:from-blue-500 hover:to-purple-600 transition-all duration-300 rounded-lg mx-2 font-medium;
}

.footer-social-link {
  @apply text-gray-400 hover:text-white hover:bg-gradient-to-r hover:from-blue-500 hover:to-purple-600 p-3 rounded-full transition-all duration-300 transform hover:scale-110 hover:shadow-lg;
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
</style>