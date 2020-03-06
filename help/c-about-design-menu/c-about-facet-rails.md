---
description: Webページ上のファセットのグループを並べ替えるには、「ファセットパネル」を使用します。
seo-description: Webページ上のファセットのグループを並べ替えるには、「ファセットパネル」を使用します。
seo-title: ファセットパネルについて
solution: Target
subtopic: Navigation
title: ファセットパネルについて
topic: Design,Site search and merchandising
uuid: 6da2bd67-8c20-4955-9836-bc8ba88546c5
translation-type: tm+mt
source-git-commit: 6b3aa733b0dfaace956f0ffc25f433fefd21e15f

---


# ファセットパネルについて{#about-facet-rail}

Webページ上のファセットのグループを並べ替えるには、「ファセットパネル」を使用します。

## ファセットパネルの使用 {#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB}

ファセットは、プロパティまたは特性の1つで、検索結果を一般に分類する方法です。 例えば、製造元、価格、色はファセットのグループと見なすことができます。 各ファセットには、複数の制約や値を設定できます。 例えば、色をファセットとして使用する場合、「ファセット値」は、赤、オレンジ、黄色、緑、青、藍、紫のいずれかになります。

ファセット [についてを参照してくださ](../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5)い。

Webページ上のファセットのグループを並べ替えるには、Facet Railを使用します。 例えば、Webページの左側に検索結果のセクションがあったとします。 表示されるセクションは、上から下、カテゴリファセット、ブランドファセット、価格ファセット、最頻訪問ファセットです。 ファセットパネルを使用すると、例えば、最頻使用ファセットをカテゴリファセットの上または下に表示できます。

並べ替えを行うファセットのグループは、ファセットレールタグに属します。 ファセットは1つのファセットパネルにしか属せません。 ファセットパネルはプレゼンテーションテンプレートタグで、ファセットの1つの表現を囲みます。 このレールに属するすべてのファセットは、その単一のファセット表現を共有します。

「プレゼンテー [ションテンプレート](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5) 」タグの「テンプレートとフ [ァセットについて」を参照してくださ](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)い。

## ファセットパネルの設定 {#task_561A8FF1CAD1402B9DD33E276BBC6A0E}

ファセットパネルを追加して、プレゼンテーションレイヤーをカスタマイズできます。 Facet Railsは、Webページ上のファセットの順序に基づいて検索結果を詳細に調べるためのガイド付き検索を提供します。

<!-- 

t_configuring_facet_rail.xml

-->

ファセットレールに対して行った変更は、履歴機能を使用して元に戻すことができます。

**ファセットパネルを設定するには**

1. ファセットパネルを設定する前に、ファセットが既に追加されていることを確認し、そのタスクの一部としてファセットパネル名を指定します。

   「新しいフ [ァセットの追加」を参照してくださ](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B)い。
1. 製品メニューで、//をクリ **[!UICONTROL Design]** ックしま **[!UICONTROL Navigation]** す **[!UICONTROL Facet Rail.]**
1. ページ [!DNL Facet Rail] で、ファセットパネルに含めるファセットを選択し、ドロップダウンリスト **[!UICONTROL Sort Facets Method]** からオプションを設定します。

   <!-- 
   r_facet_rail_options.xml
   -->

   | 機能/オプション | 説明 |
   |--- |--- |
   | Facet Rail 名前 | ファセットパネルの名前を指定します。  ファセットを追加する際に、ファセットパネルの名前を作成します。  「新しいフ [ァセットの追加」を参照してください。](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B) |
   | 含まれるファセット | ファセットパネルに追加するために選択できるファセットのリストです。  を使用してファセットを並べ替える場合、 `Custom`ここでファセットを選択した順序によって、テキストボックスに表示される順序が決 `Custom Facet Order` まります。 |
   | Sort Facetsメソッド | ドロップダウンリストで、次の3つのオプションのいずれかを選択します。<ul><li>`Alpha` ファセットは、句読点文字を含め、名前に基づいてアルファベット順に並べ替えられます。</li><li>`Alpha (not case sensitive)` ファセットは、名前に対してアルファベット順に並べ替えられ、大文字と小文字は区別されず、句読点も含まれます。 </li><li>`Alpha (alphanumeric only)` ファセットは、名前に基づいてアルファベット順に並べ替えられ、句読点文字は無視されます。 </li><li>`Alpha (not case sensitive, alphanumeric only)` ファセットは、名前に対してアルファベット順に並べ替えられ、大文字と小文字は区別されず、句読点も無視されます。 </li><li>`Count` ファセットは、カウントに基づいて並べ替えられます。 </li><li>`Custom` テキストボ `Custom Facet Order` ックスを開き、各ファセットの名前を正確に入力して、ファセットの順序を定義できます。 リストから除外されたファセットラベルはすべて削除さ `Custom Facet Order` れます。</li></ul> |
   | カスタムファセットの順序 | このオプションは、コンボボックスから選択 `Custom` した場合に `Sort Facets Method` のみ使用できます。  ファセット名を1行に1つ、またはすべて1行とコンマで区切って表示できます。 ファセットラベルが定義されている場合は、括弧で囲ま `Facets Included` れたファセットラベルがリストに表示されます。  テキストボックスにファセットラベルを含め `Custom Facet Order` ないでください。  リストでファセットを選択または選択解除す `Facets Included` ると、テキストボ `Custom Facet Order` ックスが自動的に更新されます。 |

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）ページ [!DNL Facet Rail] で、次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

1. 次の手順を実行して、プレゼンテーションテンプレートを編集します。

   * プレゼンテーションテンプレート上に「ファセットテンプレート」を作成します。
   * 「ファセットテンプレート」をタグで囲 `<guided-facet-rail>` みます。

      プレゼンテーションテンプレートタ [グのファセットを参照してくださ](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)い。

      例：

      ```
      <guided-facet-rail>
        <guided-facet>
          <guided-facet-display-name/>
          ...
          </guided-facet>
        </guided-facet-rail>
      ```

      これらのタグは、プレゼンテーションテンプレートの一部を切り取って、ファセットパネルの各ファセットの繰り返し可能なパターンにします。 ファセットパネルに属する各ファセットは、この分割されたセクションを使用して出力を評価します。 最終的なプレゼンテー `<guided-facet-rail>` ションテンプレートには、1つのタグのみを表示できます。

      次のタグは、検索時に動的に値が決 `gsname` 定され、正し `<guided-facet-rail>` く置き換えられるので、内部の属性を必要としません。

      `<guided-facet>`
      `<guided-facet-display-name>`
      `<guided-facet-total-count>`
      `<guided-facet-undo-link>`
      `<guided-facet-undo-path>`
      `<guided-facet-behavior>`

   * プレゼンテーションテンプレートを保存し、ライブにプッシュします。

      詳しくは、プ [レゼンテーションまたは転送テンプレートの編集を参照してくださ](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)い。
