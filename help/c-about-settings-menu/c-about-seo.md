---
description: SEO（検索エンジンの最適化）メタタグを使用して、ページの特定の要素を調整し、検索エンジンの配置を改善できます。
seo-description: SEO（検索エンジンの最適化）メタタグを使用して、ページの特定の要素を調整し、検索エンジンの配置を改善できます。
seo-title: SEOについて
solution: Target
subtopic: SEO
title: SEOについて
topic: Settings,Site search and merchandising
uuid: 5c5d64f5-fe79-4489-85c6-399d1437f2c4
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# SEOについて{#about-seo}

SEO（検索エンジンの最適化）メタタグを使用して、ページの特定の要素を調整し、検索エンジンの配置を改善できます。

## SEOの使用 {#concept_C58BFCE720824A2B9B5F5E613CFD4C0B}

これらの各要素を、開始テキストの後に単語のリストが続く部分として定義できます。 単語のリストには、次の項目を含めることができます。

* 選択した期間（例：「先月」）にサイトで人気のある検索フレーズ。カスタムの除外の対象となります。
* ページの検索元の1つ以上のフィールドの値セット。
* リストで定義する静的な語句

SEOで最も一般的なページ要素は、ページタイトル、「キーワード」および「説明」メタタグです。 これらの3つのページ要素の設定を定義できます。 さらに、次の3種類のページのそれぞれに対して次の3つの設定を定義できます。検索結果ページ、ブラウズページおよび項目の詳細ページ

SEO設定を保存またはプレビューすると、小さなセグメントの検索（トランスポート）テンプレートが生成され、テンプレートタグを使用して他の検索テンプレートに含めること `<search-include>` ができます。 例えば、次の項目を含む別のテンプレートに「検索結果ページのタイトル」フィールドを含めることができます。

```
<search-include file="seo/seo_search_title.tpl" />
```

SEOフィールドのタグの属 `file` 性に使用でき `<search-include>` る9つの値は次のとおりです。

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

まず、前述のとお `<search-include>` り、要素内のXML検索テンプレートに目的のフィールドを含め `<general>` ます。

次に、各タグをタグと `<search-include>` タグで囲 `<general-field>` み、 `</general-field>` 次の例のように、属性 `name` にフィールド名を指定します。

```
<general> 
    <general-field name="seo_search_title"><search-include file="seo/seo_search_title.tpl" /></general-field> 
    <general-field name="seo_search_description"><search-include file="seo/seo_search_description.tpl" /></general-field> 
    <general-field name="seo_search_keywords"><search-include file="seo/seo_search_keywords.tpl" /></general-field> 
</general>
```

次の例のように、プレゼンテーションテンプレートで、タグ `<guided-general-field>` を使用して、必要な場所に名前の付いたフィールドを挿入できます。

```
<title><guided-general-field gsname="default" field="seo_search_title"></title> 
<meta name="description" content="<guided-general-field gsname="default" field="seo_search_description">"/> 
<meta name="keywords" content="<guided-general-field gsname="default" field="seo_search_keywords">"/>
```

属性を使用して、「デ `gsname` フォルト」の検索を指定します。この場合は、

また、Webページで使用できる9種類のSEOフィールドを定義できます。 以下が含まれます。

* 検索結果ページ — タイトル、説明、キーワード
* ブラウズページ — タイトル、説明、キーワード
* 項目の詳細ページ — タイトル、説明、キーワード

9つのフィールドはすべて同様の設定で定義されます。 実際、「検索結果ページ」の「タイトル」フィールドなど、9つのフィールドの名前は、使用方法の提案に過ぎません。 プレゼンテーションテンプレートや検索テンプレートの任意のコンテキストで、任意のフィールドを使用できます。

テンプレートにつ [いても参照](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5)。

「プレゼンテーションテ [ンプレートタグ」も参照してくださ](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)い。

「検索テンプレート [タグ」も参照してくださ](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)い。

