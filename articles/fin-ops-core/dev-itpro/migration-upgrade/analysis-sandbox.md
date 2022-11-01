---
title: 'AX 2012 からのアップグレード: 分析のためのデモ環境の展開'
description: この記事では、Microsoft Dynamics AX 2012 から財務と運用にアップグレードする分析フェーズ中に、デモ環境を配置する方法について説明します。
author: sericks007
ms.date: 01/31/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2017-05-31
ms.dyn365.ops.version: Platform update 8
ms.custom: 106163
ms.assetid: ''
ms.openlocfilehash: 846ce1b8833e505e4a3eb520c525bd74e959dd6d
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/20/2022
ms.locfileid: "9702172"
---
# <a name="upgrade-from-ax-2012---deploy-a-demo-environment-for-analysis"></a>AX 2012 からのアップグレード: 分析のためのデモ環境の展開

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

この記事では、Microsoft Dynamics AX 2012 から財務と運用にアップグレードするためのプロジェクトの解析フェーズ中に、デモ環境を展開する理由および方法を説明します。

デモの財務と運用環境を配置することにより、プログラムの実践的な経験を積むことができ、興味のある新機能を活用できます。 また、業務プロセス用プログラムで違いを検証する機会があるため、ギャップの可能性を識別またはギャップが存在しないことを確認することができます。 アップグレード プロジェクトのこのステージでは、データとコードを環境内で使用することができません。 したがって、すべてがビジネス プロセスに準拠していることを検証する能力は限られています。 ただし、この手順はその認定作業での最初の手順です。

ライセンスをまだ購入しておらず、無料トライアルを使用している場合は、 [デモ環境の配置](../deployment/deploy-demo-environment.md) の手順に従い、自分で持ち込む Microsoft Azure サブスクリプションにデモ環境を配置できます。

ライセンスを既に購入している場合、Microsoft Dynamics Lifecycle Services (LCS) で特殊なタイプのプロジェクト (実装プロジェクト) を構成するためのリンクを受け取ります。 実装プロジェクトにより、開発者/テスト環境とサンドボックス環境を配置できます。 このタイプの環境の配置の詳細については、[AX 2012 アップグレード - サンドボックス環境でのデータ アップグレード](/d365F-O/fin-ops-core/dev-itpro/migration-upgrade/data-upgrade-self-service) を参照してください。

> [!IMPORTANT]
> アップグレードを実行する前に、使用している Dynamics 365 バージョンの最新の **品質更新プログラム** を適用してください。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
