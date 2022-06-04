<template>
  <section class="section section-about-profile">
    <div class="container">
      <h1 class="page-ttl">ABOUT</h1>
      <figure class="prof-fig">
        <picture class="prof-fig-img">
          <img
            src="imgs/page/about/self-pic.jpg"
            alt="+81_kentaのプロフィール画像"
          />
        </picture>
      </figure>
      <h2 class="prof-nm">+81_kenta</h2>
      <p class="prof-position">SE, Webデザイナー</p>
      <hr class="prof-hr" />
      <p class="prof-bio prof-bio-ja">
        1996年生まれ大阪生まれ。給費生として神奈川大学国際経営学科入学後、アメリカ・韓国・スペインに留学し語学を学ぶ、
        事業会社にてPBXクラウド化、アンケートシステム構築・運用を担当。現在は、rails,nuxt.jsを使用したWeb開発案件を行う傍ら、Webデザイナーとしても活動を行う。
      </p>
      <!-- <p class="prof-bio prof-bio-en"></p> -->
    </div>
  </section>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.section-about-profile {
  > .container {
    padding-bottom: 40px;

    > .prof-fig {
      position: relative;
      display: flex;

      &::before {
        content: '';
        width: 100%;
        padding-top: 51.851851851%;
      }

      > .prof-fig-img {
        position: absolute;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
        max-width: 800px;
        margin: 0 auto;
      }
    }

    > .prof-nm {
      margin-top: 32px;
      letter-spacing: 0;
      text-align: left;

      @include mq(sm) {
        margin-top: 24px;
        font-size: 24px;
      }

      @include mq(xs) {
        text-align: center;
      }
    }

    > .prof-position {
      margin-top: 8px;
      text-align: left;

      @include mq(sm) {
        margin-top: 4px;
      }

      @include mq(xs) {
        text-align: center;
      }
    }

    > .prof-hr {
      width: 32%;
      max-width: 240px;
      min-width: 160px;
      margin-top: 32px;
      margin-bottom: 0;
      border-color: var(--color-stroke-gray);

      @include mq(sm) {
        margin-top: 24px;
      }

      @include mq(xs) {
        margin: 24px auto 0;
      }
    }

    > .prof-bio {
      max-width: 960px;
      margin-top: 40px;
      padding-right: 40px;

      @include mq(sm) {
        margin-top: 24px;
        padding-right: 0;
      }
    }
  }
}
</style>
