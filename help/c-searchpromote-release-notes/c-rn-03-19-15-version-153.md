---
description: Search&amp;Promote 15.3.1リリースノート。
solution: Target
title: Search&amp;Promote 15.3.1リリースノート（2015年3月25日）
topic-legacy: Release Notes,Site search and merchandising
uuid: f02da5a4-2207-4603-aa05-5cff7be16dd5
exl-id: 2d254275-f777-45e5-a838-b6a35365a6dd
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 1%

---

# Search&amp;Promote15.3.1リリースノート（2015年3月25日）{#search-promote-release-notes}

## 新機能および機能強化 {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* 製品モデル番号の検索 — 新しい「言語」設定が追加され、アルファベット順の数値トランジションにトークンをオプションで分割できるようになりました。 この機能により、パーツや製品スタイルのトークンに対する自由なテキストの一致をより柔軟に行うことができます。

   [検索用語とWebコンテンツとの一致方法の設定の&#x200B;**[!UICONTROL Partial Alphanumeric Matching]**&#x200B;を参照してください。](../c-about-linguistics-menu/c-about-words-and-language.md#task_351A9144A51F4B41923BDBACDEF3B616)。

* データ表示の結果をエクスポートする機能を追加しました。

   [データ表示について](../c-about-reports-menu/c-about-data-views.md#concept_DCA897D074464BC1861AA47B40CC86C3)を参照してください。

* 幅のある属性の自動ファセット値のグループ化機能に対して、動的に生成される範囲。

   現在、Adobe Systemsでは、これを行うために、コンテンツ識別範囲の値を指定する必要があります。 例えば、価格が10の場合は、「$10 ～ $20」の範囲文字列を生成します。 または、Adobe Systemsではスクリプトフィルタリングを使用する必要があります。 `Type=Number`フィールド専用の、メタデータフィールド定義に新しい属性を追加しました。 新しいオプションは、数値フィールドを`Type=Text`フィールドに関連付け、範囲の説明の作成方法を説明する設定情報を指定します。

   「[新しいmetaタグフィールドの追加](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)」を参照してください。

## 修正点 {#section_22D1AFC99F394D569898828A0D3C419D}

* ファセットパネルの編集ダイアログには、ステージファセットが含まれている必要があります。
* 日本語の文字を含む検索の場合、「埋め込み」検索モードのコア検索結果を空にする。
* Wordの.docxファイルをTika変換すると、`title`属性に値が設定されるようになりました。
* **[!UICONTROL Banner]**&#x200B;マネージャの誤った「重複バナー」メッセージを修正。
* [!DNL Dynamic Media Classic] バナーは、プロトコルに依存しなくなりました。
* **[!UICONTROL Table Name]**&#x200B;フィールド属性が、メタデータユーザーインターフェイスでユーザ定義フィールドを編集する際に、アカウントで&#x200B;**[!UICONTROL Dynamic Facets]**&#x200B;が有効になっている場合でも、非表示になることがありました。
* **[!UICONTROL Recent Searches]** 非ASCII文字を乗算エンコードしなくなりました。
* スクリプトフィルタリングを使用せずに、MDIフィールドを入力できます。
* 候補のエンコードが正しくありません。
* 複雑なビジネスルールで、「その他のファセットが選択された」トリガーが正しく機能するようになりました。
