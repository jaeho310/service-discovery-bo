<template>
  <section id="about-me">
    <div class="py-12" />
    <v-container class="text-center">
      <h2 class="text-h2 font-weight-bold mb-3">SERVICE DISCOVERY </h2>
      <v-responsive
        class="mx-auto mb-8"
        width="56"
      >
        <v-divider class="mb-1" />
        <v-divider />
      </v-responsive>
      <v-responsive
        class="mx-auto text-h4 font-weight-light mb-8"
        max-width="720"
      >
        kubernetes 분석, 모니터링 서비스 입니다.
      </v-responsive>
      <v-avatar
        class="mb-12"
        size="128"
      >
        <v-img src="@/assets/vmd.svg" />
      </v-avatar>
      <div />
      <v-btn
        color="grey"
        href="http://b-iris.mobigen.com/"
        outlined
        large
      >
        <span class="grey--text text--darken-1 font-weight-bold">
          Go to B-iris
        </span>
      </v-btn>
    </v-container>
    <div class="py-12" />
  </section>
</template>

<script>
  export default {
    name: 'HomeView',
  }
</script>
