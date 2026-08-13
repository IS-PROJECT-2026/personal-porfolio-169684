<script setup>
import HeroSection from '../components/HeroSection.vue'
import Navbar from '../components/Navbar.vue'
import About from '../components/About.vue'
import Showcase from '../components/Showcase.vue'
import ContactFooter from '../components/ContactFooter.vue'
</script>

<template>
    <div class="bg-[#f7f7f3]">
        <Navbar />

        <main>
            <HeroSection />
            <About />
            <Showcase />
        </main>

        <ContactFooter />
    </div>
</template>