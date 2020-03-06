---
description: 'null'
seo-description: 'null'
seo-title: Search&Promote 8.9リリースノート（2012年7月19日）
solution: Target
title: Search&Promote 8.9リリースノート（2012年7月19日）
topic: Release Notes,Site search and merchandising
uuid: 3853c75d-19ed-4e36-9e81-dcbffe5f5b0c
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Search&amp;Promote 8.9 Release Notes (07/19/2012){#search-promote-release-notes}

**新機能**

* メタデータ管理の強化 — 顧客フィードからの動的なメタデータの定義

   顧客から提供されたメタデータ定義に基づき、貴社の Search&amp;Promote アカウントを動的に再設定するスキームを作成します。
* インデックス作成パフォーマンスの向上 — Index Loader

   Index Loader は、XML コンテンツを Search&amp;Promote インデックスに直接インポートできる新しい手段です。これは既存の Index Connector 機能のサブセットで、アドビの標準の XML フィードファイルをすばやくインポートするよう設計されています。

**修正点および改良点**

* ビジネスルールによる並べ替えオプションの変更がサポートされるようになりました。
* In the Help system `<search-description>` tag shows the body instead when the meta tag for the description has empty content.
* 結果ベースのアクションによって追加された結果に対し、該当する表のヒットを追跡する機能を追加しました。
* POSTを使用したクエリパラメーターの送信のサポートを追加しました。
* クロール時、場合によっては最後の mirror_account 操作をスキップできます。
* Adobe Analytics URLには、CGI引数と、同様にURLキーからCGI引数を取り除くために必要なAdobe Analyticsの参照を行うSearch&amp;Promoteコードは含まれません。
* 再書き込みルールがプッシュされ有効になった後で、これらのルールがユーザーインターフェイスから断続的に非表示になっていました。
* 結果が低いので提案を行うように設定された「お客様の平均値」設定のSearch&amp;Promoteアカウントでは、結果が断続的にな場合があります。
* 書き換えルールのテスト出力に改行が含まれていませんでした。
* Search URL Rules ページと Crawl List Store URL Rules ページが示す History ページが正しくありませんでした。
* 一部のバナーで「Edit」をクリックしても、Edit ページが表示されませんでした。
* 更新コードの再ランク付けが、異常に遅い場合がありました。
* ファセット名に大文字と小文字が混在している場合、ファセット項目の削除やプッシュが機能しませんでした。

