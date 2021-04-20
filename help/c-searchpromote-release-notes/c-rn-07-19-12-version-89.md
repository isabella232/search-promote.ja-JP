---
description: Search&amp;Promote 8.9リリースノート。
solution: Target
title: Search&amp;Promote 8.9リリースノート（2012年7月19日）
topic: Release Notes,Site search and merchandising
uuid: 3853c75d-19ed-4e36-9e81-dcbffe5f5b0c
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 57%

---


# Search&amp;Promote8.9リリースノート（2012年7月19日）{#search-promote-release-notes}

**新機能**

* メタデータ管理の強化 — 顧客フィードからの動的なメタデータ定義

   顧客から提供されたメタデータ定義に基づき、貴社の Search&amp;Promote アカウントを動的に再設定するスキームを作成します。
* インデックス作成パフォーマンスの向上 — Index Loader

   Index Loader は、XML コンテンツを Search&amp;Promote インデックスに直接インポートできる新しい手段です。これは既存の Index Connector 機能のサブセットで、アドビの標準の XML フィードファイルをすばやくインポートするよう設計されています。

**修正点および改良点**

* ビジネスルールによる並べ替えオプションの変更がサポートされるようになりました。
* ヘルプシステムの`<search-description>`タグでは、説明のメタタグの内容が空の場合に、本文が代わりに表示されます。
* 結果ベースのアクションによって追加された結果に対し、該当する表のヒットを追跡する機能を追加しました。
* POSTを介したクエリパラメーターの送信のサポートを追加しました。
* クロール時、場合によっては最後の mirror_account 操作をスキップできます。
* Adobe AnalyticsのURLには、CGI引数は含まれません。Adobe Analyticsの参照を行うSearch&amp;Promoteコードは、同様にURLキーからCGI引数を取り除くために必要です。
* 再書き込みルールがプッシュされ有効になった後で、これらのルールがユーザーインターフェイスから断続的に非表示になっていました。
* 結果が低いので提案を行うように設定されたSearch&amp;Promoteアカウントでは、結果が断続的になる場合があります。
* 書き換えルールのテスト出力に改行が含まれていませんでした。
* Search URL Rules ページと Crawl List Store URL Rules ページが示す History ページが正しくありませんでした。
* 一部のバナーで「Edit」をクリックしても、Edit ページが表示されませんでした。
* 更新コードの再ランク付けが、異常に遅い場合がありました。
* ファセット名に大文字と小文字が混在している場合、ファセット項目の削除やプッシュが機能しませんでした。

