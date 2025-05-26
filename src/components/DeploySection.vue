<template>
  <section class="py-16 sm:py-20 lg:py-24 relative">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <div class="animate-fade-in-up">
          <h2 class="text-3xl sm:text-4xl lg:text-5xl font-bold text-white mb-4">
            Deploy in Minutes, Not Hours
          </h2>
          <p class="text-lg sm:text-xl text-gray-400 max-w-3xl mx-auto">
            Get your SaaS application live with our streamlined deployment process.
          </p>
        </div>
      </div>
      
      <div class="max-w-4xl mx-auto">
        <div class="space-y-8">
          <div v-for="(step, index) in deploySteps" :key="step.title" 
               class="flex flex-col md:flex-row items-start md:items-center gap-6 p-6 bg-gray-900/50 rounded-xl border border-gray-800/50 hover:border-gray-700/50 transition-all duration-500 transform hover:scale-105 backdrop-blur-sm group animate-fade-in-up"
               :style="{ animationDelay: `${index * 0.2}s` }">
            <div class="flex-shrink-0">
              <div class="w-12 h-12 bg-gradient-to-r from-blue-500 to-purple-600 rounded-full flex items-center justify-center text-white font-bold text-lg transition-transform duration-300 group-hover:scale-110 group-hover:rotate-12">
                {{ index + 1 }}
              </div>
            </div>
            <div class="flex-grow">
              <h3 class="text-xl font-semibold text-white mb-2 group-hover:text-blue-400 transition-colors duration-300">{{ step.title }}</h3>
              <p class="text-gray-400 mb-4 group-hover:text-gray-300 transition-colors duration-300">{{ step.description }}</p>
              <div class="bg-gray-800/50 rounded-lg p-4 border border-gray-700/50 group-hover:border-gray-600/50 transition-colors duration-300">
                <code class="text-sm text-green-400 font-mono">{{ step.command }}</code>
              </div>
            </div>
            <div class="flex-shrink-0">
              <span class="text-blue-400 text-2xl transition-transform duration-300 group-hover:scale-110">{{ step.icon }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const deploySteps = [
  {
    title: 'Connect Your Repository',
    description: 'Link your GitHub, GitLab, or Bitbucket repository to SaaSify with one click.',
    command: 'git clone https://github.com/your-repo/saas-app.git',
    icon: '🔗'
  },
  {
    title: 'Configure Environment',
    description: 'Set up your environment variables and database connections through our intuitive dashboard.',
    command: 'saasify env:setup --auto-detect',
    icon: '⚙️'
  },
  {
    title: 'Deploy Instantly',
    description: 'Hit deploy and watch your application go live with automatic SSL, CDN, and scaling.',
    command: 'saasify deploy --production',
    icon: '🚀'
  },
  {
    title: 'Monitor & Scale',
    description: 'Track performance, monitor errors, and scale automatically based on traffic demands.',
    command: 'saasify monitor --real-time',
    icon: '��'
  }
]
</script> 