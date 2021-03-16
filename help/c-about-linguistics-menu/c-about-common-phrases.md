---
description: Webサイトで使用する共通フレーズを定義して、顧客が検索クエリを入力したときに、定義したフレーズを引用符で囲む必要がないようにすることができます。
solution: Target
title: 共通フレーズについて
topic: 言語、サイト検索、マーチャンダイジング
uuid: 0f980a22-d826-4476-97de-0e9c14549bc8
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 1%

---


# 共通フレーズについて{#about-common-phrases}

Webサイトで使用する共通フレーズを定義して、顧客が検索クエリを入力したときに、定義したフレーズを引用符で囲む必要がないようにすることができます。

## 共通フレーズの使用{#concept_4946E53586DF492EAEB1B7F757FD440F}

>[!NOTE]
>
>共通フレーズ機能は、デフォルトでは有効になっていないので、ユーザーインターフェイスに表示されません。 お使いの場合は、テクニカルサポートにこの機能を有効にするように依頼してください。

共通フレーズは、顧客の検索中に認識される複数語フレーズの集まりです。 この関数は、フレーズを個々の単語ではなく、組み合わされた単語のグループとして扱います。 顧客がWebサイト上で検索クエリを入力すると、「太平洋」などの重複を引用符で囲むことで語句を識別できます。 ただし、共通フレーズのグループを追加すると、検索クエリで一致フレーズが見つかった場合に、その顧客に対して自動的に引用符の使用手順が実行されます。

例えば、Webサイトの顧客が次の検索クエリを入力したとします。

`hotels near the pacific ocean`

`pacific ocean`の周りに引用符を追加しないと、顧客の検索結果は世界中の海の近くにあるホテルに対して返されますが、これは顧客の意図したものではありません。

ただし、「太平洋」という共通のフレーズを追加すると、検索クエリは自動的に次のように変換されます。

`hotels near the "pacific ocean"`

共通フレーズを使用すると、顧客が単語のフレーズを明示的に引用符で囲む必要がなくなります。その代わりに、これらの定義済みフレーズが検索クエリで見つかった場合に引用符が追加されるだけです。

この検索クエリの拡張は、バックエンド検索CGIパラメータ`sp_q`と`sp_q_#`に適用されます。

[バックエンド検索CGIパラメーター](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)の表行25、26、32を参照してください。

## 共通フレーズグループの追加{#task_35C84FABCD9042C5B48C5C788B752871}

共通フレーズグループを追加すると、検索クエリが入力した語句をすべて含むWebページを、正確に、その順序と近接性の両方で返すことができます。

共通フレーズグループを追加する際は、共通フレーズグループのメインページにある「検索」機能を使用できます。 「検索」機能を使用すると、既存のフレーズを検索し、そのフレーズが存在するグループを特定できます。

