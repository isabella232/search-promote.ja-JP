---
description: バナーを使用して、Webサイト上のバナー広告を管理できます。
seo-description: バナーを使用して、Webサイト上のバナー広告を管理できます。
seo-title: バナーについて
solution: Target
title: バナーについて
topic: Design,Site search and merchandising
uuid: 653b567d-5cf3-41a0-a260-a6912d0fd20d
translation-type: tm+mt
source-git-commit: 7f1b5d94e8002992d62ec1e3dce11f9c5605fde8

---


# バナーについて {#about-banners}

バナーを使用して、Webサイト上のバナー広告を管理できます。

## バナーの使用 {#concept_5BBE01FEC6134393B43CC917C8CC64DA}

<!-- 

c_about_banners.xml

 -->

Webサイトにバナー広告を追加する方法は2つあります。

1つ目の方法は、Target、Search&amp;Promoteを使用してバナーを追加する方法です。 バナーは、顧客がWebサイトを検索したときに表示されるHTMLコードスニペットです。 バナーには、GIF、JPEG、PNG形式のテキストや画像、またはその両方を含めることができます。 プリセットサイズから選択するか、ページに合わせて独自のカスタムサイズを定義できます。 バナーの表示に使用するHTMLコードは、使用するフォントスタイルや境界線などを指定することもできます。 このバナーの追加方法は、基本的な機能を提供し、追加のソフトウェアは必要ありません。

2つ目の方法は、Dynamic Media ManagementおよびPublishing ServiceであるAdobe Dynamic Media Classicを使用する方法です。 有効なAdobe Dynamic Media Classicアカウントを使用すると、Dynamic Media Classicを使用して、バナーコンテンツを直接Target、Search&amp;Promoteに管理および配信できます。 サイト検索/マーチャンダイジングでは、Dynamic Media Classicアカウントへのアクセスを設定します。 次に、ダイナミックメディアクラシックメディアブラウザを開き、バナーとして使用するダイナミックメディアアセットを選択します。

>[!NOTE]
>
>サイト検索/マーチャンダイジングでダイナミックメディアアセットをバナーとして使用する前に、アセットは最初にアップロードされ、Scene7 Publishing Systemで公開する準備が整います。 サイト検索/マーチャンダイジング内からアセットをアップロードし、Scene7 Publishing Systemで公開する準備を自動的に行うことができます。 また、Scene7 Publishing System内からアセットをすべてアップロードして公開することもできます。

## バナーとAdobe Scene7 Publishing Systemの統合 {#section_D4D7ADEA6A6348E68EDA138E184FE579}

画像、ダイナミックバナー、画像テンプレートやFlashテンプレートなどのテンプレートを含む、サイト検索/マーチャンダイジングのバナーとして、Dynamic Media Classicのアセットタイプを使用できます。

テンプレートは、Adobe Photoshop®などの画像編集アプリケーションのレイヤーファイルのような、動的に作成され、アドレス指定可能なレイヤー画像ファイルです。 静的な画像ファイルとは異なり、テンプレートにはパラメータを含めることができます。 パラメータを使用して、可変の画像プロパティと画像コンテンツをカスタマイズできます。

>[!NOTE]
>
>また、Scene7 Publishing Systemの印刷テンプレートを使用して、レイアウトベースのデザインからテンプレートを作成したり、Adobe IllustratorおよびAdobe InDesignのファイルを作成したりすることもできます。

