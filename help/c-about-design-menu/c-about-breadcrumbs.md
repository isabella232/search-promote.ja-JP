---
description: パンくずリストは、Webサイトに追加できるナビゲーションコントロールです。 パンくずリストには、検索結果セット内のどこにあるかに関するフィードバックが表示されます。 また、前のステップにすばやく戻ることもできます。
solution: Target
subtopic: Navigation
title: パンくずリストについて
topic-legacy: Design,Site search and merchandising
uuid: 3e630a72-a631-4f4f-8aa5-adf2882cdf1c
exl-id: e668d706-6899-4db9-968b-d98df9090ad9
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 1%

---

# パンくずリスト{#about-breadcrumbs}について

パンくずリストは、Webサイトに追加できるナビゲーションコントロールです。 パンくずリストには、検索結果セット内のどこにあるかに関するフィードバックが表示されます。 また、前のステップにすばやく戻ることもできます。

## パンくずリスト{#concept_FB8A943C594A4A1593B118141DA61F03}の使用

パンくずリストでは、検索された用語と、結果セットを絞り込むために選択された後続のファセットを追跡します。

パンくずリストの設定を使用して、検索プレゼンテーションレイヤーのパンくずリストをカスタマイズします。 プレゼンテーションレイヤーに複数の検索結果のセットが含まれる場合、パンくずリストコントロールは、ページ上のプライマリ検索に対して機能します。

パンくずリストを編集して、デフォルトの動作、最大値の幅、値の拡張子を変更したり、クエリ項目を含めるかどうかを選択したりできます。

## 新しい階層リンクの追加{#task_2FFA94F82AE74F10BDDE7367CDCEAE8B}

顧客がWebサイトのどこにいるかを追跡できるように、階層リンクバーを追加できます。

<!-- 

t_adding_a_new_breadcrumb.xml

 -->

>[!NOTE]
>
>Webサイトに表示されるように、プレゼンテーションテンプレートの階層リンクを必ず参照してください。

**新しい階層リンクを追加するには**

