---
description: アカウントオプションメニューを使用して、アカウント設定の更新、マーチャンダイジングの環境設定の設定、独自のSearch&amp;Promoteアカウントの削除を行います。
solution: Target
subtopic: Account Options
title: '[アカウントオプション]メニューについて'
topic-legacy: Settings,Site search and merchandising
uuid: 0f830033-de9e-4197-8d76-906c818662eb
exl-id: 0acaeeed-1649-46bb-af41-20f144400d7c
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '1657'
ht-degree: 2%

---

# [アカウントオプション]メニューについて{#about-the-account-options-menu}

アカウントオプションメニューを使用して、アカウント設定の更新、マーチャンダイジングの環境設定、または独自のSearch&amp;Promoteアカウントの削除を行います。

## アカウント設定{#task_80A38D0C8E4F453395BD67B81E4B45D9}

Webサイトの名前や住所、タイムゾーンなどのアカウント設定を管理します。 または、アカウント番号を表示します。

**アカウント設定を構成するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Account Options]**/**[!UICONTROL Account Settings]**&#x200B;をクリックします。
1. [!DNL Account Settings]ページで、必要なオプションを設定します。

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
      <td colname="col2"> <p>必須。 </p> <p>Webサイト/アカウントの説明に使用する短い名前。 このオプションは、複数のWebサイトがある場合に役立ちます。 </p> <p> <p>注意： 使用する1つ以上の名前を選択する場合は、テクニカルサポートに問い合わせる必要があります。 </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Webサイトのアドレス </p> </td> 
      <td colname="col2"> <p>必須。 </p> <p>WebサイトのURLアドレス。 ここで指定するアドレスは、Webサイトのメインエントリポイントとして使用されます。 </p> <p><a href="../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45" type="task" format="dita" scope="local">インデックスを作成する複数のURLエントリポイントの追加</a>も参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>タイムゾーン（レポートおよびスケジュール用） </p> </td> 
      <td colname="col2"> <p>レポートおよび公開操作に使用するタイムゾーン。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>保存時にテンプレートタグ属性を検証 </p> </td> 
      <td colname="col2"> <p>Staged Template Editorでテンプレートを保存する際に、<span class="codeph"> &lt;guided-*&gt; </span>と<span class="codeph"> &lt;search-*&gt; </span>のすべての属性を検証します。 </p> <p>「<a href="../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3" type="task" format="dita" scope="local">プレゼンテーションまたはトランスポートテンプレートの編集</a>」を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>保存時にGSオブジェクトへのテンプレート参照を検証する </p> </td> 
      <td colname="col2"> <p> <span class="codeph"> &lt;guided-*&gt; </span>タグで参照されるメニュー、ファセット、パンくずリスト、カスタムVars、テンプレートなどのガイド付き検索オブジェクトの存在を確認します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>厳密なテンプレート構文チェックの強制 </p> </td> 
      <td colname="col2"> <p>テンプレートバリデーターをより厳密にし、不平衡な引用符や&lt;&gt;記号などをチェックできるようにします。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>アカウント番号 </p> </td> 
      <td colname="col2"> <p>アカウント番号は編集できません。 これは表示の目的でのみ使用します。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Save Changes]**.

## Adobe CQ5との統合の設定{#task_EA2FC2C24960498DAE01A1AB769D2F14}

サイト検索/マーチャンダイジングとAdobe CQ5の統合を設定できます。

**Adobe CQ5との統合を設定するには**

1. 次の手順を実行して、メンバーIDとアカウントIDを取得します。

   * サイトの検索/マーチャンダイジングアカウントにログインします。
   * URLパスで、メンバーIDとアカウントIDをコピーします。

      例えば、アカウントへのURLパスが`https://searchandpromote.mycompany.com/px/home/?sp_id=00123a4b-sp1234a5b6`の場合、メンバーIDは`00123a4b`、アカウントIDは`sp1234a5b6`になります。

1. Adobe CQ5では、「Cloud Services」タブを使用して、サイトの検索とマーチャンダイジングの設定を作成します。

   それぞれの設定で、コピーしたメンバーIDとアカウントIDを使用します。

## マーチャンダイジングの環境設定{#task_7AC7B9F5D9F44E10AB5BC0B8CB31C37A}

デフォルトのルールビルダーやデフォルトの検索語句など、マーチャンダイジングの環境設定を管理します。

**マーチャンダイジングの環境設定を指定するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Account Options]**/**[!UICONTROL Merchandising Preferences]**&#x200B;をクリックします。
1. [!DNL Merchandising Preferences]ページで、必要なオプションを設定します。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>トリガー群優性閾値 </p> </td> 
      <td colname="col2"> <p> 「アカウントのデフォルトを使用」を指定する、「グループ優先」の結果ベースのトリガーに適用するしきい値の割合。 </p> <p>この設定を変更すると、直ちにライブ検索に影響を与える可能性があるので、注意が必要です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>グループ定義 </p> </td> 
      <td colname="col2"> <p>マーチャンダイジングコンソールのグループの結果数。 最大50,000件。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> 「マーチャンダイジングドキュメントID」(MDI)フィールド </p> </td> 
      <td colname="col2"> <p> 指定するフィールドは、「単一の結果」の結果ベースのトリガーとアクションを使用して操作する検索結果を「一意に」修飾する必要があります。 </p> <p>事前定義URLフィールドの使用は、場合によっては機能しますが、お勧めしません。 各ページに固有のIDを持つユーザー定義のメタフィールド（SKUやproduct_idなど）は、「URL」フィールドを使用するよりも効率的です。 「none」を指定すると、ルールマネージャーの「single result」結果ベースのトリガーとアクションが無効になります。 このオプションの変更は、今後保存されるルールにのみ適用されます。既存のルールは、元々保存されたMDIを引き続き使用します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>デフォルトのVRB(Visual Rule Builder)検索語句 </p> </td> 
      <td colname="col2"> <p> Visual Rule Builderで使用される最初の検索用語をカスタマイズできます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>VRB既定の検索 </p> </td> 
      <td colname="col2"> <p>この設定を使用すると、Visual Rule Builderで最初に選択されるデフォルトの検索を設定できます。 </p> <p> この設定は、複数の検索を含む導入でのみ有効です。 VRBを使用すると、定義したグループが適用するトリガーまたはアクションの検索対象を選択できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>VRB/シミュレータのタイムアウト </p> </td> 
      <td colname="col2"> <p>VRBおよびシミュレーターは、実稼動検索よりも低速なプロキシサーバーを通じて検索を送信します。 アセットの読み込みの遅さなど、特定の状況では、VRBまたはシミュレーターがタイムアウトする場合があります。 ユーザーインターフェイスが停止するまで待機する秒数は、増減できます。 この設定をデフォルトの60から増やす必要はほとんどありません。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Save Changes]**.

