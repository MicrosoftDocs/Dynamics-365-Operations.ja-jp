---
title: ライセンス プレート ラベルのドキュメント ルーティング レイアウト
description: このトピックでは、書式設定メソッドを使用してラベルに値を印刷する方法について説明します。
author: perlynne
manager: tfehr
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 7c20d3d0540f8f1a05928df9aff5253745982da9
ms.sourcegitcommit: 4ecc1bf82fbb04882d7ef5e1994ef3c07ef953dc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/08/2021
ms.locfileid: "5558265"
---
# <a name="document-routing-layout-for-license-plate-labels"></a><span data-ttu-id="8f434-103">ライセンス プレート ラベルのドキュメント ルーティング レイアウト</span><span class="sxs-lookup"><span data-stu-id="8f434-103">Document routing layout for license plate labels</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="8f434-104">ドキュメント ルーティング レイアウトでは、ライセンス プレート ラベルのレイアウトと、その上に印刷されるデータを定義します。</span><span class="sxs-lookup"><span data-stu-id="8f434-104">The document routing layout defines the layout of license plate labels, and the data that is printed on them.</span></span> <span data-ttu-id="8f434-105">印刷トリガー ポイントは、モバイル デバイスのメニュー項目と作業テンプレートを設定するときに設定します。</span><span class="sxs-lookup"><span data-stu-id="8f434-105">You configure the printing trigger points when you set up mobile device menu items and work templates.</span></span>

<span data-ttu-id="8f434-106">一般的なシナリオでは、倉庫の受け取り担当者は、受け取りエリアに到着したパレットの内容を記録した後にライセンス プレート ラベルを印刷します。</span><span class="sxs-lookup"><span data-stu-id="8f434-106">In a typical scenario, warehouse receiving clerks print license plate labels immediately after they record the contents of pallets that arrive in the receiving area.</span></span> <span data-ttu-id="8f434-107">物理的なラベルがパレットに貼られます。</span><span class="sxs-lookup"><span data-stu-id="8f434-107">The physical labels are applied to the pallets.</span></span> <span data-ttu-id="8f434-108">これらは、後続のプット アウェイ プロセスと出荷ピッキング処理の一部として検証に使用できます。</span><span class="sxs-lookup"><span data-stu-id="8f434-108">They can then be used for validation as part of the put-away process that follows and future outbound picking operations.</span></span>

<span data-ttu-id="8f434-109">印刷デバイスが送信されたテキストを解釈できる場合は、非常に複雑なラベルを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="8f434-109">You can print highly complex labels, provided that the printing device can interpret the text that is sent to it.</span></span> <span data-ttu-id="8f434-110">たとえば、バーコードを含む Zebra プログラミング 言語 (ZPL) レイアウトは、次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="8f434-110">For example, a Zebra Programming Language (ZPL) layout that includes a bar code might resemble the following example.</span></span>

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

<span data-ttu-id="8f434-111">ラベル印刷プロセスの一部として、この例のテキスト `$LicensePlateId$` はデータ値に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="8f434-111">As part of the label printing process, the text `$LicensePlateId$` in this example will be replaced with a data value.</span></span>

<span data-ttu-id="8f434-112">印刷される値を表示するには、**倉庫管理 \> 照会およびレポート \> ライセンス プレート ラベル** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8f434-112">To see the values that will be printed, go to **Warehouse management \> Inquiries and reports \> License plate labels**.</span></span>

<span data-ttu-id="8f434-113">いくつかの広く使用されているラベル生成ツールには、ラベル レイアウトのテキストの書式設定に役立つものがあります。</span><span class="sxs-lookup"><span data-stu-id="8f434-113">Several widely available label generation tools can help you format the text for the label layout.</span></span> <span data-ttu-id="8f434-114">これらのツールの多くは、`$FieldName$` 形式をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="8f434-114">Many of these tools support the `$FieldName$` format.</span></span> <span data-ttu-id="8f434-115">さらに、Microsoft Dynamics 365 Supply Chain Management では、ドキュメント ルーティング レイアウトのフィールド マッピングの一部として特別な書式設定ロジックを使用しています。</span><span class="sxs-lookup"><span data-stu-id="8f434-115">In addition, Microsoft Dynamics 365 Supply Chain Management uses special formatting logic as part of the field mapping for the document routing layout.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="8f434-116">システムでこの機能を有効化する</span><span class="sxs-lookup"><span data-stu-id="8f434-116">Turn on this feature for your system</span></span>

<span data-ttu-id="8f434-117">このトピックで説明する機能がシステムにまだ含まれていない場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) に移動して、*拡張されたライセンス プレート ラベルのレイアウト* 機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="8f434-117">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Enhanced license plate label layouts* feature.</span></span>

