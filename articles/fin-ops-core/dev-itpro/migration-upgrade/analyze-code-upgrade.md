---
title: AX 2012 からのアップグレード - コードのアップグレード サービスを使用した工数見積
description: このトピックでは、LCS のコード アップグレード サービスを使用して、Microsoft Dynamics AX 2012 から Finance and Operations にコード ベースをアップグレードするために必要な作業と労力を見積もる方法を説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 01/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 106163
ms.assetid: ''
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2017-05-31
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 32eb1932cd320beaea72f24adc41e4175262a53e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683482"
---
# <a name="upgrade-from-ax-2012---estimate-effort-by-using-the-code-upgrade-service"></a><span data-ttu-id="368c3-103">AX 2012 からのアップグレード - コードのアップグレード サービスを使用した工数見積</span><span class="sxs-lookup"><span data-stu-id="368c3-103">Upgrade from AX 2012 - Estimate effort by using the Code upgrade service</span></span>

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

<span data-ttu-id="368c3-104">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) のコード アップグレード サービスを使用して、Microsoft Dynamics AX 2012 から Finance and Operations にコード ベースをアップグレードするために必要な作業と労力を見積もる方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="368c3-104">This topic explains how to use the Code upgrade service in Microsoft Dynamics Lifecycle Services (LCS) to help estimate the tasks and effort that are required in order to upgrade a code base from Microsoft Dynamics AX 2012 Finance and Operations.</span></span>

<span data-ttu-id="368c3-105">コード アップグレード サービスは、AX 2012 モデル ストアのエクスポートを適切な形式に変換します。</span><span class="sxs-lookup"><span data-stu-id="368c3-105">The Code upgrade service converts an export of your AX 2012 model store to the correct format.</span></span> <span data-ttu-id="368c3-106">ただし、サービスが識別してもまだ独自で解決できない問題を開発者が解決するまで、コードの新しいバージョンは完全に機能しません。</span><span class="sxs-lookup"><span data-stu-id="368c3-106">However, the new version of your code won’t be fully functional until a developer resolves any issues that the service identifies but can’t resolve itself.</span></span>

<span data-ttu-id="368c3-107">コード アップグレード サービスは、これらのアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="368c3-107">The Code upgrade service performs these actions:</span></span>

- <span data-ttu-id="368c3-108">いくつかのタイプの競合問題を直接解決します。</span><span class="sxs-lookup"><span data-stu-id="368c3-108">Directly resolve some types of conflict issues.</span></span>
- <span data-ttu-id="368c3-109">その他の問題については、Microsoft Azure DevOps タスクにログ記録します。</span><span class="sxs-lookup"><span data-stu-id="368c3-109">For other issues, log Microsoft Azure DevOps tasks.</span></span>
- <span data-ttu-id="368c3-110">適切な形式でコード バージョンを作成し、Azure DevOps プロジェクトの新しい分岐への新しいバージョンを確認します。</span><span class="sxs-lookup"><span data-stu-id="368c3-110">Create a version of your code in the correct format, and check the new version into a new branch of your Azure DevOps project.</span></span>

<span data-ttu-id="368c3-111">分析フェーズでは、レポートを使用してコード変換アクティビティを完了するために必要な作業量を見積もります。</span><span class="sxs-lookup"><span data-stu-id="368c3-111">In the Analyze phase, we use the report to help estimate the effort that is required in order to complete code conversion activities.</span></span>

<span data-ttu-id="368c3-112">次の図は、コードのアップグレード サービスを構成するプロセスの概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="368c3-112">The following illustration shows an overview of the process for configuring the Code upgrade service.</span></span>

![コード アップグレード サービスのコンフィギュレーション プロセス](media/codeUpgradeConfigurationProcess.png)

<span data-ttu-id="368c3-114">コード アップグレード サービスを構成する方法については、 [Lifecycle Services (LCS) で、コード アップグレード サービスを構成する](../lifecycle-services/configure-execute-code-upgrade.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="368c3-114">For information about how to configure the Code upgrade service, see [Configure the code upgrade service in Lifecycle Services (LCS)](../lifecycle-services/configure-execute-code-upgrade.md).</span></span>

<span data-ttu-id="368c3-115">コード アップグレード サービスの出力は、開発者が使用するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="368c3-115">The output of the Code upgrade service is designed to be consumed by a developer.</span></span> <span data-ttu-id="368c3-116">この出力は、開発者がコードのアップグレード タスクを完了するために必要な工数を見積もるのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="368c3-116">This output will help the developer estimate the effort that is required in order to complete the code upgrade tasks.</span></span> <span data-ttu-id="368c3-117">見積もりを作成するには、サービスが Azure DevOps で生成するタスクと、サービスが生成する新しいバージョンのコードを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="368c3-117">To form an estimate, the developer must review the tasks that the service generates in Azure DevOps and the new version of the code that the service generates.</span></span>
