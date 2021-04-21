---
description: 直接ヒットを使用すると、顧客が一致する用語を検索した場合に、顧客を指定のURLにリダイレクトできます。 この種の機能を使用すると、Webサイトの検索のナビゲーションを改善できます。
solution: Target
title: ダイレクトヒットについて
topic-legacy: Rules,Site search and merchandising
uuid: 374d63c8-2b82-4165-b543-05b587757baa
exl-id: 251dfa47-f55a-469c-8fca-e187877b7759
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 1%

---

# 直接ヒットについて{#about-direct-hits}

直接ヒットを使用すると、顧客が一致する用語を検索した場合に、顧客を指定のURLにリダイレクトできます。 この種の機能を使用すると、Webサイトの検索のナビゲーションを改善できます。

## 直接ヒットの使用{#concept_C5EE074A19FD4D5B8DD21DB575E35565}

直接ヒットは2つの主要な要素で構成されます。webサイトのURLと、1つ以上のカンマ区切りの検索用語。 直接ヒットは次のように指定します。

```
    website_URL: term
    website_URL: term, term, term
```

例えば、会社のWebサイトに、すべての利用条件を指定するページがあるとします。 顧客が用語と条件を検索した場合、結果を表示する代わりに、顧客を用語と条件ページにリダイレクトできます。

```
    https://www.mycompany.com/policies.asp?article=terms: terms and conditions, terms, conditions, security
    https://www.mycompany.com/press/news.asp: press releases, press
```

クエリ用語が直接ヒットと一致しない場合、検索結果は通常の方法で返されます。

## 直接ヒットの設定{#task_64DFB8C554874C699FCC0C2F26C3669F}

検索結果を返す代わりに、WebブラウザーをURIにリダイレクトする検索用語を指定できます。

<!-- 

t_configuring_direct_hits.xml

 -->

空白行と、「#」（ハッシュ）文字で始まるコメント行が使用できます。

**ダイレクトヒットを設定するには**

1. 製品メニューで、**[!UICONTROL Rules]**/**[!UICONTROL Direct Hits]**&#x200B;をクリックします。
1. [!DNL Direct Hits]フィールドに、WebサイトのURLと、1つ以上のカンマ区切りの検索用語を入力します。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 直接ヒットのテスト{#task_1E2EA833BF90423AA0DD8C5BBFE77445}

ダイレクトヒットルールをライブにプッシュする前に、キーワードを入力してダイレクトヒットをテストできます。

<!-- 

t_testing_direct_hits.xml

 -->

ダイレクトヒットルールの対象でない用語をテストする場合は、通知するメッセージが表示されます。 このようなシナリオでは、ダイレクトヒットルールがWebサイト上で実稼動していた場合、検索結果は通常どおり返されます。 ダイレクトヒットルールが適用される用語をテストする場合、指定したURLへのリダイレクトが発生したことを知らせるメッセージが表示されます。

**直接ヒットをテストするには**

1. 製品メニューで、**[!UICONTROL Rules]**/**[!UICONTROL Direct Hits]**&#x200B;をクリックします。
1. [!DNL Test Direct Hits]フィールドに検索語句を入力し、**[!UICONTROL Test]**&#x200B;をクリックします。
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。
