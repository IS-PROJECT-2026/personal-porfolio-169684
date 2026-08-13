<script setup>
    
const handleAction = (action) => {
  console.log(`Action triggered: ${action}`)
}
</script>

<template>
  <section
    id="home"
    aria-label="Hero section"
    class="relative grid min-h-[90svh] place-items-center overflow-hidden bg-[radial-gradient(circle_at_12%_15%,rgba(255,106,61,0.18),transparent_45%),radial-gradient(circle_at_88%_25%,rgba(28,166,164,0.18),transparent_40%),linear-gradient(180deg,#fefbf5_0%,#fbf9f4_50%,#f4f7fb_100%)] px-5 py-20 text-[#10131a] md:px-10 md:py-24"
  >
    <!-- Background Ambient Orbs -->
    <div
      aria-hidden="true"
      class="motion-safe:animate-float-orb absolute left-[-6%] top-[8%] aspect-square w-[min(45vw,380px)] rounded-full bg-[radial-gradient(circle_at_35%_35%,rgba(255,255,255,0),rgba(255,201,182,0.65))] pointer-events-none blur-sm"
    ></div>
    <div
      aria-hidden="true"
      class="motion-safe:animate-float-orb absolute bottom-[-15%] right-[-8%] aspect-square w-[min(48vw,420px)] rounded-full bg-[radial-gradient(circle_at_35%_35%,rgba(255,255,255,0),rgba(179,235,233,0.65))] [animation-delay:1.5s] pointer-events-none blur-sm"
    ></div>

    <div
      class="motion-safe:animate-hero-reveal relative z-10 grid w-full max-w-[1020px] gap-6 text-left"
    >
      <!-- Academic & Status Pill -->
      <div class="flex flex-wrap items-center gap-3">
        <span
          class="inline-flex items-center gap-2 rounded-full border border-[rgba(214,79,38,0.2)] bg-white/80 px-3.5 py-1.5 text-xs font-semibold uppercase tracking-[0.12em] text-[#d64f26] shadow-sm backdrop-blur-md"
        >
          <span class="relative flex h-2 w-2">
            <span class="absolute inline-flex h-full w-full animate-ping rounded-full bg-[#ff6a3d] opacity-75"></span>
            <span class="relative inline-flex h-2 w-2 rounded-full bg-[#d64f26]"></span>
          </span>
          Software Engineer & Informatics Specialist
        </span>
        <span class="hidden text-xs font-medium text-[#516078] sm:inline-block">
          Strathmore University '26
        </span>
      </div>

      <!-- Main Headline -->
      <h1
        class="m-0 max-w-[17ch] text-[clamp(2.4rem,6.8vw,5.2rem)] font-extrabold leading-[1.02] tracking-[-0.035em] text-[#10131a] [font-family:'Avenir_Next','Gill_Sans','Segoe_UI',sans-serif]"
      >
        Engineered systems that bridge 
        <span class="mt-2 block bg-gradient-to-r from-[#d64f26] via-[#e65c33] to-[#1ca6a4] bg-clip-text text-transparent">
          software precision & intuitive UX.
        </span>
      </h1>

      <!-- Subtitle Description -->
      <p class="m-0 max-w-[68ch] text-[clamp(1.05rem,2vw,1.25rem)] leading-[1.7] text-[#425066]">
        I design and deliver resilient end-to-end digital solutions—ranging from native mobile apps 
        and full-stack platforms to intelligent data systems and embedded designs. Driven by clean architecture, refined interaction, and real-world impact.
      </p>

      <!-- Primary Action Buttons -->
      <div class="mt-2 flex flex-wrap items-center gap-4">
        <button
          type="button"
          class="inline-flex items-center gap-2 rounded-full border border-transparent bg-[#ff6a3d] px-6 py-3.5 text-[0.98rem] font-bold tracking-[0.01em] text-white shadow-[0_10px_28px_rgba(214,79,38,0.3)] transition-all duration-200 hover:-translate-y-0.5 hover:bg-[#d64f26] hover:shadow-[0_14px_32px_rgba(214,79,38,0.38)] active:translate-y-0"
          @click="handleAction('projects')"
        >
          <span>Explore Featured Work</span>
          <svg class="h-4 w-4 fill-current" viewBox="0 0 20 20">
            <path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd" />
          </svg>
        </button>

        <button
          type="button"
          class="rounded-full border border-[rgba(16,19,26,0.18)] bg-white/80 px-6 py-3.5 text-[0.98rem] font-bold tracking-[0.01em] text-[#10131a] backdrop-blur-md transition-all duration-200 hover:-translate-y-0.5 hover:border-[rgba(16,19,26,0.3)] hover:bg-white hover:shadow-[0_8px_24px_rgba(16,19,26,0.12)] active:translate-y-0"
          @click="handleAction('contact')"
        >
          Let's Connect
        </button>
      </div>

      <!-- Key Capabilities & Stack Highlights -->
      <div class="mt-6 border-t border-[rgba(16,19,26,0.12)] pt-6">
        <ul
          aria-label="Technical focus highlights"
          class="grid list-none grid-cols-1 gap-4 p-0 sm:grid-cols-3"
        >
          <li class="flex flex-col gap-1 rounded-xl bg-white/40 p-3.5 border border-white/60 shadow-sm backdrop-blur-sm">
            <strong class="text-[clamp(1.35rem,2.5vw,1.75rem)] font-bold leading-none text-[#10131a]">
              Full-Stack & Mobile
            </strong>
            <span class="text-xs font-medium text-[#516078]">
              Vue, React, Kotlin & Jetpack Compose
            </span>
          </li>

          <li class="flex flex-col gap-1 rounded-xl bg-white/40 p-3.5 border border-white/60 shadow-sm backdrop-blur-sm">
            <strong class="text-[clamp(1.35rem,2.5vw,1.75rem)] font-bold leading-none text-[#10131a]">
              Systems & Data
            </strong>
            <span class="text-xs font-medium text-[#516078]">
              ML Optimization & Node.js Backends
            </span>
          </li>

          <li class="flex flex-col gap-1 rounded-xl bg-white/40 p-3.5 border border-white/60 shadow-sm backdrop-blur-sm">
            <strong class="text-[clamp(1.35rem,2.5vw,1.75rem)] font-bold leading-none text-[#10131a]">
              Hardware & IoT
            </strong>
            <span class="text-xs font-medium text-[#516078]">
              ESP32 Microcontrollers & Embedded C
            </span>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<style scoped>
@keyframes hero-reveal {
  from {
    opacity: 0;
    transform: translateY(24px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes float-orb {
  0%,
  100% {
    transform: translateY(0) translateX(0) scale(1);
  }
  50% {
    transform: translateY(-16px) translateX(8px) scale(1.03);
  }
}

.animate-hero-reveal {
  animation: hero-reveal 850ms cubic-bezier(0.16, 1, 0.3, 1) both;
}

.animate-float-orb {
  animation: float-orb 8s ease-in-out infinite;
}
</style>
