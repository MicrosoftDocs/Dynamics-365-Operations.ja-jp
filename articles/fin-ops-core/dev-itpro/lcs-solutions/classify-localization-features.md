---
title: ローカリゼーション機能の分類
description: このトピックでは、規制機能と競合機能の違いについて説明し、その機能のタイトルにどのように機能タイプが使用されるかを示します。
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.custom: 27601
ms.assetid: 7e2031b4-a092-482e-a76d-1e582edecd86
ms.search.region: global
ms.author: janeaug
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7904f11cbd4a2578c1d4789b8efcb441376f7dd5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749277"
---
# <a name="classification-of-localization-features"></a>ローカライズ機能の分類

[!include [banner](../includes/banner.md)]

ローカライズおよび翻訳向け LCS ソリューションの要件の一部として、ローカライズ機能は Microsoft Dynamics Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM) ライブラリで規制または競合として分類される必要があります。 この記事では、これらの 2 つのタイプの機能の違いについて説明し、その機能のタイトルにどのように機能タイプが使用されるかを示します。

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

BPMの詳細については、 [ユーザー定義の業務プロセスをビジネス プロセス モデラー (BPM) にアップロードする](../lifecycle-services/upload-business-processes-bpm-task-recorder.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

- [グローバリゼーション リソース](country-region.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]