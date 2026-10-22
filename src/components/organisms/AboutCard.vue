<script setup lang="ts">
import BackButton from '../atoms/BackButton.vue'
import SectionTitle from '../atoms/SectionTitle.vue'
import ContentList from '../molecules/ContentList.vue'

const emit = defineEmits<(e: 'navigate', action: string) => void>()
</script>

<template>
  <div class="about-card">
    <div class="card-inner">
      <!-- Top Back Link -->
      <BackButton @click="emit('navigate', 'home')" />

      <!-- 所属 -->
      <SectionTitle title="所属" />
      <ContentList variant="primary">
        <li><p>株式会社ひなセンス</p></li>
        <li><p>株式会社PLETECH</p></li>
      </ContentList>

      <!-- 作ったもの -->
      <SectionTitle title="作ったもの" />
      <ContentList variant="primary">
        <li><p>VRChat</p></li>
      </ContentList>
      <ContentList variant="secondary">
        <li>
          <p><a href="https://booth.pm/ja/items/1337219" target="_blank">VRChatModeSwitcher</a>(C#/.NET Framework)</p>
        </li>
        <li>
          <p><a href="https://github.com/hinanoaira/lilToon-emissivefreak" target="_blank">lilToon EmissiveFreak</a>(HLSL/Unity Shader, C#/Unity)</p>
        </li>
        <li>
          <p>でかプコンシェルジュ(Electron,TypeScript/Vue3)</p>
        </li>
        <li>
          <p>ToNおたすけNPC(Unity, HLSL/Unity Shader)</p>
        </li>
        <li>
          <p>イベント用ゲームワールド SummerSweet！杉の木伐採まつり(Unity, UdonSharp/Udon)</p>
        </li>
      </ContentList>

      <ContentList variant="primary">
        <li><p>neosVR</p></li>
      </ContentList>
      <ContentList variant="secondary">
        <li><p>NameBadgeEditor(LogiX)</p></li>
        <li><p>ShelfBangle(LogiX)</p></li>
        <li><p>neosCommentGenerator(C#/.NET Framework, LogiX)</p></li>
        <li><p>neosMultiCommentViewer(C#/.NET Framework, LogiX)</p></li>
        <li><p>ネオ麻雀 API(JavaScript/Express)</p></li>
        <li><p>Neos 銀行(TypeScript/NestJS)</p></li>
      </ContentList>

      <ContentList variant="primary">
        <li><p>その他趣味</p></li>
      </ContentList>
      <ContentList variant="secondary">
        <li><p>DiscordBot(C#/.NET ,TypeScript)</p></li>
        <li><p>MusicBee プラグイン(Visual C++)</p></li>
        <li><p>Misskey Disocrdを使ったSSO実装(TypeScript/Vue3)</p></li>
        <li>
          <p><a href="https://hns.jp/ipv6" target="_blank">test-ipv6.hns.jp</a></p>
        </li>
      </ContentList>

      <ContentList variant="primary">
        <li><p>お仕事</p></li>
      </ContentList>
      <ContentList variant="secondary">
        <li><p>ネットリサーチ関連サービス フロントエンド開発(Dart/Flutter)</p></li>
        <li><p>配信ツール(C#/Unity, C#/.NET Core)</p></li>
        <li><p>VRChat OBS 連携ソフトウェア プラグイン開発(C#/.NET Core)</p></li>
        <li><p>自社制作ゲームエンジンデバッグ用ツール(TypeScript/Vue3)</p></li>
        <li><p>Github Actions/AWS自動テスト・デプロイ機構</p></li>
        <li><p>デバッグ用AIツールMachineHeads(Python,MachinHeadsノーコード)</p></li>
        <li><p>Unity[禁則事項]([禁則事項])</p></li>
      </ContentList>

      <!-- いまやっていること -->
      <SectionTitle title="いまやっていること" />
      <ContentList variant="primary">
        <li><p>VRChat</p></li>
      </ContentList>
      <ContentList variant="secondary">
        <li><p>LPK48 メンバー</p></li>
        <li><p>SummerSweet! メンバー</p></li>
        <li>
          <p>Castrato Developer(<a href="https://twitter.com/traviata_cat" target="_blank">トラヴィ</a>)</p>
        </li>
      </ContentList>

      <ContentList variant="primary">
        <li><p>resonite</p></li>
      </ContentList>
      <ContentList variant="secondary">
        <li><p>resonite メンタートレーナー</p></li>
      </ContentList>

      <ContentList variant="primary">
        <li><p>にりらみすきー部</p></li>
      </ContentList>
      <ContentList variant="secondary">
        <li>
          <p><a href="https://misskey.niri.la/@hinanoaira" target="_blank">でぺろっぱー</a></p>
        </li>
      </ContentList>

      <ContentList variant="primary">
        <li><p>ArchLinux</p></li>
      </ContentList>
      <ContentList variant="secondary">
        <li>
          <p><a href="https://aur.archlinux.org/account/hinanoaira" target="_blank">AURメンテナー</a></p>
        </li>
      </ContentList>

      <ContentList variant="primary">
        <li><p>その他</p></li>
      </ContentList>
      <ContentList variant="secondary">
        <li><p>TOKYOスマホサポーター 認定サポーター</p></li>
      </ContentList>

      <!-- 過去にやっていたこと / 実績 -->
      <SectionTitle title="過去にやっていたこと / 実績" />
      <ContentList variant="primary">
        <li><p>minecraft</p></li>
      </ContentList>
      <ContentList variant="secondary">
        <li><p>サーバー運営 インフラ維持,プラグイン開発(最大規模 同接 50 人)</p></li>
        <li><p>ほげ.class メンバー</p></li>
        <li><p>一般社団法人 BridgeKnitworks 設立理事</p></li>
        <li><p>ニコニコ超会議 超マイクラひろば 出展</p></li>
      </ContentList>

      <ContentList variant="primary">
        <li><p>VRChat</p></li>
      </ContentList>
      <ContentList variant="secondary">
        <li><p>VR 麻雀倶楽部 リーダー</p></li>
      </ContentList>

      <ContentList variant="primary">
        <li><p>neosVR</p></li>
      </ContentList>
      <ContentList variant="secondary">
        <li><p>neosVR メンター</p></li>
        <li><p>VR アミューズメント NEOGRAND/CROWN スタッフ</p></li>
        <li><p>VR アミューズメント HinassQueen 主催</p></li>
        <li><p>NeosFesta3 出展</p></li>
        <li><p>NeosFesta4 アンバサダー就任</p></li>
        <li><p>Metaverse Maker Conpetition 2021 優勝</p></li>
        <li><p>Metaverse Maker Conpetition 2022 優秀賞</p></li>
      </ContentList>

      <ContentList variant="primary">
        <li><p>Virtual Market</p></li>
      </ContentList>
      <ContentList variant="secondary">
        <li><p>Vket2023Summer</p></li>
      </ContentList>
      <ContentList variant="tertiary">
        <li><p>Vketスタッフ</p></li>
        <li><p>VketRealスタッフ</p></li>
      </ContentList>
      <ContentList variant="secondary">
        <li><p>Vket2023Winter</p></li>
      </ContentList>
      <ContentList variant="tertiary">
        <li><p>Vket出店</p></li>
        <li><p>Vketスタッフ</p></li>
        <li><p>VketRealスタッフ</p></li>
      </ContentList>
      <ContentList variant="secondary">
        <li><p>Vket2024Summer</p></li>
      </ContentList>
      <ContentList variant="tertiary">
        <li><p>Vket出店</p></li>
        <li><p>Vketスタッフ</p></li>
      </ContentList>
      <ContentList variant="secondary">
        <li><p>Vket2024Winter</p></li>
      </ContentList>
      <ContentList variant="tertiary">
        <li><p>Vketスタッフ</p></li>
      </ContentList>

      <!-- スキル / 知識 -->
      <SectionTitle title="スキル / 知識" />
      <ContentList variant="primary">
        <li><p>言語</p></li>
      </ContentList>
      <ContentList variant="secondary">
        <li><p>C#</p></li>
        <li><p>Java</p></li>
        <li><p>JavaScript / TypeScript</p></li>
        <li><p>Dart</p></li>
        <li><p>PHP</p></li>
        <li><p>HLSL / GLSL</p></li>
      </ContentList>

      <ContentList variant="primary">
        <li><p>開発環境 / フレームワーク</p></li>
      </ContentList>
      <ContentList variant="secondary">
        <li><p>.NET / .NET Core/ .NET Framework</p></li>
        <li><p>Flutter</p></li>
        <li><p>React</p></li>
        <li><p>next.js</p></li>
        <li><p>NestJS</p></li>
        <li><p>Vue2 / Vue3</p></li>
        <li><p>Electron</p></li>
      </ContentList>

      <ContentList variant="primary">
        <li><p>クエリ言語</p></li>
      </ContentList>
      <ContentList variant="secondary">
        <li><p>MySQL / PostgreSQL</p></li>
        <li><p>GraphQL</p></li>
      </ContentList>

      <ContentList variant="primary">
        <li><p>クラウド</p></li>
      </ContentList>
      <ContentList variant="secondary">
        <li><p>Amazon AWS</p></li>
        <li><p>Google Cloud Platform</p></li>
        <li><p>Microsoft Azure</p></li>
        <li><p>CloudFlare</p></li>
        <li><p>WebArena Indigo</p></li>
      </ContentList>

      <ContentList variant="primary">
        <li><p>サーバー OS</p></li>
      </ContentList>
      <ContentList variant="secondary">
        <li><p>Windows Server</p></li>
        <li><p>CentOS</p></li>
        <li><p>Ubuntu</p></li>
        <li><p>Debian</p></li>
        <li><p>Arch Linux</p></li>
      </ContentList>

      <ContentList variant="primary">
        <li><p>インフラ / その他</p></li>
      </ContentList>
      <ContentList variant="secondary">
        <li><p>ネットワーク構築(Ethernet/IP)</p></li>
        <li><p>トンネル技術(IPIP, IPSec, OpenVPN, SoftEther, PPPoE)</p></li>
        <li><p>動的ルーティング技術(BGP)</p></li>
        <li><p>DNS / DNSSEC / DNS over HTTPS</p></li>
        <li><p>公開鍵認証基盤(PKI)</p></li>
        <li><p>Gnu Privacy Guard</p></li>
        <li><p>Web(Apache, nginx)</p></li>
        <li><p>メールサービス</p></li>
        <li><p>仮想化プラットフォーム(Hyper-V, Proxmox, KVM)</p></li>
        <li><p>コンテナ技術(Docker, LXC)</p></li>
        <li><p>経理(freee会計)</p></li>
      </ContentList>

      <!-- 職歴(業託含む) -->
      <SectionTitle title="職歴(業託含む)" />
      <ContentList variant="primary">
        <li><p>イオン千歳店</p></li>
        <li><p>千歳総合メンテサービス有限会社</p></li>
        <li><p>セブンイレブン千歳白樺店</p></li>
        <li><p>[禁則事項]</p></li>
        <li><p>株式会社HIKKY</p></li>
        <li><p>[禁則事項]</p></li>
      </ContentList>

      <!-- Bottom Back Link -->
      <BackButton @click="emit('navigate', 'home')" />
    </div>
  </div>
</template>

<style scoped>
.about-card {
  width: 100%;
  animation: fadeUp 0.6s cubic-bezier(0.16, 1, 0.3, 1) both;
}

.card-inner {
  width: 37rem;
  max-width: 100%;
  margin: 0 auto;
  background-image: linear-gradient(45deg, rgba(0, 0, 0, 0.078) 0%, rgba(0, 0, 0, 0.271) 100%);
  background-position: 0% 0%;
  background-repeat: repeat;
  background-size: cover;
  -webkit-backdrop-filter: blur(0.3rem);
  backdrop-filter: blur(0.3rem);
  border: 1px solid rgba(255, 255, 255, 0.271);
  border-radius: 1.25rem;
  padding: 2rem;
  box-sizing: border-box;
}

@keyframes fadeUp {
  0% {
    opacity: 0;
    transform: translateY(1.5rem);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

@media (max-width: 480px) {
  .card-inner {
    padding: 1.75rem 1.25rem;
  }
}
</style>

