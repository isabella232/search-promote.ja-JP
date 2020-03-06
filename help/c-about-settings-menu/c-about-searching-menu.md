---
description: 検索メニューを使用して、除外する単語、コレクション、制限、プレビューおよびフレームを設定します。
seo-description: 検索メニューを使用して、除外する単語、コレクション、制限、プレビューおよびフレームを設定します。
seo-title: 検索メニューについて
solution: Target
subtopic: Searching
title: 検索メニューについて
topic: Settings,Site search and merchandising
uuid: 072111fc-a32b-4acb-8337-cb21bcdb5542
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# 検索メニューについて{#about-the-searching-menu}

検索メニューを使用して、除外する単語、コレクション、制限、プレビューおよびフレームを設定します。

## 検索について {#concept_207105CF26B1448F8A3D223787C56AB8}

[検索]を使用して、プレゼンテーションテンプレートで参照できる名前付きの検索を定義し、カスタマイズできます。

<!-- 

c_about_searches.xml

 -->

プレゼンテーションテンプレートでは、検索モジュール内で定義された任意の名前付き検索を参照できます。 これにより、特定のテンプレートセットに対して行われる検索のタイプを簡単にカスタマイズできます。

頻繁に使用するフレーズや共通語を検索結果から除外する方法については、除外する単語の設定を [参照してください](../c-about-linguistics-menu/c-about-excluded-words.md#task_60BF6BB7A66C48479D2BBB32C0F38CDE)。

Webサイトの特定の検索可能な領域を定義する方法については、コレクションの追加を参 [照してくださ](../c-about-settings-menu/c-about-searching-menu.md#task_07732D0F00104E59AD421297A704B2F6)い。

検索結果リンクのターゲットフレームを指定する方法については、「フォームでのフ [レームの使用」を参照してくださ](../c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5)い。

HTTPリファラー、IPアドレス、またはリクエストスキーム（HTTPまたはHTTPS）に基づいて検索を制限するには、「プレビューでの値の設 [定」を参照してください](../c-about-settings-menu/c-about-searching-menu.md#task_CE267A0FF621474E80AB43B67B1C28D7)。

## 検索のヒント {#section_22F0E2BCF259459FA5F49FBCC0F09A7C}

より具体的な検索結果を得るには、次の検索のヒントを使用できます。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>検索のヒント </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>スペルチェック </p> </td> 
   <td colname="col2"> <p>検索用語のスペルが正しいことを確認します。 言語/ <span class="uicontrol"> 単語と言語で「類似 </span> 音の一致」が有効になって <span class="uicontrol"></span><span class="uicontrol"></span>いる場合、検索エンジンは検索語句に類似した語を検索しようとします。 ただし、検索用語のスペルを正しく入力することをお勧めします。 </p> <p>単語と言 <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> 語についてを参照してくださ </a>い。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>複数の単語を使用 </p> </td> 
   <td colname="col2"> <p>例： 
     <userinput>
       弊社の無料製品 
     </userinput> </p> <p>複数語のクエリは、単一語のクエリよりも絞り込まれた結果を返します。 </p> <p>例： 
     <userinput>
       弊社の無料製品 
     </userinput> 単なる結果よりも関連性の高い結果を返す 
     <userinput>
       product 
     </userinput>。 </p> <p>すべてのクエリー用語が含まれていない場合でも、関連する結果が返されることに注意してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>類似の単語を使用 </p> </td> 
   <td colname="col2"> <p>例： 
     <userinput>
       安全なプライバシー保護 
     </userinput> </p> <p>検索クエリで使用できる単語がより似ているほど、検索結果がより関連性の高いものになります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>大文字と小文字の適切な使用 </p> </td> 
   <td colname="col2"> <p>例： 
     <userinput>
       検索テンプレートの参照 
     </userinput> </p> <p>固有名詞を大文字にします。 小文字の単語を使用すると、検索エンジンはその単語の大文字と小文字を区別して一致します。 </p> <p>例えば、「 
     <userinput>
       search 
     </userinput>を指定すると、「search」、「Search」および「SEARCH」という語を含むすべてのドキュメントが検索エンジンから返されます。 ただし、 
     <userinput>
       検索 
     </userinput>の場合、検索エンジンは大文字で始まる単語のみを含むドキュメントを返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>引用符の使用 </p> </td> 
   <td colname="col2"> <p>例： 
     <userinput>
       「お前に誓う 
     </userinput> </p> <p>「お客様への誓い」など、お互いに隣接して表示する単語を検索するには、引用符を使用します。 引用符を囲まないと、検索結果には「our」、「plesge」、「to」および「you」という語が含まれますが、必ずしもその順序ではありません。 その代わりに、ドキュメント内の任意の場所、任意の順序で単語が表示されます。 </p> <p> アドバンス検索フォームのラジオボタンを使用している場合は、 <span class="uicontrol"> すべてお </span>よびすべてのラジオボタンを使用している場合は、フレーズを選択している場合にのみ、引用符を使用するこ <span class="uicontrol"> とがで </span><span class="uicontrol"></span><span class="uicontrol"></span> きます。 すべてまたはフレーズが選択さ <span class="uicontrol"> れている場 </span> 合、引用 <span class="uicontrol"> 符は無視 </span> されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>+（プラス）または — （マイナス）を使用します。 </p> </td> 
   <td colname="col2"> <p>例： 
     <userinput>
       +"template language" 
     </userinput> </p> <p>「+」を使用して、検索語句を検索結果に表示する必要があることを示します。 </p> <p> — を使用して、検索語句が検索結果に含まれていない必要があることを示します。 </p> <p>フレーズは引用符で囲む必要があります。 上の例のように、プラス記号またはマイナス記号と検索語の間にスペースを入れないでください。 </p> <p> アドバンス検索フォームのラジオボタンを使用している場合は、 <span class="uicontrol"> すべてお </span>よびすべてのラジオボタンを使用している場合は、フレーズを選択している場合にのみ、引用符を使用するこ <span class="uicontrol"> とがで </span><span class="uicontrol"></span><span class="uicontrol"></span> きます。 すべてのまたはフレーズが選択されている場合、プラス修飾子 <span class="uicontrol"> とマイナス修 </span> 飾子 <span class="uicontrol"> は無視 </span> されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>フィールド検索の使用 </p> </td> 
   <td colname="col2"> <p>例： </p> <p> 
     <ul id="ul_F7CFF7652894402E8D19D6BA49792530"> 
      <li id="li_27492EF933C5437CB2C499746EC8CF39"> 
       <userinput>
         タイトル：説明 
       </userinput> </li> 
      <li id="li_BD21505122104FD0B16A4DAD777811DA"> 
       <userinput>
         desc:"Our Team" 
       </userinput> </li> 
      <li id="li_8264630F8B3D46BF872EFEB1D69DB6BE"> 
       <userinput>
         キー：ログイン 
       </userinput> </li> 
      <li id="li_EBB81CBFC6DA45E99A524890DCD56E9F"> 
       <userinput>
         ボディ：セキュリティ 
       </userinput> </li> 
      <li id="li_6A852E35D6984A2C94144AB6C6D2DFA0"> 
       <userinput>
         alt:"今すぐ参加" 
       </userinput> </li> 
      <li id="li_F4C5699360484D12ACD62BBFB84A7904"> 
       <userinput>
         url:help 
       </userinput> </li> 
      <li id="li_B2DBBA2239E74D98868D92B3EDEF5B51"> 
       <userinput>
         target:Adobe 
       </userinput> </li> 
     </ul> </p> <p>フィールド検索を使用すると、ドキュメントの特定の部分に表示される単語に対して特定の検索を作成できます。 </p> <p>本文テキスト(body:)、タイトルテキスト(title:)、代替テキスト(alt:)、メタ説明(desc:)、メタキーワード(keys:)、URL(url:)またはメタターゲットキーワード(target:)に対してフィールド検索を実行できます。 フィールド名には小文字を使用し、その直後にコロンを付けます。 コロンと検索語の間にスペースはありません。 </p> <p>フィールド検索の後に続くのは、単語または句のみです。 フレーズは引用符で囲む必要があります。 </p> <p>フィールド名のリストボックスと共にアドバンス検索フォームを使用している場合は、フィールド名を選択したときに、単語またはフレーズの前にのみフィール <span class="uicontrol"> ド名を入 </span> 力できます。 リストボックスで他のアドバンス検索フォームフィールドが選択されている場合、特定のフィールド名は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ワイルドカードの使用 </p> </td> 
   <td colname="col2"> <p>例： </p> <p> 
     <ul id="ul_D8E3867EB15641B0A6E55AD546CCB4DD"> 
      <li id="li_CB8B8FC15EB14B13BB33BB69F5206303"> 
       <userinput>
         wh* 
       </userinput> </li> 
      <li id="li_5350A934648C4C81BD6C0875061B426B"> 
       <userinput>
         "wh* are" 
       </userinput> </li> 
      <li id="li_7965A2F7186F40039D2F0736299D11B1"> 
       <userinput>
         415-*-* 
       </userinput> </li> 
     </ul> </p> <p>ワイルドカード検索は、特定のリクエストに対する一致数を拡張します。 ワイルドカード文字として*文字が使用されます。 </p> <p>例えば、 
     <userinput>
       wh* 
     </userinput> は、「what」、「whey」、「when」、「wheth」、および「wh」で始まる他の単語を検索します。 *her*を検索すると、「here」、「wheth」、「togher」、「gathering」、および単語内の任意の場所に「her」を含む他の単語が検索されます。 </p> <p>ワイルドカードを、+および — 修飾子、フレーズの引用符、およびフィールド検索指定子と組み合わせることができます。 </p> <p>検索 
     <userinput>
       +wh* -se*ch 
     </userinput> は、「wh」で始まり、「se」で始まり「ch」で終わる単語を含まない単語を含むすべてのページを検索します。 </p> <p>検索 
     <userinput>
       "wh* are" 
     </userinput> は、「where are」、「what are」、「whey are」などのフレーズを検索します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 新しい検索定義の追加 {#task_98D3A168AB5D4F30A1ADB6E0D48AB648}

パネルを使用して、 [!DNL GS Add Search] プレゼンテーションレイヤーで、ファセット、パンくずリスト、ページナビゲーション、メニュー、最近の検索など、ガイド付き検索コンポーネントの新しい検索定義を設定および追加できます。

<!-- 

t_adding_a_new_definition.xml

 -->

新しい検索定義を追加した後は、プレゼンテーションテンプレートで参照して表示されるようにしてください。

テンプレート [についてを参照してくださ](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5)い。

**新しい検索定義を追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Searching]** ます **[!UICONTROL Searches]**。
1. ページ上で、 [!DNL Searches] をクリックしま **[!UICONTROL Add New Search]**&#x200B;す。
1. ページ **[!UICONTROL GS Add Search]** で、必要なオプションを設定します。

   <!-- 
   
   r_gs_search_options.xml
   
   -->

   プレゼンテーションテンプレートを選択する処理ルールは、これらのオプションの一部を上書きする可能性があることに注意してください。

   「新しい [検索定義の追加](../c-about-settings-menu/c-about-searching-menu.md#task_98D3A168AB5D4F30A1ADB6E0D48AB648) 」または「検索 [定義の編集」を参照してください](../c-about-settings-menu/c-about-searching-menu.md#task_AF1FFB1AEF874C13AB359C28F74BF461)。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>検索名 </p> </td> 
      <td colname="col2"> <p>定義済みの検索の名前を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ソース </p> </td> 
      <td colname="col2"> <p>使用するバックエンド検索を選択できます。 SiteSearchまたはマーチャンダイジ <span class="wintitle"> ングか </span> ら選択 <span class="wintitle"> できま </span>す。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>アカウント </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして <span class="uicontrol"> Search&amp;Promoteを選択した場合にの </span> み使用できます。 </p> <p>検索するサイト検索/マーチャンダイジングアカウントを選択できます。 通常、検索では、現在使用しているアカウント内で検索を行います。 ただし、プレゼンテーションテンプレートでは、他のアカウントのバックエンド検索を使用できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>サーバー名/IP </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして「マーチャンダイジング」を選択 <span class="uicontrol"> した場合に </span> のみ使用できます。 </p> <p>マーチャンダイジング検索でアクセ <span class="wintitle"> スするマ </span> ーチャンダイジングサーバ <span class="wintitle"> ーの完全 </span> な名前を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>サーバーポート </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして「マーチャンダイジング」を選択 <span class="uicontrol"> した場合に </span> のみ使用できます。 </p> <p>マーチャンダイジング <span class="wintitle"> サーバーの </span> ポート番号を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ピラミッド </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして「マーチャンダイジング」を選択 <span class="uicontrol"> した場合に </span> のみ使用できます。 </p> <p>マーチャンダイジングサーバー内のピラ <span class="wintitle"> ミッドを指 </span> 定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>結果数 </p> </td> 
      <td colname="col2"> <p>返す検索結果の数を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最初のページの結果数（異なる場合） </p> </td> 
      <td colname="col2"> <p>最初のページで返される結果の数を指定します。 他のページとは異なるページを使用する必要がある場合に、このオプションを使用します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>列数 </p> </td> 
      <td colname="col2"> <p>検索結果を分割する列数を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>検索の種類 </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして <span class="uicontrol"> Search&amp;Promoteを選択した場合にの </span> み使用できます。 </p> <p>次の3種類の検索から選択できます。 </p> <p> 
        <ul id="ul_2F6FA9EFD8DB49EEAB866C3D070E2644"> 
          <li id="li_ECFEBEDD86FF4DE2BB768423B3B91B5E"> <span class="uicontrol"> all </span> <p>クエリ文字列内のすべての単語を含むドキュメントを検索します。 </p> <p>検索語を無効にする前に「+」と「 — 」を使用し、これらの文字は無視されます。 </p> </li> 
          <li id="li_62EB215BDDE74DF0BF76B3BD5B96776F"> <span class="uicontrol"> 任意 </span> <p>「+」と「 — 」の単語プリフィックスを使用できます。 </p> </li> 
          <li id="li_3D71982C0BBA41AFA353069AF3F2F6D8"> <span class="uicontrol"> フレーズ </span> <p>クエリ文字列は引用符で囲まれたフレーズとして扱われ、ユーザーが入力した引用符はすべて無視されます。 </p> <p>検索語を無効にする前に「+」と「 — 」を使用し、これらの文字は無視されます。 </p> </li> 
        </ul> </p> <p> クエリ内の各単語がファセット値を選択する可能性がある場合は、プライマリ検索で常にすべてを使用する必要があ <span class="uicontrol"> りま </span>す。 </p> <p>検索クエリでの+および — 修飾子の使用に関する検索のヒントを確認できます。 </p> <p><a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">検索について</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>コレクション </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして <span class="uicontrol"> Search&amp;Promoteを選択した場合にの </span> み使用できます。 </p> <p>検索するインデックス内のコレクションを指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Promosearch </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして <span class="uicontrol"> Search&amp;Promoteを選択した場合にの </span> み使用できます。 </p> <p>指定した結果数に基づいて、検索結果からランダムに選 <span class="uicontrol"> 択を使用で </span> きます。 </p> <p>プロモサーチは、従来の概念です。 そのため、サイト検索/マーチャンダイジング内で新しいバナー管理システムを使用することをお勧めします。 </p> <p><a href="../c-about-design-menu/c-about-banners.md#concept_5BBE01FEC6134393B43CC917C8CC64DA" type="concept" format="dita" scope="local">バナーについて</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファセットパラメータの適用 </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして <span class="uicontrol"> Search&amp;Promoteを選択し、Promosearchを選 </span> 択した場合にのみ使用で <span class="uicontrol"> きます </span>。 </p> <p>プロモーション検索で、選択したファセットを使用してプロモーションを絞り込むことを指定します。 ほとんどのプロモサーチアカウントでは、このオプションは使用されません。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>一致するプロモーションがない場合にデフォルトのプロモーションを指定する </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして <span class="uicontrol"> Search&amp;Promoteを選択し、Promosearchを選 </span> 択した場合にのみ使用で <span class="uicontrol"> きます </span>。 </p> <p>プロモーションの最初の検索で何も見つからない場合に、プロモーションの別の検索を行うことを指定します。 2つ目のプロモーションの検索では、キーワードが削除されます。 代わりに、「is_default」メタデータフィールドが「yes」に設定されているプロモーションが検索されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>検索のハイライト </p> </td> 
      <td colname="col2"> <p>「ヒーローゾーン」でハイライトする、メイン検索から選択した数の結果を取り出します。 </p> <p>通常、ハイライト検索では、メイン検索と同じ検索条件が使用されますが、特定の結果をハイライトするための別のランク付けメカニズムを使用します。 メイン検索から重複が削除されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ベース検索 </p> </td> 
      <td colname="col2"> <p>このオプションは、「検索をハイライト」を選択した場 <span class="uicontrol"> 合にのみ使用できま </span>す。 </p> <p>結果をハイライト表示する検索結果を含む検索を選択できます。 重複がこの検索から削除されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>重複除外の優先度 </p> </td> 
      <td colname="col2"> <p>このオプションは、「検索をハイライト」を選択した場 <span class="uicontrol"> 合にのみ使用できま </span>す。 </p> <p>複数のハイライト検索を使用できます。 </p> <p>複数のハイライト検索がある場合、重複除外の優先順位を指定する必要があります。ここで、「1」が最も高い優先順位です。 </p> <p>例えば、2つのハイライト検索があるとします。ベストセラーと新製品 理論的には ベストセラーも新製品の可能性がある。 この場合、複製を新しい製品とメイン検索から削除します。 したがって、ベストセラーの優先順位を1に、新製品の優先順位を2に設定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>パラメーター </p> </td> 
      <td colname="col2"> <p>検索にCGIパラメータを追加できます。 </p> <p>バックエンド <a scope="local" href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita"> 検索のCGIパラメーターを参照してくだ </a>さい。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Add]**.
1. （オプション）ページで、 [!DNL Searches] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 検索定義の編集 {#task_AF1FFB1AEF874C13AB359C28F74BF461}

このパネルを使用して、ガ [!DNL Staged GS Edit Search] イド付き検索プレゼンテーションレイヤーの既存の検索定義を再設定できます。

<!-- 

t_editing_a_search_definition.xml

 -->

検索定義を編集した後、表示されるように、プレゼンテーションテンプレートでその定義を参照していることを確認します。

テンプレート [についてを参照してくださ](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5)い。

**検索定義を編集するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Searching]** ます **[!UICONTROL Searches]**。
1. ページ [!DNL Searches] の表で、変更する定 **[!UICONTROL Edit]** 義の行をクリックします。
1. ページ **[!UICONTROL GS Edit Search]** で、必要なオプションを設定します。

   <!-- 
   
   r_gs_search_options.xml
   
   -->

   プレゼンテーションテンプレートを選択する処理ルールは、これらのオプションの一部を上書きする可能性があることに注意してください。

   「新しい [検索定義の追加](../c-about-settings-menu/c-about-searching-menu.md#task_98D3A168AB5D4F30A1ADB6E0D48AB648) 」または「検索 [定義の編集」を参照してください](../c-about-settings-menu/c-about-searching-menu.md#task_AF1FFB1AEF874C13AB359C28F74BF461)。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>検索名 </p> </td> 
      <td colname="col2"> <p>定義済みの検索の名前を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ソース </p> </td> 
      <td colname="col2"> <p>使用するバックエンド検索を選択できます。 SiteSearchまたはマーチャンダイジ <span class="wintitle"> ングか </span> ら選択 <span class="wintitle"> できま </span>す。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>アカウント </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして <span class="uicontrol"> Search&amp;Promoteを選択した場合にの </span> み使用できます。 </p> <p>検索するサイト検索/マーチャンダイジングアカウントを選択できます。 通常、検索では、現在使用しているアカウント内で検索を行います。 ただし、プレゼンテーションテンプレートでは、他のアカウントのバックエンド検索を使用できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>サーバー名/IP </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして「マーチャンダイジング」を選択 <span class="uicontrol"> した場合に </span> のみ使用できます。 </p> <p>マーチャンダイジング検索でアクセ <span class="wintitle"> スするマ </span> ーチャンダイジングサーバ <span class="wintitle"> ーの完全 </span> な名前を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>サーバーポート </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして「マーチャンダイジング」を選択 <span class="uicontrol"> した場合に </span> のみ使用できます。 </p> <p>マーチャンダイジング <span class="wintitle"> サーバーの </span> ポート番号を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ピラミッド </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして「マーチャンダイジング」を選択 <span class="uicontrol"> した場合に </span> のみ使用できます。 </p> <p>マーチャンダイジングサーバー内のピラ <span class="wintitle"> ミッドを </span> 指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>結果数 </p> </td> 
      <td colname="col2"> <p>返す検索結果の数を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最初のページの結果数（異なる場合） </p> </td> 
      <td colname="col2"> <p>最初のページで返される結果の数を指定します。 他のページとは異なるページを使用する必要がある場合に、このオプションを使用します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>列数 </p> </td> 
      <td colname="col2"> <p>検索結果を分割する列数を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>検索の種類 </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして <span class="uicontrol"> Search&amp;Promoteを選択した場合にの </span> み使用できます。 </p> <p>次の3種類の検索から選択できます。 </p> <p> 
        <ul id="ul_E1D8B3DE9DB24DE4813D53F6298A03A6"> 
          <li id="li_C3DD7AA7699B477A9EE0731CFC012630"> <span class="uicontrol"> all </span> <p>クエリ文字列内のすべての単語を含むドキュメントを検索します。 </p> <p>検索語を無効にする前に「+」と「 — 」を使用し、これらの文字は無視されます。 </p> </li> 
          <li id="li_4C66B9EFEFA042908A4D3730F9F54EB0"> <span class="uicontrol"> 任意 </span> <p>「+」と「 — 」の単語プリフィックスを使用できます。 </p> </li> 
          <li id="li_37E9AD42A61C4E31A0816DFB8E71118D"> <span class="uicontrol"> フレーズ </span> <p>クエリ文字列は引用符で囲まれたフレーズとして扱われ、ユーザーが入力した引用符はすべて無視されます。 </p> <p>検索語を無効にする前に「+」と「 — 」を使用し、これらの文字は無視されます。 </p> </li> 
        </ul> </p> <p> クエリ内の各単語がファセット値を選択する可能性がある場合は、プライマリ検索で常にすべてを使用する必要があ <span class="uicontrol"> りま </span>す。 </p> <p>検索クエリでの+および — 修飾子の使用に関する検索のヒントを確認できます。 </p> <p><a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">検索について</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>コレクション </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして <span class="uicontrol"> Search&amp;Promoteを選択した場合にの </span> み使用できます。 </p> <p>検索するインデックス内のコレクションを指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Promosearch </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして <span class="uicontrol"> Search&amp;Promoteを選択した場合にの </span> み使用できます。 </p> <p>指定した結果数に基づいて、検索結果からランダムに選 <span class="uicontrol"> 択を使用で </span> きます。 </p> <p>プロモサーチは、従来の概念です。 そのため、サイト検索/マーチャンダイジング内で新しいバナー管理システムを使用することをお勧めします。 </p> <p><a href="../c-about-design-menu/c-about-banners.md#concept_5BBE01FEC6134393B43CC917C8CC64DA" type="concept" format="dita" scope="local">バナーについて</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファセットパラメータの適用 </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして <span class="uicontrol"> Search&amp;Promoteを選択し、Promosearchを選 </span> 択した場合にのみ使用で <span class="uicontrol"> きます </span>。 </p> <p>プロモーション検索で、選択したファセットを使用してプロモーションを絞り込むことを指定します。 ほとんどのプロモサーチアカウントでは、このオプションは使用されません。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>一致するプロモーションがない場合にデフォルトのプロモーションを指定する </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして <span class="uicontrol"> Search&amp;Promoteを選択し、Promosearchを選 </span> 択した場合にのみ使用で <span class="uicontrol"> きます </span>。 </p> <p>プロモーションの最初の検索で何も見つからない場合に、プロモーションの別の検索を行うことを指定します。 2つ目のプロモーションの検索では、キーワードが削除されます。 代わりに、「is_default」メタデータフィールドが「yes」に設定されているプロモーションが検索されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>検索のハイライト </p> </td> 
      <td colname="col2"> <p>「ヒーローゾーン」でハイライトする、メイン検索から選択した数の結果を取り出します。 </p> <p>通常、ハイライト検索では、メイン検索と同じ検索条件が使用されますが、特定の結果をハイライトするための別のランク付けメカニズムを使用します。 メイン検索から重複が削除されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ベース検索 </p> </td> 
      <td colname="col2"> <p>このオプションは、「検索をハイライト」を選択した場 <span class="uicontrol"> 合にのみ使用できま </span>す。 </p> <p>結果をハイライト表示する検索結果を含む検索を選択できます。 重複がこの検索から削除されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>重複除外の優先度 </p> </td> 
      <td colname="col2"> <p>このオプションは、「検索をハイライト」を選択した場 <span class="uicontrol"> 合にのみ使用できま </span>す。 </p> <p>複数のハイライト検索を使用できます。 </p> <p>複数のハイライト検索がある場合、重複除外の優先順位を指定する必要があります。ここで、「1」が最も高い優先順位です。 </p> <p>例えば、2つのハイライト検索があるとします。ベストセラーと新製品 理論的には ベストセラーも新製品の可能性がある。 この場合、複製を新しい製品とメイン検索から削除します。 したがって、ベストセラーの優先順位を1に、新製品の優先順位を2に設定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>パラメーター </p> </td> 
      <td colname="col2"> <p>検索にCGIパラメータを追加できます。 </p> <p>バックエンド <a scope="local" href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita"> 検索のCGIパラメーターを参照してくだ </a>さい。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）ページで、 [!DNL Searches] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 検索定義の削除 {#task_1D8E991E4C4146B7A7311FAE5DAA3742}

不要になったガイド検索定義を削除したり、使用したりできます。

<!-- 

t_deleting_a_search_definition.xml

 -->

テンプレート [についてを参照してくださ](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5)い。

**検索定義を削除するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Searching]** ます **[!UICONTROL Searches]**。
1. ページ [!DNL Searches] の表で、削除する定義 **[!UICONTROL Delete]** の行をクリックします。
1. ダイアログボッ [!DNL Confirmation] クスで、をクリックしま **[!UICONTROL OK]**&#x200B;す。
1. （オプション）ページで、 [!DNL Searches] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 固定された結果キーワードマネージャについて {#concept_0C5F152C029C485D8872C6795CBCD7C7}

検索結果を特定の場所に手動でピン留めできます。 これらの固定された結果は、特定の検索クエリまたはキーワードに関連付けられます。 を使用して、すべての [!DNL Pinned Result Keyword Manager] キーワードをピン留めされた結果で管理できます。

<!-- 

c_about_pinned_results_keyword_manager.xml

 -->

## 従うキーワード検索ルール {#section_ED67A24BE884468286F34FA5DFF826D7}

パネルに入力する検索クエリには、次のルールがあります。

* 先頭と末尾のスペースがクエリから削除されます。
* 次のような特殊な検索文字は使用できません。

   * アスタリスク(*)を使用したワイルドカードの一致。
   * 「必須」または「必須」にプラスまたはマイナス（+または — ）を使用しない。
   * コロン文字(:)を含むフィールド指定子がありません。
   * コンマや二重引用符（または&quot;）は使用できません。

* クエリー内で複数のキーワードまたは単語をスペースで区切ることができます。
* 大文字は小文字に変換されます。

検索用語は、そのまま記憶される。同じ検索結果を得るには、完全に同じ検索用語を再度使用する必要があります。

固定された結果では、大文字と小文字の区別がサポートされません。 すべてのキーワードの大文字は小文字に変換されます。

## 検索結果の順序変更 {#section_46FBE5279C7740A09D6DC9F54FE104AA}

パネルまたはパネル内のキーワードを検索す [!DNL Stage Add New Keyword] ると、検索結果に [!DNL Staged Edit Keyword] は次のインデックス操作の後に何が起こる可能性があるかが反映されます。 テーブル内の検索結果の順序は、3つの方法のいずれかを使用して変更できます。

1つ目の方法は、チェックボックスを使用 **[!UICONTROL Pinned]** します。 このチェックボックスを使用して、結果を特定の位置に固定します。 このチェックボックスを選択すると、チェックボックスより上のすべての検索結果もピン留めされます。 この機能により、このチェックボックスより上のすべての結果が特定の順序で表示されます。 検索結果の固定を解除すると、現在ピン留めされているすべての結果の下にドロップします。

2つ目の方法は、テーブル内でドラッグ&amp;ドロップを使用する方法です。 ドラッグ&amp;ドロップで結果を新しい位置に移動できます。 結果を新しい位置にドラッグすると、新しい位置より上のすべての結果が固定されます。 この自動固定により、残りの結果が最近ドラッグした結果の上に表示されます。

3つ目の方法は、「#」列に特定の位置を入力して、ピン結果の順序を設定する方法です。 ドラッグ&amp;ドロップとは異なり、シミュレートされた検索結果の順序は、次にパネルを開いたときにのみ明らかにな [!DNL Staged Edit Keyword] ります。 現在ピン留めされていない行の注文番号を設定すると、少なくとも多数の項目が固定されます。 現在ピン留めされている行の順序番号を設定すると、現在ピン留めされている項目内の項目の順序が設定されます。 ただし、ピン留めされた項目の数は増えません。

検索結果を保存すると、[キーワード]フィールドに同じクエリを入力して、結果を再度表示できます。

## 固定された検索結果について {#section_46780B7812F249F3B45503161C4FBDEE}

検索結果は、多くの場合、関連度スコアで並べられます。 ただし、固定検索結果は関連度スコアを無視し、自然順序を事前に決められた位置で上書きしようとします。 結果が相対的にその場所に留まるようにすることで、その上にある他の既知の検索結果を固定する必要があります。

パネルに表示される検索結果は、次のインデックスの後に表示されるものをシミュレートします。 ただし、元のドキュメントの変更や、Member Centerでの特定の設定の変更は、不一致のある結果を生み出す可能性があります。 例えば、ドキュメントの内容の変更は、インデックスの後に行われるまで不明です。

固定された結果は、関連性を無視するので、インデックスの後に同じ順序または同じ順序で表示されます。 ピン留めされていない結果は、インデックスの後で元の位置に戻ります。ピン留めされていない結果の順序は保証されません。

## Adding a new keyword {#task_8CED128DADD34D0DAD2C64B64D0D6B06}

新しいキーワードとその固定された結果を追加できます。

<!-- 

t_adding_a_new_keyword.xml

 -->

新しいキーワードを追加する際に、検索結果の順序を変更し、特定の位置に固定することができます。

**新しいキーワードを追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Searching]** ます **[!UICONTROL Pinned Results]**。
1. ページ上で、 [!DNL Pinned Keyword Results Manager] をクリックしま **[!UICONTROL Add New Keyword]**&#x200B;す。
1. ページ [!DNL Add New Keyword] のフィールド **[!UICONTROL Keyword]** に検索クエリを入力し、をクリックします **[!UICONTROL Search Keyword]**。

   <!-- 
   
   r_keyword_options.xml
   
   -->

   「テーブルを編集」ボタンを使用して、検索結果のテーブルの表示方法を調整できます。 例えば、列のリストを使用して、特定の列の表示/非表示を切り替えることができます。 ドラッグ&amp;ドロップを使用して、列の順序を並べ替えることもできます。

   次の表に、テーブルエディターに表示される列のプロパティを示します。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>列 </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Order </p> </td> 
      <td colname="col2"> <p>列の表示順序を指定します。 列をドラッグ&amp;ドロップして、自動的に順序を更新できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フィールド名 </p> </td> 
      <td colname="col2"> <p>ステージングされた新しいキーワードの追加パネルとステージされた編集キーワードパネルのシミュレ <span class="wintitle"> ートされた </span> 検索結果テーブルに表示さ <span class="wintitle"> れる列見出し </span> の名前を識別 <span class="wintitle"></span> します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>以下を含む </p> </td> 
      <td colname="col2"> <p>チェックボックスがオンの場合、「ピン留めされた結果テーブル」(Pinned Results Table)にコラムが表示されます。 このボックスが空の場合や選択が解除されている場合は、列がテーブルから消えます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URLを画像として表示 </p> </td> 
      <td colname="col2"> <p>この列に割り当てられたメタフィールドに、グラフィックまたは画像のURLが含まれている場合は、このボックスをオンにすると、HTML画像タグがその周囲に配置され、画像が表示されます。 画像が見つからないか、無効なリンクが空です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フィールドの長さ </p> </td> 
      <td colname="col2"> <p>省略記号(...)で切り詰められる前に表示するテキストの最大長を入力します。 URLを画像として表示するように列を設定した場合、このフィールドは無効です。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. （オプション）次のいずれかの操作を行います。

   * 検索結果の順序を変更します。
   * をクリ **[!UICONTROL Edit Table]** ックして、テーブルの表示を調整 [!DNL Simulated Search Results] します。 完了したら、をクリックし **[!UICONTROL Save Changes]** てパネルに戻り [!DNL Add New Keyword] ます。

1. クリック **[!UICONTROL Save Search Results]**.
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。
1. （オプション）ページで、 [!DNL Pinned Results Keyword Manager] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## キーワードの編集 {#task_30C550A7350B4394B5B43536368A84B1}

既存のキーワードとその固定結果を編集できます。

<!-- 

t_editing_a_keyword.xml

 -->

キーワードを編集する際に、検索結果の順序を変更し、特定の位置に固定することができます。

**キーワードを編集するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Searching]** ます **[!UICONTROL Pinned Results]**。
1. ページ [!DNL Pinned Keyword Results Manager] の表で、変更するキーワ **[!UICONTROL Edit]** ードの行をクリックします。
1. ページ [!DNL Edit Keyword] のフィールド **[!UICONTROL Keyword]** に検索クエリを入力し、をクリックします **[!UICONTROL Search Keyword]**。

   必ずキーワード検索のルールに従ってください。

   <!-- 
   
   r_keyword_options.xml
   
   -->

   「テーブルを編集」ボタンを使用して、検索結果のテーブルの表示方法を調整できます。 例えば、列のリストを使用して、特定の列の表示/非表示を切り替えることができます。 ドラッグ&amp;ドロップを使用して、列の順序を並べ替えることもできます。

   次の表に、テーブルエディターに表示される列のプロパティを示します。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>列 </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Order </p> </td> 
      <td colname="col2"> <p>列の表示順序を指定します。 列をドラッグ&amp;ドロップして、自動的に順序を更新できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フィールド名 </p> </td> 
      <td colname="col2"> <p>ステージングされた新しいキーワードの追加パネルとステージされた編集キーワードパネルのシミュレ <span class="wintitle"> ートされた </span> 検索結果テーブルに表示さ <span class="wintitle"> れる列見出し </span> の名前を識別 <span class="wintitle"></span> します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>以下を含む </p> </td> 
      <td colname="col2"> <p>チェックボックスがオンの場合、「ピン留めされた結果テーブル」(Pinned Results Table)にコラムが表示されます。 このボックスが空の場合や選択が解除されている場合は、列がテーブルから消えます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URLを画像として表示 </p> </td> 
      <td colname="col2"> <p>この列に割り当てられたメタフィールドに、グラフィックまたは画像のURLが含まれている場合は、このボックスをオンにすると、HTML画像タグがその周囲に配置され、画像が表示されます。 画像が見つからないか、無効なリンクが空です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フィールドの長さ </p> </td> 
      <td colname="col2"> <p>省略記号(...)で切り詰められる前に表示するテキストの最大長を入力します。 URLを画像として表示するように列を設定した場合、このフィールドは無効です。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. （オプション）次のいずれかの操作を行います。

   * 検索結果の順序を変更します。
   * をクリ **[!UICONTROL Edit Table]** ックして、テーブルの表示を調整 [!DNL Simulated Search Results] します。

      詳しくは、 [新しいキーワードの追加を参照してくださ](../c-about-settings-menu/c-about-searching-menu.md#task_8CED128DADD34D0DAD2C64B64D0D6B06)い。

      完了したら、をクリックし **[!UICONTROL Save Changes]** てパネルに戻り [!DNL Add New Keyword] ます。

1. クリック **[!UICONTROL Save Search Results]**.
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。
1. （オプション）ページで、 [!DNL Pinned Results Keyword Manager] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## キーワードの削除 {#task_F17D6357D6DD416495E6D4117899D81D}

不要になったキーワードや使用しなくなったキーワードは削除できます。

<!-- 

t_deleting_a_keyword.xml

 -->

新しいキーワードを追加する際に、検索結果の順序を変更し、特定の位置に固定することができます。

**キーワードを削除するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Searching]** ます **[!UICONTROL Pinned Results]**。
1. ページ [!DNL Pinned Keyword Results Manager] の表で、削除するキーワ **[!UICONTROL Delete]** ードの行をクリックします。
1. ページ上で、 [!DNL Delete Keyword] をクリックしま **[!UICONTROL Delete]**&#x200B;す。
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。
1. （オプション）ページで、 [!DNL Pinned Results Keyword Manager] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## コレクションについて {#concept_62E42ACE53D54EEE9273433B86259127}

コレクションを使用すると、顧客がWebサイトの特定の領域を検索できるので、探しているものをすばやく見つけることができます。

<!-- 

c_about_collections.xml

 -->

[検索について](../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8)を参照してください。

「検索フォ [ームでのコレクションの使用」を参照してくださ](../c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3)い。

例えば、顧客は、製品の販売やサポートサービスに関連するURLのコレクションを検索できます。 指定したコレクションを顧客が使用できるようにするには、検索フォームメニューの検索フォームを必ず更新してください。

コレクション設定の効果がユーザーに表示される前に、サイトインデックスを再構築します。

コレクションをテストするには、任意選択フィールドにWebサイトのURLの1つを入力し、 **[!UICONTROL Test Collections]** をクリックします **[!UICONTROL Test]**。 指定したページが属するコレクションが返されます。

各コレクションは、名前とURLマスクを持つ1行で指定されます。 URLマスクは、次の要素で構成できます。

* ～のようなフルパス `https://www.mydomain.com/products.html`
* ～のような部分的な経路 `https://www.mydomain.com/products`
* 正規表現

   マスクを正規表現にするには、コレクション名とURLマ `regexp` スクの間にキーワードを挿入します。

   正規表 [現を参照](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)。

「コレクション」フィールドの各行には、URLマスクを1つだけ含めることができます。 ただし、同じコレクション名に対して複数のURLマスクを異なる行で指定できます。 次の例には、4つの異なるコレクション名と5つのURLマスクが含まれています。

```
Company Info https://www.yoursite.com/company 
Products https://www.yoursite.com/products 
FAQs regexp ^.*/faqs 
Support https://www.yoursite.com/email_support/ 
Support https://www.yoursite.com/phone_support/
```

この例では、検索フォームを更新してこれらのコレクションを含めた後、ユーザーは定義済みの各コレクションを個別に選択して検索できます。 コレクション `Support` には、両方のURLマスクに一致するファイルが含まれるので、このコレクションを選択すると、両方のURL `www.yoursite.com/email_support/` マスクに一致するフ `www.yoursite.com/phone_support` ァイルが、両方とも検索されます。

## コレクションの追加 {#task_07732D0F00104E59AD421297A704B2F6}

コレクションを追加して、顧客がWebサイトの特定の領域を検索できるようにし、探しているものをすばやく見つけることができます。

<!-- 

t_adding_collections.xml

 -->

URLマスクの結果が顧客に表示されるように、サイトのインデックスを必ず再構築してください。

詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。

**コレクションを追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Searching]** ます **[!UICONTROL Collections]**。
1. フィールド [!DNL Collections] に、コレクション名とURLマスクアドレスを1行に1つずつ入力します。
1. （オプション）ページの [!DNL Collections] フィールドに、Webサ **[!UICONTROL Test Collections]** イトのテストURLマスクを入力し、をクリックします **[!UICONTROL Test]**。

   テストコレクションの出力ウィンドウが表示され、URLとコレクションの名前が示されます。
1. コレクションの追加が完了したら、をクリックしま **[!UICONTROL Save Changes]**&#x200B;す。
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。
1. （オプション）ページで、 [!DNL Collections] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 制限について {#concept_B5B527E04EBF4E9AB5956EEF881DDBF1}

検索を実行する前に、参照URLとIPアドレスを調べて、その場所から検索が可能かどうかを判断します。 で指定した内容によって、検索 [!DNL Restrictions] が許可されるかどうかが決まります。 検索が許可されない場合、一般的なエラーページが要求者に返されます。

<!-- 

c_about_restrictions.xml

 -->

制限の設定は、リファラーURLマスクまたはIPアドレスマスクとして指定できます。 どちらの制限も、検索を許可するマスクと、検索を拒否するマスクを含めます。

リファラーURLとIPアドレス制限条件の両方を渡す場合、検索が許可されます。 どちらの設定でも検索が許可されない場合、検索を許可する他の制限に関係なく、検索は失敗します。

例えば、検索要求の「HTTPリファラー」フィールドが「exclude」リファラーURLマスクと一致する場合、要求元IPアドレスが「include」IPアドレスマスクと一致する場合でも、検索は失敗します。 リファラーURLまたはIPアドレスに一致するマスクがない場合、デフォルトで場所が含まれます。

1行に「マスクを含む」または「マスクを除外」を入力します。

## リファラーURLマスクまたはIPアドレスマスクの制限の追加 {#task_E6FF2DD83E8D4B00A0E2809DC13A56C9}

制限の設定は、「リファラーURLマスク」または「IPアドレスマスク」のいずれかに指定できます。 どちらの制限も、検索を許可するマスクと、検索を拒否するマスクを含めます。 リファラーURLとIPアドレスの制限条件の両方を渡す場合、検索が許可されます。

<!-- 

t_adding_url_mask_or_jp_address_restrictions.xml

 -->

**リファラーURLマスクまたはIPアドレスマスクの制限を追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Searching]** ます **[!UICONTROL Restrictions]**。
1. ページ [!DNL Restrictions] で、必要な制限オプションを設定します。 リファラーURLマスクアドレス、IPアドレスマスクアドレス、またはオプションで、サイトの検索を許可されていない顧客に表示するカスタマイズしたWebページのURLアドレスを入力します。

   <!-- 
   
   r_restriction_options.xml
   
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
      <td colname="col1"> <p>リファラーURLマスク </p> </td> 
      <td colname="col2"> <p>HTTPリファラーヘッダーのリファラーURLが読み取られます。 リファラーURLに一致する最初のマスクは、マスクがインクルードマスクの場合に検索を許可するかどうかを決定します。 または、マスクが除外マスクである場合に検索を許可しないかどうかを指定します。 リファラーURLに一致するマスクがない場合、そのURLが含まれ、検索が許可されます。 </p> <p> 検索テンプレートに新しい検索フォームが含まれている場合や、検索テンプレートに「次の10」、「前の10」、「概要を非表示」などのリンクが含まれている場合は、検索結果テンプレートを「含む」マスクとして表示します。 最も簡単な方法は、次の例のように正規表現を使用する方法です。 </p> <p> <span class="codeph"> regexp ^https?://[^/]*\.atomz\.com/を含めます。*[?&amp;]sp_a=sp1000130e.*$ </span> </p> <p>次の例に、5つの異なるリファラーURLマスクを示します。 </p> <p> <code> include&nbsp;https://www.mydomain.com/search/ 
          include&nbsp;https://search.mydomain.com/ 
          include&nbsp;regexp&nbsp;^https://www.mydomain.com/help/.*/search/ 
          include&nbsp;regexp&nbsp;^https?://[^/]*\.atomz\.com/.*[?&amp;]sp_a=sp1000130e.*$ 
          exclude&nbsp;* </code> </p> <p>リファラーURLマスクが次の場合： </p> <p> <code> https://www.mydomain.com/search/searchpage.html&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          https://search.mydomain.com/advanced/&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          https://www.mydomain.com/help/products/search/advanced/&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          https://www.mydomain.com/help/products/&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] 
          https://www.anotherdomain.com/&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] 
          blank&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>IPアドレスマスク </p> </td> 
      <td colname="col2"> <p>IPアドレスに一致する最初のマスクは、マスクがインクルードマスクの場合に検索を許可するかどうかを決定します。 または、マスクが除外マスクの場合に検索を許可するかどうかを指定します。 要求元のIPアドレスに一致するマスクがない場合、そのIPアドレスが含まれ、検索が許可されます。 </p> <p>次の例は、4種類のIPアドレスマスクを示しています。 </p> <p> <code> include&nbsp;64.128.192.* 
          include&nbsp;192.168. 
          include&nbsp;regexp&nbsp;^209\.42\.97\.[1-5]+ 
          exclude&nbsp;* </code> </p> <p>参照IPアドレスマスクが次の場合： </p> <p> <code> 64.128.192.10&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          192.168.10.127&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          209.42.97.14&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          64.128.193.10&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] 
          192.169.10.14&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] 
          209.42.97.68&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>HTTPSを使用する検索のみを許可する </p> </td> 
      <td colname="col2"> <p>検索をHTTPSに制限する。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>許可されていない要求の送信先URL </p> </td> 
      <td colname="col2"> <p> 制限付きユーザーは、ここに入力したURLにリダイレクトされます。 このオプションを使用すると、サイトの検索を許可されていない顧客に対して表示するカスタムエラーページを作成できます。 </p> <p>URLを指定しない場合、制限付きユーザーがサイトを検索しようとすると、一般的なエラーページが返されます。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## プレビューについて {#concept_DF293FD3B02C467F8842C8C21D62F294}

