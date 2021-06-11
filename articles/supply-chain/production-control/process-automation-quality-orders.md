---
title: プロセス自動化フローを呼び出して品質指示を作成する
description: このトピックでは、Power Automate を使用して業務プロセスを自動化するためのリソースを品質指示の例を使用して示します。
author: cabeln
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f35adab3075ba810964a41899ba95ae40c115e83
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115198"
---
# <a name="invoke-process-automation-flows-to-create-quality-orders"></a><span data-ttu-id="0f5c7-103">プロセス自動化フローを呼び出して品質指示を作成する</span><span class="sxs-lookup"><span data-stu-id="0f5c7-103">Invoke process automation flows to create quality orders</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="0f5c7-104">組織では、標準的な業務プロセスを自動化し、より便利な対話機能をスタッフに提供し、さまざまなデータ信号やシステムを利用して業務プロセスを自動的に進めるという要求が高まっています。</span><span class="sxs-lookup"><span data-stu-id="0f5c7-104">Organizations have an increasing demand to automate standard business processes, provide more convenient interactions to the staff, and utilize various data signals and systems to drive business processes automatically.</span></span> <span data-ttu-id="0f5c7-105">ロボティック プロセス オートメーション (RPA) と Microsoft Power Automate により、企業はコードなしのエクスペリエンスを使用して反復プロセスを自動化できるため、効率と精度が向上します。</span><span class="sxs-lookup"><span data-stu-id="0f5c7-105">With robotic process automation (RPA) and Microsoft Power Automate, businesses can use a no-code experience to automate repetitive processes, thus gaining efficiency and accuracy.</span></span>

<span data-ttu-id="0f5c7-106">Supply Chain Management のダウンロード可能な自動化ソリューション テンプレートでは、Power Automate を使用して業務プロセスを自動化する方法を、品質指示を例として示しています。</span><span class="sxs-lookup"><span data-stu-id="0f5c7-106">The downloadable automation solution template for Supply Chain Management showcases how Power Automate can be used to automate business processes using quality orders as an example.</span></span>

<span data-ttu-id="0f5c7-107">自動化ソリューション テンプレートは [こちら](https://aka.ms/D365SCMQualityOrderRPASolution) からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="0f5c7-107">You can download the automation solution template [here](https://aka.ms/D365SCMQualityOrderRPASolution).</span></span>

<span data-ttu-id="0f5c7-108">このフィーチャーの概要とその機能については、次のビデオを参照してください: [RPAを使用した Dynamics 365 Supply Chain Management での品質指示の作成](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span><span class="sxs-lookup"><span data-stu-id="0f5c7-108">For an overview of this feature and its capabilities, see the following video: [Utilize RPA to create quality orders in Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span></span>

<span data-ttu-id="0f5c7-109">![RPA を使用した自動化オプション](media/rpa-automation-options.png "RPA を使用した自動化オプション")</span><span class="sxs-lookup"><span data-stu-id="0f5c7-109">![Automation options with RPA](media/rpa-automation-options.png "Automation options with RPA")</span></span>

<span data-ttu-id="0f5c7-110">Power Automate ソリューション テンプレートには、Supply Chain Management での品質指示の作成を自動化する、クラウド自動化フローとデスクトップ自動化フローが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0f5c7-110">The Power Automate solution template includes a cloud automation flow and a desktop automation flow that automate the creation of quality orders in Supply Chain Management.</span></span>

<span data-ttu-id="0f5c7-111">自動化は、ユーザー入力やマシン信号 (モノのインターネット (IoT) を含む) など、多くのイベントや信号に応じて開始できます。</span><span class="sxs-lookup"><span data-stu-id="0f5c7-111">The automation can be started in response to many events and signals, including user input or machine signals (including the Internet of Things (IoT)).</span></span> <span data-ttu-id="0f5c7-112">ソリューション テンプレートには *Q-Order* Power Application の例が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0f5c7-112">The *Q-Order* Power Application example is included in the solution template.</span></span> <span data-ttu-id="0f5c7-113">ユーザーは、品目の QR コードをスキャンしたり、数量を入力したり、カメラを使用して画像を添付したりできます。</span><span class="sxs-lookup"><span data-stu-id="0f5c7-113">It allows the user to scan an item QR code, enter quantity, and attach pictures using a camera.</span></span>

<span data-ttu-id="0f5c7-114">ソリューション パラメータは、生産施設の特定のユース ケースに対して自動化を構成するために含まれています。</span><span class="sxs-lookup"><span data-stu-id="0f5c7-114">Solution parameters are included to configure the automation for a specific use case in a production facility.</span></span>

<span data-ttu-id="0f5c7-115">![品質指示の作成](media/rpa-create-quality-roder.png "品質指示の作成")</span><span class="sxs-lookup"><span data-stu-id="0f5c7-115">![Create quality order](media/rpa-create-quality-roder.png "Create quality order")</span></span>

<span data-ttu-id="0f5c7-116">サンプル ソリューションをダウンロード、インストール、および使用して品質指示の作成を自動化する方法に関する完全なステップ バイ ステップ ガイドについては、[Power Automate Desktop を使用したロボティック プロセス オートメーションによる Dynamics 365 Supply Chain Management での品質指示作成の自動化](/power-automate/desktop-flows/dynamics365-scm-rpa) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f5c7-116">For a complete step-by-step guide about how to download, install, and use the sample solution for automating quality order creation, see [Automate quality order creation on Dynamics 365 Supply Chain Management with Robotic Process Automation using Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).</span></span>

