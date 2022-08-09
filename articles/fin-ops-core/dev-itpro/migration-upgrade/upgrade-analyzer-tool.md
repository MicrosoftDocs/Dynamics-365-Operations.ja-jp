---
title: AX 2012 からのアップグレード - アップグレード アナライザー ツールを使用した計画
description: この記事では、アップグレード アナライザー ツールを使用して、Dynamics AX 2012 からアップグレードを計画する方法について説明します。
author: tariqbell
ms.date: 01/31/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 106163
ms.assetid: ''
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2017-05-31
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: faee06c3790ec474191522157fa3c2877f65879c
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124728"
---
# <a name="upgrade-from-ax-2012---plan-by-using-the-upgrade-analyzer-tool"></a>AX 2012 からのアップグレード - アップグレード アナライザー ツールを使用した計画

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

この記事では、アップグレード アナライザー ツールを使用して、Microsoft Dynamics AX 2012 からアップグレードを計画する方法について説明します。 このツールは、AX 2012 環境に対して実行され、財務と運用アプリのサブスクリプション コストの削減を助けるために、AX 2012 内でクリーンアップする必要のあるデータを識別します。 このツールは、アップグレード プロセスのスピードアップに役立つ SQL 構成の最適化を提案します。 また、AX 2012 で使用する機能が現在のバージョンで廃止されている場合は、このツールが警告します。 したがって、これらの機能を置き換える方法や回避する方法を計画できます。

アップグレード アナライザーは、Dynamics Lifecycle Services (LCS) の通常のシステム診断サービスの一部として、AX 2012 環境からデータを収集します。 システム診断サービスの概要、および LCS を通じて使用できるようにデータを収集しクラウドに押し戻す方法に関する情報については、[Lifecycle Services (LCS) のシステム診断](/dynamicsax-2012/appuser-itpro/system-diagnostics-lifecycle-services-lcs)を参照してください。

LCS の Microsoft Power BI レポートでは、システム診断サービスの結果を表示できます。 レポートには、AX 2012 環境で完了する必要のあるタスクのリストが表示されます。

アップグレード分析レポートにアクセスするには、https://diag.lcs.dynamics.com/UpgradeAnalysisReport/Report/"ProjectID" に移動します ("ProjectID" を現在のプロジェクト ID で置き換えます。これは現在の LCS プロジェクトの URL にある整数です)。

次の図は、アップグレード アナライザーを使用する手順の概要を示しています。

![アナライザー プロセスのアップグレード。](media/upgradeAnalyzerProcess.png)

AX 2012 環境内のシステム診断サービスを既に使用している場合は、既存のコンピューターとは異なるコンピューターで、サービスの新しいインスタンスをコンフィギュレーションする必要があります。

AX 2012 環境内のシステム診断サービスをコンフィギュレーションする方法の詳細については、[システム診断のインストールと実行](/dynamicsax-2012/appuser-itpro/install-run-system-diagnostics)を参照してください。

システム診断サービスを構成してから数分で、AX 2012 環境が LCS プロジェクトに表示されます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
