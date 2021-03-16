---
description: 「垂直更新」を使用すると、大量のデータを処理する必要なく、インデックスの一部をすばやく更新できます。
solution: Target
subtopic: Vertical Update
title: 垂直方向の更新について
topic: Index,Site search and merchandising
uuid: ded09e89-5a52-4e8c-a6f7-3e25b4191183
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---


# 垂直更新について{#about-vertical-update}

「垂直更新」を使用すると、大量のデータを処理する必要なく、インデックスの一部をすばやく更新できます。

## 垂直更新の使用{#concept_E65A70C9C2E04804BF24FBE1B3CAD899}

垂直インデックスは、実行に数秒かかるだけで、大容量のeコマースWebサイトで役立ちます。このWebサイトでは、インデックスの完全な作成またはインクリメンタル作成に数時間かかる場合があります。

垂直インデックスを生成すると、インデックス作成プロセス中の開始時間、経過時間、エラーなどのステータス情報が表示されます。

垂直インデックス作成プロセスは、いつでも停止または再開できます。

新しい縦置き版のインデックスが本番用Webサイトを更新する間、ユーザーは現在のインデックスを使用してサイトを検索し続けることができます。

>[!NOTE]
>
>この機能は、デフォルトでは[!DNL Adobe Search&Promote]では有効になっていません。 お使いの機能をアクティブにするには、テクニカルサポートにお問い合わせください。

垂直方向の更新は、特にIndexConnectorを使用して検索インデックスの内容を提供するeコマーススタイルの[!DNL Adobe Search&Promote]アカウントで使用されます。 一般的な使用例は、[!DNL Adobe Search&Promote]インデックスが検索可能な商品カタログを表し、在庫管理、在庫管理、在庫管理、価格など頻繁に変更される値をすばやく更新できる必要がある場合です。 垂直方向の更新は、各ドキュメントの一部の更新のみを除いて、増分方向のインデックスと多少似ています。一方、増分方向のインデックスは、ドキュメント全体を新しいバージョンで置き換えます。

「垂直方向の更新」とは、[!DNL Adobe Search&Promote]インデックスを列付きのテーブルとして、各列を[!DNL Adobe Search&Promote]メタデータフィールドの定義に、各行をドキュメントに対応付けるという概念を指します。 縦置き版の更新処理では、1つ以上の列が置き換えられ、他の列のコンテンツを変更する必要はありません。

コンテンツのメインソースであるIndexConnectorフィードには、インデックスの作成に必要なすべてのデータ要素が含まれ、垂直更新フィードはメインフィードのサブセットです。垂直更新フィードは、同じIndexConnector &quot;スキーマ&quot;を使用してデータ要素を定義しますが、*更新が必要なデータ項目のみ*&#x200B;が含まれます。

少なくとも、縦置き版のフィードには、(IndexConnector設定の&#x200B;**プライマリキー**&#x200B;のチェックボックスで識別される)「主キー」要素と、更新する少なくとも1つのデータ要素を含める必要があります。

例えば、プライマリIndexConnectorフィードは次のようになります（ただし、通常、他のデータ項目が多い場合）。

```xml
<?xml version="1.0" encoding="UTF-8"?>
<products>
<product>
  <id><![CDATA[123]]></id>
  <title><![CDATA[Title for product 123]]></title>
  <description><![CDATA[Description for product 123.]]></description>
  <price>3.99</price>
  <link><![CDATA[https://www.somewhere.com/products/123]]></link>
  <image><![CDATA[https://www.somewher.com/images/products/123.jpg]]></image>
  <label><![CDATA[PROD123]]></label>
  <inventory>100</inventory>
  <brand><![CDATA[brand123]]></brand>
  ...
</product>
<product>
...
</product>
</products>
```

お客様のサイトでは値が急速に変化する可能性があるので、`<price>`と`<inventory>`の値だけをすばやく更新できる必要があります。 垂直的な更新のフィードは、次のようになります。

```xml
<?xml version="1.0" encoding="UTF-8"?>
<products>
<product>
  <id><![CDATA[123]]></id>
  <price>3.50</price>
  <inventory>90</inventory>
</product>
<product>
...
</product>
</products>
```

この情報は通常、顧客のサーバー上の別のファイルに保存され、IndexConnectorの「Vertical File Path」設定はこのファイルを指します。 垂直更新プロセスは、この新しいコンテンツを読み取り、既存の[!DNL Adobe Search&Promote]インデックスを更新します。この場合は、`<price>`と`<inventory>`の値のみを更新します。 以降の検索では、新たに更新されたコンテンツが返されます。

>[!NOTE]
この例では、`<price>`と`<inventory>`のメタデータフィールドを、**垂直方向の更新フィールド**&#x200B;オプションをオンにして定義する必要があります。

[インデックス作成のリモートコントロールについて](../c-about-index-menu/c-about-remote-control-for-indexing.md#concept_C79B322190E84106A434E5C6D4A4118F)および[新しいメタタグフィールドの追加](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)も参照してください。

## ステージングされたWebサイトの垂直更新の設定{#task_46A367B0786C4C90BFFA5D3F95FD86C0}

URLを指定して、縦置き版の更新に含めるインデックスコネクタのソースを設定できます。

**ステージングされたWebサイトの垂直更新を設定するには**

1. 製品メニューで、**[!UICONTROL Index]**/**[!UICONTROL Vertical Update]**/**[!UICONTROL Configuration]**&#x200B;をクリックします。
1. **[!UICONTROL Vertical Update Configuration]**&#x200B;ページの「URLを更新」フィールドで、インデックスを作成するページのURLを指定します。

   検索ロボットは、指定されたインデックスコネクタソースで識別されたドキュメントのみを更新します。

   次の例のように、このフィールドにはインデックスコネクタURLのみを含める必要があります。

   `index:product_catalog` を参照してください。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## ライブまたはステージングされたWebサイトの垂直更新ログの表示{#task_E668E1F1240C476DAA1CA783DC728232}

垂直方向のライブ更新または段階的な垂直方向の更新が完了した場合、関連するログを表示して、発生した可能性のあるエラーをトラブルシューティングできます。

縦置き版の更新ログファイルは書き出せません。また、ログファイルを保存することもできません。 ログファイルは、次のインデックスが発生するまで表示可能です。

**ライブWebサイトまたはステージングされたWebサイトの垂直更新ログを表示するには**

1. 製品メニューで、次のいずれかの操作を行います。

   * **[!UICONTROL Index]**/**[!UICONTROL Vertical Update]**/**[!UICONTROL Live Log]**&#x200B;をクリックします。

   * **[!UICONTROL Index]**/**[!UICONTROL Vertical Update]**/**[!UICONTROL Staged Log]**&#x200B;をクリックします。

1. ログページの上部または下部で、次のいずれかの操作を行います。

   * **[!UICONTROL First]**、**[!UICONTROL Prev]**、**[!UICONTROL Next]**、**[!UICONTROL Last]**、または&#x200B;**[!UICONTROL Go to line]**&#x200B;のナビゲーションオプションを使用してログ内を移動します。

   * 表示オプション&#x200B;**[!UICONTROL Errors only]**、**[!UICONTROL Wrap line]**、または&#x200B;**[!UICONTROL Show]**&#x200B;を使用して、表示内容を絞り込みます。

