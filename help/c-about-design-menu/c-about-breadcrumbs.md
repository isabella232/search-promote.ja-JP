---
description: パンくずリストは、Webサイトに追加できるナビゲーションコントロールです。 パンくずリストでは、検索結果セット内の場所に関するフィードバックが表示されます。 また、前の手順にすばやく戻すのに役立ちます。
seo-description: パンくずリストは、Webサイトに追加できるナビゲーションコントロールです。 パンくずリストでは、検索結果セット内の場所に関するフィードバックが表示されます。 また、前の手順にすばやく戻すのに役立ちます。
seo-title: パンくずリストについて
solution: Target
subtopic: Navigation
title: パンくずリストについて
topic: Design,Site search and merchandising
uuid: 3e630a72-a631-4f4f-8aa5-adf2882cdf1c
translation-type: tm+mt
source-git-commit: 7f1b5d94e8002992d62ec1e3dce11f9c5605fde8

---


# パンくずリストについて{#about-breadcrumbs}

パンくずリストは、Webサイトに追加できるナビゲーションコントロールです。 パンくずリストでは、検索結果セット内の場所に関するフィードバックが表示されます。 また、前の手順にすばやく戻すのに役立ちます。

## パンくずリストの使用 {#concept_FB8A943C594A4A1593B118141DA61F03}

パンくずリストでは、検索された用語と、結果セットを絞り込むために選択された後続のファセットを追跡します。

パンくずリストの設定を使用して、検索プレゼンテーションレイヤーのパンくずリストの制御をカスタマイズします。 プレゼンテーションレイヤーに複数の検索結果が含まれる場合、階層リンクコントロールはページのプライマリ検索に対して動作します。

パンくずリストを編集して、デフォルトの動作、最大値の幅、値の拡張子を変更したり、クエリー用語を含めるかどうかを選択したりできます。

## Adding a new breadcrumb {#task_2FFA94F82AE74F10BDDE7367CDCEAE8B}

顧客がWebサイトのどこにいるかを追跡できるように、階層リンクバーを追加できます。

<!-- 

t_adding_a_new_breadcrumb.xml

 -->

>[!NOTE]
>
>Webサイトに表示されるように、プレゼンテーションテンプレートの階層リンクを必ず参照してください。

