---
description: 動的ファセットを使用して、検索時に新しい範囲の選択を自動的に作成します。 必要に応じて、各動的ファセットフィールドをAdobe Search&amp;Promoteアカウント内の最大1つのテーブル名に関連付けることができます。 検索時に、検索に関連する動的ファセットフィールドに対して、これらのテーブルの関係を適用します。
seo-description: 動的ファセットを使用して、検索時に新しい範囲の選択を自動的に作成します。 必要に応じて、各動的ファセットフィールドをAdobe Search&amp;Promoteアカウント内の最大1つのテーブル名に関連付けることができます。 検索時に、検索に関連する動的ファセットフィールドに対して、これらのテーブルの関係を適用します。
seo-title: 動的ファセットについて
solution: Target
subtopic: Navigation
title: 動的ファセットについて
topic: Design,Site search and merchandising
uuid: 1ea91c22-dcc2-4173-aa50-ce618ad0a99c
translation-type: tm+mt
source-git-commit: ffdec2cfcb30e733c664a7d1ca23868b7a9a9aa5

---


# 動的ファセットについて{#about-dynamic-facets}

動的ファセットを使用して、検索時に新しい範囲の選択を自動的に作成します。 必要に応じて、各動的ファセットフィールドをAdobe Search&amp;Promoteアカウント内の最大1つのテーブル名に関連付けることができます。 検索時に、検索に関連する動的ファセットフィールドに対して、これらのテーブルの関係を適用します。

## 動的ファセットの使用 {#concept_E65A70C9C2E04804BF24FBE1B3CAD899}

>[!NOTE]
>
>この機能は、ではデフォルトでは有 [!DNL Adobe Search&Promote]効になっていません。 お使いの機能を有効にするには、テクニカルサポートにお問い合わせください。

ダイナミックファセットを使用しない場合は、関連する属性を「スロット」にマージし、特定の検索で同種のスロットのみを表示する必要がありました。 つまり、「靴のサイズ」や「リングのサイズ」など、論理属性の値を1つだけ含めることができます。 この方法は、一意の属性の大きなセットを持つ十分な検索時パフォーマンスを提供しました。

ただし、動的なファセット設定を使用する場合、コア検索が効率的に追跡できるファセットの数に制限はありません。 数百もの動的ファセットを定義できます。このファセットから、特定の検索に対してコア検索が「トップの動的ファセット」を返すことができます。この場合、 `N``N` は通常、10 ～ 20以下のより小さな値です。 この方法により、属性をスロットする必要がなくなり、Webサイト全体の属性に対して一意の動的ファセットを作成できるようになりました。

## どのファセットを動的にする必要がありますか。 {#section_254EE034BCAD4250A5D09FBF6158C4A5}

Webサイト全体にわずかに入力され、検索のサブセットにのみ表示されるファセットは、動的にするには適しています。 例えば、「forefoot width」という名前のファセットは、靴やブーツを検索する場合にのみ設定できます。 一方、「Face Numeral Style」という別のファセットは、「Roman」と「Arabic」の値を指定できますが、このファセットは、時計や時計を検索する場合にのみ表示されます。

アカウントに多数のファセットがある場合は、検索パフォーマンスが向上し、すべての検索で可能なファセット全体を常に選択する代わりに、動的ファセットを使用できるようになります。 「SKU」や「ブランド」などの汎用ファセットは、通常、すべての検索結果と共に表示するのに適しているが、通常は動的ファセットとしては適していない。

## ファセットとメタタグフィールドとの関係 {#section_2869E5FCDA8B431A87BC6E5573F2B0A0}

ファセットは、メタタグフィールドの上に構築されます。 メタタグフィールドは、の低レベルのコア検索レイヤー機能で [!DNL Adobe Search&Promote]す。 一方、ファセットはGS（ガイド付き検索）の一部で、Adobe Search&amp;Promoteの高度なプレゼンテーションレイヤーです。 ファセットには独自のメタタグフィールドがありますが、メタタグフィールドはファセットに関する情報を何も知りません。 動的ファセットを設定する場合は、最初にファセットを追加し、次に、「動的ファセット」オプションを選択してメタタグフィールドを追加し、識別されたファセットを動的に設定します。

