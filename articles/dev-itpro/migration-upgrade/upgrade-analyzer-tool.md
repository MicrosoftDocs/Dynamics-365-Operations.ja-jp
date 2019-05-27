---
title: AX 2012 からのアップグレード - アップグレード アナライザー ツールを使用した計画
description: このトピックでは、アップグレード アナライザー ツールを使用して、Dynamics AX2012 から Dynamics 365 for Finance and Operations へのアップグレードを計画する方法について説明します。
author: tariqbell
manager: AnnBe
ms.date: 01/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 106163
ms.assetid: ''
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-05-31
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: c1e51d35bb01dc91ceaca2afb50c205419dd3e4c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537358"
---
# <a name="upgrade-from-ax-2012---plan-by-using-the-upgrade-analyzer-tool"></a>AX 2012 からのアップグレード - アップグレード アナライザー ツールを使用した計画

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

このトピックでは、アップグレード アナライザー ツールを使用して、Microsoft Dynamics AX 2012 から Microsoft Dynamics 365 for Finance and Operations へのアップグレードを計画する方法について説明します。 このツールは、AX 2012 環境に対して実行され、 Finance and Operations サブスクリプション コストの削減を助けるために、AX 2012 内でクリーンアップする必要のあるデータを識別します。 このツールは、アップグレード プロセスのスピードアップに役立つ SQL 構成の最適化を提案します。 また、AX 2012 で使用する機能が Finance and Operations で廃止されている場合は、このツールが警告します。 したがって、これらの機能を置き換える方法や回避する方法を計画できます。

アップグレード アナライザーは、Microsoft Dynamics Lifecycle Services (LCS) の通常のシステム診断サービスの一部として、AX 2012 環境からデータを収集します。 システム診断サービスの概要、および LCS を通じて使用できるようにデータを収集しクラウドに押し戻す方法に関する情報については、[システム診断 (AX 2012)](../lifecycle-services/ax-2012/system-diagnostics-lcs.md) を参照してください。

LCS の Microsoft Power BI レポートでは、システム診断サービスの結果を表示できます。 レポートには、AX 2012 環境で完了する必要のあるタスクのリストが表示されます。

アップグレード分析レポートにアクセスするには、https://diag.lcs.dynamics.com/UpgradeAnalysisReport/Report/"ProjectID" に移動します ("ProjectID" を現在のプロジェクト ID で置き換えます。これは現在の LCS プロジェクトの URL にある整数です)。

次の図は、アップグレード アナライザーを使用する手順の概要を示しています。

![アナライザー プロセスのアップグレード](media/upgradeAnalyzerProcess.png)

AX 2012 環境内のシステム診断サービスを既に使用している場合は、既存のコンピューターとは異なるコンピューターで、サービスの新しいインスタンスをコンフィギュレーションする必要があります。

AX 2012 環境内のシステム診断サービスをコンフィギュレーションする方法の詳細については、[システム診断のインストールと実行 (AX 2012)](../lifecycle-services/ax-2012/install-run-system-diagnostics-lcs.md) を参照してください。

システム診断サービスを構成してから数分で、AX 2012 環境が LCS プロジェクトに表示されます。
