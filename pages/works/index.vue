<template>
  <div class="flex justify-center flex-wrap">
    <!-- anywhere-paint -->
    <div class="max-w-sm rounded overflow-hidden shadow-lg m-6">
      <a href="https://tunamagur0.github.io/anywhere-paint-sample/">
        <div class="flex justify-center p-2 hover:shadow-md">
          <img src="~/assets/img/anywhere-paint.png" alt="anywhere-paint" />
        </div>
      </a>
      <div class="px-6 py-4">
        <div class="font-bold text-xl mb-2">anywhere-paint</div>
        <div class="text-gray-700 text-base">
          お絵かきアプリを簡単に作るためのTypeScript製ライブラリです。<br />
          レイヤー機能やUndo,Redo機能も備えています。
          <a
            class="text-blue-500 hover:text-blue-800 hover:underline"
            href="https://www.npmjs.com/package/anywhere-paint"
            >npm.js</a
          >
          よりインストールすることができます。<br />
        </div>
      </div>
      <div class="px-6 py-4">
        <a class="px-2" href="https://www.github.com/tunamagur0/anywhere-paint"
          ><fa :icon="faGithub"
        /></a>
        <a class="px-2" href="https://www.npmjs.com/package/anywhere-paint"
          ><fa :icon="faNpm"
        /></a>
        <a
          class="text-blue-500 hover:text-blue-800 hover:underline px-2"
          href="https://tunamagur0.github.io/anywhere-paint-sample"
          >Sample</a
        >
      </div>
    </div>

    <!-- anywhere-paint-sample -->
    <div class="max-w-sm rounded overflow-hidden shadow-lg m-6">
      <a href="https://tunamagur0.github.io/anywhere-paint-sample/">
        <div class="flex justify-center p-2 hover:shadow-md">
          <img
            src="~/assets/img/anywhere-paint-sample.png"
            alt="anywhere-paint-sample"
          />
        </div>
      </a>
      <div class="px-6 py-4">
        <div class="font-bold text-xl mb-2">anywhere-paint-sample</div>
        <div class="text-gray-700 text-base">
          前に挙げたTypeScript製のライブラリ（anywhere-paint）を使用したサンプルです。Reactを使用しています。
        </div>
      </div>
      <div class="px-6 py-4 self-end">
        <a
          class="px-2"
          href="https://www.github.com/tunamagur0/anywhere-paint-sample"
          ><fa :icon="faGithub"
        /></a>
      </div>
    </div>

    <!-- interval-timer -->
    <div class="max-w-sm rounded overflow-hidden shadow-lg m-6">
      <div class="flex justify-center p-2 hover:shadow-md">
        <a href="https://interval-t-timer.web.app"
          ><img src="~/assets/img/interval-timer.png" alt="インターバルタイマー"
        /></a>
      </div>
      <div class="px-6 py-4">
        <div class="font-bold text-xl mb-2">インターバルタイマー</div>
        <div class="text-gray-700 text-base">
          Vue.jsを使ったインターバルタイマーです。トレーニングなどに使用できます。<br />
          PWAにも対応しているため、スマートフォンなどにインストールすることもできます。<br />
          アニメーションや効果音も自作しました。
        </div>
      </div>
      <div class="flex px-6 py-4">
        <a class="px-2" href="https://github.com/tunamagur0/interval-timer"
          ><fa :icon="faGithub"
        /></a>
        <a
          class="text-blue-500 hover:text-blue-800 hover:underline px-2"
          href="https://interval-t-timer.web.app"
          ><img
            src="~/assets/img/interval-timer-icon.png"
            alt="インターバルタイマー"
        /></a>
      </div>
    </div>

    <!-- 140editor -->
    <div class="max-w-sm rounded overflow-hidden shadow-lg m-6">
      <div class="flex justify-center p-2 hover:shadow-md">
        <a href="https://editor-140.herokuapp.com"
          ><img src="~/assets/img/editor-140.png" alt="文字数チェッカー"
        /></a>
      </div>
      <div class="px-6 py-4">
        <div class="font-bold text-xl mb-2">文字数チェッカー</div>
        <div class="text-gray-700 text-base">
          文字数を調べてクリップボートにコピーできるWebアプリケーションです。Vue.jsを使用しています。<br />
          コピーする際には入力した文字列に「（oo文字）」という文字列が付与され、この文字列を文字数として含むかどうかをオプションとして選択できます。
        </div>
      </div>
      <div class="flex px-6 py-4">
        <a class="px-2" href="https://github.com/tunamagur0/140checker"
          ><fa :icon="faGithub"
        /></a>
      </div>
    </div>

    <!-- desktop timer -->
    <div class="max-w-sm rounded overflow-hidden shadow-lg m-6">
      <div class="flex justify-center p-2 hover:shadow-md">
        <a href="https://github.com/tunamagur0/DesktopTimer"
          ><img src="~/assets/img/desktop-timer.png" alt="デスクトップクロック"
        /></a>
      </div>
      <div class="px-6 py-4">
        <div class="font-bold text-xl mb-2">デスクトップクロック</div>
        <div class="text-gray-700 text-base">
          デスクトップ上の好きな位置に配置でき、常に表示しておくことができる時計です。UWPアプリとなっており、C#でプログラミングされています。
        </div>
      </div>
      <div class="flex px-6 py-4">
        <a class="px-2" href="https://github.com/tunamagur0/DesktopTimer"
          ><fa :icon="faGithub"
        /></a>
      </div>
    </div>

    <!-- openvr driver -->
    <div class="max-w-sm rounded overflow-hidden shadow-lg m-6">
      <div class="flex justify-center p-2 hover:shadow-md">
        <a href="https://github.com/tunamagur0/my-openvr-driver"
          ><img src="~/assets/img/m5stack-openvr.gif" alt="m5stack openvr"
        /></a>
      </div>
      <div class="px-6 py-4">
        <div class="font-bold text-xl mb-2">M5Stackを用いたOpenVRドライバ</div>
        <div class="text-gray-700 text-base">
          M5Stackというマイコンモジュールをトラッキングデバイスとして利用する、OpenVRのドライバです。
          OpenVRのドライバなので、Steamのゲームにも使用する事ができます。<br />
          現時点では3DoFとなっており、回転運動しかトラッキングできませんが、前後左右の動きもトラッキングすることを目標としています。
        </div>
      </div>
      <div class="flex px-6 py-4">
        <a class="px-2" href="https://github.com/tunamagur0/my-openvr-driver"
          ><fa :icon="faGithub"
        /></a>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import { faGithub, faNpm } from '@fortawesome/free-brands-svg-icons';
export default Vue.extend({
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
