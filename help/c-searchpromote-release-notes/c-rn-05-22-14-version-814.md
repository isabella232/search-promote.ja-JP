---
description: 'null'
seo-description: 'null'
seo-title: Search&Promote 8.14.0リリースノート（2014年5月23日）
solution: Target
title: Search&Promote 8.14.0リリースノート（2014年5月23日）
topic: Release Notes,Site search and merchandising
uuid: 308d84a9-ec38-4fec-b146-e8a353e65be4
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Search&amp;Promote 8.14.0 Release Notes (05/22/2014){#search-promote-release-notes}

**修正点**

* [!DNL sqlite_open] に失敗する場合、古い SQLite データベースファイルが退避され、新しいファイルが最初から作成されます。
* 同じ検索が繰り返されると、主要な検索結果が異なっていた問題を修正しました。
* 検索結果ごとに多くのフィールドが出力される場合のテンプレート処理のパフォーマンスが向上しました。
* ビジネスルールの履歴にメモが追加されました。
* インデックス作成処理時に、結果ベースのトリガーおよびアクションのプレビューインデックス再生成フェーズのパフォーマンスが時間の経過と共に着実に低下する問題を修正しました。
* **SPIN キャッシュをリセット**&#x200B;オプションがいいえ／次回に実行のブール型から、いいえ／常に／次回に実行の 3 つの選択肢に変更されました。

