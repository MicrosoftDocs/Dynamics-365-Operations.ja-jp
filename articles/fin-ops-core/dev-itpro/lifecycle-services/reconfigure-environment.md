---
title: 新しいプラットフォームまたはトポロジを使用するために環境を再構成
description: このトピックでは、新しいプラットフォームまたはトポロジを使用して環境を再構成する方法と、既存の環境の構成を更新する方法について説明します。
author: sarvanisathish
manager: AnnBe
ms.date: 12/05/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 60373
ms.assetid: ''
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2017-12-05
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 5f6b153aeae945a1e2cb0e87d18f440a159ccf11
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183191"
---
# <a name="reconfigure-environments-to-take-a-new-platform-or-topology"></a><span data-ttu-id="a9e77-103">新しいプラットフォームまたはトポロジを使用するために環境を再構成</span><span class="sxs-lookup"><span data-stu-id="a9e77-103">Reconfigure environments to take a new platform or topology</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9e77-104">このトピックでは、新しいプラットフォームまたはトポロジを使用して環境を再構成する方法と、既存の環境の構成を更新する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a9e77-104">This topic provides information about how to reconfigure your environment with a new platform or topology and how to update the configuration of your existing environment.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="a9e77-105">前提条件</span><span class="sxs-lookup"><span data-stu-id="a9e77-105">Prerequisites</span></span>
<span data-ttu-id="a9e77-106">このトピックの手順を実行する前に、ローカル エージェントを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9e77-106">Before you complete the steps in this topic, you must update your local agent.</span></span> <span data-ttu-id="a9e77-107">詳細については、トピックの、「[ローカル エージェントの更新](update-local-agent.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9e77-107">For more information, see the topic, [Update the local agent](update-local-agent.md).</span></span> <span data-ttu-id="a9e77-108">このトピックにある手順は、バージョン 1.1.0 以上のローカル エージェントでのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="a9e77-108">The procedure in this topic will only work with local agents that are on or above version 1.1.0.</span></span> 

## <a name="reconfigure-your-environment"></a><span data-ttu-id="a9e77-109">環境の再構成</span><span class="sxs-lookup"><span data-stu-id="a9e77-109">Reconfigure your environment</span></span>

1. <span data-ttu-id="a9e77-110">Lifecycle Services (LCS) で、オンプレミスのプロジェクトに移動し、**環境**ブレードを開きます。</span><span class="sxs-lookup"><span data-stu-id="a9e77-110">In Lifecycle Services (LCS), navigate to your on-premises project and open the **Environments** blade.</span></span> 

2. <span data-ttu-id="a9e77-111">新しい配置を再設定するかどうかに基づいて、次のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="a9e77-111">Do one of the following based on whether you are going to reconfigure or take a new deployment.</span></span>

- <span data-ttu-id="a9e77-112">環境を再構成する場合は、**再構成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9e77-112">If you need to reconfigure your environment, click **Reconfigure**.</span></span>
- <span data-ttu-id="a9e77-113">新しい展開またはトポロジーを使用する必要がある場合は、使用しているプラットフォーム用の新しいトポロジーを選択し、環境名を入力します。</span><span class="sxs-lookup"><span data-stu-id="a9e77-113">If you need to take a new deployment or topology, select the new topology for your platform and enter the environment name.</span></span> <span data-ttu-id="a9e77-114">同じ名前を使用したり、新しい名前を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="a9e77-114">You can use the same name or enter a new one.</span></span> 
  
3. <span data-ttu-id="a9e77-115">**詳細設定**をクリックし、コンフィギュレーションを更新します。</span><span class="sxs-lookup"><span data-stu-id="a9e77-115">Click **Advanced Settings** to update your configuration.</span></span> <span data-ttu-id="a9e77-116">以前の展開の設定が保存されます。</span><span class="sxs-lookup"><span data-stu-id="a9e77-116">The configuration from your previous deployment will be saved.</span></span> 
