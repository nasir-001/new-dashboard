<template>
  <div class="pl-5">
    <router-link :to="to">
      <span class="inline-flex items-center justify-start my-1 p-1 text-white">
        <span
          :class="
            $route.path === to
              ? 'mx-4 font-semibold text-gray-200'
              : 'mx-4 font-semibold text-white'
          "
        >
          {{ title }}
        </span>
      </span>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'SidenavItem',
  props: {
    to: {
      type: String,
      default: '',
    },
    title: {
      type: String,
      default: '',
    },
  },
}
</script>
