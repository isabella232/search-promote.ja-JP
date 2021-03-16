---
description: ビジネスルールを使用して、検索をマーチャンダイジングできます。
solution: Target
title: ビジネス・ルールについて
topic: ルール，サイト検索とマーチャンダイジング
uuid: f2186f54-7a39-4f46-bb29-5115d5a17f07
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '3120'
ht-degree: 1%

---


# ビジネス・ルールについて{#about-business-rules}

ビジネスルールを使用して、検索をマーチャンダイジングできます。

## ビジネスルールの使用{#concept_2A93D76216754D3D8412CDEA00BD26BD}

例えば、バナーを表示するタイミングや、結果をどのような順序で表示するかを設定できます。 また、ファセット内の項目の位置、および特定の検索に使用するテンプレートを設定することもできます。 ルールは、定義された順に実行されます。ルールの注文番号が大きいほど、後でプロセス内で実行され、以前のルールが切り捨てられます。 ルールは、ドラッグ&amp;ドロップして順序を変更することも、「ルールの順序」テキストボックスに新しい番号を入力して順序を変更することもできます。

各ビジネスルールは、トリガーとアクションで構成されます。

トリガーは、ルールを実行するタイミングを定義します。 例えば、クエリ用語が「mens」の場合や、結果の大部分がhatsの場合です。 トリガーは複数の条件で構成され、これらの条件のすべてが真になるか、トリガー全体が真になるように条件のいずれかが真になる必要があります。 トリガー演算子を変更して、優先順位を指定できます。

アクションは、トリガー条件が満たされた場合の動作を定義します。 例えば、バナーを設定して、特定の結果を位置1に表示または移動します。 ルールの表には、ルールに関する概要情報が表示されます。 ルール名をクリックすると、そのルール名が開き、追加情報が表示されます。

ルールの表には、すべてのビジネスルールのリストが表示されます。 デフォルトでは、表には、追加された最近10個のルールが降順で表示されます。 テーブルの列ヘッダーをクリックして、ルールを昇順または降順で並べ替えることができます。

ビジネスルールは、次の3つの状態のいずれかを持つことができます。承認済、休止済またはWIP(Work In Progress)

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ビジネスルールの状態 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>承認済み </p> </td> 
   <td colname="col2"> <p>承認されたビジネスルールは、実稼働環境ーとステージングされた環境ーで実行されます。 ビジネスルールは、アドバンスルールビルダで承認します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>停止中 </p> </td> 
   <td colname="col2"> <p>停止されたビジネスルールは、ステージングされた環境ーや実稼働中の環境では実行されません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>仕掛品 </p> </td> 
   <td colname="col2"> <p>WIP(Work In Progress)は、承認も休止もされていないビジネス・ルールです。 つまり、まだ作業を続けている場合や、承認する前にテストを行う必要がある場合があります。 WIP状態のビジネスルールは、ステージングされた環境でのみ実行されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ビジネスルールを承認し、ライブ環境で実行できるようにライブにプッシュします。 現在、*すべての*&#x200B;ルールをライブにプッシュすることしかできません。 ただし、ルールのステータスを変更して、実稼働環境で実行するルールと実行しないルールを制御することができます。

デフォルトでは、関連するトリガーが満たされると必ずルールが実行されます。 ただし、特定の日時範囲に対してルールを実行するようにスケジュールすることもできます。

また、デフォルトでは、すべてのストアで関連付けられたトリガーが満たされると、ルールが実行されます。 ルールを特定のストアにのみ適用する場合は、ストアパネルを使用して、ルールを適用する1つ以上のストアを選択できます。

## 新しいビジネスルールの追加{#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7}

[!DNL Visual Rule Builder]または[!DNL Advanced Rule Builder]を使用して、顧客の検索エクスペリエンスをカスタマイズするビジネスルールを追加できます。

**新しいビジネスルールを追加するには**

次の手順は、Visual Rule Builderを使用していることを前提としています。

