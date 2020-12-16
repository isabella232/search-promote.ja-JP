---
description: SEO（検索エンジン最適化）メタタグを使用すると、ページの特定の要素をカスタマイズし、検索エンジンの配置を改善できます。
seo-description: SEO（検索エンジン最適化）メタタグを使用すると、ページの特定の要素をカスタマイズし、検索エンジンの配置を改善できます。
seo-title: SEOについて
solution: Target
subtopic: SEO
title: SEOについて
topic: Settings,Site search and merchandising
uuid: 5c5d64f5-fe79-4489-85c6-399d1437f2c4
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a
workflow-type: tm+mt
source-wordcount: '1226'
ht-degree: 1%

---


# SEO{#about-seo}について

SEO（検索エンジン最適化）メタタグを使用すると、ページの特定の要素をカスタマイズし、検索エンジンの配置を改善できます。

## SEO {#concept_C58BFCE720824A2B9B5F5E613CFD4C0B}を使用

このような各要素を、開始テキストの後に単語のリストが続くように定義できます。 単語のリストには、次のものがあります。

* 選択した期間（「先月」など）におけるサイトでよく使用される検索フレーズ。カスタム除外の対象となります。
* ページの検索元の1つ以上のフィールドの値セット。
* リストで定義する静的な語句

SEOで最も一般的なページ要素は、ページタイトル、「キーワード」、「説明」メタタグです。 これらの3つのページ要素の設定を定義できます。 さらに、次の3種類のページのそれぞれに対して、これら3つの設定を定義できます。検索結果ページ、ブラウズページおよび項目の詳細ページ

SEO設定を保存またはプレビューすると、小さなセグメントの検索（トランスポート）テンプレートが生成され、`<search-include>`テンプレートタグを使用して他の検索テンプレートに含めることができます。 例えば、次の項目を含む別のテンプレートに、「検索結果ページのタイトル」フィールドを含めることができます。

```
<search-include file="seo/seo_search_title.tpl" />
```

SEOフィールドの`<search-include>`タグの`file`属性に指定できる9つの値は次のとおりです。

* `seo/seo_search_title.tpl`
* `seo/seo_search_description.tpl`
* `seo/seo_search_keywords.tpl`
* `seo/seo_browse_title.tpl`
* `seo/seo_browse_description.tpl`
* `seo/seo_browse_keywords.tpl`
* `seo/seo_item_title.tpl`
* `seo/seo_item_description.tpl`
* `seo/seo_item_keywords.tpl`

プレゼンテーションテンプレートでSEOフィールドを使用するには、いくつかの手順を実行します。

まず、前述の`<search-include>`を使用して、`<general>`要素内のXML検索テンプレートに目的のフィールドを含めます。

次に、各`<search-include>`タグを`<general-field>`タグと`</general-field>`タグで囲み、次の例のように`name`属性にフィールド名を指定します。

```
<general> 
    <general-field name="seo_search_title"><search-include file="seo/seo_search_title.tpl" /></general-field> 
    <general-field name="seo_search_description"><search-include file="seo/seo_search_description.tpl" /></general-field> 
    <general-field name="seo_search_keywords"><search-include file="seo/seo_search_keywords.tpl" /></general-field> 
</general>
```

次の例のように、プレゼンテーションテンプレートで`<guided-general-field>`タグを使用して、必要な場所に名前付きフィールドを挿入できます。

```
<title><guided-general-field gsname="default" field="seo_search_title"></title> 
<meta name="description" content="<guided-general-field gsname="default" field="seo_search_description">"/> 
<meta name="keywords" content="<guided-general-field gsname="default" field="seo_search_keywords">"/>
```

`gsname`属性を使用して、この場合は「デフォルト」検索を指定します。

また、Webページで使用できる9つの異なるSEOフィールドを定義できます。 以下が含まれます。

* 検索結果ページ — タイトル、説明、キーワード
* ブラウズページ — タイトル、説明、キーワード
* 項目の詳細ページ — タイトル、説明、キーワード

9つのフィールドはすべて同じ設定で定義されます。 実際、「検索結果ページ」の「タイトル」フィールドなど、9つのフィールドの名前は、使い方の提案にすぎません。 プレゼンテーションテンプレートや検索テンプレートの任意のコンテキストで、任意のフィールドを使用できます。

[テンプレートについて](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5)も参照してください。

「[プレゼンテーションテンプレートタグ](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)」も参照してください。

「[検索テンプレートタグ](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)」も参照してください。

