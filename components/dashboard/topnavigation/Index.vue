<template>
  <header class="h-16 md:h-20 shadow border-b-2 border-blue-200 bg-white items-center relative z-10">
    <div
      class="
        flex flex-center flex-col
        h-full
        justify-center
        mx-auto
        relative
        px-3
        text-white
        z-10
      "
    >
      <div
        class="
          flex
          items-center
          pl-1
          relative
          w-full
          sm:ml-0 sm:pr-2
          lg:max-w-68
        "
      >
        <div class="flex group h-full items-center relative w-16">
          <button
            type="button"
            aria-expanded="false"
            aria-label="Toggle sidenav"
            class="text-4xl text-blueBackground focus:outline-none"
            @click="toggle"
          >
            <svg
              viewBox="0 0 16 16" 
              class="text-blueBackground fill-current w-8 h-8 md:w-10 md:h-10 ml-2"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path d="m0 0h16v16h-16z" fill="none"/><path d="m1 9h14v-2h-14zm0 5h14v-2h-14zm0-12v2h14v-2z"/>
            </svg>
          </button>
        </div>
        <div
          class="
            flex
            items-center
            justify-end
            ml-5
            mr-0
            p-1
            relative
            text-gray-700
            w-full
            sm:mr-0 sm:right-auto
          "
        >
          <a href="#" class="block pr-5 relative">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-6 w-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9"
              />
            </svg>
          </a>
          <a href="#" class="block relative">
            <img
              alt="Stone Cold Steve Austin"
              src="/images/1.jpg"
              class="h-10 object-cover rounded-full w-10"
            />
          </a>
          <select class="ml-2 text-gray-600 font-semibold">
            <option class="text-gray-600 font-semibold" value="">Jane doe</option>
            <option class="text-gray-600 font-semibold" value="">Profile</option>
            <option class="text-gray-600 font-semibold" value="">Log out</option>
          </select>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'TopNavigation',
  inject: ['toggle'],
}
</script>
