<script setup>
const props = defineProps({
  loading: {
    type: Boolean,
    default: false,
  },
})

// The Structured Data Array
const projects = [
  {
    id: 1,
    category: 'Native Mobile',
    title: 'TigerPlayer',
    description: 'A high-fidelity, performance-oriented Android music player built for enthusiasts.',
    techStack: ['Kotlin', 'Android', 'Glassmorphism'],
    accent: 'bg-[#ff6a3d]',
    link: 'https://github.com/tyejaedon/TigerPlayer'
  },
  {
    id: 2,
    category: 'Full-Stack Web',
    title: 'Waste Connect (ICS-PROJECT-1)',
    description: 'A digital solution designed to bridge the gap between citizens and waste management authorities.',
    techStack: ['JavaScript', 'Web Architecture', 'Sustainability'],
    accent: 'bg-[#1ca6a4]',
    link: 'https://github.com/tyejaedon/ICS-PROJECT-1'
  }
]
</script>

<template>
  <section
    id="projects"
    aria-label="Project Showcase"
    class="relative w-full overflow-hidden bg-[#fefbf5] px-4 py-24 text-[#10131a] sm:px-6 lg:px-10 lg:py-28 2xl:px-14"
  >
    <div class="relative z-10 mx-auto w-full max-w-7xl">
      <div class="mb-14 flex flex-col items-start gap-4 md:mb-16 md:items-center md:text-center">
        <span class="text-xs font-bold uppercase tracking-[0.15em] text-[#1ca6a4]">
          Featured Work
        </span>
        <h2 class="text-[clamp(2rem,4vw,3rem)] font-extrabold leading-[1.1] tracking-[-0.03em] text-[#10131a]">
          Open Source & Engineered Solutions.
        </h2>
      </div>


      <div class="grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-3 lg:gap-7">
        <article 
          v-for="project in projects" 
          :key="project.id"
          class="group relative flex flex-col justify-between overflow-hidden rounded-2xl border border-[rgba(16,19,26,0.08)] bg-white/60 p-7 shadow-sm transition-all duration-300 hover:-translate-y-1 hover:shadow-lg"
        >
          <div>
            <div class="mb-5 flex items-center justify-between">
              <span class="text-xs font-bold tracking-wider text-[#516078] uppercase">Native Mobile</span>
            </div>
            <h3 class="mb-3 text-xl font-bold leading-tight text-[#10131a]">
              TigerPlayer (Version 2.0)
            </h3>
            <p class="mb-8 text-sm leading-[1.6] text-[#425066]">
              A high-fidelity, performance-oriented Android music player built for enthusiasts.
            </p>
          </div>
        </article>
      </div>

    </div>
  </section>
</template>