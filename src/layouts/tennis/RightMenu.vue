<template>
<div>
<!--  <simplebar id="sidebar" aria-label="Main Navigation">-->
<!--    <slot>-->
<!--      &lt;!&ndash; Side Header &ndash;&gt;-->
<!--      <div class="content-header bg-white-5">-->
<!--        &lt;!&ndash; Logo &ndash;&gt;-->
<!--        <router-link to="/" class="font-w600 text-dual">-->
<!--          <i class="fa fa-circle-notch text-primary"></i><span class="font-w700 font-size-h5 ml-1 smini-hide">ne</span>-->
<!--        </router-link>-->
<!--        &lt;!&ndash; END Logo &ndash;&gt;-->

<!--        &lt;!&ndash; Extra &ndash;&gt;-->
<!--        <div>-->
<!--          &lt;!&ndash; Options &ndash;&gt;-->
<!--          <b-dropdown size="sm" variant="dual" class="d-inline-block ml-2" menu-class="font-size-sm smini-hide border-0"-->
<!--                      right no-caret>-->
<!--            <template #button-content>-->
<!--              <i class="si si-drop"></i>-->
<!--            </template>-->
<!--            <li>-->
<!--              &lt;!&ndash; Color Themes &ndash;&gt;-->
<!--              <a class="dropdown-item d-flex align-items-center justify-content-between"-->
<!--                 @click.prevent="$store.commit('setColorTheme', { theme: '' })" href="#">-->
<!--                <span>Default</span>-->
<!--                <i class="fa fa-circle text-default"></i>-->
<!--              </a>-->
<!--              <a class="dropdown-item d-flex align-items-center justify-content-between"-->
<!--                 @click.prevent="$store.commit('setColorTheme', { theme: 'amethyst' })" href="#">-->
<!--                <span>Amethyst</span>-->
<!--                <i class="fa fa-circle text-amethyst"></i>-->
<!--              </a>-->
<!--              <a class="dropdown-item d-flex align-items-center justify-content-between"-->
<!--                 @click.prevent="$store.commit('setColorTheme', { theme: 'city' })" href="#">-->
<!--                <span>City</span>-->
<!--                <i class="fa fa-circle text-city"></i>-->
<!--              </a>-->
<!--              <a class="dropdown-item d-flex align-items-center justify-content-between"-->
<!--                 @click.prevent="$store.commit('setColorTheme', { theme: 'flat' })" href="#">-->
<!--                <span>Flat</span>-->
<!--                <i class="fa fa-circle text-flat"></i>-->
<!--              </a>-->
<!--              <a class="dropdown-item d-flex align-items-center justify-content-between"-->
<!--                 @click.prevent="$store.commit('setColorTheme', { theme: 'modern' })" href="#">-->
<!--                <span>Modern</span>-->
<!--                <i class="fa fa-circle text-modern"></i>-->
<!--              </a>-->
<!--              <a class="dropdown-item d-flex align-items-center justify-content-between"-->
<!--                 @click.prevent="$store.commit('setColorTheme', { theme: 'smooth' })" href="#">-->
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
<!--      &lt;!&ndash; END Side Header &ndash;&gt;-->

<!--      &lt;!&ndash; Side Navigation &ndash;&gt;-->
<!--      <div class="content-side content-side-full">-->
<!--        <base-navigation :nodes="navigation"></base-navigation>-->
<!--      </div>-->
<!--      &lt;!&ndash; END Side Navigation &ndash;&gt;-->
<!--    </slot>-->
<!--  </simplebar>-->



  <div id="main-container" v-b-visible="Sidebar">
    <b-row class="m-0">

      <b-col class="ml-6 p-0">
        <slot name="content"></slot>
        <transition name="fade" mode="out-in">
          <router-view></router-view>
        </transition>
      </b-col>



      <b-col cols="2" class="p-0">
        <b-col cols="10" class="p-0 float-right simplebar-content-wrapper">
<!--          <simplebar class="slider-right " aria-label="Main Navigation">-->
<!--            <slot>-->
        <div class="w-100  Bg-main menu-radius nav-main-link-icon h-100"   >

          <div class="content-side content-side-full p-0 pt-6    " dir="rtl">
<!--            <base-navigation-->
<!--              :nodes="[-->
<!--            {-->
<!--              name: 'پیشخوان',-->
<!--              to: '/',-->
<!--              icon: 'si si-speedometer'-->
<!--            },-->
<!--            {-->
<!--              name: 'More',-->
<!--              heading: true-->
<!--            },-->
<!--            {-->
<!--              name: 'Landing',-->
<!--              to: '/landing',-->
<!--              icon: 'si si-rocket'-->
<!--            }-->
<!--          ]"-->
<!--            ></base-navigation>-->
            <base-navigation :nodes="navigation"></base-navigation>
          </div>

        </div>
<!--            </slot>-->
<!--          </simplebar>-->
        </b-col>
      </b-col>
    </b-row>


  </div>
</div>


</template>

<script>
    // import simplebar from "simplebar-vue";
    import menuList from '@/data/menu'

    export default {
        name: "RightMenu",
      components: {
        // simplebar
      },
      data () {
        return {

          // Get main navigation
          navigation: menuList.tennis
        }
      }
    }
</script>

<style scoped>

</style>
