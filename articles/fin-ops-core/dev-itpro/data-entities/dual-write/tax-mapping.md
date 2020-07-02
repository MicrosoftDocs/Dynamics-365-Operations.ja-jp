---
title: 統合された税
description: このトピックでは、Finance and Operations と Common Data Service 間の税データの統合について説明します。
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 69521ec8c664a7025050c94105eca58f7f2c5c00
ms.sourcegitcommit: 7d943499f302298c6ff127f56cecc34af6cee289
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/08/2020
ms.locfileid: "3435563"
---
# <a name="integrated-tax"></a>統合された税

[!include [banner](../../includes/banner.md)]



税設定データでは、間接税 (VAT、GST、売上税) および源泉徴収税の両方の設定が定義されます。 税金計算ルール、税率、税務会計、決済、およびその他の概念について説明します。

## <a name="templates"></a>テンプレート

次の表に示すように、税データには、データ操作中に連携して動作するエンティティ マップのコレクションが含まれています。

Finance and Operations アプリ | Dynamics 365 のモデル駆動型アプリ | 説明 |
-------------------------|---------------------------------|----|
品目売上税グループ | msdyn_taxitemgroups |
消費税所轄官庁 | msdyn_taxauthorities |
消費税非課税コード エンティティ CDS | msdyn_taxexemptcodes |
消費税グループ | msdyn_taxgroups |
消費税元帳転記グループ V2 | msdyn_taxpostinggroups |
源泉徴収税コード | msdyn_withholdingtaxcodes |
源泉徴収税グループ | msdyn_withholdingtaxgroups | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