で設定したクエリ文字列とパラメータは、検索フォ [!DNL Preview] ームがソフトウェアでテストまたはプレビューされるたびに使用されます。

<!-- 

c_about_preview.xml

 -->

See also [About Searches](../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8).

## プレビューでの値の設定 {#task_CE267A0FF621474E80AB43B67B1C28D7}

設定したプレビュー値は、検索フォームがソフトウェアでテストまたはプレビューされたときに常に使用されます。

<!-- 

t_setting_values_in_preview.xml

 -->

**プレビューで値を設定するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Searching]** ます **[!UICONTROL Preview]**。
1. ページ [!DNL Preview] で、必要なオプションを設定します。

   <!-- 
   
   r_preview_options.xml
   
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
      <td colname="col1"> <p>クエリ </p> </td> 
      <td colname="col2"> <p>デフォルトでは、クエリ文字列は <span class="codeph"> *に設定さ </span>れ、通常は結果を返します。 ただし、Webサイトのコンテンツに対してより具体的なクエリを指定できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>パラメーター </p> </td> 
      <td colname="col2"> <p>パラメーターは名前と値で設定されます。 必要な数の追加パラメーターを指定できます。 例えば、sp_q_1および <span class="codeph"> sp_x_1パラメーターを使 </span> 用して追 <span class="codeph"> 加の検索条件を指定でき </span> ます。 パラメータ値 <span class="codeph"></span> sp_q_1=windows&amp;sp_x_1=platformは、検索ページの「プラットフォーム」メタタグ内の値「windows」を検索し、メインクエリに加えてプレビュー検索を作成します。 </p> <p>バックエンド <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> 検索のCGIパラメーターを参照してくだ </a>さい。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ホスト </p> </td> 
      <td colname="col2"> <p>Webサイトでプライベートドメインのラベル付けを使用している場合は、検索結果を正確にプレビューするために適切なホスト名を設定します。 </p> <p>プライベートドメインのラベル付けについて詳しくは、カスタマーサポートにお問い合わせください。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## フィードについて {#concept_FEBFEE51A3AB49F88CBA0D16E2AD6916}

