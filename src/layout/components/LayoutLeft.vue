<template>
  <div class="layout-left">
    <div style="height: 50px"></div>
    <el-menu default-active="2" :collapse="isCollapse">
      <el-sub-menu index="1">
        <template #title>
          <el-icon>
            <location />
          </el-icon>
          <span>Navigator One</span>
        </template>
        <el-menu-item-group>
          <template #title><span>Group One</span></template>
          <el-menu-item index="1-1">item one</el-menu-item>
          <el-menu-item index="1-2">item two</el-menu-item>
        </el-menu-item-group>
        <el-menu-item-group title="Group Two">
          <el-menu-item index="1-3">item three</el-menu-item>
        </el-menu-item-group>
        <el-sub-menu index="1-4">
          <template #title><span>item four</span></template>
          <el-menu-item index="1-4-1">item one</el-menu-item>
        </el-sub-menu>
      </el-sub-menu>
      <el-menu-item index="2">
        <el-icon>
          <icon-menu />
        </el-icon>
        <template #title>Navigator Two</template>
      </el-menu-item>
      <el-menu-item index="3" disabled>
        <el-icon>
          <document />
        </el-icon>
        <template #title>Navigator Three</template>
      </el-menu-item>
      <el-menu-item index="4">
        <el-icon>
          <setting />
        </el-icon>
        <template #title>Navigator Four</template>
      </el-menu-item>
    </el-menu>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "LayoutLeft",
  components: {},
  setup() {
    const isCollapse = ref(false);

    return {
      isCollapse,
    };
  },
});
</script>

<style lang="scss" scoped>
.layout-left {
  background: rgb(48, 65, 86);
}
</style>
