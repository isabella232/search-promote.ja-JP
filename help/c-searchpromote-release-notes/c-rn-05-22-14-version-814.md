---
description: 'null'
seo-description: 'null'
seo-title: Search&Promote 8.14.0リリースノート（2014年5月23日）
solution: Target
title: Search&Promote 8.14.0リリースノート（2014年5月23日）
topic: Release Notes,Site search and merchandising
uuid: 308d84a9-ec38-4fec-b146-e8a353e65be4
translation-type: tm+mt
source-git-commit: ffdec2cfcb30e733c664a7d1ca23868b7a9a9aa5

---


# Search&amp;Promote 8.14.0 Release Notes (05/22/2014){#search-promote-release-notes}

**修正点**

* [!DNL sqlite_open] に失敗する場合、古い SQLite データベースファイルが退避され、新しいファイルが最初から作成されます。
* 同じ検索が繰り返されると、主要な検索結果が異なっていた問題を修正しました。
* 検索結果ごとに多くのフィールドが出力される場合のテンプレート処理のパフォーマンスが向上しました。
* にメモを追加しまし **[!UICONTROL Business Rule History]**&#x200B;た。
* インデックス作成処理時に、結果ベースのトリガーおよびアクションのプレビューインデックス再生成フェーズのパフォーマンスが時間の経過と共に着実に低下する問題を修正しました。
* Changed **[!UICONTROL Reset SPIN cache]** option from boolean no/next-run to a tri-state: no/always/next-run.