1. 次のいずれかを実行します。

   * 製品メニューで、**[!UICONTROL Rules]**/**[!UICONTROL Business Rules]**&#x200B;をクリックします。 [!DNL Business Rules]ページで、**[!UICONTROL Add New Rule]**&#x200B;をクリックします。

   * 製品メニューで&#x200B;**[!UICONTROL Simulator]**&#x200B;をクリックします。 **[!UICONTROL Simulator for Today]**&#x200B;ページで、**[!UICONTROL Options]**&#x200B;ドロップダウンメニューの右にある&#x200B;**[!UICONTROL Add New Rule]**&#x200B;をクリックします。

      **[!UICONTROL Add New Rule]**&#x200B;オプションがページに表示されない場合は、**[!UICONTROL Options]**&#x200B;ドロップダウンメニューで&#x200B;**[!UICONTROL Simulate Staged]**&#x200B;をクリックします。

      ![](assets/Simulator.png)

1. **[!UICONTROL Name]**&#x200B;テキストフィールドに、ビジネスルールの新しい名前を入力します。

   まだ&#x200B;**[!UICONTROL Save Rule]**&#x200B;をクリックしないでください。
1. （オプション）多数のビジネスルールを管理する場合は、ビジネスルールに特定のラベルを付けることができます。 **[!UICONTROL Tags]**&#x200B;フィールドに、1つ以上のタグラベルを入力します。カンマ、タブ、またはEnterを区切り文字として使用します。

   [!DNL Business Rules]ページで、**[!UICONTROL Filter by tag]**&#x200B;機能を使用して、指定したラベルに一致するルールをフィルターします。 1. [!DNL Business Rule Builder]ページで、使用するトリガーとアクションを設定します。

   **トリガーオプション**

   トリガーとは、ビジネスルールを実行するために満たす必要がある条件です。 ビジネスルールに複数のトリガーがある場合、次の3つの方法のいずれかを使用して、トリガーの応答方法を設定できます。

   * 次の例のように、すべてのトリガーがtrue（デフォルト設定）である必要がある応答です。

      `if a AND b AND c then ...`

   * 次の例のように、いずれかのトリガーがtrueである必要がある場合の応答です。

      `if a OR b OR c then ...`

   * トリガーのカスタムの組み合わせが指定された応答。 つまり、個々のトリガーまたは「条件」を`AND`演算子と`OR`演算子と組み合わせます。

      また、次の例のように、左括弧と右括弧の組み合わせを追加して、評価の優先順位を変更することもできます。

      `if (a OR b) AND c then ...`

      >[!NOTE]
      >
      >カスタムビジネスルールセットで`AND`演算子と`OR`演算子を組み合わせる場合は、トリガーが正しい順序で評価されるように、括弧を適切に指定してください。

      トリガーの組み合わせをカスタマイズできるというこの特徴は、デフォルトでは有効になっていません。 お使いの場合は、テクニカルサポートにこの機能を有効にするように依頼してください。
   <table> 
      <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>トリガーオプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>キーワードの一致 </p> </td> 
      <td colname="col2"> <p>トリガーは、検索語句が特定の大文字と小文字を区別するキーワードと一致する場合にtrueになります。 このトリガーは、言語学辞書で定義されている、キーワードとそのすべての同義語の両方に当てはまります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> クエリの一致 </p> </td> 
      <td colname="col2"> <p> トリガーは、すべての検索パラメータが一致する場合にtrueになります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> 結果グループが優先 </p> </td> 
      <td colname="col2"> <p> トリガーは、特定の検索で定義された結果のグループが結果セットより優先される場合にtrueです。 </p> <p>デフォルトでは、優先度は50%に設定されています。 この設定は、設定できるマーチャンダイジング設定です。 </p> <p> 
        <!--See <xref href="t_Configuring_Merchandising_preferences.xml#task_7AC7B9F5D9F44E10AB5BC0B8CB31C37A" type="task" format="dita" scope="local">Configuring Merchandising preferences</xref>. --> </p> <p>このトリガーが真になるには、グループ全体が結果セット内に存在する必要があります。 結果のグループは動的です。 インデックス操作の後、元の検索条件に一致する結果に応じて変化する場合があります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>結果グループが存在する </p> </td> 
      <td colname="col2"> <p> トリガーは、特定の検索で定義された結果のグループが結果セットに存在する場合にtrueになります。 このトリガーを満たすには、グループ全体が結果セット内に存在する必要があります（結果はどのページにも表示できます）。 結果のグループは動的で、元の検索条件に一致する結果に応じてインデックス操作後に変化する場合があります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> 結果の存在 </p> </td> 
      <td colname="col2"> <p> トリガーは、個々の結果が結果セット内で見つかった場合にtrueになります。 結果は結果セットのどこにでもかまいません。ユーザーが現在閲覧中のページにある必要はありません。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **アクションオプション**

   ビジネスルールのトリガーが満たされると、そのルールに関連付けられたアクションが実行されます。 Visual Rule Builderでは次のアクションを作成できますが、Advanced Rule Builderでは追加のタイプのアクションを作成できます。

   次の表に示す「ファセット項目を削除」、「ファセット項目を表示」、「ファセットを表示」、「ファセットを削除」、「ファセット項目をプッシュ」の各アクションには、ファセットが必要です。 ファセットを選択するためのインターフェイスは、アカウントの設定方法によって異なります。 例えば、通常のアカウントでは、ファセットの選択にドロップダウンリストを使用します。 ただし、アカウントにスロットファセットがある場合は、「オートコンプリート」テキストボックスが表示され、任意のファセットの名前を入力できます。 オートコンプリートは、ファセット名を入力すると、ドロップダウンリストのファセットを提示します。 提案には、現在定義されているファセットが含まれます。 アカウントにスロットマップがある場合は、スロットファセットも提示されます。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>アクションオプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>プッシュグループ </p> </td> 
      <td colname="col2"> <p> 指定した検索条件で定義された検索結果のグループを特定の位置にプッシュします。 </p> <p>検索結果のグループをプッシュしても、グループは暗黙的に追加されません。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>追加グループ </p> </td> 
      <td colname="col2"> <p> 指定し追加た検索条件で定義された検索結果のグループ。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>グループの削除 </p> </td> 
      <td colname="col2"> <p> 指定した検索条件で定義された検索結果のグループを削除します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>プッシュ（1つ） </p> </td> 
      <td colname="col2"> <p> 個々の検索結果を選択した位置にプッシュします。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>追加単一 </p> </td> 
      <td colname="col2"> <p> 選択した位置に個々の検索結果を追加します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>単一の削除 </p> </td> 
      <td colname="col2"> <p> 検索結果セットから個々の検索結果を削除します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>すべての結果を削除 </p> </td> 
      <td colname="col2"> <p>検索結果セットからすべての結果を削除します。 </p> <p> 
        <!-- Bug #3331637 The option is meant to be used in conjunction with other rule actions in order to create "canned landing pages" where we want to create a page's content solely by rule actions, and need to completely discard the "natural" results of the search. Given that the other options don't have any kind of "here's how/why you might use this", I don't see much point in breaking that precedent here.--> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>別のバナーを選択 </p> </td> 
      <td colname="col2"> <p> 選択したバナー領域のバナーを変更します。 </p> <p>このオプションは、Webページ表示領域のバナーを右クリックすると使用できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>追加バナーコマンド </p> </td> 
      <td colname="col2"> <p>AdobeのDynamic Mediaクラシックテンプレートにのみ適用されます。 </p> <p>バナーテンプレートで使用する初期設定のパラメーターを変更できます。 </p> <p><a scope="local" href="../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3" type="reference" format="dita">AdobeDynamic Mediaクラシック</a>を使用したバナーの追加のオプションの表を参照してください。 </p> <p>「AdobeDynamic Mediaクラシック</a>を使用したバナーの編集」も参照してください。<a href="../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9" type="task" format="dita" scope="local"> </a></p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>バナーの削除 </p> </td> 
      <td colname="col2"> <p> 選択したバナー領域からバナーを削除します。バナーを設定する別のルールがこのルールを上書きする場合を除き、バナーは表示されません。 </p> <p>このオプションは、Webページ表示領域のバナーを右クリックすると使用できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファセット項目をプッシュ </p> </td> 
      <td colname="col2"> <p> ファセット内の項目を選択した位置にプッシュします。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ゾーンの削除 </p> </td> 
      <td colname="col2"> <p> 検索結果ページからゾーンを削除します。 </p> <p>以下の「ファセットを削除」アクションも参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>領域を表示 </p> </td> 
      <td colname="col2"> <p> 検索結果ページにゾーンを表示します。 </p> <p>以下の「ファセットを表示」アクションも参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファセット項目の削除 </p> </td> 
      <td colname="col2"> <p> ファセット項目をファセットから削除します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファセット項目を表示アクションが </p> </td> 
      <td colname="col2"> <p> 特定のファセット項目を表示します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファセットを表示 </p> </td> 
      <td colname="col2"> <p> 特定のファセットを表示します。 この操作は、「Reveal Zone」操作よりも適しています。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファセットの削除 </p> </td> 
      <td colname="col2"> <p> 特定のファセットを削除します。 この操作は、「Remove Zone」操作よりも優先されます。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

   アクティブな（展開された）ルールビルダーパネルに応じて、次の操作を実行してトリガーとアクションを設定することもできます。

   * **[!UICONTROL Triggers]**&#x200B;パネルが展開されたら、[ビジネスルールビルダ]ページのプレゼンテーションテンプレート領域で、検索結果または検索ファセットを右クリックし、[**[!UICONTROL Add "result present" trigger]**]をクリックします。

      トリガーパネルで、トリガーの左側の「X」をクリックして、トリガーのリストから削除します。

   * **[!UICONTROL Actions]**&#x200B;パネルが展開されたとき — ビジネスルールビルダーページのプレゼンテーションテンプレート領域で、検索結果を右クリックします。 **[!UICONTROL Add Result]**、**[!UICONTROL Remove Result]**、**[!UICONTROL Push to bottom]**、または&#x200B;**[!UICONTROL Push to #`<n>`]**（`<n>`は数字）をクリックします。


1. （オプション）ビジネスルールビルダーパネル（[!DNL Triggers]、[!DNL Actions]、または[!DNL Schedule]）で、次のいずれかの操作を行います。

   * [ビジネスルールビルダ]ページ領域のプレゼンテーションテンプレート領域で、バナーを右クリックし、[**[!UICONTROL Select different banner]**]をクリックします。 **[!UICONTROL Pick Banner]**&#x200B;ページで、バナーサムネールの下の&#x200B;**[!UICONTROL Pick this banner]**&#x200B;をクリックして、それをプレゼンテーションテンプレートに追加します。 プレゼンテーションテンプレート上の元のバナーのサイズと領域に一致するバナーのみを選択できます。

      バナーを追加アクションが[!DNL Actions]パネルに追加されます。

   * [!DNL Business Rule Builder]ページのプレゼンテーションテンプレート領域で、パラメーターを変更するAdobeDynamic Mediaクラシックテンプレートのバナーを右クリックし、「**[!UICONTROL Add banner commands]**」をクリックします。 [!DNL Change Parameters]ダイアログボックスで、必要なパラメータオプションを設定します。

      [AdobeDynamic Mediaクラシックを使用したバナーの追加](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3)のオプションの表を参照してください。

      クリック **[!UICONTROL Save]**.

      パラメーターの変更が[!DNL Actions]パネルに追加されます。

      「AdobeDynamic Mediaクラシック](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9)を使用したバナーの編集」も参照してください。[

   * [ビジネスルールビルダ]ページのプレゼンテーションテンプレート領域で、ページから削除するバナーを右クリックし、[**[!UICONTROL Remove banner]**]をクリックします。 アクションパネルに「バナーを削除」アクションが追加されます。

1. （オプション）**[!UICONTROL Schedule]**&#x200B;パネルで、次のいずれかの操作を行います。

   * **[!UICONTROL Run Indefinitely]**&#x200B;をクリックすると、関連するトリガーが満たされるたびにルールが実行されます。 このオプションはデフォルトです。
   * **[!UICONTROL Fixed Schedule]**&#x200B;をクリックし、開始の日時と、ルールを実行する終了日時を、関連するトリガーに達したときに指定します。

1. クリック **[!UICONTROL Save Rule]**.
1. （オプション）[!DNL Business Rules]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## ビジネスルールの編集{#task_375CFA75D1D94D9E92A35DE1228E5087}

Visual Rule BuilderまたはAdvanced Rule Builderを使用して、追加したビジネスルールを編集できます。

**新しいビジネスルールを編集するには**

1. 製品メニューで、**[!UICONTROL Rules]**/**[!UICONTROL Business Rules]**&#x200B;をクリックします。
1. [!DNL Business Rules]ページで、次のいずれかの操作を行います。

   * [!DNL Name]列の下で、変更するビジネスルールの名前をクリックします。

      ビジネスルールは、**[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL My Preferences]**&#x200B;で指定されているデフォルトのインターフェイスで開きます。

   * ドロップダウンリストで、編集するビジネスルール名の横にある&#x200B;**[!UICONTROL Edit in advanced mode]**&#x200B;または&#x200B;**[!UICONTROL Edit in visual mode]**&#x200B;をクリックします。

