---
title: 連結グループおよび追加の連結勘定の作成
description: この手順では、連結勘定グループの作成方法と、グループへの勘定の追加方法について説明します。
author: aprilolson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup, MainAccountConsolidateAccount
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6c60b09fd0481c84a9c3a3eb35b66264d92d00eb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832781"
---
# <a name="create-consolidation-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="bde44-103">連結グループおよび追加の連結勘定の作成</span><span class="sxs-lookup"><span data-stu-id="bde44-103">Create consolidation groups and additional consolidation accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bde44-104">この手順では、連結勘定グループの作成方法と、グループへの勘定の追加方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="bde44-104">This procedure shows how to create a consolidation account group and then add accounts to the group.</span></span> <span data-ttu-id="bde44-105">この手順では、デモ データ会社 USMF を使用します。</span><span class="sxs-lookup"><span data-stu-id="bde44-105">This procedure uses the demo data company USMF.</span></span>


## <a name="create-a-consolidation-account-group"></a><span data-ttu-id="bde44-106">連結勘定グループの作成</span><span class="sxs-lookup"><span data-stu-id="bde44-106">Create a consolidation account group</span></span>
1. <span data-ttu-id="bde44-107">[総勘定元帳] > [勘定科目表] > [勘定] > [連結勘定グループ] に移動します。</span><span class="sxs-lookup"><span data-stu-id="bde44-107">Go to General ledger > Chart of accounts > Accounts > Consolidation account groups.</span></span>
2. <span data-ttu-id="bde44-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bde44-108">Click New.</span></span>
3. <span data-ttu-id="bde44-109">[連結勘定グループ] フィールドに連結勘定グループ固有の ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="bde44-109">In the Consolidation account group field, enter a unique identifier for the consolidation account group.</span></span>
4. <span data-ttu-id="bde44-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bde44-110">In the Name field, type a value.</span></span>

## <a name="add-accounts-to-consolidation-account-group"></a><span data-ttu-id="bde44-111">連結勘定グループに勘定を追加</span><span class="sxs-lookup"><span data-stu-id="bde44-111">Add accounts to consolidation account group</span></span>
1. <span data-ttu-id="bde44-112">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="bde44-112">Close the page.</span></span>
2. <span data-ttu-id="bde44-113">[総勘定元帳] > [勘定科目表] > [勘定] > [追加連結勘定] に移動します。</span><span class="sxs-lookup"><span data-stu-id="bde44-113">Go to General ledger > Chart of accounts > Accounts > Additional consolidation accounts.</span></span>
3. <span data-ttu-id="bde44-114">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bde44-114">Click New.</span></span>
4. <span data-ttu-id="bde44-115">[主勘定] フィールドで、ドロップダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="bde44-115">In the Main account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="bde44-116">一覧で、マップする主勘定をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bde44-116">In the list, click the main account that you want to map.</span></span>
6. <span data-ttu-id="bde44-117">[連結勘定グループ] フィールドで、ドロップダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="bde44-117">In the Consolidation account group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="bde44-118">一覧で、連結勘定グループをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bde44-118">In the list, click the consolidation account group.</span></span>
8. <span data-ttu-id="bde44-119">[連結勘定] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bde44-119">In the Consolidation account field, type a value.</span></span>
9. <span data-ttu-id="bde44-120">[連結勘定名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bde44-120">In the Consolidation account name field, type a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]