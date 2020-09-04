---
description: バナーを使用して、Webサイトのバナー広告を管理できます。
seo-description: バナーを使用して、Webサイトのバナー広告を管理できます。
seo-title: バナーについて
solution: Target
title: バナーについて
topic: Design,Site search and merchandising
uuid: 653b567d-5cf3-41a0-a260-a6912d0fd20d
translation-type: tm+mt
source-git-commit: 552f93f1f630c64bbe3d5c8a87c4f5895ae6868c
workflow-type: tm+mt
source-wordcount: '4810'
ht-degree: 1%

---


# バナーについて {#about-banners}

バナーを使用して、Webサイト上のバナー広告を管理できます。

## バナーの使用 {#concept_5BBE01FEC6134393B43CC917C8CC64DA}

<!-- 

c_about_banners.xml

 -->

Webサイトにバナー広告を追加する方法は2つあります。

1つ目の方法は、ターゲットとSearch&amp;Promoteを使用してバナーを追加する方法です。 バナーは、顧客がWebサイトを検索したときに表示されるHTMLコードスニペットです。 バナーには、GIF、JPEG、PNG形式のテキストまたは画像を含めるか、その両方を組み合わせることができます。 プリセットサイズから選択するか、ページに合わせて独自のカスタムサイズを定義することができます。 バナーの表示に使用するHTMLコードでは、使用するフォントスタイルや境界線などを指定することもできます。 このバナーオファーの追加方法は、基本機能を追加するものであり、追加のソフトウェアは必要ありません。

2つ目の方法は、Adobeダイナミックメディアクラシック、ダイナミックメディア管理および公開サービスを使用することです。 有効なAdobeのダイナミックメディアクラシックアカウントを使用すると、バナーコンテンツを直接ターゲット、Search&amp;Promoteに管理および配信できます。 サイト検索/マーチャンダイジングでは、Dynamic Media Classicアカウントへのアクセスを設定します。 次に、ダイナミックメディアクラシックメディアブラウザを開き、バナーとして使用するダイナミックメディアアセットを選択します。

>[!NOTE]
>
>サイト検索/マーチャンダイジングで動的なメディアアセットをバナーとして使用する前に、アセットは最初にアップロードされ、Scene7パブリッシングシステムでの公開用に準備されます。 サイト検索/マーチャンダイジング内からアセットをアップロードし、Scene7パブリッシングシステムによる投稿の準備を自動的に行わせることができます。 または、すべてのアセットをScene7パブリッシングシステム内からアップロードして公開できます。

## バナーとAdobe Scene7パブリッシングシステムの統合 {#section_D4D7ADEA6A6348E68EDA138E184FE579}

画像、動的バナー、および画像テンプレートやFlashテンプレートなどのテンプレートを含む、サイト検索/マーチャンダイジングで、Dynamic Media Classicのアセットタイプをバナーとして使用できます。

テンプレートは、Adobe Photoshop®などの画像編集アプリケーションのレイヤーファイルのような、動的に作成され、アドレス指定可能なレイヤー画像ファイルです。 静的な画像ファイルとは異なり、テンプレートにはパラメーターを含めることができます。 パラメータを使用して、可変の画像のプロパティや画像コンテンツをカスタマイズできます。

>[!NOTE]
>
>また、Scene7Publishing Systemの印刷テンプレートを使用して、レイアウトベースのデザインからテンプレートを作成したり、Adobe IllustratorやAdobe InDesignのファイルを作成したりすることもできます。

