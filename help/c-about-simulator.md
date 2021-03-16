---
description: シミュレーターを使用して、現在ステージングされているライブ上の項目をすべてプッシュした場合の検索結果を確認します。
solution: Target
title: シミュレーターについて
topic: シミュレータ，サイト検索とマーチャンダイジング
uuid: 7ec8f5b9-3ab3-4b9a-bf8a-65d0ca1dfddb
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 1%

---


# シミュレーターについて{#about-simulator}

シミュレーターを使用して、現在ステージングされているライブ上の項目をすべてプッシュした場合の検索結果を確認します。

## シミュレーターについて{#concept_020AA6751E32421A96A3455508364C7E}

シミュレーターを使用して、現在ステージングされているライブ上の項目をすべてプッシュした場合の検索結果を確認します。

また、現在のライブ検索を比較の目的でシミュレートすることもできます。 シミュレーターには組み込みデバッガーがあり、特定の検索で実行されるビジネスルールを示します。 関連付けられたルールのチェックを外すと、シミュレーターは、そのルールが存在しないかのようにサイトの検索を再シミュレートします。 ルールは、優先度が最も高いものから最も低いものへと順に表示され、優先度が高いものは、優先度が低いものから順に表示されます。

「[新しいビジネスルールの追加](c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7)」も参照してください。

## シミュレーターの使用{#task_739E14F61F8D47B196515F815E3F3BD9}

シミュレーターを使用して、現在ステージングされているすべての項目をライブにプッシュした場合の検索結果を確認できます。

「[新しいビジネスルールの追加](c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7)」を参照してください。

**シミュレーターを使用するには**

1. 製品メニューで&#x200B;**[!UICONTROL Simulator]**&#x200B;をクリックします。
1. **[!UICONTROL Options]**&#x200B;ドロップダウンリストで、実行するオプションを選択します。

   <!-- 
   
   r_simulator_page_options.xml
   
   -->

   （オプション）シミュレーターページの表のチェックボックス列を使用して、シミュレーション内の特定のルールのオン/オフを切り替えます。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p><span class="uicontrol">ステージング/シミュレーションライブ</span> </p> </td> 
      <td colname="col2"> <p>ライブ環境をシミュレートするか、ステージ環境をシミュレートするかを切り替えます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p><span class="uicontrol">処理ルールの表示/非表示</span> </p> </td> 
      <td colname="col2"> <p>ビジネスルールだけでなく、実行されたすべての処理ルールを表示または非表示にします。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p><span class="uicontrol">シミュレーション日の変更</span> </p> </td> 
      <td colname="col2"> <p>指定した日付の検索結果をシミュレートします。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p><span class="uicontrol">PCでシミュレート</span> </p> </td> 
      <td colname="col2"> <p>パソコンを使っているかのように検索結果をシミュレートする。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p><span class="uicontrol">モバイルでシミュレート</span> </p> </td> 
      <td colname="col2"> <p>携帯電話やタブレットを使用している場合と同じように、検索結果をシミュレートします。 </p> <p>このオプションを選択すると、次の関連するオプションから選択できます。 </p> 
        <ul id="ul_2A9901418212486A8EE67A78CB99CBE4"> 
        <li id="li_B210E954DF0D44C397718112C72C2103"> <b><span class="uicontrol">デバイス</span></b> <p>携帯電話やタブレットでの検索結果をシミュレートする。 </p> </li> 
        <li id="li_90B64EAA0B57446A90CE22172E703594"> <b><span class="uicontrol">解像度</span></b> <p>選択したデバイスに基づいて、関連する解像度を選択できます。 </p> </li> 
        <li id="li_042AF9FA3FA846EDB48F7296DB361515"> <b><span class="uicontrol">水平表示</span></b> <p>選択したデバイス上でシミュレートされた検索結果が水平方向にどのように表示されるかを表示します。 </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

1. Webサイトの検索機能を使用して、現在の設定とアクティブなルールに基づいて検索結果をテストします。 必要に応じて、ルールと設定を調整し、目的の結果を得ます。
