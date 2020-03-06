---
description: 'null'
seo-description: 'null'
seo-title: Search&Promote 8.16.0リリースノート（2014年9月19日）
solution: Target
title: Search&Promote 8.16.0リリースノート（2014年9月19日）
topic: Release Notes,Site search and merchandising
uuid: 0a59858b-213b-40d6-aea1-d085c4d6d2fa
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Search&amp;Promote 8.16.0 Release Notes (9/18/2014){#search-promote-release-notes}

## Search&amp;Promote 8.16.0 Release Notes (9/18/2014) {#topic_5BECD3F66C684987828F6AE65E62DA29}

## New features {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* ガイド付き検索3(GS3)での検索結果のキャッシュ — このカスタム機能を設定して、お使いのアカウントで使用できるようにするには、アドビのテクニカルアカウントマネージャーにお問い合わせください。
* 頻繁に変更されるフィールドの垂直方向の更新 — コンテンツのインデックスを完全に再作成する必要なく、一連のメタデータフィールドのすべての値をすばやく更新できるようになりました。

   新しいメタタグフィールドの追加の表の「垂直方向の更新フィールド」オ [プションと、垂直方向の更新について](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)[「垂直方](../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899)向の更新フィールド」を参照してください。

   This feature can only be used on [!DNL Adobe Search&Promote] accounts that use Index Connector. このカスタム機能を設定して、お使いのアカウントで使用できるようにするには、Adobe テクニカルアカウントマネージャーにお問い合わせください。

## Fixes and enhancements {#section_22D1AFC99F394D569898828A0D3C419D}

* Corrected the Index Connector parsing of XML feeds that contained `?>` string.
* 最少のドキュメント数が強制される場合のインデックスコネクタSFTPフィードを修正しました。
* Microsoft Excel へのレポート書きだしで、UTF8 をサポートするようになりました。
* ガイド付き検索：ファセットのコンパイルが遅かった問題を修正しました。
* 属性ローダー：データの集計でキーが重複していた問題を修正しました。
* 個別のルールをライブにプッシュする際の、間違ったビジネスルールの実行命令を修正しました。
* ガイド付き検索によって、間違ったファセットの元に戻すリンクが生成されていた問題を修正しました。
* 新しいリモートコントロール操作が追加され（`sp_lines=N`）、現在実行中のインデックスクロールの進捗状況と状態をチェックできます。

   About Remote Control for Indexingを参照し [てください](../c-about-index-menu/c-about-remote-control-for-indexing.md#concept_C79B322190E84106A434E5C6D4A4118F)。

* インデックスコネクタの増分中に削除した情報を取得する際に、認証情報を送信する必要があります。
* The [!DNL Change Log] report now identifies the user who initiates a manual index operation.

   See [Viewing the Change Log](../c-about-reports-menu/c-about-reports-menu.md#task_166F1156719F4B3D834BEA8E249C8057).

* When you export a [!DNL Terms Report], you are no longer limited to 500 or less items in the report.

   「キーワ [ードレポートの表示」または「検索キーワードが空の場合」を参照してください。](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* The Index Connector **[!UICONTROL Strip HTML]** setting was always displaying as checked.
* Inconsistent search results were experienced with the **[!UICONTROL Common Phrases]** feature.
* ルールリストの概要で、属性名の表示が切り詰められていた問題を修正しました。
* 個別のビジネスルールをライブにプッシュすると、すべてのビジネスルールがライブにプッシュされていた問題を修正しました。