## <a name="custom-number-formats"></a><span data-ttu-id="8f434-118">カスタム数値形式</span><span class="sxs-lookup"><span data-stu-id="8f434-118">Custom number formats</span></span>

<span data-ttu-id="8f434-119">次の形式のコードを使用して、印刷される数値フィールド値の書式設定は、カスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="8f434-119">You can customize the formatting of numerical field values that are printed by using codes that have the following format.</span></span>

```dos
$FieldName:FormatString$
```

<span data-ttu-id="8f434-120">この形式の説明は以下の通りです:</span><span class="sxs-lookup"><span data-stu-id="8f434-120">Here is an explanation of this format:</span></span>

- <span data-ttu-id="8f434-121">`FieldName` はデータ フィールドの名前 (**数量** など) です。</span><span class="sxs-lookup"><span data-stu-id="8f434-121">`FieldName` is the name of the data field (such as **Qty**).</span></span>
- <span data-ttu-id="8f434-122">`FormatString` は、データの印刷方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="8f434-122">`FormatString` defines how the data must be printed.</span></span>

<span data-ttu-id="8f434-123">次の例では、作業数量 (**数量**) フィールドをカスタマイズする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="8f434-123">The following examples show how you can customize the work quantity (**Qty**) field:</span></span>

- <span data-ttu-id="8f434-124">(プレースホルダーとしてゼロを使用して) 常に 4 桁を表示するには、`$Qty:0000$` を使用します。</span><span class="sxs-lookup"><span data-stu-id="8f434-124">To always show four digits (by using zeros as placeholders), use `$Qty:0000$`.</span></span> <span data-ttu-id="8f434-125">たとえば、数量が 10 の場合、ラベルは "0010" と表示されます。</span><span class="sxs-lookup"><span data-stu-id="8f434-125">For example, if the quantity is 10, the label will show "0010."</span></span>
- <span data-ttu-id="8f434-126">常に小数点以下 2 桁を表示するには、`$Qty:0.00$` を使用します。</span><span class="sxs-lookup"><span data-stu-id="8f434-126">To always show two decimal places, use `$Qty:0.00$`.</span></span> <span data-ttu-id="8f434-127">たとえば、数量が 10 の場合、ラベルは "10.00" と表示されます。</span><span class="sxs-lookup"><span data-stu-id="8f434-127">For example, if the quantity is 10, the label will show "10.00."</span></span>

