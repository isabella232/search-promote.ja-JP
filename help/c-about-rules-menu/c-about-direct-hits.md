---
description: ダイレクトヒットを使用すると、顧客が一致する用語を検索する際に、顧客を指定したURLにリダイレクトできます。 このような機能を使用すると、Webサイトの検索のナビゲーションを改善できます。
seo-description: ダイレクトヒットを使用すると、顧客が一致する用語を検索する際に、顧客を指定したURLにリダイレクトできます。 このような機能を使用すると、Webサイトの検索のナビゲーションを改善できます。
seo-title: ダイレクトヒットについて
solution: Target
title: ダイレクトヒットについて
topic: Rules,Site search and merchandising
uuid: 374d63c8-2b82-4165-b543-05b587757baa
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# ダイレクトヒットについて{#about-direct-hits}

ダイレクトヒットを使用すると、顧客が一致する用語を検索する際に、顧客を指定したURLにリダイレクトできます。 このような機能を使用すると、Webサイトの検索のナビゲーションを改善できます。

## ダイレクトヒットの使用 {#concept_C5EE074A19FD4D5B8DD21DB575E35565}

直接ヒットは、2つの主要な要素で構成されます。WebサイトのURLと、1つ以上のカンマ区切りの検索用語。 直接ヒットは次のように指定します。

```
    website_URL: term
    website_URL: term, term, term
```

例えば、会社のWebサイトに、すべての利用条件を指定するページがあるとします。 顧客がキーワードと条件を検索する際に、結果を表示する代わりに、顧客をキーワードと条件のページにリダイレクトできます。

```
    https://www.mycompany.com/policies.asp?article=terms: terms and conditions, terms, conditions, security
    https://www.mycompany.com/press/news.asp: press releases, press
```

クエリー語句がどの直接ヒットにも一致しない場合、検索結果は通常の方法で返されます。

## 直接ヒットの設定 {#task_64DFB8C554874C699FCC0C2F26C3669F}

検索結果を返す代わりに、WebブラウザーをURIにリダイレクトする検索用語を指定できます。

<!-- 

t_configuring_direct_hits.xml

 -->

空白行と、「#」（ハッシュ）文字で始まるコメント行が許可されます。

**直接ヒットを設定するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Rules]** クしま **[!UICONTROL Direct Hits]**&#x200B;す。
1. このフィー [!DNL Direct Hits] ルドに、WebサイトのURLと、1つ以上の検索用語をコンマで区切って入力します。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 直接ヒットのテスト {#task_1E2EA833BF90423AA0DD8C5BBFE77445}

ダイレクトヒットルールをライブにプッシュする前に、キーワードを入力して、ダイレクトヒットをテストできます。

<!-- 

t_testing_direct_hits.xml

 -->

ダイレクトヒットルールの対象でないキーワードをテストする場合は、通知するメッセージが表示されます。 このようなシナリオでは、ダイレクトヒットルールがWebサイト上で実行されていた場合、検索結果は通常どおり返されます。 ダイレクトヒットルールの対象となる用語をテストする場合、指定したURLへのリダイレクトが発生したことを知らせるメッセージが表示されます。

**直接ヒットをテストするには**

1. 製品メニューで、/をクリッ **[!UICONTROL Rules]** クしま **[!UICONTROL Direct Hits]**&#x200B;す。
1. フィールド [!DNL Test Direct Hits] に検索語句を入力し、をクリックしま **[!UICONTROL Test]**&#x200B;す。
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

