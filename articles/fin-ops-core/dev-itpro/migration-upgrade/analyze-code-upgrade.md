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
ms.openlocfilehash: 0a6edd4eb4b88f5d0edcdbfe2c32744bb5c9f482
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191891"
---
# <a name="upgrade-from-ax-2012---estimate-effort-by-using-the-code-upgrade-service"></a><span data-ttu-id="c6aba-103">AX 2012 からのアップグレード - コードのアップグレード サービスを使用した工数見積</span><span class="sxs-lookup"><span data-stu-id="c6aba-103">Upgrade from AX 2012 - Estimate effort by using the Code upgrade service</span></span>

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

<span data-ttu-id="c6aba-104">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) のコード アップグレード サービスを使用して、Microsoft Dynamics AX 2012 から Finance and Operations にコード基準をアップグレードするために必要なタスクと工数を見積もる方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="c6aba-104">This topic explains how to use the Code upgrade service in Microsoft Dynamics Lifecycle Services (LCS) to help estimate the tasks and effort that are required in order to upgrade a code base from Microsoft Dynamics AX 2012 Finance and Operations.</span></span>

<span data-ttu-id="c6aba-105">コード アップグレード サービスは、AX 2012 モデル ストアのエクスポートを適切な形式に変換します。</span><span class="sxs-lookup"><span data-stu-id="c6aba-105">The Code upgrade service converts an export of your AX 2012 model store to the correct format.</span></span> <span data-ttu-id="c6aba-106">ただし、サービスが識別してもまだ独自で解決できない問題を開発者が解決するまで、コードの新しいバージョンは完全に機能しません。</span><span class="sxs-lookup"><span data-stu-id="c6aba-106">However, the new version of your code won’t be fully functional until a developer resolves any issues that the service identifies but can’t resolve itself.</span></span>

<span data-ttu-id="c6aba-107">コード アップグレード サービスは、これらのアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="c6aba-107">The Code upgrade service performs these actions:</span></span>

- <span data-ttu-id="c6aba-108">いくつかのタイプの競合問題を直接解決します。</span><span class="sxs-lookup"><span data-stu-id="c6aba-108">Directly resolve some types of conflict issues.</span></span>
- <span data-ttu-id="c6aba-109">その他の問題については、Microsoft Azure DevOps タスクにログ記録します。</span><span class="sxs-lookup"><span data-stu-id="c6aba-109">For other issues, log Microsoft Azure DevOps tasks.</span></span>
- <span data-ttu-id="c6aba-110">適切な形式でコード バージョンを作成し、Azure DevOps プロジェクトの新しい分岐への新しいバージョンを確認します。</span><span class="sxs-lookup"><span data-stu-id="c6aba-110">Create a version of your code in the correct format, and check the new version into a new branch of your Azure DevOps project.</span></span>

<span data-ttu-id="c6aba-111">分析フェーズでは、レポートを使用してコード変換アクティビティを完了するために必要な作業量を見積もります。</span><span class="sxs-lookup"><span data-stu-id="c6aba-111">In the Analyze phase, we use the report to help estimate the effort that is required in order to complete code conversion activities.</span></span>

<span data-ttu-id="c6aba-112">次の図は、コードのアップグレード サービスを構成するプロセスの概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="c6aba-112">The following illustration shows an overview of the process for configuring the Code upgrade service.</span></span>

![コード アップグレード サービスのコンフィギュレーション プロセス](media/codeUpgradeConfigurationProcess.png)

<span data-ttu-id="c6aba-114">コード アップグレード サービスをコンフィギュレーションする方法については、「[Lifecycle Services でコード アップグレード サービスをコンフィギュレーションする](../lifecycle-services/configure-execute-code-upgrade.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c6aba-114">For information about how to configure the Code upgrade service, see [Configure the code upgrade service in Lifecycle Services](../lifecycle-services/configure-execute-code-upgrade.md).</span></span>

<span data-ttu-id="c6aba-115">コード アップグレード サービスの出力は、開発者が使用するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="c6aba-115">The output of the Code upgrade service is designed to be consumed by a developer.</span></span> <span data-ttu-id="c6aba-116">この出力は、開発者がコードのアップグレード タスクを完了するために必要な工数を見積もるのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c6aba-116">This output will help the developer estimate the effort that is required in order to complete the code upgrade tasks.</span></span> <span data-ttu-id="c6aba-117">見積もりを作成するには、サービスが Azure DevOps で生成するタスクと、サービスが生成する新しいバージョンのコードを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6aba-117">To form an estimate, the developer must review the tasks that the service generates in Azure DevOps and the new version of the code that the service generates.</span></span>