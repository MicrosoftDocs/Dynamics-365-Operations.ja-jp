---
title: 一括でユーザーをインポートする
description: システム管理者はこの手順を使用して、Azure Active Directory から多数のユーザーをインポートすることができます。
author: maertenm
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb2c316465f8c6964a562e92ce0a2233b37d38fe
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180901"
---
# <a name="import-users-in-bulk"></a><span data-ttu-id="ff879-103">ユーザーの一括インポート</span><span class="sxs-lookup"><span data-stu-id="ff879-103">Import users in bulk</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ff879-104">システム管理者はこの手順を使用して、Azure Active Directory から多数のユーザーをインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="ff879-104">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>


## <a name="run-as-a-batch-job"></a><span data-ttu-id="ff879-105">バッチ ジョブとして実行</span><span class="sxs-lookup"><span data-stu-id="ff879-105">Run as a batch job</span></span>
1. <span data-ttu-id="ff879-106">[システム管理] > [ユーザー] > [ユーザー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ff879-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="ff879-107">[バッチ インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ff879-107">Click Batch import.</span></span>
3. <span data-ttu-id="ff879-108">[バックグラウンドで実行] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="ff879-108">Expand the Run in the background section.</span></span>
4. <span data-ttu-id="ff879-109">[バッチ処理] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff879-109">Select Yes in the Batch processing field.</span></span>
5. <span data-ttu-id="ff879-110">[タスクの説明] フィールドでは、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ff879-110">In the Task description field, type a value.</span></span>
6. <span data-ttu-id="ff879-111">[バッチ グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="ff879-111">In the Batch group field, enter or select a value.</span></span>
    * <span data-ttu-id="ff879-112">これは、オプションのステップです。</span><span class="sxs-lookup"><span data-stu-id="ff879-112">This is an optional step.</span></span>  
7. <span data-ttu-id="ff879-113">[個人] フィールドでは、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff879-113">Select Yes in the Private field.</span></span>
    * <span data-ttu-id="ff879-114">これは、オプションのステップです。</span><span class="sxs-lookup"><span data-stu-id="ff879-114">This is an optional step.</span></span>  
8. <span data-ttu-id="ff879-115">[重要なジョブ] フィールドでは、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff879-115">Select Yes in the Critical Job field.</span></span>
    * <span data-ttu-id="ff879-116">これは、オプションのステップです。</span><span class="sxs-lookup"><span data-stu-id="ff879-116">This is an optional step.</span></span>  
9. <span data-ttu-id="ff879-117">[監視カテゴリ] フィールドでは、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ff879-117">In the Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="ff879-118">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ff879-118">Click OK.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="ff879-119">サンドボックス環境で実行</span><span class="sxs-lookup"><span data-stu-id="ff879-119">Run in a sandbox environment</span></span>
1. <span data-ttu-id="ff879-120">[バッチ インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ff879-120">Click Batch import.</span></span>
2. <span data-ttu-id="ff879-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ff879-121">Click OK.</span></span>

