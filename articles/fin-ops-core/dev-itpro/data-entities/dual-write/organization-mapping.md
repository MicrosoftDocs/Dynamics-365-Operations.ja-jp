---
title: Dataverse の組織階層
description: この記事では、財務と運用アプリと Dataverse 間の組織データの統合について説明します。
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 2f900637855bee3e21916652a373c683e6bf1392
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112021"
---
# <a name="organization-hierarchy-in-dataverse"></a>Dataverse の組織階層

[!include [banner](../../includes/banner.md)]



Dynamics 365 Finance は財務システムであるため、*組織* は中核的な概念であり、システムの設定は組織階層の構成から始まります。 ビジネスの財務は、組織レベルおよび組織階層内のすべてのレベルで追跡できます。

Dataverse は組織階層の概念はないが、総売上高など、いくつかの緩い概念はあります。 Dataverse 統合の一環として、組織階層データ構造が Dataverse に追加されます。

## <a name="data-flow"></a>データ フロー

財務と運用アプリおよび Dataverse を構成するビジネス エコシステムは、組織階層を持ち続けます。 この組織階層は財務と運用アプリに基づいて構築されていますが、情報と拡張目的のために Dataverse で公開されています。 次の図は、財務と運用アプリから Dataverse に一方向のデータ フローとして Dataverse 内に公開される、組織階層の情報を示します。

![アーキテクチャ イメージ。](media/dual-write-data-flow.png)

組織階層のテーブル マップは、財務と運用アプリから Dataverse へのデータの一方向の同期に使用できます。

## <a name="templates"></a>テンプレート

組織とは、業務プロセスを実行や目標の達成を協力して行う人々の集まりです。 組織階層とは、業務を構成する組織の関係を表すものです。 法人、作業単位、およびチームという内部組織のタイプを定義できます。 次の表に示すように、テーブル マップのコレクションが法人、営業単位、および関連するまたは認識階層の情報を同期するために作成されます。

財務と運用アプリ | Customer Engagement アプリ     | Description
-----------------------|--------------------------------|---
[法人](mapping-reference.md#102) | cdm_companies | 
[法人](mapping-reference.md#142) | msdyn_internalorganizations |
[作業単位](mapping-reference.md#143) | msdyn_internalorganizations |
[組織階層 - 公開済み](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | このテンプレートでは、組織階層の公開済みテーブルの一方向の同期を行うことができます。
[組織階層の目的](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | このテンプレートでは、組織階層目的テーブルの一方向の同期を行うことができます。
[組織階層タイプ](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | このテンプレートでは、組織階層タイプ テーブルの一方向の同期を行うことができます。

## <a name="internal-organization"></a>内部組織

Dataverse の内部組織情報は、**作業単位** と **法人エンティティ** の 2 つのテーブルから来ています。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

