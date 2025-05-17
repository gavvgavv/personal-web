<template>
  <div class="bg-[var(--color-background)] text-[var(--color-text)] font-sans min-h-screen">
    <!-- Hero -->
    <section class="flex flex-col items-center justify-center text-center py-24 px-6">
      <h1 class="text-[var(--color-primary)] text-4xl md:text-5xl font-bold mb-4">Hi, I'm a Web Developer 👋</h1>
      <p class="text-lg max-w-xl">
        I love building stuff — especially crafting scalable backend architectures that make products truly reliable.
      </p>
      <div class="mt-6">
        <NuxtLink to="#projects" class="bg-[var(--color-accent)] text-white px-5 py-2 rounded-lg font-bold hover:bg-[var(--color-primary)] transition">
          View My Work
        </NuxtLink>
      </div>
    </section>

    <!-- About -->
    <section class="bg-[var(--color-secondary)] py-16 px-6">
      <div class="max-w-3xl mx-auto text-center">
        <h2 class="text-2xl font-bold mb-4 text-[var(--color-dark-background)]">About Me</h2>
        <p class="text-base text-[var(--color-dark-background)]">
          I'm passionate about web development, especially backend systems design — APIs, databases, distributed systems, and everything in between.
        </p>
      </div>
    </section>

    <!-- Projects -->
    <section id="projects" class="py-20 px-6">
      <div class="max-w-5xl mx-auto">
        <h2 class="text-3xl font-bold text-center mb-10">Projects</h2>
        <div class="grid md:grid-cols-3 gap-8">
          <div v-for="project in projects" :key="project.title" class="bg-white rounded-xl shadow-md p-6 hover:shadow-lg transition">
            <h3 class="text-xl font-bold text-[var(--color-primary)] mb-2">{{ project.title }}</h3>
            <p class="text-base text-gray-700">{{ project.description }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact -->
    <section class="bg-[var(--color-primary)] text-white py-16 px-6 text-center">
      <h2 class="text-2xl font-bold mb-4">Let’s Connect</h2>
      <p class="mb-6">Got a project or just want to say hi? Reach out!</p>
      <a href="mailto:you@example.com" class="underline">you@example.com</a>
    </section>
  </div>
</template>

<script setup>
const projects = [
  {
    title: 'Scalable Order Management System',
    description: 'Built a distributed backend system that handles thousands of daily orders with PostgreSQL and Redis.',
  },
  {
    title: 'Real-time Dashboard API',
    description: 'Developed a real-time stats API for a web dashboard using WebSockets and Redis Pub/Sub.',
  },
  {
    title: 'Modular Authentication System',
    description: 'Created a plug-and-play auth system with multi-role support using AdonisJS and PostgreSQL.',
  },
]
</script>

<style>
body {
  font-family: var(--font-kumbh);
}
</style>
