# Nuxt.jsビギナーズガイド
> Vue.jsベースのフレームワークによるシングルページアプリケーション開発

## 目次

1. Nuxt.jsの概要
    1. モダンフロントエンドのイマ
        - いわゆる「フロントエンド」について
        - 安定したフロントエンドJavaScriptに求められるもの
        - Nuxt.jsとこれからのWebアプリケーション開発
    2. Nuxt.jsとは
        - Next.jsをリスペクトして生まれたNuxt.js
        - Nuxt.jsの特徴と機能
        - 多くの企業に愛されるNuxt.js
    3. Nuxt.jsがもたらすもの
        - Nuix.jsがフロントエンドにもたらす「規約」
    4. Nuxt.jsがマッチするプロジェクトやシチュエーション
        - Nuxt.jsを採用すべきシチュエーション
        - Nuxt.jsを採用すべきでないシチュエーション
2. Nuxt.jsによるシンプルなアプリケーション開発
    1. 開発するアプリケーションについて
        - 開発するアプリケーションの概要
        - 完成品のサンプルリポジトリについて
    2. 事前準備
        - Node.jsとYarnによる必須環境の導入
        - 推奨ツール「direnv」の導入
    3. Vue CLIによるアプリケーションひな形の作成
    4. はじめてのページ作成と「Hello, world」
    5. Nuxt.jsプロジェクトの構成について
        - assetsディレクトリ
        - componentsディレクトリ
        - pagesディレクトリ
        - staticディレクトリ
        - storeディレクトリ
    6. ルーティングとページコンポーネントの作成
    7. 動的ルーティングのコンテンツの出し分け
    8. axios-modeleによる外部リソースの取得
        - Axios-moduleの導入
        - Qiita APIへのアクセス
    9. 認証情報を付与したAPIリクエスト
        - Qiita APIの制限
        - Qiitaのアクセストークンの取得
        - 認証情報の設定
    10. 非同期通信を含むコンテンツのサーバーサイドレンダリング
    11. ルーティングと組み合わせたサーバーサイドレンダリング
    12. head()によるHTMLメタの設定
        - 共通タイトルの設定
        - ページごとのタイトルの設定
    13. ロジックのVueストアへの移譲
    14. 完成品のリポジトリと改変について
3. Nuxt.jsの機能の活用
    1. layoutsディレクトリによるレイアウトの共通化
        - レイアウトの構築機能について
        - レイアウトのルールとdefault vueの編集
        - 複数のレイアウトの管理
        - 今見ているページのレイアウトはVue.js Devtoolsでも確認可能
        - レイアウトファイル設計のベスト・プラクティス
    2. Nuxt.jsのライフサイクル
    3. middlewareによるグローバルなフックの登録
        - Middlewareを利用した認証の必要なルーティングの実装
        - ミドルウェアの作成とグローバルへの登録
        - ミドルウェアへの認証の実装
        - ミドルウェアの魅力と注意点について
    4. プラグインによるVue.jsプラグイン資産の有効活用
        - プラグインの実装と登録
    5. Vuexのモジュールモードを活用したオートローディング
        - モジュールモードの仕組みについて
    6. より多くの機能を知りたい場合は
4. 中規模以上の開発を意識したNuxt.jsによるWebアプリケーション開発
    1. 本章で開発するもの
        - 開発するアプリケーションについて
        - 利用するAPIサーバーについて
        - 完成品のサンプルについて
    2. Firebaseのセットアップ
        - Firebaseプロジェクトの作成
        - Realtime Databaseのセットアップ
    3. プロジェクトのスキャフォールディング
        - Create-nuxt-appによるプロジェクト作成
        - プロジェクトディレクトリの移動
        - APIサーバーの設定
    4. ユーザーインターフェイスの構築
        - 共通レイアウトの作成
        - ログインページの作成
        - 投稿一覧ページ
    5. ログイン機能の実装
        - ユーザーのリソース構造について
        - アカウント登録とログイン機能処理の実装
        - ログイン情報の永続化
        - グローバルナビゲーションでのログイン確認
    6. 基本的な投稿機能の実装
        - 投稿データのエンティティについて
        - 投稿ページの作成
        - 投稿機能のロジック実装
        - 投稿一覧ページの作成
        - 投稿個別ページの作成
    7. ユーザーページの実装
        - usersモジュールの作成と実装
        - マイページのコーディングと実装
    8. 「いいね」機能の実装
        - 「いいね」の持ちうる構造
        - 「いいね」情報の格納先とモジュール
        - 「いいね」のロジック実装
        - 「いいね」の表示機能の実装
        - キャッシュを考慮した「いいね」設計
    9. おわりに
        - 発展的な要素について
5. Nuxt.jsアプリケーションのテスティング
    1. フロントエンドにおけるテストの必要性
        - フロントエンドのテストの難しさと民主化
        - 依然として残るテストの課題
        - どこまでテストを書くか
        - 本章で取り扱う範囲について
    2. Jestの紹介と導入
        - サンプルリポジトリについて
        - Facebook製の高機能テストランナーJest
        - Jest環境の導入
    3. Jestを用いたJavaScriptのテスティング
        - テスト対象となるVuexストアの実装
        - Vue/VuexテストのためのVue Test Utilsの導入
        - Vue/Vuexストアのテストコードの記述
        - Babelを利用したモダンな記述が可能なテスト環境の構築
        - モダンJavaScriptを利用したテストの記述
    4. Vue/Nuxt.jsの特有のテスト環境について
        - Vue.js/Nuxt.js向けのエイリアスの登録
        - Vue.js向けのJestプラグインの導入
        - Vueコンポーネントの振る舞い駆動のテスト
        - コンポーネント出力結果のスナップショットテスト
    5. フロントエンドのテストを腐らせないために
        - カバレッジレポートの出力
        - 継続的インテグレーション環境の構築
6. アプリケーションのデプロイと運用
    1. Nuxt.jsアプリケーションの３つのデプロイ方法
        - それぞれのモードの簡単な比較
        - デフォルトのUniversalモード
        - Webサイトなどに最適なgenerateモード
        - 最もシンプルなgenerateモード
    2. SSRの場合に利用できるデプロイ先の候補
        - Heroku
        - AWS Lambda + API Gateway
        - Google App Engine (Standard)
    3. 静的サイトのデプロイ先の候補
        - 最もモダンな静的ホスティングサイトNetlify
        - Amazon S3 + CloudFrontによる堅牢なホスティング
    4. メンテナンスしやすいNuxt.jsアプリケーションのインフラのために
7. プラグインとモジュール、エコシステムの開発・貢献
    1. 開発をさらに効率的にするNuxt.js謹製モジュール
        - サンプルプロジェクトについて
        - Axios-moduleによるプロキシ
        - 公式モジュールによるPWA対応
    2. サードパーティモジュールの探し方
    3. 自作プラグイン・モジュールの開発
        - サンプルとして開発するモジュール
        - モジュール用のプロジェクトへの作成
        - モジュールの開発規約
        - モジュールの開発環境の構築
        - モジュールへの機能実装
    4. パッケージのNPMへの公開
        - Standard-versionを利用したバージョニング
        - NPMへのpublish
8. 最新情報のキャッチアップのススメ
    1. 日本語に対応した情報収集
        - ７カ国語に翻訳されるNuxt.jsドキュメント
        - Vue.jsの日本語公式Slackの活用
    2. 英語ベースの情報収集環境
        - 公式Twitterアカウントによる開発情報のキャッチアップ
        - CMTYによるオフィシャルなコミュニケーション
        - 公式Discordによるラフなコミュニケーション
        - どうしてもない情報はソースコードへ
