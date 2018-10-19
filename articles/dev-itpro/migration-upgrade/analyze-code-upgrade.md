---
title: "AX 2012 からのアップグレード - コードのアップグレード サービスを使用した工数見積"
description: "このトピックでは、LCS のコード アップグレード サービスを使用して、Microsoft Dynamics AX 2012 から Dynamics 365 for Finance and Operations にアップグレードするために必要な作業と労力を見積もる方法を説明します。"
author: tariqbell
manager: AnnBe
ms.date: 01/31/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 106163
ms.assetid: 
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-05-31
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: d22fe0c9a38026350c839d1d7d35835bfc77d995
ms.openlocfilehash: 4d944c26e13f3307fa79b73922e702d3d787a594
ms.contentlocale: ja-jp
ms.lasthandoff: 09/17/2018

---

# <a name="upgrade-from-ax-2012---estimate-effort-by-using-the-code-upgrade-service"></a><span data-ttu-id="96cf1-103">AX 2012 からのアップグレード - コードのアップグレード サービスを使用した工数見積</span><span class="sxs-lookup"><span data-stu-id="96cf1-103">Upgrade from AX 2012 - Estimate effort by using the Code upgrade service</span></span>

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

<span data-ttu-id="96cf1-104">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して、Microsoft Dynamics AX 2012 から Microsoft Dynamics 365 for Finance and Operations にアップグレードするために必要な作業と労力を見積もる方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="96cf1-104">This topic explains how to use the Code upgrade service in Microsoft Dynamics Lifecycle Services (LCS) to help estimate the tasks and effort that are required in order to upgrade a code base from Microsoft Dynamics AX 2012 to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="96cf1-105">コード アップグレード サービスは、AX 2012 モデル ストアのエクスポートを Finance and Operations の適切な形式に変換します。</span><span class="sxs-lookup"><span data-stu-id="96cf1-105">The Code upgrade service converts an export of your AX 2012 model store to the correct format for Finance and Operations.</span></span> <span data-ttu-id="96cf1-106">ただし、サービスが識別してもまだ独自で解決できない問題を開発者が解決するまで、コードの新しいバージョンは完全に機能しません。</span><span class="sxs-lookup"><span data-stu-id="96cf1-106">However, the new version of your code won’t be fully functional until a developer resolves any issues that the service identifies but can’t resolve itself.</span></span>

<span data-ttu-id="96cf1-107">コード アップグレード サービスは、これらのアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="96cf1-107">The Code upgrade service performs these actions:</span></span>

- <span data-ttu-id="96cf1-108">いくつかのタイプの競合問題を直接解決します。</span><span class="sxs-lookup"><span data-stu-id="96cf1-108">Directly resolve some types of conflict issues.</span></span>
- <span data-ttu-id="96cf1-109">その他の問題については、Microsoft Azure DevOps タスクにログ記録します。</span><span class="sxs-lookup"><span data-stu-id="96cf1-109">For other issues, log Microsoft Azure DevOps tasks.</span></span>
- <span data-ttu-id="96cf1-110">Finance and Operations の形式でコードのバージョンを作成し、Azure DevOps プロジェクトの新しい分岐で新しいバージョンを確認します。</span><span class="sxs-lookup"><span data-stu-id="96cf1-110">Create a version of your code in the Finance and Operations format, and check the new version into a new branch of your Azure DevOps project.</span></span>

<span data-ttu-id="96cf1-111">分析フェーズでは、レポートを使用してコード変換アクティビティを完了するために必要な作業量を見積もります。</span><span class="sxs-lookup"><span data-stu-id="96cf1-111">In the Analyze phase, we use the report to help estimate the effort that is required in order to complete code conversion activities.</span></span>

<span data-ttu-id="96cf1-112">次の図は、コードのアップグレード サービスを構成するプロセスの概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="96cf1-112">The following illustration shows an overview of the process for configuring the Code upgrade service.</span></span>

![コード アップグレード サービスのコンフィギュレーション プロセス](media/codeUpgradeConfigurationProcess.png)

<span data-ttu-id="96cf1-114">コード アップグレード サービスをコンフィギュレーションする方法については、「[Lifecycle Services でコード アップグレード サービスをコンフィギュレーションする](../lifecycle-services/configure-execute-code-upgrade.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96cf1-114">For information about how to configure the Code upgrade service, see [Configure the code upgrade service in Lifecycle Services](../lifecycle-services/configure-execute-code-upgrade.md).</span></span>

<span data-ttu-id="96cf1-115">コード アップグレード サービスの出力は、Finance and Operations 開発者が消費するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="96cf1-115">The output of the Code upgrade service is designed to be consumed by a Finance and Operations developer.</span></span> <span data-ttu-id="96cf1-116">この出力は、開発者がコードのアップグレード タスクを完了するために必要な工数を見積もるのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="96cf1-116">This output will help the developer estimate the effort that is required in order to complete the code upgrade tasks.</span></span> <span data-ttu-id="96cf1-117">見積もりを作成するには、サービスが Azure DevOps で生成するタスクと、サービスが生成する新しいバージョンのコードを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="96cf1-117">To form an estimate, the developer must review the tasks that the service generates in Azure DevOps and the new version of the code that the service generates.</span></span>

