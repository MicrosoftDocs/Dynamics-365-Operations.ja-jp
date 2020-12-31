---
title: 主勘定カテゴリの設定
description: このトピックでは、Dynamics 365 Finance で主勘定カテゴリを設定する方法について説明します。
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e0a015283064af2287013bccc065b4467a308c5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445112"
---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="bffb6-103">主勘定カテゴリの設定</span><span class="sxs-lookup"><span data-stu-id="bffb6-103">Set up main account categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bffb6-104">このトピックでは、主勘定カテゴリを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="bffb6-104">This topic explains how to set up main account categories.</span></span> <span data-ttu-id="bffb6-105">主勘定カテゴリは、財務報告と Power BI の既定のレポートに使用されます。</span><span class="sxs-lookup"><span data-stu-id="bffb6-105">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="bffb6-106">既定で作成される主勘定カテゴリの名前は変更できますが、削除はできません。</span><span class="sxs-lookup"><span data-stu-id="bffb6-106">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="bffb6-107">追加の勘定カテゴリを作成しレポートおよび分析に使用できます。</span><span class="sxs-lookup"><span data-stu-id="bffb6-107">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="bffb6-108">このトピックでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="bffb6-108">This topic uses the USMF demo company.</span></span>

## <a name="create-a-main-account-category"></a><span data-ttu-id="bffb6-109">主勘定カテゴリの作成</span><span class="sxs-lookup"><span data-stu-id="bffb6-109">Create a main account category</span></span>
1. <span data-ttu-id="bffb6-110">ナビゲーション ウィンドウで、**モジュール > 総勘定元帳 > 勘定科目表 > 勘定 > 主勘定カテゴリ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bffb6-110">In the navigation pane, go to **Modules > General Ledger > Chart of accounts > Accounts > Main account categories**.</span></span>
2. <span data-ttu-id="bffb6-111">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bffb6-111">Select **New**.</span></span>
3. <span data-ttu-id="bffb6-112">**主勘定カテゴリ** フィールドに一意の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="bffb6-112">In the **Main account category** field, enter a unique name.</span></span>
4. <span data-ttu-id="bffb6-113">**説明フィールド** に、主勘定カテゴリの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="bffb6-113">In the **Description field**, enter a description for the main account category.</span></span>
5. <span data-ttu-id="bffb6-114">**主勘定タイプ** フィールドで、カテゴリにリンクされる主勘定タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="bffb6-114">In the **Main account type** field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="bffb6-115">主勘定の勘定カテゴリへのリンク</span><span class="sxs-lookup"><span data-stu-id="bffb6-115">Link main accounts to account category</span></span>
1. <span data-ttu-id="bffb6-116">**主勘定をリンク** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bffb6-116">Click **Link main accounts**.</span></span>
2. <span data-ttu-id="bffb6-117">一覧で、主勘定カテゴリに割り当てる主勘定を選択するには、**リンク** された列のチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="bffb6-117">In the list, select the main accounts to assign to the main account category by checking the boxes in the **Linked** column.</span></span> <span data-ttu-id="bffb6-118">主勘定を主勘定カテゴリに割り当てると、そのカテゴリが財務報告と分析に使用された際に勘定の残高を集計します。</span><span class="sxs-lookup"><span data-stu-id="bffb6-118">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="bffb6-119">**リンク済** オプションを選択またはクリアして主勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="bffb6-119">Select or clear the **Linked** option to choose the main accounts.</span></span>
4. <span data-ttu-id="bffb6-120">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bffb6-120">Select **OK**.</span></span>
5. <span data-ttu-id="bffb6-121">**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bffb6-121">Select **Yes**.</span></span>
