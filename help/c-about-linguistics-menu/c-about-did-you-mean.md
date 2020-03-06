---
description: 顧客が検索に失敗した場合に有効な検索用語の提案を受け取るように、「Did You Mean」を設定できます。 サーチクエリは、有効な検索に結びついた検索用語のスペルを検索し、修正を入力することで作成されます。
seo-description: 顧客が検索に失敗した場合に有効な検索用語の提案を受け取るように、「Did You Mean」を設定できます。 サーチクエリは、有効な検索に結びついた検索用語のスペルを検索し、修正を入力することで作成されます。
seo-title: Did You Mean
solution: Target
title: Did You Mean
topic: Linguistics,Site search and merchandising
uuid: c5973541-3d6b-4fc9-bad4-66d4d3559fe8
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# About Did You Mean{#about-did-you-mean}

顧客が検索に失敗した場合に有効な検索用語の提案を受け取るように、「Did You Mean」を設定できます。 サーチクエリは、有効な検索に結びついた検索用語のスペルを検索し、修正を入力することで作成されます。

## Did You Meanの設定 {#task_B539D6A0043547EFB1CA19B67E762371}

顧客のクエリが検索結果を [!DNL site search/merchandising] 返さない（つまり最小限に抑える）場合に、検索の提案をどのように行うかを調整できます。

<!-- 

t_configuring_did_you_mean.xml

 -->

**Did You Meanを設定するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Linguistics]** クしま **[!UICONTROL Did You Mean]**&#x200B;す。
1. ページの「 [!DNL Did You Mean] サーチクエリから **次の単語を削除** 」テキストフィールドに、望ましくないサーチクエリをフィルターするために、スペースまたは行で区切った単語を入力します。

   これらの単語は、推奨される代替検索用語として表示されない検索インデックス内の単語です。 正規表現を使用して、パターンに一致する任意の単語を除外できます。 それ以外の場合は、正確な単語だけが削除されます。

