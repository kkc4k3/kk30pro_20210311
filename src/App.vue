<template>
  <div class="main_layout">
    <h1 class="id">kk30pro@Twitter</h1>
    <section class="section">
      <div class="section_content">
        <h2 class="head">このアカウントの傾向</h2>
        <div class="content">
          <ul>
            <li>ゴールデンカムイ（だいたい）</li>
            <li>シャドーハウス（たまに）</li>
          </ul>
          <p>
            本誌の感想と申し訳程度に（めちゃくちゃ拗らせている）カップリング話<br />
            ネタバレの配慮はまったくありません<br />
            二次創作3DCGやイラスト、自作ねんどろ鯉登ドールやちゅんコレ鯉登の写真もたまに上がります
          </p>
          <p>
            性癖・解釈・話題・人間関係全て好き嫌いがものすごく激しいのと発信を見てもらえれば満足するタイプなので基本的にフォローは一切しない方針です<br />
            いいね・リツイート（引用含む）・リプライはFF外、カップリング問わず大歓迎なのでご自由にどうぞ（じゃなきゃ公開アカウントでやってないので……）<br />
            （僕が）見る人はめちゃくちゃ選ぶが自分が見られる分には特に気にしないという感じです
          </p>
          <p>
            例外としてグッズ交換の取引が成立した場合は一時的にフォローをさせていただきます、上記の方針があるため取引が終了次第フォローを外させていただきますがご了承いただけますと幸いです
          </p>
        </div>
      </div>
    </section>
    <section class="section">
      <div class="section_content">
        <h2 class="head">カップリングの好みとか性癖</h2>
        <div class="content">
          <p>
            以下ほとんどゴカムの話です<br />
            基本方針としては以下
          </p>
          <ul>
            <li>鯉登右</li>
            <li><strong>鯉月を除く</strong>月島右</li>
            <li><s>月島と鯉登は百合</s></li>
          </ul>
          <p>
            BLカップリング（ヘテロカップリングは平気）における鯉登左が苦手なこと以外は明確な地雷はないです
            ただ明文化しにくい解釈とか細かい描写にめちゃくちゃこだわりが強いので選り好みはめちゃくちゃします、地雷レベルでダメなのがこれだけというのが近いかも
          </p>
          <p>
            カップリング単位だと月鯉/鶴月/鶴鯉/門キラあたりが好きでわりかし話題がよく出ます<br />最近は菊杉も少し気になっている
          </p>
          <p>
            エロネタも苦手じゃないむしろ大好きですが基本的にモブエロ至高主義でカップリングにドエロいのはそこまで求めてないです（見れないわけではない）<br />
            完全に個人的な気持ちの問題でエロネタを大っぴらにするのが憚られる（他人のそれを見る分には特に気にはしてない）のであまりTwitterではそういうネタを投稿していませんが、もしかしたら別途そういう場を今後作る可能性はあるかもしれません（Misskey（後述）では稀にそういう話をCWつけてしてるときもあります）
          </p>
          <p>
            <span class="hide_toggle" @click="nsfwToggle">
              個人的な好みのエロネタとしては<br />
              （{{ nsfwNote }}）
            </span>
            <br />
            <span v-show="nsfwShow">
              月島と鯉登がモブ上官になんかしらの手段で催眠をかけられおちんぽ大好き❤上官殿のおちんぽにご奉仕することこそ軍人の至上の喜びです❤状態にされて延々とちんぽの悦びを教え込まれた結果、最終的に2人揃って上層部専用オナホにされる、みたいなやつが好きなんですがあんまりないですね……
            </span>
          </p>
          <p>シャドーハウスはルイーズが好きです</p>
        </div>
      </div>
    </section>
    <section class="section">
      <div class="section_content">
        <h2 class="head">アカウントの主について</h2>
        <div class="content">
          <p>
            名前はkkcake（けーけーけーき）です<br />
            平成一桁生まれのアラサー、2021年現在ギリギリ20代です
          </p>
          <p>
            自然と遠出が好き、原付ツーリングによく行くけど本当は中型二輪免許がほしい<br />
            最近はDIYに興味がある
          </p>
          <p>Vue.jsを主に書いて生活しています</p>
          <p>
            普段はTwitterではなくMisskeyというSNSの<a
              href="https://ms.kvche.ch/@kkcake"
              target="_blank"
              >自鯖</a
            >にいます、そちらの方がより踏み込んだ話をしている場合もあるので物好きな方はどうぞ（ただし雑多垢なので関係ない話題も多いです、むしろ関係ない話題のほうがメインです）
          </p>
          <p>
            一応名前そのままIDの<a
              href="https://twitter.com/kkcake"
              target="_blank"
              >Twitter本垢</a
            >も存在しますがここ最近は滅多にログインしてません
          </p>
        </div>
      </div>
    </section>
  </div>
</template>

<script lang="ts">
import { computed, defineComponent, ref } from "vue"

export default defineComponent({
  name: "App",
  components: {},
  setup() {
    let nsfwShow = ref(false)
    const nsfwToggle = () => {
      nsfwShow.value = !nsfwShow.value
    }

    const nsfwNote = computed(() => {
      if (nsfwShow.value) {
        return "再度クリックで閉じます"
      } else {
        return "クリックで開きます、人を選ぶと思うので何でも許せる人だけ見てね"
      }
    })

    return {
      nsfwShow,
      nsfwToggle,
      nsfwNote,
    }
  },
})
</script>

<style lang="scss">
@import "~/assets/css/destyle.css";
@import url("https://fonts.googleapis.com/css2?family=M+PLUS+Rounded+1c:wght@400;700&display=swap");
$space_s: 15px;
$space_m: 30px;
$space_l: 60px;
body {
  min-height: 100vh;
  width: 100%;
  background: #b2dfdb;
  color: #263238;
  font-family: "M PLUS Rounded 1c", sans-serif;
}

.main_layout {
  padding: $space_l $space_s;
  font-size: 15px;
  max-width: 640px;
  width: 100%;
  margin: 0 auto;

  > .id {
    font-size: 30px;
    font-weight: bold;
  }

  > .section {
    margin-top: $space_m;
  }
}

.section_content {
  > .head {
    font-weight: bold;
    font-size: 17px;
  }
  > .content {
    > p,
    > ul {
      margin-top: $space_s;
      line-height: 1.5;

      > a {
        color: #00796b;
        text-decoration: underline;
      }
    }

    > ul {
      margin-left: $space_m;
      list-style-type: disc;
    }
  }
}

.hide_toggle {
  cursor: pointer;
  user-select: none;
}
</style>
