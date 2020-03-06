---
description: 「日付」データ型のフィールドを解析し、インデックスを作成するときに使用する日付形式を定義できます。
seo-description: 「日付」データ型のフィールドを解析し、インデックスを作成するときに使用する日付形式を定義できます。
seo-title: 日付形式
solution: Target
title: 日付形式
topic: Appendices,Site search and merchandising
uuid: 148914b5-33ef-41db-8404-67c03f6f0832
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# 日付形式{#date-formats}

「日付」データ型のフィールドを解析し、インデックスを作成するときに使用する日付形式を定義できます。

日時の形式は、形式文字列を使用して指定します。 書式文字列は、0個以上の変換指定（変換指定は、パーセント記号と他の1文字で構成されます）と通常の文字で構成されます。 各日付フィールドの日付形式文字列のデフォルトのリストが提供されます。

このリストは完全に制御でき、サイトのニーズに合わせて追加または変更できます。 最上位の形式文字列が優先され、以降の形式文字列は、特定のメタデータタグの内容を解析してエラーが発生した場合にのみ使用されます。

例えば、次の日付形式を指定したとします。

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%B %d、%Y %T %Z </p> <p>%Y年%b %d日%T %Z </p> <p>%A %B %d、%Y %T %Z </p> <p>%A %b %d、%Y %T %Z </p> <p>%a %B %d、%Y %T %Z </p> <p>%Y %Y %T %Z %a %b %d </p> <p>%d %b %Y %T %Z </p> </td> 
  </tr> 
 </tbody> 
</table>

最初の形式「%B %d, %Y %T %Z」は、次の「2014年9月20日13:12:00 PDT」のような日付と一致します。 メタデータタグの内容がこの形式文字列で解析できない場合は、次に使用可能な形式&quot;%b %d, %Y %T %Z&quot;が試行されます。 この形式は、次のような日付と一致します。「Sep 20, 2014 3:12:00 PDT」 この形式文字列でメタデータタグの内容を解析できない場合、サイト検索/マーチャンダイジングは、機能する形式文字列が見つかるまで、形式文字列のリストを下に移動します。

次の表に、使用可能な日付形式の文字列を示します。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>データフォーマット </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>% </p> </td> 
   <td colname="col2"> <p>完全な曜日の名前を国内表現（例：「Monday」）に一致させます。 各国語表現は、「単語と言語」オプションの「言語」設定から決定されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a </p> </td> 
   <td colname="col2"> <p> 曜日の略式名の国内表現に一致します。省略形は最初の3文字です。例：「月」 各国語表現は、「単語と言語」オプションの「言語」設定から決定されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%B </p> </td> 
   <td colname="col2"> <p> は、完全な月名の国別表現に一致します。例：「6月」 各国語表現は、「単語と言語」オプションの「言語」設定から決定されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%b </p> </td> 
   <td colname="col2"> <p> 月の略式名の国単位の表現に一致します。省略形は最初の3文字です。例：「ジュン」 各国語表現は、「単語と言語」オプションの「言語」設定から決定されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%D </p> </td> 
   <td colname="col2"> <p> は「%m/%d/%y」と等しい(例："06/06/01" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%d </p> </td> 
   <td colname="col2"> <p> は、月の日を10進数で表した数値(01 ～ 31)と一致します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%e </p> </td> 
   <td colname="col2"> <p> は、月の日を10進数(1 ～ 31)で表します。1桁の数字の前に空白が付く </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%H </p> </td> 
   <td colname="col2"> <p> は、時（24時間形式）を10進数(00 ～ 23)で表します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%h </p> </td> 
   <td colname="col2"> <p> 月の略式名の国単位の表現に一致します。省略形は最初の3文字です。例："Jun" （%bと同じ） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%I </p> </td> 
   <td colname="col2"> <p> は、10進数(01 ～ 12)で時（12時間制）を表します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%j </p> </td> 
   <td colname="col2"> <p> は、年の何日目かを10進数で表す数値と一致します(001 ～ 366)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%k </p> </td> 
   <td colname="col2"> <p> は、時（24時間形式）を10進数(0 ～ 23)で表した値に一致します。1桁の数字の前に空白が付く </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%l </p> </td> 
   <td colname="col2"> <p> は、10進数(1 ～ 12)として時（12時間制）に一致します。1桁の数字の前に空白が付く </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%M </p> </td> 
   <td colname="col2"> <p> は、分を10進数(00 ～ 59)で表します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%m </p> </td> 
   <td colname="col2"> <p> は、月を10進数(01 ～ 12)で表します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%p </p> </td> 
   <td colname="col2"> <p> は、必要に応じて、「午前時」または「午後時」の国内表現に一致します。例えば、「総理。」 各国語表現は、「単語と言語」オプションの「言語」設定から決定されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%R </p> </td> 
   <td colname="col2"> <p> は「%H:%M」と同じです。例："13:23" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%r </p> </td> 
   <td colname="col2"> <p> は"%I:%M:%S %p"と同等です。例："01:23:45 PM" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%S </p> </td> 
   <td colname="col2"> <p> は、10進数(00 ～ 60)で2番目の値と一致します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%T </p> </td> 
   <td colname="col2"> <p> は"%H:%M:%S"と同等です。例："13:26:47" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%U </p> </td> 
   <td colname="col2"> <p> は、年の週番号（日曜日を週の最初の日として）を10進数(00 ～ 53)で表します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%v </p> </td> 
   <td colname="col2"> <p> は「%e-%b-%Y」と同じです。例："2001年6月6日" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%はい </p> </td> 
   <td colname="col2"> <p> は、世紀を10進数で表した年と一致します。例："2001" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%y </p> </td> 
   <td colname="col2"> <p> は、世紀を10進数で表した年(00 ～ 99)に一致します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Z </p> </td> 
   <td colname="col2"> <p> は、タイムゾーン名と一致します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%% </p> </td> 
   <td colname="col2"> <p> matches "%" </p> </td> 
  </tr> 
 </tbody> 
</table>

**デフォルトの書式文字列**

テンプレートでは、次のデフォルトの書式文字列が使用されます。 必要に応じて、このリストに追加したり、編集したりできます。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>デフォルトの書式文字列 </p> </th> 
   <th colname="col2" class="entry"> <p>結果の例 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%B %d、%Y %T %Z </p> </td> 
   <td colname="col2"> <p> 1999年9月5日13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Y年%b %d日%T %Z </p> </td> 
   <td colname="col2"> <p> 1999年9月5日13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%A %B %d、%Y %T %Z </p> </td> 
   <td colname="col2"> <p> 1999年9月5日曜日13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%A %b %d、%Y %T %Z </p> </td> 
   <td colname="col2"> <p> 1999年9月5日日曜日13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a %B %d、%Y %T %Z </p> </td> 
   <td colname="col2"> <p> Sun September 5, 1999 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Y %Y %T %Z %a %b %d </p> </td> 
   <td colname="col2"> <p> Sun Sep 5, 1999 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%d %b %Y %T %Z </p> </td> 
   <td colname="col2"> <p> 1999年9月5日13:12:00 PDT </p> </td> 
  </tr> 
 </tbody> 
</table>

