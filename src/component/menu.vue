<template>
    <a-layout class="layout">
        <a-layout-sider collapsible breakpoint="xl">
            <div class="menu">
                <a-menu :style="{ width: '100%' }" :default-open-keys="['0']" :default-selected-keys="['0_2']"
                    accordion=true>
                    <a-sub-menu key="0">
                        <template #icon>
                            <icon-apps></icon-apps>
                        </template>
                        <template #title>Navigation 1</template>
                        <a-menu-item key="0_0">Menu 1</a-menu-item>
                        <a-menu-item key="0_1">Menu 2</a-menu-item>
                        <a-menu-item key="0_2">Menu 3</a-menu-item>
                        <a-menu-item key="0_3">Menu 4</a-menu-item>
                    </a-sub-menu>
                    <a-sub-menu key="1">
                        <template #icon>
                            <icon-bug></icon-bug>
                        </template>
                        <template #title>Navigation 2</template>
                        <a-menu-item key="1_0">Menu 1</a-menu-item>
                        <a-menu-item key="1_1">Menu 2</a-menu-item>
                        <a-menu-item key="1_2">Menu 3</a-menu-item>
                    </a-sub-menu>
                    <a-sub-menu key="2">
                        <template #icon>
                            <icon-bulb></icon-bulb>
                        </template>
                        <template #title>Navigation 3</template>
                        <a-menu-item key="2_0">Menu 1</a-menu-item>
                        <a-menu-item key="2_1">Menu 2</a-menu-item>
                        <a-sub-menu key="2_2" title="Navigation 4">
                            <a-menu-item key="2_2_0">Menu 1</a-menu-item>
                            <a-menu-item key="2_2_1">Menu 2</a-menu-item>
                        </a-sub-menu>
                    </a-sub-menu>
                </a-menu>
            </div>
        </a-layout-sider>
        <a-layout>
            <a-layout-header style="padding-left: 20px;">
                Header
            </a-layout-header>
            <a-layout style="padding: 0 24px;">
                <a-breadcrumb :style="{ margin: '16px 0' }">
                    <a-breadcrumb-item>Home</a-breadcrumb-item>
                    <a-breadcrumb-item>List</a-breadcrumb-item>
                    <a-breadcrumb-item>App</a-breadcrumb-item>
                </a-breadcrumb>
                <a-layout-content>
                    <slot></slot>
                </a-layout-content>
                <a-layout-footer>Footer</a-layout-footer>
            </a-layout>
        </a-layout>

    </a-layout>
    <!-- <p>{{Log}}</p> -->
</template>
<script>
import {
    IconMenuFold,
    IconMenuUnfold,
    IconApps,
    IconBug,
    IconBulb,
} from '@arco-design/web-vue/es/icon';

export default {
    components: {
        IconMenuFold,
        IconMenuUnfold,
        IconApps,
        IconBug,
        IconBulb,
    },
    data() {
        return {
        }
    },
    methods: {
    }
};
</script>
<style scoped>
.menu {
    box-sizing: border-box;
    width: 100%;
    height: 100%;
    padding: 0px;
    background-color: var(--color-neutral-2);
}
.layout {
  height: 100%;
  background: var(--color-fill-2);
  border: 1px solid var(--color-border);
}
.layout :deep(.arco-layout-content) {
  color: var(--color-text-2);
  font-weight: 400;
  font-size: 14px;
  background: var(--color-bg-3);
}
</style>
