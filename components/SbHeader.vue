<template>
  <header class="header max-w-screen-2xl ml-auto p-8">
    <nav>
      <ul class="flex justify-end">
        <li class="mr-4" v-for="({ text, link }, i) in links" :key="i">
          <nuxt-link class="text-teal-600 hover:underline" :to="link">
            {{ text }}
          </nuxt-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  data() {
    return {
      links: [
        {
          link: "/",
          text: "Home",
        },
        {
          link: "/collections",
          text: "Collections",
        },
        {
          link: "/blog",
          text: "Blog",
        },
      ],
    };
  },
};
</script>

<style scoped>
.header {
  position: absolute;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 100%;
  z-index: 1;
  display: flex;
  justify-content: flex-end;
}
.header a {
  color: antiquewhite;
}
</style>
