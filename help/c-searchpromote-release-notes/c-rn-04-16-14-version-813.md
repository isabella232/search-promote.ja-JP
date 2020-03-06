---
description: 'null'
seo-description: 'null'
seo-title: Search&Promote 8.13.0リリースノート（2014年4月17日）
solution: Target
title: Search&Promote 8.13.0リリースノート（2014年4月17日）
topic: Release Notes,Site search and merchandising
uuid: b3524992-ff00-4a7c-a404-078242456734
translation-type: tm+mt
source-git-commit: 9d5ac055d665b39d09b28063179d74a389d7f830

---


# Search&amp;Promote 8.13.0 Release Notes (04/16/2014){#search-promote-release-notes}

| 新機能と機能強化 | 説明 |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 完全テーブル一致を含む動的ファセットのサポート | 「SKUレベル」の属性が多数あり、動的ファセットを使用して選択して表示したいと考える顧客もいました。 その場合、オプションで、各動的ファセットフィールドを静的アカウント設定の最大 1 つのテーブル名に関連付けることができます。こうしたテーブルのリレーションシップは、検索時に、その検索に関連する動的ファセットフィールドに適用できます。動的事 [実についてを参照](../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899)。 |

**修正点**

* Changed the data view description field to use the tag `<search-display-field>` instead of the `<search-description>`.
* Index Connector に、プライマリキーに 2 つ以上のフィールドを連結する機能が追加されました。
* AttributeLoader-Regen-Enabled スクリプトの `attributeloader-regen.pl` が変更され、HTML エンコードされた値でなくなりました。
* 「範囲検索」クエリーのインデックス時間と検索時間の空白文字の処理が一致するようになりました。
* 動的ファセットを有効にすると、ビジネスルールの追加がエラーになることがあった問題を修正しました。

   See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* A Javascript error prevented adding or editing a definition in **Settings** > **SPIN** > **IndexConnector**.
* ビジネスルールの作成時に時間が選択された場合、ビジネスルールが保存されると、GMTタイムゾーンがデフォルトで表示されていました。 ビジネスルールの保存後、アカウントのタイムゾーンで表示され、実施されていました。

   See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* ステージでのビジネスルールの並び替えが正しく動作していなかった問題を修正しました。

   See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* 検索パフォーマンスレポートが強化され、電子メール配信のレポートをスケジュールできるようになりました。
* ビジネスルールのスケジュールが修正され、自動的に夏時間に変更されるようになりました。

   See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* 多数の動的ファセットフィールドが定義されている場合、コア検索の応答時間が遅くなっていました。
* 正しくない範囲インデックスエラーが発生していた問題を修正しました。
* 北米以外のデータセンターでのDynamic Media Classicのアクセスが壊れていた問題を修正しました。
* SPIN XPath 検証関数が誤検知エラーを返していた問題を修正しました。

* SPIN の有効化／無効化の操作の後、ユーザーがメンバーセンターログインページにリダイレクトされていた問題を修正しました。

