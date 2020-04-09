---
title: 連結グループおよび追加の連結勘定の作成
description: この手順では、連結勘定グループの作成方法と、グループへの勘定の追加方法について説明します。
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup, MainAccountConsolidateAccount
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 826a65af563207fbfbc7391b176aa0e65b3363f9
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145242"
---
# <a name="create-consolidation-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="53a62-103">連結グループおよび追加の連結勘定の作成</span><span class="sxs-lookup"><span data-stu-id="53a62-103">Create consolidation groups and additional consolidation accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="53a62-104">この手順では、連結勘定グループの作成方法と、グループへの勘定の追加方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="53a62-104">This procedure shows how to create a consolidation account group and then add accounts to the group.</span></span> <span data-ttu-id="53a62-105">この手順では、デモ データ会社 USMF を使用します。</span><span class="sxs-lookup"><span data-stu-id="53a62-105">This procedure uses the demo data company USMF.</span></span>


## <a name="create-a-consolidation-account-group"></a><span data-ttu-id="53a62-106">連結勘定グループの作成</span><span class="sxs-lookup"><span data-stu-id="53a62-106">Create a consolidation account group</span></span>
1. <span data-ttu-id="53a62-107">[総勘定元帳] > [勘定科目表] > [勘定] > [連結勘定グループ] に移動します。</span><span class="sxs-lookup"><span data-stu-id="53a62-107">Go to General ledger > Chart of accounts > Accounts > Consolidation account groups.</span></span>
2. <span data-ttu-id="53a62-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53a62-108">Click New.</span></span>
3. <span data-ttu-id="53a62-109">[連結勘定グループ] フィールドに連結勘定グループ固有の ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="53a62-109">In the Consolidation account group field, enter a unique identifier for the consolidation account group.</span></span>
4. <span data-ttu-id="53a62-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="53a62-110">In the Name field, type a value.</span></span>

## <a name="add-accounts-to-consolidation-account-group"></a><span data-ttu-id="53a62-111">連結勘定グループに勘定を追加</span><span class="sxs-lookup"><span data-stu-id="53a62-111">Add accounts to consolidation account group</span></span>
1. <span data-ttu-id="53a62-112">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="53a62-112">Close the page.</span></span>
2. <span data-ttu-id="53a62-113">[総勘定元帳] > [勘定科目表] > [勘定] > [追加連結勘定] に移動します。</span><span class="sxs-lookup"><span data-stu-id="53a62-113">Go to General ledger > Chart of accounts > Accounts > Additional consolidation accounts.</span></span>
3. <span data-ttu-id="53a62-114">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53a62-114">Click New.</span></span>
4. <span data-ttu-id="53a62-115">[主勘定] フィールドで、ドロップダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="53a62-115">In the Main account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="53a62-116">一覧で、マップする主勘定をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53a62-116">In the list, click the main account that you want to map.</span></span>
6. <span data-ttu-id="53a62-117">[連結勘定グループ] フィールドで、ドロップダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="53a62-117">In the Consolidation account group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="53a62-118">一覧で、連結勘定グループをクリックします。</span><span class="sxs-lookup"><span data-stu-id="53a62-118">In the list, click the consolidation account group.</span></span>
8. <span data-ttu-id="53a62-119">[連結勘定] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="53a62-119">In the Consolidation account field, type a value.</span></span>
9. <span data-ttu-id="53a62-120">[連結勘定名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="53a62-120">In the Consolidation account name field, type a value.</span></span>

