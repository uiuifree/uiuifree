# uiuifree — Rust libraries for Japanese open data and SEO

**Web Backend Developer / Engineer** based in Japan 🇯🇵

I love Rust. I publish Rust crates on [crates.io](https://crates.io/users/uiuifree) for Japanese open data (corporate number, gBizINFO, J-Quants, minimum wage, postal codes, reverse geocoding), Japanese text processing for job data, Google / SEO APIs, and API clients (OpenAI, LINE, Slack). Repositories are usually named `rust-<crate-name>`.

Rustが好きです。日本のオープンデータ（法人番号・gBizINFO・J-Quants・最低賃金・郵便番号・逆ジオコーディング）、求人データ向けの日本語テキスト処理、Google / SEO 系API、各種APIクライアントのRustクレートをcrates.ioに公開しています。

[![GitHub followers](https://img.shields.io/github/followers/uiuifree?style=social)](https://github.com/uiuifree)
[![X (Twitter)](https://img.shields.io/badge/-@uiuifree-1DA1F2?style=flat&logo=x&logoColor=white)](https://x.com/uiuifree)
[![Zenn](https://img.shields.io/badge/-Zenn-3EA8FF?style=flat&logo=zenn&logoColor=white)](https://zenn.dev/uiuifree)

## 🛠 Tech Stack

![Rust](https://img.shields.io/badge/-Rust-000000?style=flat&logo=rust&logoColor=white)
![Go](https://img.shields.io/badge/-Go-00ADD8?style=flat&logo=go&logoColor=white)
![PHP](https://img.shields.io/badge/-PHP-777BB4?style=flat&logo=php&logoColor=white)
![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Vue.js](https://img.shields.io/badge/-Vue.js-4FC08D?style=flat&logo=vuedotjs&logoColor=white)
![Elasticsearch](https://img.shields.io/badge/-Elasticsearch-005571?style=flat&logo=elasticsearch&logoColor=white)
![Google Cloud](https://img.shields.io/badge/-Google%20Cloud-4285F4?style=flat&logo=googlecloud&logoColor=white)

## 🦀 Rust Libraries

All crates are published on crates.io. Crate name links to the GitHub repository.

### 🗾 Japan Data

| Crate | Version | Description |
|-------|---------|-------------|
| [houjin-bangou-api](https://github.com/uiuifree/rust-houjin-bangou-api) | [![Crates.io](https://img.shields.io/crates/v/houjin-bangou-api.svg)](https://crates.io/crates/houjin-bangou-api) | Async Rust client for the Japan NTA Corporate Number (Houjin Bangou) Web-API v4: lookup by corporate number, name search, date-range diff sync, trade-name / address change history / 国税庁 法人番号システム Web-API (Ver.4) の非同期Rustクライアント。法人番号検索・法人名検索・期間指定の差分取得・商号／所在地の変更履歴 |
| [gbiz-info-api](https://github.com/uiuifree/rust-gbiz-info-api) | [![Crates.io](https://img.shields.io/crates/v/gbiz-info-api.svg)](https://crates.io/crates/gbiz-info-api) | Rust client for the gBizINFO REST API v2 (corporate data published by METI) / 経済産業省 gBizINFO REST API (v2) のRustクライアント |
| [jquants-api](https://github.com/uiuifree/rust-jquants-api) | [![Crates.io](https://img.shields.io/crates/v/jquants-api.svg)](https://crates.io/crates/jquants-api) | Unofficial async Rust client for the J-Quants API v2 (Japanese stock market data by JPX) / J-Quants API v2（JPXが提供する日本株データ）の非公式・非同期Rustクライアント |
| [minimum_wage_jp](https://github.com/uiuifree/rust-minimum-wage-jp) | [![Crates.io](https://img.shields.io/crates/v/minimum_wage_jp.svg)](https://crates.io/crates/minimum_wage_jp) | Japan's regional minimum wage by prefecture: rate for any date and compliance check with shortage amount. MHLW data embedded, no network access / 都道府県別の最低賃金を日付指定で取得し、時給が満たすか判定（不足額つき）。厚労省データ同梱・通信不要 |
| [jp-address-search](https://github.com/uiuifree/rust-jp-address-search) | [![Crates.io](https://img.shields.io/crates/v/jp-address-search.svg)](https://crates.io/crates/jp-address-search) | Fast, zero-dependency Japanese address search: postal code to address, prefecture / municipality master data, city latitude/longitude. Data bundled / 郵便番号→住所、都道府県・市区町村マスタ、市区町村の緯度経度。依存ゼロ・データ同梱 |
| [japan-reverse-geocoder](https://github.com/uiuifree/rust-japan-reverse-geocoder) | [![Crates.io](https://img.shields.io/crates/v/japan-reverse-geocoder.svg)](https://crates.io/crates/japan-reverse-geocoder) | Offline reverse geocoding for Japan (latitude/longitude to prefecture and municipality) using MLIT location reference data / 国土交通省の位置参照情報を同梱し、緯度経度→都道府県・市区町村をオフラインで引く |
| [jismeshcode](https://github.com/uiuifree/rust-jismeshcode) | [![Crates.io](https://img.shields.io/crates/v/jismeshcode.svg)](https://crates.io/crates/jismeshcode) | Japanese Standard Grid Square Code (JIS X 0410) library / 日本標準地域メッシュコード（JIS X 0410）のRustライブラリ |
| [jp-location-relation](https://crates.io/crates/jp-location-relation) | [![Crates.io](https://img.shields.io/crates/v/jp-location-relation.svg)](https://crates.io/crates/jp-location-relation) | Adjacency relations of Japanese prefectures and municipalities / 日本の都道府県・市区町村の隣接関係を取得するライブラリ |

### 💼 Job Data / Japanese Text Processing

| Crate | Version | Description |
|-------|---------|-------------|
| [tagpipe-core](https://github.com/uiuifree/tagpipe-core) | [![Crates.io](https://img.shields.io/crates/v/tagpipe-core.svg)](https://crates.io/crates/tagpipe-core) | Dictionary-based, explainable / auditable tagging & attribute-extraction pipeline engine with Japanese text normalization / 辞書ベースで説明可能・監査可能なタグ付け・属性抽出パイプラインエンジン（日本語正規化対応） |
| [job-formatter-core](https://github.com/uiuifree/job-formatter-core) | [![Crates.io](https://img.shields.io/crates/v/job-formatter-core.svg)](https://crates.io/crates/job-formatter-core) | Industry-agnostic job-feed formatting engine: CSV/Excel → normalized JSONL → per-media rows. Parallel, order-preserving, Shift_JIS auto-detection / 企業CSV/Excelを正規化JSONL・媒体別データへ変換する求人フィード整形エンジン（並列・順序保持・Shift_JIS自動判定） |
| [salary-parser-jp](https://github.com/uiuifree/rust-salary-parser-jp) | [![Crates.io](https://img.shields.io/crates/v/salary-parser-jp.svg)](https://crates.io/crates/salary-parser-jp) | Parse Japanese job-posting salary text into typed yen amounts (hourly / daily / monthly / yearly) / 求人の給与テキスト（「月給21万円〜26万円」等）を時給・日給・月給・年収の金額に構造化するパーサー |
| [station-resolver-jp](https://github.com/uiuifree/rust-station-resolver-jp) | [![Crates.io](https://img.shields.io/crates/v/station-resolver-jp.svg)](https://crates.io/crates/station-resolver-jp) | Japanese station-access text parser: extracts walk / bus / car / train minutes and resolves station names / 求人のアクセス欄から徒歩・バス・車・電車の所要時間を抽出し、駅名を解決するパーサー |

### 📈 Google / SEO

| Crate | Version | Description |
|-------|---------|-------------|
| [google-indexing-api](https://github.com/uiuifree/rust-google-indexing-api) | [![Crates.io](https://img.shields.io/crates/v/google-indexing-api.svg)](https://crates.io/crates/google-indexing-api) | Async Rust client for the Google Indexing API: notify Google of updated / deleted URLs (JobPosting, Google for Jobs), one by one or in batches of 100 / Google Indexing APIの非同期Rustクライアント。URLの更新・削除通知（1件ずつ・100件バッチ） |
| [indexnow-api](https://github.com/uiuifree/rust-indexnow-api) | [![Crates.io](https://img.shields.io/crates/v/indexnow-api.svg)](https://crates.io/crates/indexnow-api) | IndexNow API client: notify Bing, Yandex, Naver, Seznam.cz and Yep about URL changes / IndexNow APIのRustクライアント。Bing・Yandex・Naver等へURL変更を通知 |
| [google-search-console-api](https://github.com/uiuifree/rust-google-search-console-api) | [![Crates.io](https://img.shields.io/crates/v/google-search-console-api.svg)](https://crates.io/crates/google-search-console-api) | Unofficial async Rust client for the Google Search Console API: Search Analytics, Sitemaps, Sites, URL Inspection / Google Search Console APIの非公式・非同期Rustクライアント |
| [google-analytics-api-ga4](https://github.com/uiuifree/rust-google-analytics-api-ga4) | [![Crates.io](https://img.shields.io/crates/v/google-analytics-api-ga4.svg)](https://crates.io/crates/google-analytics-api-ga4) | Async Rust client for the Google Analytics 4 (GA4) Data API / Google Analytics 4 (GA4) Data APIの非同期Rustクライアント |
| [data-for-seo](https://github.com/uiuifree/rust-data-for-seo) | [![Crates.io](https://img.shields.io/crates/v/data-for-seo.svg)](https://crates.io/crates/data-for-seo) | Rust client for the DataForSEO API v3: SERP, keyword data, backlinks and other SEO metrics / DataForSEO API v3（SERP・キーワード・バックリンク等）のRustクライアント |
| [sitemap-writer](https://github.com/uiuifree/rust-sitemap-writer) | [![Crates.io](https://img.shields.io/crates/v/sitemap-writer.svg)](https://crates.io/crates/sitemap-writer) | XML sitemap generator: sitemap index, 50,000-URL splitting, gzip / サイトマップXML生成ライブラリ（sitemap index・50,000 URL分割・gzip対応） |

### 🔌 API Clients

| Crate | Version | Description |
|-------|---------|-------------|
| [openai_chatgpt_api](https://github.com/uiuifree/rust-openai-chatgpt-api) | [![Crates.io](https://img.shields.io/crates/v/openai_chatgpt_api.svg)](https://crates.io/crates/openai_chatgpt_api) | Rust client for the OpenAI ChatGPT API / OpenAI ChatGPT APIのRustクライアント |
| [line-bot-messaging-api](https://github.com/uiuifree/rust-line-messaging-api) | [![Crates.io](https://img.shields.io/crates/v/line-bot-messaging-api.svg)](https://crates.io/crates/line-bot-messaging-api) | Rust client for the LINE Messaging API / LINE Messaging APIのRustクライアント |
| [line-login-api](https://github.com/uiuifree/rust-line-login-api) | [![Crates.io](https://img.shields.io/crates/v/line-login-api.svg)](https://crates.io/crates/line-login-api) | Rust client for the LINE Login API / LINE Login APIのRustクライアント |
| [slack-web-api](https://github.com/uiuifree/rust-slack-web-api) | [![Crates.io](https://img.shields.io/crates/v/slack-web-api.svg)](https://crates.io/crates/slack-web-api) | Rust client for the Slack Web API / Slack Web APIのRustクライアント |
| [web-arena-indigo](https://github.com/uiuifree/rust-web-arena-indigo) | [![Crates.io](https://img.shields.io/crates/v/web-arena-indigo.svg)](https://crates.io/crates/web-arena-indigo) | Async Rust client for the WebARENA Indigo VPS API (NTTPC) / WebARENA Indigo VPS API（NTTPC）の非同期Rustクライアント |

### 🔍 Elasticsearch

| Crate | Version | Description |
|-------|---------|-------------|
| [elastic-query-builder](https://github.com/uiuifree/elastic-query-builder) | [![Crates.io](https://img.shields.io/crates/v/elastic-query-builder.svg)](https://crates.io/crates/elastic-query-builder) | Query builder for the Elasticsearch query DSL / Elasticsearch DSLを簡単に構築するためのクエリビルダー |
| [elastic-parser](https://github.com/uiuifree/elastic-parser) | [![Crates.io](https://img.shields.io/crates/v/elastic-parser.svg)](https://crates.io/crates/elastic-parser) | Parser for Elasticsearch responses / Elasticsearchレスポンスのパーサー |

### 🧰 Utilities

| Crate | Version | Description |
|-------|---------|-------------|
| [shinchoku](https://github.com/uiuifree/shinchoku) | [![Crates.io](https://img.shields.io/crates/v/shinchoku.svg)](https://crates.io/crates/shinchoku) | NDJSON protocol for batch CLI progress reporting — Rust / Go / Node / PHP / Python ([shinchoku.app](https://shinchoku.app/)) / バッチCLIの進捗報告のためのNDJSONプロトコル |
