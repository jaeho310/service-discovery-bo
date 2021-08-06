<template>
  <v-app>
    <default-bar />

    <default-drawer />

    <default-view />

    <default-footer />

    <!-- <default-settings /> -->
  </v-app>
</template>

<script>
  export default {
    name: 'DefaultLayout',

    components: {
      // 상단 앱바
      DefaultBar: () => import(
        /* webpackChunkName: "default-app-bar" */
        './AppBar'
      ),
      // 사이드바
      DefaultDrawer: () => import(
        /* webpackChunkName: "default-drawer" */
        './Drawer'
      ),
      // 푸터
      DefaultFooter: () => import(
        /* webpackChunkName: "default-footer" */
        './Footer'
      ),
      // 우측 세팅
      // DefaultSettings: () => import(
      //   /* webpackChunkName: "default-settings" */
      //   './Settings'
      // ),
      // 메인 뷰
      DefaultView: () => import(
        /* webpackChunkName: "default-view" */
        './View'
      ),
    },
  }
</script>
