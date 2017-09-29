--- 
title: "主勘定カテゴリの設定"
description: "主勘定カテゴリは、財務報告と Power BI の既定のレポートに使用されます。"
author: aprilolson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 94e17d7cbcc8f826e806a8d4bc026a9d7844e910
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="4ec0e-103">主勘定カテゴリの設定</span><span class="sxs-lookup"><span data-stu-id="4ec0e-103">Set up main account categories</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4ec0e-104">主勘定カテゴリは、財務報告と Power BI の既定のレポートに使用されます。</span><span class="sxs-lookup"><span data-stu-id="4ec0e-104">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="4ec0e-105">既定で作成される主勘定カテゴリの名前は変更できますが、削除はできません。</span><span class="sxs-lookup"><span data-stu-id="4ec0e-105">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="4ec0e-106">追加の勘定カテゴリを作成しレポートおよび分析に使用できます。</span><span class="sxs-lookup"><span data-stu-id="4ec0e-106">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="4ec0e-107">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec0e-107">This task uses the USMF demo company.</span></span>


## <a name="create-a-main-account-category"></a><span data-ttu-id="4ec0e-108">主勘定カテゴリの作成</span><span class="sxs-lookup"><span data-stu-id="4ec0e-108">Create a main account category</span></span>
1. <span data-ttu-id="4ec0e-109">[総勘定元帳] > [勘定科目表] > [勘定] > [主勘定カテゴリ] に移動します。</span><span class="sxs-lookup"><span data-stu-id="4ec0e-109">Go to General ledger > Chart of accounts > Accounts > Main account categories.</span></span>
2. <span data-ttu-id="4ec0e-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ec0e-110">Click New.</span></span>
3. <span data-ttu-id="4ec0e-111">[主勘定カテゴリ] フィールドに一意の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="4ec0e-111">In the Main account category field, enter a unique name.</span></span>
4. <span data-ttu-id="4ec0e-112">[説明] フィールドに主勘定カテゴリの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="4ec0e-112">In the Description field, enter a description for the main account category.</span></span>
5. <span data-ttu-id="4ec0e-113">[主勘定タイプ] フィールドで、カテゴリにリンクされる主勘定タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="4ec0e-113">In the Main account type field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="4ec0e-114">主勘定の勘定カテゴリへのリンク</span><span class="sxs-lookup"><span data-stu-id="4ec0e-114">Link main accounts to account category</span></span>
1. <span data-ttu-id="4ec0e-115">[主勘定をリンク] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ec0e-115">Click Link main accounts.</span></span>
2. <span data-ttu-id="4ec0e-116">一覧で、主勘定カテゴリに割り当てる主勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="4ec0e-116">In the list, select the main accounts to assign to the main account category.</span></span>
    * <span data-ttu-id="4ec0e-117">主勘定を主勘定カテゴリに割り当てると、そのカテゴリが財務報告と分析に使用された際に勘定の残高を集計します。</span><span class="sxs-lookup"><span data-stu-id="4ec0e-117">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="4ec0e-118">[リンク済] オプションを選択またはクリアして主勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="4ec0e-118">Select or clear the Linked option to choose the main accounts.</span></span>
4. <span data-ttu-id="4ec0e-119">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ec0e-119">Click OK.</span></span>
5. <span data-ttu-id="4ec0e-120">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ec0e-120">Click Yes.</span></span>