1. 製品メニューで、**[!UICONTROL Design]**/**[!UICONTROL Navigation]**/**[!UICONTROL Breadcrumbs]**&#x200B;をクリックします。
1. [!DNL Breadcrumbs]ページで、**[!UICONTROL Add Breadcrumb]**&#x200B;をクリックします。
1. [!DNL Add Breadcrumb]ページで、必要なオプションを設定します。

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
      <td colname="col1"> <p>パンくずリスト名 </p> </td> 
      <td colname="col2"> <p>階層リンクの名前。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>動作 </p> </td> 
      <td colname="col2"> <p>次の3つのパンくずリストの動作のいずれかを設定します。 </p> <p> 
      <ul id="ul_7E66ACC1DA494B20BEC3B0B2CCAB103A"> 
        <li id="li_D81876660A8B48AFB70D3317063FBF6F"> <span class="uicontrol"> 移動 </span> <p>Gotoを指定すると、クリックされたパンくずリストの後にあるすべてのパンくずリストが削除され、その時点で新しい検索が開始されます。 </p> </li> 
        <li id="li_63AE06B544B64DCAA8C55031B3DFFFF7"> <span class="uicontrol"> 削除 </span> <p>顧客がクリックした階層リンクから削除を削除し、新しい検索を開始します。 この動作は、検索をドリルダウンする際の手順をユーザーが取り消せるようにする場合に役立ちます。 </p> </li> 
        <li id="li_EEC810D420FF41498ECE49EBAAB33BE5"> <span class="uicontrol"> ドロップ  </span> <p>ドロップすると、すべてのパンくずリストが削除されます。 </p> </li> 
      </ul> </p> <p> 例えば、1 &gt; 2 &gt; 3 &gt; 4の階層リンクがあるとします。 顧客が「2」をクリックすると、選択した動作に基づいて次の結果が得られます。 </p> <p> 
      <ul id="ul_96FCD8E4C3704B45B59BC18A7A1AC52A"> 
        <li id="li_B880037088DF426F880788EAA3072180">移動先 — 1 &gt; 2 </li> 
        <li id="li_D0F07A15DCD043EFA4563632ED33A9E2">削除 — 1 &gt; 3 &gt; 4 </li> 
        <li id="li_D848ED44B4E44538AA92010F9F186224"> ドロップ — 階層リンク全体がドロップされ、ドリルダウンを開始する前のポイントに顧客が戻ります。 </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最大値の幅 </p> </td> 
      <td colname="col2"> <p>パンくずリスト内の各値の長さを指定します。 設定は文字数で指定します。 </p> <p>例えば、6に設定した場合、階層リンクの末尾は、スペースを含めて最大6文字になります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>値の拡張子 </p> </td> 
      <td colname="col2"> <p>パンくずリストが切り捨てられた場合に使用する省略記号を指定します。 </p> <p>デフォルトでは、「。..」 （楕円）が使用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>クエリ用語を含む </p> </td> 
      <td colname="col2"> <p>パンくずリスト内のクエリ用語の存在を制御します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ユーザー定義のバンクリを有効にする </p> </td> 
      <td colname="col2"> <p>URLに<span class="codeph"> uX=[名前]&amp;[名前]=[値] </span>パラメーターを使用して、パンくずリストでユーザー定義項目を使用できるようにします。 処理ルールを使用して、このパラメーターを適切に処理できます。 </p> <p>例えば、この機能を有効にし、URLを<code> https://search.host.com/?1=category&amp;q1=Clothes&amp;u2= 
          type&amp;type=Men&amp;x3=kind&amp;q3=Sweater </code>持っている場合、ファセット<span class="codeph"> <span class="varname">カテゴリ</span> </span>および<span class="codeph"> </span> </span>の場合、パンくずリストは<span class="codeph">衣類&gt;メン&gt;セーター</span>のようになります。.<span class="varname"> </span></p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ユーザー定義のクラム名 </p> </td> 
      <td colname="col2"> <p>ユーザー定義パンくずリスト項目のすべての可能な名前をコンマで区切ったリスト。 </p> <p>このオプションは、「<span class="uicontrol"> Enable User-Defined Crumbs </span> 」を選択した場合にのみ使用できます。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Add]**.
1. （オプション）[!DNL Breadcrumbs]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 階層リンクの編集{#task_583481D9A23E4E0F97AEB18E72CBE13F}

追加した階層リンクの設定は編集できます。

<!-- 

t_editing_a_breadcrumb.xml

 -->

>[!NOTE]
>
>Webサイトに表示されるように、プレゼンテーションテンプレートの階層リンクを必ず参照してください。

**パンくずリストを編集するには**

1. 製品メニューで、**[!UICONTROL Design]**/**[!UICONTROL Navigation]**/**[!UICONTROL Breadcrumbs]**&#x200B;をクリックします。
1. [!DNL Breadcrumbs]ページで、階層リンク名の最も右側の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。
1. [!DNL Edit Breadcrumb]ページで、必要なオプションを設定します。

   「[新しいパンくずリストの追加](../c-about-design-menu/c-about-breadcrumbs.md#task_2FFA94F82AE74F10BDDE7367CDCEAE8B)」のオプションの表を参照してください。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）**[!UICONTROL Breadcrumb]**&#x200B;ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 階層リンク{#task_401C6E481A744284906E15A29E04F757}の削除

追加したパンくずリストは削除できます。

<!-- 

t_deleting_a_breadcrumb.xml

 -->

**パンくずリストを削除するには**

1. 製品メニューで、**[!UICONTROL Design]**/**[!UICONTROL Navigation]**/**[!UICONTROL Breadcrumbs]**&#x200B;をクリックします。
1. [!DNL Breadcrumbs]ページで、階層リンク名の最も右側の&#x200B;**[!UICONTROL Delete]**&#x200B;をクリックします。
1. [!DNL Confirmation]ダイアログボックスで、**[!UICONTROL OK]**&#x200B;をクリックします。
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。
