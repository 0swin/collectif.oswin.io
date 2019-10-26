<template>
  <div class="p-2">
    <div class="flex flex-col md:flex-row p-4 bg-white rounded-lg shadow-xl">
      <div class="flex-grow-0 flex-shrink-0 mr-4">
        <img
          class="w-20 lg:w-32 lg:m-2 rounded-full shadow-inner mx-auto"
          :src="profile.photo"
          :alt="'Picture of ' + profile.name"
        />
      </div>
      <div class="flex-1 text-gray-900 text-center md:text-left">
        <h1 class="text-2xl">{{ profile.name }}</h1>
        <p class="text-sm text-gray-700 uppercase tracking-wide">{{ profile.job }}</p>
        <hr class="my-2 mr-4" />
        <ul>
          <li class="mb-1" v-for="skill in profile.skills" :key="skill.id">
            <div class="inline-block h-5 w-5 rounded-full text-blue-500 align-text-bottom">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                stroke="currentColor"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
                class="feather feather-check-circle"
                viewBox="0 0 24 24"
              >
                <path d="M22 11v1a10 10 0 11-6-9" />
                <path d="M22 4L12 14l-3-3" />
              </svg>
            </div>
            {{ skill }}
          </li>
        </ul>
        <hr class="my-2 mx-6" />
        <ul>
          <li class="inline mr-4" v-for="link in profile.links" :key="link.id">
            <a
              class="text-sm uppercase tracking-wide text-blue-600 underline"
              :href="link.url"
            >{{ link.text }}</a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    profile: Object
  }
};
</script>

<style>
</style>