1. [!DNL Name]テキストフィールドに、ビジネスルールの新しい名前を入力します。

   まだ&#x200B;**[!UICONTROL Save Rule]**&#x200B;をクリックしないでください。 1. [!DNL Business Rule Builder]ページで、使用するトリガーとアクションを設定します。

   「[新しいビジネスルールの追加](../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7)」のオプションの表を参照してください。
1. （オプション）任意の&#x200B;**[!UICONTROL Business Rule Builder]**&#x200B;パネル（[!DNL Triggers]、[!DNL Actions]、または[!DNL Schedule]）で、次のいずれかの操作を行います。

   * [!DNL Business Rule Builder]ページのプレゼンテーションテンプレート領域で、バナーを右クリックし、「**[!UICONTROL Select different banner]**」をクリックします。 [!DNL Pick Banner page]上で、バナーサムネールの下の&#x200B;**[!UICONTROL Pick this banner]**&#x200B;をクリックして、それをプレゼンテーションテンプレートに追加します。 プレゼンテーションテンプレート上の元のバナーのサイズと領域に一致するバナーのみを選択できます。

      バナーを追加アクションが[!DNL Actions]パネルに追加されます。

   * [!DNL Business Rule Builder]ページのプレゼンテーションテンプレート領域で、パラメーターを変更するAdobeDynamic Mediaクラシックテンプレートのバナーを右クリックし、「**[!UICONTROL Add banner commands]**」をクリックします。 [!DNL Change Parameters]ダイアログボックスで、必要なパラメータオプションを設定します。

      [AdobeDynamic Mediaクラシックを使用したバナーの追加](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3)のオプションの表を参照してください。

      クリック **[!UICONTROL Save]**.

      パラメーターの変更が[!DNL Actions]パネルに追加されます。

      「AdobeDynamic Mediaクラシック](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9)を使用したバナーの編集」も参照してください。[

   * [!DNL Business Rule Builder]ページのプレゼンテーションテンプレート領域で、ページから削除するバナーを右クリックし、「**[!UICONTROL Remove banner]**」をクリックします。 バナーの削除アクションが[!DNL Actions]パネルに追加されます。

1. （オプション）[!DNL Schedule]パネルで、次のいずれかの操作を行います。

   * **[!UICONTROL Run Indefinitely]**&#x200B;をクリックすると、関連するトリガーが満たされるたびにルールが実行されます。 このオプションはデフォルトです。
   * **[!UICONTROL Fixed Schedule]**&#x200B;をクリックし、開始の日時と、ルールを実行する終了日時を、関連するトリガーに達したときに指定します。

1. クリック **[!UICONTROL Save Rule]**.

   [!DNL Business Rule Builder]ページが閉じ、**[!UICONTROL Business Rule]**&#x200B;ページに戻ります。 ルールが表に表示されます。 **[!UICONTROL Modified]**&#x200B;列見出しをクリックして、編集日でルールを並べ替えます。 1.（オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## ビジネスルールのコピー{#task_89F1879C71A54EE9B7454439302C03EC}

既存のビジネスルールをコピーして、作成する新しいビジネスルールの基本として使用できます。

**ビジネス・ルールをコピーするには**

1. 製品メニューで、**[!UICONTROL Rules]**/**[!UICONTROL Business Rules]**&#x200B;をクリックします。
1. **[!UICONTROL Business Rules]**&#x200B;ページの、コピーするビジネスルール名の横にあるドロップダウンリストで、**[!UICONTROL Copy rule]**&#x200B;をクリックします。
1. コピーしたビジネスルールを通常どおり編集します。

   「[ビジネスルールの編集](../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087)」を参照してください。

## ビジネスルールの承認{#task_BD569D18BF664272B8692294C162E2C1}

ステータスがWIP(Work In Progress)または中断のビジネス・ルールをアクティブ化できます。

**ビジネスルールを承認するには**

1. 製品メニューで、**[!UICONTROL Rule]**/**[!UICONTROL Business Rules]**&#x200B;をクリックします。
1. [!DNL Business Rules]ページで、ビジネスルールテーブルの[!DNL Status]列のステータス列ヘッダーを使用して、ステータスが&#x200B;**[!UICONTROL WIP]**&#x200B;または&#x200B;**[!UICONTROL suspended]**&#x200B;のルールを並べ替えます。

   テーブルの左側のチェックボックス列のヘッダーを使用して、現在ページに表示されているすべてのルールを確認するか、ステータスが&#x200B;**[!UICONTROL WIP]**&#x200B;または&#x200B;**[!UICONTROL suspended]**&#x200B;のルールのみを確認します。 1.ページ上部付近のメニューバーで、「**[!UICONTROL Approve]**」をクリックします。
1. **[!UICONTROL Confirm Action]**&#x200B;ダイアログボックスで、**[!UICONTROL OK]**&#x200B;をクリックします。
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## ビジネスルール{#task_364E1FFB905141C08E306C8F1794A20E}を休止中

ステータスがWIP(Work In Progress)または承認済のビジネス・ルールを休止できます。

ルールを一時停止すると、一時的に非アクティブにし、別の時間そのルールに関する作業を保留していることがユーザーインターフェイスに表示されます。 ただし、中断されたルールを編集することはできます。

**ビジネスルールを中断するには**

1. 製品メニューで、**[!UICONTROL Rule]**/**[!UICONTROL Business Rules]**&#x200B;をクリックします。
1. [!DNL Business Rules]ページで、ビジネスルールテーブルの「ステータス」列のステータスを使用し、テーブルの最も左側の列で、ステータスが&#x200B;**[!UICONTROL WIP]**&#x200B;または&#x200B;**[!UICONTROL approved]**&#x200B;のルールを確認します。
1. ページ上部付近のメニューバーで、**[!UICONTROL Suspend]**&#x200B;をクリックします。
1. **[!UICONTROL Confirm Action]**&#x200B;ダイアログボックスで、**[!UICONTROL OK]**&#x200B;をクリックします。
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## ビジネスルールの再開{#task_E67D678C765B436EA2A3D6ADD7A49ABA}

ビジネスルールを再開して、中断されたルールを再アクティブ化できます。 ビジネス・ルールを再開すると、そのステータスは「WIP(Work In Progress)」に設定されます。

**ビジネスルールを再開するには**

1. 製品メニューで、**[!UICONTROL Rule]**/**[!UICONTROL Business Rules]**&#x200B;をクリックします。
1. [!DNL Business Rules]ページで、ビジネスルールテーブルの「ステータス」列のステータスを使用し、テーブルの最も左側の列で、ステータスが&#x200B;**[!UICONTROL suspended]**&#x200B;のルールを確認します。
1. ページ上部付近のメニューバーで、**[!UICONTROL Resume]**&#x200B;をクリックします。
1. [!DNL Confirm Action]ダイアログボックスで、**[!UICONTROL OK]**&#x200B;をクリックします。
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## ビジネスルールの実行順序の変更{#task_FE3B1C17307F49B49050C2EC5A063991}

ビジネスルールの順序を変更して、プレゼンテーションテンプレートで実行する順序を変更できます。

ビジネスルールは、定義された順に実行されます。ルールの注文番号が大きいほど、後でプロセス内で実行され、以前のルールが切り捨てられます。 ルールの順序を変更するには、[!DNL Business Rules]ページのテーブルの順序列に新しい番号を入力します。 ルールのドラッグ&amp;ドロップを使用して、ルールの実行順序を変更することもできます。

**ビジネスルールの実行順序を変更するには**

1. 製品メニューで、**[!UICONTROL Rule]**/**[!UICONTROL Business Rules]**&#x200B;をクリックします。
1. [!DNL Business Rules]ページの表で、次のいずれかの操作を行います。

   * **[!UICONTROL Order]**&#x200B;列ヘッダーをクリックして、ルールを昇順または降順に並べ替えます。
   * **[!UICONTROL Order]**&#x200B;列のビジネスルール名の左側にあるテキストフィールドに、ルールを実行する注文番号を入力します。
   * ルールを実行する位置にテーブル行をドラッグ&amp;ドロップします。 ルールが実行される新しい順序を反映するために、すべての注文番号が更新されます。

1. クリック **[!UICONTROL Save Changes]**.

   これで、ビジネスルールは指定した順序で実行されます。 リダイレクトビジネスルールが指定されている場合は例外です。 リダイレクトビジネスルールがトリガーまたはヒットされた場合、およびその時点で、ビジネスルールの処理が停止し、リダイレクトが許可されます。
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## ビジネスルール{#task_AE37B42412044541BCC6D46CF8793DFF}を削除しています

「バルクアクション」(Bulk Actions)ドロップダウンメニューを使用して、ステータスがWIP、休止、または承認のビジネスルールを削除できます。

**ビジネスルールを削除するには**

1. 製品メニューで、**[!UICONTROL Rules]**/**[!UICONTROL Business Rules]**&#x200B;をクリックします。
1. [!DNL Business Rules]ページで、次のいずれかの操作を行います。

   * チェックボックスの列見出しを使用して、ページに現在表示されているすべてのルールをチェックします。
   * 表の「ステータス」列のステータスに基づいて、削除するビジネスルールのみをチェックします。

1. [!DNL Bulk Actions]ドロップダウンリストで、**[!UICONTROL Delete]**&#x200B;をクリックします。
1. [!DNL Confirm Action]ダイアログボックスで、**[!UICONTROL OK]**&#x200B;をクリックします。
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。
