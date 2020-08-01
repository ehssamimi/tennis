<template>
  <!-- Sidebar -->
  <!--
    Sidebar Mini Mode - Display Helper classes

    Adding 'smini-hide' class to an element will make it invisible (opacity: 0) when the sidebar is in mini mode
    Adding 'smini-show' class to an element will make it visible (opacity: 1) when the sidebar is in mini mode
    If you would like to disable the transition animation, make sure to also add the 'no-transition' class to your element

    Adding 'smini-hidden' to an element will hide it when the sidebar is in mini mode
    Adding 'smini-visible' to an element will show it (display: inline-block) only when the sidebar is in mini mode
    Adding 'smini-visible-block' to an element will show it (display: block) only when the sidebar is in mini mode
    -->
  <simplebar id="sidebar" aria-label="Main Navigation" class="  Bg-main h-100    h-100  " >
    <slot>
      <!-- Side Header -->
<!--      <div class="content-header bg-white-5">-->
<!--        &lt;!&ndash; Logo &ndash;&gt;-->
<!--        <router-link to="/" class="font-w600 text-dual">-->
<!--          <i class="fa fa-circle-notch text-primary"></i><span class="font-w700 font-size-h5 ml-1 smini-hide">ne</span>-->
<!--        </router-link>-->
<!--        &lt;!&ndash; END Logo &ndash;&gt;-->

<!--        &lt;!&ndash; Extra &ndash;&gt;-->
<!--        <div>-->
<!--          &lt;!&ndash; Options &ndash;&gt;-->
<!--          <b-dropdown size="sm" variant="dual" class="d-inline-block ml-2" menu-class="font-size-sm smini-hide border-0" right no-caret>-->
<!--            <template #button-content>-->
<!--              <i class="si si-drop"></i>-->
<!--            </template>-->
<!--            <li>-->
<!--              &lt;!&ndash; Color Themes &ndash;&gt;-->
<!--              <a class="dropdown-item d-flex align-items-center justify-content-between" @click.prevent="$store.commit('setColorTheme', { theme: '' })" href="#">-->
<!--                <span>Default</span>-->
<!--                <i class="fa fa-circle text-default"></i>-->
<!--              </a>-->
<!--              <a class="dropdown-item d-flex align-items-center justify-content-between" @click.prevent="$store.commit('setColorTheme', { theme: 'amethyst' })" href="#">-->
<!--                <span>Amethyst</span>-->
<!--                <i class="fa fa-circle text-amethyst"></i>-->
<!--              </a>-->
<!--              <a class="dropdown-item d-flex align-items-center justify-content-between" @click.prevent="$store.commit('setColorTheme', { theme: 'city' })" href="#">-->
<!--                <span>City</span>-->
<!--                <i class="fa fa-circle text-city"></i>-->
<!--              </a>-->
<!--              <a class="dropdown-item d-flex align-items-center justify-content-between" @click.prevent="$store.commit('setColorTheme', { theme: 'flat' })" href="#">-->
<!--                <span>Flat</span>-->
<!--                <i class="fa fa-circle text-flat"></i>-->
<!--              </a>-->
<!--              <a class="dropdown-item d-flex align-items-center justify-content-between" @click.prevent="$store.commit('setColorTheme', { theme: 'modern' })" href="#">-->
<!--                <span>Modern</span>-->
<!--                <i class="fa fa-circle text-modern"></i>-->
<!--              </a>-->
<!--              <a class="dropdown-item d-flex align-items-center justify-content-between" @click.prevent="$store.commit('setColorTheme', { theme: 'smooth' })" href="#">-->
<!--                <span>Smooth</span>-->
<!--                <i class="fa fa-circle text-smooth"></i>-->
<!--              </a>-->
<!--              &lt;!&ndash; END Color Themes &ndash;&gt;-->

<!--              <div role="separator" class="dropdown-divider"></div>-->

<!--              &lt;!&ndash; Sidebar Styles &ndash;&gt;-->
<!--              <base-layout-modifier tag="a" action="sidebarStyleLight" class="dropdown-item">-->
<!--                Sidebar Light-->
<!--              </base-layout-modifier>-->
<!--              <base-layout-modifier tag="a" action="sidebarStyleDark" class="dropdown-item">-->
<!--                Sidebar Dark-->
<!--              </base-layout-modifier>-->
<!--              &lt;!&ndash; Sidebar Styles &ndash;&gt;-->

<!--              <div role="separator" class="dropdown-divider"></div>-->

<!--              &lt;!&ndash; Header Styles &ndash;&gt;-->
<!--              <base-layout-modifier tag="a" action="headerStyleLight" class="dropdown-item">-->
<!--                Header Light-->
<!--              </base-layout-modifier>-->
<!--              <base-layout-modifier tag="a" action="headerStyleDark" class="dropdown-item">-->
<!--                Header Dark-->
<!--              </base-layout-modifier>-->
<!--              &lt;!&ndash; Header Styles &ndash;&gt;-->
<!--            </li>-->
<!--          </b-dropdown>-->
<!--          &lt;!&ndash; Options &ndash;&gt;-->

<!--          &lt;!&ndash; Close Sidebar, Visible only on mobile screens &ndash;&gt;-->
<!--          <base-layout-modifier size="sm" variant="dual" action="sidebarClose" class="d-lg-none ml-2">-->
<!--            <i class="fa fa-times"></i>-->
<!--          </base-layout-modifier>-->
<!--          &lt;!&ndash; END Close Sidebar &ndash;&gt;-->
<!--        </div>-->
<!--        &lt;!&ndash; END Extra &ndash;&gt;-->
<!--      </div>-->
      <!-- END Side Header -->

      <!-- Side Navigation -->
      <div class="content-side content-side-full mt-5 ">
        <base-navigation :nodes="navigation"></base-navigation>

      </div>
      <!-- END Side Navigation -->
    </slot>
  </simplebar>
  <!-- END Sidebar -->
</template>

<script>
// SimpleBar, for more info and examples you can check out https://github.com/Grsmto/simplebar/tree/master/packages/simplebar-vue
import simplebar from 'simplebar-vue'

// Get navigation data
import menuList from '@/data/menu'

export default {
  name: 'BaseSidebar',
  props: {
    classes: String
  },
  components: {
    simplebar
  },
  data () {
    return {
      // Get main navigation
      navigation: menuList.tennis
    }
  }
}
</script>
