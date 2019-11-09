---
title: 環境サービスの再開
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を通じて展開される環境で個々のサービスを再起動する方法について説明します。こ
author: kfend
manager: AnnBe
ms.date: 03/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2018-03-05
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: d59b4bd3f1b3289e10bf23a4733dd0ec212b39f6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183189"
---
# <a name="restart-environment-services"></a><span data-ttu-id="bafd1-103">環境サービスの再開</span><span class="sxs-lookup"><span data-stu-id="bafd1-103">Restart environment services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bafd1-104">Microsoft Dynamics Lifecycle Services (LCS) のサービスの再開機能を使用すると、Microsoft サブスクリプションで展開された階層 2、階層 3、階層 4、または階層 5 の標準承認テスト (サンドボックス) 環境に関連付けられた個々のサービスを再開することができます。</span><span class="sxs-lookup"><span data-stu-id="bafd1-104">You can use the Restart services functionality in Microsoft Dynamics Lifecycle Services (LCS) to restart individual services that are associated with a Tier 2, Tier 3, Tier 4, or Tier 5 standard acceptance test (sandbox) environment that is deployed in a Microsoft subscription.</span></span> <span data-ttu-id="bafd1-105">この機能を使用すると、次のサービスを再起動することができます。</span><span class="sxs-lookup"><span data-stu-id="bafd1-105">You can use this functionality to restart the following services:</span></span>

- <span data-ttu-id="bafd1-106">IIS</span><span class="sxs-lookup"><span data-stu-id="bafd1-106">IIS</span></span>
- <span data-ttu-id="bafd1-107">DIXF</span><span class="sxs-lookup"><span data-stu-id="bafd1-107">DIXF</span></span>
- <span data-ttu-id="bafd1-108">LCS 診断</span><span class="sxs-lookup"><span data-stu-id="bafd1-108">LCS Diagnostics</span></span>
- <span data-ttu-id="bafd1-109">バッチ</span><span class="sxs-lookup"><span data-stu-id="bafd1-109">Batch</span></span>
- <span data-ttu-id="bafd1-110">レポート サーバー</span><span class="sxs-lookup"><span data-stu-id="bafd1-110">Reporting Server</span></span>

<span data-ttu-id="bafd1-111">プロジェクト所有者、組織管理者、または環境マネージャーとして LCS プロジェクトに追加されたすべてのユーザーは、この機能を使用するアクセス許可を持っています。</span><span class="sxs-lookup"><span data-stu-id="bafd1-111">Any user who has been added as a project owner, organization admin, or environment manager in an LCS project has permissions to use this functionality.</span></span>

## <a name="restart-a-specific-service"></a><span data-ttu-id="bafd1-112">特定のサービスを再起動する</span><span class="sxs-lookup"><span data-stu-id="bafd1-112">Restart a specific service</span></span>

<span data-ttu-id="bafd1-113">展開された環境で特定のサービスを再起動するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="bafd1-113">To restart a specific service in a deployed environment, follow these steps.</span></span>

1. <span data-ttu-id="bafd1-114">LCS で、適切なプロジェクトを開き、サービスを再起動する環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="bafd1-114">In LCS, open the appropriate project, and select the environment to restart the service for.</span></span>
2. <span data-ttu-id="bafd1-115">**環境の詳細**ページで、**メンテナンス** &gt; **サービスのリセット**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bafd1-115">On the **Environment details** page, select **Maintain** &gt; **Restart services**.</span></span>
3. <span data-ttu-id="bafd1-116">**サービスを再起動します**ダイアログ ボックスで、再起動するサービスを選択してから **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bafd1-116">In the **Restart a service** dialog box, select the service to restart, and then select **OK**.</span></span>

    <span data-ttu-id="bafd1-117">**環境状態** 値は、サービスが再起動されると更新されます。</span><span class="sxs-lookup"><span data-stu-id="bafd1-117">The **Environment state** value is updated when the service is restarted.</span></span>

4. <span data-ttu-id="bafd1-118">更新された状態を表示するには、ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="bafd1-118">To view the updated status, refresh the page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bafd1-119">サービスの再起動には数秒しかかからないため、**環境の状態**の値はすでに**配置済み**にリセットされている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="bafd1-119">Because restart of a service might require only a few seconds, the **Environment state** value might already have been reset to **Deployed**.</span></span> <span data-ttu-id="bafd1-120">再起動が完了すると、エントリが **履歴** ページに追加されます。</span><span class="sxs-lookup"><span data-stu-id="bafd1-120">When the restart is completed, an entry is added to the **History** page.</span></span>
    
    
 ## <a name="stop-and-start-all-services"></a><span data-ttu-id="bafd1-121">すべてのサービスを再起動する</span><span class="sxs-lookup"><span data-stu-id="bafd1-121">Stop and start all services</span></span>
 
 <span data-ttu-id="bafd1-122">**すべて** のサービスを再起動するには、環境の詳細 ページにて **停止** メニュー オプションを実行した後で、 **開始** オプションを実行します。</span><span class="sxs-lookup"><span data-stu-id="bafd1-122">To stop and start **all** services, use the **Stop** menu option followed by the **Start** option on the environment details page.</span></span>
 
  > [!NOTE]
  > <span data-ttu-id="bafd1-123">この機能は Tier-2+ Sandbox においてのみ利用可能となっています。プロダクション環境でがご利用いただけません。</span><span class="sxs-lookup"><span data-stu-id="bafd1-123">This functionality is only available in Tier-2+ Sandbox environments and not in the production environment.</span></span>