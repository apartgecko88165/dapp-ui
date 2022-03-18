<script lang="ts">
import { defineComponent } from "vue";
import { Icon } from "@iconify/vue";

export default defineComponent({
  props: {
    currentPage: String,
  },
  data() {
    return {
      navItem:
        "flex justify-center bg-slate-500 w-[6rem] h-[6rem] rounded-xl hover:rounded-3xl hover:shadow-xl",
      navIcon: "flex flex-col justify-center",
    };
  },
  components: {
    Icon,
  },
});
</script>

<template>
  <nav class="flex justify-center h-screen bg-gray-600 w-[8rem]">
    <ul class="flex flex-col justify-evenly">
      <li :class="navItem">
        <button :class="navIcon">
          <Icon icon="mdi:account-edit-outline" width="70" />
        </button>
      </li>
      <li :class="navItem">
        <button :class="navIcon">
          <Icon icon="mdi:home-outline" width="70" />
        </button>
      </li>
      <li :class="navItem">
        <button :class="navIcon">
          <Icon icon="mdi:mail-outline" width="70" />
        </button>
      </li>
      <li :class="navItem">
        <button :class="navIcon">
          <Icon icon="mdi:arrow-right-bold-circle-outline" width="70" />
        </button>
      </li>
      <li :class="navItem">
        <button :class="navIcon">
          <Icon icon="mdi:calendar-blank-multiple" width="70" />
        </button>
      </li>
      <li :class="navItem">
        <button :class="navIcon">
          <Icon icon="mdi:cog-outline" width="70" />
        </button>
      </li>
    </ul>
  </nav>
</template>
