<template>
  <footer class="bg-gray-950 text-white py-12 sm:py-16 border-t border-gray-800/50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Main Footer Content -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-5 gap-8 mb-8">
        <!-- Company Info -->
        <div class="lg:col-span-2 animate-fade-in-up">
          <div class="flex items-center mb-4 group">
            <div class="w-8 h-8 bg-gradient-to-r from-blue-500 to-purple-600 rounded-lg flex items-center justify-center transition-transform duration-300 group-hover:scale-110 group-hover:rotate-12">
              <span class="text-white font-bold text-sm">S</span>
            </div>
            <span class="ml-2 text-xl font-bold group-hover:text-blue-400 transition-colors duration-300">SaaSify</span>
          </div>
          <p class="text-gray-400 mb-6 max-w-md group-hover:text-gray-300 transition-colors duration-300">
            The complete platform for modern SaaS applications. Build faster, scale effortlessly, and focus on what matters most.
          </p>
          <div class="flex space-x-4">
            <a href="#" class="text-gray-400 hover:text-white transition-all duration-300 transform hover:scale-110 hover:-translate-y-1" aria-label="Twitter">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                <path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"/>
              </svg>
            </a>
            <a href="#" class="text-gray-400 hover:text-white transition-all duration-300 transform hover:scale-110 hover:-translate-y-1" aria-label="LinkedIn">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
              </svg>
            </a>
            <a href="#" class="text-gray-400 hover:text-white transition-all duration-300 transform hover:scale-110 hover:-translate-y-1" aria-label="GitHub">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
              </svg>
            </a>
            <a href="#" class="text-gray-400 hover:text-white transition-all duration-300 transform hover:scale-110 hover:-translate-y-1" aria-label="Discord">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                <path d="M20.317 4.3698a19.7913 19.7913 0 00-4.8851-1.5152.0741.0741 0 00-.0785.0371c-.211.3753-.4447.8648-.6083 1.2495-1.8447-.2762-3.68-.2762-5.4868 0-.1636-.3933-.4058-.8742-.6177-1.2495a.077.077 0 00-.0785-.037 19.7363 19.7363 0 00-4.8852 1.515.0699.0699 0 00-.0321.0277C.5334 9.0458-.319 13.5799.0992 18.0578a.0824.0824 0 00.0312.0561c2.0528 1.5076 4.0413 2.4228 5.9929 3.0294a.0777.0777 0 00.0842-.0276c.4616-.6304.8731-1.2952 1.226-1.9942a.076.076 0 00-.0416-.1057c-.6528-.2476-1.2743-.5495-1.8722-.8923a.077.077 0 01-.0076-.1277c.1258-.0943.2517-.1923.3718-.2914a.0743.0743 0 01.0776-.0105c3.9278 1.7933 8.18 1.7933 12.0614 0a.0739.0739 0 01.0785.0095c.1202.099.246.1981.3728.2924a.077.077 0 01-.0066.1276 12.2986 12.2986 0 01-1.873.8914.0766.0766 0 00-.0407.1067c.3604.698.7719 1.3628 1.225 1.9932a.076.076 0 00.0842.0286c1.961-.6067 3.9495-1.5219 6.0023-3.0294a.077.077 0 00.0313-.0552c.5004-5.177-.8382-9.6739-3.5485-13.6604a.061.061 0 00-.0312-.0286zM8.02 15.3312c-1.1825 0-2.1569-1.0857-2.1569-2.419 0-1.3332.9555-2.4189 2.157-2.4189 1.2108 0 2.1757 1.0952 2.1568 2.419 0 1.3332-.9555 2.4189-2.1569 2.4189zm7.9748 0c-1.1825 0-2.1569-1.0857-2.1569-2.419 0-1.3332.9554-2.4189 2.1569-2.4189 1.2108 0 2.1757 1.0952 2.1568 2.419 0 1.3332-.9555 2.4189-2.1568 2.4189Z"/>
              </svg>
            </a>
          </div>
        </div>
        
        <!-- Product Links -->
        <div class="animate-fade-in-up" style="animation-delay: 0.1s;">
          <h4 class="text-lg font-semibold mb-4 text-white">Product</h4>
          <ul class="space-y-3">
            <li><a href="#features" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Features</a></li>
            <li><a href="#pricing" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Pricing</a></li>
            <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">API Documentation</a></li>
            <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Integrations</a></li>
            <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Changelog</a></li>
            <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Roadmap</a></li>
          </ul>
        </div>
        
        <!-- Company Links -->
        <div class="animate-fade-in-up" style="animation-delay: 0.2s;">
          <h4 class="text-lg font-semibold mb-4 text-white">Company</h4>
          <ul class="space-y-3">
            <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">About Us</a></li>
            <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Blog</a></li>
            <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Careers</a></li>
            <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Press Kit</a></li>
            <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Partners</a></li>
            <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Contact</a></li>
          </ul>
        </div>
        
        <!-- Support & Legal Links -->
        <div class="animate-fade-in-up" style="animation-delay: 0.3s;">
          <h4 class="text-lg font-semibold mb-4 text-white">Support & Legal</h4>
          <ul class="space-y-3">
            <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Help Center</a></li>
            <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Community</a></li>
            <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Status Page</a></li>
            <li><a href="#privacy" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Privacy Policy</a></li>
            <li><a href="#terms" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Terms of Service</a></li>
            <li><a href="#cookies" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Cookie Policy</a></li>
          </ul>
        </div>
      </div>
      
      <!-- Bottom Footer -->
      <div class="border-t border-gray-800 pt-8">
        <div class="flex flex-col md:flex-row justify-between items-center space-y-4 md:space-y-0 animate-fade-in-up" style="animation-delay: 0.4s;">
          <!-- Copyright -->
          <div class="text-gray-400 text-sm">
            © {{ new Date().getFullYear() }} SaaSify. All rights reserved.
          </div>
          
          <!-- Legal Links -->
          <div class="flex flex-wrap justify-center md:justify-end space-x-6 text-sm">
            <a href="#privacy" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy</a>
            <a href="#terms" class="text-gray-400 hover:text-white transition-colors duration-300">Terms</a>
            <a href="#cookies" class="text-gray-400 hover:text-white transition-colors duration-300">Cookies</a>
            <a href="#security" class="text-gray-400 hover:text-white transition-colors duration-300">Security</a>
            <a href="#accessibility" class="text-gray-400 hover:text-white transition-colors duration-300">Accessibility</a>
          </div>
          
          <!-- Language/Region Selector -->
          <div class="flex items-center space-x-2 text-sm">
            <svg class="w-4 h-4 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3.055 11H5a2 2 0 012 2v1a2 2 0 002 2 2 2 0 012 2v2.945M8 3.935V5.5A2.5 2.5 0 0010.5 8h.5a2 2 0 012 2 2 2 0 104 0 2 2 0 012-2h1.064M15 20.488V18a2 2 0 012-2h3.064M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path>
            </svg>
            <select class="bg-transparent text-gray-400 hover:text-white transition-colors duration-300 focus:outline-none cursor-pointer">
              <option value="en">English (US)</option>
              <option value="es">Español</option>
              <option value="fr">Français</option>
              <option value="de">Deutsch</option>
              <option value="ja">日本語</option>
            </select>
          </div>
        </div>
        
        <!-- Trust Badges -->
        <div class="mt-8 pt-6 border-t border-gray-800/50">
          <div class="flex flex-wrap justify-center items-center space-x-8 space-y-4 md:space-y-0 animate-fade-in-up" style="animation-delay: 0.5s;">
            <div class="flex items-center space-x-2 text-gray-400 text-sm">
              <svg class="w-5 h-5 text-green-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"></path>
              </svg>
              <span>SOC 2 Compliant</span>
            </div>
            <div class="flex items-center space-x-2 text-gray-400 text-sm">
              <svg class="w-5 h-5 text-green-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z"></path>
              </svg>
              <span>GDPR Ready</span>
            </div>
            <div class="flex items-center space-x-2 text-gray-400 text-sm">
              <svg class="w-5 h-5 text-green-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path>
              </svg>
              <span>99.9% Uptime</span>
            </div>
            <div class="flex items-center space-x-2 text-gray-400 text-sm">
              <svg class="w-5 h-5 text-green-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3.055 11H5a2 2 0 012 2v1a2 2 0 002 2 2 2 0 012 2v2.945M8 3.935V5.5A2.5 2.5 0 0010.5 8h.5a2 2 0 012 2 2 2 0 104 0 2 2 0 012-2h1.064M15 20.488V18a2 2 0 012-2h3.064M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path>
              </svg>
              <span>Global CDN</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template> 