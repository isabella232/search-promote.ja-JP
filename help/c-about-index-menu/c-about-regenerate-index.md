---
description: 「インデックスを再生成」を使用すると、サイトを再クロールすることなく、Webサイトのインデックスを更新できます。
seo-description: 「インデックスを再生成」を使用すると、サイトを再クロールすることなく、Webサイトのインデックスを更新できます。
seo-title: インデックスの再生成について
solution: Target
subtopic: Regenerate Index
title: インデックスの再生成について
topic: Index,Site search and merchandising
uuid: 9d1f1d88-0453-4422-a625-a348febbf224
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# インデックスの再生成について{#about-regenerate-index}

を使用すると、サ [!DNL Regenerate Index] イトを再クロールする必要なく、Webサイトのインデックスを更新できます。

## インデックスの再生成の使用 {#concept_6CBE6B8D18EF47D293091CBA542245FA}

このオプションは、次のアカウントオプションを変更する際に使用できます。

* 単語と言語
* 除外された単語
* 同義語
* メタデータフィールドの削除、フィールド名、データ型、日付形式、並べ替え順、最小または最大ランク値、デフォルトのランク値、リストの種類、リストの区切り文字の変更など、メタデータの設定。

更新されたアカウントオプション情報は、新しいサイトインデックスの生成に使用されます。 「再生成」を使用すると、サイトのインデックスを迅速かつ効率的に変更できます。

デフォルトでは、新規または変更されたWebサイトのコンテンツはインデックスに含まれません。 このようなコンテンツを含めるには、完全インデックスまたは増分インデックスを実行します。

ライブまたはステ [ージングされたWebサイトの完全なインデックスの実行も参照してください。](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

ライブまたはス [テージングされたWebサイトの増分インデックスの実行も参照してください。](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## ライブまたはステージWebサイトのインデックスの再生成 {#task_B28DE40C0E9A475ABCBCBC4FF993AACD}

を使用すると、サ [!DNL Regenerate Index] イトを再読み込みすることなく、Webサイトのインデックスを更新できます。

**ライブまたはステージングされたWebサイトのインデックスを再生成するには**

1. 製品メニューで、次のいずれかの操作を行います。

   * Click **[!UICONTROL Index]** > **[!UICONTROL Regenerate Index]** > **[!UICONTROL Live Regenerate]**.

   * Click **[!UICONTROL Index]** > **[!UICONTROL Regenerate Index]** > **[!UICONTROL Staged Regenerate]**.

1. ページ上で、 [!DNL Regenerate] をクリックしま **[!UICONTROL Regenerate Index Now]**&#x200B;す。
1. （オプション）次のいずれかの操作を行います。

   * 実行を選択した場合は、をクリ **[!UICONTROL Live Regenerate]**&#x200B;ックして、実 **[!UICONTROL View Last Crawl]** 行された最後のライブインデックスの再生成に関するパフォーマンス統計を確認します。

   * インデックスの再生成中に、をクリックし **[!UICONTROL Stop Regenerate Now]** てインデックスの再生成処理を停止します。
   * インデックスの再生成中に、をクリックし **[!UICONTROL Restart Regenerate Now]** て、インデックスの再生成処理を最初から再開します。
   * ステージング再生後にインデックスエラーが発生した場合は、をクリックし **[!UICONTROL View Errors]** て関連するログを表示します。

## ライブまたはステージングされたWebサイトの再生成されたインデックスログの表示 {#task_61CE8F9E7BF84BA89A8D482B2106BB15}

ライブインデックスの再生成またはステージングインデックスの再生成が完了すると、関連するログを表示して、発生したエラーのトラブルシューティングを行うことができます。

ログをエクスポートしたり、保存したりすることはできません。 ただし、新しいインデックスが発生するまで、ログは引き続き表示できます。

**ライブまたはステージングされたWebサイトの再生成されたインデックスログを表示するには**

1. 製品メニューで、次のいずれかの操作を行います。

   * Click **[!UICONTROL Index]** > **[!UICONTROL Regenerate Index]** > **[!UICONTROL Live Log]**.

   * Click **[!UICONTROL Index]** > **[!UICONTROL Regenerate Index]** > **[!UICONTROL Staged Log]**.

1. ログページの上部または下部で、次のいずれかの操作を行います。

   * ナビゲーションオプシ **[!UICONTROL First]**&#x200B;ョン、、、、 **[!UICONTROL Prev]**&#x200B;また **[!UICONTROL Next]**&#x200B;はを使 **[!UICONTROL Last]**&#x200B;用して **[!UICONTROL Go to line]** ログ内を移動します。

   * 表示オプション、または **[!UICONTROL Errors only]**&#x200B;を使用 **[!UICONTROL Wrap line]**&#x200B;して、 **[!UICONTROL Show]** 表示内容を調整します。

