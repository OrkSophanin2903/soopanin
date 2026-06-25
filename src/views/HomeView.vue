<script setup lang="ts">
import { GlassCard } from "@/components/ui/glass-card";
import { TextType } from "@/components/ui/text-type";
import { ShinyText } from "@/components/ui/shiny-text";
import { Mail } from "lucide-vue-next";
</script>

<template>
  <main class="flex items-center justify-center min-h-screen p-6">
    <GlassCard class="max-w-xl">
      <template #header>
        <p class="text-3xl font-bold">
          <TextType
            :text="['Hi, I am Sophanin.', 'Nice to meet you.']"
            :typing-speed="60"
            :deleting-speed="30"
            :pause-duration="1800"
          />
        </p>
        <h2 class="text-base font-medium tracking-wide">
          <ShinyText :speed="3">Senior Software Developer</ShinyText>
        </h2>
      </template>

      <p class="leading-relaxed">
        I have 6+ years of experience as a software developer, building scalable web applications
        and backend systems. Skilled in JavaScript, TypeScript, PHP, Python, Vue.js, Nuxt.js,
        Laravel, and FastAPI. I've led key projects that improved performance and delivered real
        business value. I'm passionate about solving complex problems, automating and optimizing
        workflows, and writing clear, efficient code. Always learning, and currently exploring
        machine learning and AI-driven development.
      </p>

      <template v-if="false" #footer>
        <a
          href="mailto:sophanin11t@gmail.com"
          class="inline-flex items-center gap-1.5 rounded-md border border-white/20 px-3 py-1.5 text-sm transition-colors hover:bg-white/10"
        >
          <Mail class="size-4" />
          Email
        </a>
        <a
          href="https://github.com/your-username"
          target="_blank"
          rel="noopener noreferrer"
          class="inline-flex items-center gap-1.5 rounded-md border border-white/20 px-3 py-1.5 text-sm transition-colors hover:bg-white/10"
        >
          <!-- Lucide deprecated brand icons; use the GitHub logo as inline SVG. -->
          <svg class="size-4" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
            <path
              d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"
            />
          </svg>
          GitHub
        </a>
        <a
          href="https://linkedin.com/in/your-handle"
          target="_blank"
          rel="noopener noreferrer"
          class="inline-flex items-center gap-1.5 rounded-md border border-white/20 px-3 py-1.5 text-sm transition-colors hover:bg-white/10"
        >
          <!-- Lucide deprecated brand icons; use the LinkedIn logo as inline SVG. -->
          <svg class="size-4" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
            <path
              d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.225 0z"
            />
          </svg>
          LinkedIn
        </a>
      </template>
    </GlassCard>
  </main>
</template>
