---
title: AX 2012 からのアップグレード - コードのアップグレード サービスを使用した工数見積
description: このトピックでは、LCS のコード アップグレード サービスを使用して、Microsoft Dynamics AX 2012 から Finance and Operations にコード基準をアップグレードするために必要なタスクと工数を見積もる方法について説明します。
author: tariqbell
manager: AnnBe
ms.date: 01/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 106163
ms.assetid: ''
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-05-31
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 0b1ab85e61edf67e05682f697c2ba1b0ffb6e236
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811957"
---
# <a name="upgrade-from-ax-2012---estimate-effort-by-using-the-code-upgrade-service"></a>AX 2012 からのアップグレード - コードのアップグレード サービスを使用した工数見積

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) のコード アップグレード サービスを使用して、Microsoft Dynamics AX 2012 から Finance and Operations にコード基準をアップグレードするために必要なタスクと工数を見積もる方法を説明します。

コード アップグレード サービスは、AX 2012 モデル ストアのエクスポートを適切な形式に変換します。 ただし、サービスが識別してもまだ独自で解決できない問題を開発者が解決するまで、コードの新しいバージョンは完全に機能しません。

コード アップグレード サービスは、これらのアクションを実行します。

- いくつかのタイプの競合問題を直接解決します。
- その他の問題については、Microsoft Azure DevOps タスクにログ記録します。
- 適切な形式でコード バージョンを作成し、Azure DevOps プロジェクトの新しい分岐への新しいバージョンを確認します。

分析フェーズでは、レポートを使用してコード変換アクティビティを完了するために必要な作業量を見積もります。

次の図は、コードのアップグレード サービスを構成するプロセスの概要を示しています。

![コード アップグレード サービスのコンフィギュレーション プロセス](media/codeUpgradeConfigurationProcess.png)

コード アップグレード サービスを構成する方法については、 [Lifecycle Services (LCS) で、コード アップグレード サービスを構成する](../lifecycle-services/configure-execute-code-upgrade.md) を参照してください。

コード アップグレード サービスの出力は、開発者が使用するように設計されています。 この出力は、開発者がコードのアップグレード タスクを完了するために必要な工数を見積もるのに役立ちます。 見積もりを作成するには、サービスが Azure DevOps で生成するタスクと、サービスが生成する新しいバージョンのコードを確認する必要があります。