検索インデックスは、Webサイトの大きなデータベースとして表示されます。 正しいメタタグから十分な情報を得て、情報が収集され、データフィードに組織（シンジケート）されます。 これらのデータフィードは、サードパーティの受信者など、別のサービスに送信できます。

<!-- 

c_about_feeds.xml

 -->

Webサイトのクロールとインデックス作成が完了したら、自動フィードを生成し、サードパーティのオーガニック検索エンジンやショッピングエンジンに送信できます。 次のストリームフィードを作成できます。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>フィードのタイプ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Adobe Recommendations </p> </td> 
   <td colname="col2"> <p>Recommendations フィードは、Adobe Recommendationsでデータ同期機能を提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>汎用フィード </p> </td> 
   <td colname="col2"> <p>汎用フィードタイプを持つ多くのフィードを実装できます。 Webサイトのインデックスに対してカスタム検索クエリが実行されます。 データは、検索結果を表示するのと同じテンプレート言語を使用して、カスタマイズされた検索テンプレートを通じて返されます。 このような柔軟性により、特定のフィードタイプに限らず、多くのベンダーにフィードを送信できます。 </p> <p>次のヘルプトピックの手順を使用して、トランスポート（検索）テンプレートを追加できます。 </p> <p>詳しくは、新し <a href="../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012" type="task" format="dita" scope="local"> いプレゼンテーションまたは転送テンプレートファイルの追加を参照してくだ </a>さい。 </p> <p> テンプレートを追加した後、検索テンプレートタグを使用して編集し、含める検索メタデータフィールドとその形式を定義します。 </p> <p>詳しくは、プ <a href="../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3" type="task" format="dita" scope="local"> レゼンテーションまたは転送テンプレートの編集を参照してくだ </a>さい。 </p> <p>詳しくは、検索テ <a href="../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4" type="reference" format="dita" scope="local"> ンプレートタグを参照してくだ </a>さい。 </p> <p>トランスポートテンプレートファイルの名前を忘れないでください。 フィードの条件を指定する場合は、名前を使用して汎用フィードをテンプレートに連結します。 </p> <p>以前に他のフィードを扱ったことがある場合は、フィードフィールドを検索メタデータフィールドにマップすることに注意してください。 汎用フィードには、フィードの作成ウィザードのこの手順 <span class="uicontrol"> はあり </span> ません。 代わりに、テンプレートではメタデータとメタデータの形式を指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Googleマーチャント </p> </td> 
   <td colname="col2"> <p>Googleマーチャントセンターを使用すると、複数のGoogleサービスを通じて製品を販売できます。 データシンジケーションコンポーネントを備えており、定期的に販売されている製品のリストを提出できます。 </p> <p>サードパーティのフィードベンダーと同様、Google Merchant Centerには、フィードが正当と見なされる前に満たす特定の標準が用意されています。 詳しくは、顧客担当者にお問い合わせの上、Google Merchantのドキュメントを参照してください。 フィードの検証時にGoogle Merchant Centerが考慮する概要を以下に示します。 </p> 
    <ul id="ul_3D84D4A6A4BF4C08860F86403F8F9CD6"> 
     <li id="li_5B6516CC7BC7493B8B8E8AFB454E573F">各製品には製品ページがあり、専用のURL。 </li> 
     <li id="li_5A6D5AD5E1B54A94B224D19E888B5443"> 各製品バリアントは、フィードに個別のエントリを持ちます。 </li> 
     <li id="li_89748D3241B34A4493576DAC38681988"> 各製品には、好ましくはサーバーから取得した画像URLが含まれています。 製品のバリエーションには、実際のバリエーションを示す特定の画像が含まれます。 つまり、異なる靴の色で同じ画像を共有することはできません。 </li> 
     <li id="li_A594AD19480F41EAA72181355F28447B"> 各製品には、利用可能時間、条件、説明、カテゴリ、価格などの特定の情報が含まれています。 </li> 
     <li id="li_0955B3A6ED2746D2B7CB42DC8AB27D3A">一般に、各製品には、ISBN、UPC、JAN、EANなどの一意の識別子があります。 </li> 
     <li id="li_2C371653F1C5471FA638F3A3818ABC17">一般に、各製品はGoogleの製品分類法で分類されます。 </li> 
     <li id="li_6EB392A5A0BE490FAED5BC5E83228E32"> アパレル製品には、性別、年齢層、色、サイズなど、追加の必須フィールドがあります。 </li> 
     <li id="li_44B91FA9A95F4172A2F03F8206E9081E"> 税金と送料は、Google Merchant Center内またはこのフィード内の製品別のアカウント設定として指定されます。 </li> 
     <li id="li_71A63E9905B840C0A04F6CDAA23C9AB0"> 一部のルールでは、カスタムメードの製品や特定のアパレル製品を免除することができますが、その免除の許可や詳細については、Googleに問い合わせる必要があります。 </li> 
    </ul> <p>フィードの検証には、多くの詳細が適用されます。 フィード管理について詳しくは、Google Merchantのドキュメントを参照してください。 Googleは仕様を頻繁に変更するので、ドキュメントを頻繁に確認してください。 </p> <p>Google Merchant Centerに関連付けられているフィードは、多くの場合、Google製品検索フィードと呼ばれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Googleサイトマップ </p> </td> 
   <td colname="col2"> <p>Googleサイトマップを使用すると、GoogleによるWebサイトのクロール方法に影響を与えることができます。 この場合、シンジケートデータフィードは、サイトマップとして、定期的にGoogleサイトマップに送信されます。 サイトマップには、インターネットに到達可能なURLと、最終変更日やページの優先順位などの特定の情報を各URLに関連付けることができます。 このような情報をGoogleに提供すると、特定のページがクロールされ、インデックスが作成される頻度と確率が高くなります。 場合によっては、サイトマップを使用して、通常の状況でクローラーがアクセスできないリンクのリストをアドバタイズします。 </p> <p>フィード機能を使用してGoogleサイトマップを作成したい場合は、顧客担当者にお問い合わせください。 Googleは、Googleサイトマップサービスを一般の人々に提供し、Google Webマスターツールページにドキュメントを提供しています。 </p> <p> <b>Googleサイトマップフィードを作成するための要件</b> </p> <p>Googleサイトマップフィードを作成するには、Google Sitemapが既に設定されているGoogle Webmaster Toolsアカウントを持っていることを確認してください。 Googleサイトマップの設定については、Google Webmaster Toolsのドキュメントを参照してください。 </p> <p>また、サイトマップファイルの配信方法を決定する必要もあります。 一般に、サイトマップファイルはドメイン、特にWebサイトのルートから取得されます。 単純なモデルは、FTP経由でサーバーにファイルを配信することです。 もう1つの解決策は、サイトマップファイルのリクエストをサイト検索/マーチャンダイジングコンテンツネットワークにリダイレクトすることです。 サイトマップフィードの配信の調整と設定については、コンサルティング担当者にお問い合わせください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

