---
description: アカウントオプションメニューを使用して、アカウント設定の更新、マーチャンダイジングの環境設定の設定、または独自のSearch&Promoteアカウントの削除を行います。
seo-description: アカウントオプションメニューを使用して、アカウント設定の更新、マーチャンダイジングの環境設定の設定、または独自のSearch&Promoteアカウントの削除を行います。
seo-title: アカウントオプションメニューについて
solution: Target
subtopic: Account Options
title: アカウントオプションメニューについて
topic: Settings,Site search and merchandising
uuid: 0f830033-de9e-4197-8d76-906c818662eb
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# アカウントオプションメニューについて{#about-the-account-options-menu}

アカウントオプションメニューを使用して、アカウント設定の更新、マーチャンダイジングの環境設定の設定、または独自のSearch&amp;Promoteアカウントの削除を行います。

## アカウント設定の指定 {#task_80A38D0C8E4F453395BD67B81E4B45D9}

Webサイトの名前や住所、タイムゾーンなどのアカウント設定を管理します。 または、アカウント番号を表示します。

**アカウント設定を行うには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Account Options]** ます **[!UICONTROL Account Settings]**。
1. ページ [!DNL Account Settings] で、必要なオプションを設定します。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Webサイト名 </p> </td> 
      <td colname="col2"> <p>必須。 </p> <p>Webサイト/アカウントの説明に使用される短い名前。 このオプションは、複数のWebサイトがある場合に役立ちます。 </p> <p> <p>注意： 使用する1つ以上の名前を選択する場合は、テクニカルサポートにお問い合わせください。 </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Webサイトのアドレス </p> </td> 
      <td colname="col2"> <p>必須。 </p> <p>WebサイトのURLアドレス。 ここで指定したアドレスは、Webサイトのメインエントリポイントとして使用されます。 </p> <p>インデックスを作 <a href="../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45" type="task" format="dita" scope="local"> 成する複数のURLエントリポイントの追加も参照してくださ </a>い。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>タイムゾーン（レポートおよびスケジュール用） </p> </td> 
      <td colname="col2"> <p>レポートおよび発行操作に使用されるタイムゾーン。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>保存時にテンプレートタグ属性を検証 </p> </td> 
      <td colname="col2"> <p>ステージングされたテンプ <span class="codeph"> レートエディターでテンプレートを保存すると </span> きに、 &lt;guided-*&gt;と&lt;search-*&gt; <span class="codeph"></span> のすべての属性を検証します。 </p> <p>詳しくは、プ <a href="../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3" type="task" format="dita" scope="local"> レゼンテーションまたは転送テンプレートの編集を参照してくだ </a>さい。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>保存時にGSオブジェクトへのテンプレート参照を検証 </p> </td> 
      <td colname="col2"> <p> &lt;guided-*&gt;タグで参照される、メニュー、ファセット、パンくずリスト、カスタムVar、テンプレートなどのガイド付き検索オブジェクトの存在を確認し <span class="codeph"></span> ます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>厳密なテンプレート構文チェックの実施 </p> </td> 
      <td colname="col2"> <p>テンプレートバリデーターをより厳密にし、不平衡な引用符や&lt;&gt;記号などをチェックできるようにします。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>アカウント番号 </p> </td> 
      <td colname="col2"> <p>アカウント番号は編集できません。 これは表示目的のみです。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Save Changes]**.

## Adobe CQ5との統合の設定 {#task_EA2FC2C24960498DAE01A1AB769D2F14}

Adobe CQ5とサイト検索/マーチャンダイジングの統合を設定できます。

**Adobe CQ5との統合を設定するには**

1. 次の手順を実行して、メンバーIDとアカウントIDを取得します。

   * サイト検索/マーチャンダイジングアカウントにログインします。
   * URLパスで、メンバーIDとアカウントIDをコピーします。

      例えば、アカウントのURLパスが `https://searchandpromote.mycompany.com/px/home/?sp_id=00123a4b-sp1234a5b6`次の場合、メンバーIDは `00123a4b` となり、アカウントIDはとなります `sp1234a5b6`。

1. Adobe CQ5で、「クラウドサービス」タブを使用して、サイト検索/マーチャンダイジングの設定を作成します。

   コピーしたメンバーIDとアカウントIDをそれぞれの設定で使用します。

## マーチャンダイジングの環境設定 {#task_7AC7B9F5D9F44E10AB5BC0B8CB31C37A}

デフォルトのルールビルダーやデフォルトの検索語句など、マーチャンダイジングの環境設定を管理します。

