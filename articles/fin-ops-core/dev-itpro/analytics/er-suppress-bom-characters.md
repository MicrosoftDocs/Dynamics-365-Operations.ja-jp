---
title: 生成されたファイルの BOM 文字を非表示にする ER 構成の設計
description: このトピックでは、バイト オーダー マーク (BOM) 文字を非表示にするレポートを生成するために電子申告 (ER) 形式を構成する方法について説明します。
author: NickSelin
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b9265578deaff4100eb5987eb6090eaa12876044
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323744"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a>生成されたファイルの BOM 文字を非表示にする ER 構成の設計

[!include [banner](../includes/banner.md)]

送信ドキュメントを生成するための [電子申告 (ER)](general-electronic-reporting.md) [ソリューション](er-quick-start1-new-solution.md) をデザインできます。 ドキュメントをテキスト ファイルまたは XML ファイルとして生成するには、ER 形式 コンポーネントを含む ER [構成](general-electronic-reporting.md#Configuration) をソリューションに含める必要があります。 生成されたファイル内の文字セットを表す [文字エンコード](/windows/win32/intl/character-sets) を指定するには、ER 形式に **Common\\File** 形式要素を含む必要があります。 ER 形式コンポーネントを構成するには、ER 形式デザイナーで ER 構成の [下書き](general-electronic-reporting.md#component-versioning) バージョンを開き、**Common\\File** 要素を追加します。 **エンコード** フィールドで、このコンポーネントを使用して実行時に生成される送信ファイルのエンコードを指定します。

> [!NOTE]
> 形式に誤ったエンコード名が含まれている場合、形式の設定に対する変更を保存すると、エラーがスローされます。

![形式デザイナー ページでルート要素を追加する。](./media/er-suppress-bom-characters-image1.gif)

エンコードとして **UTF-8**、**UTF-16**、または **UTF-32** を指定すると、**BOM 文字の非表示** オプションが使用可能になります。 このオプションを **はい** に設定して、編集可能な ER 形式の実行時に、実行時に生成される発信ファイルで [バイト オーダー マーク (BOM) 文字](/globalization/encoding/byte-order-mark) を非表示にします。

> [!NOTE]
> **エンコード** フィールドを空白のままにすると、既定の **UTF-8** エンコードが使用されます。

![形式デザイナー ページで BOM 文字の非表示オプションを設定する。](./media/er-suppress-bom-characters-image2.gif)

実行時に機能を確認するには、適切な手順を実行します。 たとえば、[ER 形式における XML 要素の実行の延期](er-defer-xml-element.md) トピックの手順を実行します。 そのトピックにある [計算が生成された出力に基づくように形式を変更する](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) セクションの手順を完了したら、次の追加手順に従います。

1. UTF エンコードを指定します:

    1. **Common\\File** タイプの **レポート** 要素を選択します。
    2. **エンコード** フィールドで 、**UTF-8** のエンコードを指定します。

2. BOM 文字を含む XML ファイルを生成します:

    1. **BOM 文字の非表示** オプションを **いいえ** に設定して、生成された XML ファイルに BOM 文字を含めます。
    2. [電子申告形式における XML 要素の実行の延期](er-defer-xml-element.md) トピックの [計算された合計が使用されるように集計 XML 要素の実行を延期](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) セクションの手順を完了し、生成されたファイルを **SampleXmlReport.xml** として保存します。

3. BOM 文字を含まない XML ファイルを生成します:

    1. **BOM 文字の非表示** オプションを **はい** に設定して、生成された XML ファイルで BOM 文字を非表示にします。
    2. [電子申告形式における XML 要素の実行の延期](er-defer-xml-element.md) トピックの [計算された合計が使用されるように集計 XML 要素の実行を延期](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) セクションの手順を完了し、生成されたファイルを **SampleXmlReport (1).xml** として保存します。

4. ファイル比較ユーティリティで、生成されたファイルを比較します。

    最初に気付く違いは、ファイル ヘッダーにあります。 SampleXmlReport.xml ファイルには BOM 文字が含まれていますが、SampleXmlReport (1).xml ファイルには含まれていません。

    ![ファイル比較ユーティリティを使用して生成されたファイルを比較する。](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a>参照

- [電子申告形式における XML 要素の実行の延期](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
