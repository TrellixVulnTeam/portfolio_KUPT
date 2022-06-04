<template>
  <div class="section section-top-sns">
    <div class="container">
      <section class="sns sns-insta">
        <div class="container">
          <h2 class="sns-ttl txt-center">
            <svg viewBox="0 0 24 24" class="sns-icon">
              <use xlink:href="#i-instagram" />
            </svg>
          </h2>
          <ListSnsImg :sns="instagram" />
          <ButtonLinkBlank to="https://www.instagram.com/onmywaysince1996/">
            instagram
          </ButtonLinkBlank>
        </div>
      </section>
      <!-- <section class="sns sns-shop">
        <div class="container">
          <h2 class="sns-ttl txt-center">
            <svg viewBox="0 0 24 24" class="sns-icon">
              <use xlink:href="#i-shop" />
            </svg>
          </h2>
          <ListSnsImg :sns="shop" />
          <ButtonLinkBlank to="https://www.instagram.com/onmywaysince1996/">
            shop more
          </ButtonLinkBlank>
        </div>
      </section> -->
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      instagram: [
        {
          href: 'https://www.instagram.com/p/CVsnjlxPsRi/',
          img: '/imgs/page/top/instagram1.jpg',
          alt: '+81_kentaのインスタグラム1',
        },
        {
          href: 'https://www.instagram.com/p/CVskiepP5AT/',
          img: '/imgs/page/top/instagram2.jpg',
          alt: '+81_kentaのインスタグラム2',
        },
        {
          href: 'https://www.instagram.com/p/CVsj5PqPSuW/',
          img: '/imgs/page/top/instagram3.jpg',
          alt: '+81_kentaのインスタグラム３',
        },
        {
          href: 'https://www.instagram.com/p/CLJtOFdAVCc/',
          img: '/imgs/page/top/instagram4.jpg',
          alt: '+81_kentaのインスタグラム４',
        },
        {
          href: 'https://www.instagram.com/p/CLEtXiDAymS/',
          img: '/imgs/page/top/instagram5.jpg',
          alt: '+81_kentaのインスタグラム５',
        },
        {
          href: 'https://www.instagram.com/p/CEMWNZXAaTG/',
          img: '/imgs/page/top/instagram6.jpg',
          alt: '+81_kentaのインスタグラム６',
        },
        {
          href: 'https://www.instagram.com/p/CCf3bqQAtT2/',
          img: '/imgs/page/top/instagram7.jpg',
          alt: '+81_kentaのインスタグラム７',
        },
        {
          href: 'https://www.instagram.com/p/CCfjaYRgyi7/',
          img: '/imgs/page/top/instagram8.jpg',
          alt: '+81_kentaのインスタグラム８',
        },
        {
          href: 'https://www.instagram.com/p/CCQ_rPtg7f5/',
          img: '/imgs/page/top/instagram9.jpg',
          alt: '+81_kentaのインスタグラム９',
        },
      ],

      shop: [
        {
          href:
            'https://amity-sensei.stores.jp/items/5cf4ab3aadb2a14721a54ad5/',
          img: '/imgs/page/top/amitysensei-top-store.jpg',
          alt: '+81_kentaのショップ１',
        },
        {
          href:
            'https://amity-sensei.stores.jp/items/5fc097ecdf5159329dd1fe35/',
          img: '/imgs/page/top/amitysensei-top-store.jpg',
          alt: '+81_kentaのショップ２',
        },
        {
          href:
            'https://amity-sensei.stores.jp/items/5cc02bf40b921104c346bcac/',
          img: '/imgs/page/top/amitysensei-top-store.jpg',
          alt: '+81_kentaのショップ３',
        },
        {
          href:
            'https://amity-sensei.stores.jp/items/5cc011ebadb2a137e4f32da4/',
          img: '/imgs/page/top/amitysensei-top-store.jpg',
          alt: '+81_kentaのショップ４',
        },
        {
          href:
            'https://amity-sensei.stores.jp/items/5e11a2fd6c7d632fbb60ff70/',
          img: '/imgs/page/top/amitysensei-top-store.jpg',
          alt: '+81_kentaのショップ５',
        },
        {
          href:
            'https://amity-sensei.stores.jp/items/5ed344bc55fa032e32c06a3e/',
          img: '/imgs/page/top/amitysensei-top-store.jpg',
          alt: '+81_kentaのショップ６',
        },
        {
          href:
            'https://amity-sensei.stores.jp/items/5ed3447e34ef0138b5594215/',
          img: '/imgs/page/top/amitysensei-top-store.jpg',
          alt: '+81_kentaのショップ７',
        },
        {
          href:
            'https://amity-sensei.stores.jp/items/5eb3aae972b9116c9aa6c706/',
          img: '/imgs/page/top/amitysensei-top-store.jpg',
          alt: '+81_kentaのショップ８',
        },
        {
          href:
            'https://amity-sensei.stores.jp/items/5eb3b35855fa0345bb05c89f/',
          img: '/imgs/page/top/amitysensei-top-store.jpg',
          alt: '+81_kentaのショップ９',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.section-top-sns {
  @include mq(sm) {
    padding: 0;
  }

  > .container {
    display: flex;
    justify-content: space-between;
    padding-top: 88px;

    @include mq(sm) {
      display: block;
      padding-top: 0;
    }

    > .sns {
      width: 49%;
      max-width: 520px;
      padding: 0 24px;
      background-color: var(--color-bg-gray);

      @include mq(sm) {
        width: 100%;
        max-width: none;
        padding: 0 26px;
      }

      > .container {
        max-width: 432px;
        padding-top: 40px;
        padding-bottom: 56px;

        @include mq(sm) {
          max-width: 360px;
          padding-top: 64px;
          padding-bottom: 80px;
        }

        > .sns-ttl {
          display: flex;
          justify-content: center;

          > .sns-icon {
            width: 48px;

            @include mq(sm) {
              width: 40px;
            }
          }
        }

        > .list {
          margin-top: 32px;

          @include mq(sm) {
            margin-top: 24px;
          }
        }

        > .button {
          max-width: 200px;
          margin: 32px auto 0;
        }
      }

      &.sns-shop {
        @include mq(sm) {
          background-color: transparent;
        }

        > .container {
          @include mq(sm) {
            padding-bottom: 0;
          }
        }
      }
    }
  }
}
</style>