**マーチャンダイジングの環境設定を行うには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Account Options]** ます **[!UICONTROL Merchandising Preferences]**。
1. ページ [!DNL Merchandising Preferences] で、必要なオプションを設定します。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>トリガーグループ優性しきい値 </p> </td> 
      <td colname="col2"> <p> 「グループ優先」の結果ベースのトリガーに適用するしきい値の割合（「アカウントのデフォルトを使用」を指定）。 </p> <p>この設定を変更すると、直ちにライブ検索に影響する可能性があるので、注意して使用してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>グループ定義 </p> </td> 
      <td colname="col2"> <p>マーチャンダイジングコンソールのグループの結果の数。 最大5万。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> 「マーチャンダイジングドキュメントID」(MDI)フィールド </p> </td> 
      <td colname="col2"> <p> 指定するフィールドは、「単一の結果」の結果ベースのトリガーおよびアクションを使用して操作する検索結果を「一意に」修飾する必要があります。 </p> <p>事前定義URLフィールドの使用は、場合によっては機能しますが、お勧めしません。 各ページに固有のIDを持つユーザー定義のメタフィールド（SKUやproduct_idなど）は、URLフィールドを使用するよりもはるかに効率的です。 「なし」を指定すると、ルールマネージャーでの「単一結果」の結果ベースのトリガーとアクションが無効になります。 このオプションの変更は、今後保存されるルールにのみ適用されます。既存のルールは、元々保存されたMDIを引き続き使用します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>デフォルトのVRB (Visual Rule Builder)検索語句 </p> </td> 
      <td colname="col2"> <p> Visual Rule Builderで使用される最初の検索語句をカスタマイズできます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>VRBの既定の検索 </p> </td> 
      <td colname="col2"> <p>この設定を使用すると、Visual Rule Builderで最初に選択されるデフォルトの検索を設定できます。 </p> <p> この設定は、複数の検索を含む実装にのみ適用されます。 VRBを使用すると、定義したグループが適用するトリガーまたはアクションを選択できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>VRB /シミュレーターのタイムアウト </p> </td> 
      <td colname="col2"> <p>VRBとシミュレーターは、実稼動検索よりも遅いプロキシサーバーを通じて検索を送信します。 アセットの読み込みの遅さなど、特定の状況では、VRBまたはシミュレーターがタイムアウトする場合があります。 ユーザーインターフェイスが停止するまでに待機する秒数を増減できます。 この設定をデフォルトの60から増やす必要はほとんどありません。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Save Changes]**.

## Adobe Dynamic Media Classicアカウントへのアクセスの設定 {#task_CEFF88C2033D41D0B2FE86C435EDAC6D}

サイト検索/マーチャンダイジングアカウントをAdobe Dynamic Media Classicにリンクすると、Adobe Scene7からアップロードしたデジタルアセットを使用して、Webサイトにバナー広告を簡単に追加できます。

[バナーについて](../c-about-design-menu/c-about-banners.md#concept_5BBE01FEC6134393B43CC917C8CC64DA)を参照してください。

Adobe Dynamic Media Classic [を使用したバナーの追加を参照してください](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3)。

**Adobe Dynamic Media Classicアカウントへのアクセスを設定するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Account Options]** ます **[!UICONTROL Scene7 Configuration]**。
1. ページ [!DNL Scene7 Configuration] で、必要なオプションを設定します。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>地域 </p> </td> 
      <td colname="col2"> <p>必須。Dynamic Media Classicアカウントが各種Dynamic Media Classicサーバにアクセスする世界の地域を示します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>デフォルトの会社 </p> </td> 
      <td colname="col2"> <p>Dynamic Media Classicアカウントに関連付けられている会社の名前を示します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> 電子メール </p> </td> 
      <td colname="col2"> <p>必須。Dynamic Media Classicのログインと通信に使用する電子メールアドレスを指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Password </p> </td> 
      <td colname="col2"> <p>必須。Dynamic Media Classicのログインパスワード。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>有効 </p> </td> 
      <td colname="col2"> <p>サイト検索/マーチャンダイジング内のすべてのダイナミックメディアクラシックコントロールを有効にします。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>テスト </p> </td> 
      <td colname="col2"> <p>Dynamic Media Classicの地域名、電子メールアドレス、パスワードの詳細が正しいことを確認します。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. （オプション）をク **[!UICONTROL Test]** リックして、Dynamic Media Classicの地域名、電子メールアドレス、パスワードの詳細が正しいことを確認します。
1. クリック **[!UICONTROL Save Changes]**.

## Adobe Analyticsリダイレクターの設定 {#task_2C9DE333FD7246E4A460FC0F55204160}

