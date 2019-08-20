---
title: Common Data Service の組織階層
description: このトピックでは、Finance and Operations と Common Data Service 間の組織データの統合について説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca2ac0f9dbb8544b12f23a271423a43b0e601272
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789213"
---
## <a name="organization-hierarchy-in-common-data-service"></a>Common Data Service の組織階層

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Microsoft Dynamics 365 for Finance and Operations は財務システムであるため、*組織*は中核的な概念であり、システムの設定は組織階層の構成から始まります。 その後、ビジネスの Financials and Operations は、組織レベルおよび組織階層内の任意のレベルで追跡できます。

Common Data Service は組織階層の概念はないが、総売上高など、いくつかの緩い概念はあります。 Common Data Service 統合の一環として、組織階層データ構造が Common Data Service に追加されます。

## <a name="data-flow"></a>データ フロー

Finance and Operations と Common Data Service を構成するビジネス エコシステムは、組織階層を持ち続けます。 この組織階層は Finance and Operations に基づいて構築されていますが、情報と拡張目的の Common Data Service で公開されています。 次の図は、Finance and Operations から Common Data Service に一方行のデータ フローとして Common Data Service 内に公開される、組織階層の情報を示します。

![アーキテクチャ イメージ](media/dual-write-data-flow.png)

## <a name="templates"></a>テンプレート

組織階層のエンティティ マップは、Finance and Operations から Common Data Service にデータの一方向の同期に使用できます。

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a>内部の組織階層の目的

このテンプレートは、Finance and Operations から Dynamics 365 for Customer Engagement への組織階層目的エンティティの一方行の同期を提供します。

<!-- ![architecture image](media/dual-write-purpose.png) -->

ソース フィールド | タイプのマッピング | 出力先フィールド
---|---|---
HIERARCHYTYPE | \> | msdyn\_hierarchypurposetypename
HIERARCHYTYPE | \> | msdyn\_hierarchytype.msdyn\_name
HIERARCHYPURPOSE | \>\> | msdyn\_hierarchypurpose
IMMUTABLE | \>\> | msdyn\_immutable
SETASDEFAULT | \>\> | msdyn\_setasdefault

## <a name="internal-organization-hierarchy-type"></a>内部の組織階層タイプ

このテンプレートは、Finance and Operations から Customer Engagement への組織階層タイプ エンティティの一方行の同期を提供します。

<!-- ![architecture image](media/dual-write-type.png) -->

ソース フィールド | タイプのマッピング | 出力先フィールド
---|---|---
名前 | \> | msdyn\_name

## <a name="internal-organization-hierarchy"></a>内部の組織階層

このテンプレートは、Finance and Operations から Customer Engagement への組織階層の公開済みエンティティの一方行の同期を提供します。

<!-- ![architecture image](media/dual-write-organization.png) -->

ソース フィールド | タイプのマッピング | 出力先フィールド
---|---|---
VALIDTO | \> | msdyn\_validto
VALIDFROM | \> | msdyn\_validfrom
HIERARCHYTYPE | \> | msdyn\_hierarchytypename
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentpartyid
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childpartyid
HIERARCHYTYPE | \> | msdyn\_hierarchytypeid.msdyn\_name
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childid.msdyn\_partynumber
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentid.msdyn\_partynumber

## <a name="internal-organization"></a>内部組織

Common Data Service の内部組織情報は、**作業単位**と**法人エンティティ**の 2 つの Finance and Operations エンティティから来ています。

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a>作業単位

ソース フィールド | タイプのマッピング | 出力先フィールド
---|---|---
LANGUAGEID | \> | msdyn\_languageid
NAMEALIAS | \> | msdyn\_namealias
名前 | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
OPERATINGUNITTYPE | \>\> | msdyn\_type

### <a name="legal-entity"></a>法人エンティティ

ソース フィールド | タイプのマッピング | 出力先フィールド
---|---|---
NAMEALIAS | \> | msdyn\_namealias
LANGUAGEID | \> | msdyn\_languageid
名前 | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
なし | \>\> | msdyn\_type
LEGALENTITYID | \> | msdyn\_companycode

## <a name="company"></a>法人

Finance and Operations と Customer Engagement の間の法人 (会社) 情報の双方向同期を提供します。

<!-- ![architecture image](media/dual-write-company.png) -->

ソース フィールド | タイプのマッピング | 出力先フィールド
---|---|---
名前 | = | cdm\_name
LEGALENTITYID | = | cdm\_companycode
