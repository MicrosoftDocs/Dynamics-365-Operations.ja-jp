---
title: 事業継続とディザスター リカバリー
description: このトピックでは、Azure リージョンの広範囲で稼働停止が発生した場合に Microsoft が Microsoft Dynamics 365 SaaS アプリケーションの実稼働インスタンスに対して提供する、事業の継続性と障害復旧について説明します。
author: MicroSri
ms.date: 07/13/2021
ms.topic: article
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sriknair
ms.search.validFrom: 2021-07-31
ms.openlocfilehash: 7f87b293ab67a34d88a85a1317469d4bf42596d4
ms.sourcegitcommit: 7aa7d756e1e98a53da62e03c608a9597ef9893ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/20/2021
ms.locfileid: "7404125"
---
# <a name="business-continuity-and-disaster-recovery"></a>事業の継続性と障害復旧

[!include[banner](../includes/banner.md)]

Microsoft Azure の地域の広範囲で稼働停止が発生した場合、Microsoft は、Dynamics 365 のサービスとしてのソフトウェア (SaaS) アプリケーションの実稼働インスタンスに対して、事業の継続性と障害復旧を提供します。

適切なライセンスを購入した顧客は、Finance and Operations アプリケーションの実稼働インスタンスを配置することができます。 詳細については、[クラウド配置の概要](../deployment/cloud-deployment-overview.md)を参照してください。

実稼働環境では、配置時にセカンダリ地域に異なるストレージ サービスの複製 (Azure SQL Database およびファイル ストレージ) が作成されます。 これらの複製は、*geo-secondaries* と呼ばれます。

geo-secondaries は、継続的なデータ レプリケーションを通じてプライマリ インスタンスと同期されます。 geo-secondaries とプライマリ インスタンスとの間には、レプリケーションの待機時間が少し、または最大 15 分のラグがあります。 詳細については、[事業の継続性と障害復旧 (BCDR): Azure Paired Regions](/azure/best-practices-availability-paired-regions) を参照してください。

![Geo-secondaries](media/Finance-and-Operations-apps.png)

非実稼働環境でのデータ保護に関する詳細については、[データベース移動操作ホーム ページ](../database/dbmovement-operations.md)を参照してください。

## <a name="planned-failover"></a>計画フェールオーバー

主要な Azure リージョンの可用性に危険があると Microsoft が判断した場合 (たとえば、ハリケーンが差し迫っている場合など)、顧客に通知し、環境を切り替えてセカンダリ地域から動作するようにします。 環境がセカンダリ地域で構成されている間、短時間、稼働停止します。 ただし、両方の Azure リージョンがオンラインであり、レプリケーションが実行されるため、データが失われる可能性はありません。

## <a name="unplanned-failover"></a>予定外のフェールオーバー

地域の広範囲にわたって予想せぬ稼働停止が発生し (たとえば、地震などの自然災害など)、Microsoft が妥当な時間内に使用可能にならないと判断した場合、顧客に通知し、環境を切り替えてセカンダリ地域から動作するようにします。 この場合、稼働停止の性質とタイミングによっては、最大 15 分間、顧客データの損失を経験することがあります。

> [!IMPORTANT]
> セカンダリ地域から環境が運用されている間、Finance and Operations アプリ環境では機能が制限されます。 Financial Reporting および Power BI Reporting は使用できません。 災害の間、顧客にとって Financial Reporting が重要である場合、顧客はサポート チケットを通して Microsoft にサービスの復元を要求することができます。
>
> また、非実稼働インスタンスのサービスが低下することがあります。 新しい非実稼働環境の配置がブロックされることがあります。

## <a name="failback"></a>フェールバック

プライマリ地域がオンラインに戻り、完全に運用していると Microsoft が判断した場合、顧客に通知し、環境を切り替えて、再度プライマリ地域から機能できるようにします。 すべての非実稼働インスタンスを含め、サービスが完全に復元されます。 データが失われる可能性はありません。
