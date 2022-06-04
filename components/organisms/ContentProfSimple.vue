<template>
  <div class="content content-prof-simple">
    <figure class="prof-fig">
      <picture class="prof-fig-img">
        <img src="/imgs/self-pic.jpg" alt="+81_kenta" loading="lazy" />
      </picture>
    </figure>
    <h2 class="prof-nm txt-center">+81_kenta</h2>
    <p class="prof-position txt-center">SE, Webデザイナー</p>
    <p class="prof-bio">
      事業会社にてPBXクラウド化、アンケートシステム構築・運用を担当。現在は、rails,nuxt.jsを使用したWeb開発案件を行う傍ら、Webデザイナーとしても活動を行う。
    </p>
    <div class="sns-more">
      <ListSns class="icon-large" />
      <ButtonLink to="/about">ABOUT</ButtonLink>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.content-prof-simple {
  > .prof-fig {
    position: relative;
    display: flex;
    justify-content: center;
    width: 160px;
    margin: auto;
    border-radius: 50%;
    overflow: hidden;

    @include mq(md) {
      width: 120px;
    }

    @include mq(sm) {
      width: 100px;
    }

    @include mq(xs) {
      width: 88px;
    }

    &::before {
      content: '';
      width: 100%;
      padding-top: 100%;
    }

    > .prof-fig-img {
      position: absolute;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
    }
  }

  > .prof-nm {
    margin-top: 16px;
    letter-spacing: 0;

    @include mq(sm) {
      font-size: 24px;
    }
  }

  > .prof-position {
    margin-top: 14px;

    @include mq(sm) {
      font-size: 12px;
    }
  }

  > .prof-bio {
    margin-top: 8px;

    @include mq(sm) {
      margin-top: 16px;
    }

    @include mq(xxs) {
      letter-spacing: -0.01em;
    }
  }

  > .sns-more {
    display: flex;
    flex-direction: column;

    > .list {
      order: 1;
      width: 100%;
      margin-top: 16px;
      justify-content: center;

      @include mq(md) {
        order: 2;
        margin-top: 20px;
      }
    }

    > .button-link {
      order: 2;
      width: 100%;
      max-width: 200px;
      margin: 24px auto 0;

      @include mq(md) {
        order: 1;
      }
    }
  }
}
</style>
