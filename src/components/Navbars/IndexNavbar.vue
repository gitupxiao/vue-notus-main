<template>
  <nav
    class="top-0 fixed z-50 w-full flex flex-wrap items-center justify-between px-2 py-3 navbar-expand-lg bg-white shadow"
  >
    <div
      class="container px-4 mx-auto flex flex-wrap items-center justify-between"
    >
      <div
        class="w-full relative flex justify-between lg:w-auto lg:static lg:block lg:justify-start"
      >
        <router-link to="/">
          <a
            class="text-blueGray-700 text-sm font-bold leading-relaxed inline-block mr-4 py-2 whitespace-nowrap uppercase"
            href="#pablo"
          >
           中国特殊教育
          </a>
        </router-link>
        <button
          class="cursor-pointer text-xl leading-none px-3 py-1 border border-solid border-transparent rounded bg-transparent block lg:hidden outline-none focus:outline-none"
          type="button"
          v-on:click="setNavbarOpen"
        >
          <i class="fas fa-bars"></i>
        </button>
      </div>
      <div
        class="lg:flex flex-grow items-center"
        :class="[navbarOpen ? 'block' : 'hidden']"
        id="example-navbar-warning"
      >
        <ul class="flex flex-col lg:flex-row list-none mr-auto">
          <li class="flex items-center">
            <a
              class="hover:text-blueGray-500 text-blueGray-700 px-3 py-2 flex items-center text-xs uppercase font-bold"
              href="#"
            >
              <i
                class="text-blueGray-400 far fa-file-alt text-lg leading-lg mr-2"
              />
              文章
            </a>
          </li>
        </ul>
        <ul class="flex flex-col lg:flex-row list-none lg:ml-auto">
          <li class="flex items-center">
            <router-link
                to="/admin/dashboard"
                class="text-sm py-2 px-4 font-normal block w-full whitespace-nowrap bg-transparent text-blueGray-700"
            >
              可视化1
            </router-link>
            <router-link
                to="/admin/settings"
                class="text-sm py-2 px-4 font-normal block w-full whitespace-nowrap bg-transparent text-blueGray-700"
            >
              可视化2
            </router-link>
            <router-link
                to="/admin/tables"
                class="text-sm py-2 px-4 font-normal block w-full whitespace-nowrap bg-transparent text-blueGray-700"
            >
              可视化3
            </router-link>
            <router-link
                to="/admin/maps"
                class="text-sm py-2 px-4 font-normal block w-full whitespace-nowrap bg-transparent text-blueGray-700"
            >
              可视化4
            </router-link>
            <div class="h-0 mx-4 my-2 border border-solid border-blueGray-100" />
            <span
                class="text-sm pt-2 pb-0 px-4 font-bold block w-full whitespace-nowrap bg-transparent text-blueGray-400"
            >
            </span>
          </li>
          <li class="flex items-center">
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>

export default {
  data() {
    return {
      navbarOpen: false,
    };
  },
  methods: {
    setNavbarOpen: function () {
      this.navbarOpen = !this.navbarOpen;
    },
  },
  components: {

  },
};
</script>