自動フィードに興味がある場合は、プロフェッショナルサービスにお問い合わせください。 各フィードは、データの品質とファイルの送信に関しては、厳しい要件を持ちます。

選択したフィードのタイプは、ウィザードを使用してフィールドを作成する際に表示されるオプションに影響 **[!UICONTROL Create Feed]** します。 フィードのタイプごとに、異なるデータ形式があります。 フィードの受信者によるフィードの拒否や、不適切なデータの顧客への投稿を避けるために、適切なデータ形式に従ってください。 ベンダーは通常、データ形式の他に、1つ以上の推奨されるデータ受信方法を持っています。 フィードについては、ベンダーのドキュメントを参照してください。

フィードの作成に関する課題は、サイト検索/マーチャンダイジングとフィードの間でデータを一致させることです。 通常、インデックスのクロールから取得されたデータの形式が正しくないか、データが見つかりません。 次に、フィードの作成時に何を探すかに焦点を当てるのに役立つ質問の一覧を示します。

* フィードの受信者とのビジネス上の関係はどのようなタイプですか。
* 登録して、フィードの受信者にアカウントを作成する必要がありますか？
* 誰が、ベンダーに関してフィードに関する問題を監視し、対処するか。 一般に、ベンダーのアカウントを管理するのはお客様の責任です。 例えば、Googleサイトマップでは、WebMasterアカウントと、サイトマップの正常性を監視するユーザーが必要です。
* フィードのデータ形式は何ですか。
* インデックスはフィードの文字エンコーディングと一致しますか？ タブ区切りデータ形式とカンマ区切りデータ形式は、データにタブやコンマが含まれている場合に問題となります。
* データにタブやコンマが含まれている場合は、どのように処理しますか。
* インデックス内に空のデータを持つページはありますか？
* フィード受信者は空のデータを受け入れることができますか。 ソフトウェアでデータを取得する方法を条件を編集することで、空のデータを解決できます。
* データ形式は、フィードの受信者が望むものに含まれますか。 例えば、一部のフィード受信者は、価格と通貨の表示方法に固有の情報を受け取ります。
* 仕入先が受け入れ可能な最大数の品目を持っているか。 この潜在的な問題は、検索条件で結果を制限することで解決できます。
* ベンダーはどのようにフィードを受け取りたいと思っていますか。 FTP送信とHTTPホスティングがサポートされています。