1. 目的の「 **Did You Mean** 」オプションを設定します。

   <!-- 
   
   r_did_you_mean_options.xml
   
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
      <td colname="col1"> <p>提案アルゴリズム </p> </td> 
      <td colname="col2"> <p>提案を見つけるためにソフトウェアがどの程度まで移動するかを調整します。 ユーザーが1文字の誤りを犯した場合、すべてのアルゴリズムで同じ提案が生成されます。 理由は、1つの編集で作業提案に到達し、すべてのアルゴリズムで元のアルゴリズムに近い単語が見つかるからです。 ただし、元の検索用語がインデックス内の既存の用語と似ていない場合は、 <b>Deep</b> Spellers <b>Suggestionアルゴリズムと</b> Bad Spellers Algorithmアルゴリズムで引き続き候補が検索されます。 このシナリオは、入力が困難な正しい名前を顧客が試み、その名前を聞き出す場合に役立ちます。 ただし、類似した提案のみを表示する場合は、クイックアルゴリズムを選択 <b>できます</b> 。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>表示する提案のデフォルトの数 </p> </td> 
      <td colname="col2"> <p>顧客の検索で結果が返されない場合に表示する、「Did You Mean」キーワードの提案(0 ～ 20)の数を指定します。 デフォルトは 3 です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>提案単語の最小長 </p> </td> 
      <td colname="col2"> <p>プルーニングされた単語の最小文字数を指定して、キーワードを意味しました。 </p> <p>例えば、値を4に設定した場合、1、2、3文字の単語は推奨されません。 値を0に指定した場合、短い単語はキーワードの提案から削除されません。 高い値を指定すると、通常はキーワードの提案が行われません。 デフォルト値は 3 です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最小インデックス頻度 </p> </td> 
      <td colname="col2"> <p> 単語がDid You Mean辞書に含まれる前に、その単語がインデックスに出現する必要がある最小回数を指定します。 </p> <p>フィールドに負の数を指定することはできません。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>検索結果が見つからない場合は、提案用語を検索します。 </p> </td> 
      <td colname="col2"> <p>顧客の検索で結果が得られず、少なくとも1つの「Did You Mean」という用語の提案がある場合、最初に提案された用語を自動的に再検索します。 </p> <p>プレゼンテーションテンプレートで次のタグを使用して、サイト検索/マーチャンダイジングが自動的に別のキーワードを検索することを示すことができます。 </p> <p> <code>&nbsp;&lt;guided-if-suggestion-autosearch&gt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Search&nbsp;for&nbsp;&lt;guided-param&nbsp;gsname="q"&nbsp;/&gt;&nbsp;instead&nbsp;of&nbsp;guided-suggestion-original-query&nbsp;/&gt;&nbsp;&lt;/guided-if-suggestion-autosearch&gt;</code> </p> <p>他の提案をここに表示することもできます。 </p> <p> <code>&nbsp;&lt;guided-if-suggestion-autosearch&gt;&nbsp;&nbsp;There&nbsp;was&nbsp;0&nbsp;matches&nbsp;for&nbsp;&lt;guided-suggestion-original-query&nbsp;/&gt;&nbsp;&nbsp;&nbsp;Did&nbsp;You&nbsp;Mean&nbsp;&lt;guided-param&nbsp;gsname="q"&gt;?&nbsp;Here&nbsp;are&nbsp;the&nbsp;results&nbsp;for&nbsp;that&nbsp;search.&nbsp;&nbsp;&nbsp;Or&nbsp;Did&nbsp;You&nbsp;Mean&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestions&gt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestion-link&gt;&lt;guided-suggestion&nbsp;/&gt;&lt;/guided-suggestion-link&gt;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-suggestions&gt;&nbsp;&lt;/guided-if-suggestion-autosearch&gt;</code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>結果が低いので提案を行う </p> </td> 
      <td colname="col2"> <p>顧客が10件未満の検索結果を得る用語を検索した場合、検索エンジンは100件を超える結果を得る可能性のある提案があるかどうかを確認します。 その場合は、次のタグを使用して、検索結果がある間に他の検索を希望した可能性があることをユーザーに示すことができます。 </p> <p> <code>&nbsp;&lt;guided-if-suggestion-low-results&gt; &nbsp;&nbsp;You&nbsp;have&nbsp;a&nbsp;low&nbsp;result&nbsp;count&nbsp;for&nbsp;&lt;Search&nbsp;for&nbsp;guided-param&nbsp;gsname="q"&gt;.&nbsp;&nbsp;Did&nbsp;you&nbsp;mean:&nbsp;&lt;guided-suggestion&gt;&lt;guided-suggestion-link&gt;&lt;guided-suggestion&nbsp;/&gt;&lt;/guided-suggestion-link&gt;&lt;guided-if-not-last&gt;,&nbsp;&lt;/guided-if-not-last&gt;&lt;/guided-suggestions&gt;&nbsp;&lt;/guided-if-suggestion-low-results&gt;</code> </p> <p> 上記のシナリオでは、提案の数は、「表示する提案のデフォルトの数」で指定さ <span class="uicontrol"> れた値で制御されます</span>。 低しきい値と高しきい値は、以下のオプションで設定できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最初の結果が </p> </td> 
      <td colname="col2"> <p>システムが提案を提供し始めたときの結果の数を制御します。 </p> <p>このオプションは、「結果が少ないので提案を <span class="uicontrol"> 行う」をオンにした場合にのみ表示されます</span>。 </p> <p>デフォルトは 10 です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>提案は、少なくともこの数の結果を生み出す必要があります </p> </td> 
      <td colname="col2"> <p>プライマリ検索での検索結果が少ないことが原因で提案された結果を、結果数でフィルタします。 </p> <p>このオプションは、「結果が少ないので提案を <span class="uicontrol"> 行う」をオンにした場合にのみ表示されます</span>。 </p> <p>デフォルトは 100 です。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 「**変更を保存**」をクリックします。
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

