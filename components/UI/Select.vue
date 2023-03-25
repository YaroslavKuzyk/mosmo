<template>
  <div class="select" :class="{ active: active }">
    <div class="select-header" @click="active = !active">
      {{ model }}
      <svg
        width="8"
        height="6"
        viewBox="0 0 8 6"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          fill-rule="evenodd"
          clip-rule="evenodd"
          d="M0.30967 2.38765L3.01492 5.0929C3.42227 5.50025 4.0803 5.50025 4.48766 5.0929L7.19291 2.38765C7.85094 1.72962 7.38091 0.601562 6.45131 0.601562H1.04082C0.111215 0.601562 -0.348364 1.72962 0.30967 2.38765Z"
          fill="#ED6A5E"
        />
      </svg>
    </div>
    <div v-if="active" class="select-body">
      <div
        class="select-body__item"
        v-for="(item, index) in list"
        :key="index"
        @click="chooseLang(item)"
      >
        {{ item }}
      </div>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  props: {
    items: {
      type: Array,
      default: () => [],
    },
    model: {
      type: String,
      default: "",
    },
  },
  data() {
    return {
      active: false,
    };
  },
  computed: {
    list(): string[] {
      const list = this.items as string[];
      return list.filter((el) => el != this.model);
    },
  },
  methods: {
    chooseLang(item: string) {
      this.$emit("update:model", item);
      this.active = false;
    },
  },
};
</script>

<style lang="scss" scoped>
@import "~/assets/variables.scss";

.select {
  position: relative;
  cursor: pointer;

  svg {
    transition: 0.5s;
  }

  &.active {
    svg {
      transform: rotate(-180deg);
    }
  }

  &-body {
    position: absolute;
    top: 23px;
    background: $extra-light-color;
    padding: 0 5px;
    left: -5px;

    &__item {
      margin-bottom: 2px;
    }
  }
}
</style>
