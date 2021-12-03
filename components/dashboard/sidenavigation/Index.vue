<template>
  <aside
    :class="state.open
      ? 'scrollbar bg-blueBackground shadow h-full overflow-y-auto lg:block lg:relative lg:w-16 lg:z-auto'
      : 'scrollbar bg-blueBackground shadow h-full overflow-y-auto lg:block lg:relative lg:w-64 lg:z-auto'
    ">
    <div class="pb-32 lg:pb-6">
      <sidenav-header />
      <ul class="mt-6 md:pl-6">
        <li>
          <sidenav-items />
        </li>
      </ul>
    </div>
  </aside>
</template>

<script>
import SidenavItems from './Items.vue'
import SidenavHeader from './Header.vue'

export default {
  name: 'SideNavigation',
  components: { SidenavItems, SidenavHeader },
  inject: ['state'],
  props: {
    mobilePosition: {
      type: String,
      default: '',
    },
  },
  data() {
    return {
      style: {
        left: 'left-0'
      },
    }
  },
}
</script>

<style scoped>
.scrollbar::-webkit-scrollbar {
  width: 0;
  background: transparent; /* hide sidenav scrollbar on Chrome, Opera and other webkit Browsers*/
}
.scrollbar {
  -ms-overflow-style: none;
  scrollbar-width: none; /* hide sidenav scrollbar on Firefox, IE and Edge*/
}
</style>
