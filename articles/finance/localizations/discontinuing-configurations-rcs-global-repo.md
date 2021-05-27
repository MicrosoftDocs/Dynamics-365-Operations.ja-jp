---
title: RCS グローバル リポジトリのコンフィギュレーションの中止
description: このトピックでは、RCS グローバル リポジトリのコンフィギュレーションを中止する方法について説明します。
author: JaneA07
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 2bd22e991de376cfd93f75158f1f29716d2559e1
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018736"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a><span data-ttu-id="c594c-103">RCS グローバル リポジトリのコンフィギュレーションの中止</span><span class="sxs-lookup"><span data-stu-id="c594c-103">Discontinue configurations in the RCS Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c594c-104">このトピックでは、RCS グローバル リポジトリのコンフィギュレーションを中止する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c594c-104">This topic describes how to discontinue configuration in the RCS Global repository.</span></span> <span data-ttu-id="c594c-105">以前は、不要になったコンフィギュレーションのみを削除できました。</span><span class="sxs-lookup"><span data-stu-id="c594c-105">Previously, it was possible only to delete configurations that were no longer required.</span></span> <span data-ttu-id="c594c-106">現在は、RCS グローバル リポジトリでリリースされたコンフィギュレーションを **中止** としてマークできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="c594c-106">However now you can mark a released configuration as **Discontinued** in the RCS Global repository.</span></span> <span data-ttu-id="c594c-107">この機能によって、次の操作も実行できます。</span><span class="sxs-lookup"><span data-stu-id="c594c-107">With this functionality, you can also do the following:</span></span> 
 
 - <span data-ttu-id="c594c-108">コンフィギュレーションの中止が予定されている場合は、事前に通知してください。</span><span class="sxs-lookup"><span data-stu-id="c594c-108">Provide up front notifications when a configuration is planned to be discontinued.</span></span>
 - <span data-ttu-id="c594c-109">代替コンフィギュレーションに適用される詳細を含めます。</span><span class="sxs-lookup"><span data-stu-id="c594c-109">Include applicable details about the replacement configuration.</span></span>
 - <span data-ttu-id="c594c-110">特定のコンフィギュレーションに **サポート終了日** を設定し、いつ中止されるかをユーザーに通知します。</span><span class="sxs-lookup"><span data-stu-id="c594c-110">Set a **Supported until** date for the specific configuration to inform the user when it will be discontinued.</span></span>

<span data-ttu-id="c594c-111">コンフィギュレーション バージョンを中止する場合は、次のオプション情報を指定できます。</span><span class="sxs-lookup"><span data-stu-id="c594c-111">When you discontinue a configuration version, you can specify the following optional information:</span></span>

  - <span data-ttu-id="c594c-112">**代替コンフィギュレーション**</span><span class="sxs-lookup"><span data-stu-id="c594c-112">**Replacement configuration**</span></span>
  - <span data-ttu-id="c594c-113">**代替コンフィギュレーション バージョン**</span><span class="sxs-lookup"><span data-stu-id="c594c-113">**Replacement configuration version**</span></span>
  - <span data-ttu-id="c594c-114">**自由書式の注記**: このフィールドを使用して、ドキュメントへのリンクや参照を提供します</span><span class="sxs-lookup"><span data-stu-id="c594c-114">**Free text note**: Use this field to provide documentation links or references</span></span>
  - <span data-ttu-id="c594c-115">**サポート終了日**: このフィールドは、現在の構成/バージョンのサポート終了日を示します。</span><span class="sxs-lookup"><span data-stu-id="c594c-115">**Supported until**: This field provides the proposed date up to which the current configuration/version will be supported.</span></span> <span data-ttu-id="c594c-116">この日付は手動で更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c594c-116">This date must be updated manually.</span></span>
  
<span data-ttu-id="c594c-117">コンフィギュレーションを中止するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c594c-117">To discontinue the configuration, complete the following steps.</span></span> 