## AdobeのDynamic Mediaクラシックアカウントへのアクセスを設定する{#task_CEFF88C2033D41D0B2FE86C435EDAC6D}

サイト検索/マーチャンダイジングアカウントをAdobeDynamic Mediaクラシックにリンクすると、Adobe Scene7からアップロードしたデジタルアセットを使用して、Webサイトにバナー広告を簡単に追加できます。

[バナーについて](../c-about-design-menu/c-about-banners.md#concept_5BBE01FEC6134393B43CC917C8CC64DA)を参照してください。

「AdobeDynamic Mediaクラシック](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3)を使用したバナーの追加」を参照してください。[

**AdobeのDynamic Mediaクラシックアカウントへのアクセスを設定するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Account Options]**/**[!UICONTROL Scene7 Configuration]**&#x200B;をクリックします。
1. [!DNL Scene7 Configuration]ページで、必要なオプションを設定します。

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
      <td colname="col2"> <p>必須。Dynamic Mediaクラシックアカウントが様々なDynamic Mediaクラシックサーバにアクセスする世界の地域を示します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>デフォルト会社 </p> </td> 
      <td colname="col2"> <p>Dynamic Mediaクラシックアカウントに関連付けられている会社の名前を示します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> 電子メール </p> </td> 
      <td colname="col2"> <p>必須。Dynamic Mediaクラシックのログインと通信に使用する電子メールアドレスを識別します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Password </p> </td> 
      <td colname="col2"> <p>必須。Dynamic Mediaクラシックログインパスワード。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>有効 </p> </td> 
      <td colname="col2"> <p>サイト検索/マーチャンダイジング内のすべてのDynamic Mediaクラシックコントロールを有効にします。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>テスト </p> </td> 
      <td colname="col2"> <p>Dynamic Mediaクラシック地域名、電子メールアドレス、パスワードの詳細が正しいことを確認します。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. （オプション）**[!UICONTROL Test]**&#x200B;をクリックして、Dynamic Mediaクラシック地域名、電子メールアドレス、パスワードの詳細が正しいことを確認します。
1. クリック **[!UICONTROL Save Changes]**.

## Adobe Analyticsリダイレクターの設定{#task_2C9DE333FD7246E4A460FC0F55204160}

サイト訪問者の追跡に[!DNL Adobe Analytics]を使用する場合、サイト検索/マーチャンダイジングで[!DNL Adobe Analytics Redirector]を使用して、[!DNL Adobe Analytics]ですべてのHTTPリダイレクトを追跡できます。

**Adobe Analyticsリダイレクターを設定するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Account Options]**/**[!UICONTROL Adobe Analytics Redirector]**&#x200B;をクリックします。
1. [!DNL Adobe Analytics Redirector]ページで、必要なオプションを設定します。

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
      <td colname="col2"> <p>Adobe AnalyticsとのHTTPリダイレクトの追跡をオンにします。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>トラッキングサーバー </p> </td> 
      <td colname="col2"> <p> Adobe Analyticsトラッキングサーバー名を識別します。 </p> <p>トラッキングサーバー名を調べるには、 </p> <p> 
      <ol id="ol_D17B77E81F8D40D0948415CD60839BE3"> 
      <li id="li_BE58DBA104D44F0DB6C64AD3F12CEA97"> Adobe Analyticsで、<span class="uicontrol">管理者</span> &gt; <span class="uicontrol">Admin Console</span> &gt; <span class="uicontrol">コードマネージャー</span>の順にクリックします。 </li> 
      <li id="li_67A93D17C3A14874928C6DC4FF2D4784"> 「<span class="wintitle">オプション</span>」グループボックスで、それぞれのドロップダウンリストからレポートスイートを選択します。 </li> 
      <li id="li_5AAB004AC58441DBB0F813BDE30EFFD4"> 「<span class="uicontrol">コードの生成</span>」をクリックします。 </li> 
      <li id="li_E80368993F4D4DD69E37509FF4348B36"> <span class="wintitle">コードマネージャー</span>ページで、「<span class="uicontrol">コアJavaScriptファイル」タブ</span>をクリックします。 </li> 
      <li id="li_991BDCDDA41A445F85CEEAAE9A46A304"> <span class="wintitle"> Config Section </span>で、次の行を探します。 <p> <code> s.trackingServer="yourcompany.122.2o7.net" </code> </p> <p>トラッキングサーバー名（この場合）は<span class="codeph"> "yourcompany.122.2o7.net" </span>です。 </p> </li> 
      </ol> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>レポートスイート ID </p> </td> 
      <td colname="col2"> <p> レポートスイートIDを識別します。 </p> <p>レポートスイートIDを調べるには、 </p> <p> 
      <ol id="ol_4FD7B2459358486DBDB130426131D16A"> 
      <li id="li_9AF624CEB128453C808892EEE385D5D1"> Adobe Analyticsで、<span class="uicontrol">管理者</span>/<span class="uicontrol">Admin Console</span>/<span class="uicontrol">レポートスイート</span>をクリックします。 </li> 
      <li id="li_AAC47EAA04144A67BDCB5C7B8D8098E9"> 表の<span class="wintitle">レポートスイートID </span>列を見て、IDを探します。 </li> 
      </ol> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>カスタムパラメーター </p> </td> 
      <td colname="col2"> <p>Adobe AnalyticsのリダイレクトURLにカスタムパラメーターを追加できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>すべてのカスタム値の大文字と小文字を </p> </td> 
      <td colname="col2"> <p>上記で指定したカスタムパラメータ値に使用する大文字と小文字の区別を標準化できます。 Adobe Analyticsでは大文字と小文字が区別されるので、値の大文字と小文字を統一する理由があります。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。
