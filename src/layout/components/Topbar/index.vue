<!--
 * @Date: 2021-08-02 14:01:22
 * @LastEditors: baici
 * @LastEditTime: 2021-08-05 01:07:47
 * @FilePath: \src\layout\components\Topbar\index.vue
 * @Github: https://github.com/baici1/CTGUadmin
-->
<template>
  <div class="header">
    <div class="navigation">
      <!-- 用于mobile显示 -->
      <logo v-if="isShowLogo"></logo>
      <hamburger></hamburger>
      <breadcrumbs></breadcrumbs>
    </div>
    <div class="action">
      <Userinfo></Userinfo>
    </div>
  </div>
</template>

<script>
import Logo from "@/layout/components/Sidebar/Logo.vue";
import Hamburger from "./Hamburger.vue";
import Breadcrumbs from "./Breadcrumbs.vue";
import Userinfo from "./Userinfo.vue";
import { computed } from "vue";

export default {
  components: {
    Logo,
    Hamburger,
    Breadcrumbs,
    Userinfo,
  },
  setup() {
    const isShowLogo = computed(() => false);
    return { isShowLogo };
  },
};
</script>

<style lang="scss" scoped>
.header {
  height: 48px;
  border-bottom: 1px solid #e0e4ef;
  display: flex;
  justify-content: space-between;
  .navigation {
    display: flex;
    align-items: center;
    overflow: hidden;
  }
  .action {
    display: flex;
    align-items: center;
  }
}
</style>