1. <span data-ttu-id="c594c-118">**すべてのバージョン** を **はい** に設定して、1 回の操作で 1 つのバージョンを中止するか、同じ設定のすべてのバージョンを中止するかを選択します。</span><span class="sxs-lookup"><span data-stu-id="c594c-118">Select whether you want to discontinue a single version or all versions with the same settings in one operation by setting **All versions** to **Yes**.</span></span> 
2. <span data-ttu-id="c594c-119">**中止** パラメーターを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="c594c-119">Set the **Discontinue** parameter to **Yes**.</span></span>
3. <span data-ttu-id="c594c-120">**OK** を選択すると、コンフィギュレーションが中止されます。</span><span class="sxs-lookup"><span data-stu-id="c594c-120">Select **OK** to discontinue the configurations.</span></span> <span data-ttu-id="c594c-121">変更を保存すると、**中止日** フィールドが設定されます。</span><span class="sxs-lookup"><span data-stu-id="c594c-121">The **Discontinued date** field will be populated when you save the changes.</span></span>

![コンフィギュレーション中止の情報](media/Discontinue-details-2.png)
  
<span data-ttu-id="c594c-123">いつでもコンフィギュレーションを **共有** に戻したり、中止情報を調整することができます。</span><span class="sxs-lookup"><span data-stu-id="c594c-123">You can revert configuration back to **Shared** or adjust discontinuation information at any time.</span></span> <span data-ttu-id="c594c-124">コンフィギュレーションを共有する場合は、**サポート終了日** と、中止に関連するその他すべての情報を指定して、将来の中止計画を示します。</span><span class="sxs-lookup"><span data-stu-id="c594c-124">If you share a configuration, specify the **Supported until** date and all other information related to the discontinuation to indicate your plans for future discontinuation.</span></span>

<span data-ttu-id="c594c-125">計画された中止に関する情報を共有する場合は、実際にコンフィギュレーションを中止する前に、ユーザーは置換に関連するすべてのフィールドを事前に入力できますが、**中止** パラメーターは **いいえ** に設定したままにします。</span><span class="sxs-lookup"><span data-stu-id="c594c-125">If you want to share information about a planned discontinuation, prior to actually discontinuing the configuration, user is able to prefill all fields related to replacement but leave the **Discontinue** parameter set to **No**.</span></span>

> [!NOTE]
> <span data-ttu-id="c594c-126">中止はコンフィギュレーションの操作を制限しません。</span><span class="sxs-lookup"><span data-stu-id="c594c-126">Discontinuation doesn't limit operations with configurations.</span></span> <span data-ttu-id="c594c-127">コンフィギュレーションのインポート、実行、または派生を続行できます。これらのフィールドは情報提供のため使用されます。</span><span class="sxs-lookup"><span data-stu-id="c594c-127">You can continue to import, run, or derive the configurations, these fields are informational.</span></span>

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a><span data-ttu-id="c594c-128">Finance はバージョン 10.0.14 からこの情報表示をサポート</span><span class="sxs-lookup"><span data-stu-id="c594c-128">Finance supports displaying this information starting in version 10.0.14</span></span>

<span data-ttu-id="c594c-129">バージョン 10.0.14 以降、Dynamics 365 Finance は中止情報の表示をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="c594c-129">Starting in version 10.0.14, Dynamics 365 Finance supports displaying discontinuation information.</span></span> <span data-ttu-id="c594c-130">**グローバル リポジトリ** ページで、中止に関連する最新の情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="c594c-130">On the **Global repository** page, you can view up to date information related to discontinuation.</span></span> <span data-ttu-id="c594c-131">既定では、中止されたコンフィギュレーションは除外されます。</span><span class="sxs-lookup"><span data-stu-id="c594c-131">By default, configurations that are discontinued are filtered out.</span></span>
  
<span data-ttu-id="c594c-132">**インポートされたコンフィギュレーション** (ERSolutionTable) ページには、インポート時に既に中止されたコンフィギュレーションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c594c-132">The **Imported configurations** (ERSolutionTable) page, shows configurations that were already discontinued when there were imported.</span></span> <span data-ttu-id="c594c-133">インポート後に中止されたコンフィギュレーションの場合、**コンフィギュレーション更新のインポート** ジョブを実行することにより、中止情報を同期できます。</span><span class="sxs-lookup"><span data-stu-id="c594c-133">For those configurations that were discontinued after import, the discontinuation information can be synchronized by running the **Import configurations updates** job.</span></span>


