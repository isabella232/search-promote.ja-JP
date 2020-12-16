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
source-git-commit: 552f93f1f630c64bbe3d5c8a87c4f5895ae6868c
workflow-type: tm+mt
source-wordcount: '11182'
ht-degree: 1%

---


# 検索メニューについて{#about-the-searching-menu}

検索メニューを使用して、除外する単語、コレクション、制限、プレビューおよびフレームを設定します。

## 検索について{#concept_207105CF26B1448F8A3D223787C56AB8}

[検索]を使用すると、プレゼンテーションテンプレートで参照できる名前付き検索を定義およびカスタマイズできます。

<!-- 

c_about_searches.xml

 -->

プレゼンテーションテンプレートでは、検索モジュール内で定義された任意の名前付き検索を参照できます。 また、これにより、特定のテンプレートセットに対して行われる検索のタイプを簡単にカスタマイズできます。

頻繁に使用するフレーズや共通語を検索結果から除外する方法については、[除外する単語の設定](../c-about-linguistics-menu/c-about-excluded-words.md#task_60BF6BB7A66C48479D2BBB32C0F38CDE)を参照してください。

Webサイトの特定で検索可能な領域を定義する方法については、[コレクションの追加](../c-about-settings-menu/c-about-searching-menu.md#task_07732D0F00104E59AD421297A704B2F6)を参照してください。

検索結果リンクのターゲットフレームを指定する方法については、[フォーム](../c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5)を含むフレームの使用を参照してください。

HTTP転送者、IPアドレス、またはリクエストスキーム（HTTPまたはHTTPS）に基づいて検索を制限する方法については、[プレビュー](../c-about-settings-menu/c-about-searching-menu.md#task_CE267A0FF621474E80AB43B67B1C28D7)の値の設定を参照してください。

## 検索のヒント{#section_22F0E2BCF259459FA5F49FBCC0F09A7C}

より具体的な検索結果を得るには、次の検索のヒントを使用できます。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>検索ヒント </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>スペルチェック </p> </td> 
   <td colname="col2"> <p>検索用語のスペルが正しいことを確認します。 <span class="uicontrol">言語<span class="uicontrol"> &gt; <span class="uicontrol">単語と言語</span>で&lt;a0/&gt;サウンドアリクマッチ</span>が有効な場合、検索エンジンは検索用語に似た単語を探そうとします。 </span>ただし、検索用語のスペルを正しく入力することをお勧めします。 </p> <p><a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local">単語と言語について</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>複数の単語を使用 </p> </td> 
   <td colname="col2"> <p>例: 
     <code>
       our free product 
     </code> </p> <p>複数語のクエリは、単一語のクエリよりも絞り込みの効果を返します。 </p> <p>例えば、 
     <code>
       our free product 
     </code>は単に&lt;a0/&gt;を返す以上の結果を返します 
     <code>
       product 
     </code>. </p> <p>すべてのクエリ用語が含まれていない場合でも、関連する結果が返されることに注意してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>類似の単語を使用 </p> </td> 
   <td colname="col2"> <p>例: 
     <code>
       safe secure privacy security 
     </code> </p> <p>検索クエリで使用できる語がより類似しているほど、関連性の高い検索結果が表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>大文字と小文字の適切な使用 </p> </td> 
   <td colname="col2"> <p>例: 
     <code>
       Search Template Reference 
     </code> </p> <p>固有名詞を大文字にします。 小文字の単語を使用すると、検索エンジンは単語の大文字と小文字を区別して一致します。 </p> <p>例えば、 
     <code>
       search 
     </code>の場合、検索エンジンは「search」、「Search」、「SEARCH」を含むすべてのドキュメントを返します。 ただし、 
     <code>
       Search 
     </code>の場合、検索エンジンは大文字で始まる単語のみを含むドキュメントを返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>引用符の使用 </p> </td> 
   <td colname="col2"> <p>例: 
     <code>
       "our pledge to you" 
     </code> </p> <p>「お客様への誓約」など、お互いに隣接して表示する必要のある単語を検索するには、引用符を使用します。 前後の引用符がない場合、検索結果には「our」、「plesge」、「to」、「you」という語が含まれますが、必ずしもその順序ではありません。 代わりに、ドキュメント内の任意の場所、任意の順序で単語が表示されます。 </p> <p> <span class="uicontrol">任意の</span>、<span class="uicontrol">すべての</span>、<span class="uicontrol">フレーズ</span>のラジオボタンと共にアドバンス検索フォームを使用する場合、引用符の使用は<span class="uicontrol">任意の</span>が選択されているときにのみ可能です。 <span class="uicontrol">すべての</span>または<span class="uicontrol">フレーズ</span>が選択されている場合、引用符は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>+（プラス）または — （マイナス）を使用します。 </p> </td> 
   <td colname="col2"> <p>例: 
     <code>
       +"template language" 
     </code> </p> <p>「+」を使用して、検索用語または語句を検索結果に表示する必要があることを示します。 </p> <p> — は、検索用語または語句を検索結果に含めない必要があることを示します。 </p> <p>フレーズは引用符で囲む必要があります。 上記の例のように、プラス記号またはマイナス記号と検索語句の間にスペースを入れないでください。 </p> <p> <span class="uicontrol">任意の</span>、<span class="uicontrol">すべての</span>、<span class="uicontrol">フレーズ</span>のラジオボタンと共にアドバンス検索フォームを使用する場合、引用符の使用は<span class="uicontrol">任意の</span>が選択されているときにのみ可能です。 すべての</span>または<span class="uicontrol">フレーズ</span>が選択されている場合、プラス修飾子とマイナス修飾子は無視されます。<span class="uicontrol"> </span></p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>フィールド検索の使用 </p> </td> 
   <td colname="col2"> <p>例： </p> <p> 
     <ul id="ul_F7CFF7652894402E8D19D6BA49792530"> 
      <li id="li_27492EF933C5437CB2C499746EC8CF39"> 
       <code>
         title:about 
       </code> </li> 
      <li id="li_BD21505122104FD0B16A4DAD777811DA"> 
       <code>
         desc:"Our Team" 
       </code> </li> 
      <li id="li_8264630F8B3D46BF872EFEB1D69DB6BE"> 
       <code>
         keys:login 
       </code> </li> 
      <li id="li_EBB81CBFC6DA45E99A524890DCD56E9F"> 
       <code>
         body:security 
       </code> </li> 
      <li id="li_6A852E35D6984A2C94144AB6C6D2DFA0"> 
       <code>
         alt:"join now" 
       </code> </li> 
      <li id="li_F4C5699360484D12ACD62BBFB84A7904"> 
       <code>
         url:help 
       </code> </li> 
      <li id="li_B2DBBA2239E74D98868D92B3EDEF5B51"> 
       <code>
         target:Adobe 
       </code> </li> 
     </ul> </p> <p>フィールド検索を使用すると、ドキュメントの特定の部分に表示される単語に対する特定の検索を作成できます。 </p> <p>本文テキスト（本文：）、タイトルテキスト（表題：）、代替テキスト（代替：）、メタ説明（説明：）、メタキーワード（キー：）、URL(URL:)またはメタターゲットキーワード(ターゲット:)に対して、フィールド検索を実行できます。 フィールド名には小文字を使用し、その直後にコロンを付けます。 コロンと検索語句の間にスペースは入れません。 </p> <p>フィールドの検索の後に続くのは、単語またはフレーズのみです。 フレーズは引用符で囲む必要があります。 </p> <p>フィールド名にリストボックスを付けてアドバンス検索フォームを使用している場合は、<span class="uicontrol">任意の</span>を選択したときに、単語またはフレーズの前にのみフィールド名を入力できます。 「リスト」ボックスで他のアドバンス検索フォームフィールドが選択されている場合、特定のフィールド名は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ワイルドカードの使用 </p> </td> 
   <td colname="col2"> <p>例： </p> <p> 
     <ul id="ul_D8E3867EB15641B0A6E55AD546CCB4DD"> 
      <li id="li_CB8B8FC15EB14B13BB33BB69F5206303"> 
       <code>
         wh* 
       </code> </li> 
      <li id="li_5350A934648C4C81BD6C0875061B426B"> 
       <code>
         "wh* are" 
       </code> </li> 
      <li id="li_7965A2F7186F40039D2F0736299D11B1"> 
       <code>
         415-*-* 
       </code> </li> 
     </ul> </p> <p>ワイルドカード検索は、特定のリクエストに対する一致の数を拡張します。 ワイルドカード文字には*文字を使用します。 </p> <p>例えば、 
     <code>
       wh* 
     </code>は、「what」、「whey」、「when」、「whef」、および「wh」を開始する他の単語を検索します。 *her*を検索すると、「here」、「wheth」、「togher」、「gathering」、および単語内の任意の場所に「her」を含む他の単語が検索されます。 </p> <p>ワイルドカードを+および — 修飾子、フレーズの引用符、フィールド検索指定子と組み合わせることができます。 </p> <p>検索 
     <code>
       +wh* -se*ch 
     </code>は、「wh」を含む単語を含み、「se」を含み「ch」で終わる開始を含まないすべてのページを検索します。 </p> <p>検索 
     <code>
       "wh* are" 
     </code>は、「where are」、「what are」、「whey are」などのフレーズを検索します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 新しい検索定義{#task_98D3A168AB5D4F30A1ADB6E0D48AB648}を追加する

[!DNL GS Add Search]パネルを使用して、プレゼンテーションレイヤーで、ファセット、パンくずリスト、ページナビゲーション、メニュー、最近の検索など、ガイド付き検索コンポーネントの新しい検索定義を設定および追加できます。

<!-- 

t_adding_a_new_definition.xml

 -->

新しい検索定義を追加した後は、プレゼンテーションテンプレートでその定義を参照して表示されるようにしてください。

[テンプレートについて](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5)を参照してください。

**新しい検索定義を追加するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Searching]**/**[!UICONTROL Searches]**&#x200B;をクリックします。
1. [!DNL Searches]ページで、**[!UICONTROL Add New Search]**&#x200B;をクリックします。
1. **[!UICONTROL GS Add Search]**&#x200B;ページで、必要なオプションを設定します。

   <!-- 
   
   r_gs_search_options.xml
   
   -->

   プレゼンテーションテンプレートを選択する処理ルールは、これらのオプションの一部を上書きできる場合があることに注意してください。

   「[新しい検索定義の追加](../c-about-settings-menu/c-about-searching-menu.md#task_98D3A168AB5D4F30A1ADB6E0D48AB648)」または「[検索定義の編集](../c-about-settings-menu/c-about-searching-menu.md#task_AF1FFB1AEF874C13AB359C28F74BF461)」を参照してください。

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
      <td colname="col2"> <p>使用するバックエンド検索を選択できます。 <span class="wintitle"> SiteSearch </span>または<span class="wintitle">マーチャンダイジング</span>から選択できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>アカウント </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして<span class="uicontrol">Search&amp;Promote</span>を選択した場合にのみ使用できます。 </p> <p>検索するサイト検索/マーチャンダイジングのアカウントを選択できます。 通常、検索は、現在使用しているアカウント内を検索します。 ただし、プレゼンテーションテンプレートでは、他の任意のアカウントに対してバックエンド検索を使用できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>サーバー名/IP </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして<span class="uicontrol">マーチャンダイジング</span>を選択した場合にのみ使用できます。 </p> <p><span class="wintitle">マーチャンダイジング</span>検索がアクセスする<span class="wintitle">マーチャンダイジング</span>サーバーの完全な名前を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>サーバーポート </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして<span class="uicontrol">マーチャンダイジング</span>を選択した場合にのみ使用できます。 </p> <p><span class="wintitle">マーチャンダイジング</span>サーバーのポート番号を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ピラミッド </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして<span class="uicontrol">マーチャンダイジング</span>を選択した場合にのみ使用できます。 </p> <p><span class="wintitle">マーチャンダイジング</span>サーバー内のピラミッドを指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>結果数 </p> </td> 
      <td colname="col2"> <p>返す検索結果の数を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最初のページの結果数（異なる場合） </p> </td> 
      <td colname="col2"> <p>最初のページで返す結果の数を指定します。 他のページとは異なるページにする必要がある場合に、このオプションを使用します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>列数 </p> </td> 
      <td colname="col2"> <p>検索結果を分割する列数を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>検索の種類 </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして<span class="uicontrol">Search&amp;Promote</span>を選択した場合にのみ使用できます。 </p> <p>次の3種類の検索から選択できます。 </p> <p> 
        <ul id="ul_2F6FA9EFD8DB49EEAB866C3D070E2644"> 
          <li id="li_ECFEBEDD86FF4DE2BB768423B3B91B5E"> <span class="uicontrol"> all </span> <p>クエリ文字列内のすべての単語を含むドキュメントを検索します。 </p> <p>検索語を無効にする前に「+」と「 — 」を使用し、これらの文字は無視されます。 </p> </li> 
          <li id="li_62EB215BDDE74DF0BF76B3BD5B96776F"> <span class="uicontrol"> 任意 </span> <p>「+」と「 — 」の語頭文字を使用できます。 </p> </li> 
          <li id="li_3D71982C0BBA41AFA353069AF3F2F6D8"> <span class="uicontrol"> フレーズ  </span> <p>クエリ文字列は引用符で囲まれたフレーズとして扱われ、ユーザーが入力した引用符はすべて無視されます。 </p> <p>検索語を無効にする前に「+」と「 — 」を使用し、これらの文字は無視されます。 </p> </li> 
        </ul> </p> <p> クエリ内の各単語にファセット値を選択する可能性を持たせる場合、プライマリ検索では常に<span class="uicontrol">すべて</span>を使用する必要があります。 </p> <p>検索クエリでの+および — 修飾子の使用に関する検索のヒントを確認できます。 </p> <p><a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">検索について</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>コレクション </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして<span class="uicontrol">Search&amp;Promote</span>を選択した場合にのみ使用できます。 </p> <p>インデックス内で検索するコレクションを識別します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Promosearch </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして<span class="uicontrol">Search&amp;Promote</span>を選択した場合にのみ使用できます。 </p> <p>指定した<span class="uicontrol">検索結果数</span>に従って、検索結果からランダムに選択して使用できます。 </p> <p>プロモサーチは、従来の概念です。 そのため、サイト検索/マーチャンダイジング内で新しいバナー管理システムを使用することをお勧めします。 </p> <p><a href="../c-about-design-menu/c-about-banners.md#concept_5BBE01FEC6134393B43CC917C8CC64DA" type="concept" format="dita" scope="local">バナーについて</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファセットパラメータの適用 </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして<span class="uicontrol">Search&amp;Promote</span>を選択し、<span class="uicontrol">プロモサーチ</span>を選択した場合にのみ使用できます。 </p> <p>プロモーション検索で、選択したファセットを使用してプロモーションを絞り込むことを指定します。 ほとんどのプロモ検索アカウントでは、このオプションは使用されません。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>一致するプロモーションがない場合にデフォルトのプロモーションを指定する </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして<span class="uicontrol">Search&amp;Promote</span>を選択し、<span class="uicontrol">プロモサーチ</span>を選択した場合にのみ使用できます。 </p> <p>プロモーションの最初の検索で何も見つからない場合に、プロモーションの別の検索を行うことを指定します。 2つ目のプロモーションの検索では、キーワードが削除されます。 代わりに、「is_default」メタデータフィールドが「yes」に設定されているすべてのプロモーションを探します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>検索のハイライト </p> </td> 
      <td colname="col2"> <p>「ヒーローゾーン」で強調したい、メイン検索から選択した数の結果を取り出します。 </p> <p>通常、ハイライト検索には、メイン検索と同様の検索条件がありますが、異なるランク付けメカニズムを使用して特定の結果をハイライトします。 重複はメイン検索から削除されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ベース検索 </p> </td> 
      <td colname="col2"> <p>このオプションは、「<span class="uicontrol">検索をハイライト</span>」を選択した場合にのみ使用できます。 </p> <p>結果をハイライト表示する検索結果を含む検索を選択できます。 重複はこの検索から削除されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>重複除外の優先度 </p> </td> 
      <td colname="col2"> <p>このオプションは、「<span class="uicontrol">検索をハイライト</span>」を選択した場合にのみ使用できます。 </p> <p>複数のハイライト検索を行うことができます。 </p> <p>複数のハイライト検索を使用する場合は、重複除外の優先度を指定する必要があります。ここで、「1」が最も高い優先度です。 </p> <p>例えば、2つの検索ハイライトがあるとします。ベストセラーと新製品 理論的には ベストセラーも新製品の可能性がある。 この場合、新しい商品とメイン検索から重複を削除します。 したがって、ベストセラーの優先度を1に、新製品の優先度を2に設定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>パラメーター </p> </td> 
      <td colname="col2"> <p>検索にCGIパラメーターを追加できます。 </p> <p><a scope="local" href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita">バックエンド検索CGIパラメーター</a>を参照してください。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Add]**.
1. （オプション）[!DNL Searches]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 検索定義の編集{#task_AF1FFB1AEF874C13AB359C28F74BF461}

[!DNL Staged GS Edit Search]パネルを使用して、ガイド付き検索プレゼンテーションレイヤーの既存の検索定義を再設定できます。

<!-- 

t_editing_a_search_definition.xml

 -->

検索定義を編集した後、表示されるように、プレゼンテーションテンプレートでその定義を参照していることを確認します。

[テンプレートについて](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5)を参照してください。

**検索定義を編集するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Searching]**/**[!UICONTROL Searches]**&#x200B;をクリックします。
1. [!DNL Searches]ページのテーブルで、変更する定義の行の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。
1. **[!UICONTROL GS Edit Search]**&#x200B;ページで、必要なオプションを設定します。

   <!-- 
   
   r_gs_search_options.xml
   
   -->

   プレゼンテーションテンプレートを選択する処理ルールは、これらのオプションの一部を上書きできる場合があることに注意してください。

   「[新しい検索定義の追加](../c-about-settings-menu/c-about-searching-menu.md#task_98D3A168AB5D4F30A1ADB6E0D48AB648)」または「[検索定義の編集](../c-about-settings-menu/c-about-searching-menu.md#task_AF1FFB1AEF874C13AB359C28F74BF461)」を参照してください。

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
      <td colname="col2"> <p>使用するバックエンド検索を選択できます。 <span class="wintitle"> SiteSearch </span>または<span class="wintitle">マーチャンダイジング</span>から選択できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>アカウント </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして<span class="uicontrol">Search&amp;Promote</span>を選択した場合にのみ使用できます。 </p> <p>検索するサイト検索/マーチャンダイジングのアカウントを選択できます。 通常、検索は、現在使用しているアカウント内を検索します。 ただし、プレゼンテーションテンプレートでは、他の任意のアカウントに対してバックエンド検索を使用できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>サーバー名/IP </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして<span class="uicontrol">マーチャンダイジング</span>を選択した場合にのみ使用できます。 </p> <p><span class="wintitle">マーチャンダイジング</span>検索がアクセスする<span class="wintitle">マーチャンダイジング</span>サーバーの完全な名前を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>サーバーポート </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして<span class="uicontrol">マーチャンダイジング</span>を選択した場合にのみ使用できます。 </p> <p><span class="wintitle">マーチャンダイジング</span>サーバーのポート番号を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ピラミッド </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして<span class="uicontrol">マーチャンダイジング</span>を選択した場合にのみ使用できます。 </p> <p><span class="wintitle">マーチャンダイジング</span>サーバー内のピラミッドを指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>結果数 </p> </td> 
      <td colname="col2"> <p>返す検索結果の数を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最初のページの結果数（異なる場合） </p> </td> 
      <td colname="col2"> <p>最初のページで返す結果の数を指定します。 他のページとは異なるページにする必要がある場合に、このオプションを使用します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>列数 </p> </td> 
      <td colname="col2"> <p>検索結果を分割する列数を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>検索の種類 </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして<span class="uicontrol">Search&amp;Promote</span>を選択した場合にのみ使用できます。 </p> <p>次の3種類の検索から選択できます。 </p> <p> 
        <ul id="ul_E1D8B3DE9DB24DE4813D53F6298A03A6"> 
          <li id="li_C3DD7AA7699B477A9EE0731CFC012630"> <span class="uicontrol"> all  </span> <p>クエリ文字列内のすべての単語を含むドキュメントを検索します。 </p> <p>検索語を無効にする前に「+」と「 — 」を使用し、これらの文字は無視されます。 </p> </li> 
          <li id="li_4C66B9EFEFA042908A4D3730F9F54EB0"> <span class="uicontrol"> 任意 </span> <p>「+」と「 — 」の語頭文字を使用できます。 </p> </li> 
          <li id="li_37E9AD42A61C4E31A0816DFB8E71118D"> <span class="uicontrol"> フレーズ  </span> <p>クエリ文字列は引用符で囲まれたフレーズとして扱われ、ユーザーが入力した引用符はすべて無視されます。 </p> <p>検索語を無効にする前に「+」と「 — 」を使用し、これらの文字は無視されます。 </p> </li> 
        </ul> </p> <p> クエリ内の各単語にファセット値を選択する可能性を持たせる場合、プライマリ検索では常に<span class="uicontrol">すべて</span>を使用する必要があります。 </p> <p>検索クエリでの+および — 修飾子の使用に関する検索のヒントを確認できます。 </p> <p><a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">検索について</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>コレクション </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして<span class="uicontrol">Search&amp;Promote</span>を選択した場合にのみ使用できます。 </p> <p>インデックス内で検索するコレクションを識別します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Promosearch </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして<span class="uicontrol">Search&amp;Promote</span>を選択した場合にのみ使用できます。 </p> <p>指定した<span class="uicontrol">検索結果数</span>に従って、検索結果からランダムに選択して使用できます。 </p> <p>プロモサーチは、従来の概念です。 そのため、サイト検索/マーチャンダイジング内で新しいバナー管理システムを使用することをお勧めします。 </p> <p><a href="../c-about-design-menu/c-about-banners.md#concept_5BBE01FEC6134393B43CC917C8CC64DA" type="concept" format="dita" scope="local">バナーについて</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファセットパラメータの適用 </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして<span class="uicontrol">Search&amp;Promote</span>を選択し、<span class="uicontrol">プロモサーチ</span>を選択した場合にのみ使用できます。 </p> <p>プロモーション検索で、選択したファセットを使用してプロモーションを絞り込むことを指定します。 ほとんどのプロモ検索アカウントでは、このオプションは使用されません。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>一致するプロモーションがない場合にデフォルトのプロモーションを指定する </p> </td> 
      <td colname="col2"> <p>このオプションは、ソースとして<span class="uicontrol">Search&amp;Promote</span>を選択し、<span class="uicontrol">プロモサーチ</span>を選択した場合にのみ使用できます。 </p> <p>プロモーションの最初の検索で何も見つからない場合に、プロモーションの別の検索を行うことを指定します。 2つ目のプロモーションの検索では、キーワードが削除されます。 代わりに、「is_default」メタデータフィールドが「yes」に設定されているすべてのプロモーションを探します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>検索のハイライト </p> </td> 
      <td colname="col2"> <p>「ヒーローゾーン」で強調したい、メイン検索から選択した数の結果を取り出します。 </p> <p>通常、ハイライト検索には、メイン検索と同様の検索条件がありますが、異なるランク付けメカニズムを使用して特定の結果をハイライトします。 重複はメイン検索から削除されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ベース検索 </p> </td> 
      <td colname="col2"> <p>このオプションは、「<span class="uicontrol">検索をハイライト</span>」を選択した場合にのみ使用できます。 </p> <p>結果をハイライト表示する検索結果を含む検索を選択できます。 重複はこの検索から削除されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>重複除外の優先度 </p> </td> 
      <td colname="col2"> <p>このオプションは、「<span class="uicontrol">検索をハイライト</span>」を選択した場合にのみ使用できます。 </p> <p>複数のハイライト検索を行うことができます。 </p> <p>複数のハイライト検索を使用する場合は、重複除外の優先度を指定する必要があります。ここで、「1」が最も高い優先度です。 </p> <p>例えば、2つの検索ハイライトがあるとします。ベストセラーと新製品 理論的には ベストセラーも新製品の可能性がある。 この場合、新しい商品とメイン検索から重複を削除します。 したがって、ベストセラーの優先度を1に、新製品の優先度を2に設定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>パラメーター </p> </td> 
      <td colname="col2"> <p>検索にCGIパラメーターを追加できます。 </p> <p><a scope="local" href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita">バックエンド検索CGIパラメーター</a>を参照してください。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）[!DNL Searches]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 検索定義{#task_1D8E991E4C4146B7A7311FAE5DAA3742}の削除

不要になった、または使用しなくなったガイド検索定義を削除できます。

<!-- 

t_deleting_a_search_definition.xml

 -->

[テンプレートについて](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5)を参照してください。

**検索定義を削除するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Searching]**/**[!UICONTROL Searches]**&#x200B;をクリックします。
1. [!DNL Searches]ページのテーブルで、削除する定義の行の&#x200B;**[!UICONTROL Delete]**&#x200B;をクリックします。
1. [!DNL Confirmation]ダイアログボックスで、**[!UICONTROL OK]**&#x200B;をクリックします。
1. （オプション）[!DNL Searches]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 固定結果キーワードマネージャについて{#concept_0C5F152C029C485D8872C6795CBCD7C7}

検索結果を特定の場所に手動でピン留めできます。 これらの固定された結果は、特定の検索クエリまたはキーワードに関連付けられます。 [!DNL Pinned Result Keyword Manager]を使用すると、検索結果をピン留めしたすべてのキーワードを管理できます。

<!-- 

c_about_pinned_results_keyword_manager.xml

 -->

## {#section_ED67A24BE884468286F34FA5DFF826D7}に従うキーワード検索ルール

パネルに入力する検索クエリには、次のルールがあります。

* 先頭と末尾の空白文字はクエリから削除されます。
* 次のような特殊な検索文字は使用できません。

   * アスタリスク(*)を使用したワイルドカード一致。
   * 必須または必須でないが、プラスまたはマイナス（+または — ）を使用しない。
   * コロン文字(:)を含むフィールド指定子はありません。
   * コンマや重複引用符（または&quot;）は使用できません。

* クエリ内でスペースで区切られた複数のキーワードまたは単語を使用できます。
* 大文字は小文字に変換されます。

検索用語は、そのまま記憶される。完全に同じ検索用語をもう一度使用して、完全に同じ結果を得る必要があります。

固定された結果は、大文字と小文字の区別をサポートしません。 すべてのキーワードの大文字は小文字に変換されます。

## 検索結果の順序変更{#section_46FBE5279C7740A09D6DC9F54FE104AA}

[!DNL Stage Add New Keyword]パネルまたは[!DNL Staged Edit Keyword]パネルでキーワードを検索すると、検索結果には次のインデックス操作後に何が起きるかが反映されます。 テーブル内の検索結果の順序は、3つの方法のいずれかで変更できます。

1つ目の方法は、**[!UICONTROL Pinned]**&#x200B;チェックボックスを使用します。 このチェックボックスを使用して、結果を特定の位置に固定します。 このチェックボックスを選択すると、このチェックボックスより上の検索結果もすべて固定されます。 この機能により、このチェックボックスより上のすべての結果が特定の順序で表示されます。 検索結果の固定を解除すると、現在ピン留めされているすべての結果の下にドロップします。

2つ目の方法は、テーブル内のドラッグ&amp;ドロップを使用する方法です。 ドラッグ&amp;ドロップで結果を新しい位置に移動できます。 結果を新しい場所にドラッグすると、新しい場所より上のすべての結果が固定されます。 この自動固定により、残りの結果が最近ドラッグした結果の上に表示されます。

3つ目の方法は、「#」列に特定の位置を入力して、ピン結果の順序を設定する方法です。 ドラッグ&amp;ドロップとは異なり、シミュレートされた検索結果の順序は、次に[!DNL Staged Edit Keyword]パネルを開いたときに明らかになります。 現在ピン留めされていない行の注文番号を設定すると、少なくとも多数の項目が固定されます。 現在ピン留めされている行の順序番号を設定すると、現在ピン留めされている項目内の項目の順序が設定されます。 ただし、ピン留めされた項目の数は増えません。

検索結果を保存する際に、[キーワード]フィールドに同じクエリを入力すると、再び結果を表示できます。

## 固定された検索結果について{#section_46780B7812F249F3B45503161C4FBDEE}

検索結果は、関連性のスコアで並べられることがよくあります。 ただし、固定検索結果では、関連性スコアが無視され、自然順序があらかじめ決められた位置で上書きされるよう試みます。 結果が相対的にその場所に留まるようにすることで、その上にある他の既知の検索結果を固定する必要があります。

パネルに表示される検索結果は、次のインデックスの後に表示される内容と同じになります。 ただし、元のドキュメントの変更やMember Centerでの設定の変更は、不一致の結果を生み出す可能性があります。 例えば、ドキュメントの内容の変更は、インデックスの後になるまで不明です。

ピン留めされた結果は関連性を無視するので、インデックスの後に同じ順序または同じ順序で表示されます。 ピン留めされていない結果は、指数の後、自然な位置に戻ります。ピン留めされていない結果の順序は保証されません。

## 新しいキーワードの追加{#task_8CED128DADD34D0DAD2C64B64D0D6B06}

新しいキーワードとその固定した結果を追加できます。

<!-- 

t_adding_a_new_keyword.xml

 -->

新しいキーワードを追加する際に、検索結果の順序を変更し、検索結果を特定の位置に固定することができます。

**新しいキーワードを追加するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Searching]**/**[!UICONTROL Pinned Results]**&#x200B;をクリックします。
1. [!DNL Pinned Keyword Results Manager]ページで、**[!UICONTROL Add New Keyword]**&#x200B;をクリックします。
1. [!DNL Add New Keyword]ページの&#x200B;**[!UICONTROL Keyword]**&#x200B;フィールドに検索クエリを入力し、**[!UICONTROL Search Keyword]**&#x200B;をクリックします。

   <!-- 
   
   r_keyword_options.xml
   
   -->

   「テーブルの編集」ボタンを使用して、検索結果のテーブルの表示方法を調整できます。 例えば、列のリストを使用して、特定の列の表示/非表示を切り替えることができます。 ドラッグ&amp;ドロップを使用して列の順序を並べ替えることもできます。

   次の表に、テーブルエディター内の列プロパティを示します。

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
      <td colname="col2"> <p>列の表示順序を指定します。 列をドラッグ&amp;ドロップして自動的に並べ替えることができます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フィールド名 </p> </td> 
      <td colname="col2"> <p><span class="wintitle">段階化された新しいキーワード</span>パネルと<span class="wintitle">段階化された編集キーワード</span>パネルの<span class="wintitle">シミュレートされた検索結果</span>テーブルに表示される列見出しの名前を識別します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>以下を含む </p> </td> 
      <td colname="col2"> <p>チェックボックスがオンの場合、列が「ピン結果テーブル」(Pinned Results Table)に表示されます。 このボックスが空の場合または選択解除されている場合、列はテーブルから消えます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URLを画像として表示 </p> </td> 
      <td colname="col2"> <p>この列に割り当てられたメタフィールドに、グラフィックや画像へのURLが含まれている場合、このチェックボックスをオンにすると、HTML画像タグがその列の周りに配置され、画像が表示されます。 見つからない画像または無効なリンクが空です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フィールドの長さ </p> </td> 
      <td colname="col2"> <p>楕円(...)で切り捨てる前に、表示するテキストの最大長を入力できます。 URLを画像として表示するように列を設定した場合、このフィールドは無効です。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. （オプション）次のいずれかの操作を行います。

   * 検索結果の順序を変更します。
   * **[!UICONTROL Edit Table]**&#x200B;をクリックして[!DNL Simulated Search Results]テーブルの表示を調整します。 終了したら、**[!UICONTROL Save Changes]**&#x200B;をクリックして[!DNL Add New Keyword]パネルに戻ります。

1. クリック **[!UICONTROL Save Search Results]**.
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。
1. （オプション）[!DNL Pinned Results Keyword Manager]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## キーワードの編集{#task_30C550A7350B4394B5B43536368A84B1}

既存のキーワードとその固定した結果を編集できます。

<!-- 

t_editing_a_keyword.xml

 -->

キーワードを編集する際に、検索結果の順序を変更し、検索結果を特定の位置に固定することができます。

**キーワードを編集するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Searching]**/**[!UICONTROL Pinned Results]**&#x200B;をクリックします。
1. [!DNL Pinned Keyword Results Manager]ページの表で、変更するキーワードの行の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。
1. [!DNL Edit Keyword]ページの&#x200B;**[!UICONTROL Keyword]**&#x200B;フィールドに検索クエリを入力し、**[!UICONTROL Search Keyword]**&#x200B;をクリックします。

   キーワード検索のルールに必ず従ってください。

   <!-- 
   
   r_keyword_options.xml
   
   -->

   「テーブルの編集」ボタンを使用して、検索結果のテーブルの表示方法を調整できます。 例えば、列のリストを使用して、特定の列の表示/非表示を切り替えることができます。 ドラッグ&amp;ドロップを使用して列の順序を並べ替えることもできます。

   次の表に、テーブルエディター内の列プロパティを示します。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>列 </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>注文 </p> </td> 
      <td colname="col2"> <p>列の表示順序を指定します。 列をドラッグ&amp;ドロップして自動的に並べ替えることができます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フィールド名 </p> </td> 
      <td colname="col2"> <p><span class="wintitle">段階化された新しいキーワード</span>パネルと<span class="wintitle">段階化された編集キーワード</span>パネルの<span class="wintitle">シミュレートされた検索結果</span>テーブルに表示される列見出しの名前を識別します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>以下を含む </p> </td> 
      <td colname="col2"> <p>チェックボックスがオンの場合、列が「ピン結果テーブル」(Pinned Results Table)に表示されます。 このボックスが空の場合または選択解除されている場合、列はテーブルから消えます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URLを画像として表示 </p> </td> 
      <td colname="col2"> <p>この列に割り当てられたメタフィールドに、グラフィックや画像へのURLが含まれている場合、このチェックボックスをオンにすると、HTML画像タグがその列の周りに配置され、画像が表示されます。 見つからない画像または無効なリンクが空です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フィールドの長さ </p> </td> 
      <td colname="col2"> <p>楕円(...)で切り捨てる前に、表示するテキストの最大長を入力できます。 URLを画像として表示するように列を設定した場合、このフィールドは無効です。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. （オプション）次のいずれかの操作を行います。

   * 検索結果の順序を変更します。
   * **[!UICONTROL Edit Table]**&#x200B;をクリックして[!DNL Simulated Search Results]テーブルの表示を調整します。

      「[新しいキーワードの追加](../c-about-settings-menu/c-about-searching-menu.md#task_8CED128DADD34D0DAD2C64B64D0D6B06)」を参照してください。

      終了したら、**[!UICONTROL Save Changes]**&#x200B;をクリックして[!DNL Add New Keyword]パネルに戻ります。

1. クリック **[!UICONTROL Save Search Results]**.
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。
1. （オプション）[!DNL Pinned Results Keyword Manager]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## キーワード{#task_F17D6357D6DD416495E6D4117899D81D}の削除

不要になったキーワードや使用しなくなったキーワードは削除できます。

<!-- 

t_deleting_a_keyword.xml

 -->

新しいキーワードを追加する際に、検索結果の順序を変更し、検索結果を特定の位置に固定することができます。

**キーワードを削除するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Searching]**/**[!UICONTROL Pinned Results]**&#x200B;をクリックします。
1. [!DNL Pinned Keyword Results Manager]ページの表で、削除するキーワードの行の&#x200B;**[!UICONTROL Delete]**&#x200B;をクリックします。
1. [!DNL Delete Keyword]ページで、**[!UICONTROL Delete]**&#x200B;をクリックします。
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。
1. （オプション）[!DNL Pinned Results Keyword Manager]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## コレクションについて{#concept_62E42ACE53D54EEE9273433B86259127}

コレクションを使用すると、顧客がWebサイトの特定の領域を検索できるので、検索対象をすばやく見つけることができます。

<!-- 

c_about_collections.xml

 -->

[検索について](../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8)を参照してください。

「[検索フォームでのコレクションの使用](../c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3)」を参照してください。

例えば、製品の販売やサポートサービスに関連するURLのコレクションを検索できます。 ユーザーが指定したコレクションを使用できるようにするには、[検索フォーム]メニューで検索フォームを更新する必要があります。

コレクション設定の効果がユーザーに表示される前に、サイトインデックスを作成し直します。

オプションの&#x200B;**[!UICONTROL Test Collections]**&#x200B;フィールドにWebサイトのURLを1つ入力し、**[!UICONTROL Test]**&#x200B;をクリックすると、コレクションをテストできます。 指定したページが属するコレクションが返されます。

各コレクションは、名前とURLマスクを持つ1行に指定されます。 URLマスクは、次のいずれかで構成できます。

* `https://www.mydomain.com/products.html`などのフルパス
* `https://www.mydomain.com/products`などの部分的なパス
* 正規式

   マスクを正規式にするには、コレクション名とURLマスクの間にキーワード`regexp`を挿入します。

   [正規式](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)を参照してください。

「コレクション」フィールドの各行に含めることができるURLマスクは1つだけです。 ただし、同じコレクション名に対して、異なる行で複数のURLマスクを指定できます。 次の例には、4つの異なるコレクション名と5つのURLマスクが含まれています。

```
Company Info https://www.yoursite.com/company 
Products https://www.yoursite.com/products 
FAQs regexp ^.*/faqs 
Support https://www.yoursite.com/email_support/ 
Support https://www.yoursite.com/phone_support/
```

この例では、検索フォームを更新してこれらのコレクションを含めた後、ユーザーは定義済みの各コレクションを個別に選択して検索できます。 `Support`コレクションには、両方のURLマスクに一致するファイルが含まれているので、このコレクションが選択されたときに`www.yoursite.com/email_support/`と`www.yoursite.com/phone_support`の両方のファイルが検索されます。

## コレクションの追加{#task_07732D0F00104E59AD421297A704B2F6}

コレクションを追加して、顧客がWebサイトの特定の領域を検索できるようにすることで、探しているものをすばやく見つけることができます。

<!-- 

t_adding_collections.xml

 -->

URLマスクの結果がユーザーに表示されるように、サイトインデックスを再構築してください。

「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。

**コレクションを追加するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Searching]**/**[!UICONTROL Collections]**&#x200B;をクリックします。
1. [!DNL Collections]フィールドに、コレクション名とURLマスクアドレスを1行に1つずつ入力します。
1. （オプション）[!DNL Collections]ページの&#x200B;**[!UICONTROL Test Collections]**&#x200B;フィールドに、WebサイトのテストURLマスクを入力し、**[!UICONTROL Test]**&#x200B;をクリックします。

   テストコレクションの出力ウィンドウが表示され、URLとコレクションの名前が示されます。
1. コレクションの追加が完了したら、「**[!UICONTROL Save Changes]**」をクリックします。
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。
1. （オプション）[!DNL Collections]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 制限について{#concept_B5B527E04EBF4E9AB5956EEF881DDBF1}

検索を実行する前に、参照URLとIPアドレスを調べて、その場所から検索が可能かどうかを判断します。 [!DNL Restrictions]で指定した内容によって、検索が許可されるかどうかが決まります。 検索が許可されない場合は、一般的なエラーページがリクエスト元に返されます。

<!-- 

c_about_restrictions.xml

 -->

制限の設定は、転送者URLマスクまたはIPアドレスマスクのいずれかとして指定できます。 どちらの制限も、検索を許可するマスクを含めたり、検索を拒否するマスクを除外したりします。

転送者URLとIPアドレス制限条件の両方を渡す場合は、検索が許可されます。 いずれかの設定で検索が許可されていない場合、検索が許可されている他の制限に関係なく、検索は失敗します。

例えば、検索リクエストの「HTTP転送者」フィールドが「exclude」転送者のURLマスクと一致する場合、要求元IPアドレスが「include」IPアドレスマスクと一致する場合でも、検索は失敗します。 転送者のURLまたはIPアドレスに一致するマスクがない場合、その場所がデフォルトで含まれます。

1行に各「マスクを含む」または「マスクを除外」を入力します。

## 転送者URLマスクまたはIPアドレスマスクの制限の追加{#task_E6FF2DD83E8D4B00A0E2809DC13A56C9}

制限の設定は、「転送者URLマスク」または「IPアドレスマスク」のいずれかで指定できます。 どちらの制限も、検索を許可するマスクを含めたり、検索を拒否するマスクを除外したりします。 転送者URLとIPアドレス制限条件の両方を渡す場合は、検索が許可されます。

<!-- 

t_adding_url_mask_or_jp_address_restrictions.xml

 -->

**転送者URLマスクまたはIPアドレスマスクの制限を追加するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Searching]**/**[!UICONTROL Restrictions]**&#x200B;をクリックします。
1. [!DNL Restrictions]ページで、必要な制限オプションを設定します。 転送者URLマスクアドレス、IPアドレスマスクアドレス、またはオプションで、サイトの検索を許可されていない顧客に対して表示されるカスタマイズWebページのURLアドレスを入力します。

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
      <td colname="col1"> <p>転送者URLマスク </p> </td> 
      <td colname="col2"> <p>HTTP転送者ヘッダーから転送者URLを読み取ります。 転送者URLと最初に一致するマスクによって、マスクが含むマスクの場合に検索を許可するかどうかが決まります。 または、マスクが除外マスクの場合に検索を許可しないかどうかを指定します。 転送者URLに一致するマスクがない場合は、そのURLが含まれ、検索が許可されます。 </p> <p> 検索テンプレートに新しい検索フォームが含まれている場合、または検索テンプレートに「次の10」、「前の10」、「概要を非表示」などのリンクを含めることができる場合は、検索結果テンプレートを「含む」マスクとしてリストします。 これを行う最も簡単な方法は、次の例のように、正規式を使用することです。 </p> <p> <span class="codeph"> regexp ^https?://[^/]*\.atomz\.com/を含めます。*[?&amp;]sp_a=sp1000130e.*$ </span> </p> <p>次の例には、5つの異なる転送者URLマスクが含まれています。 </p> <p> <code> include&nbsp;https://www.mydomain.com/search/ 
          include&nbsp;https://search.mydomain.com/ 
          include&nbsp;regexp&nbsp;^https://www.mydomain.com/help/.*/search/ 
          include&nbsp;regexp&nbsp;^https?://[^/]*\.atomz\.com/.*[?&amp;]sp_a=sp1000130e.*$ 
          exclude&nbsp;* </code> </p> <p>転送者URLマスクが次の場合： </p> <p> <code> https://www.mydomain.com/search/searchpage.html&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          https://search.mydomain.com/advanced/&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          https://www.mydomain.com/help/products/search/advanced/&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          https://www.mydomain.com/help/products/&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] 
          https://www.anotherdomain.com/&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] 
          blank&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>IPアドレスマスク </p> </td> 
      <td colname="col2"> <p>IPアドレスと最初に一致するマスクによって、マスクがインクルードマスクの場合に検索を許可するかどうかが決まります。 または、マスクが除外マスクの場合に検索を許可するかどうかを指定します。 要求元のIPアドレスに一致するマスクがない場合は、そのIPアドレスが含まれ、検索が許可されます。 </p> <p>次の例は、4つの異なるIPアドレスマスクを示しています。 </p> <p> <code> include&nbsp;64.128.192.* 
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
      <td colname="col2"> <p> 制限付きユーザーは、ここに入力したURLにリダイレクトされます。 このオプションを使用すると、サイトの検索を許可されていない顧客に対して表示する、独自のカスタムエラーページを作成できます。 </p> <p>URLを指定しない場合、制限付きユーザーがサイトを検索しようとすると、一般的なエラーページが返されます。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## プレビュー{#concept_DF293FD3B02C467F8842C8C21D62F294}について

[!DNL Preview]で設定したクエリ文字列とパラメーターは、検索フォームがソフトウェアでテストまたはプレビューされたときに常に使用されます。

<!-- 

c_about_preview.xml

 -->

[検索について](../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8)も参照してください。

## プレビュー{#task_CE267A0FF621474E80AB43B67B1C28D7}の値の設定

設定したプレビュー値は、検索フォームがソフトウェアでテストまたはプレビューされたときに常に使用されます。

<!-- 

t_setting_values_in_preview.xml

 -->

**プレビューに値を設定するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Searching]**/**[!UICONTROL Preview]**&#x200B;をクリックします。
1. [!DNL Preview]ページで、必要なオプションを設定します。

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
      <td colname="col2"> <p>デフォルトでは、クエリ文字列は<span class="codeph"> * </span>に設定され、通常は結果を返します。 ただし、Webサイトのコンテンツにより限定的なクエリを指定できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>パラメーター </p> </td> 
      <td colname="col2"> <p>パラメーターは、名前と値を使用して設定されます。 必要な数の追加パラメーターを指定できます。 例えば、<span class="codeph"> sp_q_1 </span>パラメーターと<span class="codeph"> sp_x_1 </span>パラメーターを使用して、追加の検索条件を指定できます。 パラメータ値<span class="codeph"> sp_q_1=windows&amp;sp_x_1=platform </span>は、検索ページの「platform」メタタグで、メインクエリに加えて「windows」という値を探すプレビュー検索を作成します。 </p> <p><a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local">バックエンド検索CGIパラメーター</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ホスト </p> </td> 
      <td colname="col2"> <p>Webサイトでプライベートドメインのラベル付けを使用している場合は、検索結果を正確にプレビューできるように適切なホスト名を設定します。 </p> <p>プライベートドメインのラベル付けについて詳しくは、カスタマーサポートにお問い合わせください。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## フィードについて{#concept_FEBFEE51A3AB49F88CBA0D16E2AD6916}

検索インデックスは、Webサイトの大規模なデータベースとして表示されます。 正しいメタタグから十分な情報を得ると、情報が収集され、データフィード内にシンジケート（シンジケート）されます。 これらのデータフィードは、サードパーティ受信者など、別のサービスに送信できます。

<!-- 

c_about_feeds.xml

 -->

Webサイトのクロールとインデックス作成が完了すると、自動フィードを生成して、サードパーティのオーガニック検索エンジンやショッピングエンジンに送信できます。 次のストリームフィードを作成できます。

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
   <td colname="col2"> <p>Recommendations フィードは、Adobe Recommendationsとデータシンジケーション機能を提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>汎用フィード </p> </td> 
   <td colname="col2"> <p>汎用フィードタイプを持つ多くのフィードを実装できます。 Webサイトのインデックスに対してカスタム検索クエリが作成されます。 データは、検索結果を表示するのと同じテンプレート言語を使用して、カスタマイズされた検索テンプレートを通じて返されます。 この種の柔軟性は、特定のフィードタイプに限らず、多くのベンダーにフィードを送信できることを意味します。 </p> <p>次のヘルプトピックの手順を使用して、トランスポート（検索）テンプレートを追加できます。 </p> <p>「<a href="../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012" type="task" format="dita" scope="local">新しいプレゼンテーションまたはトランスポートテンプレートファイルの追加</a>」を参照してください。 </p> <p> テンプレートを追加した後、検索テンプレートタグを使用して、テンプレートを編集し、含める検索メタデータフィールドとその形式を定義します。 </p> <p>「<a href="../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3" type="task" format="dita" scope="local">プレゼンテーションまたはトランスポートテンプレートの編集</a>」を参照してください。 </p> <p><a href="../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4" type="reference" format="dita" scope="local">検索テンプレートタグ</a>を参照してください。 </p> <p>トランスポートテンプレートファイルの名前を忘れないでください。 フィードの条件を指定する場合は、名前を使用して汎用フィードをテンプレートに連結します。 </p> <p>以前に他のフィードを扱ったことがある場合は、フィードフィールドを検索メタデータフィールドにマップしていることに注意してください。 汎用フィードは、<span class="uicontrol">フィードを作成</span>ウィザードでは、この手順を行いません。 代わりに、テンプレートはメタデータとメタデータの形式を指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Googleマーチャント </p> </td> 
   <td colname="col2"> <p>Google Merchant Centerを使用すると、複数のGoogleサービスを通じて製品を販売できます。 データシンジケーションコンポーネントを備えており、定期的に販売されている商品のリストを提出できます。 </p> <p>サードパーティのフィードベンダーと同様、Google Merchant Centerには、フィードが正当と見なされる前に満たす特定の標準があります。 詳細については、カスタマーサポートにお問い合わせの上、Googleマーチャントのドキュメントを参照してください。 以下に、Google Merchant Centerがフィードの検証時に考慮する要約を簡単に示します。 </p> 
    <ul id="ul_3D84D4A6A4BF4C08860F86403F8F9CD6"> 
     <li id="li_5B6516CC7BC7493B8B8E8AFB454E573F">各商品には商品ページがあり、専用のURL。 </li> 
     <li id="li_5A6D5AD5E1B54A94B224D19E888B5443"> 各製品バリアントのフィードには、個別のエントリがあります。 </li> 
     <li id="li_89748D3241B34A4493576DAC38681988"> 各製品には、好ましくはお使いのサーバから取得した画像URLが含まれています。 製品のバリエーションには、実際のバリエーションを示す特定の画像があります。 つまり、靴の色が異なっても同じイメージを共有してはならない。 </li> 
     <li id="li_A594AD19480F41EAA72181355F28447B"> 各製品には、利用可能な情報、条件、説明、カテゴリ、価格などの固有の情報が含まれています。 </li> 
     <li id="li_0955B3A6ED2746D2B7CB42DC8AB27D3A">一般に、各製品には、ISBN、UPC、JAN、EANなどの一意の識別子があります。 </li> 
     <li id="li_2C371653F1C5471FA638F3A3818ABC17">一般に、各製品はGoogleの製品分類で分類されます。 </li> 
     <li id="li_6EB392A5A0BE490FAED5BC5E83228E32"> 衣料品には、性別、年齢層、色、サイズなど、追加の必須フィールドがあります。 </li> 
     <li id="li_44B91FA9A95F4172A2F03F8206E9081E"> 税金と送料は、Google Merchant Center内またはこのフィード内の製品別のアカウント設定として指定されます。 </li> 
     <li id="li_71A63E9905B840C0A04F6CDAA23C9AB0"> 一部の規則では、カスタムメードの製品や特定のアパレル製品を免除することができますが、免除の許可や詳細については、Googleに問い合わせる必要があります。 </li> 
    </ul> <p>フィードの検証を制御する詳細は多数あります。 フィード管理について詳しくは、Googleマーチャントのドキュメントを参照してください。 Googleは仕様を頻繁に変更するので、ドキュメントをよく調べてください。 </p> <p>Google Merchant Centerに関連付けられているフィードは、多くの場合、Googleによる製品検索フィードと呼ばれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Googleサイトマップ </p> </td> 
   <td colname="col2"> <p>Googleサイトマップを使用すると、GoogleによるWebサイトのクロールに影響を与えることができます。 この場合、シンジケートされたデータフィード、サイトマップは定期的にGoogleサイトマップに送信されます。 サイトマップには、インターネットに到達可能なURLと、最終変更日やページの優先度などの特定の情報が各URLに関連付けられます。 このような情報をGoogleに提供すると、特定のページがクロールされ、インデックス付けされる頻度と可能性が高くなります。 通常の状況では、クローラーがアクセスできないリンクのリストを情報提供するためにサイトマップが使用される場合があります。 </p> <p>フィード機能を使用してGoogleサイトマップを作成したい場合は、カスタマー担当者にお問い合わせください。 Googleは、Google Sitemapサービスを一般向けに提供し、Google Webマスターツールページに関するドキュメントを提供しています。 </p> <p> <b>Googleサイトマップフィードを作成するための要件</b> </p> <p>Googleサイトマップフィードを作成するには、Google Sitemapが既に設定されているGoogle Webマスターツールアカウントを持っていることを確認してください。 Googleサイトマップの設定については、Google Webマスターツールのドキュメントを参照してください。 </p> <p>また、サイトマップファイルの配信方法を決定する必要もあります。 一般に、サイトマップファイルは、ドメイン、特にWebサイトのルートから作成されます。 単純なモデルは、ファイルをFTP経由でサーバに配信することです。 もう1つの解決策は、サイトマップファイルのリクエストをサイト検索/マーチャンダイジングコンテンツネットワークにリダイレクトすることです。 サイトマップフィードの配信の調整と設定については、コンサルティング担当者にお問い合わせください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

自動フィードに興味がある場合は、プロフェッショナルサービスにお問い合わせください。 各フィードでは、データの質とファイルの送信に関して厳しい要件があります。

選択したフィードのタイプは、**[!UICONTROL Create Feed]**&#x200B;ウィザードを使用してフィールドを作成する際に表示されるオプションに影響します。 フィードのタイプごとに、異なるデータ形式があります。 フィード受信者によるフィードの拒否や、不適切なデータの顧客への投稿が行われないように、適切なデータ形式に従ってください。 通常、データ形式の他に、ベンダーはデータを受け取る1つ以上の推奨される方法を持っています。 フィードについては、ベンダーのドキュメントを参照してください。

フィードの作成に関する課題は、サイト検索/マーチャンダイジングとフィードの間のデータを一致させることです。 通常、インデックスクロールから取得されたデータの形式が正しくないか、データが見つかりません。 以下は、フィードを作成する際に何を探すかに焦点を当てるのに役立つ質問のリストです。

* フィード受信者との取引関係のタイプは何ですか。
* フィード受信者に登録してアカウントを作成する必要がありますか？
* ベンダーに関するフィードに関する問題を監視および対処するのは誰ですか。 一般的に、ベンダーのアカウントを管理するのはお客様の責任です。 例えば、GoogleサイトマップにはWebMasterアカウントと、サイトマップの正常性を監視するユーザーが必要です。
* フィードのデータ形式とは何ですか。
* インデックスはフィードの文字エンコーディングと一致しますか？ タブ区切りデータ形式およびカンマ区切りデータ形式は、データにタブやカンマが含まれている場合に問題になります。
* データにタブやコンマが含まれている場合、どのようにしますか。
* インデックス内に空のデータを含むページはありますか？
* フィード受信者は空のデータを受け付けますか？ データがソフトウェアによって取得される条件を編集することで、空のデータを解決できる場合があります。
* データ形式は、フィード受信者が必要とする形式と一緒に表示されますか。 例えば、一部のフィード受信者は、価格と通貨の表示方法に固有のものです。
* 仕入先が受け入れることのできる最大数の品目があるか。 この潜在的な問題は、検索条件で結果を制限することで解決できます。
* 仕入先はフィードをどのように受け取りたいか。 FTP送信とHTTPホスティングがサポートされます。

## フィードの作成{#task_63179C1FC359497483CD6CE13FD1C250}

1つ以上のデータフィードを作成できます。

<!-- 

t_creating_a_feed.xml

 -->

**フィードを作成するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Searching]**/**[!UICONTROL Feeds]**&#x200B;をクリックします。
1. [!DNL Feeds]ページで、**[!UICONTROL Create Feed]**&#x200B;ドロップダウンリストからフィードのタイプを選択します。
1. 選択したフィードのタイプに応じて、[!DNL Create Feed]ダイアログボックスで、ウィザードの各パネルで指定したオプションを設定します。

   <!-- 
   
   r_feed_options.xml
   
   -->

   作成または編集するフィードのタイプによって、使用できるオプションが少し異なります。

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
      <td colname="col3"> <p>ベンダー固有のフィードフィールドを、サイト検索/マーチャンダイジングメタデータフィールドにマップできます。 このウィザードのマッピング手順は重要です。これは、フィードがインデックス内のフィールドとフィードデータ内のフィールドとの間の情報を関連付けることができるからです。 ほとんどの場合、<span class="wintitle">汎用フィード</span>を除き、相関関係は動的に生成された検索テンプレートに保存されます。 </p> <p><span class="wintitle">フィールドマップ</span>テーブルの各行は、フィールドマッピングを表します。 テーブルの追加/削除列で、<span class="uicontrol"> + </span>をクリックして、新しいフィールドマッピング行を追加します。「<span class="uicontrol"> - </span>」をクリックすると、現在選択されているフィールドマッピング行がテーブルから削除されます。 フィードフィールドをサイト検索/マーチャンダイジングメタデータフィールドに関連付けるには、それぞれのドロップダウンリストを使用して目的のフィールドを選択します。 </p> <p> <b>Adobe Recommendationsのフィールドマッピング</b> </p> <p>レコメンデーションデータフィードはCSVファイルで、データの列はコンマで区切って指定します。 CSVフィードファイル内の列の順序を決定するため、フィールドマップテーブル上の各マッピングの表示順序は重要です。 マッピングの行は次の順序で作成します。各行は必須です。 </p> <p> 
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
        </ol> </p> <p> <b>高度な使用方法</b> </p> <p>前述のように最初の9つの必須フィードフィールドをマッピングしたら、独自のカスタムフィールドを作成できます。 <span class="wintitle">フィードフィールド</span>ドロップダウンリストで、<span class="uicontrol">カスタム</span>をクリックします。 関連するテキストフィールドに、そのフィールドのカスタムタグ名を入力します。 このカスタムオプションは、フィードに特別なベンダー固有のフィールドが必要な場合に役立ちます。 </p> <p> <p>注意： レコメンデーションフィードの仕様では、各フィールド名の先頭に「entity」を付ける必要があると記載されていますが、この場合は不要です。 </p> </p> <p>カスタムメタデータフィールドを作成することもできます。 「<span class="wintitle">メタデータフィールド</span>」ドロップダウンリストで、「<span class="uicontrol">カスタム</span>」をクリックします。 関連するテキストフィールドに、カスタムメタデータフィールドの値を入力します。 この値は、事前に生成されたテンプレートに挿入され、カスタム検索テンプレートタグの挿入にも使用できます。 </p> <p><a href="../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4" type="reference" format="dita" scope="local">検索テンプレートタグ</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>3 </p> </td> 
      <td colname="col2"> <p>検索条件 </p> </td> 
      <td colname="col3"> <p>フィードファイルが生成されると、検索クエリを使用してデータがフィルターされます。 このパネルで、検索クエリに使用するフィルターを定義します。 </p> 
        <ul id="ul_799ECF61C03A44878C7182F8B88CC3AD"> 
        <li id="li_0763F600A4FB4650ACC28BF337EB50AF"> <span class="uicontrol"> Meta Field  </span> <p>フィルタリングに使用するメタデータフィールドを定義します。 </p> <p> <b>高度な使用方法</b> </p> <p>フィルタリングシステムは標準の検索クエリなので、ドロップダウンリストから「<span class="uicontrol">自由形式</span>」を選択して、CGI検索パラメーターとその値を入力できます。 URLエスケープが必要です。 検索引数<span class="codeph"> sp_q </span>は無視されます。 自由形式のテキストボックスは複数行に作成できます。 各行の間の引数は、自動的に&amp;で区切られます。 </p> <p><a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> CGIパラメーターの検索</a>を参照してください。 </p> </li> 
        <li id="li_756B776902AE4A0E95524442D663343E"> <span class="uicontrol"> 条件 </span> <p>フィルタリング操作を定義します。 ドロップダウンリストから選択したフィルタリング操作により、3列目に入力した定数値が適用されます。 </p> </li> 
        <li id="li_7ADEDB8747B241D78AC50F1AC75AE695"> <span class="uicontrol"> 値 </span> <p>定数値。 </p> </li> 
        <li id="li_4039A9BC2F74460B83BFF662B58DAA1B"> <span class="uicontrol"> アクション </span> <p>新しいフィールドマッピング行を追加するか、現在ハイライトされている行を削除します。 </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>4 </p> </td> 
      <td colname="col2"> <p>ファイルの送信 </p> </td> 
      <td colname="col3"> <p>フィードファイルの送信スケジュールを設定し、ファイルのアップロードに使用する方法を設定できます。 </p> 
        <ul id="ul_55E253F83BDA46BAABF2BE38F0918E80"> 
        <li id="li_877A376B5B30422FAC816E31D50EA508"> <span class="uicontrol"> スケジュール </span> <p>フィードが送信される最大頻度を設定します。 「<span class="uicontrol">なし</span>」を選択すると、フィードがオフになります。 その他の値は、フィードが再度送信されるまでの待機期間を定義します。 フィードを送信するタイミングの決定は、各インデックスで行われます。 つまり、インデックスの最後に、フィードがチェックされ、有効期限が切れていて、ベンダーが更新して送信する必要があるかどうかを確認します。 また、アカウントがベンダーに過剰に送信されるのを防ぐ方法としても使用されます。 一部のベンダーは、アップロードが頻繁に行われるデータフィードソースに対するポリシーを持っています。 送信の頻度に関するデータフィードベンダーのポリシーを必ず確認してください。 
          <!--The time of the last upload and the status of the upload feed is displayed here. If any other feeds are currently running, their status appears here instead. Each account processes one feed at a time. --> 
          <!--ick <uicontrol>Manual Upload</uicontrol> to generate the feed and push the files to the final destination. Any schedule restrictions that you have already set are ignored. --> </p> <p> 
          <!--If <uicontrol>Manual Upload</uicontrol> is dimmed (inactive), the account is currently processing this feed or another feed. An account only works with one feed at a time. --> </p> </li> 
        <li id="li_760F5068D3ED46C582AE41392A2CA342"> <span class="uicontrol"> アップロード方法  </span> <p>ほとんどのフィードには、ファイルを配布する方法が2つあります。FTPとホストコンテンツネットワークを参照してください。 </p> 
          <ul id="ul_666759EDDD034537AA7C0ED936A2F315"> 
          <li id="li_B4AD5CEEBB7B41C0B8DC291B95DC5F83"> <span class="uicontrol">FTP</span> <p>サイト検索/マーチャンダイジングサーバーはパッシブFTPを使用します。 </p> <p>ファイルを別のサーバーにプッシュするには、FTPしか使用できません。 </p> <p> <span class="uicontrol"> FTPサーバー </span> - FTPサーバーの名前を指定します。プロトコルや先行する「ftp://」は含めないでください。 </p> <p> <span class="uicontrol"> FTPユーザー名 </span> - FTPアカウント名を指定します。 </p> <p> <span class="uicontrol"> FTPパスワード </span> - FTPアカウントのパスワードを指定します。 </p> <p> <span class="uicontrol"> FTPファイル名 </span>  — 送信するファイルの名前を指定します。この名前は、フィードで複数のファイルが生成される場合にテンプレートとなります。通常、名前の末尾で拡張子の前に番号が増えます。 次に例を示します。basename.xml、basename1.xml、basename2.xml、...、basename-Nth.xml </p> <p> <span class="uicontrol"> FTPディレクトリ </span>  — 特定のディレクトリパスが必要な場合は、ここに入力します。パスにファイル名を含めないでください。 </p> </li> 
          <li id="li_C082D3993C6C469B9067F207703BE619"> <span class="uicontrol"> ホストコンテンツネットワーク  </span> <p>コンテンツネットワークは、サイト検索/マーチャンダイジングのWebサーバーからファイルを提供する手段です。 フィードの受信者は、HTTPリクエストを使用してWebサーバーから取り込みます。 この設定に必要な情報は<span class="uicontrol">コンテンツネットワークファイル名</span>だけです。 ファイル名は、提供されるファイルの基本名です。 ファイル名の拡張子が付いたファイル名のみを使用してください。 フィードに応じて、ファイル名は複数のファイルのテンプレートになります。フィードによって次の形式で複数のファイルが生成される場合があります。basename.xml、basename1.xml、basename2.xml、...、basename-Nth.xml。 </p> <p>ベースファイル名を入力し、フィードが正常に保存されると、コンテンツネットワークファイルのURLがウィザードの検証パネルに表示されます。 URLは、フィードが正常に処理されるとアクティブになります。 ベンダーは、このURLからフィードデータを取得できます。 複数のファイルが同じURLパスを使用します。 ただし、定義済みリストスキームに従ってファイル名を置き換えたり、変更したりする必要があります。 </p> </li> 
          </ul> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>5 </p> </td> 
      <td colname="col2"> <p>検証 </p> </td> 
      <td colname="col3"> <p><span class="wintitle">検証</span>パネルに移動すると、その時点でフィードが保存されます。 ただし、実際のフィードファイルは後で保存されます。 </p> <p><span class="wintitle">検証</span>パネルでは、次の操作を実行できます。 </p> 
        <ul id="ul_0C6EFB38E06F401696084863D85CBD0D"> 
        <li id="li_07FC9F04C7F640048546F9DC5D91DA1D"> <span class="uicontrol"> データ表示  </span> <p>リンクをクリックして、表形式で表示されるデータ表示を通してフィードの出力を確認できます。 また、データ表示は、選択したメタフィールドと、ウィザードの<span class="wintitle">検索条件</span>パネルで指定した検索条件がフィードの出力にどのように影響するかを示すことで、トラブルシューティングに役立ちます。 データ表示は動的に生成されるので、いつでも使用できます。 </p> </li> 
        <li id="li_67046A56D08C48298E5A3E1F9C4A8AF3"> <span class="uicontrol"> フィードファイル  </span> <p>サイト検索/マーチャンダイジングサーバーがフィードファイルを生成したら、<span class="uicontrol">フィードファイル</span>ドロップダウンリストを使用して、サーバーからファイルを表示できます。 新しいブラウザータブまたは新しいブラウザーウィンドウが開き、フィードのコンテンツが表示されます。 この方法は、フォーマットの問題があるフィードのトラブルシューティングに役立ちます。 最終的な宛先またはベンダー自身のファイルは表示しないことに注意してください。 </p> <p> フィードが新しい場合は、フィードファイルを生成するまで、ドロップダウンリストは空になります。 </p> </li> 
        <li id="li_99D66C7AD87A475CB3D831D514DB78A0"> <span class="uicontrol"> コンテンツネットワークリンク  </span> <p>ウィザードの<span class="wintitle">ファイル送信</span>パネルで、アップロード方法として「<span class="uicontrol">ホストコンテンツネットワーク</span>」を選択した場合、URLはここに表示されます。 フィードファイルをまだ生成していない場合は、フィードが正常に生成されるまで、URLは無効です。 </p> </li> 
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
      <td colname="col2"> <p>フィード名 </p> </td> 
      <td colname="col3"> <p>フィードの名前を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>2 </p> </td> 
      <td colname="col2"> <p>検索条件 </p> </td> 
      <td colname="col3"> <p>フィードファイルが生成されると、検索クエリを使用してデータがフィルターされます。 このパネルで、検索クエリに使用するフィルターを定義します。 </p> 
        <ul id="ul_C750687E69A647D0A4440FF1B6CC7E05"> 
        <li id="li_B5C3B8523D71472E9508A04E23AC0211"> <span class="uicontrol"> Meta Field  </span> <p>フィルタリングに使用するメタデータフィールドを定義します。 </p> <p> <b>高度な使用方法</b> </p> <p>フィルタリングシステムは標準の検索クエリなので、ドロップダウンリストから「<span class="uicontrol">自由形式</span>」を選択して、CGI検索パラメーターとその値を入力できます。 URLエスケープが必要です。 検索引数<span class="codeph"> sp_q </span>は無視されます。 自由形式のテキストボックスは複数行に作成できます。 各行の間の引数は、自動的に&amp;で区切られます。 </p> <p><a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> CGIパラメーターの検索</a>を参照してください。 </p> </li> 
        <li id="li_D1E49834BBEA42CC8C49AE7D72037C53"> <span class="uicontrol"> 条件 </span> <p>フィルタリング操作を定義します。 ドロップダウンリストから選択したフィルタリング操作により、3列目に入力した定数値が適用されます。 </p> </li> 
        <li id="li_D5F0651B834F4EACAD15A2D154A0737B"> <span class="uicontrol"> 値 </span> <p>定数値。 </p> </li> 
        <li id="li_FC8F382BD20C4518BC2230D4B4954591"> <span class="uicontrol"> アクション </span> <p>新しいフィールドマッピング行を追加するか、現在ハイライトされている行を削除します。 </p> </li> 
        </ul> <p>汎用フィードには、特別なCGIパラメーターを指定する必要があります。 このフィードに関連付けられている特別なテンプレートを連結するには、<span class="codeph"> sp_t </span>パラメータを定義します。 <span class="codeph"> sp_t </span>の値をトランスポートテンプレートファイルの名前に設定します。 例えば、<span class="codeph"> super_feed.tpl </span>という名前のトランスポートテンプレートファイルを追加した場合、カスタムCGI検索パラメーターを<span class="codeph"> sp_t=super_feed </span>として作成します。 <span class="codeph"> sp_t </span>を入力するテキストボックスは、<span class="wintitle">メタフィールド</span>ドロップダウンリストから<span class="uicontrol">フリーフォーム</span>を選択するまで表示されません。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>ファイルの送信 </p> </td> 
      <td colname="col3"> <p>フィードファイルの送信スケジュールを設定し、ファイルのアップロードに使用する方法を設定できます。 </p> 
        <ul id="ul_30E830C41F6A4526822AF1FD3083075A"> 
        <li id="li_79EAFDBD2B9F411EA985CAEC1BAF3926"> <span class="uicontrol"> スケジュール </span> <p>フィードが送信される最大頻度を設定します。 「<span class="uicontrol">なし</span>」を選択すると、フィードがオフになります。 その他の値は、フィードが再度送信されるまでの待機期間を定義します。 フィードを送信するタイミングの決定は、各インデックスで行われます。 つまり、インデックスの最後に、フィードがチェックされ、有効期限が切れていて、ベンダーが更新して送信する必要があるかどうかを確認します。 また、アカウントがベンダーに過剰に送信されるのを防ぐ方法としても使用されます。 一部のベンダーは、アップロードが頻繁に行われるデータフィードソースに対するポリシーを持っています。 フィードベンダーのポリシーで、送信の頻度を確認してください。 
          <!--he time of the last upload and the status of the upload feed is displayed here. If any other feeds are currently running, their status appears here instead. Each account processes one feed at a time. --> 
          <!--<uicontrol>Manual Upload</uicontrol> to generate the feed and push the files to the final destination. Any schedule restrictions that you have already set are ignored. --> </p> <p> 
          <!--If <uicontrol>Manual Upload</uicontrol> is dimmed (inactive), the account is currently processing this feed or another feed. An account only works with one feed at a time. --> </p> </li> 
        <li id="li_20BF70A19E7E45BA91CD972E2FCE0EA4"> <span class="uicontrol"> アップロード方法  </span> <p>ほとんどのフィードには、ファイルを配布する方法が2つあります。FTPとホストコンテンツネットワークを参照してください。 </p> 
          <ul id="ul_5888C2E9097645CE89938EE09F8CB4F1"> 
          <li id="li_EA9ED19F3BEA4BEAB1A9F2C2FAFF85F7"> <span class="uicontrol">FTP</span> <p>サイト検索/マーチャンダイジングサーバーはパッシブFTPを使用します。 </p> <p>ファイルを別のサーバーにプッシュするには、FTPしか使用できません。 </p> <p> <span class="uicontrol"> FTPサーバー </span> - FTPサーバーの名前を指定します。プロトコルや先行する「ftp://」は含めないでください。 </p> <p> <span class="uicontrol"> FTPユーザー名 </span> - FTPアカウント名を指定します。 </p> <p> <span class="uicontrol"> FTPパスワード </span> - FTPアカウントのパスワードを指定します。 </p> <p> <span class="uicontrol"> FTPファイル名 </span>  — 送信するファイルの名前を指定します。この名前は、フィードで複数のファイルが生成される場合にテンプレートとなります。通常、名前の末尾で拡張子の前に番号が増えます。 次に例を示します。basename.xml、basename1.xml、basename2.xml、...、basename-Nth.xml </p> <p> <span class="uicontrol"> FTPディレクトリ </span>  — 特定のディレクトリパスが必要な場合は、ここに入力します。パスにファイル名を含めないでください。 </p> </li> 
          <li id="li_181268A7EE40456CA1DB768E8C66EEB9"> <span class="uicontrol"> ホストコンテンツネットワーク  </span> <p>ホストコンテンツネットワークは、サイト検索/マーチャンダイジングのWebサーバーからファイルを提供する手段です。 フィードの受信者は、HTTPリクエストを使用してWebサーバーから取り込みます。 この設定に必要な情報は<span class="uicontrol">コンテンツネットワークファイル名</span>だけです。 ファイル名は、提供されるファイルの基本名です。 ファイル名の拡張子が付いたファイル名のみを使用してください。 
            <!--Depending on the feed, the file name is a template for multiple files where the feed might generate multiple files in the following format: basename.xml, basename1.xml, basename2.xml, ..., basename-Nth.xml. --> </p> <p>ベースファイル名を入力し、フィードが正常に保存されると、コンテンツネットワークファイルのURLがウィザードの検証パネルに表示されます。 URLは、フィードが正常に処理されるとアクティブになります。 ベンダーは、このURLからフィードデータを取得できます。 </p> </li> 
          </ul> </li> 
        <li id="li_4DF56FA607A7479296CDA042A63C5A2C"> <p> <b>タブを保持しますか？</b> </p> <p>フィード内のタブ文字を維持します。 </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>4 </p> </td> 
      <td colname="col2"> <p>検証 </p> </td> 
      <td colname="col3"> <p><span class="wintitle">検証</span>パネルに移動すると、その時点でフィードが保存されます。 ただし、実際のフィードファイルは後で保存されます。 </p> <p><span class="wintitle">検証</span>パネルでは、次の操作を実行できます。 </p> 
        <ul id="ul_7420C415987448A796DD979CF5FA2EB6"> 
        <li id="li_AF02E8609B7B4F20A01AF4E010308E15"> <span class="uicontrol"> データ表示  </span> <p>リンクをクリックして、表形式で表示されるデータ表示を通してフィードの出力を確認できます。 また、データ表示は、選択したメタフィールドと、ウィザードの<span class="wintitle">検索条件</span>パネルで指定した検索条件がフィードの出力にどのように影響するかを示すことで、トラブルシューティングに役立ちます。 データ表示は動的に生成されるので、いつでも使用できます。 </p> </li> 
        <li id="li_32CEB8885C184354BFA1773BA66DB7A7"> <span class="uicontrol"> フィードファイル  </span> <p>サイト検索/マーチャンダイジングサーバーがフィードファイルを生成したら、<span class="uicontrol">フィードファイル</span>ドロップダウンリストを使用して、サーバーからファイルを表示できます。 新しいブラウザータブまたは新しいブラウザーウィンドウが開き、フィードのコンテンツが表示されます。 この方法は、フォーマットの問題があるフィードのトラブルシューティングに役立ちます。 最終的な宛先またはベンダー自身のファイルは表示しないことに注意してください。 </p> <p> フィードが新しい場合は、フィードファイルを生成するまで、ドロップダウンリストは空になります。 </p> </li> 
        <li id="li_8D1B876B0EC2455C8654EC573EC53FA9"> <span class="uicontrol"> コンテンツネットワークリンク  </span> <p>ウィザードの<span class="wintitle">ファイル送信</span>パネルで、アップロード方法として「<span class="uicontrol">ホストコンテンツネットワーク</span>」を選択した場合、URLはここに表示されます。 フィードファイルをまだ生成していない場合は、フィードが正常に生成されるまで、URLは無効です。 </p> </li> 
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
      <td colname="col1"> <p>3 </p> </td> 
      <td colname="col2"> <p>フィード名 </p> </td> 
      <td colname="col3"> <p>フィードの名前を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>2 </p> </td> 
      <td colname="col2"> <p>フィールドマップ </p> </td> 
      <td colname="col3"> <p>ベンダー固有のフィードフィールドを、サイト検索/マーチャンダイジングメタデータフィールドにマップできます。 このウィザードのマッピング手順は重要です。これは、フィードがインデックス内のフィールドとフィードデータ内のフィールドとの間の情報を関連付けることができるからです。 ほとんどの場合、<span class="wintitle">汎用フィード</span>を除き、相関関係は動的に生成された検索テンプレートに保存されます。 </p> <p>フィールドマップテーブルの各行は、フィールドマッピングを表します。 テーブルの<span class="wintitle">追加/Remove </span>列で、<span class="uicontrol"> + </span>をクリックして、新しいフィールドマッピング行を追加します。「<span class="uicontrol"> - </span>」をクリックすると、現在選択されているフィールドマッピング行がテーブルから削除されます。 フィードフィールドをサイト検索/マーチャンダイジングメタデータフィールドに関連付けるには、それぞれのドロップダウンリストを使用して目的のフィールドを選択します。 </p> <p> <b>高度な使用方法</b> </p> <p>独自のカスタムフィールドを作成できます。 <span class="wintitle">フィードフィールド</span>ドロップダウンリストで、<span class="uicontrol">カスタム</span>をクリックします。 関連するテキストフィールドに、そのフィールドのカスタムタグ名を入力します。 このカスタムオプションは、フィードに特別なベンダー固有のフィールドが必要な場合に役立ちます。 </p> <p>カスタムメタデータフィールドを作成することもできます。 「<span class="wintitle">メタデータフィールド</span>」ドロップダウンリストで、「<span class="uicontrol">カスタム</span>」をクリックします。 関連するテキストフィールドに、カスタムメタデータフィールドの値を入力します。 この値は、事前に生成されたテンプレートに挿入され、カスタム検索テンプレートタグの挿入にも使用できます。 </p> <p><a href="../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4" type="reference" format="dita" scope="local">検索テンプレートタグ</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>検索条件 </p> </td> 
      <td colname="col3"> <p>フィードファイルが生成されると、検索クエリを使用してデータがフィルターされます。 このパネルで、検索クエリに使用するフィルターを定義します。 </p> 
        <ul id="ul_8179321A58BB4C72B0CDB2B2BEC58FE4"> 
        <li id="li_9F8008A2398A4667B106BC49C94E5E3E"> <span class="uicontrol"> Meta Field  </span> <p>フィルタリングに使用するメタデータフィールドを定義します。 </p> <p> <b>高度な使用方法</b> </p> <p>フィルタリングシステムは標準の検索クエリなので、ドロップダウンリストから「<span class="uicontrol">自由形式</span>」を選択して、CGI検索パラメーターとその値を入力できます。 URLエスケープが必要です。 検索引数<span class="codeph"> sp_q </span>は無視されます。 自由形式のテキストボックスは複数行に作成できます。 各行の間の引数は、自動的に&amp;で区切られます。 </p> <p><a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> CGIパラメーターの検索</a>を参照してください。 </p> </li> 
        <li id="li_50C9CE59E9E5418895F8C1A070560063"> <span class="uicontrol"> 条件 </span> <p>フィルタリング操作を定義します。 ドロップダウンリストから選択したフィルタリング操作により、3列目に入力した定数値が適用されます。 </p> </li> 
        <li id="li_9F86D0F5010046A4A9F93DBA5FB158B3"> <span class="uicontrol"> 値 </span> <p>定数値。 </p> </li> 
        <li id="li_1051AFD5AEA447D0AF5FAB305E1D1E64"> <span class="uicontrol"> アクション </span> <p>新しいフィールドマッピング行を追加するか、現在ハイライトされている行を削除します。 </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>4 </p> </td> 
      <td colname="col2"> <p>ファイルの送信 </p> </td> 
      <td colname="col3"> <p>フィードファイルの送信スケジュールを設定し、ファイルのアップロードに使用する方法を設定できます。 </p> 
        <ul id="ul_A6A3C333AADD4438B835BF3E16E2AEFF"> 
        <li id="li_FCC4DAF198E149278B5CFB870CB6218C"> <span class="uicontrol"> スケジュール </span> <p>フィードが送信される最大頻度を設定します。 「<span class="uicontrol">なし</span>」を選択すると、フィードがオフになります。 その他の値は、フィードが再度送信されるまでの待機期間を定義します。 フィードを送信するタイミングの決定は、各インデックスで行われます。 つまり、インデックスの最後に、フィードがチェックされ、有効期限が切れていて、ベンダーが更新して送信する必要があるかどうかを確認します。 また、アカウントがベンダーに過剰に送信されるのを防ぐ方法としても使用されます。 一部のベンダーは、アップロードが頻繁に行われるデータフィードソースに対するポリシーを持っています。 フィードベンダーのポリシーで、送信の頻度を確認してください。 </p> <p> 
          <!--The time of the last upload and the status of the upload feed is displayed here. If any other feeds are currently running, their status appears here instead. Each account processes one feed at a time. --> </p> <p> 
          <!--Click <uicontrol>Manual Upload</uicontrol> to generate the feed and push the files to the final destination. Any schedule restrictions that you have already set are ignored. --> </p> <p> 
          <!--If <uicontrol>Manual Upload</uicontrol> is dimmed (inactive), the account is currently processing this feed or another feed. An account only works with one feed at a time. --> </p> </li> 
        <li id="li_2D9ECAFB8E8544D39B486F7BC3DCE589"> <span class="uicontrol"> アップロード方法  </span> <p>ほとんどのフィードには、ファイルを配布する方法が2つあります。FTPとホストコンテンツネットワークを参照してください。 </p> <p>データフィードを送信する場合の推奨アップロード方法は<span class="uicontrol"> FTP </span>です。 この目的で、Google Merchant CenterがFTPサーバーをホストします。 このGoogle製品検索フィードに対するGoogle FTPアカウントの個別設定については、Google Merchant Centerヘルプを参照してください。 </p> 
          <ul id="ul_BC0D8B541068407883CAC948496DBD0A"> 
          <li id="li_DB28CA23C94A4AF09E1A0EB06DF8F40C"> <span class="uicontrol">FTP</span> <p>サイト検索/マーチャンダイジングサーバーはパッシブFTPを使用します。 </p> <p>ファイルを別のサーバーにプッシュするには、FTPしか使用できません。 </p> <p> <span class="uicontrol"> FTPサーバー </span> - FTPサーバーの名前を指定します。この場合、 
            <code>
              uploads.google.com 
            </code>. プロトコルや先行する「ftp://」は含めないでください。 </p> <p> <span class="uicontrol"> FTPユーザー名 </span> - FTPアカウント名を指定します。 </p> <p> <span class="uicontrol"> FTPパスワード </span> - FTPアカウントのパスワードを指定します。 </p> <p> <span class="uicontrol"> FTPファイル名 </span>  — 送信するファイルの名前を指定します。この名前は、フィードで複数のファイルが生成される場合にテンプレートとなります。通常、名前の末尾で拡張子の前に番号が増えます。 次に例を示します。basename.xml、basename1.xml、basename2.xml、...、basename-Nth.xml </p> <p> <span class="uicontrol"> FTPディレクトリ </span>  — 特定のディレクトリパスが必要な場合は、ここに入力します。パスにファイル名を含めないでください。 </p> </li> 
          <li id="li_5990927146434DAF89273F4636D21437"> <span class="uicontrol"> ホストコンテンツネットワーク  </span> <p>コンテンツネットワークは、サイト検索/マーチャンダイジングのWebサーバーからファイルを提供する手段です。 フィードの受信者は、HTTPリクエストを使用してWebサーバーから取り込みます。 </p> <p> 
            <!--After the base filename is entered and the feed is successfully saved, the URL of the Content Network file is displayed on the Verification panel of the wizard. The URL becomes active after the feed is successfully processed. The vendor can get the feed data from this URL. Multiple files use the same URL path. However, be sure that you replace or change the filename according to the enumeration scheme. --> </p> </li> 
          </ul> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>5 </p> </td> 
      <td colname="col2"> <p>検証 </p> </td> 
      <td colname="col3"> <p><span class="wintitle">検証</span>パネルに移動すると、その時点でフィードが保存されます。 ただし、実際のフィードファイルは後で保存されます。 </p> <p><span class="wintitle">検証</span>パネルでは、次の操作を実行できます。 </p> 
        <ul id="ul_4A94355A8DF840A3BAF6BD5E9F11C27F"> 
        <li id="li_825697CB36B34C4AB5959B15EDDB55F1"> <span class="uicontrol"> データ表示  </span> <p>リンクをクリックして、表形式で表示されるデータ表示を通してフィードの出力を確認できます。 また、データ表示は、選択したメタフィールドと、ウィザードの<span class="wintitle">検索条件</span>パネルで指定した検索条件がフィードの出力にどのように影響するかを示すことで、トラブルシューティングに役立ちます。 データ表示は動的に生成されるので、いつでも使用できます。 </p> </li> 
        <li id="li_91B8B5F5F9DE4A13863CD62F74AA6206"> <span class="uicontrol"> フィードファイル  </span> <p>サイト検索/マーチャンダイジングサーバーがフィードファイルを生成したら、<span class="uicontrol">フィードファイル</span>ドロップダウンリストを使用して、サーバーからファイルを表示できます。 新しいブラウザータブまたは新しいブラウザーウィンドウが開き、フィードのコンテンツが表示されます。 この方法は、フォーマットの問題があるフィードのトラブルシューティングに役立ちます。 最終的な宛先またはベンダー自身のファイルは表示しないことに注意してください。 </p> <p> フィードが新しい場合は、フィードファイルを生成するまで、ドロップダウンリストは空になります。 </p> </li> 
        <li id="li_4A5EC089628E43029A38F8919888FF0A"> <span class="uicontrol"> コンテンツネットワークリンク  </span> <p>ウィザードの<span class="wintitle">ファイル送信</span>パネルで、アップロード方法として「<span class="uicontrol">ホストコンテンツネットワーク</span>」を選択した場合、URLはここに表示されます。 フィードファイルをまだ生成していない場合は、フィードが正常に生成されるまで、URLは無効です。 </p> </li> 
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
      <td colname="col1"> <p>3 </p> </td> 
      <td colname="col2"> <p>フィード名 </p> </td> 
      <td colname="col3"> <p>フィードの名前を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>2 </p> </td> 
      <td colname="col2"> <p>フィールドマップ </p> </td> 
      <td colname="col3"> <p>ベンダー固有のフィードフィールドを、サイト検索/マーチャンダイジングメタデータフィールドにマップできます。 このウィザードのマッピング手順は重要です。これは、フィードがインデックス内のフィールドとフィードデータ内のフィールドとの間の情報を関連付けることができるからです。 ほとんどの場合、<span class="wintitle">汎用フィード</span>を除き、相関関係は動的に生成された検索テンプレートに保存されます。 </p> <p>フィールドマップテーブルの各行は、フィールドマッピングを表します。 テーブルの追加/削除列で、<span class="uicontrol"> + </span>をクリックして、新しいフィールドマッピング行を追加します。「<span class="uicontrol"> - </span>」をクリックすると、現在選択されているフィールドマッピング行がテーブルから削除されます。 フィードフィールドをメタデータフィールドに関連付けるには、それぞれのドロップダウンリストを使用して目的のフィールドを選択します。 </p> <p> <b>高度な使用方法</b> </p> <p>独自のカスタムフィールドを作成できます。 <span class="wintitle">フィードフィールド</span>ドロップダウンリストで、<span class="uicontrol">カスタム</span>をクリックします。 関連するテキストフィールドに、そのフィールドのカスタムタグ名を入力します。 このカスタムオプションは、フィードに特別なベンダー固有のフィールドが必要な場合に役立ちます。 </p> <p>カスタムメタデータフィールドを作成することもできます。 「<span class="wintitle">メタデータフィールド</span>」ドロップダウンリストで、「<span class="uicontrol">カスタム</span>」をクリックします。 関連するテキストフィールドに、カスタムメタデータフィールドの値を入力します。 この値は、事前に生成されたテンプレートに挿入され、カスタム検索テンプレートタグの挿入にも使用できます。 </p> <p><a href="../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4" type="reference" format="dita" scope="local">検索テンプレートタグ</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>検索条件 </p> </td> 
      <td colname="col3"> <p>フィードファイルが生成されると、検索クエリを使用してデータがフィルターされます。 このパネルで、検索クエリに使用するフィルターを定義します。 </p> 
        <ul id="ul_994585E89A044BD3A89A99D30F277432"> 
        <li id="li_61FA9246B9824E3C8124958C8EBFF0DA"> <span class="uicontrol"> Meta Field  </span> <p>フィルタリングに使用するメタデータフィールドを定義します。 </p> <p> <b>高度な使用方法</b> </p> <p>フィルタリングシステムは標準の検索クエリなので、ドロップダウンリストから「<span class="uicontrol">自由形式</span>」を選択して、CGI検索パラメーターとその値を入力できます。 URLエスケープが必要です。 検索引数<span class="codeph"> sp_q </span>は無視されます。 自由形式のテキストボックスは複数行に作成できます。 各行の間の引数は、自動的に&amp;で区切られます。 </p> <p><a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> CGIパラメーターの検索</a>を参照してください。 </p> </li> 
        <li id="li_A5D00883738845C8B8F612A7521F160F"> <span class="uicontrol"> 条件 </span> <p>フィルタリング操作を定義します。 ドロップダウンリストから選択したフィルタリング操作により、3列目に入力した定数値が適用されます。 </p> </li> 
        <li id="li_5A312C2984454C2CB518CA453AD9F6D2"> <span class="uicontrol"> 値 </span> <p>定数値。 </p> </li> 
        <li id="li_666AAE1BC7A2432E91953B08EC7394DC"> <span class="uicontrol"> アクション </span> <p>新しいフィールドマッピング行を追加するか、現在ハイライトされている行を削除します。 </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>4 </p> </td> 
      <td colname="col2"> <p>ファイルの送信 </p> </td> 
      <td colname="col3"> <p>フィードファイルの送信スケジュールを設定し、ファイルのアップロードに使用する方法を設定できます。 </p> 
        <ul id="ul_49B3255BE669424B925BBAEE4C9B385F"> 
        <li id="li_939828C774D440EBB0769F6D5B0BBA23"> <span class="uicontrol"> スケジュール </span> <p>フィードが送信される最大頻度を設定します。 「<span class="uicontrol">なし</span>」を選択すると、フィードがオフになります。 その他の値は、フィードが再度送信されるまでの待機期間を定義します。 フィードを送信するタイミングの決定は、各インデックスで行われます。 つまり、インデックスの最後に、フィードがチェックされ、有効期限が切れていて、ベンダーが更新して送信する必要があるかどうかを確認します。 また、アカウントがベンダーに過剰に送信されるのを防ぐ方法としても使用されます。 一部のベンダーは、アップロードが頻繁に行われるデータフィードソースに対するポリシーを持っています。 フィードベンダーのポリシーで、送信の頻度を確認してください。 </p> <p> 
          <!--The time of the last upload and the status of the upload feed is displayed here. If any other feeds are currently running, their status appears here instead. Each account processes one feed at a time. --> </p> <p> 
          <!--Click <uicontrol>Manual Upload</uicontrol> to generate the feed and push the files to the final destination. Any schedule restrictions that you have already set are ignored. --> </p> <p> 
          <!--If <uicontrol>Manual Upload</uicontrol> is dimmed (inactive), the account is currently processing this feed or another feed. An account only works with one feed at a time. --> </p> </li> 
        <li id="li_07B5BCF7936241A7915C4898B231184B"> <span class="uicontrol"> アップロード方法  </span> <p>ほとんどのフィードには、ファイルを配布する方法が2つあります。FTPとホストコンテンツネットワークを参照してください。 </p> 
          <ul id="ul_74FA98A82754469BA5FADCC63FC364F7"> 
          <li id="li_02940B712D6444A8B65C0A51834187E6"> <span class="uicontrol">FTP</span> <p>サイト検索/マーチャンダイジングサーバーはパッシブFTPを使用します。 </p> <p>ファイルを別のサーバーにプッシュするには、FTPしか使用できません。 </p> <p> <span class="uicontrol"> FTPサーバー </span> - FTPサーバーの名前を指定します。プロトコルや先行する「ftp://」は含めないでください。 </p> <p> <span class="uicontrol"> FTPユーザー名 </span> - FTPアカウント名を指定します。 </p> <p> <span class="uicontrol"> FTPパスワード </span> - FTPアカウントのパスワードを指定します。 </p> <p> <span class="uicontrol"> FTPファイル名 </span>  — 送信するファイルの名前を指定します。この名前は、フィードで複数のファイルが生成される場合にテンプレートとなります。通常、名前の末尾で拡張子の前に番号が増えます。 次に例を示します。basename.xml、basename1.xml、basename2.xml、...、basename-Nth.xml </p> <p> <span class="uicontrol"> FTPディレクトリ </span>  — 特定のディレクトリパスが必要な場合は、ここに入力します。パスにファイル名を含めないでください。 </p> </li> 
          <li id="li_EAE504436CD84452BA04BE51855A2BEF"> <span class="uicontrol"> ホストコンテンツネットワーク  </span> <p>コンテンツネットワークは、サイト検索/マーチャンダイジングのWebサーバーからファイルを提供する方法です。 フィードの受信者は、HTTPリクエストを使用してWebサーバーから取り込みます。 </p> <p> 
            <!--After the base filename is entered and the feed is successfully saved, the URL of the Content Network file is displayed on the Verification panel of the wizard. The URL becomes active after the feed is successfully processed. The vendor can get the feed data from this URL. Multiple files use the same URL path. However, be sure that you replace or change the filename according to the enumeration scheme. --> </p> </li> 
          </ul> </li> 
        </ul> <p>どちらのアップロード方法でも、Googleがサイトマップを取得する際に使用するURLを<span class="wintitle">メインサイトマップURL </span>フィールドに指定する必要があります。 サイトマップファイルの名前もここで決定します。 サイトマップが大きい場合は、複数のファイルが存在する可能性があり、ファイルの末尾にインデックス番号を付けるのが命名規則です（番号1から始まります）。 最初のファイルまたはインデックスファイルには、<span class="codeph"> sitemap.xml </span>、<span class="codeph"> sitemap1.xml </span>、<span class="codeph"> sitemap2.xml </span> ... <span class="codeph"> sitemap12.xml </span>のように、インデックスがありません。 </p> <p>アップロード方法として「<span class="uicontrol">ホストコンテンツネットワーク</span>」を選択した場合、ファイルのURLは同じファイル名になりますが、URLにはホストサービスのパスとホスト名が含まれます。 したがって、サイトマップのリクエストをホストされるコンテンツネットワークにリダイレクトします。 同じ場所からファイルを引き出すこともできます。 </p> <p>フィードファイルが作成されて中間の宛先に送信されると、Googleはpingされ、サイトマップフィードの準備ができたことを通知します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>5 </p> </td> 
      <td colname="col2"> <p>検証 </p> </td> 
      <td colname="col3"> <p><span class="wintitle">検証</span>パネルに移動すると、その時点でフィードが保存されます。 ただし、実際のフィードファイルは後で保存されます。 </p> <p><span class="wintitle">検証</span>パネルでは、次の操作を実行できます。 </p> 
        <ul id="ul_A1D889A84972419599FC83F39EA2676A"> 
        <li id="li_C8ED077B6DD1461E85A4914C1CFDBE88"> <span class="uicontrol"> データ表示  </span> <p>リンクをクリックして、表形式で表示されるデータ表示を通してフィードの出力を確認できます。 また、データ表示は、選択したメタフィールドと、ウィザードの<span class="wintitle">検索条件</span>パネルで指定した検索条件がフィードの出力にどのように影響するかを示すことで、トラブルシューティングに役立ちます。 データ表示は動的に生成されるので、いつでも使用できます。 </p> </li> 
        <li id="li_DACEE40703AF40EFBCD90D43825CE9C1"> <span class="uicontrol"> フィードファイル  </span> <p>フィードファイルが生成されたら、「<span class="uicontrol">フィードファイル</span>」ドロップダウンリストを使用して、サーバーからファイルを表示できます。 新しいブラウザータブまたは新しいブラウザーウィンドウが開き、フィードのコンテンツが表示されます。 この方法は、フォーマットの問題があるフィードのトラブルシューティングに役立ちます。 最終的な保存先やベンダー自身のファイルに表示を付けることはできません。 </p> <p> フィードが新しい場合は、フィードファイルを生成するまで、ドロップダウンリストは空になります。 </p> </li> 
        <li id="li_1C530354B4F34EC79D92CEFEB5B39ED7"> <span class="uicontrol"> コンテンツネットワークリンク  </span> <p>ウィザードの<span class="wintitle">ファイル送信</span>パネルで、アップロード方法として「<span class="uicontrol">ホストコンテンツネットワーク</span>」を選択した場合、URLはここに表示されます。 フィードファイルをまだ生成していない場合は、フィードが正常に生成されるまで、URLは無効です。 </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

