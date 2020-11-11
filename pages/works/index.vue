<template>
  <div class="flex justify-center flex-wrap">
    <!-- anywhere-paint -->
    <card>
      <template v-slot:image>
        <a
          href="https://tunamagur0.github.io/anywhere-paint-sample/"
          target="_blank"
        >
          <div class="flex justify-center p-2 hover:shadow-md">
            <img src="~/assets/img/anywhere-paint.png" alt="anywhere-paint" />
          </div>
        </a>
      </template>
      <template v-slot:title>anywhere-paint</template>
      <template v-slot:content
        >お絵かきアプリを簡単に作るためのTypeScript製ライブラリです。<br />
        レイヤー機能やUndo,Redo機能も備えています。
        <a
          class="text-blue-500 hover:text-blue-800 hover:underline"
          href="https://www.npmjs.com/package/anywhere-paint"
          target="_blank"
          >npmjs.com</a
        >
        よりインストールすることができます。<br
      /></template>
      <template v-slot:icons
        ><a
          class="px-2"
          href="https://www.github.com/tunamagur0/anywhere-paint"
          target="_blank"
          ><fa class="text-xl" :icon="faGithub"
        /></a>
        <a
          class="px-2"
          href="https://www.npmjs.com/package/anywhere-paint"
          target="_blank"
          ><fa class="text-xl" :icon="faNpm"
        /></a>
        <a
          class="text-blue-500 hover:text-blue-800 hover:underline px-2"
          href="https://tunamagur0.github.io/anywhere-paint-sample"
          target="_blank"
          >Sample</a
        ></template
      >
    </card>

    <!-- anywhere-paint-sample -->
    <card>
      <template v-slot:image>
        <a
          href="https://tunamagur0.github.io/anywhere-paint-sample/"
          target="_blank"
        >
          <div class="flex justify-center p-2 hover:shadow-md">
            <img
              src="~/assets/img/anywhere-paint-sample.png"
              alt="anywhere-paint-sample"
            />
          </div>
        </a>
      </template>
      <template v-slot:title>anywhere-paint-sample</template>
      <template v-slot:content>
        前に挙げたTypeScript製のライブラリ（anywhere-paint）を使用したサンプルです。Reactを使用しています。
      </template>
      <template v-slot:icons>
        <a
          class="px-2"
          href="https://www.github.com/tunamagur0/anywhere-paint-sample"
          target="_blank"
          ><fa class="text-xl" :icon="faGithub"
        /></a>
      </template>
    </card>

    <!-- interval-timer -->
    <card>
      <template v-slot:image>
        <a href="https://interval-t-timer.web.app" target="_blank"
          ><img src="~/assets/img/interval-timer.png" alt="インターバルタイマー"
        /></a>
      </template>
      <template v-slot:title>
        インターバルタイマー
      </template>
      <template v-slot:content>
        Vue.jsを使ったインターバルタイマーです。トレーニングなどに使用できます。<br />
        PWAにも対応しているため、スマートフォンなどにインストールすることもできます。<br />
        アニメーションや効果音も自作しました。
      </template>
      <template v-slot:icons>
        <a
          class="px-2"
          href="https://github.com/tunamagur0/interval-timer"
          target="_blank"
          ><fa class="text-xl" :icon="faGithub"
        /></a>
        <a
          class="text-blue-500 hover:text-blue-800 hover:underline px-2"
          href="https://interval-t-timer.web.app"
          target="_blank"
          ><img
            src="~/assets/img/interval-timer-icon.png"
            alt="インターバルタイマー"
        /></a>
      </template>
    </card>

    <!-- openvr driver -->
    <card>
      <template v-slot:image>
        <a href="https://github.com/tunamagur0/my-openvr-driver" target="_blank"
          ><img src="~/assets/img/m5stack-openvr.gif" alt="m5stack openvr"
        /></a>
      </template>
      <template v-slot:title>M5Stackを用いたOpenVRドライバ</template>
      <template v-slot:content>
        M5Stackというマイコンモジュールをトラッキングデバイスとして利用する、OpenVRのドライバです。
        OpenVRのドライバなので、Steamのゲームにも使用する事ができます。<br />
        現時点では3DoFとなっており、回転運動しかトラッキングできませんが、前後左右の動きもトラッキングすることを目標としています。
      </template>
      <template v-slot:icons
        ><a
          class="px-2"
          href="https://github.com/tunamagur0/my-openvr-driver"
          target="_blank"
          ><fa class="text-xl" :icon="faGithub"/></a
      ></template>
    </card>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import { faGithub, faNpm } from '@fortawesome/free-brands-svg-icons';
import Card from '~/components/Card.vue';

export default Vue.extend({
  components: {
    Card
  },
  computed: {
    faGithub() {
      return faGithub;
    },
    faNpm() {
      return faNpm;
    }
  }
});
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
  @apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
