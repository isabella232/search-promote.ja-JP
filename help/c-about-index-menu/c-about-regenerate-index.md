---
description: 「インデックスを再生成」を使用すると、サイトを再クロールすることなく、Webサイトのインデックスを更新できます。
solution: Target
subtopic: Regenerate Index
title: インデックスの再生成について
topic-legacy: Index,Site search and merchandising
uuid: 9d1f1d88-0453-4422-a625-a348febbf224
exl-id: 4155a52c-33f6-4f54-b69b-2a092530f7aa
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# インデックスの再生成{#about-regenerate-index}について

[!DNL Regenerate Index]を使用すると、サイトを再クロールすることなくWebサイトのインデックスを更新できます。

## インデックスの再生成を使用{#concept_6CBE6B8D18EF47D293091CBA542245FA}

このオプションは、次のアカウントオプションに変更を加えたときにいつでも使用できます。

* 単語と言語
* 除外された単語
* 同義語
* メタデータフィールドを削除する場合、フィールド名、データ型、日付形式、並べ替え順、最小または最大ランク値、デフォルトランク値、リストタイプ、リスト区切り文字などのメタデータ設定。

更新されたアカウントオプション情報は、新しいサイトインデックスの生成に使用されます。 「再生成」を使用すると、サイトインデックスをすばやく効率的に変更できます。

デフォルトでは、新しいWebサイトのコンテンツや変更されたWebサイトのコンテンツは、インデックスに含まれません。 このようなコンテンツを含めるには、フルインデックスまたはインクリメンタルインデックスを実行します。

[ライブまたはステージングされたWebサイトの完全なインデックスの実行も参照してください…](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

[ライブまたはステージングされたWebサイトの増分インデックスの実行も参照してください…](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## ライブまたはステージングされたWebサイトのインデックスの再生成{#task_B28DE40C0E9A475ABCBCBC4FF993AACD}

[!DNL Regenerate Index]を使用すると、サイトを再読み込みすることなく、Webサイトのインデックスを更新できます。

**ライブまたはステージングされたWebサイトのインデックスを再生成するには**

1. 製品メニューで、次のいずれかの操作を行います。

   * **[!UICONTROL Index]**/**[!UICONTROL Regenerate Index]**/**[!UICONTROL Live Regenerate]**&#x200B;をクリックします。

   * **[!UICONTROL Index]**/**[!UICONTROL Regenerate Index]**/**[!UICONTROL Staged Regenerate]**&#x200B;をクリックします。

1. [!DNL Regenerate]ページで、**[!UICONTROL Regenerate Index Now]**&#x200B;をクリックします。
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL Live Regenerate]**&#x200B;の実行を選択した場合は、**[!UICONTROL View Last Crawl]**&#x200B;をクリックして、実行された最後のライブインデックスの再生成に関するパフォーマンス統計を確認します。

   * インデックスの再生成中に&#x200B;**[!UICONTROL Stop Regenerate Now]**&#x200B;をクリックして、インデックス再生成処理を停止します。
   * インデックスの再生成中に、**[!UICONTROL Restart Regenerate Now]**&#x200B;をクリックしてインデックス再生成処理を最初から再開します。
   * ステージングされた再生成の後にインデックスエラーが発生した場合は、**[!UICONTROL View Errors]**&#x200B;をクリックして関連するログを表示します。

## ライブまたはステージングされたWebサイトの再生成されたインデックスログの表示{#task_61CE8F9E7BF84BA89A8D482B2106BB15}

ライブインデックスの再生成またはステージングされたインデックスの再生成が完了した場合、関連するログを表示して、発生したエラーのトラブルシューティングを行うことができます。

ログをエクスポートしたり、保存したりすることはできません。 ただし、新しいインデックスが発生するまで、ログは引き続き閲覧可能です。

**ライブまたはステージングされたWebサイトの再生成されたインデックスログを表示するには**

1. 製品メニューで、次のいずれかの操作を行います。

   * **[!UICONTROL Index]**/**[!UICONTROL Regenerate Index]**/**[!UICONTROL Live Log]**&#x200B;をクリックします。

   * **[!UICONTROL Index]**/**[!UICONTROL Regenerate Index]**/**[!UICONTROL Staged Log]**&#x200B;をクリックします。

1. ログページの上部または下部で、次のいずれかの操作を行います。

   * **[!UICONTROL First]**、**[!UICONTROL Prev]**、**[!UICONTROL Next]**、**[!UICONTROL Last]**、または&#x200B;**[!UICONTROL Go to line]**&#x200B;のナビゲーションオプションを使用してログ内を移動します。

   * 表示オプション&#x200B;**[!UICONTROL Errors only]**、**[!UICONTROL Wrap line]**、または&#x200B;**[!UICONTROL Show]**&#x200B;を使用して、表示内容を絞り込みます。