1. （オプション）[!DNL Adobe Analytics Redirector]ページで、次のいずれかの操作を行います。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## ルートファイルの設定{#task_5F175C8743FB49A2A003813CBF7C56BF}

Webサイトのルートフォルダーにあるルートファイルを管理します。

**ルートファイルを設定するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Account Options]**/**[!UICONTROL Root Files]**&#x200B;をクリックします。
1. [!DNL Root Files]ページで、アップロードするルートファイルを参照します。

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
      <td colname="col2"> <p>Webサイトで利用可能なすべてのページのリストを含むXMLファイルです。 </p> </td> 
    </tr> 
    <tr> 
      <td colname="col1"> <p>crossdomain.xml </p> </td> 
      <td colname="col2"> <p>Flash Playerが複数のドメインにまたがるファイルにアクセスすることを許可または禁止します。 </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。
1. （オプション）[!DNL Root Files]ページで、次のいずれかの操作を行います。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 別のアカウントユーザー{#task_47E3C66CC6374274830DA10171E0CF17}にアカウント所有権を転送しています

アカウントの所有者は、ログインをキャンセルする場合、まず所有権を別のアクティブなアカウントユーザーに転送する必要があります。 [!DNL Transfer Ownership]を使ってこのタスクを達成できます。

所有権は、既存のサイト検索/マーチャンダイジングアカウントユーザーに転送できます。

所有権の移転が完了すると、新しいアカウントの所有者は電子メール通知を受け取り、元の所有者はその職位の制限や責任を解除される。

アカウントごとに所有者は1人しかありません。 自分の所有権を別のユーザーに移すと、所有権権限は失われます。

[ログインのキャンセル](../c-about-settings-menu/c-about-my-profile-menu.md#task_D57701BB726243B08CEA14EEC86C3087)を参照してください。

「[アカウントの削除](../c-about-settings-menu/c-about-account-options-menu.md#task_975178D5B9444BF8B52D72B897A49C32)」を参照してください。

[アカウントから自分を削除する](../c-about-settings-menu/c-about-account-options-menu.md#task_C56F5AB87B664BAAAC2FD2F15003E73F)を参照してください。

**アカウント所有権を別のアカウントに転送するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Account Options]**/**[!UICONTROL Transfer Ownership]**&#x200B;をクリックします。
1. [!DNL Transfer Ownership]ページで、アカウントの所有権を取得するユーザーをクリックします。
1. クリック **[!UICONTROL Transfer]**.

