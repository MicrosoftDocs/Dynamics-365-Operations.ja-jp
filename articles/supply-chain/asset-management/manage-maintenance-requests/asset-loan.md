---
title: 資産ローン
description: このトピックでは、資産管理でローン資産を登録する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9a365fb5b1e0126b9de56bcc84a14f2352208d4f
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571717"
---
# <a name="asset-loans"></a><span data-ttu-id="cd114-103">資産ローン</span><span class="sxs-lookup"><span data-stu-id="cd114-103">Asset loans</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="cd114-104">会社が内部の場所または顧客から、修理またはメンテナンス ジョブ用の資産を受け取り、それらの場所または顧客に資産を一時的に貸与する場合、資産管理は資産ローンを追跡できます。</span><span class="sxs-lookup"><span data-stu-id="cd114-104">If your company receives assets for repair or maintenance jobs from either internal locations or customers, and if you temporarily loan assets to those locations or customers, Asset Management can track the asset loans.</span></span>

## <a name="register-asset-loans-on-a-maintenance-request"></a><span data-ttu-id="cd114-105">メンテナンス要求で資産ローンを登録する</span><span class="sxs-lookup"><span data-stu-id="cd114-105">Register asset loans on a maintenance request</span></span>

1. <span data-ttu-id="cd114-106">**資産管理** \> **共通** \> **メンテナンス要求** \> **すべてのメンテナンス要求**または**有効なメンテナンス要求**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd114-106">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="cd114-107">資産ローンを登録するメンテナンス要求を選択してから、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd114-107">Select the maintenance request to register an asset loan on, and then select **Edit**.</span></span>
3. <span data-ttu-id="cd114-108">**要求**ページで、**ローン資産の送信**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd114-108">On the **Request** page, select **Send loan asset**.</span></span>
4. <span data-ttu-id="cd114-109">資産を選択し、返却予定日を入力します。</span><span class="sxs-lookup"><span data-stu-id="cd114-109">Select the asset, and enter the expected return date.</span></span>
5. <span data-ttu-id="cd114-110">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd114-110">Select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="cd114-111">ローン資産は、同じ資産タイプの資産が使用可能な場合にのみ送信できます。</span><span class="sxs-lookup"><span data-stu-id="cd114-111">You can send a loan asset only if an asset of the same asset type is available.</span></span>
> - <span data-ttu-id="cd114-112">貸与する資産には、**InStorage** など、ローン資産として使用できる資産ライフサイクルの状態が必要です。</span><span class="sxs-lookup"><span data-stu-id="cd114-112">The asset that you loan must have an asset lifecycle state that allows it to be used as a loan asset, such as **InStorage**.</span></span> <span data-ttu-id="cd114-113">資産ローンが登録されると、その資産の資産ライフサイクルの状態が **OnLoan** などに自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="cd114-113">When the asset loan is registered, the asset lifecycle state of the asset is automatically updated to, for example, **OnLoan**.</span></span>

<span data-ttu-id="cd114-114">他の場所または顧客に貸与したすべての資産の一覧を表示するには、**資産管理** \> **共通** \> **資産ローン** \> **すべての資産ローン**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd114-114">To view a list of all the assets that you've loaned to other locations or customers, select **Asset management** \> **Common** \> **Asset loan** \> **All asset loans**.</span></span> <span data-ttu-id="cd114-115">資産に対して**終了**チェック ボックスがオンの場合、資産は会社に返却済として登録されています。</span><span class="sxs-lookup"><span data-stu-id="cd114-115">If the **Ended** check box is selected for an asset, the asset has been registered as returned to your company.</span></span>

![メンテナンス要求の管理](media/06-manage-maintenance-requests.png)

<span data-ttu-id="cd114-117">**有効な資産ローン** ページで、会社に返却されていないすべてのローン資産の一覧を表示できます。</span><span class="sxs-lookup"><span data-stu-id="cd114-117">On the **Active asset loans** page, you can view a list of all the loan assets that haven't yet been returned to your company.</span></span>

## <a name="register-loan-assets-as-returned"></a><span data-ttu-id="cd114-118">ローン資産を返却済として登録する</span><span class="sxs-lookup"><span data-stu-id="cd114-118">Register loan assets as returned</span></span>

1. <span data-ttu-id="cd114-119">**資産管理** \> **共通** \> **資産ローン** \> **有効な資産ローン**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd114-119">Select **Asset management** \> **Common** \> **Asset loan** \> **Active asset loans**.</span></span>
2. <span data-ttu-id="cd114-120">返却済として登録する資産ローンを選択し、**資産ローンの返却**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd114-120">Select the asset loan to register as returned, and then select **Return asset loan**.</span></span>
3. <span data-ttu-id="cd114-121">**返却済**フィールドで、日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="cd114-121">In the **Returned** field, enter the date and time.</span></span>
4. <span data-ttu-id="cd114-122">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd114-122">Select **OK**.</span></span>
5. <span data-ttu-id="cd114-123">**有効な資産ローン** リスト ページを更新し、資産ローンが一覧に表示されなくなったことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="cd114-123">Refresh the **Active asset loans** list page, and notice that the asset loan no longer appears in the list.</span></span>
