<template>
  <div v-if="saleVisible" class="sales">
    Скидки до -20% в это воскресенье!
    <button class="close" @click="changeVisible()">
      <svg
        width="12"
        height="12"
        viewBox="0 0 12 12"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M10.3535 2.35348L9.64648 1.64648L5.99998 5.293L2.35348 1.64648L1.64648 2.35348L5.29298 6L1.64648 9.6465L2.35348 10.3535L5.99998 6.707L9.64648 10.3535L10.3535 9.6465L6.70698 6L10.3535 2.35348Z"
          fill="#F7F7F7"
        />
      </svg>
    </button>
  </div>
</template>

<script lang="ts">
export default {
  data() {
    return {
      saleVisible: true,
    };
  },
  methods: {
    changeVisible() {
      this.saleVisible = false;
      localStorage.setItem("saleVisible", JSON.stringify(this.saleVisible));
    },
  },
  mounted() {
    const saleVisible: boolean = JSON.parse(
      localStorage.getItem("saleVisible") as string
    );
    saleVisible == false
      ? (this.saleVisible = saleVisible)
      : (this.saleVisible = true);
  },
};
</script>

<style lang="scss" scoped>
@import "~/assets/variables.scss";
.sales {
  position: relative;
  padding: 6px 0;
  font-weight: 500;
  font-size: 13px;
  line-height: 18px;
  text-align: center;
  color: $extra-light-color;
  background: $extra-dark-color;

  .close {
    position: absolute;
    right: 12px;
    top: 50%;
    transform: translateY(-50%);
    background: transparent;
    border: 0;
    cursor: pointer;
  }
}
</style>
