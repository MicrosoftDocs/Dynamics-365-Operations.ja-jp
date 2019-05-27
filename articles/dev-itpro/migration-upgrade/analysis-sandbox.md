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
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 106163
ms.assetid: ''
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-05-31
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: f0ff9929cafbbe84ca56ba05cf09e6d20d359c64
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537206"
---
# <a name="upgrade-from-ax-2012---deploy-a-demo-environment-for-analysis"></a><span data-ttu-id="04a15-103">AX 2012 からのアップグレード: 分析のためのデモ環境の展開</span><span class="sxs-lookup"><span data-stu-id="04a15-103">Upgrade from AX 2012 - Deploy a demo environment for analysis</span></span>

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

<span data-ttu-id="04a15-104">このトピックでは、Microsoft Dynamics AX 2012 から Microsoft Dynamics 365 for Finance and Operations にアップグレードするためのプロジェクトの解析フェーズ中に、デモ環境を展開する理由および方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="04a15-104">This topic explains why and how you should deploy a demo environment during the Analyze phase of your project for upgrading from Microsoft Dynamics AX 2012 to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="04a15-105">デモの Finance and Operations 環境を配置することにより、プログラムの実践的な経験を積むことができ、興味のある新機能を活用できます。</span><span class="sxs-lookup"><span data-stu-id="04a15-105">By deploying a demo Finance and Operations environment, you gain hands-on experience with the program and can explore new features that you might be interested in.</span></span> <span data-ttu-id="04a15-106">また、業務プロセス用プログラムで違いを検証する機会があるため、ギャップの可能性を識別またはギャップが存在しないことを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="04a15-106">You also have an opportunity to validate differences in the program for your business processes, so that you can identify potential gaps or confirm that no gaps exist.</span></span> <span data-ttu-id="04a15-107">アップグレード プロジェクトのこのステージでは、データとコードを環境内で使用することができません。</span><span class="sxs-lookup"><span data-stu-id="04a15-107">At this stage in your upgrade project, your data and code won’t be available in the environment.</span></span> <span data-ttu-id="04a15-108">したがって、すべてがビジネス プロセスに準拠していることを検証する能力は限られています。</span><span class="sxs-lookup"><span data-stu-id="04a15-108">Therefore, you will have limited ability to validate that everything conforms to your business process.</span></span> <span data-ttu-id="04a15-109">ただし、この手順はその認定作業での最初の手順です。</span><span class="sxs-lookup"><span data-stu-id="04a15-109">However, this step is the first step in that work stream.</span></span>

<span data-ttu-id="04a15-110">Finance and Operations のライセンスをまだ購入しておらず、無料トライアルを使用している場合は、[Microsoft Dynamics 365 for Finance and Operations を展開する](../deployment/deploy-demo-environment.md)の手順に従い、自分で持ち込む Microsoft Azure サブスクリプションにデモ環境を展開することができます。</span><span class="sxs-lookup"><span data-stu-id="04a15-110">If you haven’t yet purchased licenses for Finance and Operations, and you’re using a free trial, you can follow the steps in [Deploy a Microsoft Dynamics 365 for Finance and Operations demo environment](../deployment/deploy-demo-environment.md) to deploy a demo environment to a Microsoft Azure subscription that you bring yourself.</span></span>

<span data-ttu-id="04a15-111">Finance and Operations のライセンスを既に購入している場合、Microsoft Dynamics Lifecycle Services (LCS) で特殊なタイプのプロジェクト (実装プロジェクト) を構成するためのリンクを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="04a15-111">If you’ve already purchased licenses for Finance and Operations, you received a link to configure a special type of project in Microsoft Dynamics Lifecycle Services (LCS): an implementation project.</span></span> <span data-ttu-id="04a15-112">実装プロジェクトにより、開発者/テスト環境とサンドボックス環境を配置できます。</span><span class="sxs-lookup"><span data-stu-id="04a15-112">The implementation project will let you deploy a dev/test environment and a sandbox environment.</span></span> <span data-ttu-id="04a15-113">このタイプの環境の配置の詳細については、[サンドボックス環境でデータのアップグレード](upgrade-data-sandbox.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="04a15-113">For more information about this type of environment deployment, see [Data upgrade in a sandbox environment]](upgrade-data-sandbox.md).</span></span>