[特定の単語を含むフレーズ](../c-about-linguistics-menu/c-about-common-phrases.md#task_20714969274740A7BB4DC71E705EA15E)を参照してください。

**共通フレーズグループを追加するには**

1. 製品メニューで、**[!UICONTROL Linguistics]**/**[!UICONTROL Common Phrases]**&#x200B;をクリックします。
1. [!DNL Common Phrases Groups]ページで、「**フレーズグループ**」追加をクリックします。
1. [!DNL Add Common Phrase Group]ページで、必要なオプションを設定し、グループを構成するすべてのフレーズを追加します。

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
      <td colname="col2"> <p>必須。 </p> <p>共通フレーズグループの一意の名前。 </p> <p>後で共通フレーズグループを編集する場合は、グループ名を変更できないことに注意してください。 グループ名を変更するには、<span class="uicontrol">名前の変更</span>機能を使用します。 </p> <p>「<a href="../c-about-linguistics-menu/c-about-common-phrases.md#task_168E07C59C0F40989D43E7010EFF22EB" format="dita" scope="local">共通フレーズグループの名前の変更</a>」を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>メモ </p> </td> 
      <td colname="col2"> <p>オプション. </p> <p>共通フレ追加ーズグループに関連する情報です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フレーズ </p> </td> 
      <td colname="col2"> <p>必須。 </p> <p>最大5語までのフレーズを指定できます。 単語の最大値の設定を調整するには、テクニカルサポートにお問い合わせください。 </p> <p>入力する各フレーズは、共通フレーズグループ内で一意である必要があります。 </p> <p>「アクション」列のプラス(+)アイコンとマイナス(-)アイコンを使用して、入力したフレーズを追加したり、フレーズを削除したりします。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 「**追加**」をクリックします。
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 共通フレーズのテスト{#task_A0C344E051CA45A9A0588242F9DA675D}

フレーズグループに関連付けるメタデータフィールドを選択した場合は、特定のフレーズの拡張をテストできます。

フレーズの拡張をテストする場合は、フレーズグループに関連付けたメタデータフィールドに対して、完全に一致するフレーズを検索します。 この句は引用符で囲まれているかのように検索されます。 その他のメタデータフィールドでは、句内の語のみが検索され、引用符は使用されません。 例えば、`audi TT`というフレーズをテストしたとします。 返される結果は次のようになります。

`title|body|field3:"Audi TT" url|desc|keys|target|alt:Audi TT`

**共通のフレーズをテストするには**

1. 製品メニューで、**[!UICONTROL Linguistics]**/**[!UICONTROL Common Phrases]**&#x200B;をクリックします。
1. [!DNL Common Phrases Groups]ページの&#x200B;**「**&#x200B;を含むテストフレーズ」テキストフィールドに、メタデータの拡張をテストするフレーズを入力します。
1. クリック **[!UICONTROL Test]**.

   拡張の結果がテキストボックスに表示されます。
1. （オプション）テキストボックスの右下隅をドラッグして、表示領域を展開します。

## フレーズ{#task_20714969274740A7BB4DC71E705EA15E}内の特定の単語を含む検索グループ

[!DNL Find]を使用すると、追加した既存のグループの中から特定の語句を検索できます。

「検索」を使用すると、次の場所が検出されます。

* 全てのグループの中から完全に同じフレーズが見つかる
* フレーズ内の語順や近接性に関係なく、すべてのグループの間でそのフレーズ内の任意の単語。

「[共通フレーズグループの編集](../c-about-linguistics-menu/c-about-common-phrases.md#task_5CAC3A133C5342EEAFE55A7EABCBCD61)」も参照してください。

**特定の単語を含むグループを検索するには**

1. 製品メニューで、**[!UICONTROL Linguistics]**/**[!UICONTROL Common Phrases]**&#x200B;をクリックします。
1. [!DNL Common Phrases Groups]ページの&#x200B;**[!UICONTROL Find groups with phrases that contain]**&#x200B;テキストフィールドに、フレーズを入力します。
1. クリック **[!UICONTROL Find]**.

   結果がテキストボックスに表示されます。
1. （オプション）次の操作を1つ以上行います。

   * テキストボックスの右下隅をドラッグして、表示領域を展開します。
   * 結果ウィンドウで、ハイパーリンク付きのフレーズをクリックして、関連付けられたグループの共通フレーズグループを編集ページを開きます。

## 共通フレーズグループの編集{#task_5CAC3A133C5342EEAFE55A7EABCBCD61}

追加した共通フレーズグループの既存のフィールド、メモ、フレーズを編集できます。 ただし、グループ名を編集するには[!DNL Rename]機能を使用する必要があります。

「[共通フレーズグループの名前の変更](../c-about-linguistics-menu/c-about-common-phrases.md#task_168E07C59C0F40989D43E7010EFF22EB)」も参照してください。

**共通フレーズグループを編集するには**

1. 製品メニューで、**[!UICONTROL Linguistics]**/**[!UICONTROL Common Phrases]**&#x200B;をクリックします。
1. [!DNL Common Phrases Groups]ページで、グループ名の一番右にある&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。
1. [!DNL Edit Common Phrase Group]ページで、必要なオプションを設定します。

   [共通フレーズグループの追加](../c-about-linguistics-menu/c-about-common-phrases.md#task_35C84FABCD9042C5B48C5C788B752871)のオプションの表を参照してください。
1. 「**変更を保存**」をクリックします。
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 共通フレーズグループの名前変更{#task_168E07C59C0F40989D43E7010EFF22EB}

既存の共通フレーズグループの名前を変更できます。 ただし、共通フレーズグループの既存のフィールド、メモ、フレーズを変更する場合は、[!DNL Edit]機能を使用する必要があります。

「[共通フレーズグループの編集](../c-about-linguistics-menu/c-about-common-phrases.md#task_5CAC3A133C5342EEAFE55A7EABCBCD61)」を参照してください。

**共通フレーズグループの名前を変更するには**

1. 製品メニューで、**[!UICONTROL Linguistics]**/**[!UICONTROL Common Phrases]**&#x200B;をクリックします。
1. [!DNL Common Phrases Groups]ページで、グループ名の一番右にある&#x200B;**[!UICONTROL Rename]**&#x200B;をクリックします。
1. [!DNL Rename Common Phrase Group]ページの&#x200B;**[!UICONTROL Group Name]**&#x200B;テキストフィールドに、グループの新しい名前を入力します。
1. 「**名前を変更**」をクリックします。
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 共通フレーズグループの削除{#task_4106D282A2ED4A27B09EE5A8CAAEDA36}

追加した共通フレーズグループは削除できます。 誤ってグループを削除した場合は、[!DNL History]を使用してグループを復元できます。

[「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

**共通フレーズグループを削除するには**

1. 製品メニューで、**[!UICONTROL Linguistics]**/**[!UICONTROL Common Phrases]**&#x200B;をクリックします。
1. [!DNL Common Phrases Groups]ページで、グループ名の一番右にある&#x200B;**[!UICONTROL Delete]**&#x200B;をクリックします。
1. [!DNL Delete Common Phrase Group]ページで、**[!UICONTROL Delete]**&#x200B;をクリックします。
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