>[!NOTE]
>
>に「動的ファセット」設定はありませ **[!UICONTROL Design > Navigation > Facets]**&#x200B;ん。 ファセットを「動的」にするのは、基になる「メタタグフィールド」が、で設定した動的なものであるという点で **[!UICONTROL Settings > Metadata > Definitions]**&#x200B;す。

## 動的ファセットの実行例 {#section_BC699A05E2E742EF94D41679163ACE84}

「boots」の検索後に表示される動的ファセットの例：

![](assets/dynamicfacets_boots.png)

「watches」の検索後に表示される動的ファセットの別の例：

![](assets/dynamicfacets_watches.png)

詳しくは、

* [バックエンド検索CGIパラメータ](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)
* [プレゼンテーションテンプレートタグ](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)
* [転送テンプレートタグ](../c-appendices/c-templates.md#reference_227D199F5A7248049BE1D405C0584751)

## 動的ファセットの設定 {#task_D17F484130E448258100BAC1EEC53F39}

Search&amp;Promoteでの動的ファセットの設定を参照してください。

<!-- 

t_configuring_dynamic_facets.xml

 -->

>[!NOTE]
>
>この機能は、Adobe Search&amp;Promoteではデフォルトでは有効になっていません。 お使いの機能を有効にするには、テクニカルサポートにお問い合わせください。

動的ファセットの効果が顧客に表示される前に、サイトインデックスを再構築する必要があります。

詳しくは、

* [バックエンド検索CGIパラメータ](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)
* [プレゼンテーションテンプレートタグ](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)
* [転送テンプレートタグ](../c-appendices/c-templates.md#reference_227D199F5A7248049BE1D405C0584751)

**動的ファセットを設定するには**

1. ファセットが既に追加されていることを確認します。

   「新しいフ [ァセットの追加」を参照してくださ](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B)い。
1. ファセットを追加したら、新しいユーザー定義のメタタグフィールドにファセットが追加されていることを確認します。

   詳しくは、 [新しいメタタグフィールドの追加を参照してくださ](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)い。
1. 製品メニューで、//をクリ **[!UICONTROL Settings]** ックしま **[!UICONTROL Metadata]** す **[!UICONTROL Definitions.]**
1. ページの [!DNL Definitions] 表の列で、動的 [!DNL User-defined fields] にす [!DNL Actions] るファセットに関連付けられたメタタグフィールド名の行にある鉛筆アイコン（編集）をクリックします。
1. ページで、 [!DNL Edit Field] チェックしま **[!UICONTROL Dynamic Facet]**&#x200B;す。

   新しいメタタグフィールドの追加のオ [プションの表を参照してください](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)。
1. クリック **[!UICONTROL Save Changes]**.
1. 青いボッ **クスでステージ済みのサイトインデックスを** 「再生成」をクリックして、ステージ済みのWebサイトインデックスをすばやく再構築します。

   ライブまたはステ [ージングされたWebサイトのインデックスの再生成も参照してくださ](../c-about-index-menu/c-about-regenerate-index.md#task_B28DE40C0E9A475ABCBCBC4FF993AACD)い。
1. 特定の検索に対して選択する動的ファセットの数を決定します。 このタスクは、次のいずれかを実行して行います。

   * 目的の条件を持つクエリクリーニングルールを作成し、アクション `set`( `backend parameter`, `sp_sfvl_df_count` , `X`to value)を実行します。は、検索時にリクエストする動的ファセットの数です。は、その後、をクリックします `X`**[!UICONTROL Add]**。
   ![](assets/querycleaningrule_dynamicfacets.png)

   詳しくは、 [クエリクリーニング規則の追加を参照](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54)。

   詳しくは、表の [「バックエンド検索CGIパラメータ](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)」の行40も参照してくださ `sp_sfvl_df_count`い。

   * 検追加索を行い、「カスタム」パラメータを目的 `sp_sfvl_df_count` の値に設定して、をクリックしま **[!UICONTROL Add]**&#x200B;す。
   ![](assets/gs_addsearch_dynamic_facets.png)

   「新しい [検索定義の追加」を参照してくださ](../c-about-settings-menu/c-about-searching-menu.md#task_98D3A168AB5D4F30A1ADB6E0D48AB648)い。

   詳しくは、表の [「バックエンド検索CGIパラメータ](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)」の行40も参照してくださ `sp_sfvl_df_count`い。

1. 適切なトランスポートテンプレートを編集して、コア検索が返す動的ファセットを出力します。

   詳しくは、プ [レゼンテーションまたは転送テンプレートの編集を参照してくださ](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)い。

   例えば、トランスポートテンプレートに名前が付いているとしま `guided.tpl`す。 この場合、製品メニューでをクリックしま **[!UICONTROL Design > Templates]**&#x200B;す。 ページ上 [!DNL Templates] で、テーブル `guided.tpl` 内を見つけます。 名前の最 **[!UICONTROL Edit]** も右側をクリックします。 編集ページで、次のコードブロックをの末尾に追加します `</facets>`。JSON出力：

   ```
   ... 
   }<search-dynamic-facet-fields>, 
           { 
               "name" : "<search-dynamic-facet-field-name>", 
               "dynamic-facet" : 1, 
               "values" : [<search-field-value-list quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
               "counts" : [<search-field-value-list quotes="yes" commas="yes" data="results" sortby="values" />] 
   
           }</search-dynamic-facet-fields> 
   ...
   ```

1. 適切なプレゼンテーションテンプレートまたはテンプレートを編集して、動的ファセットを出力します。

   詳しくは、プ [レゼンテーションまたは転送テンプレートの編集を参照してくださ](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)い。

   例えば、シミュレーターでコンテンツを出力するために使 `sim.tmpl` 用する、という名前のテンプレートがあるとします。 そのテンプレートを編集するには、製品メニューでをクリックしま **[!UICONTROL Design > Templates]**&#x200B;す。 ページ上 [!DNL Templates] で、テーブル `sim.tmpl` 内を見つけます。 名前の最 **[!UICONTROL Edit]** も右側をクリックします。 編集ページで、テンプレートのファセット表示領域に次を追加します。

   ```
   <h6>DF RAIL</h6> 
   <guided-facet-rail gsname="__dynamic_facets"> 
               <guided-facet ><!-- behavior=Normal --> 
               <div class="facet-block" id="facet"> 
               <p><b><guided-facet-display-name /></b></p> 
               <ul> 
                   <guided-facet-values> 
                       <guided-if-facet-value-equals-length-threshold> 
               </ul> 
               <ul id="brand" style="display:none"> 
                       </guided-if-facet-value-equals-length-threshold> 
                       <guided-if-facet-value-selected> 
                           <li><guided-facet-value> [<guided-lt>a href="<guided-facet-value-undo-path />"<guided-gt>X</a>]</li> 
                       <guided-else-facet-value-selected> 
                           <li><guided-facet-link><guided-facet-value></guided-facet-link> (<guided-facet-count>) </li> 
                       </guided-if-facet-value-selected> 
                   </guided-facet-values> 
               </ul> 
               <guided-if-facet-long> 
                 <br /><guided-lt />a href="#" onclick="moreless(this,'brand');return false;" <guided-gt /><button style="font-size:10px;">VIEW MORE</button></a> 
               </guided-if-facet-long> 
               </div> 
               </guided-facet> 
   </guided-facet-rail> 
   <h6>/DF RAIL</h6>
   ```

   また、必要に応じて、他のプレゼンテーションテンプレート（など）にも同様の変更を加えま `json.tmpl`す。

   タグ内ののに必ず `__dynamic_facets` を指定 `gsname` してくだ `guided-facet-rail` さい。 このタグは、特定の検索に対して返される動的ファセットを出力するために予約された、事前定義のファセットレールです。

   オプションで、次の図に示すように、を使用して、この特別なファセ **[!UICONTROL Rules > Business Rules]**&#x200B;ットレールを編集する **[!UICONTROL Advanced Rule Builder]** こともできます。

   ![](assets/dynamicfacetrail_businessrule.png)

   「新しいビジネ [スルールの追加」も参照してください。](../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7)
