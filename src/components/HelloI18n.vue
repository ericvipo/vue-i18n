<template>
  <div>
    <!-- <p>{{ $t("hello", {name}) }}</p>
    <p>{{ $t("email", {email}) }}</p>
    <p>{{ $t("goodbye") }}</p> -->

    <p>{{ $tc("car", 2) }}</p>
    <p>{{ $tc("person", 0) }}</p>
    <p>{{ $tc("person", 1) }}</p>
    <p>{{ $tc("person", 9) }}</p>


    <button class="button" @click="setLocale('en')">English</button>
    <button class="button" @click="setLocale('es')">Spanish</button>
    <button class="button" @click="setLocale('de')">German</button>
  </div>
</template>

<script>
export default {
  name: "HelloI18n",
  data() {
    return {
      name: 'Eric',
      email: 'ericvpoma@gmail.com'
    }
  },
  methods: {
    setLocale(locale) {
      this.$root.$i18n.locale = locale;
      // localStorage.setItem('locale', locale)
    }
  }
};
</script>

<!-- <i18n>
{
  "en": {
    "hello": "Hello i18n in SFC!"
  },
  "es": {
    "hello": "Hola i18n in SFC!"
  }
}
</i18n> -->
