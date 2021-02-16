---
title: 統合された税
description: このトピックでは、Finance and Operations と Dataverse 間の税データの統合について説明します。
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 14c22dd6602b5fbf866c8dc6b057f6c8acb1f48f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679299"
---
# <a name="integrated-tax"></a>統合された税

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



税設定データでは、間接税 (VAT、GST、売上税) および源泉徴収税の両方の設定が定義されます。 税金計算ルール、税率、税務会計、決済、およびその他の概念について説明します。

## <a name="templates"></a>テンプレート

次の表に示すように、税データには、データ操作中に連携して動作するテーブル マップのコレクションが含まれています。

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

