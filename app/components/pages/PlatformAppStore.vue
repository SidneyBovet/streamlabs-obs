<template>
<div>
  <div class="app-store-container">
    <webview-loader>
      <webview
        class="app-store"
        v-if="loggedIn"
        id="appStoreWebview"
        :src="appStoreUrl"
        ref="appStoreWebview"
        preload="bundles/guest-api">
      </webview>
    </webview-loader>
  </div>
</div>
</template>

<script lang="ts" src="./PlatformAppStore.vue.ts"></script>

<style lang="less" scoped>
.app-store-container {
  position: absolute;
  top: -1px;
  right: 0;
  bottom: 0;
  left: 0;
}

.app-store {
  position: absolute;
  top: -2px;
  right: 0;
  bottom: 0;
  left: 0;
}
</style>