## フィードの作成 {#task_63179C1FC359497483CD6CE13FD1C250}

1つ以上のデータフィードを作成できます。

<!-- 

t_creating_a_feed.xml

 -->

**フィードを作成するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Searching]** ます **[!UICONTROL Feeds]**。
1. ページで [!DNL Feeds] 、ドロップダウンリストからフィードの **[!UICONTROL Create Feed]** タイプを選択します。
1. 選択したフィードのタイプに応じて、ダイアログボ [!DNL Create Feed] ックスで、ウィザードの各パネルで指定したオプションを設定します。

   <!-- 
   
   r_feed_options.xml
   
   -->

   作成または編集するフィードのタイプによって、使用できるオプションは少し異なります。

   **Adobe Recommendations**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>パネル </p> </th> 
      <th colname="col2" class="entry"> <p>ウィザードパネル名 </p> </th> 
      <th colname="col3" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>Feed Name </p> </td> 
      <td colname="col3"> <p>フィードの名前を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>2 </p> </td> 
      <td colname="col2"> <p>フィールドマップ </p> </td> 
      <td colname="col3"> <p>ベンダー固有のフィードフィールドをサイト検索/マーチャンダイジングメタデータフィールドにマップできます。 このウィザードのマッピング手順は重要です。これは、フィードがインデックス内のフィールドとフィードデータ内のフィールドとの間の情報を関連付けることができるからです。 一般的なフィードを除くほとんどの場 <span class="wintitle"> 合、クロ </span>ス集計は動的に生成された検索テンプレートに保存されます。 </p> <p>[フィールドマップ]テーブル <span class="wintitle"> の各行は、フ </span> ィールドのマッピングを表します。 表の「追加と削除」列で、「 <span class="uicontrol"> +」をクリックし </span> て、新しいフィールドマッピング行を追加します。現在選択 <span class="uicontrol"> されて </span> いるフィールドマッピング行をテーブルから削除するには、「 — 」をクリックします。 フィードフィールドをサイト検索/マーチャンダイジングメタデータフィールドに関連付けるには、それぞれのドロップダウンリストを使用して、目的のフィールドを選択します。 </p> <p> <b>Adobe Recommendationsのフィールドマッピング</b> </p> <p>レコメンデーションデータフィードはCSVファイルで、データの列はコンマで区切られます。 CSVフィードファイル内の列の順序を決定するので、フィールドマップテーブル上の各マッピングの表示順序は重要です。 マッピングの行を次の順序で作成します。各行は必須です。 </p> <p> 
        <ol id="ol_49C739D04DD340168DC6C1F794544C35"> 
          <li id="li_A95D9C5A353746A3A0D38F200AC2EEA2"> ID </li> 
          <li id="li_044763D4C7054CEB948C94590735D74F"> name </li> 
          <li id="li_832F07CA0E3F4E10A4AE30171F3E8541"> categoryId </li> 
          <li id="li_2A33FB42F7E942ED881BA1F478542C4D"> message </li> 
          <li id="li_A76E66B2366845B0B63ED5C200531ADD"> thumbnailURL </li> 
          <li id="li_518CCD5E7E404521AB8199981BA86F76"> value </li> 
          <li id="li_14A0A8FCC2B34B758E1FBB98E3F2DFB2"> pageURL </li> 
          <li id="li_36D22F1603394AF89E0C7ADB18AAAAB7"> inventory </li> 
          <li id="li_ABDB9C762BBC4F27B82FEA4425A8DDC4"> margin </li> 
        </ol> </p> <p> <b>高度な使用方法</b> </p> <p>上述のように最初の9つの必須フィードフィールドをマッピングしたら、独自のカスタムフィールドを作成できます。 「フィードフ <span class="wintitle"> ィールド」ド </span> ロップダウンリストで、「カスタム」をクリ <span class="uicontrol"> ックしま </span>す。 関連するテキストフィールドに、そのフィールドのカスタムタグ名を入力します。 このカスタムオプションは、フィードに特別なベンダー固有のフィールドが必要な場合に役立ちます。 </p> <p> <p>注意： レコメンデーションフィードの仕様では、各フィールド名の先頭に「entity」を付ける必要があると記述されていますが、この場合は不要です。 </p> </p> <p>また、カスタムメタデータフィールドを作成することもできます。 「メタデータフ <span class="wintitle"> ィールド」ド </span> ロップダウンリストで、「カスタム」をク <span class="uicontrol"> リックしま </span>す。 関連するテキストフィールドに、カスタムメタデータフィールドの値を入力します。 この値は、事前に生成されたテンプレートに挿入され、カスタム検索テンプレートタグの挿入にも使用できます。 </p> <p>詳しくは、検索テ <a href="../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4" type="reference" format="dita" scope="local"> ンプレートタグを参照してくだ </a>さい。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>3 </p> </td> 
      <td colname="col2"> <p>検索条件 </p> </td> 
      <td colname="col3"> <p>フィードファイルが生成されると、検索クエリを使用してデータがフィルターされます。 このパネルで、検索クエリに使用するフィルタを定義します。 </p> 
        <ul id="ul_799ECF61C03A44878C7182F8B88CC3AD"> 
        <li id="li_0763F600A4FB4650ACC28BF337EB50AF"> <span class="uicontrol"> メタフィールド </span> <p>フィルタするメタデータフィールドを定義します。 </p> <p> <b>高度な使用方法</b> </p> <p>フィルタリングシステムは標準の検索クエリなので、ドロップダウンリストから「 <span class="uicontrol"> Free Form」 </span> を選択して、CGI検索パラメータとその値を入力できます。 URLエスケープが必要です。 検索引数 <span class="codeph"> sp_qは無視 </span> されます。 フリーフォームのテキストボックスは複数行作成できます。 各行の間の引数は、自動的に&amp;で区切られます。 </p> <p>CGIパラメータ <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> ーの検索を参照してくだ </a>さい。 </p> </li> 
        <li id="li_756B776902AE4A0E95524442D663343E"> <span class="uicontrol"> 条件 </span> <p>フィルター操作を定義します。 ドロップダウンリストから選択したフィルタリング操作により、3列目に入力した定数値が適用されます。 </p> </li> 
        <li id="li_7ADEDB8747B241D78AC50F1AC75AE695"> <span class="uicontrol"> 値 </span> <p>定数値。 </p> </li> 
        <li id="li_4039A9BC2F74460B83BFF662B58DAA1B"> <span class="uicontrol"> アクション </span> <p>新しいフィールドマッピング行を追加するか、現在ハイライトされている行を削除します。 </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>4 </p> </td> 
      <td colname="col2"> <p>ファイル送信 </p> </td> 
      <td colname="col3"> <p>フィードファイルの送信スケジュールを設定し、ファイルのアップロードに使用する方法を設定できます。 </p> 
        <ul id="ul_55E253F83BDA46BAABF2BE38F0918E80"> 
        <li id="li_877A376B5B30422FAC816E31D50EA508"> <span class="uicontrol"> スケジュール </span> <p>フィードが送信される最大頻度を設定します。 「なし」を <span class="uicontrol"> 選択する </span> と、フィードがオフになります。 その他の値は、フィードが再び送信されるまで待機する期間を定義します。 フィードを送信するタイミングの決定は、各インデックスで行われます。 つまり、インデックスの最後で、フィードがチェックされ、有効期限が切れていて、ベンダーが更新して送信する必要があるかどうかを確認します。 また、アカウントがベンダーに過剰に送信されるのを防ぐ方法としても使用されます。 一部のベンダーは、アップロードが頻繁に行われるデータフィードソースに対するポリシーを持っています。 送信の頻度に関するデータフィードベンダーのポリシーを必ず確認してください。 
          <!--The time of the last upload and the status of the upload feed is displayed here. If any other feeds are currently running, their status appears here instead. Each account processes one feed at a time. --> 
          <!--ick <uicontrol>Manual Upload</uicontrol> to generate the feed and push the files to the final destination. Any schedule restrictions that you have already set are ignored. --> </p> <p> 
          <!--If <uicontrol>Manual Upload</uicontrol> is dimmed (inactive), the account is currently processing this feed or another feed. An account only works with one feed at a time. --> </p> </li> 
        <li id="li_760F5068D3ED46C582AE41392A2CA342"> <span class="uicontrol"> アップロード方法 </span> <p>ほとんどのフィードには、ファイルを配布する2つの方法があります。FTPおよびホストコンテンツネットワークを参照してください。 </p> 
          <ul id="ul_666759EDDD034537AA7C0ED936A2F315"> 
          <li id="li_B4AD5CEEBB7B41C0B8DC291B95DC5F83"> <span class="uicontrol">FTP</span> <p>サイト検索/マーチャンダイジングサーバーはパッシブFTPを使用します。 </p> <p>ファイルを別のサーバーにプッシュするには、FTPが唯一の方法です。 </p> <p> <span class="uicontrol"> FTPサーバ </span> ー — FTPサーバーの名前を指定します。 プロトコルや「ftp://」の前には含めないでください。 </p> <p> <span class="uicontrol"> FTPユーザー名 — </span> FTPアカウントの名前を指定します。 </p> <p> <span class="uicontrol"> FTPパスワー </span> ド — FTPアカウントのパスワードを指定します。 </p> <p> <span class="uicontrol"> FTPファイル名 — </span> 送信するファイルの名前を指定します。 この名前は、フィードで複数のファイルが生成される場合に、テンプレートとなります。通常、名前の末尾で拡張子の前に番号が増分されます。 例：basename.xml、basename1.xml、basename2.xml、...、basename-Nth.xml </p> <p> <span class="uicontrol"> FTPディレクトリ — </span> 特定のディレクトリパスが必要な場合は、ここにパスを入力します。 パスにファイル名を含めないでください。 </p> </li> 
          <li id="li_C082D3993C6C469B9067F207703BE619"> <span class="uicontrol"> ホストコンテンツネットワーク </span> <p>コンテンツネットワークは、サイト検索/マーチャンダイジングのWebサーバーからファイルを提供する手段です。 フィードの受信者は、HTTP要求を使用してWebサーバーからフィードを取り込みます。 これを設定する唯一の情報は、コンテンツネットワークフ <span class="uicontrol"> ァイル名で </span>す。 ファイル名は、提供されるファイルのベース名です。 ファイル名の拡張子はファイル名のみ使用してください。 フィードに応じて、ファイル名は複数のファイルのテンプレートで、フィードによって次の形式で複数のファイルが生成される場合があります。basename.xml、basename1.xml、basename2.xml、...、basename-Nth.xml。 </p> <p>ベースファイル名を入力し、フィードが正常に保存されると、コンテンツネットワークファイルのURLがウィザードの検証パネルに表示されます。 フィードが正常に処理されると、URLがアクティブになります。 ベンダーは、このURLからフィードデータを取得できます。 複数のファイルが同じURLパスを使用します。 ただし、列挙スキームに従ってファイル名を置き換えたり、変更したりする必要があります。 </p> </li> 
          </ul> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>5 </p> </td> 
      <td colname="col2"> <p>検証 </p> </td> 
      <td colname="col3"> <p>Verificationパネルに移動する <span class="wintitle"> と、 </span> その時点でフィードが保存されます。 ただし、実際のフィードファイルは後で保存されます。 </p> <p>The <span class="wintitle"> Verification </span> panel lets you do the following: </p> 
        <ul id="ul_0C6EFB38E06F401696084863D85CBD0D"> 
        <li id="li_07FC9F04C7F640048546F9DC5D91DA1D"> <span class="uicontrol"> データビュー </span> <p>リンクをクリックして、テーブルフォームに表示されるデータビューを通してフィードの出力を確認できます。 また、データ表示は、選択したメタフィールドを表示し、ウィザードの検索条件パネルで指定した検索条件がフィードの出力にどのように影響するかを確認することで、トラブルシューティング <span class="wintitle"></span> に役立つことができます。 データビューは動的に生成されるので、常に使用できます。 </p> </li> 
        <li id="li_67046A56D08C48298E5A3E1F9C4A8AF3"> <span class="uicontrol"> フィードファイル </span> <p>サイト検索/マーチャンダイジングサーバーがフィードファイルを生成したら、「フィードファイル」ドロッ <span class="uicontrol"> プダウンリスト </span> を使用して、サーバーのファイルを表示できます。 新しいブラウザータブまたは新しいブラウザーウィンドウが、フィードのコンテンツと共に表示されます。 この方法は、形式の問題があるフィードのトラブルシューティングに役立ちます。 最終的な宛先またはベンダー自体のファイルは表示されません。 </p> <p> フィードが新しい場合は、フィードファイルを生成するまで、ドロップダウンリストは空になります。 </p> </li> 
        <li id="li_99D66C7AD87A475CB3D831D514DB78A0"> <span class="uicontrol"> コンテンツネットワークリンク </span> <p>ウィザードのファイル送信 <span class="uicontrol"> パネルで、アッ </span> プロード方法として「ホストされたコンテ <span class="wintitle"> ンツネ </span> ットワーク」を選択した場合、URLがここに表示されます。 フィードファイルをまだ生成していない場合、URLはフィードが正常に生成されるまで有効ではありません。 </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

   **汎用フィード**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>パネル </p> </th> 
      <th colname="col2" class="entry"> <p>ウィザードパネル名 </p> </th> 
      <th colname="col3" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>Feed Name </p> </td> 
      <td colname="col3"> <p>フィードの名前を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>2 </p> </td> 
      <td colname="col2"> <p>検索条件 </p> </td> 
      <td colname="col3"> <p>フィードファイルが生成されると、検索クエリを使用してデータがフィルターされます。 このパネルで、検索クエリに使用するフィルタを定義します。 </p> 
        <ul id="ul_C750687E69A647D0A4440FF1B6CC7E05"> 
        <li id="li_B5C3B8523D71472E9508A04E23AC0211"> <span class="uicontrol"> メタフィールド </span> <p>フィルタするメタデータフィールドを定義します。 </p> <p> <b>高度な使用方法</b> </p> <p>フィルタリングシステムは標準の検索クエリなので、ドロップダウンリストから「 <span class="uicontrol"> Free Form」 </span> を選択して、CGI検索パラメータとその値を入力できます。 URLエスケープが必要です。 検索引数 <span class="codeph"> sp_qは無視 </span> されます。 フリーフォームのテキストボックスは複数行作成できます。 各行の間の引数は、自動的に&amp;で区切られます。 </p> <p>CGIパラメータ <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> ーの検索を参照してくだ </a>さい。 </p> </li> 
        <li id="li_D1E49834BBEA42CC8C49AE7D72037C53"> <span class="uicontrol"> 条件 </span> <p>フィルター操作を定義します。 ドロップダウンリストから選択したフィルタリング操作により、3列目に入力した定数値が適用されます。 </p> </li> 
        <li id="li_D5F0651B834F4EACAD15A2D154A0737B"> <span class="uicontrol"> 値 </span> <p>定数値。 </p> </li> 
        <li id="li_FC8F382BD20C4518BC2230D4B4954591"> <span class="uicontrol"> アクション </span> <p>新しいフィールドマッピング行を追加するか、現在ハイライトされている行を削除します。 </p> </li> 
        </ul> <p>汎用フィードには、特別なCGIパラメーターを指定する必要があります。 このフィードに関連付けられている特殊なテンプレートを連結するには、 <span class="codeph"> sp_tパラメータを定義 </span> します。 sp_tの値をトランス <span class="codeph"> ポートテン </span> プレートファイルの名前に設定します。 例えば、 <span class="codeph"> super_feed.tplという名前のトランスポートテンプレートファイルを追加した場合、カス </span>タムCGI検索パラメーターを <span class="codeph"> sp_t=super_feedとして作成します </span>。 sp_tを入力するためのテキストボックスは、「 <span class="codeph"> メタフィールド」ドロッ </span> プダウンリスト <span class="uicontrol"> から「フ </span> リーフ <span class="wintitle"> ォーム」を選択するまで表示 </span> されません。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>3 </p> </td> 
      <td colname="col2"> <p>ファイル送信 </p> </td> 
      <td colname="col3"> <p>フィードファイルの送信スケジュールを設定し、ファイルのアップロードに使用する方法を設定できます。 </p> 
        <ul id="ul_30E830C41F6A4526822AF1FD3083075A"> 
        <li id="li_79EAFDBD2B9F411EA985CAEC1BAF3926"> <span class="uicontrol"> スケジュール </span> <p>フィードが送信される最大頻度を設定します。 「なし」を <span class="uicontrol"> 選択する </span> と、フィードがオフになります。 その他の値は、フィードが再び送信されるまで待機する期間を定義します。 フィードを送信するタイミングの決定は、各インデックスで行われます。 つまり、インデックスの最後で、フィードがチェックされ、有効期限が切れていて、ベンダーが更新して送信する必要があるかどうかを確認します。 また、アカウントがベンダーに過剰に送信されるのを防ぐ方法としても使用されます。 一部のベンダーは、アップロードが頻繁に行われるデータフィードソースに対するポリシーを持っています。 送信の頻度に関するフィードベンダーのポリシーを必ず確認してください。 
          <!--he time of the last upload and the status of the upload feed is displayed here. If any other feeds are currently running, their status appears here instead. Each account processes one feed at a time. --> 
          <!--<uicontrol>Manual Upload</uicontrol> to generate the feed and push the files to the final destination. Any schedule restrictions that you have already set are ignored. --> </p> <p> 
          <!--If <uicontrol>Manual Upload</uicontrol> is dimmed (inactive), the account is currently processing this feed or another feed. An account only works with one feed at a time. --> </p> </li> 
        <li id="li_20BF70A19E7E45BA91CD972E2FCE0EA4"> <span class="uicontrol"> アップロード方法 </span> <p>ほとんどのフィードには、ファイルを配布する2つの方法があります。FTPおよびホストコンテンツネットワークを参照してください。 </p> 
          <ul id="ul_5888C2E9097645CE89938EE09F8CB4F1"> 
          <li id="li_EA9ED19F3BEA4BEAB1A9F2C2FAFF85F7"> <span class="uicontrol">FTP</span> <p>サイト検索/マーチャンダイジングサーバーはパッシブFTPを使用します。 </p> <p>ファイルを別のサーバーにプッシュするには、FTPが唯一の方法です。 </p> <p> <span class="uicontrol"> FTPサーバ </span> ー — FTPサーバーの名前を指定します。 プロトコルや「ftp://」の前には含めないでください。 </p> <p> <span class="uicontrol"> FTPユーザー名 — </span> FTPアカウントの名前を指定します。 </p> <p> <span class="uicontrol"> FTPパスワー </span> ド — FTPアカウントのパスワードを指定します。 </p> <p> <span class="uicontrol"> FTPファイル名 — </span> 送信するファイルの名前を指定します。 この名前は、フィードで複数のファイルが生成される場合に、テンプレートとなります。通常、名前の末尾で拡張子の前に番号が増分されます。 例：basename.xml、basename1.xml、basename2.xml、...、basename-Nth.xml </p> <p> <span class="uicontrol"> FTPディレクトリ — </span> 特定のディレクトリパスが必要な場合は、ここにパスを入力します。 パスにファイル名を含めないでください。 </p> </li> 
          <li id="li_181268A7EE40456CA1DB768E8C66EEB9"> <span class="uicontrol"> ホストコンテンツネットワーク </span> <p>ホストコンテンツネットワークは、サイト検索/マーチャンダイジングのWebサーバーからファイルを提供する手段です。 フィードの受信者は、HTTP要求を使用してWebサーバーからフィードを取り込みます。 これを設定する唯一の情報は、コンテンツネットワークフ <span class="uicontrol"> ァイル名で </span>す。 ファイル名は、提供されるファイルのベース名です。 ファイル名の拡張子はファイル名のみ使用してください。 
            <!--Depending on the feed, the file name is a template for multiple files where the feed might generate multiple files in the following format: basename.xml, basename1.xml, basename2.xml, ..., basename-Nth.xml. --> </p> <p>ベースファイル名を入力し、フィードが正常に保存されると、コンテンツネットワークファイルのURLがウィザードの検証パネルに表示されます。 フィードが正常に処理されると、URLがアクティブになります。 ベンダーは、このURLからフィードデータを取得できます。 </p> </li> 
          </ul> </li> 
        <li id="li_4DF56FA607A7479296CDA042A63C5A2C"> <p> <b>タブを保持しますか？</b> </p> <p>フィード内のタブ文字を維持します。 </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>4 </p> </td> 
      <td colname="col2"> <p>検証 </p> </td> 
      <td colname="col3"> <p>Verificationパネルに移動する <span class="wintitle"> と、 </span> その時点でフィードが保存されます。 ただし、実際のフィードファイルは後で保存されます。 </p> <p>The <span class="wintitle"> Verification </span> panel lets you do the following: </p> 
        <ul id="ul_7420C415987448A796DD979CF5FA2EB6"> 
        <li id="li_AF02E8609B7B4F20A01AF4E010308E15"> <span class="uicontrol"> データビュー </span> <p>リンクをクリックして、テーブルフォームに表示されるデータビューを通してフィードの出力を確認できます。 また、データ表示は、選択したメタフィールドを表示し、ウィザードの検索条件パネルで指定した検索条件がフィードの出力にどのように影響するかを確認することで、トラブルシューティング <span class="wintitle"></span> に役立つことができます。 データビューは動的に生成されるので、常に使用できます。 </p> </li> 
        <li id="li_32CEB8885C184354BFA1773BA66DB7A7"> <span class="uicontrol"> フィードファイル </span> <p>サイト検索/マーチャンダイジングサーバーがフィードファイルを生成したら、「フィードファイル」ドロッ <span class="uicontrol"> プダウンリスト </span> を使用して、サーバーのファイルを表示できます。 新しいブラウザータブまたは新しいブラウザーウィンドウが、フィードのコンテンツと共に表示されます。 この方法は、形式の問題があるフィードのトラブルシューティングに役立ちます。 最終的な宛先またはベンダー自体のファイルは表示されません。 </p> <p> フィードが新しい場合は、フィードファイルを生成するまで、ドロップダウンリストは空になります。 </p> </li> 
        <li id="li_8D1B876B0EC2455C8654EC573EC53FA9"> <span class="uicontrol"> コンテンツネットワークリンク </span> <p>ウィザードのファイル送信 <span class="uicontrol"> パネルで、アッ </span> プロード方法として「ホストされたコンテ <span class="wintitle"> ンツネ </span> ットワーク」を選択した場合、URLがここに表示されます。 フィードファイルをまだ生成していない場合、URLはフィードが正常に生成されるまで有効ではありません。 </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

   **Googleマーチャントセンター**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>パネル </p> </th> 
      <th colname="col2" class="entry"> <p>ウィザードパネル名 </p> </th> 
      <th colname="col3" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>Feed Name </p> </td> 
      <td colname="col3"> <p>フィードの名前を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>2 </p> </td> 
      <td colname="col2"> <p>フィールドマップ </p> </td> 
      <td colname="col3"> <p>ベンダー固有のフィードフィールドをサイト検索/マーチャンダイジングメタデータフィールドにマップできます。 このウィザードのマッピング手順は重要です。これは、フィードがインデックス内のフィールドとフィードデータ内のフィールドとの間の情報を関連付けることができるからです。 一般的なフィードを除くほとんどの場 <span class="wintitle"> 合、クロ </span>ス集計は動的に生成された検索テンプレートに保存されます。 </p> <p>[フィールドマップ]テーブルの各行は、フィールドのマッピングを表します。 テーブルの <span class="wintitle"> 「追加/削 </span> 除」列で、「 <span class="uicontrol"> +」をクリックし </span> て、新しいフィールドマッピング行を追加します。現在選択 <span class="uicontrol"> されて </span> いるフィールドマッピング行をテーブルから削除するには、「 — 」をクリックします。 フィードフィールドをサイト検索/マーチャンダイジングメタデータフィールドに関連付けるには、それぞれのドロップダウンリストを使用して、目的のフィールドを選択します。 </p> <p> <b>高度な使用方法</b> </p> <p>独自のカスタムフィールドを作成できます。 「フィードフ <span class="wintitle"> ィールド」ド </span> ロップダウンリストで、「カスタム」をクリ <span class="uicontrol"> ックしま </span>す。 関連するテキストフィールドに、そのフィールドのカスタムタグ名を入力します。 このカスタムオプションは、フィードに特別なベンダー固有のフィールドが必要な場合に役立ちます。 </p> <p>また、カスタムメタデータフィールドを作成することもできます。 「メタデータフ <span class="wintitle"> ィールド」ド </span> ロップダウンリストで、「カスタム」をク <span class="uicontrol"> リックしま </span>す。 関連するテキストフィールドに、カスタムメタデータフィールドの値を入力します。 この値は、事前に生成されたテンプレートに挿入され、カスタム検索テンプレートタグの挿入にも使用できます。 </p> <p>詳しくは、検索テ <a href="../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4" type="reference" format="dita" scope="local"> ンプレートタグを参照してくだ </a>さい。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>3 </p> </td> 
      <td colname="col2"> <p>検索条件 </p> </td> 
      <td colname="col3"> <p>フィードファイルが生成されると、検索クエリを使用してデータがフィルターされます。 このパネルで、検索クエリに使用するフィルタを定義します。 </p> 
        <ul id="ul_8179321A58BB4C72B0CDB2B2BEC58FE4"> 
        <li id="li_9F8008A2398A4667B106BC49C94E5E3E"> <span class="uicontrol"> メタフィールド </span> <p>フィルタするメタデータフィールドを定義します。 </p> <p> <b>高度な使用方法</b> </p> <p>フィルタリングシステムは標準の検索クエリなので、ドロップダウンリストから「 <span class="uicontrol"> Free Form」 </span> を選択して、CGI検索パラメータとその値を入力できます。 URLエスケープが必要です。 検索引数 <span class="codeph"> sp_qは無視 </span> されます。 フリーフォームのテキストボックスは複数行作成できます。 各行の間の引数は、自動的に&amp;で区切られます。 </p> <p>CGIパラメータ <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> ーの検索を参照してくだ </a>さい。 </p> </li> 
        <li id="li_50C9CE59E9E5418895F8C1A070560063"> <span class="uicontrol"> 条件 </span> <p>フィルター操作を定義します。 ドロップダウンリストから選択したフィルタリング操作により、3列目に入力した定数値が適用されます。 </p> </li> 
        <li id="li_9F86D0F5010046A4A9F93DBA5FB158B3"> <span class="uicontrol"> 値 </span> <p>定数値。 </p> </li> 
        <li id="li_1051AFD5AEA447D0AF5FAB305E1D1E64"> <span class="uicontrol"> アクション </span> <p>新しいフィールドマッピング行を追加するか、現在ハイライトされている行を削除します。 </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>4 </p> </td> 
      <td colname="col2"> <p>ファイル送信 </p> </td> 
      <td colname="col3"> <p>フィードファイルの送信スケジュールを設定し、ファイルのアップロードに使用する方法を設定できます。 </p> 
        <ul id="ul_A6A3C333AADD4438B835BF3E16E2AEFF"> 
        <li id="li_FCC4DAF198E149278B5CFB870CB6218C"> <span class="uicontrol"> スケジュール </span> <p>フィードが送信される最大頻度を設定します。 「なし」を <span class="uicontrol"> 選択する </span> と、フィードがオフになります。 その他の値は、フィードが再び送信されるまで待機する期間を定義します。 フィードを送信するタイミングの決定は、各インデックスで行われます。 つまり、インデックスの最後で、フィードがチェックされ、有効期限が切れていて、ベンダーが更新して送信する必要があるかどうかを確認します。 また、アカウントがベンダーに過剰に送信されるのを防ぐ方法としても使用されます。 一部のベンダーは、アップロードが頻繁に行われるデータフィードソースに対するポリシーを持っています。 送信の頻度に関するフィードベンダーのポリシーを必ず確認してください。 </p> <p> 
          <!--The time of the last upload and the status of the upload feed is displayed here. If any other feeds are currently running, their status appears here instead. Each account processes one feed at a time. --> </p> <p> 
          <!--Click <uicontrol>Manual Upload</uicontrol> to generate the feed and push the files to the final destination. Any schedule restrictions that you have already set are ignored. --> </p> <p> 
          <!--If <uicontrol>Manual Upload</uicontrol> is dimmed (inactive), the account is currently processing this feed or another feed. An account only works with one feed at a time. --> </p> </li> 
        <li id="li_2D9ECAFB8E8544D39B486F7BC3DCE589"> <span class="uicontrol"> アップロード方法 </span> <p>ほとんどのフィードには、ファイルを配布する2つの方法があります。FTPおよびホストコンテンツネットワークを参照してください。 </p> <p>データフィードを送信する場合の推奨アップロード方法は <span class="uicontrol"> FTPで </span>す。 Google Merchant Centerは、この目的でFTPサーバーをホストします。 このGoogle製品検索フィード用の別のGoogle FTPアカウントの設定については、Google Merchant Centerのヘルプを参照してください。 </p> 
          <ul id="ul_BC0D8B541068407883CAC948496DBD0A"> 
          <li id="li_DB28CA23C94A4AF09E1A0EB06DF8F40C"> <span class="uicontrol">FTP</span> <p>サイト検索/マーチャンダイジングサーバーはパッシブFTPを使用します。 </p> <p>ファイルを別のサーバーにプッシュするには、FTPが唯一の方法です。 </p> <p> <span class="uicontrol"> FTPサーバ </span> ー — FTPサーバーの名前を指定します。 この場合、 
            <userinput>
              uploads.google.com 
            </userinput> プロトコルや「ftp://」の前には含めないでください。 </p> <p> <span class="uicontrol"> FTPユーザー名 — </span> FTPアカウントの名前を指定します。 </p> <p> <span class="uicontrol"> FTPパスワー </span> ド — FTPアカウントのパスワードを指定します。 </p> <p> <span class="uicontrol"> FTPファイル名 — </span> 送信するファイルの名前を指定します。 この名前は、フィードで複数のファイルが生成される場合に、テンプレートとなります。通常、名前の末尾で拡張子の前に番号が増分されます。 例：basename.xml、basename1.xml、basename2.xml、...、basename-Nth.xml </p> <p> <span class="uicontrol"> FTPディレクトリ — </span> 特定のディレクトリパスが必要な場合は、ここにパスを入力します。 パスにファイル名を含めないでください。 </p> </li> 
          <li id="li_5990927146434DAF89273F4636D21437"> <span class="uicontrol"> ホストコンテンツネットワーク </span> <p>コンテンツネットワークは、サイト検索/マーチャンダイジングのWebサーバーからファイルを提供する手段です。 フィードの受信者は、HTTP要求を使用してWebサーバーからフィードを取り込みます。 </p> <p> 
            <!--After the base filename is entered and the feed is successfully saved, the URL of the Content Network file is displayed on the Verification panel of the wizard. The URL becomes active after the feed is successfully processed. The vendor can get the feed data from this URL. Multiple files use the same URL path. However, be sure that you replace or change the filename according to the enumeration scheme. --> </p> </li> 
          </ul> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>5 </p> </td> 
      <td colname="col2"> <p>検証 </p> </td> 
      <td colname="col3"> <p>Verificationパネルに移動する <span class="wintitle"> と、 </span> その時点でフィードが保存されます。 ただし、実際のフィードファイルは後で保存されます。 </p> <p>The <span class="wintitle"> Verification </span> panel lets you do the following: </p> 
        <ul id="ul_4A94355A8DF840A3BAF6BD5E9F11C27F"> 
        <li id="li_825697CB36B34C4AB5959B15EDDB55F1"> <span class="uicontrol"> データビュー </span> <p>リンクをクリックして、テーブルフォームに表示されるデータビューを通してフィードの出力を確認できます。 また、データ表示は、選択したメタフィールドを表示し、ウィザードの検索条件パネルで指定した検索条件がフィードの出力にどのように影響するかを確認することで、トラブルシューティング <span class="wintitle"></span> に役立つことができます。 データビューは動的に生成されるので、常に使用できます。 </p> </li> 
        <li id="li_91B8B5F5F9DE4A13863CD62F74AA6206"> <span class="uicontrol"> フィードファイル </span> <p>サイト検索/マーチャンダイジングサーバーがフィードファイルを生成したら、「フィードファイル」ドロッ <span class="uicontrol"> プダウンリスト </span> を使用して、サーバーのファイルを表示できます。 新しいブラウザータブまたは新しいブラウザーウィンドウが、フィードのコンテンツと共に表示されます。 この方法は、形式の問題があるフィードのトラブルシューティングに役立ちます。 最終的な宛先またはベンダー自体のファイルは表示されません。 </p> <p> フィードが新しい場合は、フィードファイルを生成するまで、ドロップダウンリストは空になります。 </p> </li> 
        <li id="li_4A5EC089628E43029A38F8919888FF0A"> <span class="uicontrol"> コンテンツネットワークリンク </span> <p>ウィザードのファイル送信 <span class="uicontrol"> パネルで、アッ </span> プロード方法として「ホストされたコンテ <span class="wintitle"> ンツネ </span> ットワーク」を選択した場合、URLがここに表示されます。 フィードファイルをまだ生成していない場合、URLはフィードが正常に生成されるまで有効ではありません。 </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

   **Googleサイトマップ**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>パネル </p> </th> 
      <th colname="col2" class="entry"> <p>ウィザードパネル名 </p> </th> 
      <th colname="col3" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>Feed Name </p> </td> 
      <td colname="col3"> <p>フィードの名前を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>2 </p> </td> 
      <td colname="col2"> <p>フィールドマップ </p> </td> 
      <td colname="col3"> <p>ベンダー固有のフィードフィールドをサイト検索/マーチャンダイジングメタデータフィールドにマップできます。 このウィザードのマッピング手順は重要です。これは、フィードがインデックス内のフィールドとフィードデータ内のフィールドとの間の情報を関連付けることができるからです。 一般的なフィードを除くほとんどの場 <span class="wintitle"> 合、クロ </span>ス集計は動的に生成された検索テンプレートに保存されます。 </p> <p>[フィールドマップ]テーブルの各行は、フィールドのマッピングを表します。 表の「追加と削除」列で、「 <span class="uicontrol"> +」をクリックし </span> て、新しいフィールドマッピング行を追加します。現在選択 <span class="uicontrol"> されて </span> いるフィールドマッピング行をテーブルから削除するには、「 — 」をクリックします。 フィードフィールドをメタデータフィールドに関連付けるには、それぞれのドロップダウンリストを使用して、目的のフィールドを選択します。 </p> <p> <b>高度な使用方法</b> </p> <p>独自のカスタムフィールドを作成できます。 「フィードフ <span class="wintitle"> ィールド」ド </span> ロップダウンリストで、「カスタム」をクリ <span class="uicontrol"> ックしま </span>す。 関連するテキストフィールドに、そのフィールドのカスタムタグ名を入力します。 このカスタムオプションは、フィードに特別なベンダー固有のフィールドが必要な場合に役立ちます。 </p> <p>また、カスタムメタデータフィールドを作成することもできます。 「メタデータフ <span class="wintitle"> ィールド」ド </span> ロップダウンリストで、「カスタム」をク <span class="uicontrol"> リックしま </span>す。 関連するテキストフィールドに、カスタムメタデータフィールドの値を入力します。 この値は、事前に生成されたテンプレートに挿入され、カスタム検索テンプレートタグの挿入にも使用できます。 </p> <p>詳しくは、検索テ <a href="../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4" type="reference" format="dita" scope="local"> ンプレートタグを参照してくだ </a>さい。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>3 </p> </td> 
      <td colname="col2"> <p>検索条件 </p> </td> 
      <td colname="col3"> <p>フィードファイルが生成されると、検索クエリを使用してデータがフィルターされます。 このパネルで、検索クエリに使用するフィルタを定義します。 </p> 
        <ul id="ul_994585E89A044BD3A89A99D30F277432"> 
        <li id="li_61FA9246B9824E3C8124958C8EBFF0DA"> <span class="uicontrol"> メタフィールド </span> <p>フィルタするメタデータフィールドを定義します。 </p> <p> <b>高度な使用方法</b> </p> <p>フィルタリングシステムは標準の検索クエリなので、ドロップダウンリストから「 <span class="uicontrol"> Free Form」 </span> を選択して、CGI検索パラメータとその値を入力できます。 URLエスケープが必要です。 検索引数 <span class="codeph"> sp_qは無視 </span> されます。 フリーフォームのテキストボックスは複数行作成できます。 各行の間の引数は、自動的に&amp;で区切られます。 </p> <p>CGIパラメータ <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> ーの検索を参照してくだ </a>さい。 </p> </li> 
        <li id="li_A5D00883738845C8B8F612A7521F160F"> <span class="uicontrol"> 条件 </span> <p>フィルター操作を定義します。 ドロップダウンリストから選択したフィルタリング操作により、3列目に入力した定数値が適用されます。 </p> </li> 
        <li id="li_5A312C2984454C2CB518CA453AD9F6D2"> <span class="uicontrol"> 値 </span> <p>定数値。 </p> </li> 
        <li id="li_666AAE1BC7A2432E91953B08EC7394DC"> <span class="uicontrol"> アクション </span> <p>新しいフィールドマッピング行を追加するか、現在ハイライトされている行を削除します。 </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>4 </p> </td> 
      <td colname="col2"> <p>ファイル送信 </p> </td> 
      <td colname="col3"> <p>フィードファイルの送信スケジュールを設定し、ファイルのアップロードに使用する方法を設定できます。 </p> 
        <ul id="ul_49B3255BE669424B925BBAEE4C9B385F"> 
        <li id="li_939828C774D440EBB0769F6D5B0BBA23"> <span class="uicontrol"> スケジュール </span> <p>フィードが送信される最大頻度を設定します。 「なし」を <span class="uicontrol"> 選択する </span> と、フィードがオフになります。 その他の値は、フィードが再び送信されるまで待機する期間を定義します。 フィードを送信するタイミングの決定は、各インデックスで行われます。 つまり、インデックスの最後で、フィードがチェックされ、有効期限が切れていて、ベンダーが更新して送信する必要があるかどうかを確認します。 また、アカウントがベンダーに過剰に送信されるのを防ぐ方法としても使用されます。 一部のベンダーは、アップロードが頻繁に行われるデータフィードソースに対するポリシーを持っています。 送信の頻度に関するフィードベンダーのポリシーを必ず確認してください。 </p> <p> 
          <!--The time of the last upload and the status of the upload feed is displayed here. If any other feeds are currently running, their status appears here instead. Each account processes one feed at a time. --> </p> <p> 
          <!--Click <uicontrol>Manual Upload</uicontrol> to generate the feed and push the files to the final destination. Any schedule restrictions that you have already set are ignored. --> </p> <p> 
          <!--If <uicontrol>Manual Upload</uicontrol> is dimmed (inactive), the account is currently processing this feed or another feed. An account only works with one feed at a time. --> </p> </li> 
        <li id="li_07B5BCF7936241A7915C4898B231184B"> <span class="uicontrol"> アップロード方法 </span> <p>ほとんどのフィードには、ファイルを配布する2つの方法があります。FTPおよびホストコンテンツネットワークを参照してください。 </p> 
          <ul id="ul_74FA98A82754469BA5FADCC63FC364F7"> 
          <li id="li_02940B712D6444A8B65C0A51834187E6"> <span class="uicontrol">FTP</span> <p>サイト検索/マーチャンダイジングサーバーはパッシブFTPを使用します。 </p> <p>ファイルを別のサーバーにプッシュするには、FTPが唯一の方法です。 </p> <p> <span class="uicontrol"> FTPサーバ </span> ー — FTPサーバーの名前を指定します。 プロトコルや「ftp://」の前には含めないでください。 </p> <p> <span class="uicontrol"> FTPユーザー名 — </span> FTPアカウントの名前を指定します。 </p> <p> <span class="uicontrol"> FTPパスワー </span> ド — FTPアカウントのパスワードを指定します。 </p> <p> <span class="uicontrol"> FTPファイル名 — </span> 送信するファイルの名前を指定します。 この名前は、フィードで複数のファイルが生成される場合に、テンプレートとなります。通常、名前の末尾で拡張子の前に番号が増分されます。 例：basename.xml、basename1.xml、basename2.xml、...、basename-Nth.xml </p> <p> <span class="uicontrol"> FTPディレクトリ — </span> 特定のディレクトリパスが必要な場合は、ここにパスを入力します。 パスにファイル名を含めないでください。 </p> </li> 
          <li id="li_EAE504436CD84452BA04BE51855A2BEF"> <span class="uicontrol"> ホストコンテンツネットワーク </span> <p>コンテンツネットワークは、サイト検索/マーチャンダイジングのWebサーバーからファイルを提供する方法です。 フィードの受信者は、HTTP要求を使用してWebサーバーからフィードを取り込みます。 </p> <p> 
            <!--After the base filename is entered and the feed is successfully saved, the URL of the Content Network file is displayed on the Verification panel of the wizard. The URL becomes active after the feed is successfully processed. The vendor can get the feed data from this URL. Multiple files use the same URL path. However, be sure that you replace or change the filename according to the enumeration scheme. --> </p> </li> 
          </ul> </li> 
        </ul> <p>どちらのアップロード方法でも、Googleがサイトマップを取得する際に使用するURLを「メインサイトマップURL」フィールドに指定する <span class="wintitle"> 必要があることに注意し </span> てください。 サイトマップファイルの名前もここで決まります。 サイトマップが大きい場合は、複数のファイルが存在する可能性があり、命名規則では、ファイルの末尾にインデックス番号を付け、番号1から始まる番号を付けます。 最初のファイルまたはインデックスファイルには、 <span class="codeph"> sitemap.xml、 </span>sitemap1.xml、sitemap2.xmlのように、インデックス <span class="codeph"> が </span>ありま <span class="codeph"></span> せん。 <span class="codeph"> sitemap12.xmlを参照してくださ </span>い。 </p> <p>アップロード方法とし <span class="uicontrol"> て「ホストさ </span> れたコンテンツネットワーク」を選択した場合、ファイルのURLのファイル名は同じですが、URLにはホストサービスのパスとホスト名が含まれます。 したがって、サイトマップの要求をホストコンテンツネットワークにリダイレクトします。 同じ場所からファイルを取り込むこともできます。 </p> <p>フィードファイルが作成され、中間の宛先に送信された後、Googleはpingされ、サイトマップフィードの準備ができたことを通知します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>5 </p> </td> 
      <td colname="col2"> <p>検証 </p> </td> 
      <td colname="col3"> <p>Verificationパネルに移動する <span class="wintitle"> と、 </span> その時点でフィードが保存されます。 ただし、実際のフィードファイルは後で保存されます。 </p> <p>The <span class="wintitle"> Verification </span> panel lets you do the following: </p> 
        <ul id="ul_A1D889A84972419599FC83F39EA2676A"> 
        <li id="li_C8ED077B6DD1461E85A4914C1CFDBE88"> <span class="uicontrol"> データビュー </span> <p>リンクをクリックして、テーブルフォームに表示されるデータビューを通してフィードの出力を確認できます。 また、データ表示は、選択したメタフィールドを表示し、ウィザードの検索条件パネルで指定した検索条件がフィードの出力にどのように影響するかを確認することで、トラブルシューティング <span class="wintitle"></span> に役立つことができます。 データビューは動的に生成されるので、常に使用できます。 </p> </li> 
        <li id="li_DACEE40703AF40EFBCD90D43825CE9C1"> <span class="uicontrol"> フィードファイル </span> <p>フィードファイルが生成されたら、「フィードファイル」ドロッ <span class="uicontrol"> プダウンリスト </span> を使用して、サーバー上のファイルを表示できます。 新しいブラウザータブまたは新しいブラウザーウィンドウが、フィードのコンテンツと共に表示されます。 この方法は、形式の問題があるフィードのトラブルシューティングに役立ちます。 最終的な宛先またはベンダー自体のファイルは表示されません。 </p> <p> フィードが新しい場合は、フィードファイルを生成するまで、ドロップダウンリストは空になります。 </p> </li> 
        <li id="li_1C530354B4F34EC79D92CEFEB5B39ED7"> <span class="uicontrol"> コンテンツネットワークリンク </span> <p>ウィザードのファイル送信 <span class="uicontrol"> パネルで、アッ </span> プロード方法として「ホストされたコンテ <span class="wintitle"> ンツネ </span> ットワーク」を選択した場合、URLがここに表示されます。 フィードファイルをまだ生成していない場合、URLはフィードが正常に生成されるまで有効ではありません。 </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

