<template>
  <section class="mx-auto max-w-3xl px-4 py-12">
    <h1 class="font-display text-3xl font-bold">Contact</h1>
    <p class="mt-2 text-gray-600">Tell us about your project or event and we’ll get back to you within 24 hours.</p>

    <form class="mt-8 grid gap-4">
      <div class="grid gap-4 md:grid-cols-2">
        <div>
          <label class="block text-sm font-medium text-gray-700">Name</label>
          <input type="text" class="mt-1 w-full rounded-md border border-gray-300 px-3 py-2 focus:border-brand focus:outline-none" placeholder="Your name" />
        </div>
        <div>
          <label class="block text-sm font-medium text-gray-700">Email</label>
          <input type="email" class="mt-1 w-full rounded-md border border-gray-300 px-3 py-2 focus:border-brand focus:outline-none" placeholder="you@example.com" />
        </div>
      </div>
      <div>
        <label class="block text-sm font-medium text-gray-700">Service</label>
        <select class="mt-1 w-full rounded-md border border-gray-300 px-3 py-2 focus:border-brand focus:outline-none">
          <option>Wedding</option>
          <option>Portrait</option>
          <option>Commercial</option>
          <option>Event</option>
        </select>
      </div>
      <div>
        <label class="block text-sm font-medium text-gray-700">Message</label>
        <textarea rows="5" class="mt-1 w-full rounded-md border border-gray-300 px-3 py-2 focus:border-brand focus:outline-none" placeholder="Tell us about your vision..."></textarea>
      </div>
      <button type="button" class="mt-2 w-full rounded-md bg-brand px-6 py-3 text-white shadow hover:bg-brand-dark md:w-auto">Send message</button>
    </form>
  </section>
</template>