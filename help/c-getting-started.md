---
description: Search&Promoteおよび動的なナビゲーションを初めて使用する場合は、ここに開始してアカウントを使用してください。 特に、Webサイトのインデックスを作成し、検索結果のルック&フィールをカスタマイズする方法について学びます。
solution: Target
title: 導入
topic: はじめに，サイト検索とマーチャンダイジング
uuid: 816ad003-15c9-4e44-b09d-cab284518634
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 0%

---


# 導入{#getting-started}

Search&amp;Promoteおよび動的なナビゲーションを初めて使用する場合は、ここに開始してアカウントを起動して実行してください。 特に、Webサイトのインデックスを作成し、検索結果のルック&amp;フィールをカスタマイズする方法について学びます。

## アカウントの設定{#section_FD4C71A422BD4ACEA51AFC98CDD3211C}

アカウントのカスタマイズを開始する前に、最初に割り当てられたパスワードを変更します。

[ログインパスワードの変更](c-about-settings-menu/c-about-my-profile-menu.md#task_F5FF13AAD1514FE997C8882D4537C0C9)を参照してください。

また、文字セットのエンコーディング、連絡先情報、電子メールアドレス、環境設定などの個人設定を追加または編集する必要があります。

[個人ユーザー情報の設定](c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)を参照してください。

「[環境設定の設定](c-about-settings-menu/c-about-my-profile-menu.md#task_5E06BF565C284C2EBBE18E10A1C4BFBB)」を参照してください。

個人設定を終了したら、アカウント全体の設定を開きます。

「[アカウント設定の指定](c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)」を参照してください。

アカウント名とWebサイトのアドレスを確認し、レポートやスケジュールに使用するタイムゾーンを選択します。 入力するWebサイトアドレスは、サイトのメインサイト「入口」です。 エントリポイントより下のすべてのページが、指定されたURLに直接または間接的にリンクされている場合は、クロールされ、インデックスが作成されます。 例えば、エントリポイントが`https://www.mysite.com/`の場合、`https://www.mysite.com/news/04.html`ページがメインの`index.html`ページからリンクされているか、そのインデックスからリンクされているページかは、インデックスが作成されます。 Webサイトに、2番目のドメインのページなど、メインエントリポイントからリンクされていないセクションが含まれている場合は、追加のURL入力ポイントを指定できます。

[インデックスを作成する複数のURLエントリポイントの追加](c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)を参照してください。

## Webページへの検索フォームコードのサンプルの追加{#section_2BC00BE7D81245188E4A89E09D41D387}

これで、検索コードをWebページに追加する準備が整いました。 標準の検索フォーム用にサンプルフォームコードが用意されています。

[検索フォームが表示される状態をプレビューするを参照してください…](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

[検索フォームのHTMLコードを](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

検索フォームを表示したい場所に、コードをコピーしてWebページに貼り付けます。 例えば、多くのWebサイトでは、ホームページ上やナビゲーションフレーム内にフォームが配置されます。 デザインやコンテンツのニーズに合わせてフォームコードを編集したり、検索パラメーターを追加したりできます。

## 検索結果リンクのカスタマイズ{#section_0B4E2D6E1A3E4D3FBDBB607260CDB111}

オプションで、検索結果のリンク、背景色およびヘッダー情報をカスタマイズできます。

[テンプレートについて](c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5)を参照してください。

「[新しいプレゼンテーションまたはトランスポートテンプレートファイルの追加](c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)」を参照してください。

「[プレゼンテーションまたはトランスポートテンプレートの編集](c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)」を参照してください。

テンプレートの外観が完成したら、変更を保存し、**[!UICONTROL Push Live]**&#x200B;をクリックします。

[ライブまたはステージングされたWebサイトの完全なインデックスの実行を参照してください…](c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

## Webサイトのインデックス作成{#section_6BBD16929CF04CB2A78BD657681C06B8}

アカウントを初めて作成するときに、Webサイトのインデックスが作成されます。 ただし、新しいコンテンツを追加した場合や既存のコンテンツを編集した場合は、Webサイトのインデックスを再作成します。

[ライブまたはステージングされたWebサイトの完全なインデックスの実行を参照してください…](c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

また、定期的なインデックス時間をスケジュールすることもできます。

「[ライブWebサイトのフルインデックススケジュールの設定](c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0)」を参照してください。

[ライブまたはステージングされたWebサイトの増分インデックスの実行を参照してください…](c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

Webサイトのサイズが大きい場合や、頻繁に変更されるページのみを再インデックスする場合は、を設定し、インクリメンタルインデックスを実行します。

「[ステージングされたWebサイトの増分インデックスの設定](c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。

[ライブまたはステージングされたWebサイトの増分インデックスの実行を参照してください…](c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

ログインしなくても増分インデックスを実行するには、スクリプト化されたインデックスを作成します。

「[スクリプト増分インデックスの設定](c-about-index-menu/c-about-scripted-index.md#task_05AE040FE75E40FFAA5E10B6B6D4D255)」を参照してください。

または、スクリプトを使用して、インデックス作成のためのリモート要求を渡すこともできます。

[インデックス作成のためのリモートコントロールの構成](c-about-index-menu/c-about-remote-control-for-indexing.md#task_57C296258404448DA7A5ADC9B7232391)を参照してください。

## 検索語レポートの表示{#section_1F4A7F57B9C64FBDA5E3E592621BF6F4}

訪問者の検索クエリがログに記録され、日、週、月ごとにレポートが作成されます。 これらのクエリを使用すると、顧客が何を探しているか、成功した頻度、Webサイトのナビゲーションの内訳を表示できます。

[キーワードレポートまたはNULL検索キーワードレポートの表示を参照してください。](c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

## 検索エクスペリエンスをカスタマイズする高度なタスク{#section_036286EC316F47C89D0D50C2D061BB59}

顧客の検索操作を完全にカスタマイズおよび制御できる追加のオプションが多数あります。

* サイトのどの部分のインデックスが作成され、作成されない部分のインデックスがURLマスクで作成されるかを制御します。

   [URLマスクについて](c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)を参照してください。
* 日付に基づいてファイルを含めるか除外します。

   [日付マスクについて](c-about-settings-menu/c-about-crawling-menu.md#concept_F4F1F58A646F4A86B8650EC46FDCEF66)を参照してください。
* WebサイトにPDFドキュメントまたはMP3ファイルやMicrosoft Officeファイルなどの他のコンテンツタイプが含まれるファイルが含まれる場合は、そのようなファイルのインデックスを作成するかどうかを選択できます。

   「[コンテンツタイプについて](c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07)」を参照してください。
* また、サイト検索/マーチャンダイジングがWebサイトのパスワードで保護された領域にアクセスして検索できるように、パスワードを指定することもできます。

   [パスワードについて](c-about-settings-menu/c-about-crawling-menu.md#concept_3EDBD731725D46B891F834D4472774DC)を参照してください。
* Webサイトのインデックス作成に使用する接続数を制御します。

   [接続について](c-about-settings-menu/c-about-crawling-menu.md#concept_E2F3B7E7521147479E5948A94BB3A40B)を参照してください。
* クロールして送信するフォームに関する情報を入力します。

   「[フォーム送信について](c-about-settings-menu/c-about-crawling-menu.md#concept_CADD5D7CF373497DAA6F8564D7BC8502)」を参照してください。
* 検索から、「a」や「the」などの共通語を除外します。

   [除外された単語について](c-about-linguistics-menu/c-about-excluded-words.md#concept_9DB67BD2F0DC43AC88741003D9F39812)を参照してください。
* 「ニュースセクション」や「旅行セクション」など、Webサイトの特定の領域を指定して検索します。

   [コレクションについて](c-about-settings-menu/c-about-searching-menu.md#concept_62E42ACE53D54EEE9273433B86259127)を参照してください。
* フレームセットで使用するように検索をカスタマイズします。

   [フォームでのフレームの使用](c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5)を参照してください。
* 検索を開始する場所を制御します。

   [制限](c-about-settings-menu/c-about-searching-menu.md#concept_B5B527E04EBF4E9AB5956EEF881DDBF1)についてを参照してください。
* テンプレートを内部的にテストする際に使用する値を指定します。

   [プレビュー](c-about-settings-menu/c-about-searching-menu.md#concept_DF293FD3B02C467F8842C8C21D62F294)についてを参照してください。
* メタデータオプションを使用すると、顧客が検索クエリを送信したときに考慮されるHTMLフィールドとメタフィールド(ドキュメントやキーワード本文など)の関連性をカスタマイズできます。 メタデータフィールドはカスタマイズおよび定義できます。

   [定義について](c-about-settings-menu/c-about-metadata-menu.md#concept_AE48035C210145169BE067D396975620)を参照してください。
* 定義済みのフィールドの内容を変更します。 例えば、「On Sale Now!」などの新しいコンテンツを追加できます。) を`desc` metaタグに追加します。 また、実際のWebページを変更せずに、無関係なコンテンツを削除することもできます。

   [インジェクションについて](c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5)を参照してください。

* **[!UICONTROL Settings]** > **[!UICONTROL Filtering]**&#x200B;と&#x200B;**[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]**&#x200B;のオプションを使用して、ページの内容を「書き換え」してからインデックスを作成します。

* 辞書を設定して、関連単語のグループ（購入、購入、調達など）を指定できます。 これらの関連語は、顧客の検索クエリがWebページで使用されている用語と完全に一致しない場合でも、関連する結果を返すのに役立ちます。 上記の例で使用されている同義語を使用して、顧客の検索クエリで「purchase」という語を含むページを返します。

   [辞書](c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034)についてを参照してください。

