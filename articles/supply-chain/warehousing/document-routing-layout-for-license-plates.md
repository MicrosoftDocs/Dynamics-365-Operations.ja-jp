---
title: ドキュメント ルート指定 ラベル レイアウト
description: この記事では、書式設定メソッドを使用してラベルに値を印刷する方法について説明します。
author: perlynne
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: a4e0c16b71c257cae832870ca58679884047ea16
ms.sourcegitcommit: 9e6a9d644a34158390c6e209e80053ccbdb7d974
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708648"
---
# <a name="document-routing-label-layout"></a>ドキュメント ルート指定 ラベル

[!include [banner](../includes/banner.md)]

この記事では、ライセンス ライセンス 契約、コンテナー、およびラベル (複数) のレイアウトの作成方法について説明します。 また、レイアウトを作成するために使用する Zebra プログラミング言語を使用する際のガイドラインも提供します。

ドキュメント ルート指定ラベル レイアウトでは、ラベルのレイアウトと、その上に印刷されるデータを定義します。 印刷トリガー ポイントは、モバイル デバイスのメニュー項目と作業テンプレートを設定するときに設定します。

この記事の情報は、[ライセンス プレート ラベル](tasks/license-plate-label-printing.md)、[コンテナー ラベル](print-container-labels.md)、[サイクル ラベル](configure-wave-label-printing.md) など、すべてのドキュメント ルート指定ラベル のレイアウトに適用されます。

印刷デバイスが送信されたテキストを解釈できる場合は、非常に複雑なラベルを印刷できます。 たとえば、バーコードを含む  Zebra プログラミング 言語 (ZPL) レイアウトは、次の例のようになります。

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

ラベル印刷プロセスの一部として、この例のテキスト `$LicensePlateId$` はデータ値に置き換えられます。 いくつかの広く使用されているラベル生成ツールには、ラベル レイアウトのテキストの書式設定に役立つものがあります。 これらのツールの多くは、`$FieldName$` 形式をサポートしています。 さらに、Microsoft Dynamics 365 Supply Chain Management では、ドキュメント ルーティング レイアウトのフィールド マッピングの一部として特別な書式設定ロジックを使用しています。

印刷される値を表示するには、**倉庫管理 \> 照会およびレポート \> ライセンス プレート ラベル** に移動します。

## <a name="turn-on-this-feature-for-your-system"></a>システムでこの機能を有効化する

この記事で説明する機能がシステムにまだ含まれていない場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) に移動して、*拡張されたライセンス プレート ラベルのレイアウト* 機能を有効にします。 (Supply Chain Management のバージョン10.0.21 では、この機能は既定で有効になっています。 (Supply Chain Management 10.0.25 では、この機能は必須であり、オフにすることはできません。)

## <a name="custom-number-formats"></a>カスタム数値形式

次の形式のコードを使用して、印刷される数値フィールド値の書式設定は、カスタマイズできます。

```dos
$FieldName:FormatString$
```

この形式の説明は以下の通りです:

- `FieldName` はデータ フィールドの名前 (**数量** など) です。
- `FormatString` は、データの印刷方法を定義します。

次の例では、作業数量 (**数量**) フィールドをカスタマイズする方法を示します。

- (プレースホルダーとしてゼロを使用して) 常に 4 桁を表示するには、`$Qty:0000$` を使用します。 たとえば、数量が 10 の場合、ラベルは "0010" と表示されます。
- 常に小数点以下 2 桁を表示するには、`$Qty:0.00$` を使用します。 たとえば、数量が 10 の場合、ラベルは "10.00" と表示されます。

使用可能な数値形式文字列の完全な一覧については、[カスタム数値形式文字列](/dotnet/standard/base-types/custom-numeric-format-strings) を参照してください。

## <a name="custom-string-formats"></a>カスタム文字列形式

文字列の最初の文字を削除するには、次のフィールドと書式コードを使用します。

```dos
$FieldName:#..$
```

ここで、`#` はスキップする文字数を指定します。 たとえば、最初の 2 文字が含まれていない出荷コンテナ シリアル コード (SSCC) ライセンス プレート番号を印刷するには、`$LicensePlateId:2..$` を使用します。 この場合、ライセンス プレート番号 0011111111111222221 は、"11111111111222221" として印刷されます。

## <a name="custom-datetime-formats"></a>カスタム日付/時刻形式

次の例では、日付の印刷に使用される形式を制御する方法を示します。

```dos
$PrintedDate:dd-MM-yyyy$
```

この例では、日付 2020 年 4 月 30 日は "30-04-2020" として印刷されます。

使用可能な日付/時刻形式の完全な一覧については、[カスタム日付と時刻の形式文字列](/dotnet/standard/base-types/custom-date-and-time-format-strings) を参照してください。

## <a name="print-individual-lines-from-multiline-data"></a>複数行データから個々の行を印刷する

データ フィールドに複数の行 (つまり、改行で区切られた行) が含まれている場合は、次の形式を使用して個々の行を印刷できます。

```dos
$FieldName[#]$
```

ここで、`#` は印刷する行番号です。 (最初の行に 1 を使用します。)

たとえば、システムには、次の複数行の住所を格納する `AdditionalAddress` フィールドがあります。

Contoso Inc.  
123 通りの名前  
ある市、ある州

次のコードを使用して、この住所を一度に 1 行ずつ印刷できます。

| 区分 | 印刷されるテキスト |
|---|---|
| `$AdditionalAddress[1]$` | Contoso Inc. |
| `$AdditionalAddress[2]$` | 123 通りの名前 |
| `$AdditionalAddress[3]$` | ある市、ある州 |

## <a name="print-and-format-from-a-display-method"></a>表示方法からの印刷と書式設定

次の形式で表示方法から印刷できます。

```dos
$DisplayMethod()$
```

この形式は、この記事で前述した他のタイプと組み合わせることができます。 たとえば、`DisplayListOfItemsNumbers()` という名前の表示方法があり、このメソッドの最初の品目番号を印刷するとします。 この場合、次のコードを使用できます。

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a>ラベルを印刷する方法の詳細

ラベルの設定と印刷方法についての詳細は、次の記事を参照してください。

- [ライセンス プレート ラベルの印刷](tasks/license-plate-label-printing.md)
- [コンテナー ラベルの印刷](print-container-labels.md)
- [ウェーブ ラベルの印刷](configure-wave-label-printing.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
