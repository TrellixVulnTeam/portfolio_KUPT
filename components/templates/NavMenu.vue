<template>
  <aside class="nav nav-menu">
    <div class="container">
      <nav class="pages" @click="$emit('clickCloseMenu')">
        <nuxt-link to="/" class="page">
          <span class="page-txt">TOP</span>
        </nuxt-link>
        <nuxt-link to="/about" class="page">
          <span class="page-txt">ABOUT</span>
        </nuxt-link>
        <!-- <nuxt-link to="/" class="page">
          <span class="page-txt">NEWS</span>
        </nuxt-link> -->
        <nuxt-link to="/works" class="page">
          <span class="page-txt">WORKS</span>
        </nuxt-link>
        <!-- <nuxt-link to="/contact" class="page">
          <span class="page-txt">CONTACT</span>
        </nuxt-link> -->
        <!-- <a href="#" target="_blank" class="page">
          <span class="page-txt">SHOP</span>
        </a> -->
      </nav>
      <ListSns />
    </div>
  </aside>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.nav-menu {
  display: flex;
  align-items: center;
  padding: 40px;
  background: var(--color-stroke-default-72);
  backdrop-filter: blur(6px);

  @include mq(sm) {
    padding: 20px;
  }

  > .container {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    width: 100%;
    height: 100%;
    padding: 64px 0 80px;

    @include mq(sm) {
      justify-content: center;
      padding: 40px 0 80px;

      @media screen and (max-height: 720px) {
        padding-bottom: 40px;
      }
    }

    > .pages {
      display: flex;
      flex-wrap: wrap;

      > .page {
        width: 50%;
        padding: 12px 20px;
        font-size: 32px;
        line-height: 1.2em;
        letter-spacing: 0.08em;

        @include mq(sm) {
          width: 100%;
          font-weight: 500;
          font-size: 20px;
        }

        > .page-txt {
          position: relative;
          display: inline-block;
          white-space: nowrap;

          &::before {
            content: '';
            position: absolute;
            bottom: -3px;
            left: 1px;
            display: block;
            width: 0;
            height: 1px;
            background-color: var(--color-stroke-default);
            transition: all 0.24s cubic-bezier(0.11, 0, 0.5, 0);
          }
        }

        &:hover,
        &.page-active,
        &.nuxt-link-exact-active {
          > .page-txt {
            &::before {
              width: calc(100% - 2px);
            }
          }
        }
      }
    }

    > .list {
      margin-top: 40px;
      margin-left: 10px;

      @include mq(sm) {
        @media screen and (max-height: 720px) {
          margin-top: 24px;
        }
      }
    }
  }
}
</style>
