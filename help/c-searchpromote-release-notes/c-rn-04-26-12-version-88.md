---
description: Search&amp;Promote 8.8リリースノート。
solution: Target
title: Search&amp;Promote 8.8リリースノート（2012年4月27日）
topic: Release Notes,Site search and merchandising
uuid: ddb9f1af-92a4-4f85-be8f-a36f34d31add
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 68%

---


# Search&amp;Promote8.8リリースノート（2012年4月27日）{#search-promote-release-notes}

**新機能**

* 動的なファセット設定

   インデックスからインデックスへの変更（新しい属性の追加、古い属性の削除または名前変更）が行われる可能性のあるサイトコンテンツの各ページに関連付けられた、自由な形式の属性セットに対して、動的なファセット設定が可能になりました。動的なファセット設定によって、スロットファセットと実際のファセットが自動的にマッピングされます。ビジネスルールと共にGuided Search レイヤーを使用することで、この機能はとても便利になります。
* AdobeSearch&amp;Promoteeユーザーインターフェイス

   すべてのAdobeSearch&amp;PromoteWebページにAdobeユーザーインターフェイスを実装しました。
* Adobeのログインポータルとの緊密な統合

   AdobeSearch&amp;Promoteのお客様は、Adobeログインポータルのみを使用できます。 現在の[!DNL Adobe Publish]、Adobe SiteSearch、Atomzのお客様は、従来のログインを引き続き使用します。
* 中国語と日本語をサポートするための新しい形態素解析

   中国語と日本語をサポートするため、インデックスおよび検索時間に対して形態素解析が適用されるようになりました。
* Microsoft Office 2010 などの新しいドキュメントタイプのサポート

   .doc、.docx、.pdf、.mp3 などの様々なタイプのドキュメントを HTML に変換してから、インデクサーに送信することができるようになりました。
* Adobe Search&amp;Promote オンラインヘルプシステムの更新

   オンラインヘルプシステムのユーザーインターフェイスが新しくなり、タスクベースになりました。

**修正点および改良点**

* Stage Managerを使用してバナーをプッシュすると、Stage Classicに関連する機能が使用中に機能しなくなる問題を修正しました。
* ルールの編集時に「Query Parameter does not exist」というエラーが発生した場合、「Keyword contains」という誤ったメッセージに解釈される問題を修正しました。
* 2回目にパラメーターを編集できない問題を修正しました。
* Index Connector で、2 つ以上のマップ定義で同じメタデータ値またはフィールド値を示すことができない問題を修正しました。
* 一部の PDF ドキュメントのクロール時の問題を修正しました。3.03 にアップグレードすると、現在のクラッシュが解決されます。
* ビジネスルールの説明を短くする（例：マネージャーに field_table を表示しない）機能を追加しました。
* Guided Search ナビゲーションメニューに表示できる項目数が 9 個から最大 20 個に増加しました。
* Index Connector のパフォーマンスが向上しました。