## アカウントの削除{#task_975178D5B9444BF8B52D72B897A49C32}

アカウントは、サイト検索/マーチャンダイジングから完全に削除できます。 削除すると、自分および自分のアカウントの他のユーザは、そのアクセス権を持ちません。

アカウントを削除すると、そのアカウントを使用して本番用サイトのインデックスを作成したり、検索したりすることはできなくなります。 また、

他のユーザーがこのアカウントを引き続き使用できるようにするには、別のユーザーに所有権を移譲し、自分をアカウントのユーザーとして削除します。

「[アカウント所有権の別のアカウントユーザーへの移行](../c-about-settings-menu/c-about-account-options-menu.md#task_47E3C66CC6374274830DA10171E0CF17)」を参照してください。

他のアカウントがある場合は、現在のアカウントを削除すると、ログインに表示されている最初のアカウントに移動します。

[アカウントから自分を削除する](../c-about-settings-menu/c-about-account-options-menu.md#task_C56F5AB87B664BAAAC2FD2F15003E73F)を参照してください。

[ログインのキャンセル](../c-about-settings-menu/c-about-my-profile-menu.md#task_D57701BB726243B08CEA14EEC86C3087)を参照してください。

**アカウントを削除するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Account Options]**/**[!UICONTROL Remove Account]**&#x200B;をクリックします。
1. （オプション）[!DNL Reason for Removal]フィールドに、アカウント削除の理由を入力します。
1. クリック **[!UICONTROL Remove Account]**.

## アカウントから自分を削除する{#task_C56F5AB87B664BAAAC2FD2F15003E73F}

サイト検索/マーチャンダイジングアカウントから自分を削除できます。

アカウントから自分を削除すると、そのアカウントにアクセスできなくなり、アカウント設定を編集したり、サイトのインデックスを作成したりすることはできません。

アカウントに再度アクセスできるようにするには、現在のアカウントユーザーに元に戻すように依頼します。

[ログインのキャンセル](../c-about-settings-menu/c-about-my-profile-menu.md#task_D57701BB726243B08CEA14EEC86C3087)を参照してください。

「[アカウントの削除](../c-about-settings-menu/c-about-account-options-menu.md#task_975178D5B9444BF8B52D72B897A49C32)」を参照してください。

「[アカウント所有権の別のアカウントユーザーへの移行](../c-about-settings-menu/c-about-account-options-menu.md#task_47E3C66CC6374274830DA10171E0CF17)」を参照してください。

**アカウントから自分を削除するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Account Options]**/**[!UICONTROL Remove Yourself]**&#x200B;をクリックします。
1. クリック **[!UICONTROL Remove Yourself]**.
