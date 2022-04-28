<template>
  <nav>
    <ul>
      <li>
        <nuxt-link exact to="/">
          <AppLogo />
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/restaurants">Restaurants</nuxt-link>
      </li>
    </ul>
    <nuxt-link to="/cart">Cart</nuxt-link>
    
    <div class="smallnum" v-if="totalItems > 0">
        {{totalItems}}
    </div>
  </nav>
</template>

<script>
import AppLogo from "@/components/AppLogo.vue";
import { mapGetters } from 'vuex'

export default {
  components: {
    AppLogo,
  },
  computed: {
      ...mapGetters(["totalItems"])
  },
};
</script>

<style lang="scss" scoped></style>