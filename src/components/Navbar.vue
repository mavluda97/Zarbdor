<template>
  <nav class="navbar">
    <div class="logo">
      <img src="../assets/logo.svg" alt="logo" height="100%" width="100%" />
    </div>
    <a href="" class="toggle-button" @click.prevent="toggleButton()"
      ><v-icon style="color: #19d3cc">mdi-menu</v-icon></a
    >
    <div class="navbar-links" v-bind:class="{ active: isActive }">
      <ul>
        <li><a href="">Asosiy</a></li>
        <li><a href="">Ilova haqida</a></li>
        <li><a href="">Afzalliklar</a></li>
        <li><a href="">Statistika</a></li>
        <li><a href="">Qo'llanma</a></li>
        <li>
          <v-btn
            rounded
            color="#2B85C5"
            class="white--text ma-2 text-capitalize"
            >Kirish</v-btn
          >
        </li>
        <li class="lang"><a href="#">Uz</a>|<a href="#">Ru</a></li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navbar",

  data() {
    return {
      isActive: false,
    };
  },

  methods: {
    setLocale(locale) {
      this.$i18n.locale = locale;
      localStorage.setItem("locale", locale);
    },

    toggleButton() {
      this.isActive = !this.isActive;
    },
  },
};
</script>

<style scoped>
* {
  padding: 0;
  margin: 0;
}

.navbar {
  padding: 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  position: fixed;
  z-index: 111;
  background-color: #fff;
  box-shadow: 1px 6px 12px -4px rgba(0, 0, 0, 1);
  -webkit-box-shadow: 1px 6px 12px -4px rgba(0, 0, 0, 1);
  -moz-box-shadow: 1px 6px 12px -4px rgba(0, 0, 0, 1);
}

.logo {
  margin-left: 30px;
  margin-top: 3px;
}

.navbar-links ul {
  display: flex;
  align-items: baseline;
  padding-right: 20px;
  margin: 0;
}

.navbar-links ul li {
  list-style: none;
}

.navbar-links ul li a:hover {
  color: #2b85c5;
}

.navbar-links ul li a {
  text-decoration: none;
  color: #19d3cc;
  font-family: Open Sans, sans-serif, sans-serif;
  text-transform: capitalize;
  font-size: 0.875rem;
  font-weight: 500;
  letter-spacing: 0.0892857143em;
  padding: 1rem;
  display: block;
  margin: 0;
  transition: color 0.3s ease 0s;
}

.toggle-button {
  text-decoration: none;
  position: absolute;
  top: 1.5rem;
  right: 1rem;
  display: none;
}

.lang {
  display: flex;
  align-items: baseline;
  color: #19d3cc;
  justify-content: center;
}

@media (max-width: 950px) {
  .toggle-button {
    display: block;
  }
  .navbar-links {
    display: none;
  }

  .navbar {
    padding-bottom: 10px;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
  }

  .navbar-links {
    margin: 0;
    padding: 0;
    width: 100%;
  }
  .navbar-links ul {
    width: 100%;
    flex-direction: column;
    padding: 0;
    margin: 0;
  }
  .navbar-links li {
    width: 100%;
    text-align: center;
  }
  .navbar-links ul > li > a {
    padding: 6px;
  }

  .navbar-links.active {
    display: flex;
  }
}
</style>
