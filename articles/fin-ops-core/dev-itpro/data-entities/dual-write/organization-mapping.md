---
title: Dataverse の組織階層
description: このトピックでは、Finance and Operations アプリと Dataverse 間の組織データの統合について説明します。
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 5132fd85fdf2c08ccded9db590328c394a2f984e
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744696"
---
# <a name="organization-hierarchy-in-dataverse"></a>Dataverse の組織階層

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Finance は財務システムであるため、*組織* は中核的な概念であり、システムの設定は組織階層の構成から始まります。 ビジネスの財務は、組織レベルおよび組織階層内のすべてのレベルで追跡できます。

Dataverse は組織階層の概念はないが、総売上高など、いくつかの緩い概念はあります。 Dataverse 統合の一環として、組織階層データ構造が Dataverse に追加されます。

## <a name="data-flow"></a>データ フロー

Finance and Operations アプリと Dataverse を構成するビジネス エコシステムは、組織階層を持ち続けます。 この組織階層は Finance and Operations アプリに基づいて構築されていますが、情報と拡張目的のために Dataverse で公開されています。 次の図は、Finance and Operations アプリから Dataverse に一方向のデータ フローとして Dataverse 内に公開される、組織階層の情報を示します。

![アーキテクチャ イメージ](media/dual-write-data-flow.png)

組織階層のテーブル マップは、Finance and Operations アプリから Dataverse へのデータの一方向の同期に使用できます。

## <a name="templates"></a>テンプレート

製品情報には、製品分析コードや追跡、保管分析コードなど、製品とその定義に関連するすべての情報が含まれます。 次のテーブルが示すように、製品と関連する情報を同期するためにテーブル マップのコレクションが作成されます。

Finance and Operations アプリ | その他の Dynamics 365 アプリ | 説明
-----------------------|--------------------------------|---
組織階層の目的 | msdyn_internalorganizationhierarchypurposes | このテンプレートでは、組織階層目的テーブルの一方向の同期を行うことができます。
組織階層タイプ | msdyn_internalorganizationhierarchytypes | このテンプレートでは、組織階層タイプ テーブルの一方向の同期を行うことができます。
組織階層 - 公開済み | msdyn_internalorganizationhierarchies | このテンプレートでは、組織階層の公開済みテーブルの一方向の同期を行うことができます。
作業単位 | msdyn_internalorganizations |
法人 | msdyn_internalorganizations |
法人 | cdm_companies | 法人 (会社) 情報の双方向の同期を提供します。

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a>内部組織

Dataverse の内部組織情報は、**作業単位** と **法人エンティティ** の 2 つのテーブルから来ています。

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