『ダイナミ [ックメディア](https://help.adobe.com/en_US/scene7/using/WSFBFBAD30-2694-4b18-B7CE-894F9FC5CDDF.html) (Scene7)ユーザガイド』の「印刷テンプレート」を参照してください。

テンプレートには、任意の数の画像レイヤーとテキストレイヤーを含めることができます。 レイヤーPSDファイルなど、レイヤーを含む静的ファイルをテンプレートに変換したり、Dynamic Media Classicでテンプレートを作成したりできます。 Scene7 Publishing Systemにアップロードしたフォントを使用して、テンプレート内にテキストレイヤーを作成できます。 テンプレートにテキストを追加した後、テキストの位置揃え、フォント、フォントサイズ、色を変更して、書式を設定できます。

ダイナミックメディアクラシックのパラメータ画面を使用して、テンプレートの任意の要素をアドレス指定可能なパラメータに変換できます。 この場合、使用するレイヤー画像や、テンプレートで使用するテキスト値を変更できます。 パラメータはURL文字列と共に渡され、パラメータを変更してImage Serverから生成される返信画像を動的にカスタマイズできます。

ダイナミックメディアクラシックを使用してテンプレートを作成し、レイヤー上のプロパティをパラメータ化して、バナーで使用する方法について詳しく説明します。

『ダイナ [ミックメディア](https://help.adobe.com/en_US/scene7/using/WS60B68844-9054-4099-BF69-3DC998A04D3C.html) (Scene7)ユーザガイド』の基本テンプレートを参照してください。

**アセットのアップロードと公開**

アセットをサイト検索/マーチャンダイジングのバナーに使用するには、アセットをダイナミックメディアクラシックでアップロードおよび公開する必要があります。 この前提条件には、画像テンプレートまたはFlashテンプレートで使用されるアセットも含まれます。 デジタルアセットのアップロードと公開には、Dynamic Media Classicアカウントを使用します。 または、サイト検索/マーチャンダイジングを使用してデジタルアセットをアップロードし、アップロードの設定に基づいてDynamic Media Classicで自動的に公開することもできます。 まだアップロードおよび公開されていないアセットを選択しようとすると、ユーザーインターフェイスで通知され、アップロードのオプションが与えられた後で続行します。

Scene7 Publishing Systemを使用したデジタルアセットのアップロードと公開について詳しく説明します。

詳しくは [、『Dynamic Media Classic](https://help.adobe.com/en_US/scene7/using/WS3673AD39-098B-4f08-8A24-CA51261B7366.html) (Scene7)ユーザガイド』の「アセットのアップロードと公開」を参照してください。

>[!NOTE]
>
>ダイナミックメディアクラシックアセットビューアでアップロード機能を使用するには、使用するダイナミックメディアクラシックアカウントに「SPS会社管理者」という役割が既に設定されていることを確認します。

『ダイナ [ミック](https://help.adobe.com/en_US/scene7/using/WS662101DF-D697-47a7-A7D8-B52FD8E94438.html) ・メディアクラシック(Scene7)ユーザガイド』の「管理設定」を参照してください。

**ビジネス・ルールを使用したバナー内のダイナミック・メディア・クラシック・テンプレート・パラメータの変更**

Dynamic Media Classicのアセットをバナーとして追加した場合は、を使用して、Webサイ [!DNL Visual Rule Builder] トのバ [!DNL Business Rules] ナー領域にそのアセットを追加できます。 例えば、他のバナーと同様に、バナーを検索結果ページに追加します。 また、ダイナミックメディアクラシックテンプレートを特定のニーズに合わせてカスタマイズすることで、その初期設定のパラメータ値を上書きすることもできます。 この種の機能を使用すると、異なるマーケティングメッセージや異なるエンドポイントへのハイパーリンクを使用して、ダイナミックメディアクラシックテンプレートをカスタマイズできます。

「新しいビジネ [スルールの追加」も参照してくださ](../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7)い。

「ビジネスル [ールの編集」も参照してください](../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087)。

## バナーの追加 {#task_549D02B5F73B4158B105A94E39D937B7}

を使用して、 [!DNL Banners] バナー広告とWebサイト上の配置場所を管理できます。 バナーを追加する場合は、検索時に表示されるHTMLコードスニペットを使用して画像を外部参照します。

<!-- 

t_adding_a_new_banner.xml

 -->

有効なAdobe Dynamic Media Classicアカウントをお持ちの場合は、Scene7 Publishing Systemを使用してバナー広告を追加できます。

Adobe Dynamic Media Classic [を使用したバナーの追加を参照してください](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3)。

詳しくは、 [Adobe Dynamic Media Classicアカウントへのアクセスの設定を参照してください](../c-about-settings-menu/c-about-account-options-menu.md#task_CEFF88C2033D41D0B2FE86C435EDAC6D)。

**バナーを追加するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Design]** クしま **[!UICONTROL Banners]**&#x200B;す。
1. ページ [!DNL Banners] のドロップダウンリ **[!UICONTROL Add Banner]** ストで、を選択します **[!UICONTROL HTML code]**。
1. ダイアログ [!DNL Add Banner] ボックスで、必要なオプションを設定します。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>名前 </p> </td> 
      <td colname="col2"> <p>必須。バナーの名前を指定します。 名前は、Business RulesのVisual Rule Builderでバナーを追加する際に、バナーを参照するために使用されます。 名前はバナー自体には表示されません。 </p> <p>新しいビジ <a href="../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7" type="task" format="dita" scope="local"> ネスルールの追加を参照してください。</a> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>バナーHTML </p> </td> 
      <td colname="col2"> <p> バナーに関連付けられたHTMLコードを貼り付けます。 </p> <p>HTMLコードは、 
        <userinput>
          &lt;style&gt; 
        </userinput> タグ、または 
        <userinput>
          &lt;script&gt; 
        </userinput> タグを使用します。例えば、次のコードブロックは、横置きの上端タイプのテキストバナー用です。次の例 <code> &lt;div&nbsp;style="width:&nbsp;684px;&nbsp;background-image:&nbsp;url('https://www.brough.com/blackb.gif');&nbsp; 
          padding-top:&nbsp;10px;&nbsp;padding-bottom:&nbsp;10px;&nbsp;color:&nbsp;white;&nbsp;font-family:&nbsp;verdana;&nbsp; 
          text-align:&nbsp;center;&nbsp;font-size:&nbsp;20px;"&gt;&nbsp;Sound&nbsp;Study&nbsp;ships&nbsp;free!&nbsp;&lt;/div&gt; </code>では、コードのブロックはフルスプラッシュ画像用です。 <code> &lt;img&amp;nbsp;src='https://geometrixx.com/images/GEOAds/geometrixx-beauty-home-01.jpg'&amp;nbsp;border="0"&amp;nbsp;/&gt; </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>タイプ </p> </td> 
      <td colname="col2"> <p>次の種類のバナーを指定します。 
        <ul id="ul_6423AEDB9E664049989EB529D63C4A62"> 
          <li id="li_BF6CD60B3ED748D49CFFB9C5D607661C"> <span class="uicontrol"> [新しいタイプ] </span> <p>サイズや名前など、必要なバナーの種類を指定できます。 </p> </li> 
          <li id="li_1A29AB22AD644E60A12298187B5E898E"> <span class="uicontrol"> フルスプラッシュ </span> <p>このタイプのバナーの設定寸法は、幅が680ピクセル、高さが650ピクセルです。 オプションで、タイプの名前を指定するか、バナータイプ自体の名前であるデフォルトの名前を受け入れることができます。 </p> </li> 
          <li id="li_2BE06D013CB54DDE851051BFC038BB57"> <span class="uicontrol"> 水平上 </span> <p> バナーは、Webサイトの上部に配置されます。 このタイプは、バナーの左または右にハイパーリンクを追加する場合に便利です。 このタイプのバナーの設定寸法は、幅が468ピクセル、高さが60ピクセルです。 オプションで、タイプの名前を指定するか、バナータイプ自体の名前であるデフォルトの名前を受け入れることができます。 </p> </li> 
          <li id="li_EC35AB92234749F08AA8A9BD26D0EA8D"> <span class="uicontrol"> 水平上 — 全幅 </span> <p>このタイプは、新しいバナーを追加するときのデフォルトです。 バナーはWebサイトの上部に配置され、ページの幅いっぱいに表示されます。 このタイプのバナーの設定寸法は、幅が670ピクセル、高さが150ピクセルです。 オプションで、タイプの名前を指定するか、バナータイプ自体の名前であるデフォルトの名前を受け入れることができます。 </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>タグ </p> </td> 
      <td colname="col2"> <p>バナーに関連付けるタグまたは「キーワード」を追加します。 多くのバナーを使用する場合、タグを追加すると、バナーの検索を絞り込むのに役立ち、必要に応じて適切なバナーをすばやく見つけることができます。 追加したタグを削除することもできます。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Save]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## バナーの編集 {#task_D4081083BE7B40F5A003D1A2F1435AEA}

バナー [!DNL Edit Banner] 名、バナーのHTML、バナーのタイプ、関連するタグなどを変更する場合に使用します。

<!-- 

t_editing_a_banner.xml

 -->

サイト検索/マーチャンダイジングを使用してバナーを追加した場合は、Adobe Dynamic Media Classicを使用してバナーを編集することもできます。

Adobe Dynamic Media Classicを使 [用したバナーの編集も参照してください](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9)。

**バナーを編集するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Design]** クしま **[!UICONTROL Banners]**&#x200B;す。
1. ページ上で、 [!DNL Banners] をクリックしま ![](assets/icon_edit_16.gif)す。

   編集するバナーサムネールの上に表示します。
1. ページ [!DNL Edit Banner] で、必要なオプションを設定します。

   バナーの追加のオプションの表を参 [照してください](../c-about-design-menu/c-about-banners.md#task_549D02B5F73B4158B105A94E39D937B7)。
1. バナーの編集が終了したら、をクリックしま **[!UICONTROL Save]**&#x200B;す。
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## Adobe Dynamic Media Classicを使用したバナーの追加 {#task_AD1E0C00A9E04B1FA819EB93288786B3}

を使用して、Webサ [!DNL Banners] イト上のバナー広告を管理できます。 Adobe Dynamic Media Classicを使用してバナーを追加する場合、Scene7 Publishing Systemにアップロードした任意のデジタルアセットから選択できます。

<!-- 

t_adding_a_banner_using_adobe_scene7.xml

 -->

Adobe Dynamic Media Classicを使用してバナーを追加するには、有効なDynamic Media Classicアカウントへのアクセス権が設定されていることを確認してください。

詳しくは、 [Adobe Dynamic Media Classicアカウントへのアクセスの設定を参照してください](../c-about-settings-menu/c-about-account-options-menu.md#task_CEFF88C2033D41D0B2FE86C435EDAC6D)。

**Adobe Dynamic Media Classicを使用してバナーを追加するには**

1. 製品メニューで、/をクリックしま **[!UICONTROL Design]** す。 **[!UICONTROL Banners.]**
1. ページ [!DNL Banners] のドロップダウンリ **[!UICONTROL Add Banner]** ストで、をクリックします **[!UICONTROL Adobe Scene7]**。
1. ダイアログボ [!DNL Pick an Asset] ックスの左ペインで、ユーザーインターフェイスのナビゲーションオプションを使用して、バナーに使用するデジタルアセットが含まれるフォルダーを探します。

   アセットナビゲーションオプションを除き、その他のすべてのオプションは、追加または編集するために選択したデジタルアセットに依存します。

   サイト検索/マーチャンダイジングで新しいバナーに使用するアセットを見つけるには、アセットのナビゲーションオプションを使用します。 ナビゲーションオプションは、選択したすべての種類のデジタルアセットに適用されます。

   >[!NOTE]
   >
   >ダイアログボックスでバナーを編集すると、アセットのナビゲーションオプションは表 [!DNL Change Parameters] 示されません。

   詳しくは、 [Adobe Dynamic Media Classicを使用したバナーの編集を参照してください](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9)。

   **アセットナビゲーションオプション**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>ナビゲーションオプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/S7_folders.png"> </p> </td> 
      <td colname="col2"> <p>特定の会社のDynamic Media Classicアカウントをドロップダウンリストから選択し、そのアカウント内のデジタルアセットフォルダーに移動できます。 </p> <p>フォルダを選択すると、アセットを選択ダイアログボックスの右 <span class="wintitle"> 側のパネルに、その </span> フォルダ内に含まれている使用可能なすべてのデジタルアセットが表示されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_folderhistory.png"> </p> </td> 
      <td colname="col2"> <p>フォルダーのナビゲーション履歴を前後に移動できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_reloadfolder.png"> </p> </td> 
      <td colname="col2"> <p>選択したフォルダーに対して表示されるデジタルアセットのリストを更新します。 </p> <p>「アクション」ドロップダウンリストを使用して選択したアセットを移動、削除、または名前変更する場合は、このコントロールをク <span class="uicontrol"> リック </span> する必要がある場合があります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_list_or_grid.png"> </p> </td> 
      <td colname="col2"> <p>デジタルアセットをリスト表示で表示します。 リストには、各アセットに関連付けられたアイコンまたはサムネール画像、ファイル名、デジタルアセットの種類、サイズ（該当する場合）、最後に編集された日付が表示されます。 </p> <p>グリッド表示では、選択したフォルダー内のデジタルアセットがアイコン、サムネールまたはその両方で表示されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_actionsdropdown.png"> </p> </td> 
      <td colname="col2"> <p>リストビューでは、選択したデジタルアセットを移動、削除または名前変更できます。 </p> <p>グリッドビューでは、選択した1つ以上のデジタルアセットを移動または削除できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_upload.png"> </p> </td> 
      <td colname="col2"> <p>アップロード <span class="wintitle"> ダイアログ </span> ボックスを開き、選択したデジタルアセットをデスクトップまたは外部サーバーからアップロードして、バナーとして使用できるようにします。 </p> <p>アセットをアップロードすると、公開ジョブがScene7 Publishing Systemで自動的にスケジュールされます。 </p> <p>Adobe Dynamic Media Classicを使用したバナーの追 <a href="../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3" type="reference" format="dita" scope="local"> 加のオプションの表を参照してくださ </a>い。 </p> <p>Scene7 Publishing Systemを使用したデジタルアセットのアップロードと公開について詳しく説明します。 </p> <p>『Scene7 Publishing Systemユ <a href="https://help.adobe.com/en_US/scene7/using/WS3673AD39-098B-4f08-8A24-CA51261B7366.html" scope="external" format="html"> ーザガイド』のア </a> セットのアップロードと公開を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_searchfield.png"> </p> </td> 
      <td colname="col2"> <p>デジタルアセットをキーワードで検索したり、選択したフォルダー内のファイルの場所や関連するサブフォルダーで検索したりできます。 </p> <p>検索フィールドをクリックすると、オプションのフィルターフィールドが自動的に追加されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_addfilter.png"> </p> </td> 
      <td colname="col2"> <p>別のアセットフィルターを追加し、表示するデジタルアセットのリストを種類別または特定の日付別にさらに絞り込むことができます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_Kindfilter.png"> </p> </td> 
      <td colname="col2"> <p>表示するデジタルアセットのリストを絞り込み、Flash、画像、テンプレート、任意など特定の種類のアセットのみを表示します。 </p> <p>をクリッ <img src="assets/s7_deletefilter.png"> クして、検索からフィルターを削除します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_datefilter.png"> </p> </td> 
      <td colname="col2"> <p>表示されるデジタルアセットのリストを絞り込み、特定の日付より前または特定の日付より後に作成または編集されたアセットのみを表示します。 </p> <p>をクリッ <img src="assets/s7_deletefilter.png" /> クして、検索からフィルターを削除します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_assetzoom.png"> </p> </td> 
      <td colname="col2"> <p>スライダを左右にドラッグして、デジタルアセットパネルの表示全体を縮小または拡大できます。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **プロパティオプション**

   Flashテンプレート、画像テンプレートまたは画像を選択した場合は、「プロパティ」オプションが表示されます。 選択したデジタルアセットに応じて、すべてのオプションが使用できるわけではありません。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>プロパティオプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>名前 </p> </td> 
      <td colname="col2"> <p>テンプレートまたは画像の説明的な名前（空白は含まない）。 必要に応じて、画像サイズの指定を名前に含め、ユーザがアセットをさらに識別できるようにします。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>形式 </p> </td> 
      <td colname="col2"> <p>画像または画像テンプレートの形式を指定します。 </p> <p>次の形式から選択できます。 </p> 
        <ul id="ul_9A19421BCC424CF585645049DCB87F10"> 
        <li id="li_A4913D783BD547F9AFA1A259C56EC2B3">jpeg </li> 
        <li id="li_66237D7BE8754FB0B0088CE5A02C0214">png </li> 
        <li id="li_4EDDFD7C8AB04677BEC20EFC9AEBBF1F">png-alpha </li> 
        <li id="li_4FCB03C29AE647ACBAF5105016DF7579">gif </li> 
        <li id="li_B884BD7DFF1845FAA9C58EF09B888A77">gif-alpha </li> 
        </ul> <p>このオプションは、Flashテンプレートには適用されません。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>画質 </p> </td> 
      <td colname="col2"> <p>JPEGまたはGIF形式の画像の圧縮レベルを制御します。 この設定は、ファイルサイズと画質の両方に影響します。 画質は1～100です。 </p> <p>スライダを左右にドラッグすると、プレビューウィンドウの画像が更新され、画質の変化が反映されます。 </p> <p>このオプションは、Flashテンプレートには適用されません。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>幅 </p> </td> 
      <td colname="col2"> <p>デジタルアセットの幅をピクセル単位で指定します。 このディメンションは、Webサイトを訪問した顧客がアセットを表示する幅です。 </p> <p>このオプションは、Flashテンプレートには適用されません。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>高さ </p> </td> 
      <td colname="col2"> <p>デジタルアセットの高さをピクセル単位で指定します。 このディメンションは、Webサイトを訪問した顧客がアセットを表示する高さです。 </p> <p>このオプションは、Flashテンプレートには適用されません。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **バナーリンクのオプション**

   「バナーリンク」オプションは、バナーの画像または画像テンプレートを選択した場合にのみ表示されます。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>バナーリンクオプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>リンク URL </p> </td> 
      <td colname="col2"> <p>顧客が画像をクリックしたときにバナーにリンクするURLアドレスを指定します。 </p> <p>バナーを何もリンクさせない場合は、「リンクURL」フィールドを空欄にします。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Target </p> </td> 
      <td colname="col2"> <p>新しいブラウザーウィンドウや新しいタブなど、リンクされたバナーを開く場所を指定します。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **リンクの変更オプション**

   「リンクを変更」オプションは、バナーのFlashテンプレートを選択した場合にのみ表示されます。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>リンクの変更オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <img placement="inline" id="image_EBB8159690C74D4692B5DF945B045E0B" src="assets/icon_edit_16.gif" /> </p> </td> 
      <td colname="col2"> <p>Flashテンプレートで使用されるURLリンクフィールドを編集できます。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **テキストを置換オプション**

   「テキストを置換」オプションは、編集可能なテキストレイヤーを含むバナーのFlashテンプレートを選択した場合にのみ表示されます。

   Flashテンプレート内のテキストに対して行った変更は、プレビューウィンドウに反映されます。

   >[!NOTE]
   >
   >「cow」を「apple」に置き換える検索および置換コマンドを追加し、次に「apple」を「orange」に置き換える2番目のコマンドを作成した場合、2番目のコマンドは有効になりません。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>テキストを置換オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_addfilter.png"> </p> </td> 
      <td colname="col2"> <p>検索および置換フィールドを追加します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_deletefilter.png"> </p> </td> 
      <td colname="col2"> <p>[検索と置換]フィールドを削除し、以前に使用したテキストを復元します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>検索 </p> </td> 
      <td colname="col2"> <p>Flashテンプレートのレイヤー内のリンクされていないテキストの検索語句を入力できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Replace </p> </td> 
      <td colname="col2"> <p>検索するテキストの代わりに挿入するテキストを指定できます。 </p> <p>このフィールドで <span class="uicontrol"> Enterキー </span> を押すと、プレビューウィンドウが置換後のテキストで更新されます。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **パラメータのオプション**

   パラメータのオプションは、バナーの画像テンプレートまたはFlashテンプレートを選択した場合にのみ表示されます。 実際のパラメータのオプションは、Scene7 Publishing Systemでテンプレートが作成され、パラメータ化された方法によって異なります。 例えば、テンプレートに、テキスト、フォントスタイル、価格、送料無料で使用する特別なコード、バナー内の画像のサイズ、使用する別の画像を参照するなどの変更を可能にするフィールドをパラメータ化する場合があります。

   >[!NOTE]
   >
   >パラメータに対して行った変更は、ビジネスルールによって上書きされる可能性があることに注意してください。 パラメーターがデフォルトとして機能するのは、それ以外の場合はパラメーターを変更するビジネスルールが作成されない場合のみです。

   「新しいビ [ジネスルールの追加」を参照してくださ](../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7)い。

   See [Editing a business rule](../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087).

   **レイヤーの表示/非表示の切り替えオプション**

   「レイヤーの表示/非表示を切り替え」オプションは、バナーにFlashテンプレートを選択した場合にのみ適用されます。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>レイヤーの表示/非表示の切り替えオプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_togglelayervisibility.png"> </p> </td> 
      <td colname="col2"> <p>Flashテンプレートファイルを構成する様々なレイヤーの表示/非表示を切り替えます。 </p> <p>画層の表示/非表示を切り替えるたびに、プレビューウィンドウが更新され、表示が更新されます。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

   （オプション）バナーに使用するデジタルアセットが選択したフォルダーで使用できない場合は、アップロードが必要な場合があります。 をク **[!UICONTROL Upload]**&#x200B;リックし、目的のファイルとオプションを選択します。 ファイルが選択したフォルダにアップロードされます。

   >[!NOTE]
   >
   >Scene7アセットビューアでアップロード機能を使用する場合は、使用するScene7アカウントに「SPS会社管理者」という役割が既に設定されていることを確認します。

   『Scene7 Publishing System [ユーザガイド](https://help.adobe.com/en_US/scene7/using/WS662101DF-D697-47a7-A7D8-B52FD8E94438.html) 』の「管理設定」を参照してください。

   **基本オプション**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>閲覧 </p> </td> 
      <td colname="col2"> <p> アップロードして公開するファイルを参照し、バナーとして使用するファイルを選択します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> 上書き </p> </td> 
      <td colname="col2"> <p>アップロードするファイルは、選択したフォルダ内の既存のファイルを同じファイル名で置き換えます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>電子メールの設定 </p> </td> 
      <td colname="col2"> <p> アップロードに関してどの電子メール通知を受け取るかを選択できます。また、アップロードジョブに関する通知を受け取らないようにすることもできます。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **詳細オプション**

   PostScript(EPS)またはIllustrator(AI)画像ファイルをアップロードする場合、様々な方法でファイルの形式を設定できます。 ファイルをラスタライズし、印刷テンプレート用にFXGに変換し、透明な背景を維持し、解像度を選択して、カラースペースを選択することができます。

   PSD(Photoshop Document)ファイルは、ダイナミックメディアクラシックでテンプレートの作成に最もよく使用されます。 PSDファイルをアップロードする場合、ファイルからDynamic Media Classicテンプレートを自動的に作成できます(オプションを選 **[!UICONTROL Create Template]** 択します)。

   Scene7 Publishing Systemは、ファイルを使用してテンプレートを作成する場合、レイヤーを含むPSDファイルから複数の画像を作成します。各レイヤーに対して1つの画像が作成されます。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプショングループ名 </p> </th> 
      <th colname="col02" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>カラープロファイルオプション </p> </td> 
      <td colname="col02"> <p>カラープロファイル </p> </td> 
      <td colname="col2"> <p> 次のオプションから選択できます。 </p> 
        <ul id="ul_6927BC08CA2647EDB2C85DAD2B82AE31"> 
        <li id="li_CA3F44FF9C0F4CE987DCB0AF9303C2E4"> <span class="uicontrol"> SRGBに変換 </span> <p>SRGB(Standard Red Green Blue)に変換します。 Webページに画像を表示する場合は、SRGBが推奨されるカラースペースです。 </p> </li> 
        <li id="li_FCCEE6B14CCD4246ADA152932010ABF1"> <span class="uicontrol"> 元のカラースペースを維持 </span> <p>元のカラースペースを保持します。 </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>画像編集オプション </p> </td> 
      <td colname="col02"> <p>クリッピングパスからマスクを作成 </p> </td> 
      <td colname="col2"> <p>画像のクリッピングパス情報に基づいて、画像のマスクを作成します。 このオプションは、画像編集アプリケーションで作成された、クリッピングパスが作成された画像に適用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>PostScriptオプション </p> <p>Illustratorのオプション </p> </td> 
      <td colname="col02"> <p>処理中 </p> </td> 
      <td colname="col2"> <p> <span class="uicontrol"> 「ラスタラ </span> イズ」オプションを選択すると、ファイル内のベクトルグラフィックがビットマップ形式に変換されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Postscriptオプション </p> <p>Illustratorのオプション </p> </td> 
      <td colname="col02"> <p> 解像度 </p> </td> 
      <td colname="col2"> <p> 解像度設定を指定します。 この設定は、ファイル内に表示される1インチあたりのピクセル数を決定します。 デフォルトは 150 です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> PostScriptオプション </p> <p>Illustratorのオプション </p> </td> 
      <td colname="col02"> <p> カラースペース </p> </td> 
      <td colname="col2"> <p>Illustratorファイルのカラースペースを選択できます。 RGBカラースペースは、オンライン表示に適しています。 </p> <p>次のカラースペースオプションから選択できます。 </p> 
        <ul id="ul_0E83E2762A574480B243F963A7FB2ACD"> 
        <li id="li_B9FEC7D220D04CCABACD30839051DAE4"> <span class="uicontrol"> 自動検出 </span> <p> PDFファイルのカラースペースを保持します。 </p> </li> 
        <li id="li_ED0EB3B12BCF41C7AFC435447010B6FF"> <span class="uicontrol"> RGBとしてレンダリング </span> <p> RGBカラースペースに変換します。 </p> </li> 
        <li id="li_3FB5DD8887C540BC97148A4D63B38F72"> <span class="uicontrol"> CMYKとしてレンダリング </span> <p> CMYKカラースペースに変換します。 </p> </li> 
        <li id="li_6C018D3A4B254880AD41896E9F4AF3D9"> <span class="uicontrol"> グレースケールとして適用 </span> <p> グレースケールカラースペースに変換します。 </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> PostScriptオプション </p> <p>Illustratorのオプション </p> </td> 
      <td colname="col02"> <p> 透明な背景を維持 </p> </td> 
      <td colname="col2"> <p>ファイルの背景の透明度を維持します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Photoshopオプション </p> </td> 
      <td colname="col02"> <p> レイヤーの維持 </p> </td> 
      <td colname="col2"> <p>PSD内のレイヤーが存在する場合は、それを個々のアセットにリッピングします。 アセットレイヤーはPSDに関連付けられたままになります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Photoshopオプション </p> </td> 
      <td colname="col02"> <p>テンプレートの作成 </p> </td> 
      <td colname="col2"> <p> PSDファイルのレイヤーからテンプレートを作成します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Photoshopオプション </p> </td> 
      <td colname="col02"> <p> テキストの抽出 </p> </td> 
      <td colname="col2"> <p> 顧客がバナー内でキーワードを検索できるように、テキストを抽出します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Photoshopオプション </p> </td> 
      <td colname="col02"> <p> レイヤーを拡張 </p> </td> 
      <td colname="col2"> <p>リッピングされた画像レイヤーのサイズを背景レイヤーのサイズに拡張します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Photoshopオプション </p> </td> 
      <td colname="col02"> <p> レイヤーの命名 </p> </td> 
      <td colname="col2"> <p>PSDファイル内のレイヤーは、別々の画像としてアップロードされます。 Scene7 Publishing Systemで画像に名前を付ける方法を決めるには、次のオプションから選択します。 </p> 
        <ul id="ul_C2A25177A07740CA90B32C638304D39F"> 
        <li id="li_477D5BFF7238454BBF0E04B22DE378F7"> <span class="uicontrol"> PSDファイルのレイヤー名を使用 </span> <p>PSDファイル内のレイヤー名の後に画像の名前を付けます。 例えば、元のPSDファイルの <span class="codeph"> Price Tagとい </span> う名前のレイヤーは、Price Tagという名前の画像 <span class="codeph"> になりま </span>す。 ただし、PSDファイルのレイヤー名が初期設定のPhotoshopレイヤー名（背景、レイヤー1、レイヤー2など）の場合、画像の名前は初期設定のレイヤー名ではなく、PSDファイルのレイヤー番号に従います。 </p> </li> 
        <li id="li_EB4173B884FC41328CFBDE27DA6D43AA"> <span class="uicontrol"> PSDファイル名と付加番号を使用 </span> <p>PSDファイルのレイヤー番号の後に画像の名前を付け、元のレイヤー名は無視します。 画像には、Photoshopのファイル名とレイヤー番号が付いた名前が付けられます。 例えば、Spring Ad.psdというファイルの2番目のレイヤーは、Photoshopで初期設定以外の名前が付い <span class="codeph"> ている場合でも、 </span><span class="codeph"></span> Spring Ad_2という名前が付けられます。 </p> </li> 
        <li id="li_10B2D2DE2FD24BD08DB56D1D95ABA53D"> <span class="uicontrol"> PSDファイル名とレイヤー名または番号を使用 </span> <p>画像には、PSDファイルの後に、レイヤー名またはレイヤー番号が続く名前が付けられます。 PSDファイル内のレイヤー名が初期設定のPhotoshopレイヤー名の場合は、レイヤー番号が使用されます。 例えば、SpringAdというPSDファイル内の <span class="codeph"> Price Tagという名前のレ </span> イヤーは、 <span class="codeph"> Spring Ad_Price Tag </span> という名前になります <span class="codeph"></span>。 レイヤ2という名前のデフォル <span class="codeph"> トのレ </span> イヤは、 <span class="codeph"> Spring Ad_2という名前です </span>。 </p> </li> 
        <li id="li_5E57AC0719D4484B9C9BD14DB42B4455"> <span class="uicontrol"> PSDファイル名に基づいてフォルダを作成 </span> <p>PSDのファイル名を使用して、レイヤー画像のフォルダを作成します。 </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Photoshopオプション </p> </td> 
      <td colname="col02"> <p>アンカー </p> </td> 
      <td colname="col2"> <p>PSDファイルから作成されたレイヤーコンポジションから生成されたテンプレートでの画像のアンカー方法を指定します。 </p> <p>デフォルトでは、アンカーが中心です。 中央のアンカーを使用すると、置換画像の縦横比に関係なく、置換画像が同じスペースを最も適切に埋めることができます。 この画像を置き換える縦横比の異なる画像は、テンプレートを参照し、パラメータの置き換えを使用する場合、同じスペースを効果的に占有します。 アプリケーションで、テンプレートに割り当てられた領域を置換画像で埋める必要がある場合は、別の設定に変更します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>PDFオプション </p> </td> 
      <td colname="col02"> <p>処理中 </p> </td> 
      <td colname="col2"> <p> <span class="uicontrol"> ラスタライ </span> ズオプションは、PDFファイルのページをリッピングし、ベクトルグラフィックをビットマップ画像に変換します。 
        <!--Choose this option to create an eCatalog. (This option is thedefault.)--> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>PDFオプション </p> </td> 
      <td colname="col02"> <p> 解像度 </p> </td> 
      <td colname="col2"> <p>解像度設定を指定します。 この設定は、PDFファイルで1インチあたりに表示されるピクセル数を決定します。 デフォルトは 150 です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>PDFオプション </p> </td> 
      <td colname="col02"> <p> カラースペース </p> </td> 
      <td colname="col2"> <p>PDFファイルのカラースペースを選択できます。 ほとんどのPDFファイルには、RGBとCMYKの両方のカラー画像が含まれています。 RGBカラースペースは、オンライン表示に適しています。 </p> <p>次のカラースペースオプションから選択できます。 </p> 
        <ul id="ul_44A8C39DEB21473F9375E3962F14D3C6"> 
        <li id="li_1046FA0017934C5EB7C0100F8F78507D"> <span class="uicontrol"> 自動検出 </span> <p> PDFファイルのカラースペースを保持します。 </p> </li> 
        <li id="li_561CCF705EDD451993D2DA2EB33F05F7"> <span class="uicontrol"> RGBとしてレンダリング </span> <p> RGBカラースペースに変換します。 </p> </li> 
        <li id="li_D9E8CF61C40140979484EDEF7DAD2C44"> <span class="uicontrol"> CMYKとしてレンダリング </span> <p> CMYKカラースペースに変換します。 </p> </li> 
        <li id="li_F3606B45C0F84BA594263EA12243F67A"> <span class="uicontrol"> グレースケールとして適用 </span> <p> グレースケールカラースペースに変換します。 </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>PDFオプション </p> </td> 
      <td colname="col02"> <p>複数ページのPDFからeCatalogを自動生成 </p> </td> 
      <td colname="col2"> <p> PDFファイルからeCatalogを自動的に作成します。 eCatalogの名前は、アップロードしたPDFファイルの名前に従います。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> PDFオプション </p> </td> 
      <td colname="col02"> <p>キーワードの抽出 </p> </td> 
      <td colname="col2"> <p>PDFファイルから単語を抽出し、ファイルをキーワードで検索できるようにします。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 右側のウィンドウで、目的の画像、テンプレートまたはFlashファイルをクリックします。

   ポップアップ [!DNL Pick An Asset] ウィンドウが表示されます。
1. （オプション）ポップアップウ [!DNL Pick An Asset] ィンドウのドロッ [!DNL Actions] プダウンリストで、次のいずれかの操作を行います。

   * クリック **[!UICONTROL Move]**. ダイアログ [!DNL Select a folder to move to] ボックスで、デジタルアセットを移動するフォルダを選択します。 クリック **[!UICONTROL Move]**.

      別のフォルダーに移動する複数のデジタルアセットを選択することもできます。

   * クリック **[!UICONTROL Delete]**. ダイアログボッ [!DNL Delete Selected Assets] クスで、をクリックしま **[!UICONTROL Delete]**&#x200B;す。

      フォルダーから削除する複数のデジタルアセットを選択することもできます。

   * クリック **[!UICONTROL Rename]**. ダイアログ [!DNL Enter a new name for] ボックスのテキストフィールドに、デジタルアセットの新しい名前を入力します。 クリック **[!UICONTROL Rename]**.

1. （オプション）選択したデジタルアセットに応じて、ポップアップウィンドウの左 [!DNL Pick an Asset] 側のパネルで、必要なオプションを設定します。
1. アセットをクリックし、バナーとして使用するために選択します。
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## Adobe Dynamic Media Classicを使用したバナーの編集 {#task_C3E782477FBF428ABEA220751781ACA9}

Adobe Dynamic Media Classic [!DNL Edit Banner] を使用して追加したバナーのプロパティとパラメーターを変更する場合に使用します。

<!-- 

t_editing_a_banner_using_adobe_scene7.xml

 -->

HTMLコードを追加してバナーを追加した場合は、代わりにサイト検索/マーチャンダイジングを使用してバナーを編集します。

バナーの編集 [も参照してください](../c-about-design-menu/c-about-banners.md#task_D4081083BE7B40F5A003D1A2F1435AEA)。

**Adobe Dynamic Media Classicを使用してバナーを編集するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Design]** クしま **[!UICONTROL Banners]**&#x200B;す。
1. ページ [!DNL Banners] 上で、バ ![](assets/icon_edit_16.gif) ナーウィンドウの左下隅にS7アイコンが表示されたバナーサムネールの上をクリックします。
1. ページ [!DNL Change Parameter] で、必要なオプションを設定します。
1. バナーの編集が終了したら、をクリックしま **[!UICONTROL Save]**&#x200B;す。
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## バナーの削除 {#task_32F3BADC481E4E8984B2AA04B96052EB}

不要になったステージバナーを削除したり、一度に1つずつ使用したり、グループとして使用したい場合は、ステージバナーを削除できます。

<!-- 

t_deleting_banners.xml

 -->

**バナーを削除するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Design]** クしま **[!UICONTROL Banners]**&#x200B;す。
1. （オプション）次の1つ以上の操作を行います。

   * ページ [!DNL Banners] で、検索するバナーのタイプをドロップダウンリスト **[!UICONTROL Find banner of type]** から選択します。 必要に応じて、テキストフィールドにタグ名を指 **[!UICONTROL with tag]** 定するか、テキストフィールドにバナータイプ名を **[!UICONTROL with name]** 指定します。 クリック **[!UICONTROL Find.]**

   * ドロップダ **[!UICONTROL Sort]** ウンリストで、バナーの順序を選択します。
   * ドロッ **[!UICONTROL Show]** プダウンリストで、表示中の現在のページに読み込むバナーの数を選択します。

1. 次のいずれかを実行します。

   * 任意のバナーボックスの左上隅で、削除する各バナーのチェックボックスをクリックします。
   * ページの上部バーで、現在表示され [!DNL Banners] ているページ **[!UICONTROL Select all]** に読み込まれるすべてのバナーを選択する場合にオンにします。

1. ドロップダウ **[!UICONTROL Bulk Actions]** ンリストで、をクリックしま **[!UICONTROL Delete]**&#x200B;す。
1. ダイアログボッ [!DNL Confirmation Action] クスで、をクリックしま **[!UICONTROL OK]**&#x200B;す。
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## バナーのプレビュー {#task_6AB1F81A984A4DC2ACACD1FE030545E2}

ページに追加したバナーを参照して、フルサ [!DNL Banners] イズで表示することができます。 テンプレート内でバナーに影響するCSSは表示されません。

<!-- 

t_previewing_banners.xml

 -->

**バナーをプレビューするには**

1. 製品メニューで、/をクリッ **[!UICONTROL Design]** クしま **[!UICONTROL Banners]**&#x200B;す。
1. （オプション）次の1つ以上の操作を行います。

   * ページ [!DNL Banners] で、検索するバナーのタイプをドロップダウンリスト **[!UICONTROL Find banner of type]** から選択します。 必要に応じて、テキストフィールドにタグ名を指 **[!UICONTROL with tag]** 定するか、テキストフィールドにバナータイプ名を **[!UICONTROL with name]** 指定します。 クリック **[!UICONTROL Find.]**

   * ドロップダ **[!UICONTROL Sort]** ウンリストで、バナーの順序を選択します。
   * ドロッ **[!UICONTROL Show]** プダウンリストで、表示中の現在のページに読み込むバナーの数を選択します。

1. ページ上で、 [!DNL Banners] バナーのサムネールをクリックして、フルサイズで表示します。
1. 次のいずれかを実行します。

   * バナーのプレビューダイアログボックスで、左向きまたは右向き矢印をクリックして、追加したフルサイズのバナーを表示します。
   * 閉じるボタンをクリックしてバナーのプレビューダイアログボックスを閉じ、ページに戻 [!DNL Banners] ります。

## バナーのライブプッシュ {#task_161F4FEC8362474296A566E64BF05B97}

選択した1つ以上のバナーをWebサイトにライブにプッシュできます。

<!-- 

t_pushing_banners_live.xml

 -->

また、必要に応じて、ページの下部にあるオプションを使用して、すべての変更をバナーに **[!UICONTROL Push Live]** ライブにプッシュすることもで [!DNL Banners] きます。

詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

**バナーをライブにプッシュするには**

1. 製品メニューで、/をクリッ **[!UICONTROL Design]** クしま **[!UICONTROL Banners]**&#x200B;す。
1. （オプション）次の1つ以上の操作を行います。

   * ページ [!DNL Banners] で、検索するバナーのタイプをドロップダウンリスト **[!UICONTROL Find banner of type]** から選択します。 必要に応じて、テキストフィールドにタグ名を指 **[!UICONTROL with tag]** 定するか、テキストフィールドにバナータイプ名を **[!UICONTROL with name]** 指定します。 クリック **[!UICONTROL Find]**.

   * ドロップダ **[!UICONTROL Sort]** ウンリストで、バナーの順序を選択します。
   * ドロッ **[!UICONTROL Show]** プダウンリストで、表示中の現在のページに読み込むバナーの数を選択します。

1. 次のいずれかを実行します。

   * 任意のバナーボックスの左上隅で、削除する各バナーのチェックボックスをクリックします。
   * ページの上部バーで、現在表示され [!DNL Banner] ているページ **[!UICONTROL Select all]** に読み込まれるすべてのバナーを選択する場合にオンにします。

1. ドロップダウ **[!UICONTROL Bulk Actions]** ンリストで、をクリックしま **[!UICONTROL Push live]**&#x200B;す。
1. ダイアログボッ [!DNL Confirmation Action] クスで、をクリックしま **[!UICONTROL OK]**&#x200B;す。
1. （オプション）ページで、 [!DNL Banners] をクリックして **[!UICONTROL History]** 、行った変更を元に戻します。

   詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。
