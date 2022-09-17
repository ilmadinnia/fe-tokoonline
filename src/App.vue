<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
import HelloWorld from "./components/HelloWorld.vue";
import { ref } from "vue";
const products = ref([
  { id: 0, name: "Cetaphil Gentle Cleanser" },
  { id: 1, name: "Cetaphil Cleanser Oliy Skin" },
  { id: 2, name: "Cetaphil Gentle Cleanser" },
  { id: 3, name: "Cetaphil Cleanser Oliy Skin" },
  { id: 4, name: "Cetaphil Gentle Cleanser" },
  { id: 5, name: "Cetaphil Cleanser Oliy Skin" },
  { id: 6, name: "Cetaphil Gentle Cleanser" },
  { id: 7, name: "Cetaphil Cleanser Oliy Skin" },
  { id: 8, name: "Cetaphil Gentle Cleanser" },
  { id: 9, name: "Cetaphil Cleanser Oliy Skin" },
  { id: 10, name: "Cetaphil Gentle Cleanser" },
]);
</script>
<template>
  <header class="px-52 py-5">
    <img
      alt="Vue logo"
      class="logo"
      src="@/assets/logo.svg"
      width="85"
      height="85"
    />
    <div class="w-6/12">
      <form>
        <div class="flex">
          <label
            for="search-dropdown"
            class="mb-2 text-sm font-medium text-gray-900 sr-only dark:text-gray-300"
            >Your Email</label
          >
          <button
            id="dropdown-button"
            data-dropdown-toggle="dropdown"
            class="flex-shrink-0 z-10 inline-flex items-center py-2.5 px-4 text-sm font-medium text-center text-gray-900 bg-gray-100 border border-gray-300 rounded-l-lg hover:bg-gray-200 focus:ring-4 focus:outline-none focus:ring-gray-100 dark:bg-gray-700 dark:hover:bg-gray-600 dark:focus:ring-gray-700 dark:text-white dark:border-gray-600"
            type="button"
          >
            All categories
            <svg
              aria-hidden="true"
              class="ml-1 w-4 h-4"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                fill-rule="evenodd"
                d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
                clip-rule="evenodd"
              ></path>
            </svg>
          </button>
          <div
            id="dropdown"
            class="hidden z-10 w-44 bg-white rounded divide-y divide-gray-100 shadow dark:bg-gray-700"
            data-popper-reference-hidden=""
            data-popper-escaped=""
            data-popper-placement="bottom"
            style="
              position: absolute;
              inset: 0px auto auto 0px;
              margin: 0px;
              transform: translate(0px, 580px);
            "
          >
            <ul
              class="py-1 text-sm text-gray-700 dark:text-gray-200"
              aria-labelledby="dropdown-button"
            >
              <li>
                <button
                  type="button"
                  class="inline-flex py-2 px-4 w-full hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white"
                >
                  Mockups
                </button>
              </li>
              <li>
                <button
                  type="button"
                  class="inline-flex py-2 px-4 w-full hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white"
                >
                  Templates
                </button>
              </li>
              <li>
                <button
                  type="button"
                  class="inline-flex py-2 px-4 w-full hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white"
                >
                  Design
                </button>
              </li>
              <li>
                <button
                  type="button"
                  class="inline-flex py-2 px-4 w-full hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white"
                >
                  Logos
                </button>
              </li>
            </ul>
          </div>
          <div class="relative w-full">
            <input
              type="search"
              id="search-dropdown"
              class="block p-2.5 w-full z-20 text-sm text-gray-900 bg-gray-50 rounded-r-lg border-l-gray-50 border-l-2 border border-gray-300 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-l-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:border-blue-500"
              placeholder="Search Mockups, Logos, Design Templates..."
            />
            <button
              type="submit"
              class="absolute top-0 right-0 p-2.5 text-sm font-medium text-white bg-blue-700 rounded-r-lg border border-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
            >
              <svg
                aria-hidden="true"
                class="w-5 h-5"
                fill="none"
                stroke="currentColor"
                viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"
                ></path>
              </svg>
              <span class="sr-only">Search</span>
            </button>
          </div>
        </div>
      </form>
    </div>
  </header>
  <div class="w-full">
    <nav class="flex justify-left bg-black text-white w-full p-0 m-0">
      <div class="px-52">
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </div>
    </nav>
  </div>
  <div class="px-52 py-10">
    <div class="flex flex-wrap justify-left">
      <div v-for="(product, index) in products" :key="product.id">
        <div
          class="flex-initial w-48 m-2 p-4 bg-white rounded-lg border border-gray-200 shadow-md dark:bg-gray-800 dark:border-gray-700"
        >
          <a href="#">
            <h5
              class="mb-2 text-l font-bold tracking-tight text-gray-900 dark:text-white"
            >
              {{ product.name }}
            </h5>
          </a>
          <img alt="" src="@/assets/product.png" width="174" height="174" />
          <p
            class="mb-3 max-w-fit font-normal text-gray-700 dark:text-gray-400"
          >
            Gentle Cleanser for dry skin Lorem ipsum dolor sit amet
          </p>
          <button
            type="button"
            class="justify-center w-full text-gray-900 bg-white border border-black-300 focus:outline-none hover:bg-gray-100 focus:ring-4 focus:ring-gray-200 font-medium rounded-none text-sm px-5 py-2.5 mr-2 mb-2 dark:bg-gray-800 dark:text-white dark:border-black-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700"
          >
            +Add to cart
          </button>
        </div>
      </div>
    </div>
  </div>
  <RouterView />
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