1. ウィザードの手順を完了したら、**[!UICONTROL Close]**&#x200B;をクリックします。

## フィードの編集{#task_B855D28CD99B4FA58E2D4D4FD6DC9CEB}

既存のフィードの設定を編集できます。

<!-- 

t_editing_a_feed.xml

 -->

>[!NOTE]
>
>フィードを編集する場合、フィードのタイプを変更することはできません。 フィードのタイプを変更する必要がある場合は、既存のフィードを削除し、目的のタイプの新しいフィードを追加します。

「[フィードの削除](../c-about-settings-menu/c-about-searching-menu.md#task_7E39A140E69D43C6B61FB42E81051269)」を参照してください。

**フィードを編集するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Searching]**/**[!UICONTROL Feeds]**&#x200B;をクリックします。
1. 次のいずれかを実行します。

* [!DNL Feeds]ページの表の[!DNL Name]列の下で、フィード名の横のドロップダウンリストをクリックし、**[!UICONTROL Edit feed]**&#x200B;をクリックします。

* [!DNL Feeds]ページの[!DNL Name]列の下で、変更するフィードの名前をクリックします。

1. フィードのウィザードで、ウィザードの各パネルに必要なオプションを設定します。

   **フィードの追加**&#x200B;のオプションの表を参照してください。
1. ウィザードの最後の[!DNL Verification]パネルで、**[!UICONTROL Close]**&#x200B;をクリックします。

## フィードの削除{#task_7E39A140E69D43C6B61FB42E81051269}

不要になったフィードや使用していないフィードは削除できます。

<!-- 

t_deleting_a_feed.xml

 -->

**フィードを削除するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Searching]**/**[!UICONTROL Feeds]**&#x200B;をクリックします。
1. [!DNL Feeds Menu]画面の[!DNL Actions]列の下で、削除するフィード名の&#x200B;**[!UICONTROL Delete]**&#x200B;をクリックします。
1. [!DNL Delete feed]ダイアログボックスで、**[!UICONTROL Yes]**&#x200B;をクリックして削除を確定します。

