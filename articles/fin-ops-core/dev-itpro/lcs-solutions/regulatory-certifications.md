---
title: 機能タイトルの規制証明情報
description: この記事では、機能のタイトルで認証に関する情報を使用する方法について説明します。
author: kfend
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 27581
ms.assetid: d0b8286a-b2c1-4fa2-905a-3383b1d34d56
ms.openlocfilehash: d79a9b47bdaa22eeb789443ff04424081fbc451c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284462"
---
# <a name="regulatory-certification-information-in-feature-titles"></a>機能タイトルの規制認証情報

[!include [banner](../includes/banner.md)]

ローカライズ &amp; 翻訳向け LCS ソリューションの要件の一部として、ローカライズ ISV ソリューション プロバイダーは意図したマーケットでの販売を、法律に準拠したものにするために。ソリューションが必要とする規制認証に関する詳細を含める必要があります。 この記事では、機能のタイトルに認証に関する情報をどのように使用しているかを示します。

規制証明には、データ プライバシーから特定の規制に準拠する認定まで。さまざまな形式があります。 ただし、すべての規制認証にある共通の 1 つの点は、実施するの国/地域の法令や規制によって要求されるということです。 これらの認定は強制され、遵守しない場合、その国/地域で事業を行う組織にとって深刻な結果につながる可能性があります。 業務プロセス ライブラリが構築されたとき、規制認証は、ローカライズ ソリューション機能のタイトルによって、Microsoft Dynamics Lifecycle Services (LCS) の業務プロセス モデラー (BPM) ライブラリの規制に関する要件として識別する必要があります。 このタイトルのラベルは、次のテーブルに示すように、接頭辞による国/地域および認証タイプを示す次の命名規則に準拠します。

| フィーチャー タイプ | 書式設定                      | 例                                  |
|--------------|-----------------------------|------------------------------------------|
| 規制   | xx 用 XX-REG-Certification | PT-REG-会計プリンターの証明 |

次のテーブルに、名前付け規則のコンポーネントを示します。

| コンポーネント名      |  書式設定 | 説明                                                                                                                   | 例                           |
|---------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| 国/地域コード | XX      | 2 文字の ISO 国/地域コード ([ISO 3166 規格](https://www.iso.org/iso/country_names_and_code_elements)) | PT (= ポルトガル)                   |
| フィーチャー タイプ        | REG     | 機能のタイプ                                                                                                           | REG                               |
| 証明の名前  | テキスト    | 証明書とそのアプリケーションを説明する短いタイトル                                                            | 会計プリンターの証明 |

BPM の業務プロセス ライブラリでは、**APQC レベル 8.0 財務リソースの管理 (10009)** に認証を配置する必要があります。 

**例**

-   APQC レベル 8.0 財務リソースの管理 (10009)
    -   PT-REG-会計プリンターの証明

BPM の詳細については、[ビジネス プロセス モデラー (BPM) のフローチャート](../lifecycle-services/flowcharts-business-process-modeler.md) を参照してください。





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
