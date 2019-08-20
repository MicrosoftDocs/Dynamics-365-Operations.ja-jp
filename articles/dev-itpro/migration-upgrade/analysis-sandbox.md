---
title: 'AX 2012 からのアップグレード: 分析のためのデモ環境の展開'
description: このトピックでは、Microsoft Dynamics AX 2012 から Dynamics 365 for Finance and Operations にアップグレードするためのプロジェクトの解析フェーズ中に、デモ環境を展開する理由および方法を説明します。
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
ms.openlocfilehash: 74785f1e3167a80910ff9adb88d84e32b6399e62
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851793"
---
# <a name="upgrade-from-ax-2012---deploy-a-demo-environment-for-analysis"></a>AX 2012 からのアップグレード: 分析のためのデモ環境の展開

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

このトピックでは、Microsoft Dynamics AX 2012 から Microsoft Dynamics 365 for Finance and Operations にアップグレードするためのプロジェクトの解析フェーズ中に、デモ環境を展開する理由および方法を説明します。

デモの Finance and Operations 環境を配置することにより、プログラムの実践的な経験を積むことができ、興味のある新機能を活用できます。 また、業務プロセス用プログラムで違いを検証する機会があるため、ギャップの可能性を識別またはギャップが存在しないことを確認することができます。 アップグレード プロジェクトのこのステージでは、データとコードを環境内で使用することができません。 したがって、すべてがビジネス プロセスに準拠していることを検証する能力は限られています。 ただし、この手順はその認定作業での最初の手順です。

Finance and Operations のライセンスをまだ購入しておらず、無料トライアルを使用している場合は、[Microsoft Dynamics 365 for Finance and Operations を展開する](../deployment/deploy-demo-environment.md)の手順に従い、自分で持ち込む Microsoft Azure サブスクリプションにデモ環境を展開することができます。

Finance and Operations のライセンスを既に購入している場合、Microsoft Dynamics Lifecycle Services (LCS) で特殊なタイプのプロジェクト (実装プロジェクト) を構成するためのリンクを受け取ります。 実装プロジェクトにより、開発者/テスト環境とサンドボックス環境を配置できます。 このタイプの環境の配置の詳細については、[サンドボックス環境でデータのアップグレード](upgrade-data-sandbox.md) を参照してください。
