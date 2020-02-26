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
ms.openlocfilehash: 0d32a5f7859f0200da823a73d94b9a6b2a9c8e7d
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019876"
---
# <a name="integrated-tax"></a>統合された税

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

税設定データでは、間接税 (VAT、GST、売上税) および源泉徴収税の両方の設定が定義されます。 税金計算ルール、税率、税務会計、決済、およびその他の概念について説明します。

## <a name="templates"></a>テンプレート

次の表に示すように、税データには、データ操作中に連携して動作するエンティティ マップのコレクションが含まれています。

Finance and Operations   | その他の Dynamics 365 アプリ
-------------------------|---------------------------------
税コード                  | msdyn\_taxcodes.md
税グループ               | msdyn\_taxgroups.md
税品目グループ          | msdyn\_taxitemgroups.md
免税           | msdyn\_taxexemptcodes.md
税務当局          | msdyn\_taxauthorities.md
源泉徴収税コード      | msdyn\_withholdingtaxcodes.md
源泉徴収税グループ   | msdyn\_withholdingtaxgroups.md
税勘定科目グループ | msdyn\_taxpostinggroups  

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

