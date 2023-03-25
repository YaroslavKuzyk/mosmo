<template>
  <header>
    <div class="container">
      <div class="header">
        <ul class="header__category">
          <li><nuxt-link to="/famale">Женское</nuxt-link></li>
          <li><nuxt-link to="/famale">Gender Neutral</nuxt-link></li>
          <li><nuxt-link to="/famale">Мужское</nuxt-link></li>
          <li><nuxt-link to="/famale">Детское</nuxt-link></li>
        </ul>
        <nuxt-link to="/">
          <img src="~/assets/img/logo.svg" alt="Logo" />
        </nuxt-link>
        <div class="header__account">
          <button @click="openSearch = true" class="search">
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
          <nuxt-link class="favorite" to="/favorite">
            <svg
              width="20"
              height="20"
              viewBox="0 0 20 20"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M13.8903 2.5C13.1105 2.53716 12.3508 2.75972 11.6742 3.14921C10.9976 3.5387 10.4237 4.0839 9.99996 4.73958C9.57621 4.0839 9.00229 3.5387 8.3257 3.14921C7.64912 2.75972 6.88943 2.53716 6.10963 2.5C3.29696 2.5 1.66663 4.666 1.66663 7.33792C1.66663 11.2963 7.04854 16.3543 9.99996 18.3333C12.9514 16.3543 18.3333 11.2963 18.3333 7.33792C18.3333 4.666 16.703 2.5 13.8903 2.5Z"
                fill="#4C1C20"
              />
            </svg>
          </nuxt-link>
          <nuxt-link class="basket" to="/basket"
            ><svg
              width="26"
              height="26"
              viewBox="0 0 26 26"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M7.58337 20.5833C7.31554 20.5833 7.05373 20.6627 6.83104 20.8116C6.60835 20.9603 6.43478 21.1718 6.33229 21.4192C6.22979 21.6668 6.20298 21.939 6.25523 22.2017C6.30748 22.4643 6.43645 22.7057 6.62584 22.8951C6.81521 23.0844 7.05651 23.2133 7.31919 23.2657C7.58187 23.3179 7.85415 23.2911 8.10159 23.1886C8.34903 23.0861 8.56053 22.9125 8.70933 22.6899C8.85812 22.4671 8.93754 22.2053 8.93754 21.9375C8.93754 21.5784 8.79487 21.2339 8.54091 20.9799C8.28696 20.726 7.94252 20.5833 7.58337 20.5833ZM19.5 20.5833C19.2322 20.5833 18.9704 20.6627 18.7477 20.8116C18.525 20.9603 18.3515 21.1718 18.2489 21.4192C18.1464 21.6668 18.1197 21.939 18.1719 22.2017C18.2242 22.4643 18.3531 22.7057 18.5425 22.8951C18.7318 23.0844 18.9732 23.2133 19.2358 23.2657C19.4985 23.3179 19.7708 23.2911 20.0183 23.1886C20.2657 23.0861 20.4772 22.9125 20.6259 22.6899C20.7748 22.4671 20.8542 22.2053 20.8542 21.9375C20.8542 21.5784 20.7115 21.2339 20.4576 20.9799C20.2037 20.726 19.8592 20.5833 19.5 20.5833ZM19.5 19.4981V17.873L8.52707 17.8629L8.06296 15.9974L21.6675 13.3935L21.6667 5.41667H5.43133L4.89248 3.25H1.08337V4.875H3.62206L7.25642 19.4868L19.5 19.4981Z"
                fill="#4C1C20"
              />
            </svg>
          </nuxt-link>
          <div class="select-wrapper">
            <Select
              :items="languegeList"
              :model="languege"
              @update:model="languege = $event"
            />
          </div>
          <div class="account">
            <img src="~/assets/img/accout-template.svg" alt="account" />
            <span>Добрый день, Диана</span>
          </div>
        </div>
      </div>
    </div>
    <nav>
      <div class="container">
        <ul class="header-navigation">
          <li><nuxt-link to="/">Бренды</nuxt-link></li>
          <li><nuxt-link to="/">Одежда</nuxt-link></li>
          <li><nuxt-link to="/">Обувь</nuxt-link></li>
          <li><nuxt-link to="/">Сумки</nuxt-link></li>
          <li><nuxt-link to="/">Аксессуары</nuxt-link></li>
          <li><nuxt-link to="/">Украшения</nuxt-link></li>
          <li><nuxt-link to="/">Косметика</nuxt-link></li>
          <li><nuxt-link to="/">Bespoke</nuxt-link></li>
          <li><nuxt-link to="/">MSMGZN</nuxt-link></li>
          <li><nuxt-link to="/">The Earth</nuxt-link></li>
        </ul>
      </div>
    </nav>
    <Search :active="openSearch" @update:active="openSearch = $event" />
  </header>
</template>
<script lang="ts">
import Select from "~/components/UI/Select.vue";
import Search from "~/components/layouts/Search.vue";
export default {
  components: { Select, Search },
  data() {
    return {
      languegeList: ["EN", "UA", "RU"],
      languege: "EN",
      openSearch: false,
    };
  },
};
</script>
<style lang="scss" scoped>
@import "~/assets/variables.scss";

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 31px 0 43px;
}

.header__category {
  list-style: none;
  display: flex;

  li {
    margin-right: 28px;
  }

  a {
    text-decoration: none;
    color: $main-color;
    font-weight: 500;
    font-size: 14px;
    line-height: 140%;
    padding-bottom: 5px;
    border-bottom: 2px solid transparent;
    transition: 0.5s;

    &:hover {
      border-color: $event-color;
    }
  }
}

.header__account {
  display: flex;
  align-items: center;
}

.search {
  background: transparent;
  border: 0;
  margin-right: 27px;
}

.favorite {
  margin-right: 27px;
}

.basket {
  margin-right: 27px;
}

.account {
  display: flex;
  align-items: center;

  img {
    width: 26px;
    height: 26px;
    border-radius: 50%;
    padding: 3px;
    border: 1px solid rgb($main-color, 0.2);
    margin-right: 6px;
  }

  span {
    font-weight: 500;
    font-size: 14px;
    line-height: 140%;
    color: $main-color;
  }
}

nav {
  padding: 10px 0;
  background: $main-color;
}

.header-navigation {
  list-style: none;
  display: flex;
  justify-content: space-between;

  a {
    text-decoration: none;
    color: $extra-light-color;
    font-weight: 500;
    font-size: 13px;
    line-height: 140%;
  }
}

.select-wrapper {
  display: flex;
  justify-content: center;
  min-width: 40px;
  margin-right: 27px;
}
</style>