## フィードファイルの表示{#task_1E413C7650DE466EA68925F72E086884}

フィードウィザードの最後のパネルに移動すると、フィードのデータ表示をすばやく表示したり、サーバーから現在のフィードファイルをダウンロードしたりできます。 この機能は、フィードの出力を検証および確認する場合に役立ちます。

<!-- 

t_viewing_feed_files.xml

 -->

**表示フィードファイルを作成するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Searching]**/**[!UICONTROL Feeds]**&#x200B;をクリックします。
1. [!DNL Feeds]ページの表の[!DNL Name]列の下で、フィード名の横のドロップダウンリストをクリックし、**[!UICONTROL View Feed Files]**&#x200B;をクリックします。
1. フィードのウィザードの[!DNL Verification]パネルで、**[!UICONTROL Show Data View]**&#x200B;をクリックします。
1. クリック **[!UICONTROL Close]**.

## ファイルのアップロードなしでのフィードのテスト{#task_F1F390F72E0A4886B6CD4CD86EDB4C8C}

最終的なアップロード先にファイルをアップロードせずに、フィードをテストできます。

<!-- 

t_testing_a_feed_with_no_file_upload.xml

 -->

**ファイルのアップロードなしでフィードをテストするには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Searching]**/**[!UICONTROL Feeds]**&#x200B;をクリックします。
1. [!DNL Feeds]ページの表の[!DNL Name]列の下で、フィード名の横のドロップダウンリストをクリックし、**[!UICONTROL Test Feed (No file upload)]**&#x200B;をクリックします。
1. [!DNL Feeds]ページの[!DNL Feed Status]列は、テスト中およびテスト後に更新されます。

## フィードの生成とアップロード{#task_C9A57827C7674035B62A22D310DDAA0C}

フィードウィザードの[!DNL File Submission]パネルで設定したスケジュールに関係なく、フィードファイルを手動で生成して最終宛先に送信できます。

<!-- 

t_generating_and_uploading_a_feed.xml

 -->

「[フィードの作成](../c-about-settings-menu/c-about-searching-menu.md#task_63179C1FC359497483CD6CE13FD1C250)」も参照してください。

**フィードを生成してアップロードするには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Searching]**/**[!UICONTROL Feeds]**&#x200B;をクリックします。
1. [!DNL Feeds]ページの表の[!DNL Name]列の下で、フィード名の横のドロップダウンリストをクリックし、**[!UICONTROL Generate and Upload Feed]**&#x200B;をクリックします。
1. [!DNL Feeds]ページでは、データフィードの生成およびアップロード中およびその後に[!DNL Feed Status]列が更新されます。
