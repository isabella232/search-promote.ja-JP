---
description: 再ランクインデックスを使用すると、サイトを再読み込みすることなく、サイトのランク付け情報を更新できます。
solution: Target
subtopic: Re-Rank Index
title: 再ランクインデックスについて
topic-legacy: Index,Site search and merchandising
uuid: 5c2a4c12-5e06-4fcc-897c-c12fcc5d7aa8
exl-id: c4ddaec9-43ba-42ec-89dc-04d42306b9b6
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---

# 再ランクインデックスについて{#about-re-rank-index}

[!DNL Re-Rank Index]を使用すると、サイトを再読み込みすることなく、サイトのランク付け情報を更新できます。

## 再ランクインデックスの使用{#concept_147B0A9FCD51451787DA898E06F7C692}

このオプションは、特定のアカウントのランク設定を変更したときにいつでも使用できます。 更新されたアカウントオプション情報は、新しいサイトのランキングデータを生成するために使用されます。 「再ランク」を使用すると、サイトのランクをすばやく効率的に変更できます。

デフォルトでは、新しいWebサイトのコンテンツや変更されたWebサイトのコンテンツは、インデックスに含まれません。 このようなコンテンツを含めるには、フルインデックスまたはインクリメンタルインデックスを実行します。

[ライブまたはステージングされたWebサイトの完全なインデックスの実行を参照してください…](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

[ライブまたはステージングされたWebサイトの増分インデックスの実行を参照してください…](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## ライブまたはステージングされたWebサイトのインデックスの再ランキング{#task_02E190CF700742FEACAFFD5986B0353A}

[!DNL Re-Rank Index]を使用すると、サイトを再読み込みすることなく、サイトのランク付け情報を更新できます。

**ライブWebサイトまたはステージングされたWebサイトのインデックスの再ランク付けを行うには**

1. 製品メニューで、次のいずれかの操作を行います。

   * **[!UICONTROL Index]**/**[!UICONTROL Re-Rank Index]**/**[!UICONTROL Live Re-Rank]**&#x200B;をクリックします。

   * **[!UICONTROL Index]**/**[!UICONTROL Re-Rank Index]**/**[!UICONTROL Staged Re-Rank]**&#x200B;をクリックします。

1. [!DNL Re-Rank]ページで、**[!UICONTROL Re-Rank Now]**&#x200B;をクリックします。
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL Live Re-Rank]**&#x200B;の実行を選択した場合は、**[!UICONTROL View Last Crawl]**&#x200B;をクリックして、実行された最後のライブインデックスの再ランキングのパフォーマンス統計を確認します。

   * 再ランク付けの処理中に、**[!UICONTROL Stop Re-Rank Now]**&#x200B;をクリックして、インデックスの再ランク付け処理を停止します。
   * ステージングされたWebサイトの再ランク付けの後にインデックスエラーが発生した場合は、**[!UICONTROL View Errors]**&#x200B;をクリックして関連するログを表示します。

## ライブWebサイトまたはステージングされたWebサイトの再ランク付けインデックスログの表示{#task_3C76107DFAC1495FACD3ABB0A688208D}

ライブインデックスの再ランク付けまたはステージングされたインデックスの再ランク付けが完了した場合、関連するログを表示して、発生したエラーのトラブルシューティングを行うことができます。

ログをエクスポートしたり、保存したりすることはできません。 ただし、新しいインデックスが発生するまで、ログは引き続き閲覧可能です。

**ライブWebサイトまたはステージングされたWebサイトの再ランクインデックスログを表示するには**

1. 製品メニューで、次のいずれかの操作を行います。

   * **[!UICONTROL Index]**/**[!UICONTROL Re-Rank Index]**/**[!UICONTROL Live Log]**&#x200B;をクリックします。

   * **[!UICONTROL Index]**/**[!UICONTROL Re-Rank Index]**/**[!UICONTROL Staged Log]**&#x200B;をクリックします。

1. ログページの上部または下部で、次のいずれかの操作を行います。

   * **[!UICONTROL First]**、**[!UICONTROL Prev]**、**[!UICONTROL Next]**、**[!UICONTROL Last]**、または&#x200B;**[!UICONTROL Go to line]**&#x200B;のナビゲーションオプションを使用してログ内を移動します。

   * 表示オプション&#x200B;**[!UICONTROL Errors only]**、**[!UICONTROL Wrap line]**、または&#x200B;**[!UICONTROL Show]**&#x200B;を使用して、表示内容を絞り込みます。
