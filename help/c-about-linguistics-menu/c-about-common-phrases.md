---
description: 顧客が検索クエリを入力したときに、定義したフレーズを引用符で囲む必要がないように、Webサイトで使用する共通フレーズを定義できます。
seo-description: 顧客が検索クエリを入力したときに、定義したフレーズを引用符で囲む必要がないように、Webサイトで使用する共通フレーズを定義できます。
seo-title: 共通フレーズについて
solution: Target
title: 共通フレーズについて
topic: Linguistics,Site search and merchandising
uuid: 0f980a22-d826-4476-97de-0e9c14549bc8
translation-type: tm+mt
source-git-commit: 8efa90ac2927b263b7d48ccbf25d4b0e917dac79

---


# 共通フレーズについて{#about-common-phrases}

顧客が検索クエリを入力したときに、定義したフレーズを引用符で囲む必要がないように、Webサイトで使用する共通フレーズを定義できます。

## 共通フレーズの使用 {#concept_4946E53586DF492EAEB1B7F757FD440F}

>[!NOTE]
>
>共通フレーズ機能は、デフォルトでは有効になっていないので、ユーザーインターフェイスに表示されません。 お使いの機能を有効にするには、テクニカルサポートにお問い合わせください。

共通フレーズは、顧客の検索中に認識される複数語のフレーズの集まりです。 個々の単語ではなく、複数の単語を組み合わせたグループとして扱います。 顧客がWebサイトで検索クエリを入力すると、「太平洋」などの二重引用符で囲んでフレーズを識別できます。 ただし、共通フレーズのグループを追加すると、検索クエリで一致するフレーズが見つかると、その顧客に対して引用符のステップが自動的に実行されます。

例えば、Webサイトの顧客が次の検索クエリを入力したとします。

`hotels near the pacific ocean`

顧客の検索結果は、引用符を付 `pacific ocean`加しない限り、世界中の海の近くにあるホテルの検索結果を返します。これは、顧客が意図したものではありません。

ただし、共通のフレーズ「太平洋」を追加すると、検索クエリは自動的に次に変換されます。

`hotels near the "pacific ocean"`

共通フレーズを使用すると、顧客が単語のフレーズを引用符で囲んで明示的に使用する必要がなくなります。その代わりに、定義されたフレーズが検索クエリで見つかった場合に、単に引用符が追加されます。

この検索クエリの拡張は、バックエンド検索CGIパラメータおよび `sp_q``sp_q_#`、

バックエンド検索CGIパラメーターの表行25、26、32 [を参照してください](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)。

## 共通フレーズグループの追加 {#task_35C84FABCD9042C5B48C5C788B752871}

「共通フレーズグループ」を追加すると、検索クエリが、顧客が入力した語句のすべてを正確な順序と近接性で含むWebページを正確に返すことができます。

共通フレーズグループを追加する際に、メインの共通フレーズグループページの「検索」機能を使用できます。 「検索」機能を使用すると、既存のフレーズを検索し、そのフレーズが存在するグループを検索できます。

