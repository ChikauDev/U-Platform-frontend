<template>
  <div class="pt-20 bg-gray-50">
    <div class="flex px-40 pb-20">
      <img src="/image.webp">
      <div>
        <div class="desc p-8 pt-15">
          <div class="title text-3xl mb-3">Let's customize the platform as you want.</div>
          <div class="pb-10">
            <p>U Platform is the service for web developers (laravel & nuxt.js). We can create a system as you want much faster compare with the one we create from scratch.</p>
            <div class="mt-3">
              <div>Compatible languages</div>
              <ul class="pl-5">
                <li>Backend : Laravel</li>
                <li>Frontend : Nuxt.js</li>
                <li>Server : Anything you want</li>
              </ul>
            </div>
          </div>
          <div class="flex space-x-4">
            <nuxt-link to="/signup" class="bg-indigo-600 py-3 px-4 text-lg text-white rounded">
              Get started
            </nuxt-link>
            <button class="bg-white border-2 py-3 px-4 text-lg rounded">Why U Platform ?</button>
            <button class="bg-white border-2 py-3 px-4 text-lg rounded">Github</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>