1. ウィザードの手順を完了したら、をクリックしま **[!UICONTROL Close]**&#x200B;す。

## フィードの編集 {#task_B855D28CD99B4FA58E2D4D4FD6DC9CEB}

既存のフィードの設定を編集できます。

<!-- 

t_editing_a_feed.xml

 -->

>[!NOTE]
>
>フィードを編集する場合、フィードのタイプを変更することはできません。 フィードのタイプを変更する必要がある場合は、既存のフィードを削除し、目的のタイプの新しいフィードを追加します。

詳しくは、 [フィードの削除を参照してくださ](../c-about-settings-menu/c-about-searching-menu.md#task_7E39A140E69D43C6B61FB42E81051269)い。

**フィードを編集するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Searching]** ます **[!UICONTROL Feeds]**。
1. 次のいずれかを実行します。

* ページ [!DNL Feeds] の表の列の下 [!DNL Name] で、フィード名の横のドロップダウンリストをクリックし、をクリックします **[!UICONTROL Edit feed]**。

* ページ [!DNL Feeds] の列の下で、 [!DNL Name] 変更するフィードの名前をクリックします。

1. フィードのウィザードで、ウィザードの各パネルに必要なオプションを設定します。

   フィードの追加のオプションの表を **参照してください**。
1. ウィザードの最後のパネルで、をク [!DNL Verification] リックします **[!UICONTROL Close]**。

