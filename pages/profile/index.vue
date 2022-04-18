<template>
  <div class="flex justify-center">
    <div class="w-2/3 sm:w-2/4 flex flex-col bg-gray-100">
      <div class="text-gray-700 text-center px-4 py-2 m-2">
        <h1 class="text-5xl font-bold">
          Profile
        </h1>
      </div>
      <div class="text-gray-700 text-left px-4 py-2 m-2 self-start">
        <div>
          <h2 class="text-3xl font-semibold">Infomation</h2>
          <ul class="list-disc text-lg">
            <li class="py-2">{{ age }}歳</li>
            <li class="py-2">
              出身：青森県
            </li>
            <li class="py-2">
              <ul>
                <li>AtCoder</li>
                <li>- Rating：緑</li>
                <li v-show="streak !== -1">- CurrentStreak：{{ streak }}日</li>
              </ul>
            </li>
            <li class="py-2">
              <nuxt-link
                to="/works"
                class="text-blue-500 hover:text-blue-800 hover:underline"
                >作ったもの</nuxt-link
              >
            </li>
          </ul>
        </div>
      </div>
      <div class="text-gray-700 text-left px-4 py-2 m-2 self-start">
        <div>
          <h2 class="text-3xl font-semibold">Skills</h2>
          <ul class="list-disc text-lg">
            <li class="py-2">
              <ul>
                <li>JavaScript, TypeScript</li>
                <li>- Vue.js</li>
                <li>- React</li>
                <li>- Nuxt.js</li>
                <li>- Next.js</li>
                <li class="text-gray-500">- Firebase</li>
                <li class="text-gray-500">- WebAssembly</li>
                <li class="text-gray-500">- WebGL</li>
              </ul>
            </li>
            <li class="py-2">
              <ul>
                <li>C++</li>
                <li>- 競技プログラミング</li>
              </ul>
            </li>
            <li class="py-2">
              <ul>
                <li>Python</li>
                <li>- Flask</li>
              </ul>
            </li>
            <li class="py-2">
              <ul>
                <li>MySQL</li>
              </ul>
            </li>
            <li class="py-2">
              <ul>
                <li>Go</li>
                <li>- 少し</li>
              </ul>
            </li>
            <li class="py-2">
              <ul>
                <li>Unity, C#</li>
                <li>- 少し</li>
              </ul>
            </li>
          </ul>
        </div>
      </div>
      <div class="text-gray-700 text-left px-4 py-2 m-2 self-start">
        <div>
          <h2 class="text-3xl font-semibold">Accounts</h2>
          <ul class="text-lg">
            <li>
              <a
                class="text-blue-500 hover:text-blue-800 hover:underline"
                href="https://github.com/tunamagur0"
                target="_blank"
                >Github</a
              >
            </li>
            <li>
              <a
                class="text-blue-500 hover:text-blue-800 hover:underline"
                href="https://atcoder.jp/users/tunamagur0"
                target="_blank"
                >AtCoder</a
              >
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import axios from 'axios';
import Vue from 'vue';

interface Streak {
  // eslint-disable-next-line camelcase
  user_id: string;
  streak: number;
}

interface AtcoderProblems {}

export default Vue.extend({
  async asyncData(): Promise<Streak> {
    const response = await axios
      .get<Streak[]>('https://kenkoooo.com/atcoder/resources/streaks.json')
      .catch((err) => {
        if (err) {
          console.log('cannot get streaks');
        }
      });
    if (!response) return { user_id: 'tunamagur0', streak: -1 };
    const myStreakData: Streak[] = response.data.filter(
      (val) => val.user_id === 'tunamagur0'
    );
    return myStreakData[0];
  },
  computed: {
    age(): number {
      const birthDay = new Date(1998, 3 - 1, 10);
      const today = new Date();
      const age = today.getFullYear() - birthDay.getFullYear();
      return new Date(
        today.getFullYear(),
        birthDay.getMonth(),
        birthDay.getDate()
      ) > today
        ? age - 1
        : age;
    }
  }
});
</script>