『Dynamic Media Classic(Scene7)ユーザガイド』の印刷 [](https://help.adobe.com/en_US/scene7/using/WSFBFBAD30-2694-4b18-B7CE-894F9FC5CDDF.html) テンプレートを参照してください。

テンプレートには、任意の数の画像レイヤーとテキストレイヤーを含めることができます。 レイヤーPSDファイルなど、レイヤーが含まれる静的ファイルをテンプレートに変換したり、Dynamic Media Classicでテンプレートを作成したりできます。 Scene7パブリッシングシステムにアップロードしたフォントを使用して、テンプレート内にテキストレイヤーを作成できます。 テンプレートにテキストを追加した後、テキストの位置揃え、フォント、フォントサイズ、色を変更して、書式を設定できます。

ダイナミックメディアクラシックのパラメータ画面を使用して、テンプレートのあらゆる要素をアドレス指定可能なパラメータに変換できます。 その際、使用するレイヤー画像や、テンプレートで使用するテキスト値を変更できます。 パラメータはURL文字列と共に渡され、パラメータを変更することでImage Serverで生成される返信画像を動的にカスタマイズできます。

Dynamic Media Classicを使用してテンプレートを作成し、レイヤー上のプロパティをパラメータ化して、バナーで使用する方法について詳しく説明しています。

『Dynamic Media Classic(Scene7)ユーザガイド [](https://help.adobe.com/en_US/scene7/using/WS60B68844-9054-4099-BF69-3DC998A04D3C.html) 』の基本テンプレートを参照してください。

**アセットのアップロードと公開**

アセットをサイト検索/マーチャンダイジングのバナーで使用するには、Dynamic Media Classicでアセットをアップロードして公開する必要があります。 この前提条件には、画像テンプレートまたはFlashテンプレートで使用されるアセットも含まれます。 デジタルアセットをアップロードして公開するには、Dynamic Media Classicアカウントを使用します。 または、サイト検索/マーチャンダイジングを使用してデジタルアセットをアップロードし、アップロードの設定に基づいてDynamic Media Classicで自動的に公開することもできます。 アップロードおよび公開されていないアセットを選択しようとすると、操作を続行する前に、ユーザーインターフェイスに通知され、アップロードのオプションが与えられます。

Scene7パブリッシングシステムを使用したデジタルアセットのアップロードと公開についても詳しく説明しています。

『Dynamic Media Classic(Scene7)ユーザガイド [』の「アセットの](https://help.adobe.com/en_US/scene7/using/WS3673AD39-098B-4f08-8A24-CA51261B7366.html) アップロードと公開」を参照してください。

>[!NOTE]
>
>ダイナミックメディアクラシックアセットビューアのアップロード機能を使用するには、使用するダイナミックメディアクラシックアカウントに、「SPS会社管理者」というロールが既に設定されていることを確認します。

『Dynamic Media Classic(Scene7)ユーザガイド』の [](https://help.adobe.com/en_US/scene7/using/WS662101DF-D697-47a7-A7D8-B52FD8E94438.html) 管理設定を参照してください。

**ビジネス・ルールを使用したバナー内のダイナミック・メディア・クラシック・テンプレート・パラメータの変更**

Dynamic Media Classicのアセットをバナーとして追加した場合は、を使用して、Webサイト [!DNL Visual Rule Builder] の任意のバナー領域 [!DNL Business Rules] に追加できます。 例えば、バナーは他のバナーと同様に、検索結果ページに追加します。 また、Dynamic Media Classicテンプレートを特定のニーズに合わせてカスタマイズすることで、その初期設定のパラメーター値を上書きすることもできます。 この種の機能を使用すると、様々なマーケティングメッセージや異なるエンドポイントへのハイパーリンクを使用して、ダイナミックMedia Classicテンプレートをカスタマイズできます。

「新しいビジネスルールの [追加](../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7)」も参照してください。

「ビジネス・ルールの [編集](../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087)」も参照してください。

## バナーの追加 {#task_549D02B5F73B4158B105A94E39D937B7}

を使用して、バナー広告 [!DNL Banners] と、それらがWebサイト上のどこに配置されているかを管理できます。 バナーを追加すると、検索時に表示されるHTMLコードスニペットを使用して画像を外部参照します。

<!-- 

t_adding_a_new_banner.xml

 -->

有効なAdobeのダイナミックメディアクラシックアカウントをお持ちの場合は、Scene7パブリッシングシステムを介してバナー広告を追加できます。

詳しくは、Adobeダイナミックメディアクラシックを使用したバナーの [追加を参照してください](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3)。

詳しくは、AdobeのDynamic Media Classicアカウントへのアクセスの [設定を参照してください](../c-about-settings-menu/c-about-account-options-menu.md#task_CEFF88C2033D41D0B2FE86C435EDAC6D)。

**バナーを追加するには**

1. 製品メニューで、/をクリックし **[!UICONTROL Design]** ま **[!UICONTROL Banners]**&#x200B;す。
1. ページのドロ [!DNL Banners] ップダウン **[!UICONTROL Add Banner]** リストで、を選択し **[!UICONTROL HTML code]**&#x200B;ます。
1. ダイアログボッ [!DNL Add Banner] クスで、必要なオプションを設定します。

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
      <td colname="col2"> <p>必須。バナーの名前を識別します。 バナーをビジネスルールのビジュアルルールビルダーで追加するとき、バナーの名前を使用してバナーを参照します。 名前はバナーに表示されません。 </p> <p>「新しいビジネスルールの追加」を参照して <a href="../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7" type="task" format="dita" scope="local"> ください。</a> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>バナーHTML </p> </td> 
      <td colname="col2"> <p> バナーに関連付けられたHTMLコードを貼り付けることができます。 </p> <p>タグで囲まれたCSSコードや、タグで囲まれたJavaScriptコードなど、すべてのHTMLコードを使用で <code>
          &lt;style&gt; 
        </code> き <code>
          &lt;script&gt; 
        </code> ます。 例えば、次のコードブロックは、横置きの上部タイプのテキストバナー用です。 <code> &lt;div&nbsp;style="width:&nbsp;684px;&nbsp;background-image:&nbsp;url('https://www.brough.com/blackb.gif');&nbsp; 
          padding-top:&nbsp;10px;&nbsp;padding-bottom:&nbsp;10px;&nbsp;color:&nbsp;white;&nbsp;font-family:&nbsp;verdana;&nbsp; 
          text-align:&nbsp;center;&nbsp;font-size:&nbsp;20px;"&gt;&nbsp;Sound&nbsp;Study&nbsp;ships&nbsp;free!&nbsp;&lt;/div&gt; </code>次の例では、コードブロックはフルスプラッシュ画像用です。 <code> &lt;img&amp;nbsp;src='https://geometrixx.com/images/GEOAds/geometrixx-beauty-home-01.jpg'&amp;nbsp;border="0"&amp;nbsp;/&gt; </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>タイプ </p> </td> 
      <td colname="col2"> <p>次の種類のバナーを指定します。 
        <ul id="ul_6423AEDB9E664049989EB529D63C4A62"> 
          <li id="li_BF6CD60B3ED748D49CFFB9C5D607661C"> <span class="uicontrol"> [新しいタイプ] </span> <p>サイズや名前など、必要なバナーの種類を指定できます。 </p> </li> 
          <li id="li_1A29AB22AD644E60A12298187B5E898E"> <span class="uicontrol"> フルスプラッシュ </span> <p>このタイプのバナーの設定寸法は、幅が680ピクセル、高さが650ピクセルです。 オプションで種類の名前を指定するか、バナーの種類自体の名前をデフォルトの名前にすることができます。 </p> </li> 
          <li id="li_2BE06D013CB54DDE851051BFC038BB57"> <span class="uicontrol"> 水平上 </span> <p> バナーはWebサイトの上部に配置されます。 このタイプは、バナーの左または右にハイパーリンクを追加する場合に便利です。 このタイプのバナーの設定寸法は、幅が468ピクセル、高さが60ピクセルです。 オプションで種類の名前を指定するか、バナーの種類自体の名前をデフォルトの名前にすることができます。 </p> </li> 
          <li id="li_EC35AB92234749F08AA8A9BD26D0EA8D"> <span class="uicontrol"> 水平上部 — 全幅 </span> <p>このタイプは、新しいバナーを追加した場合のデフォルトです。 バナーはWebサイトの上部に配置され、ページの幅いっぱいに表示されます。 このタイプのバナーの設定寸法は、幅が670ピクセル、高さが150ピクセルです。 オプションで種類の名前を指定するか、バナーの種類自体の名前をデフォルトの名前にすることができます。 </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>タグ </p> </td> 
      <td colname="col2"> <p>バナーに関連付けるタグまたは「キーワード」を追加します。 多数のバナーを使用する場合、タグを追加すると、バナーの検索を絞り込むのに役立ち、必要に応じて適切なバナーをすばやく見つけることができます。 追加したタグを削除することもできます。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Save]**.
1. （オプション）次のいずれかの操作を行います。

   * をクリック **[!UICONTROL History]** すると、行った変更がすべて元に戻ります。

      「Historyオプションの [使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)」を参照してください。

   * クリック **[!UICONTROL Live]**.

      ライブ設定の [表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、 [ステージ設定をライブにプッシュするを参照してください](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)。

## バナーの編集 {#task_D4081083BE7B40F5A003D1A2F1435AEA}

バナー名、バナーHTML、バナーのタイプ、関連するタグなどを変更するに [!DNL Edit Banner] は、を使用します。

<!-- 

t_editing_a_banner.xml

 -->

サイト検索とマーチャンダイジングを使用してバナーを追加した場合は、AdobeのDynamic Media Classicを使用してバナーを編集することもできます。

Adobeダイナミックメディアクラシックを使用したバナーの [編集も参照してください](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9)。

**バナーを編集するには**

1. 製品メニューで、/をクリックし **[!UICONTROL Design]** ま **[!UICONTROL Banners]**&#x200B;す。
1. ページで、 [!DNL Banners] をクリックし ![](assets/icon_edit_16.gif)ます。

   編集するバナーサムネールの上に配置します。
1. ページで、目的のオプションを設定 [!DNL Edit Banner] します。

   「バナーの [追加」のオプションの表を参照してください](../c-about-design-menu/c-about-banners.md#task_549D02B5F73B4158B105A94E39D937B7)。
1. バナーの編集が終了したら、をクリックし **[!UICONTROL Save]**&#x200B;ます。
1. （オプション）次のいずれかの操作を行います。

   * をクリック **[!UICONTROL History]** すると、行った変更がすべて元に戻ります。

      「Historyオプションの [使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)」を参照してください。

   * クリック **[!UICONTROL Live]**.

      ライブ設定の [表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、 [ステージ設定をライブにプッシュするを参照してください](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)。

## Adobeダイナミックメディアクラシックを使用したバナーの追加 {#task_AD1E0C00A9E04B1FA819EB93288786B3}

を使用して、Webサイト [!DNL Banners] のバナー広告を管理できます。 Adobeダイナミックメディアクラシックを使用してバナーを追加する場合、Scene7パブリッシングシステムにアップロードした任意のデジタルアセットから選択できます。

<!-- 

t_adding_a_banner_using_adobe_scene7.xml

 -->

Adobeのダイナミックメディアクラシックを使用してバナーを追加するには、有効なダイナミックメディアクラシックアカウントへのアクセス権が設定されていることを確認してください。

詳しくは、AdobeのDynamic Media Classicアカウントへのアクセスの [設定を参照してください](../c-about-settings-menu/c-about-account-options-menu.md#task_CEFF88C2033D41D0B2FE86C435EDAC6D)。

**Adobeダイナミックメディアクラシックを使用してバナーを追加するには**

1. 製品メニューで、/をクリックし **[!UICONTROL Design]** ます。 **[!UICONTROL Banners.]**
1. ページのドロップダウン [!DNL Banners] リストで、を **[!UICONTROL Add Banner]** クリックし **[!UICONTROL Adobe Scene7]**&#x200B;ます。
1. ダイアログボックスの左 [!DNL Pick an Asset] 側のパネルで、ユーザーインターフェイスのナビゲーションオプションを使用して、バナーに使用するデジタルアセットが含まれるフォルダーを探します。

   アセットナビゲーションオプションを除き、その他のすべてのオプションは、追加または編集のために選択したデジタルアセットに依存します。

   サイト検索/マーチャンダイジングの新しいバナーに使用するアセットを見つけるには、アセットナビゲーションオプションを使用します。 ナビゲーションオプションは、選択したすべての種類のデジタルアセットに適用されます。

   >[!NOTE]
   >
   >アセットのナビゲーションオプションは、ダイアログボックスでバナーを編集するときに表示されません [!DNL Change Parameters] 。

   詳しくは、Adobeダイナミックメディアクラシックを使用したバナーの [編集を参照してください](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9)。

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
      <td colname="col2"> <p>特定の会社用のDynamic Media Classicアカウントをドロップダウンリストから選択し、そのアカウント内のデジタルアセットフォルダーに移動することもできます。 </p> <p>フォルダを選択すると、アセットを <span class="wintitle"> 選択ダイアログボックスの右側のパネルに、そのフォルダに含まれる使用可能なデジタルアセットがすべて表示され </span> ます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_folderhistory.png"> </p> </td> 
      <td colname="col2"> <p>フォルダーナビゲーション履歴を前後に移動できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_reloadfolder.png"> </p> </td> 
      <td colname="col2"> <p>選択したフォルダーに表示されているデジタルアセットのリストを更新します。 </p> <p>「 <span class="uicontrol"> アクション」ドロップダウンリストを使用して選択したアセットを移動、削除、名前変更する場合は、このコントロールをクリックする必要がある場合があ </span> ります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_list_or_grid.png"> </p> </td> 
      <td colname="col2"> <p>デジタルアセットをリスト表示で表示します。 リストには、各アセットの関連するアイコンまたはサムネール画像、ファイル名、デジタルアセットタイプ、サイズ、（該当する場合）および最後に編集された日付が表示されます。 </p> <p>グリッド表示には、選択したフォルダー内のデジタルアセットが、アイコン、サムネールまたはその両方として表示されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_actionsdropdown.png"> </p> </td> 
      <td colname="col2"> <p>リスト表示では、選択したデジタルアセットを移動、削除または名前変更できます。 </p> <p>グリッド表示では、選択した1つ以上のデジタルアセットを移動または削除できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_upload.png"> </p> </td> 
      <td colname="col2"> <p>アップロード <span class="wintitle"></span> ダイアログボックスを開きます。このダイアログボックスでは、選択したデジタルアセットをデスクトップまたは外部サーバーからアップロードし、バナーとして使用できるようにします。 </p> <p>アセットをアップロードすると、公開ジョブが自動的にScene7公開システムにスケジュールされます。 </p> <p>Adobeダイナミックメディアクラシックを使用したバナーの <a href="../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3" type="reference" format="dita" scope="local"> 追加のオプションの表を参照してくだ </a>さい。 </p> <p>Scene7パブリッシングシステムを使用したデジタルアセットのアップロードと公開についても詳しく説明しています。 </p> <p>『Scene7パブリッシングシステムユーザガイド』 <a href="https://help.adobe.com/en_US/scene7/using/WS3673AD39-098B-4f08-8A24-CA51261B7366.html" scope="external" format="html"></a> の「アセットのアップロードと公開」を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_searchfield.png"> </p> </td> 
      <td colname="col2"> <p>デジタルアセットをキーワードで検索したり、選択したフォルダー内のファイルの場所や関連付けられたサブフォルダーで検索したりできます。 </p> <p>検索フィールドをクリックすると、オプションのフィルターフィールドが自動的に追加されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_addfilter.png"> </p> </td> 
      <td colname="col2"> <p>別のアセットフィルターを追加して、種類別または特定の日付別に、表示されるデジタルアセットのリストをさらに絞り込むことができます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_Kindfilter.png"> </p> </td> 
      <td colname="col2"> <p>表示するデジタルアセットのリストを絞り込み、Flash、画像、テンプレート、任意など特定の種類のアセットのみを表示します。 </p> <p>をクリック <img src="assets/s7_deletefilter.png"> して、検索からフィルターを削除します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_datefilter.png"> </p> </td> 
      <td colname="col2"> <p>表示するデジタルアセットのリストを絞り込み、特定の日付より前または特定の日付より後に作成または編集されたアセットのみを表示します。 </p> <p>をクリック <img src="assets/s7_deletefilter.png" /> して、検索からフィルターを削除します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_assetzoom.png"> </p> </td> 
      <td colname="col2"> <p>スライダを左右にドラッグして、デジタルアセットパネルの表示全体を拡大または縮小できます。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **プロパティのオプション**

   Flashテンプレート、画像テンプレートまたは画像を選択すると、「プロパティ」オプションが表示されます。 選択したデジタルアセットに応じて、一部のオプションを使用できるわけではありません。

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
      <td colname="col2"> <p>テンプレートまたは画像のわかりやすい名前（空白は除く）。 ユーザがアセットをさらに識別しやすいように、名前に画像サイズを含めることもできます。 </p> </td> 
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
      <td colname="col1"> <p>クォリティ </p> </td> 
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
      <td colname="col2"> <p>顧客が画像をクリックしたときにバナーのリンク先となるURLアドレスを指定します。 </p> <p>バナーをリンクしない場合は、「リンクURL」フィールドを空欄にします。 </p> </td> 
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
      <td colname="col2"> <p>Flashテンプレートで使用されているURLリンクフィールドを編集できます。 </p> </td> 
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
      <th colname="col1" class="entry"> <p>「テキストを置換」オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_addfilter.png"> </p> </td> 
      <td colname="col2"> <p>検索と置換のフィールドを追加します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_deletefilter.png"> </p> </td> 
      <td colname="col2"> <p>「検索と置換」フィールドを削除し、以前に使用したテキストを復元します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>検索 </p> </td> 
      <td colname="col2"> <p>Flashテンプレートのレイヤー内の、リンクされていないテキストの検索語を入力できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Replace </p> </td> 
      <td colname="col2"> <p>検索するテキストの代わりに挿入するテキストを指定できます。 </p> <p>このフィールドで <span class="uicontrol"> Enterキーを押す </span> と、プレビューウィンドウが更新され、置換後のテキストが表示されます。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **パラメーターオプション**

   「パラメータ」オプションは、バナーに対して画像テンプレートまたはFlashテンプレートを選択した場合にのみ表示されます。 実際のパラメーターのオプションは、Scene7Publishing Systemでテンプレートを作成しパラメータ化した方法によって異なります。 例えば、テンプレートをパラメータ化して、テキスト、フォントスタイル、価格、送料無料に使用する特別コード、バナー内の画像のサイズ、使用する別の画像を参照するなどの変更を可能にする場合があります。

   >[!NOTE]
   >
   >パラメーターに対して行った変更は、ビジネスルールによって上書きされる可能性があることに注意してください。 パラメーターは、デフォルトとして機能します。デフォルトとして機能するのは、パラメーターを変更するビジネスルールが作成されていない場合のみです。

   「新しいビジネスルールの [追加](../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7)」を参照してください。

   See [Editing a business rule](../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087).

   **レイヤーの表示/非表示の切り替えオプション**

   「レイヤーの表示/非表示を切り替え」オプションは、バナーのFlashテンプレートを選択した場合にのみ適用されます。

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
      <td colname="col2"> <p>Flashテンプレートファイルを構成する様々なレイヤーの表示/非表示を切り替えます。 </p> <p>レイヤの表示/非表示を切り替えるたびに、プレビューウィンドウが更新され、表示が更新されます。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

   （オプション）バナーに使用するデジタルアセットが、選択したフォルダーで使用できない場合は、アップロードが必要な場合があります。 をクリック **[!UICONTROL Upload]**&#x200B;し、目的のファイルとオプションを選択します。 ファイルが選択したフォルダーにアップロードされます。

   >[!NOTE]
   >
   >Scene7アセットビューアでアップロード機能を使用する場合は、使用するScene7アカウントに、「SPS会社管理者」というロールが既に設定されていることを確認してください。

   『Scene7パブリッシングシステムユーザガイド [』の「](https://help.adobe.com/en_US/scene7/using/WS662101DF-D697-47a7-A7D8-B52FD8E94438.html) 管理設定」を参照してください。

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
      <td colname="col2"> <p> アップロード、公開、バナーとしての使用を選択するファイルを参照できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> 上書き </p> </td> 
      <td colname="col2"> <p>アップロードしたファイルは、選択したフォルダ内にある同じファイル名の既存のファイルと置き換えられます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>電子メールの設定 </p> </td> 
      <td colname="col2"> <p> アップロードに関して受け取る電子メール通知を選択できます。また、アップロードジョブに関連する通知を受け取らないようにすることもできます。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **詳細オプション**

   PostScript(EPS)画像ファイルまたはIllustrator(AI)画像ファイルをアップロードする場合、様々な方法でそれらのファイルをフォーマットできます。 ファイルをラスタライズし、印刷テンプレート用にFXGに変換し、透明な背景を維持し、解像度を選択し、カラースペースを選択することができます。

   PSD(Photoshopドキュメントファイル)は、Dynamic Media Classicでテンプレートを作成する際に最もよく使用されるファイルです。 PSDファイルをアップロードする場合、ファイルからDynamic Media Classicテンプレートを自動的に作成できます( **[!UICONTROL Create Template]** オプションを選択)。

   Scene7Publishing Systemでは、ファイルを使用してテンプレートを作成すると、レイヤーを持つPSDファイルから複数の画像が作成されます。各レイヤーに対して1つのイメージが作成されます。

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
        <li id="li_CA3F44FF9C0F4CE987DCB0AF9303C2E4"> <span class="uicontrol"> SRGBに変換 </span> <p>SRGB(Standard Red Green Blue)に変換します。 Webページに画像を表示する場合のカラースペースには、SRGBを使用することをお勧めします。 </p> </li> 
        <li id="li_FCCEE6B14CCD4246ADA152932010ABF1"> <span class="uicontrol"> 元のカラースペースを保持 </span> <p>元のカラースペースが保持されます。 </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>画像編集オプション </p> </td> 
      <td colname="col02"> <p>クリッピングパスからマスクを作成 </p> </td> 
      <td colname="col2"> <p>画像のクリッピングパス情報に基づいて、画像のマスクを作成します。 このオプションは、画像編集アプリケーションで作成された画像で、クリッピングパスが作成されたものに適用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>PostScriptオプション </p> <p>Illustratorオプション </p> </td> 
      <td colname="col02"> <p>処理中 </p> </td> 
      <td colname="col2"> <p> <span class="uicontrol"> 「ラスタライズ」 </span> オプションは、ファイル内のベクトルグラフィックをビットマップ形式に変換します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Postscriptオプション </p> <p>Illustratorオプション </p> </td> 
      <td colname="col02"> <p> 解像度 </p> </td> 
      <td colname="col2"> <p> 解像度設定を指定します。 この設定は、ファイルの1インチあたりに表示されるピクセル数(ppi)を決定します。 デフォルトは 150 です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> PostScriptオプション </p> <p>Illustratorオプション </p> </td> 
      <td colname="col02"> <p> カラースペース </p> </td> 
      <td colname="col2"> <p>Illustratorファイルのカラースペースを選択できます。 RGBカラースペースは、オンライン表示に適しています。 </p> <p>次のカラースペースオプションから選択できます。 </p> 
        <ul id="ul_0E83E2762A574480B243F963A7FB2ACD"> 
        <li id="li_B9FEC7D220D04CCABACD30839051DAE4"> <span class="uicontrol"> 自動検出 </span> <p> PDFファイルのカラースペースが保持されます。 </p> </li> 
        <li id="li_ED0EB3B12BCF41C7AFC435447010B6FF"> <span class="uicontrol"> RGBとしてレンダリング </span> <p> RGBカラースペースに変換します。 </p> </li> 
        <li id="li_3FB5DD8887C540BC97148A4D63B38F72"> <span class="uicontrol"> CMYKとしてレンダリング </span> <p> CMYKカラースペースに変換します。 </p> </li> 
        <li id="li_6C018D3A4B254880AD41896E9F4AF3D9"> <span class="uicontrol"> グレースケールとして強制 </span> <p> グレースケールカラースペースに変換します。 </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> PostScriptオプション </p> <p>Illustratorオプション </p> </td> 
      <td colname="col02"> <p> 透明な背景を維持 </p> </td> 
      <td colname="col2"> <p>ファイルの背景の透明度を維持します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Photoshopオプション </p> </td> 
      <td colname="col02"> <p> レイヤーを維持 </p> </td> 
      <td colname="col2"> <p>PSDにレイヤーがある場合は、そのレイヤーを個別のアセットにリッピングします。 アセットレイヤーとPSDとの関連付けは維持されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Photoshopオプション </p> </td> 
      <td colname="col02"> <p>テンプレートの作成 </p> </td> 
      <td colname="col2"> <p> PSDファイルのレイヤーからテンプレートを作成します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Photoshopオプション </p> </td> 
      <td colname="col02"> <p> テキストを抽出 </p> </td> 
      <td colname="col2"> <p> 顧客がバナー内でキーワードを検索できるように、テキストを抽出します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Photoshopオプション </p> </td> 
      <td colname="col02"> <p> レイヤーを拡張 </p> </td> 
      <td colname="col2"> <p>リッピングされた画像レイヤーを背景レイヤーのサイズに拡大します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Photoshopオプション </p> </td> 
      <td colname="col02"> <p> レイヤー名 </p> </td> 
      <td colname="col2"> <p>PSDファイル内のレイヤーは、個別の画像としてアップロードされます。 以下のオプションから選択して、Scene7パブリッシングシステムでこれらの画像に名前を付ける方法を決定できます。 </p> 
        <ul id="ul_C2A25177A07740CA90B32C638304D39F"> 
        <li id="li_477D5BFF7238454BBF0E04B22DE378F7"> <span class="uicontrol"> PSDファイルのレイヤー名を使用 </span> <p>PSDファイル内のレイヤー名が画像名になります。 例えば、元のPSDファイルで <span class="codeph"> Price Tagという名前のレイヤー </span> は、Price Tagという名前の画像にな <span class="codeph"></span>ります。 ただし、PSDファイルのレイヤー名が初期設定のPhotoshopレイヤー名（背景、レイヤー1、レイヤー2など）の場合、画像名は、初期設定のレイヤー名ではなく、PSDファイルのレイヤー番号に従って付けられます。 </p> </li> 
        <li id="li_EB4173B884FC41328CFBDE27DA6D43AA"> <span class="uicontrol"> PSDファイル名と付加番号を使用 </span> <p>PSDファイルのレイヤー番号が画像名になり、元のレイヤー名は無視されます。 画像には、Photoshopのファイル名とレイヤー番号を付けて名前を付けます。 例えば、 <span class="codeph"> Spring Ad.psdというファイルの2番目のレイヤー </span> は、Photoshopで初期設定以外の名前が付けられてい <span class="codeph"></span> た場合でも、Spring Ad_2という名前が付けられます。 </p> </li> 
        <li id="li_10B2D2DE2FD24BD08DB56D1D95ABA53D"> <span class="uicontrol"> PSDファイル名とレイヤー名または番号を使用 </span> <p>画像には、PSDファイルの後にレイヤー名またはレイヤー番号が続く名前が付けられます。 PSDファイル内のレイヤー名が初期設定のPhotoshopレイヤー名の場合は、レイヤー番号が使用されます。 例えば、SpringAdというPSDファイル <span class="codeph"> 内の </span> Price Tagという名前のレイヤー <span class="codeph"> は、 </span> Spring Ad_Price Tagという名前になり <span class="codeph"></span>ます。 レイヤー2という初期設定の名前を持つレ <span class="codeph"> イヤー </span> は、 <span class="codeph"> Spring Ad_2という名前になり </span>ます。 </p> </li> 
        <li id="li_5E57AC0719D4484B9C9BD14DB42B4455"> <span class="uicontrol"> PSDファイル名に基づいたフォルダの作成 </span> <p>PSDのファイル名を使用して、レイヤー画像のフォルダーを作成します。 </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Photoshopオプション </p> </td> 
      <td colname="col02"> <p>アンカー </p> </td> 
      <td colname="col2"> <p>PSDファイルから作成されたレイヤーコンポジションから生成されたテンプレートに画像をアンカーする方法を指定します。 </p> <p>デフォルトでは、アンカーが中央に配置されます。 中央のアンカーを使用すると、置換画像の縦横比に関係なく、置換画像を同じスペースに最も適切に埋めることができます。 この画像を置き換える縦横比が異なる画像は、テンプレートを参照し、パラメータの置き換えを使用する場合、同じスペースを効果的に占有します。 アプリケーションで、テンプレートに割り当てられたスペースを置換画像が埋める必要がある場合は、別の設定に変更します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>PDFオプション </p> </td> 
      <td colname="col02"> <p>処理中 </p> </td> 
      <td colname="col2"> <p> <span class="uicontrol"> 「ラスタライズ」 </span> オプションを選択すると、PDFファイルのページがリッピングされ、ベクトルグラフィックがビットマップ画像に変換されます。 
        <!--Choose this option to create an eCatalog. (This option is thedefault.)--> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>PDFオプション </p> </td> 
      <td colname="col02"> <p> 解像度 </p> </td> 
      <td colname="col2"> <p>解像度設定を指定します。 この設定は、PDFファイルで表示する1インチあたりのピクセル数(ppi)を指定します。 デフォルトは 150 です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>PDFオプション </p> </td> 
      <td colname="col02"> <p> カラースペース </p> </td> 
      <td colname="col2"> <p>PDFファイルのカラースペースを選択できます。 ほとんどのPDFファイルには、RGBとCMYKの両方のカラー画像が含まれています。 RGBカラースペースは、オンライン表示に適しています。 </p> <p>次のカラースペースオプションから選択できます。 </p> 
        <ul id="ul_44A8C39DEB21473F9375E3962F14D3C6"> 
        <li id="li_1046FA0017934C5EB7C0100F8F78507D"> <span class="uicontrol"> 自動検出 </span> <p> PDFファイルのカラースペースが保持されます。 </p> </li> 
        <li id="li_561CCF705EDD451993D2DA2EB33F05F7"> <span class="uicontrol"> RGBとしてレンダリング </span> <p> RGBカラースペースに変換します。 </p> </li> 
        <li id="li_D9E8CF61C40140979484EDEF7DAD2C44"> <span class="uicontrol"> CMYKとしてレンダリング </span> <p> CMYKカラースペースに変換します。 </p> </li> 
        <li id="li_F3606B45C0F84BA594263EA12243F67A"> <span class="uicontrol"> グレースケールとして強制 </span> <p> グレースケールカラースペースに変換します。 </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>PDFオプション </p> </td> 
      <td colname="col02"> <p>複数ページのPDFからeCatalogを自動生成 </p> </td> 
      <td colname="col2"> <p> PDFファイルからeCatalogを自動的に作成します。 eCatalogの名前は、アップロードしたPDFファイルに従って付けられます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> PDFオプション </p> </td> 
      <td colname="col02"> <p>キーワードの抽出 </p> </td> 
      <td colname="col2"> <p>PDFファイルから単語を抽出し、キーワードでファイルを検索できるようにします。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 右側のウィンドウで、目的の画像、Flashまたはテンプレートファイルをクリックします。

   ポップアップウィン [!DNL Pick An Asset] ドウが表示されます。
1. （オプション） [!DNL Pick An Asset] ポップアップウィンドウの [!DNL Actions] ドロップダウンリストで、次のいずれかの操作を行います。

   * クリック **[!UICONTROL Move]**. ダイアログボックスで、デジタルアセットを移動するフォルダーを選択します。 [!DNL Select a folder to move to] クリック **[!UICONTROL Move]**.

      別のフォルダーに移動する複数のデジタルアセットを選択することもできます。

   * クリック **[!UICONTROL Delete]**. ダイアログボックスで、 [!DNL Delete Selected Assets] をクリックし **[!UICONTROL Delete]**&#x200B;ます。

      フォルダーから削除する複数のデジタルアセットを選択することもできます。

   * クリック **[!UICONTROL Rename]**. ダイアログボックスのテキストフィールドに、デジタルアセットの新しい名前を入力します。 [!DNL Enter a new name for] クリック **[!UICONTROL Rename]**.

1. （オプション）選択したデジタルアセットに応じて、ポップアップウィンドウの左側のパネルで、目的のオプション [!DNL Pick an Asset] を設定します。
1. アセットをクリックして、バナーとして使用するアセットを選択します。
1. （オプション）次のいずれかの操作を行います。

   * をクリック **[!UICONTROL History]** すると、行った変更がすべて元に戻ります。

      「Historyオプションの [使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)」を参照してください。

   * クリック **[!UICONTROL Live]**.

      ライブ設定の [表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、 [ステージ設定をライブにプッシュするを参照してください](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)。

## Adobeダイナミックメディアクラシックを使用したバナーの編集 {#task_C3E782477FBF428ABEA220751781ACA9}

Adobe [!DNL Edit Banner] ダイナミックメディアクラシックを使用して追加したバナーのプロパティとパラメーターを変更する場合に使用します。

<!-- 

t_editing_a_banner_using_adobe_scene7.xml

 -->

HTMLコードを追加してバナーを追加した場合は、代わりにsite search/merchandisingを使用してバナーを編集します。

「バナーの [編集](../c-about-design-menu/c-about-banners.md#task_D4081083BE7B40F5A003D1A2F1435AEA)」も参照してください。

**Adobeダイナミックメディアクラシックを使用してバナーを編集するには**

1. 製品メニューで、/をクリックし **[!UICONTROL Design]** ま **[!UICONTROL Banners]**&#x200B;す。
1. ページ上で [!DNL Banners] 、バナーウィンドウ ![](assets/icon_edit_16.gif) の左下隅にS7アイコンが表示されたバナーサムネールの上をクリックします。
1. ページで、目的のオプションを設定 [!DNL Change Parameter] します。
1. バナーの編集が終了したら、をクリックし **[!UICONTROL Save]**&#x200B;ます。
1. （オプション）次のいずれかの操作を行います。

   * をクリック **[!UICONTROL History]** すると、行った変更がすべて元に戻ります。

      「Historyオプションの [使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)」を参照してください。

   * クリック **[!UICONTROL Live]**.

      ライブ設定の [表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、 [ステージ設定をライブにプッシュするを参照してください](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)。

## バナーの削除 {#task_32F3BADC481E4E8984B2AA04B96052EB}

不要になったステージバナーや、一度に使用したいステージバナーを削除したり、グループとして使用したい場合は、そのバナーを削除できます。

<!-- 

t_deleting_banners.xml

 -->

**バナーを削除するには**

1. 製品メニューで、/をクリックし **[!UICONTROL Design]** ま **[!UICONTROL Banners]**&#x200B;す。
1. （オプション）次の操作を1つ以上行います。

   * ページで、 [!DNL Banners] 検索するバナーのタイプをドロップダウン **[!UICONTROL Find banner of type]** リストから選択します。 必要に応じて、テキストフィールドにタグ名を指定するか、 **[!UICONTROL with tag]** テキストフィールドにバナータイプ名を指定し **[!UICONTROL with name]** ます。 クリック **[!UICONTROL Find.]**

   * ドロップダウン **[!UICONTROL Sort]** リストで、バナーのリスト順序を選択します。
   * ドロップダウン **[!UICONTROL Show]** リストで、表示している現在のページに読み込むバナーの数を選択します。

1. 次のいずれかを実行します。

   * 任意のバナーボックスの左上隅で、削除する各バナーのチェックボックスをクリックします。
   * ページの上部バーで、現在表示されている [!DNL Banners]**[!UICONTROL Select all]** ページに読み込まれるすべてのバナーを選択する場合にオンにします。

1. ドロップダウン **[!UICONTROL Bulk Actions]** リストでをクリックし **[!UICONTROL Delete]**&#x200B;ます。
1. ダイアログボックスで、 [!DNL Confirmation Action] をクリックし **[!UICONTROL OK]**&#x200B;ます。
1. （オプション）次のいずれかの操作を行います。

   * をクリック **[!UICONTROL History]** すると、行った変更がすべて元に戻ります。

      「Historyオプションの [使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)」を参照してください。

   * クリック **[!UICONTROL Live]**.

      ライブ設定の [表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、 [ステージ設定をライブにプッシュするを参照してください](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)。

## バナーのプレビュー {#task_6AB1F81A984A4DC2ACACD1FE030545E2}

ページに追加したバナーを参照して、フルサイズの表示を [!DNL Banners] 行うことができます。 テンプレート内のバナーに影響するCSSは表示されません。

<!-- 

t_previewing_banners.xml

 -->

**プレビューバナーを作成するには**

1. 製品メニューで、/をクリックし **[!UICONTROL Design]** ま **[!UICONTROL Banners]**&#x200B;す。
1. （オプション）次の操作を1つ以上行います。

   * ページで、 [!DNL Banners] 検索するバナーのタイプをドロップダウン **[!UICONTROL Find banner of type]** リストから選択します。 必要に応じて、テキストフィールドにタグ名を指定するか、 **[!UICONTROL with tag]** テキストフィールドにバナータイプ名を指定し **[!UICONTROL with name]** ます。 クリック **[!UICONTROL Find.]**

   * ドロップダウン **[!UICONTROL Sort]** リストで、バナーのリスト順序を選択します。
   * ドロップダウン **[!UICONTROL Show]** リストで、表示している現在のページに読み込むバナーの数を選択します。

1. ページ上で、バナーのサムネールをクリックして、フルサイズで表示します。 [!DNL Banners]
1. 次のいずれかを実行します。

   * バナープレビューダイアログボックスで、左または右の矢印をクリックして、追加したフルサイズのバナーに移動して表示します。
   * 「閉じる」ボタンをクリックしてバナープレビューダイアログボックスを閉じ、 [!DNL Banners] ページに戻ります。

## バナーをライブにプッシュする {#task_161F4FEC8362474296A566E64BF05B97}

選択した1つ以上のバナーをWebサイトにライブにプッシュできます。

<!-- 

t_pushing_banners_live.xml

 -->

また、必要に応じて、ページ下部にある **[!UICONTROL Push Live]** オプションを使用して、すべての変更をバナーにプッシュして有効にすることもでき [!DNL Banners] ます。

詳しくは、 [ステージ設定をライブにプッシュするを参照してください](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)。

**バナーをライブにプッシュするには**

1. 製品メニューで、/をクリックし **[!UICONTROL Design]** ま **[!UICONTROL Banners]**&#x200B;す。
1. （オプション）次の操作を1つ以上行います。

   * ページで、 [!DNL Banners] 検索するバナーのタイプをドロップダウン **[!UICONTROL Find banner of type]** リストから選択します。 必要に応じて、テキストフィールドにタグ名を指定するか、 **[!UICONTROL with tag]** テキストフィールドにバナータイプ名を指定し **[!UICONTROL with name]** ます。 クリック **[!UICONTROL Find]**.

   * ドロップダウン **[!UICONTROL Sort]** リストで、バナーのリスト順序を選択します。
   * ドロップダウン **[!UICONTROL Show]** リストで、表示している現在のページに読み込むバナーの数を選択します。

1. 次のいずれかを実行します。

   * 任意のバナーボックスの左上隅で、削除する各バナーのチェックボックスをクリックします。
   * ページの上部バーで、現在表示されている [!DNL Banner]**[!UICONTROL Select all]** ページに読み込まれるすべてのバナーを選択する場合にオンにします。

1. ドロップダウン **[!UICONTROL Bulk Actions]** リストでをクリックし **[!UICONTROL Push live]**&#x200B;ます。
1. ダイアログボックスで、 [!DNL Confirmation Action] をクリックし **[!UICONTROL OK]**&#x200B;ます。
1. （オプション） [!DNL Banners] ページでをクリックし、行った変更 **[!UICONTROL History]** を元に戻します。

   「Historyオプションの [使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)」を参照してください。
