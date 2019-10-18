---
title: グローバル アドレス帳のコンフィギュレーション
description: グローバル アドレス帳の既定値およびセキュリティ ポリシーを設定するには、この手順を使用します。
author: kfend
manager: AnnBe
ms.date: 07/23/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirParameters
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3994c7bb77e9821a880dc009681e113013129850
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189916"
---
# <a name="configure-the-global-address-book"></a><span data-ttu-id="a40d5-103">グローバル アドレス帳のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a40d5-103">Configure the global address book</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a40d5-104">グローバル アドレス帳の既定値およびセキュリティ ポリシーを設定するには、この手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="a40d5-104">Use this procedure to set the default values and security policies for the global address book.</span></span> 

<span data-ttu-id="a40d5-105">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="a40d5-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="a40d5-106">このタスクは、チームの計画およびコンフィギュレーションを対象としています。</span><span class="sxs-lookup"><span data-stu-id="a40d5-106">This task is intended for the Planning and configuration team.</span></span>

1. <span data-ttu-id="a40d5-107">ナビゲーション ウィンドウで、**モジュール > 組織管理 > グローバル アドレス帳 > グローバル アドレス帳パラメーター**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a40d5-107">In the Navigation pane, go to **Modules > Organization administration > Global address book > Global address book parameters**.</span></span>
2. <span data-ttu-id="a40d5-108">**名前の順序**フィールドで、名前の表示方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="a40d5-108">In the **Name sequence** field, select how names should be shown.</span></span>
3. <span data-ttu-id="a40d5-109">**ロールのない関係者の削除**で、ロールが割り当てられていない関係者を削除するかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="a40d5-109">In **Delete parties with no roles**, select whether to delete parties with that have not been assigned a role.</span></span>
4. <span data-ttu-id="a40d5-110">**重複チェックを使用**で、重複レコードをチェックするかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="a40d5-110">In **Use duplicate check**, select whether to check for duplicate records.</span></span>
5. <span data-ttu-id="a40d5-111">**アドレスに DUNS 番号を表示**で、アドレスに DUNS 番号を表示するかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="a40d5-111">In **Display DUNS number on addresses**, select whether to display the DUNS number on addresses.</span></span>
6. <span data-ttu-id="a40d5-112">**固有の DUNS 番号のチェック**で、固有の DUNS 番号をチェックするかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="a40d5-112">In **Check for unique DUNS number**, select whether to check for unique DUNS numbers.</span></span>
7. <span data-ttu-id="a40d5-113">**当事者**フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="a40d5-113">In the **Party** field, select an option.</span></span>
8. <span data-ttu-id="a40d5-114">**顧客**フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="a40d5-114">In the **Customer** field, select an option.</span></span>
9. <span data-ttu-id="a40d5-115">**仕入先**フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="a40d5-115">In the **Vendor** field, select an option.</span></span>
10. <span data-ttu-id="a40d5-116">**見込顧客**フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="a40d5-116">In the **Prospect** field, select an option.</span></span>
11. <span data-ttu-id="a40d5-117">**競合他社**フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="a40d5-117">In the **Competitor** field, select an option.</span></span>
12. <span data-ttu-id="a40d5-118">**プライベートな場所のセキュリティ** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a40d5-118">Click the **Private location security** tab.</span></span>
13. <span data-ttu-id="a40d5-119">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="a40d5-119">In the list, find and select the desired record.</span></span> <span data-ttu-id="a40d5-120">Shift キーを押して、**選択されたロール** ウィンドウに追加する複数のロールを選択し、次に矢印をクリックして選択したロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="a40d5-120">Press the Shift key to select multiple roles to add to the **Selected roles** pane and then click the arrow to add the selected roles.</span></span>  
14. <span data-ttu-id="a40d5-121">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a40d5-121">Click **Save**.</span></span>