検索結果のワ [ードリストの設定も参照してください](../c-about-settings-menu/c-about-seo.md#task_A459A3734EC04042BA52C81184251DD4)。

## 検索結果の単語リストの設定 {#task_A459A3734EC04042BA52C81184251DD4}

ページタイトル、説明、キーワードに含まれる検索結果の語句のリストを設定できます。

**検索結果の単語リストを設定するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL SEO]** ます **[!UICONTROL Search Result Pages]**。
1. ページ [!DNL SEO Browse Pages Word List] の各グループ、各グル [!DNL Title]ー [!DNL Description]プで、 [!DNL Keywords] 必要なオプションを設定します。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>タイトル|説明|次で始まるキーワード </p> </td> 
      <td colname="col2"> <p>単語リストの前に表示するテキストです。 </p> <p>例えば、キーワードリストを「ブランド」という語で始めたい場合があります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最頻検索を含める期間 </p> </td> 
      <td colname="col2"> <p>検索が含まれる期間。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最大検索数 </p> </td> 
      <td colname="col2"> <p>含まれる検索の最大数。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フィールド値を含む </p> </td> 
      <td colname="col2"> <p>結果の単語リストに含まれるフィールド値。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>次の語句を追加 </p> </td> 
      <td colname="col2"> <p>検索結果のページタイトル、ブラウズページのタイトル、または項目の詳細ページのタイトルに追加する単語を一覧表示します。 </p> <p>「編集」 <b>をクリックし</b> 、単語をリストに追加します。 </p> <p>1行に1つの単語またはフレーズを追加できます。 完了したら、「変更の保存」 <b>をクリックし</b>、ページを閉じてSEOのメインページに戻ります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>これらの語句を削除（含まれるフィールド値を除く） </p> </td> 
      <td colname="col2"> <p>検索結果のページタイトル、ブラウズページのタイトル、または項目の詳細ページのタイトルから削除する単語を一覧表示します。 </p> <p>「編集」 <b>をクリックし</b> 、削除リストに単語を追加します。 </p> <p>1行に1つの単語またはフレーズを追加できます。 完了したら、「変更の保存」 <b>をクリックし</b>、ページを閉じてSEOのメインページに戻ります。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. （オプション）「サンプ **ル出力のプレビュー** 」をクリックして、設定したSEOフィールドの結果の値をプレビューします。

   設定し [たSEOメタタグのプレビューを参照してください](../c-about-settings-menu/c-about-seo.md#task_3F97949E193C4F92A104AD117FE49621)。
1. 「**変更を保存**」をクリックします。
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。
1. （オプション）ページで、 [!DNL SEO Search Results Word List] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## ブラウズページのワードリストの設定 {#task_D7A1D765A92A4D6C94E672B3A86ECB5A}

ページタイトル、説明、キーワードに含まれるブラウズページの語句のリストを設定できます。

**ブラウズページのワードリストを設定するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL SEO]** ます **[!UICONTROL Browse Pages]**。
1. ページ [!DNL SEO Browse Pages Word List] の各グループ、各グル [!DNL Title]ー [!DNL Description]プで、 [!DNL Keywords] 必要なオプションを設定します。

   検索結果の単語リストの設定のオ [プションの表を参照してください](../c-about-settings-menu/c-about-seo.md#task_A459A3734EC04042BA52C81184251DD4)。
1. （オプション）「サンプ **ル出力のプレビュー** 」をクリックして、設定したSEOフィールドの結果の値をプレビューします。

   設定し [たSEOメタタグのプレビューを参照してください](../c-about-settings-menu/c-about-seo.md#task_3F97949E193C4F92A104AD117FE49621)。
1. 「**変更を保存**」をクリックします。
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。
1. （オプション）ページで、 [!DNL SEO Browse Pages Word List] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 項目の詳細の単語リストの設定 {#task_761538C519B34164BE189F13C39B2495}

ページタイトル、説明、キーワードに含まれる項目の詳細な単語やフレーズのリストを設定できます。

**項目の詳細の単語リストを設定するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL SEO]** ます **[!UICONTROL Item Detail Pages]**。
1. ページ [!DNL SEO Item Detail Word List] の各グループ、各グル [!DNL Title]ー [!DNL Description]プで、 [!DNL Keywords] 必要なオプションを設定します。

   検索結果の単語リストの設定のオ [プションの表を参照してください](../c-about-settings-menu/c-about-seo.md#task_A459A3734EC04042BA52C81184251DD4)。
1. （オプション）「サンプ **ル出力のプレビュー** 」をクリックして、設定したSEOフィールドの結果の値をプレビューします。

   設定し [たSEOメタタグのプレビューを参照してください](../c-about-settings-menu/c-about-seo.md#task_3F97949E193C4F92A104AD117FE49621)。
1. 「**変更を保存**」をクリックします。
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。
1. （オプション）ページで、 [!DNL SEO Item Detail Word List] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 設定したSEOメタタグのプレビュー {#task_3F97949E193C4F92A104AD117FE49621}

設定したSEOフィールドの結果の値をプレビューして、使用場所に何が挿入されるかを確認できます。

SEOフィールドには、含まれるフィールド値を含めることができるので、指定した検索クエリによって検索結果が異なる場合があります。

**設定したSEOメタタグをプレビューするには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL SEO]** ます **[!UICONTROL Search Result Pages]**。
1. SEOページで、「サンプル出力のプレビ **ュー」をクリックします**。
1. ページ [!DNL SEO Preview] のフィールド [!DNL Enter sample query] に、検索するクエリ用語を入力します。
1. 「**検索**」をクリックします。

   表示される「タイトル」、「説明」、「キーワード」の各フィールドには、先ほど入力した検索クエリに基づいて、ページに挿入されるコンテンツが表示されます。
1. 「閉じる **** 」をクリックして、SEOのメインページに戻ります。