サイト訪問者の追跡に [!DNL Adobe Analytics] 使用する場合、サイト検索/マーチャンダイジ [!DNL Adobe Analytics Redirector] ングでを使用して、を使用してすべてのHTTPリダイレクトを追跡できま [!DNL Adobe Analytics]す。

**Adobe Analyticsリダイレクターを設定するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Account Options]** ます **[!UICONTROL Adobe Analytics Redirector]**。
1. ページ [!DNL Adobe Analytics Redirector] で、必要なオプションを設定します。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Adobe Analyticsリダイレクター機能を有効にする </p> </td> 
      <td colname="col2"> <p>Adobe AnalyticsでのHTTPリダイレクトの追跡をオンにします。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>トラッキングサーバー </p> </td> 
      <td colname="col2"> <p> Adobe Analyticsトラッキングサーバー名を指定します。 </p> <p>トラッキングサーバー名を調べるには、 </p> <p> 
      <ol id="ol_D17B77E81F8D40D0948415CD60839BE3"> 
      <li id="li_BE58DBA104D44F0DB6C64AD3F12CEA97"> In Adobe Analytics, click <span class="uicontrol"> Admin </span> &gt; <span class="uicontrol"> Admin Console </span> &gt; <span class="uicontrol"> Code Manager </span>. </li> 
      <li id="li_67A93D17C3A14874928C6DC4FF2D4784"> [オプション] <span class="wintitle"> グ </span> ループボックスで、それぞれのドロップダウンリストからレポートスイートを選択します。 </li> 
      <li id="li_5AAB004AC58441DBB0F813BDE30EFFD4"> 「<span class="uicontrol">コードの生成</span>」をクリックします。 </li> 
      <li id="li_E80368993F4D4DD69E37509FF4348B36"> コードマネー <span class="wintitle"> ジャーペ </span> ージで、「コアJavaScriptファ <span class="uicontrol"> イル」タブをクリックしま </span>す。 </li> 
      <li id="li_991BDCDDA41A445F85CEEAAE9A46A304"> 「 <span class="wintitle"> Config Section」で、 </span>次の行を探します。 <p> <code> s.trackingServer="yourcompany.122.2o7.net" </code> </p> <p>トラッキングサーバー名は、この例で <span class="codeph"> は「yourcompany.122.2o7.net」です。 </span> </p> </li> 
      </ol> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>レポートスイート ID </p> </td> 
      <td colname="col2"> <p> レポートスイートIDを識別します。 </p> <p>レポートスイートIDを調べるには、 </p> <p> 
      <ol id="ol_4FD7B2459358486DBDB130426131D16A"> 
      <li id="li_9AF624CEB128453C808892EEE385D5D1"> In Adobe Analytics, click <span class="uicontrol"> Admin </span> &gt; <span class="uicontrol"> Admin Console </span> &gt; <span class="uicontrol"> Report Suites </span>. </li> 
      <li id="li_AAC47EAA04144A67BDCB5C7B8D8098E9"> 表の「レ <span class="wintitle"> ポートスイー </span> トID」列を見て、IDを見つけます。 </li> 
      </ol> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>カスタムパラメーター </p> </td> 
      <td colname="col2"> <p>Adobe AnalyticsのリダイレクトURLにカスタムパラメーターを追加できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>すべてのカスタム値の大文字と小文字を </p> </td> 
      <td colname="col2"> <p>上で指定したカスタムパラメータ値に使用する大文字と小文字の区別を標準化できます。 Adobe Analyticsでは大文字と小文字が区別されるので、値の大文字と小文字を統一する理由があります。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。
1. （オプション）ページで、 [!DNL Adobe Analytics Redirector] 次のいずれかの操作を行います。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## ルートファイルの設定 {#task_5F175C8743FB49A2A003813CBF7C56BF}

Webサイトのルートフォルダー内のルートファイルを管理します。

**ルートファイルを設定するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Account Options]** ます **[!UICONTROL Root Files]**。
1. ページ [!DNL Root Files] で、アップロードするルートファイルを参照します。

   <table> 
    <thead> 
    <tr> 
      <th colname="col1" class="entry"> <p>ルートファイル </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
      <td colname="col1"> <p>favicon.ico </p> </td> 
      <td colname="col2"> <p> サイトのアイコン。 通常は、顧客のブラウザーのアドレスバーに表示されます。 </p> </td> 
    </tr> 
    <tr> 
      <td colname="col1"> <p>robots.txt </p> </td> 
      <td colname="col2"> <p>ボットがWebサイトの特定の部分にアクセスすることを許可または禁止します。 </p> </td> 
    </tr> 
    <tr> 
      <td colname="col1"> <p>sitemap.xml </p> </td> 
      <td colname="col2"> <p>Webサイトで使用可能なすべてのページのリストを含むXMLファイル。 </p> </td> 
    </tr> 
    <tr> 
      <td colname="col1"> <p>crossdomain.xml </p> </td> 
      <td colname="col2"> <p>Flash Playerが複数のドメインにまたがるファイルにアクセスすることを許可または禁止します。 </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。
