---
description: Facet Railを使用して、Webページ上のファセットのグループを並べ替えます。
solution: Target
subtopic: Navigation
title: Facet Railについて
topic: デザイン，サイト検索とマーチャンダイジング
uuid: 6da2bd67-8c20-4955-9836-bc8ba88546c5
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 1%

---


# Facet Railについて{#about-facet-rail}

Facet Railを使用して、Webページ上のファセットのグループを並べ替えます。

## Facet Railの使用{#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB}

ファセットは、プロパティまたは特性の1つで、検索結果を一般的に分類する手段です。 例えば、製造元、価格、色はファセットのグループと見なすことができます。 各ファセットには、複数の制約や値を設定できます。 例えば、ファセットとして色を使用した場合、「ファセット値」には、赤、オレンジ、黄、緑、青、藍、紫が含まれます。

[ファセット](../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5)についてを参照してください。

Facet Railを使用して、Webページ上のこれらのファセットグループの順序を変更します。 例えば、Webページの左側に検索結果のセクションがあったとします。 表示されるセクション、上から下へ、カテゴリファセット、ブランドファセット、価格ファセット、最頻訪問ファセット。 ファセットパネルを使用すると、例えば、最頻使用ファセットをカテゴリファセットの上または下に表示できます。

一緒に並べ替えるファセットのグループは、ファセットパネルのタグに属しています。 ファセットは、1つのファセットパネルにのみ属すことができます。 ファセットパネルはプレゼンテーションテンプレートタグで、ファセットの1つの表現を囲みます。 このレールに属するすべてのファセットは、その単一のファセット表現を共有します。

「[テンプレート](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5)とファセットについて」（「[プレゼンテーションテンプレートタグ](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)」）を参照してください。

## ファセットパネルの設定{#task_561A8FF1CAD1402B9DD33E276BBC6A0E}

ファセットパネルを追加して、プレゼンテーションレイヤーをカスタマイズできます。 Facet Railsを使用すると、Webページのファセットの順序に基づいて検索結果を詳細に調べることができるガイド付き検索をユーザーに提供できます。

<!-- 

t_configuring_facet_rail.xml

-->

Facet Railsに加えた変更は、履歴機能を使用して元に戻すことができます。

**ファセットパネルを設定するには**

1. ファセットパネルを設定する前に、ファセットが既に追加されていることを確認し、そのタスクの一部として、ファセットパネル名を指定します。

   「[新しいファセットの追加](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B)」を参照してください。
1. 製品メニューで、**[!UICONTROL Design]**/**[!UICONTROL Navigation]**/**[!UICONTROL Facet Rail.]**&#x200B;をクリックします。
1. [!DNL Facet Rail]ページで、ファセットパネルに含めるファセットを選択し、ドロップダウンリストから&#x200B;**[!UICONTROL Sort Facets Method]**&#x200B;オプションを設定します。

   <!-- 
   r_facet_rail_options.xml
   -->

   | 機能/オプション | 説明 |
   |--- |--- |
   | Facet Rail 名前 | ファセットパネルの名前を指定します。  ファセットを追加する際に、ファセットパネルの名前を作成します。  「[新しいファセットの追加](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B)」を参照してください。 |
   | 含まれるファセット | ファセットパネルに追加するために選択できるファセットのリスト。  `Custom`を使用してファセットを並べ替える場合、ここでファセットを選択する順序によって、「`Custom Facet Order`」テキストボックスに表示される順序が決まります。 |
   | Sort Facetsメソッド | ドロップダウンリストで、次の3つのオプションのいずれかを選択します。<ul><li>`Alpha` ファセットは、句読点文字を含む名前に基づいてアルファベット順に並べ替えられます。</li><li>`Alpha (not case sensitive)` ファセットは、名前に関してアルファベット順に並べ替えられ、大文字と小文字を区別せず、句読点も含めます。 </li><li>`Alpha (alphanumeric only)` ファセットは、名前に基づいてアルファベット順に並べ替えられ、句読点文字は無視されます。 </li><li>`Alpha (not case sensitive, alphanumeric only)` ファセットは、名前に関してアルファベット順に並べ替えられます。大文字と小文字は無視され、句読点は無視されます。 </li><li>`Count` ファセットは、数に基づいて並べ替えられます。 </li><li>`Custom` テ `Custom Facet Order` キストボックスを開き、各ファセットの名前を正確に入力して、ファセットの順序を定義できます。除外されたファセットラベルはすべて`Custom Facet Order`リストから削除されます。</li></ul> |
   | カスタムファセット順序 | このオプションは、`Sort Facets Method`ドロップダウンリストから`Custom`を選択した場合にのみ使用できます。  ファセット名を1行に1つずつ、またはすべてを1行とコンマで区切ってリストできます。 ファセットラベルが定義されている場合は、括弧で囲まれた`Facets Included`リストに表示されます。  「`Custom Facet Order`」テキストボックスにファセットラベルを含めないでください。  `Facets Included`リストでファセットを選択または選択解除すると、「`Custom Facet Order`」テキストボックスが自動的に更新されます。 |

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）[!DNL Facet Rail]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

1. 次の操作を行って、プレゼンテーションテンプレートを編集します。

   * プレゼンテーションテンプレート上に「ファセットテンプレート」を作成します。
   * 「ファセットテンプレート」を`<guided-facet-rail>`タグで囲みます。

      「[プレゼンテーションテンプレートタグ](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)のファセット」を参照してください。

      例：

      ```
      <guided-facet-rail>
        <guided-facet>
          <guided-facet-display-name/>
          ...
          </guided-facet>
        </guided-facet-rail>
      ```

      これらのタグは、プレゼンテーションテンプレートのセクションを切り取り、ファセットパネルの各ファセットに対して繰り返し可能なパターンとなります。 ファセットパネルに属する各ファセットは、この分割されたセクションを使用して出力を評価します。 最終的なプレゼンテーションテンプレートには、`<guided-facet-rail>`タグを1つだけ指定できます。

      次のタグは、`<guided-facet-rail>`内の`gsname`属性を必要としません。これは、値が検索時に動的に決定され、適切に置き換えられるためです。

      `<guided-facet>`
      `<guided-facet-display-name>`
      `<guided-facet-total-count>`
      `<guided-facet-undo-link>`
      `<guided-facet-undo-path>`
      `<guided-facet-behavior>`

   * プレゼンテーションテンプレートを保存し、ライブにプッシュします。

      「[プレゼンテーションまたはトランスポートテンプレートの編集](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)」を参照してください。