<span data-ttu-id="8f434-128">使用可能な数値形式文字列の完全な一覧については、[カスタム数値形式文字列](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8f434-128">For a complete list of the available number format strings, see [Custom numeric format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="custom-string-formats"></a><span data-ttu-id="8f434-129">カスタム文字列形式</span><span class="sxs-lookup"><span data-stu-id="8f434-129">Custom string formats</span></span>

<span data-ttu-id="8f434-130">文字列の最初の文字を削除するには、次のフィールドと書式コードを使用します。</span><span class="sxs-lookup"><span data-stu-id="8f434-130">You can remove the first characters of a string by using the following field and format code.</span></span>

```dos
$FieldName:#..$
```

<span data-ttu-id="8f434-131">ここで、`#` はスキップする文字数を指定します。</span><span class="sxs-lookup"><span data-stu-id="8f434-131">Here, `#` specifies the number of characters to skip.</span></span> <span data-ttu-id="8f434-132">たとえば、最初の 2 文字が含まれていない出荷コンテナ シリアル コード (SSCC) ライセンス プレート番号を印刷するには、`$LicensePlateId:2..$` を使用します。</span><span class="sxs-lookup"><span data-stu-id="8f434-132">For example, to print a Serial Shipping Container Code (SSCC) license plate number that doesn't include the first two characters, use `$LicensePlateId:2..$`.</span></span> <span data-ttu-id="8f434-133">この場合、ライセンス プレート番号 0011111111111222221 は、"11111111111222221" として印刷されます。</span><span class="sxs-lookup"><span data-stu-id="8f434-133">In this case, the license plate number 0011111111111222221 will be printed as "11111111111222221."</span></span>

## <a name="custom-datetime-formats"></a><span data-ttu-id="8f434-134">カスタム日付/時刻形式</span><span class="sxs-lookup"><span data-stu-id="8f434-134">Custom date/time formats</span></span>

<span data-ttu-id="8f434-135">次の例では、日付の印刷に使用される形式を制御する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="8f434-135">The following example shows how you can control the format that is used to print dates.</span></span>

```dos
$PrintedDate:dd-MM-yyyy$
```

<span data-ttu-id="8f434-136">この例では、日付 2020 年 4 月 30 日は "30-04-2020" として印刷されます。</span><span class="sxs-lookup"><span data-stu-id="8f434-136">In this example, the date April 30, 2020, will be printed as "30-04-2020."</span></span>

<span data-ttu-id="8f434-137">使用可能な日付/時刻形式の完全な一覧については、[カスタム日付と時刻の形式文字列](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8f434-137">For a complete list of the available date/time formats, see [Custom date and time format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="print-individual-lines-from-multiline-data"></a><span data-ttu-id="8f434-138">複数行データから個々の行を印刷する</span><span class="sxs-lookup"><span data-stu-id="8f434-138">Print individual lines from multiline data</span></span>

<span data-ttu-id="8f434-139">データ フィールドに複数の行 (つまり、改行で区切られた行) が含まれている場合は、次の形式を使用して個々の行を印刷できます。</span><span class="sxs-lookup"><span data-stu-id="8f434-139">If a data field contains multiple lines (that is, lines that are separated by line breaks), you can print an individual line by using the following format.</span></span>

```dos
$FieldName[#]$
```

<span data-ttu-id="8f434-140">ここで、`#` は印刷する行番号です。</span><span class="sxs-lookup"><span data-stu-id="8f434-140">Here, `#` is the line number that you want to print.</span></span> <span data-ttu-id="8f434-141">(最初の行に 1 を使用します。)</span><span class="sxs-lookup"><span data-stu-id="8f434-141">(Use 1 for the first line.)</span></span>

<span data-ttu-id="8f434-142">たとえば、システムには、次の複数行の住所を格納する `AdditionalAddress` フィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="8f434-142">For example, your system has an `AdditionalAddress` field that stores the following multiline address:</span></span>

<span data-ttu-id="8f434-143">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="8f434-143">Contoso Inc.</span></span>  
<span data-ttu-id="8f434-144">123 通りの名前</span><span class="sxs-lookup"><span data-stu-id="8f434-144">123 Street Name</span></span>  
<span data-ttu-id="8f434-145">ある市、ある州</span><span class="sxs-lookup"><span data-stu-id="8f434-145">Some City, Some State</span></span>

<span data-ttu-id="8f434-146">次のコードを使用して、この住所を一度に 1 行ずつ印刷できます。</span><span class="sxs-lookup"><span data-stu-id="8f434-146">You can print this address, one line at a time, by using the following codes.</span></span>

| <span data-ttu-id="8f434-147">区分</span><span class="sxs-lookup"><span data-stu-id="8f434-147">Code</span></span> | <span data-ttu-id="8f434-148">印刷されるテキスト</span><span class="sxs-lookup"><span data-stu-id="8f434-148">Text that is printed</span></span> |
|---|---|
| `$AdditionalAddress[1]$` | <span data-ttu-id="8f434-149">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="8f434-149">Contoso Inc.</span></span> |
| `$AdditionalAddress[2]$` | <span data-ttu-id="8f434-150">123 通りの名前</span><span class="sxs-lookup"><span data-stu-id="8f434-150">123 Street Name</span></span> |
| `$AdditionalAddress[3]$` | <span data-ttu-id="8f434-151">ある市、ある州</span><span class="sxs-lookup"><span data-stu-id="8f434-151">Some City, Some State</span></span> |

## <a name="print-and-format-from-a-display-method"></a><span data-ttu-id="8f434-152">表示方法からの印刷と書式設定</span><span class="sxs-lookup"><span data-stu-id="8f434-152">Print and format from a display method</span></span>

<span data-ttu-id="8f434-153">次の形式で表示方法から印刷できます。</span><span class="sxs-lookup"><span data-stu-id="8f434-153">You can print from a display method by using the following format.</span></span>

```dos
$DisplayMethod()$
```

<span data-ttu-id="8f434-154">この形式は、このトピックで前述した他のタイプと組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="8f434-154">You can combine this format with other types that were described earlier in this topic.</span></span> <span data-ttu-id="8f434-155">たとえば、`DisplayListOfItemsNumbers()` という名前の表示方法があり、このメソッドの最初の品目番号を印刷するとします。</span><span class="sxs-lookup"><span data-stu-id="8f434-155">For example, you have a display method that is named `DisplayListOfItemsNumbers()`, and you want to print the first item number of this method.</span></span> <span data-ttu-id="8f434-156">この場合、次のコードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="8f434-156">In this case, you can use the following code.</span></span>

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a><span data-ttu-id="8f434-157">ラベルを印刷する方法の詳細</span><span class="sxs-lookup"><span data-stu-id="8f434-157">More information about how to print labels</span></span>

<span data-ttu-id="8f434-158">ラベルの設定および印刷方法の詳細については、[ライセンス プレート ラベル印刷の有効化](tasks/license-plate-label-printing.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8f434-158">For more information about how to set up and print labels, see [Enable license plate label printing](tasks/license-plate-label-printing.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]