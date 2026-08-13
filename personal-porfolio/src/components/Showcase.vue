<script setup>
const props = defineProps({
  loading: {
    type: Boolean,
    default: false,
  },
})

// Mapping your actual GitHub repositories from https://github.com/tyejaedon
const projects = [
  {
    id: 1,
    category: 'Native Mobile',
    title: 'TigerPlayer',
    description: 'A high-fidelity, performance-oriented Android music player built for enthusiasts. Designed with an emphasis on Neural Expressive UI, uncompromising audio quality, and hardware-accelerated visuals.',
    techStack: ['Kotlin', 'Android', 'Glassmorphism'],
    accent: 'bg-[#ff6a3d]',
    link: 'https://github.com/tyejaedon/TigerPlayer'
  },
  {
    id: 2,
    category: 'Full-Stack Web',
    title: 'Waste Connect (ICS-PROJECT-1)',
    description: 'A digital solution designed to bridge the gap between citizens and waste management authorities to combat plastic and toxic waste pollution in Kenya.',
    techStack: ['JavaScript', 'Web Architecture', 'Sustainability'],
    accent: 'bg-[#1ca6a4]',
    link: 'https://github.com/tyejaedon/ICS-PROJECT-1'
  },
  {
    id: 3,
    category: 'Hardware & Systems',
    title: 'IoT Optimization & Data',
    description: 'Custom hardware integration utilizing ESP32 microcontrollers to process environmental data, feeding directly into a remote Node.js optimization framework.',
    techStack: ['ESP32', 'Node.js', 'Machine Learning'],
    accent: 'bg-[#10131a]',
    link: 'https://github.com/tyejaedon'
  }
]
</script>

<template>
  <section
    v-if="loading"
    id="projects"
    aria-label="Project Showcase loading"
    class="relative w-full overflow-hidden bg-[#fefbf5] px-4 py-24 sm:px-6 lg:px-10 lg:py-28"
  >
    <div class="relative z-10 mx-auto w-full max-w-6xl">
      <div class="mb-14 space-y-4 md:mb-16">
        <div class="h-4 w-32 animate-pulse rounded bg-slate-200"></div>
        <div class="h-10 w-full max-w-2xl animate-pulse rounded bg-slate-200"></div>
        <div class="h-5 w-full max-w-3xl animate-pulse rounded bg-slate-200"></div>
      </div>

      <div class="grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-3 lg:gap-7">
        <article
          v-for="index in 3"
          :key="`skeleton-card-${index}`"
          class="rounded-2xl border border-[rgba(16,19,26,0.08)] bg-white/60 p-7"
        >
          <div class="mb-6 h-4 w-24 animate-pulse rounded bg-slate-200"></div>
          <div class="mb-3 h-6 w-2/3 animate-pulse rounded bg-slate-200"></div>
          <div class="mb-2 h-4 w-full animate-pulse rounded bg-slate-200"></div>
          <div class="mb-6 h-4 w-11/12 animate-pulse rounded bg-slate-200"></div>
          <div class="mb-5 h-px w-full bg-slate-200"></div>
          <div class="mb-4 flex gap-2">
            <div class="h-6 w-16 animate-pulse rounded bg-slate-200"></div>
            <div class="h-6 w-20 animate-pulse rounded bg-slate-200"></div>
          </div>
          <div class="h-5 w-32 animate-pulse rounded bg-slate-200"></div>
        </article>
      </div>
    </div>
  </section>

  <section
    v-else
    id="projects"
    aria-label="Project Showcase"
    class="relative w-full overflow-hidden bg-[#fefbf5] px-4 py-24 text-[#10131a] sm:px-6 lg:px-10 lg:py-28"
  >
    <!-- Ambient Background Accent -->
    <div
      aria-hidden="true"
      class="absolute right-[-10%] top-[20%] aspect-square w-[min(45vw,400px)] rounded-full bg-[radial-gradient(circle_at_50%_50%,rgba(255,106,61,0.08),transparent_65%)] pointer-events-none blur-3xl"
    ></div>

    <div class="relative z-10 mx-auto w-full max-w-6xl">
      
      <!-- Section Header -->
      <div class="mb-14 flex flex-col items-start gap-4 md:mb-16 md:items-center md:text-center">
        <span class="text-xs font-bold uppercase tracking-[0.15em] text-[#1ca6a4]">
          Featured Work
        </span>
        <h2 class="text-[clamp(2rem,4vw,3rem)] font-extrabold leading-[1.1] tracking-[-0.03em] text-[#10131a] [font-family:'Avenir_Next','Gill_Sans','Segoe_UI',sans-serif]">
          Open Source & Engineered Solutions.
        </h2>
        <p class="max-w-[54ch] text-[1.05rem] leading-[1.7] text-[#425066]">
          A selection of repositories and applications I have architected, live on GitHub.
        </p>
      </div>

      <!-- Dynamic Project Grid -->
      <div class="grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-3 lg:gap-7">
        <article 
          v-for="project in projects" 
          :key="project.id"
          class="group relative flex flex-col justify-between overflow-hidden rounded-2xl border border-[rgba(16,19,26,0.08)] bg-white/60 p-7 shadow-sm backdrop-blur-md transition-all duration-300 hover:-translate-y-1 hover:shadow-lg hover:border-[rgba(16,19,26,0.15)]"
        >
          <!-- Top Content -->
          <div>
            <div class="mb-5 flex items-center justify-between">
              <span class="text-xs font-bold tracking-wider text-[#516078] uppercase">
                {{ project.category }}
              </span>
              <span :class="['h-2.5 w-2.5 rounded-full', project.accent]"></span>
            </div>
            <h3 class="mb-3 text-xl font-bold leading-tight text-[#10131a]">
              {{ project.title }}
            </h3>
            <p class="mb-8 text-sm leading-[1.6] text-[#425066]">
              {{ project.description }}
            </p>
          </div>

          <!-- Bottom Content: Tech Stack & Action -->
          <div class="mt-auto border-t border-[rgba(16,19,26,0.08)] pt-5">
            <ul class="mb-5 flex flex-wrap gap-2">
              <li 
                v-for="tech in project.techStack" 
                :key="tech"
                class="rounded-md bg-[#f3f4f6] px-2.5 py-1 text-[0.7rem] font-semibold tracking-wide text-[#516078]"
              >
                {{ tech }}
              </li>
            </ul>
            <a 
              :href="project.link" 
              target="_blank"
              rel="noopener noreferrer"
              class="inline-flex items-center gap-2 text-sm font-bold text-[#d64f26] transition-colors duration-200 hover:text-[#ff6a3d]"
            >
              View on GitHub
              <svg class="h-4 w-4 transition-transform duration-200 group-hover:translate-x-1" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M14 5l7 7m0 0l-7 7m7-7H3" />
              </svg>
            </a>
          </div>
        </article>
      </div>
      
      <!-- Global GitHub Link -->
      <div class="mt-12 text-center">
        <a 
          href="https://github.com/tyejaedon" 
          target="_blank"
          rel="noopener noreferrer"
          class="inline-flex items-center gap-3 rounded-full bg-[#10131a] px-6 py-3 text-[0.95rem] font-bold text-white transition-transform hover:-translate-y-0.5 hover:shadow-lg"
        >
          <!-- GitHub Icon -->
          <svg class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24"><path fill-rule="evenodd" d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z" clip-rule="evenodd"/></svg>
          Explore More on @tyejaedon
        </a>
      </div>

    </div>
  </section>
</template>