詳しくは、 [特定の単語を含むグループの検索を参照してくださ](../c-about-linguistics-menu/c-about-common-phrases.md#task_20714969274740A7BB4DC71E705EA15E)い。

**共通フレーズグループを追加するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Linguistics]** クしま **[!UICONTROL Common Phrases]**&#x200B;す。
1. ページで、「フレ [!DNL Common Phrases Groups] ーズグループを追 **加」をクリックします**。
1. ページ [!DNL Add Common Phrase Group] で、必要なオプションを設定し、グループを構成するすべてのフレーズを追加します。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>グループ名 </p> </td> 
      <td colname="col2"> <p>必須。 </p> <p>共通フレーズグループの一意の名前。 </p> <p>後で共通フレーズグループを編集する場合は、グループ名を変更できないことに注意してください。 グループ名を変更するには、「名前の変更」機能を使 <span class="uicontrol"> 用し</span> ます。 </p> <p>「共通フレ <a href="../c-about-linguistics-menu/c-about-common-phrases.md#task_168E07C59C0F40989D43E7010EFF22EB" format="dita" scope="local"> ーズグループの名前の変更」を参照してくださ</a>い。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>メモ </p> </td> 
      <td colname="col2"> <p>オプション. </p> <p>共通フレーズグループに関連する情報を追加します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フレーズ </p> </td> 
      <td colname="col2"> <p>必須。 </p> <p>最大5語までのフレーズを指定できます。 最大単語数の設定を調整するには、テクニカルサポートにお問い合わせください。 </p> <p>入力する各フレーズは、任意の共通フレーズグループ内で一意である必要があります。 </p> <p>「アクション」列のプラス(+)アイコンとマイナス(-)アイコンを使用して、入力したフレーズを追加したり、フレーズを削除したりします。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 「**追加**」をクリックします。
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 共通フレーズのテスト {#task_A0C344E051CA45A9A0588242F9DA675D}

フレーズグループに関連付けるメタデータフィールドを選択した場合は、特定のフレーズの拡張をテストできます。

フレーズの拡張をテストする場合は、フレーズグループに関連付けたメタデータフィールドに対して、完全なフレーズを検索します。 この句は引用符で囲まれているかのように検索されます。 その他のメタデータフィールドでは、句内の単語のみが検索され、引用符は検索されません。 例えば、フレーズをテストしたとしま `audi TT`す。 返される結果は次のようになります。

`title|body|field3:"Audi TT" url|desc|keys|target|alt:Audi TT`

**共通のフレーズをテストするには**

1. 製品メニューで、/をクリッ **[!UICONTROL Linguistics]** クしま **[!UICONTROL Common Phrases]**&#x200B;す。
1. ページの [!DNL Common Phrases Groups] 「次を含むテ **キストフレーズ** 」テキストフィールドに、メタデータの拡張をテストするフレーズを入力します。
1. クリック **[!UICONTROL Test]**.

   展開結果がテキストボックスに表示されます。
1. （オプション）テキストボックスの右下隅をドラッグして、表示領域を展開します。

## 特定の語句を含むグループの検索 {#task_20714969274740A7BB4DC71E705EA15E}

を使用して、追 [!DNL Find] 加した既存のすべてのグループの中から特定のフレーズ内の単語を検索できます。

「検索」を使用すると、次の場所が検索されます。

* 全てのグループの中で完全に同じフレーズが見つかる場所。
* フレーズ内の語順や近接性に関係なく、すべてのグループ間でフレーズ内の任意の単語。

「共通フレーズ [グループの編集」も参照してくださ](../c-about-linguistics-menu/c-about-common-phrases.md#task_5CAC3A133C5342EEAFE55A7EABCBCD61)い。

**フレーズ内の特定の単語を含むグループを検索するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Linguistics]** クしま **[!UICONTROL Common Phrases]**&#x200B;す。
1. ページの [!DNL Common Phrases Groups] テキストフィー **[!UICONTROL Find groups with phrases that contain]** ルドにフレーズを入力します。
1. クリック **[!UICONTROL Find]**.

   結果がテキストボックスに表示されます。
1. （オプション）次の1つ以上の操作を行います。

   * テキストボックスの右下隅をドラッグして、表示領域を拡大します。
   * 結果ウィンドウで、ハイパーリンクされたフレーズをクリックして、関連付けられたグループの共通フレーズグループの編集ページを開きます。

## 共通フレーズグループの編集 {#task_5CAC3A133C5342EEAFE55A7EABCBCD61}

追加した共通フレーズグループの既存のフィールド、メモ、フレーズを編集できます。 ただし、グループ名を編集するには、この機能を使用する必要があ [!DNL Rename] ります。

「共通フレーズ [グループの名前の変更」も参照してくださ](../c-about-linguistics-menu/c-about-common-phrases.md#task_168E07C59C0F40989D43E7010EFF22EB)い。

**共通フレーズグループを編集するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Linguistics]** クしま **[!UICONTROL Common Phrases]**&#x200B;す。
1. ページ [!DNL Common Phrases Groups] 上で、グループ名 **[!UICONTROL Edit]** の一番右にあるをクリックします。
1. ページ [!DNL Edit Common Phrase Group] で、必要なオプションを設定します。

   共通フレーズグループの追加のオ [プションの表を参照してください](../c-about-linguistics-menu/c-about-common-phrases.md#task_35C84FABCD9042C5B48C5C788B752871)。
1. 「**変更を保存**」をクリックします。
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 共通フレーズグループの名前の変更 {#task_168E07C59C0F40989D43E7010EFF22EB}

既存の共通フレーズグループの名前を変更できます。 ただし、共通のフレーズグループの既存のフィールド、メモ、フレーズを変更する場合は、この機能を使用する必要があ [!DNL Edit] ります。

「共通フ [レーズグループの編集」を参照してください](../c-about-linguistics-menu/c-about-common-phrases.md#task_5CAC3A133C5342EEAFE55A7EABCBCD61) 。

**共通フレーズグループの名前を変更するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Linguistics]** クしま **[!UICONTROL Common Phrases]**&#x200B;す。
1. ページ [!DNL Common Phrases Groups] 上で、グループ名 **[!UICONTROL Rename]** の一番右にあるをクリックします。
1. ページの [!DNL Rename Common Phrase Group] テキストフィー **[!UICONTROL Group Name]** ルドに、グループの新しい名前を入力します。
1. 「名前の変更」 **をクリックしま**&#x200B;す。
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 共通フレーズグループの削除 {#task_4106D282A2ED4A27B09EE5A8CAAEDA36}

追加した共通フレーズグループは削除できます。 誤ってグループを削除した場合は、を使用してグループを復 [!DNL History] 元することができます。

詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

**共通フレーズグループを削除するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Linguistics]** クしま **[!UICONTROL Common Phrases]**&#x200B;す。
1. ページ [!DNL Common Phrases Groups] 上で、グループ名 **[!UICONTROL Delete]** の一番右にあるをクリックします。
1. ページ上で、 [!DNL Delete Common Phrase Group] をクリックしま **[!UICONTROL Delete]**&#x200B;す。
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

