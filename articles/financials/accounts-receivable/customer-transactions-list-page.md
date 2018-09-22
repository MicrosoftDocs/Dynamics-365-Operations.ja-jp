---
title: "顧客トランザクション リスト ページ"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations の顧客トランザクション リスト ページについての情報を提供します。"
author: mikefalkner
manager: aolson
ms.date: 08/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e828cb292ad48bb4690117b41589b25edcdf28bc
ms.contentlocale: ja-jp
ms.lasthandoff: 08/31/2018

---

# <a name="customer-transaction-list-page"></a><span data-ttu-id="1c269-103">顧客トランザクション リスト ページ</span><span class="sxs-lookup"><span data-stu-id="1c269-103">Customer transaction list page</span></span>

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a><span data-ttu-id="1c269-104">決済を表示する</span><span class="sxs-lookup"><span data-stu-id="1c269-104">View settlements</span></span>

<span data-ttu-id="1c269-105">アクション ウィンドウの**決済の表示**タブは、決済履歴にすばやくアクセスしたり、決済トランザクション全体についての詳細を説明したりします。</span><span class="sxs-lookup"><span data-stu-id="1c269-105">The **View settlements** tab on the action pane provides quick access to settlement history and more information about the whole settlement transaction.</span></span> <span data-ttu-id="1c269-106">同じ決済に含まれていたり、または同じ支払仕訳帳で作成された支払である場合、選択したトランザクションに関連する追加トランザクションを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="1c269-106">You can also show additional transactions that are related to the selected transaction, either because they were part of the same settlement or because they are payments that were created in the same payment journal.</span></span>

1. <span data-ttu-id="1c269-107">**売掛金勘定 \> 顧客**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1c269-107">Select **Accounts receivable \> Customers**.</span></span>
2. <span data-ttu-id="1c269-108">トランザクションを持つ顧客を選択してから、**顧客\>トランザクション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1c269-108">Select a customer that has transactions, and then select **Customer \> Transactions**.</span></span>
3. <span data-ttu-id="1c269-109">トランザクションを選択して、調査します。</span><span class="sxs-lookup"><span data-stu-id="1c269-109">Select a transaction to research.</span></span>
4. <span data-ttu-id="1c269-110">アクション ウィンドウの**決済の表示**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="1c269-110">Select the **View settlements** tab on the action pane.</span></span>

    <span data-ttu-id="1c269-111">**決済の表示**ダイアログ ボックスは、選択したトランザクションとそれに対して決済されたすべてのドキュメントを表示します。</span><span class="sxs-lookup"><span data-stu-id="1c269-111">The **View settlements** dialog box shows the selected transaction and all documents that have been settled against it.</span></span> <span data-ttu-id="1c269-112">このダイアログ ボックスは、決済履歴の表示と似ていますが、関連するすべてのドキュメントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1c269-112">This dialog box resembles the settlement history view, but it includes all related documents.</span></span> 

5. <span data-ttu-id="1c269-113">このダイアログ ボックスでは、さまざまなタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="1c269-113">You can perform various tasks from this dialog box.</span></span> <span data-ttu-id="1c269-114">次の 1 つまたは複数の伝票を選択してから、次のいずれかのメニューを選択します。</span><span class="sxs-lookup"><span data-stu-id="1c269-114">Select one or more vouchers, and then select one of the following menus:</span></span>

   - <span data-ttu-id="1c269-115">**勘定の表示** – 選択した伝票に関連するすべての伝票を表示します。</span><span class="sxs-lookup"><span data-stu-id="1c269-115">**View accounting** – All vouchers that are related to the selected documents appear.</span></span> <span data-ttu-id="1c269-116">**閉じる**を選択して、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1c269-116">Select **Close** to close the dialog box.</span></span>
   - <span data-ttu-id="1c269-117">**エクスポート**: 選択した伝票を Microsoft Excel にエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="1c269-117">**Export** – Export the selected vouchers to Microsoft Excel.</span></span>
   - <span data-ttu-id="1c269-118">**関連する支払の表示** – 選択したドキュメントに関連する支払仕訳帳で作成されたすべての支払仕訳帳トランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1c269-118">**View related payments** – All the payment journal transactions that were created in the payment journal that is related to the selected document appear.</span></span> <span data-ttu-id="1c269-119">さらに、これらの支払に関連するすべての決済が表示されます。</span><span class="sxs-lookup"><span data-stu-id="1c269-119">In addition, all the settlements that are related to those payments appear.</span></span> <span data-ttu-id="1c269-120">このメニューのラベルも**決済の表示**に変更します。</span><span class="sxs-lookup"><span data-stu-id="1c269-120">The label of this menu also changes to **View settlements**.</span></span> <span data-ttu-id="1c269-121">**決済の表示**を選択して、**決済の表示**ダイアログ ボックスを最初に開いたときに表示されるトランザクションのみを表示します。</span><span class="sxs-lookup"><span data-stu-id="1c269-121">Select **View settlements** to show only the transactions that were shown when you first opened the  **View settlements** dialog box.</span></span>
    - <span data-ttu-id="1c269-122">**トランザクションの決済** – 選択した元のドキュメントが完全に決済されなかった場合、このメニューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1c269-122">**Settle transactions** – This menu appears if the original document that was selected wasn't fully settled.</span></span> <span data-ttu-id="1c269-123">それを選択すると、**トランザクションの決済**ダイアログ ボックスが表示され、決済するトランザクションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="1c269-123">When you select it, the **Settle transactions** dialog box appears, where you can select transactions for settlement.</span></span>
    - <span data-ttu-id="1c269-124">**決済を元に戻す** – 選択した元のドキュメントが完全に決済された場合、このメニューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1c269-124">**Undo settlements** – This menu appears if the original document that was selected was fully settled.</span></span> <span data-ttu-id="1c269-125">それを選択すると、**決済を元に戻す**ダイアログ ボックスが表示され、そのドキュメントで実行された決済を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="1c269-125">When you select it, the **Undo settlements** dialog box appears, where you can undo the settlements that were done for that document.</span></span>
    

