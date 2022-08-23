---
title: CHANGETIMEZONE ER 機能
description: この記事では、CHANGETIMEZONE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: kfend
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: AX 10.0.23
ms.custom: 58771
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: d732fd8bd44c4c131f376919b2546a7ecf668495
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286122"
---
# <a name="changetimezone-er-function"></a>CHANGETIMEZONE ER 機能

[!include [banner](../includes/banner.md)]

`CHANGETIMEZONE` 関数は、あるタイムゾーンの指定された日付/時刻の値を、別のタイムゾーンの日付/時刻の値に変換した協定世界時 (グリニッジ標準時 \[GMT\]) の *[DateTime](er-formula-supported-data-types-primitive.md#datetime)* 値を返します。

## <a name="syntax"></a>構文

```vb
CHANGETIMEZONE (datetime, base time zone, target time zone)
```

## <a name="arguments"></a>引数

`datetime`: *日時*

協定世界時のタイムゾーンで、変換する日付・時刻の値を表します。

`base time zone`: *[文字列](er-formula-supported-data-types-primitive.md#string)*

指定された日付/時刻の値が変換前にシフトされるタイムゾーンの名前です。

`target time zone`: *文字列*

変換された日付/時刻の値が、変換時にシフトするタイムゾーンの名前です。

## <a name="return-values"></a>戻り値

*DateTime*

協定世界時のタイムゾーンでの結果の日付/時刻の値です。

## <a name="usage-notes"></a>使用上の注意

送信元と送信先のタイムゾーンを指定するには、[インターネット番号割当機関 (IANA)](https://www.iana.org/) が[提供している](https://data.iana.org/time-zones/releases/)タイムゾーン名や、Microsoft Windows が[サポートしている](/windows-hardware/manufacture/desktop/default-time-zones)タイムゾーン名を使用できます。

実行時に、指定された名前が IANA リストや Windows レジストリに見つからない場合は、「タイムゾーン "\<time zone name\>" が存在しません」という例外がスローされます。

サマータイムが実施されているタイムゾーンでは、協定世界時のサマータイム オフセットを考慮して変換されます。 変換時には、このオフセットに関する最新の情報が使用されます。

## <a name="example-1"></a>例 1

この例では、Windows のタイムゾーン名を使用しています。

**算出されたフィールド** タイプの **DSX** データソースを構成します。 次の式が含まれています。

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "E. Europe Standard Time", "Hawaiian Standard Time"), "O")
)
```

**計算されたフィールド** タイプの **DSY** データソースの式を `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` と設定すると、**DSX** データソースは **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00** というテキストを返します。 このテキストは、6 月 1 日に提供された 2 つのタイムゾーンの時差が 24 時間以上であることを示しています。 したがって、基準となるタイムゾーンが対象となるタイムゾーンよりも先行しているため、変換後の日時の値は指定された日時の値よりも 1 日前の値になります。

**計算されたフィールド** タイプの **DSY** データソースの式を `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` と設定すると、**DSX** データソースは **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00** というテキストを返します。 このテキストは、12 月 1 日に提供された 2 つのタイムゾーンの時差が 24 時間以下であることを示しています。 したがって、変換された日付/時刻の値は、指定された日付/時刻の値と等しくなります。

> [!NOTE]
> 同じ式は、同じタイムゾーンのペアについて、指定された日付/時刻の値と変換された日付/時刻の値の間で異なる差異を返します。これは、ある日付/時刻において、指定されたタイムゾーンで異なる協定世界時のサマータイムオフセットが実施されるためです。

## <a name="example-2"></a>例 2

この例では、IANA のタイムゾーン名を使用しています。

**算出されたフィールド** タイプの **DSX** データソースを構成します。 次の式が含まれています。

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "Europe/Athens", "US/Hawaii"), "O")
)
```

**計算されたフィールド** タイプの **DSY** データソースの式を `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` と設定すると、**DSX** データソースは **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00** というテキストを返します。 このテキストは、6 月 1 日に提供された 2 つのタイムゾーンの時差が 24 時間以上であることを示しています。 したがって、基準となるタイムゾーンが対象となるタイムゾーンよりも先行しているため、変換後の日時の値は指定された日時の値よりも 1 日前の値になります。

**計算されたフィールド** タイプの **DSY** データソースの式を `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` と設定すると、**DSX** データソースは **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00** というテキストを返します。 このテキストは、12 月 1 日に提供された 2 つのタイムゾーンの時差が 24 時間以下であることを示しています。 したがって、変換された日付/時刻の値は、指定された日付/時刻の値と等しくなります。

## <a name="example-3"></a>例 3

**算出されたフィールド** タイプの **DSX** データソースを構成します。 次の式が含まれています。

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "US/Hawaii", "Europe/Athens"), "O")
)
```

**計算されたフィールド** タイプの **DSY** データソースの式を `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` と設定すると、**DSX** データソースは **2021-06-01T12:55:00.0000000+00:00 -> 2021-06-02T01:55:00.0000000+00:00'** というテキストを返します。 このテキストは、6 月 1 日に提供された 2 つのタイムゾーンの時差が 24 時間以上であることを示しています。 したがって、変換後の日時の値は、対象となるタイムゾーンが基準となるタイムゾーンよりも先行しているため、指定された日時の値よりも 1 日遅くなります。

## <a name="example-4"></a>例 4

外部のソースから、タイムゾーン情報を含まないテキストで、日付/タイムスタンプが送信される場合があります。 しかし、ソースが運用されているタイムゾーンがわかっている場合があります。 たとえば、スペインで事業を行っているサービスから日付/時刻スタンプ **01/12/2021 12:55:00** を受け取ったとします。 この日時の値をデータベースに正しく保存するには、以下の変換を行ってください:

- **算出されたフィールド** タイプの **DSY** データソースを設定して、日付/タイムスタンプをテキストから協定世界時の日付/時刻の値に変換します。

    `DATETIMEVALUE ("01/12/2021 12:55:00", "dd/MM/yyyy HH:mm:ss", "ES")`

- **算出されたフィールド** タイプの **DSX** データソースで、変換された日付/時刻の値を、外部ソースのタイムゾーンの日付/時刻の値として協定世界時にシフトするように構成します。

    `CHANGETIMEZONE(DSY, "Romance Standard Time", "GMT Standard Time")`

> [!NOTE]
> `CHANGETIMEZONE` の機能を使用して日付/時刻の変換を行う場合、日付/時刻の値は、協定世界時のタイムゾーンの値としてデータベースに保存されることに注意してください。 この値はアプリケーションのページで表示する前に、変換されます。 この変換では、現在サインインしているアプリケーション ユーザーの優先ゾーンとして[設定](../../fin-ops/organization-administration/tasks/set-users-preferred-time-zone.md)されているタイムゾーンが考慮されます。

## <a name="additional-resources"></a>追加リソース

[日時の関数](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
