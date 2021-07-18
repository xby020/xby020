<template>
  <v-app-bar app flat dark color="#1B2021">
    <!-- logo -->
    banana
    <v-spacer></v-spacer>
    <v-switch label="darkMode" v-model="isDark"></v-switch>
  </v-app-bar>
</template>

<script>
export default {
  name: "topBar",
  data() {
    return {
      isDark: false
    };
  },
  watch: {
    isDark: {
      handler(val) {
        this.$vuetify.theme.dark = val;
      },
      immediate: true
    }
  }
};
</script>

<style lang="scss" scoped></style>
