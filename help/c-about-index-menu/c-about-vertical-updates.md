---
description: 「垂直方向の更新」を使用すると、大量のデータを処理する必要なく、インデックスの一部をすばやく更新できます。
seo-description: 「垂直方向の更新」を使用すると、大量のデータを処理する必要なく、インデックスの一部をすばやく更新できます。
seo-title: 垂直更新について
solution: Target
subtopic: Vertical Update
title: 垂直更新について
topic: Index,Site search and merchandising
uuid: ded09e89-5a52-4e8c-a6f7-3e25b4191183
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# 垂直更新について{#about-vertical-update}

「垂直方向の更新」を使用すると、大量のデータを処理する必要なく、インデックスの一部をすばやく更新できます。

## 垂直更新の使用 {#concept_E65A70C9C2E04804BF24FBE1B3CAD899}

垂直インデックスは、実行に数秒かかるだけで、大容量のeコマースWebサイトでは、完全にまたは増分インデックスを作成するのに数時間かかる場合があり、便利です。

垂直インデックスを生成すると、インデックス作成プロセス中の開始時間、経過時間、エラーなどのステータス情報が表示されます。

垂直インデックス作成プロセスは、いつでも停止または再開できます。

新しい縦置き版のインデックスがライブWebサイトを更新する間、顧客は現在のインデックスを使用してサイトを検索し続けることができます。

>[!NOTE]
>
>この機能は、ではデフォルトでは有 [!DNL Adobe Search&Promote]効になっていません。 お使いの機能を有効にするには、テクニカルサポートにお問い合わせください。

垂直方向の更新は、検索インデックスのコンテンツを提供するためにIndexConnectorを使 [!DNL Adobe Search&Promote] 用するeコマーススタイルのアカウントで特に使用されるように意図されています。 一般的な使用例は、インデックスが検索可能な製品カタログを表し、在庫、在庫、可用性、価格など頻繁に変更される値を迅速に更新する必要がある場合です。 [!DNL Adobe Search&Promote] 縦置き版の更新は増分インデックスに似ていますが、各ドキュメントの一部のみを更新し、増分版のインデックスではドキュメント全体を新しいバージョンで置き換えます。

「垂直方向の更新」とは、インデックスを列形式のテーブルとして表示し、各列をメタデータフィールドの定義に、各行をドキュメントに対応させるという概念 [!DNL Adobe Search&Promote][!DNL Adobe Search&Promote] を指します。 縦置き版の更新処理では、1つ以上の列を置き換えます。他の列のコンテンツを変更する必要はありません。

コンテンツのメインソースであるIndexConnectorフィードには、インデックスの作成に必要なすべてのデータ要素が含まれ、垂直更新フィードはメインフィードのサブセットです。垂直更新フィードは、同じIndexConnector 「スキーマ」を使用してデータ要素を定義し、更新が必要なデータ項目のみを含みます ** 。

少なくとも、垂直更新フィードには、(IndexConnector設定の「 **Primary Key** 」チェックボックスで識別される)「主キー」要素と、更新する少なくとも1つのデータ要素を含める必要があります。

例えば、プライマリIndexConnectorフィードは次のようになります（ただし、通常は他の多くのデータ項目が含まれます）。

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

顧客のサイトで値が急速に変化する可能性があるので、 `<price>` 値と値 `<inventory>` のみを迅速に更新できる必要があります。 縦置き版の更新フィードは次のようになります。

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

この情報は通常、顧客のサーバー上の別のファイルに保存され、IndexConnectorの「Vertical File Path」設定でこのファイルが参照されます。 垂直更新プロセスは、この新しいコンテンツを読み取り、既存のインデッ [!DNL Adobe Search&Promote] クスを更新します。この場合は、との値 `<price>` のみ `<inventory>`が更新されます。 以降の検索では、新しく更新されたコンテンツが返されます。

>[!NOTE]
この例では、「フィールドを `<price>` 垂直に更新 `<inventory>` 」オプションをオンにして、メタデータフィールドとメタデータフィールドを **定義する必要があります** 。

About Remote Control for Indexing [and](../c-about-index-menu/c-about-remote-control-for-indexing.md#concept_C79B322190E84106A434E5C6D4A4118F) Adding a new meta tag fieldも参照してください [](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)。

## ステージングされたWebサイトの垂直更新の設定 {#task_46A367B0786C4C90BFFA5D3F95FD86C0}

URLを指定することで、縦置きの更新に含めるインデックスコネクタのソースを設定できます。

**ステージングされたWebサイトの垂直更新を設定するには**

1. 製品メニューで//をクリ **[!UICONTROL Index]** ックし **[!UICONTROL Vertical Update]** ます **[!UICONTROL Configuration]**。
1. ページの「 **[!UICONTROL Vertical Update Configuration]** URLの更新」フィールドで、インデックスを作成するページのURLを指定します。

   検索ロボットは、指定されたインデックスコネクタソースで識別されたドキュメントのみを更新します。

   次の例のように、このフィールドにはインデックスコネクタURLのみを含める必要があります。

   `index:product_catalog` を参照してください。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## ライブまたはステージングされたWebサイトの垂直更新ログの表示 {#task_E668E1F1240C476DAA1CA783DC728232}

ライブの垂直更新または段階的な垂直更新が完了すると、関連するログを表示して、発生した可能性のあるエラーのトラブルシューティングを行うことができます。

縦置き版の更新ログファイルは書き出せず、保存することもできません。 ログファイルは、次のインデックスが発生するまで表示可能なままです。

**ライブまたはステージングされたWebサイトの垂直更新ログを表示するには**

1. 製品メニューで、次のいずれかの操作を行います。

   * Click **[!UICONTROL Index]** > **[!UICONTROL Vertical Update]** > **[!UICONTROL Live Log]**.

   * Click **[!UICONTROL Index]** > **[!UICONTROL Vertical Update]** > **[!UICONTROL Staged Log]**.

1. ログページの上部または下部で、次のいずれかの操作を行います。

   * ナビゲーションオプシ **[!UICONTROL First]**&#x200B;ョン、、、、 **[!UICONTROL Prev]**&#x200B;また **[!UICONTROL Next]**&#x200B;はを使 **[!UICONTROL Last]**&#x200B;用して **[!UICONTROL Go to line]** ログ内を移動します。

   * 表示オプション、または **[!UICONTROL Errors only]**&#x200B;を使用 **[!UICONTROL Wrap line]**&#x200B;して、 **[!UICONTROL Show]** 表示内容を調整します。