1. （オプション）ページで、 [!DNL Root Files] 次のいずれかの操作を行います。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 別のアカウントユーザーへのアカウント所有権の転送 {#task_47E3C66CC6374274830DA10171E0CF17}

アカウントの所有者は、ログインをキャンセルする場合、まず別のアクティブなアカウントユーザーに所有権を転送する必要があります。 を使用して、このタ [!DNL Transfer Ownership] スクを実行できます。

所有権は、既存のサイト検索/マーチャンダイジングアカウントユーザーに移動できます。

所有権の移転が完了すると、新しいアカウントの所有者が電子メール通知を受け取り、前の所有者がその職務の制限や責任を免除されます。

アカウントごとに所有者を1つだけ指定できます。 所有権を別のユーザーに移行した場合、所有権権限は失われます。

詳しくは、ロ [グインのキャンセルを参照してくださ](../c-about-settings-menu/c-about-my-profile-menu.md#task_D57701BB726243B08CEA14EEC86C3087)い。

「アカウ [ントの削除」を参照してくださ](../c-about-settings-menu/c-about-account-options-menu.md#task_975178D5B9444BF8B52D72B897A49C32)い。

アカウント [からの自分の削除を参照してくださ](../c-about-settings-menu/c-about-account-options-menu.md#task_C56F5AB87B664BAAAC2FD2F15003E73F)い。

**アカウント所有権を別のアカウントに転送するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Account Options]** ます **[!UICONTROL Transfer Ownership]**。
1. ページ [!DNL Transfer Ownership] で、アカウントの所有権を取得するユーザーをクリックします。
1. クリック **[!UICONTROL Transfer]**.

## アカウントの削除 {#task_975178D5B9444BF8B52D72B897A49C32}

アカウントを完全にサイト検索/マーチャンダイジングから削除できます。 この操作を行うと、自分や自分のアカウントの他のユーザーはアクセスできなくなります。

アカウントを削除すると、そのアカウントを使用して本番用サイトのインデックスを作成したり検索したりすることはできなくなります。 また、

他のユーザーがこのアカウントを引き続き使用できるようにするには、別のユーザーに所有権を移譲し、自分をアカウントのユーザーとして削除します。

別のアカウ [ントユーザーへのアカウント所有権の移行を参照してくださ](../c-about-settings-menu/c-about-account-options-menu.md#task_47E3C66CC6374274830DA10171E0CF17)い。

他のアカウントをお持ちの場合は、現在のアカウントを削除すると、ログインに表示されている最初のアカウントに移動します。

アカウント [からの自分の削除を参照してくださ](../c-about-settings-menu/c-about-account-options-menu.md#task_C56F5AB87B664BAAAC2FD2F15003E73F)い。

詳しくは、ロ [グインのキャンセルを参照してくださ](../c-about-settings-menu/c-about-my-profile-menu.md#task_D57701BB726243B08CEA14EEC86C3087)い。

**アカウントを削除するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Account Options]** ます **[!UICONTROL Remove Account]**。
1. （オプション）このフィー [!DNL Reason for Removal] ルドに、アカウントの削除の理由を入力します。
1. クリック **[!UICONTROL Remove Account]**.

## アカウントからの自分の削除 {#task_C56F5AB87B664BAAAC2FD2F15003E73F}

サイト検索/マーチャンダイジングアカウントから自分を削除できます。

アカウントから自分を削除すると、そのアカウントにアクセスできなくなり、アカウント設定の編集やサイトのインデックス作成ができなくなります。

アカウントに再度アクセスするには、現在のアカウントユーザーに元に戻すように依頼します。

詳しくは、ロ [グインのキャンセルを参照してくださ](../c-about-settings-menu/c-about-my-profile-menu.md#task_D57701BB726243B08CEA14EEC86C3087)い。

「アカウ [ントの削除」を参照してくださ](../c-about-settings-menu/c-about-account-options-menu.md#task_975178D5B9444BF8B52D72B897A49C32)い。

別のアカウ [ントユーザーへのアカウント所有権の移行を参照してくださ](../c-about-settings-menu/c-about-account-options-menu.md#task_47E3C66CC6374274830DA10171E0CF17)い。

**アカウントから自分を削除するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Account Options]** ます **[!UICONTROL Remove Yourself]**。
1. クリック **[!UICONTROL Remove Yourself]**.