## フィードの削除 {#task_7E39A140E69D43C6B61FB42E81051269}

不要になったフィードや使用しなくなったフィードは削除できます。

<!-- 

t_deleting_a_feed.xml

 -->

**フィードを削除するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Searching]** ます **[!UICONTROL Feeds]**。
1. 画面の [!DNL Feeds Menu] 列の下で、 [!DNL Actions] 削除するフ **[!UICONTROL Delete]** ィード名をクリックします。
1. ダイアログボ [!DNL Delete feed] ックスで、をクリック **[!UICONTROL Yes]** して削除を確定します。

## フィードファイルの表示 {#task_1E413C7650DE466EA68925F72E086884}

フィードウィザードの最後のパネルに移動して、フィードのデータ表示をすばやく確認したり、サーバーから現在のフィードファイルをダウンロードしたりできます。 この機能は、フィードの出力を確認および確認する場合に役立ちます。

<!-- 

t_viewing_feed_files.xml

 -->

**フィードファイルを表示するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Searching]** ます **[!UICONTROL Feeds]**。
1. ページ [!DNL Feeds] の表の列の下 [!DNL Name] で、フィード名の横のドロップダウンリストをクリックし、をクリックします **[!UICONTROL View Feed Files]**。
1. フィードの [!DNL Verification] ウィザードのパネルで、をクリックしま **[!UICONTROL Show Data View]**&#x200B;す。
1. クリック **[!UICONTROL Close]**.

