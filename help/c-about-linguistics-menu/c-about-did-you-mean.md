---
description: 顧客が失敗した検索を試みた場合に、有効な検索用語に対する提案を受け取るように、「Did You Mean」を設定できます。 サーチクエリは、有効な検索に結びついた検索用語に対するスペルや修正を探して入力することで形成されます。
solution: Target
title: Did You Mean
topic-legacy: Linguistics,Site search and merchandising
uuid: c5973541-3d6b-4fc9-bad4-66d4d3559fe8
exl-id: c86da375-ac5f-442b-9975-6a4e1ba8a70d
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 2%

---

# {#about-did-you-mean}という意味について

顧客が失敗した検索を試みた場合に、有効な検索用語に対する提案を受け取るように、「Did You Mean」を設定できます。 サーチクエリは、有効な検索に結びついた検索用語に対するスペルや修正を探して入力することで形成されます。

## 設定の意味{#task_B539D6A0043547EFB1CA19B67E762371}

顧客のクエリが検索結果を返さない（最小限に抑える）場合に、[!DNL site search/merchandising]が検索結果をどのように提案するかをカスタマイズできます。

<!-- 

t_configuring_did_you_mean.xml

 -->

**Did You Meanを設定するには**

1. 製品メニューで、**[!UICONTROL Linguistics]**/**[!UICONTROL Did You Mean]**&#x200B;をクリックします。
1. [!DNL Did You Mean]ページの「候補からこれらの単語を削除&#x200B;**」テキストフィールドに、望ましくない提案をフィルターするために、スペースまたは行で区切った単語を入力します。**

   これらは、検索インデックス内の推奨される代替検索用語として表示されない単語です。 パターンに一致する任意の単語を、正規式を使用して除外できます。 それ以外の場合は、正確な単語だけが削除されます。

1. 必要な&#x200B;**意味**&#x200B;オプションを設定します。

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
      <td colname="col1"> <p>提案のアルゴリズム </p> </td> 
      <td colname="col2"> <p>提案を見つけるためにソフトウェアの移動範囲を調整します。 ユーザーが1文字の間違いをした場合、すべてのアルゴリズムに同じ提案が表示されます。 なぜなら、1つの編集で作業候補が見つかり、すべてのアルゴリズムで元のアルゴリズムに近い単語が見つかるからです。 しかし、元の検索用語がインデックス内の既存の用語と類似していない場合、<b>ディープ</b>と<b>NGサーチクエリアルゴリズム</b>は、引き続き候補を検索します。 このシナリオは、入力が困難な固有名を試し、その名前を聞き出す場合に役立ちます。 ただし、類似した提案のみを表示したい場合は、<b>クイック</b>アルゴリズムを選択できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>表示する提案のデフォルト数 </p> </td> 
      <td colname="col2"> <p>顧客の検索で結果が返されない場合に表示する、「あなたが平均したキーワードの提案(0 ～ 20)」の数を指定します。 デフォルトは 3 です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>提案単語の最小長 </p> </td> 
      <td colname="col2"> <p>推奨単語の最低文字数を指定して、キーワードをプルーニングします。 </p> <p>例えば、値を4に設定した場合、1、2、3文字の単語は推奨されません。 値0を指定した場合、短い単語はキーワードの候補から削除されません。 高い値を指定すると、通常は用語の提案になりません。 デフォルト値は 3 です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最小インデックス頻度 </p> </td> 
      <td colname="col2"> <p> 単語がDid You Mean辞書に含まれる前に、その単語がインデックスに出現する必要のある最小回数を指定します。 </p> <p>フィールドに負の数を指定することはできません。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>検索結果が見つからない場合は、提示キーワードを検索します </p> </td> 
      <td colname="col2"> <p>顧客の検索結果が得られず、少なくとも1つの「Did You Mean」キーワードサーチクエリが存在する場合、最初の推奨キーワードを自動的に再検索します。 </p> <p>プレゼンテーションテンプレートで次のタグを使用して、Site Search/Merchandisingが自動的に別のキーワードを検索していることを示すことができます。 </p> <p> <code>&nbsp;&lt;guided-if-suggestion-autosearch&gt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Search&nbsp;for&nbsp;&lt;guided-param&nbsp;gsname="q"&nbsp;/&gt;&nbsp;instead&nbsp;of&nbsp;guided-suggestion-original-query&nbsp;/&gt;&nbsp;&lt;/guided-if-suggestion-autosearch&gt;</code> </p> <p>その他の提案をここに表示することもできます。 </p> <p> <code>&nbsp;&lt;guided-if-suggestion-autosearch&gt;&nbsp;&nbsp;There&nbsp;was&nbsp;0&nbsp;matches&nbsp;for&nbsp;&lt;guided-suggestion-original-query&nbsp;/&gt;&nbsp;&nbsp;&nbsp;Did&nbsp;You&nbsp;Mean&nbsp;&lt;guided-param&nbsp;gsname="q"&gt;?&nbsp;Here&nbsp;are&nbsp;the&nbsp;results&nbsp;for&nbsp;that&nbsp;search.&nbsp;&nbsp;&nbsp;Or&nbsp;Did&nbsp;You&nbsp;Mean&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestions&gt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestion-link&gt;&lt;guided-suggestion&nbsp;/&gt;&lt;/guided-suggestion-link&gt;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-suggestions&gt;&nbsp;&lt;/guided-if-suggestion-autosearch&gt;</code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>結果が低いために提案を行う </p> </td> 
      <td colname="col2"> <p>顧客が10件未満の検索結果をもたらす用語を検索した場合、検索エンジンは100件を超える結果をもたらす可能性がある提案があるかどうかを確認します。 その場合は、次のタグを使用して、検索結果があるが他の検索を希望していた可能性があることをユーザーに示すことができます。 </p> <p> <code>&nbsp;&lt;guided-if-suggestion-low-results&gt; &nbsp;&nbsp;You&nbsp;have&nbsp;a&nbsp;low&nbsp;result&nbsp;count&nbsp;for&nbsp;&lt;Search&nbsp;for&nbsp;guided-param&nbsp;gsname="q"&gt;.&nbsp;&nbsp;Did&nbsp;you&nbsp;mean:&nbsp;&lt;guided-suggestion&gt;&lt;guided-suggestion-link&gt;&lt;guided-suggestion&nbsp;/&gt;&lt;/guided-suggestion-link&gt;&lt;guided-if-not-last&gt;,&nbsp;&lt;/guided-if-not-last&gt;&lt;/guided-suggestions&gt;&nbsp;&lt;/guided-if-suggestion-low-results&gt;</code> </p> <p> 上記のシナリオでは、提案の数は、<span class="uicontrol">「</span>表示する提案のデフォルト数」で指定した値で制御されます。 低しきい値と高しきい値は、以下のオプションで設定できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最初の結果が </p> </td> 
      <td colname="col2"> <p>オファーの提案に対する開始が発生した場合の結果数を制御します。 </p> <p>このオプションは、「<span class="uicontrol">結果が低いために提案を行う</span>」をオンにした場合にのみ表示されます。 </p> <p>デフォルトは 10 です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>提案は少なくともこの数の結果を生み出さなければならない </p> </td> 
      <td colname="col2"> <p>結果数によるプライマリ検索の結果が少ないことが原因でフィルターが提案したもの。 </p> <p>このオプションは、「<span class="uicontrol">結果が低いために提案を行う</span>」をオンにした場合にのみ表示されます。 </p> <p>デフォルトは 100 です。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 「**変更を保存**」をクリックします。
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。
