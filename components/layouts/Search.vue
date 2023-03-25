<template>
  <div v-if="active" class="search-container">
    <div class="search-wrapper">
      <div class="search-box">
        <input
          type="text"
          placeholder="Искать по названию, артикулу, характеристике"
        />
        <button>
          <svg
            width="24"
            height="24"
            viewBox="0 0 24 24"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M22.2069 20.7929L16.3141 14.8999C17.5655 13.2888 18.1557 11.2614 17.9647 9.23038C17.7737 7.19937 16.8158 5.31752 15.286 3.96799C13.7562 2.61845 11.7696 1.90269 9.73062 1.96645C7.69165 2.0302 5.75363 2.86868 4.31115 4.31115C2.86868 5.75363 2.0302 7.69165 1.96645 9.73062C1.90269 11.7696 2.61845 13.7562 3.96799 15.286C5.31752 16.8158 7.19937 17.7737 9.23038 17.9647C11.2614 18.1557 13.2888 17.5655 14.8999 16.3141L20.7929 22.2069L22.2069 20.7929ZM9.99994 15.9999C8.81325 15.9999 7.65322 15.648 6.66652 14.9888C5.67983 14.3295 4.91079 13.3924 4.45667 12.296C4.00254 11.1997 3.88372 9.99329 4.11523 8.8294C4.34674 7.66551 4.91819 6.59642 5.7573 5.7573C6.59642 4.91819 7.66551 4.34674 8.8294 4.11523C9.99329 3.88372 11.1997 4.00254 12.296 4.45667C13.3924 4.91079 14.3295 5.67983 14.9888 6.66652C15.648 7.65322 15.9999 8.81325 15.9999 9.99994C15.9981 11.5907 15.3654 13.1158 14.2406 14.2406C13.1158 15.3654 11.5907 15.9981 9.99994 15.9999Z"
              fill="#4C1C20"
            />
          </svg>
        </button>
      </div>
      <button class="close" @click="$emit('update:active', false)">
        <svg
          width="30"
          height="30"
          viewBox="0 0 30 30"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M25.8837 5.88371L24.1162 4.11621L15 13.2325L5.88371 4.11621L4.11621 5.88371L13.2325 15L4.11621 24.1162L5.88371 25.8837L15 16.7675L24.1162 25.8837L25.8837 24.1162L16.7675 15L25.8837 5.88371Z"
            fill="#4C1C20"
          />
        </svg>
      </button>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  props: {
    active: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style lang="scss" scoped>
@import "~/assets/variables.scss";

.search-container {
  top: 0;
  left: 0;
  position: absolute;
  width: 100%;
  height: 100vh;
  background: rgba($extra-dark-color, 0.8);
}

.search-wrapper {
  position: relative;
  padding: 45px 0;
  background: $extra-light-color;
  display: flex;
  justify-content: center;
  align-content: center;
  display: flex;
  justify-content: center;
  align-content: center;
}

.close {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  right: 63px;
  background: transparent;
  border: 0;
}

.search-box {
  position: relative;
  width: 100%;
  max-width: 680px;

  input {
    background: rgba($input-color, 0.2);
    border-radius: 6px;
    padding: 24px 60px 24px 32px;
    width: calc(100% - 32px - 60px);
    border: 0;
    outline: none;
    font-weight: 400;
    font-size: 20px;
    line-height: 30px;
    letter-spacing: -0.3px;

    &::placeholder {
      color: $placeholder-color;
    }
  }

  button {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background: transparent;
    border: 0;
    right: 31px;
  }
}
</style>