## ファイルのアップロードなしでのフィードのテスト {#task_F1F390F72E0A4886B6CD4CD86EDB4C8C}

最終的なアップロード先にファイルをアップロードせずに、フィードをテストできます。

<!-- 

t_testing_a_feed_with_no_file_upload.xml

 -->

**ファイルのアップロードなしでフィードをテストするには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Searching]** ます **[!UICONTROL Feeds]**。
1. ページ [!DNL Feeds] の表の列の下 [!DNL Name] で、フィード名の横のドロップダウンリストをクリックし、をクリックします **[!UICONTROL Test Feed (No file upload)]**。
1. ページ上 [!DNL Feeds] の列は、テ [!DNL Feed Status] スト中およびテスト後に更新されます。

## フィードの生成とアップロード {#task_C9A57827C7674035B62A22D310DDAA0C}

フィードウィザードのパネルで設定したスケジュールに関係なく、フィードファイルを手動で生成し、最終的な宛先に送 [!DNL File Submission] 信することができます。

<!-- 

t_generating_and_uploading_a_feed.xml

 -->

フィードの作 [成も参照してください](../c-about-settings-menu/c-about-searching-menu.md#task_63179C1FC359497483CD6CE13FD1C250)。

**フィードを生成してアップロードするには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Searching]** ます **[!UICONTROL Feeds]**。
1. ページ [!DNL Feeds] の表の列の下 [!DNL Name] で、フィード名の横のドロップダウンリストをクリックし、をクリックします **[!UICONTROL Generate and Upload Feed]**。
1. ページ上の [!DNL Feeds] 列は、データフ [!DNL Feed Status] ィードの生成およびアップロードの間および後に更新されます。
