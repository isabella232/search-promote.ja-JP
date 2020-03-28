---
description: 'null'
seo-description: 'null'
seo-title: Search&Promote 15.3.1リリースノート（2015年3月25日）
solution: Target
title: Search&Promote 15.3.1リリースノート（2015年3月25日）
topic: Release Notes,Site search and merchandising
uuid: f02da5a4-2207-4603-aa05-5cff7be16dd5
translation-type: tm+mt
source-git-commit: ffdec2cfcb30e733c664a7d1ca23868b7a9a9aa5

---


# Search&amp;Promote 15.3.1 Release Notes (03/24/2015){#search-promote-release-notes}

## 新機能および機能強化 {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* 製品モデル番号の検索 — 新しい「言語」設定が追加されました。この設定を使用すると、オプションで、アルファベット順の数字トランジションにトークンを分割できます。 この機能により、パーツや製品スタイルのトークンに対する自由なテキストの一致がより柔軟に行えます。

   検索用 **[!UICONTROL Partial Alphanumeric Matching]** 語とWeb [コンテンツとの一致方法の設定の説明を参照してください。](../c-about-linguistics-menu/c-about-words-and-language.md#task_351A9144A51F4B41923BDBACDEF3B616).

* データの結果をエクスポートする機能を表示しました。

   データ [表示](../c-about-reports-menu/c-about-data-views.md#concept_DCA897D074464BC1861AA47B40CC86C3)。

* 幅のある属性の自動ファセット値のグループ化機能の動的な生成範囲。

   現在、アドビシステムズ社では、これを行うためにコンテンツ識別範囲の値を指定する必要があります。 例えば、価格が10の場合は、「$10 ～ $20」の範囲文字列を生成します。 または、アドビシステムズ社ではスクリプトフィルタリングを使用する必要があります。 フィールドのみのメタデータフィールド定義に新しい属性を追 `Type=Number` 加しました。 新しいオプションでは、数値フィールドをフィールドに関 `Type=Text` 連付け、範囲の説明の作成方法を説明する設定情報を指定します。

   詳しくは、 [新しいメタタグフィールドの追加を参照してくださ](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)い。

## 修正点 {#section_22D1AFC99F394D569898828A0D3C419D}

* ファセットパネルの編集ダイアログに、ステージファセットを含める必要があります。
* 日本語文字を含む検索の「埋め込み」検索モードのコア検索結果を空にする。
* Wordの.docxファイルの時間変換で属性が設定されるようになり `title` ました。
* マネージャーの誤った「重複バナー」メッセージを修正 **[!UICONTROL Banner]** しました。
* [!DNL Dynamic Media Classic] バナーは、プロトコルに依存しなくなりました。
* アカウント **[!UICONTROL Table Name]** に対して有効になっている場合でも、メタデータユーザーインターフェイスでユーザ定義フィールドを編集する際に、フィールド属性が非表示にな **[!UICONTROL Dynamic Facets]** ることがありました。
* **[!UICONTROL Recent Searches]** 非ASCII文字を乗算エンコードしなくなりました。
* MDIフィールドは、スクリプトフィルタリングを使用せずに入力できます。
* 提案のエンコーディングが正しくありません。
* 複雑なビジネスルールで、「その他のファセットが選択された」トリガーが正しく機能するようになりました。

