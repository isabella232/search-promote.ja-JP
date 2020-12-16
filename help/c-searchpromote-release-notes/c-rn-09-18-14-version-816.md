---
description: 'null'
seo-description: 'null'
seo-title: Search&amp;Promote 8.16.0リリースノート（2014年9月19日）
solution: Target
title: Search&amp;Promote 8.16.0リリースノート（2014年9月19日）
topic: Release Notes,Site search and merchandising
uuid: 0a59858b-213b-40d6-aea1-d085c4d6d2fa
translation-type: tm+mt
source-git-commit: ffdec2cfcb30e733c664a7d1ca23868b7a9a9aa5
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 37%

---


# Search&amp;Promote8.16.0リリースノート（2014年9月19日）{#search-promote-release-notes}

## Search&amp;Promote8.16.0リリースノート（2014年9月19日） {#topic_5BECD3F66C684987828F6AE65E62DA29}

## 新機能{#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* ガイド付き検索3(GS3)での検索結果のキャッシュ — このカスタム機能を設定して、お使いのアカウントで使用できるようにするには、Adobeのテクニカルアカウントマネージャーにお問い合わせください。
* 頻繁に変更されるフィールドの垂直更新 — コンテンツのインデックスを完全に再作成することなく、一連のメタデータフィールドのすべての値をすばやく更新できるようになりました。

   [新しいmetaタグフィールドの追加](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)および[垂直更新](../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899)の表の「垂直更新フィールド」オプションを参照してください。

   この機能は、インデックスコネクタを使用する[!DNL Adobe Search&Promote]アカウントでのみ使用できます。 このカスタム機能を設定して、お使いのアカウントで使用できるようにするには、Adobe テクニカルアカウントマネージャーにお問い合わせください。

## 修正点と機能強化{#section_22D1AFC99F394D569898828A0D3C419D}

* `?>`文字列を含むXMLフィードを解析するインデックスコネクタを修正しました。
* 最少のドキュメント数が強制される場合のインデックスコネクタSFTPフィードを修正しました。
* Microsoft Excel へのレポート書きだしで、UTF8 をサポートするようになりました。
* ガイド付き検索：ファセットのコンパイルが遅かった問題を修正しました。
* 属性ローダー：データの集計でキーが重複していた問題を修正しました。
* 個別のルールをライブにプッシュする際の、間違ったビジネスルールの実行命令を修正しました。
* ガイド付き検索によって、間違ったファセットの元に戻すリンクが生成されていた問題を修正しました。
* 新しいリモートコントロール操作が追加され（`sp_lines=N`）、現在実行中のインデックスクロールの進捗状況と状態をチェックできます。

   [インデックス作成のためのリモートコントロールについて](../c-about-index-menu/c-about-remote-control-for-indexing.md#concept_C79B322190E84106A434E5C6D4A4118F)を参照してください。

* インデックスコネクタの増分中に削除した情報を取得する際に、認証情報を送信する必要があります。
* [!DNL Change Log]レポートで、手動のインデックス作成操作を開始したユーザーを識別できるようになりました。

   「[変更ログの表示](../c-about-reports-menu/c-about-reports-menu.md#task_166F1156719F4B3D834BEA8E249C8057)」を参照してください。

* [!DNL Terms Report]をエクスポートする場合、レポート内の項目数が500個以下に制限されることはなくなりました。

   [キーワードレポートまたはNULL検索キーワードレポートの表示を参照してください。](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* インデックスコネクタ&#x200B;**[!UICONTROL Strip HTML]**&#x200B;の設定が常にチェック済みとして表示されていました。
* **[!UICONTROL Common Phrases]**&#x200B;機能で検索結果が一致しませんでした。
* ルールリストの概要で、属性名の表示が切り詰められていた問題を修正しました。
* 個々のビジネスルールをライブにプッシュすると、すべてのビジネスルールがライブにプッシュされていました。

