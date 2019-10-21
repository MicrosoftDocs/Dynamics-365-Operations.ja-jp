---
title: ローカライズ機能の分類
description: ローカライズ &amp; 翻訳向け LCS ソリューションの要件の一部として、ローカライズ機能は Microsoft Dynamics Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM) ライブラリで規制、または競合のいずれかに分類される必要があります。 この記事では、これらの 2 つのタイプの機能の違いについて説明し、その機能のタイトルにどのように機能タイプが使用されるかを示します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 27601
ms.assetid: 7e2031b4-a092-482e-a76d-1e582edecd86
ms.search.region: global
ms.author: janeaug
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b883d9246f35539e3bae14b0a9171e49c7534c73
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183280"
---
# <a name="classification-of-localization-features"></a>ローカライズ機能の分類

[!include [banner](../includes/banner.md)]

ローカライズ &amp; 翻訳向け LCS ソリューションの要件の一部として、ローカライズ機能は Microsoft Dynamics Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM) ライブラリで規制、または競合のいずれかに分類される必要があります。 この記事では、これらの 2 つのタイプの機能の違いについて説明し、その機能のタイトルにどのように機能タイプが使用されるかを示します。

ローカライズ機能は、Microsoft Dynamics Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM) ライブラリで規制または競合として分類される必要があります。 次の定義は、2 つのタイプの機能を区別するのに役立ちます。

-   **規制機能** – 特定の国/地域で業務を行う組織は、日々の業務トランザクションや工程に関して、国/地域固有の法律や規制を遵守する必要があり、その国/地域で実施される活動についての法的義務を満たしている必要があります。 これらの法律および規制は強制され、遵守しない場合、その国/地域で事業を行う組織にとって深刻な結果につながる可能性があります。
-   **競合機能** - このカテゴリには、前述の定義に従って規制機能とは見なされないその他のすべての機能が含まれます。

BPM ライブラリが構築されているときは、ローカライズ ソリューションの機能のタイトルで、各機能のタイプを区別する必要があります。 このタイトルのラベルは、次のテーブルに示すように、接頭辞による国/地域および機能タイプを示す次の命名規則に準拠します。

| フィーチャー タイプ | 書式設定                | 例                             |
|--------------|-----------------------|-------------------------------------|
| 規制   | XX-REG-Feature タイトル  | PT-REG-直接売上税レポート      |
| 競合  | XX-COMP-Feature タイトル | PT-COMP-国内銀行支払形式 |

次のテーブルに、名前付け規則のコンポーネントを示します。

| コンポーネント名      | 書式設定      | 説明                                                                                                                   | 例                 |
|---------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| 国/地域コード | XX          | 2 文字の ISO 国/地域コード ([ISO 3166 規格](https://www.iso.org/iso/country_names_and_code_elements)) | PT (= ポルトガル)         |
| フィーチャー タイプ        | REG または COMP | 機能のタイプ                                                                                                           | REG                     |
| フィーチャー名        | テキスト        | 機能がどのように使用されているかを説明する短い機能タイトル                                                             | 直接売上税レポート |

BPM の詳細については、[BPM に業務プロセスをアップロード](../lifecycle-services/upload-business-processes-bpm-task-recorder.md) を参照してください。

## <a name="additional-resources"></a>その他のリソース

- [ローカライズと規制の機能](country-region.md)