「[検索結果の単語リストの設定](../c-about-settings-menu/c-about-seo.md#task_A459A3734EC04042BA52C81184251DD4)」も参照してください。

## 検索結果の単語リスト{#task_A459A3734EC04042BA52C81184251DD4}の設定

ページタイトル、説明、キーワードに含まれる検索結果の語句のリストを設定できます。

**検索結果の単語リストを設定するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL SEO]**/**[!UICONTROL Search Result Pages]**&#x200B;をクリックします。
1. [!DNL SEO Browse Pages Word List]ページの[!DNL Title]、[!DNL Description]、[!DNL Keywords]の各グループで、必要なオプションを設定します。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>タイトル |説明 |キーワード開始 </p> </td> 
      <td colname="col2"> <p>リストという単語の前に表示するテキストです。 </p> <p>例えば、キーワードリストを「ブランド」という語で始めるとします。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最頻検索を含める </p> </td> 
      <td colname="col2"> <p>検索を含める期間。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最大検索数 </p> </td> 
      <td colname="col2"> <p>含める検索の最大数。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フィールド値を含む </p> </td> 
      <td colname="col2"> <p>結果の単語リストに含まれるフィールド値。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>こ追加れらの語句 </p> </td> 
      <td colname="col2"> <p>検索結果のページタイトル、ブラウズページのタイトル、または項目の詳細ページのタイトルに追加する単語をリストします。 </p> <p>「<b>編集</b>」をクリックして、リストに単語を追加します。 </p> <p>1行に1つの単語またはフレーズを追加できます。 完了したら、「<b>変更を保存</b>」をクリックし、ページを閉じてメインのSEOページに戻ります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>これらの語句を削除（含まれるフィールド値を除く） </p> </td> 
      <td colname="col2"> <p>検索結果のページタイトル、ブラウズページのタイトル、または項目の詳細ページのタイトルから削除する単語をリストします。 </p> <p>「<b>編集</b>」をクリックして、削除するリストに単語を追加します。 </p> <p>1行に1つの単語またはフレーズを追加できます。 完了したら、「<b>変更を保存</b>」をクリックし、ページを閉じてメインのSEOページに戻ります。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. （オプション）「**プレビューサンプル出力**」をクリックして、設定したSEOフィールドの結果値をプレビューします。

   [設定したSEOメタタグのプレビュー](../c-about-settings-menu/c-about-seo.md#task_3F97949E193C4F92A104AD117FE49621)を参照してください。
1. 「**変更を保存**」をクリックします。
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。
1. （オプション）[!DNL SEO Search Results Word List]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## ブラウズページのリスト{#task_D7A1D765A92A4D6C94E672B3A86ECB5A}の設定

ページタイトル、説明、キーワードに含まれるブラウズページの語句のリストを設定できます。

**ブラウズページのワードリストを設定するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL SEO]**/**[!UICONTROL Browse Pages]**&#x200B;をクリックします。
1. [!DNL SEO Browse Pages Word List]ページの[!DNL Title]、[!DNL Description]、[!DNL Keywords]の各グループで、必要なオプションを設定します。

   [検索結果の単語リストの設定](../c-about-settings-menu/c-about-seo.md#task_A459A3734EC04042BA52C81184251DD4)のオプションの表を参照してください。
1. （オプション）「**プレビューサンプル出力**」をクリックして、設定したSEOフィールドの結果値をプレビューします。

   [設定したSEOメタタグのプレビュー](../c-about-settings-menu/c-about-seo.md#task_3F97949E193C4F92A104AD117FE49621)を参照してください。
1. 「**変更を保存**」をクリックします。
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。
1. （オプション）[!DNL SEO Browse Pages Word List]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 項目の詳細の単語リスト{#task_761538C519B34164BE189F13C39B2495}の設定

ページタイトル、説明、キーワードに含まれる項目の詳細な語句のリストを設定できます。

**項目の詳細の単語リストを設定するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL SEO]**/**[!UICONTROL Item Detail Pages]**&#x200B;をクリックします。
1. [!DNL SEO Item Detail Word List]ページの[!DNL Title]、[!DNL Description]、[!DNL Keywords]の各グループで、必要なオプションを設定します。

   [検索結果の単語リストの設定](../c-about-settings-menu/c-about-seo.md#task_A459A3734EC04042BA52C81184251DD4)のオプションの表を参照してください。
1. （オプション）「**プレビューサンプル出力**」をクリックして、設定したSEOフィールドの結果値をプレビューします。

   [設定したSEOメタタグのプレビュー](../c-about-settings-menu/c-about-seo.md#task_3F97949E193C4F92A104AD117FE49621)を参照してください。
1. 「**変更を保存**」をクリックします。
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。
1. （オプション）[!DNL SEO Item Detail Word List]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 設定したSEOメタタグのプレビュー{#task_3F97949E193C4F92A104AD117FE49621}

設定したSEOフィールドの結果値をプレビューして、その使用場所に挿入された値を確認できます。

SEOフィールドには、フィールドに含める値を含めることができるので、検索結果は、指定した検索クエリに依存する場合があります。

**設定したSEOメタタグをプレビューするには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL SEO]**/**[!UICONTROL Search Result Pages]**&#x200B;をクリックします。
1. SEOページで、「**プレビューサンプル出力**」をクリックします。
1. [!DNL SEO Preview]ページの[!DNL Enter sample query]フィールドに、検索するクエリ語を入力します。
1. 「**検索**」をクリックします。

   表示される「タイトル」、「説明」、「キーワード」フィールドには、先ほど入力した検索クエリに基づいて、ページに挿入されるコンテンツが表示されます。
1. 「**閉じる**」をクリックして、メインのSEOページに戻ります。