**新しい階層リンクを追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Design]** ックし **[!UICONTROL Navigation]** ます **[!UICONTROL Breadcrumbs]**。
1. ページ上で、 [!DNL Breadcrumbs] をクリックしま **[!UICONTROL Add Breadcrumb]**&#x200B;す。
1. ページ [!DNL Add Breadcrumb] で、必要なオプションを設定します。

   これらの設定は、階層リンクの動作とデフォルト表示の両方に影響します。 これらの設定の一部は、プレゼンテーションテンプレートの設定を使用して上書きできます。

   <!-- 
   
   r_breadcrumb_options.xml
    
    -->

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>階層リンク名 </p> </td> 
      <td colname="col2"> <p>階層リンクの名前。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>動作 </p> </td> 
      <td colname="col2"> <p>次の3つのパンくずリストのいずれかの動作を設定します。 </p> <p> 
      <ul id="ul_7E66ACC1DA494B20BEC3B0B2CCAB103A"> 
        <li id="li_D81876660A8B48AFB70D3317063FBF6F"> <span class="uicontrol"> 移動 </span> <p>Gotoは、クリックされたパンくずリストの後にあるすべてのパンくずリストを削除し、その時点で新しい検索を開始します。 </p> </li> 
        <li id="li_63AE06B544B64DCAA8C55031B3DFFFF7"> <span class="uicontrol"> 削除 </span> <p>顧客がクリックした階層リンクから削除をパスから削除し、新しい検索を開始します。 この動作は、検索をドリルダウンする際に、ユーザーがステップを取り消せるようにする場合に便利です。 </p> </li> 
        <li id="li_EEC810D420FF41498ECE49EBAAB33BE5"> <span class="uicontrol"> ドロップ </span> <p>ドロップすると、すべてのパンくずリストが削除されます。 </p> </li> 
      </ul> </p> <p> 例えば、1 &gt; 2 &gt; 3 &gt; 4の階層リンクがあるとします。 顧客が「2」をクリックすると、選択した動作に基づいて、次の結果が得られます。 </p> <p> 
      <ul id="ul_96FCD8E4C3704B45B59BC18A7A1AC52A"> 
        <li id="li_B880037088DF426F880788EAA3072180">移動先 — 1 &gt; 2 </li> 
        <li id="li_D0F07A15DCD043EFA4563632ED33A9E2">削除 — 1 &gt; 3 &gt; 4 </li> 
        <li id="li_D848ED44B4E44538AA92010F9F186224"> ドロップ — 階層リンク全体が削除され、顧客がドリルダウンを開始する前のポイントに戻ります。 </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最大値の幅 </p> </td> 
      <td colname="col2"> <p>パンくずリストの各値の長さを指定します。 設定は文字数で指定します。 </p> <p>例えば、6を指定した場合、階層リンクの経路は、スペースを含めて最長6文字まで設定できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>値の拡張子 </p> </td> 
      <td colname="col2"> <p>パンくずリストが切り捨てられた場合に使用する省略記号を指定します。 </p> <p>デフォルトでは、「。..」 （省略記号）が使用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>クエリ用語を含む </p> </td> 
      <td colname="col2"> <p>パンくずリスト内でのクエリ用語の存在を制御します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ユーザー定義のクラムを有効にする </p> </td> 
      <td colname="col2"> <p>URLで <span class="codeph"> uX=[名前]&amp;[名前]=[値]パラメーターを使用して、パンくずリストでユーザー定義項目を使用できるよう </span> にする場合に選択します。 処理ルールを使用して、このパラメーターを適切に処理できます。 </p> <p>例えば、この機能を有効にし、URLを持っている場合は、ファセットカテゴリがある場合は <code> https://search.host.com/?1=category&amp;q1=Clothes&amp;u2= 
          type&amp;type=Men&amp;x3=kind&amp;q3=Sweater </code> URLを持っていて、その場合はファセットカテゴリがあり、 <span class="codeph"><span class="varname"> men&gt; </span></span><span class="codeph"><span class="varname"></span></span><span class="codeph"></span>パンくずリストがある場合はURLを持っています。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ユーザー定義のクラム名 </p> </td> 
      <td colname="col2"> <p>ユーザー定義のパンくずリスト項目のすべての可能な名前のコンマ区切りリストです。 </p> <p>このオプションは、「ユーザー定義のクラムを有効にする」をオ <span class="uicontrol"> ンにした場合にのみ使用できま </span>す。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Add]**.
1. （オプション）ページ [!DNL Breadcrumbs] で、次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 階層リンクの編集 {#task_583481D9A23E4E0F97AEB18E72CBE13F}

追加したパンくずリストの設定を編集できます。

<!-- 

t_editing_a_breadcrumb.xml

 -->

>[!NOTE]
>
>Webサイトに表示されるように、プレゼンテーションテンプレートの階層リンクを必ず参照してください。

**パンくずリストを編集するには**

1. 製品メニューで//をクリ **[!UICONTROL Design]** ックし **[!UICONTROL Navigation]** ます **[!UICONTROL Breadcrumbs]**。
1. ページ [!DNL Breadcrumbs] で、階層リンク **[!UICONTROL Edit]** 名の一番右をクリックします。
1. ページ [!DNL Edit Breadcrumb] で、必要なオプションを設定します。

   「新しいパンくずリストの追加」のオ [プションの表を参照してくださ](../c-about-design-menu/c-about-breadcrumbs.md#task_2FFA94F82AE74F10BDDE7367CDCEAE8B)い。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）ページ **[!UICONTROL Breadcrumb]** で、次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 階層リンクの削除 {#task_401C6E481A744284906E15A29E04F757}

追加したパンくずリストは削除できます。

<!-- 

t_deleting_a_breadcrumb.xml

 -->

**階層リンクを削除するには**

1. 製品メニューで//をクリ **[!UICONTROL Design]** ックし **[!UICONTROL Navigation]** ます **[!UICONTROL Breadcrumbs]**。
1. ページ [!DNL Breadcrumbs] で、階層リンク **[!UICONTROL Delete]** 名の一番右をクリックします。
1. ダイアログボッ [!DNL Confirmation] クスで、をクリックしま **[!UICONTROL OK]**&#x200B;す。
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

