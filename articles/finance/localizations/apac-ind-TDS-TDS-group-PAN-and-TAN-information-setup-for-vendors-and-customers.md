---
title: 顧客および仕入先の TDS グループ、PAN、TAN 情報の設定
description: このトピックでは、仕入先および顧客に対する源泉徴収税 (TDS) グループ、納税者番号 (PAN)、および税勘定番号 (TAN) に関する情報の設定方法について説明します。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: fd33b1775afefed798f1e9bb7601f4112222c430
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023389"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a><span data-ttu-id="0bb2a-103">顧客および仕入先の TDS グループ、PAN、TAN 情報の設定</span><span class="sxs-lookup"><span data-stu-id="0bb2a-103">TDS group, PAN, and TAN information setup for vendors and customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0bb2a-104">このトピックでは、仕入先および顧客に対する源泉徴収税 (TDS) グループ、納税者番号 (PAN)、および税勘定番号 (TAN) に関する情報の設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0bb2a-104">This topic explains how to set up information about the Tax Deducted at Source (TDS) group, permanent account number (PAN), and tax account number (TAN) for vendors and customers.</span></span>

1. <span data-ttu-id="0bb2a-105">**買掛金勘定 \> 仕入先 \> すべての仕入先** または **売掛金勘定 \> 顧客 \> すべての顧客** に移動します。</span><span class="sxs-lookup"><span data-stu-id="0bb2a-105">Go to **Accounts payable \> Vendors \> All vendors** or **Accounts receivable \> Customers \> All customers**.</span></span>

    <span data-ttu-id="0bb2a-106">[![すべての仕入先ページ](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span><span class="sxs-lookup"><span data-stu-id="0bb2a-106">[![All vendors page](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span></span>

2. <span data-ttu-id="0bb2a-107">アクション ペインで、**新規** を選択して、仕入先または顧客を作成し、必要な詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="0bb2a-107">On the Action Pane, select **New** to create a vendor or customer, and enter the required details.</span></span> <span data-ttu-id="0bb2a-108">または、既存の仕入先または顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="0bb2a-108">Alternatively, select an existing vendor or customer.</span></span>
3. <span data-ttu-id="0bb2a-109">**請求書と配送** クイック タブの **源泉徴収税** セクションで、**源泉徴収税の計算** オプションを **はい** に設定して、仕入先または顧客の源泉徴収税、TDS、または源泉徴収 (TSC) を計算します。</span><span class="sxs-lookup"><span data-stu-id="0bb2a-109">On the **Invoice and delivery** FastTab, in the **Withholding tax** section, set the **Calculate withholding tax** option to **Yes** to calculate withholding tax, TDS, or Tax Collected at Source (TCS) for the vendor or customer.</span></span>
4. <span data-ttu-id="0bb2a-110">仕入請求書の TDS は、仕入先または顧客に対して定義されている既定の TDS グループに基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="0bb2a-110">TDS for a purchase invoice is calculated based on the default TDS group that is defined for the vendor or customer.</span></span> <span data-ttu-id="0bb2a-111">**TDS グループ** フィールドで、既定の TDS グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="0bb2a-111">In the **TDS group** field, select the default TDS group.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0bb2a-112">**TDS グループ** フィールドで TDS グループを選択した場合は、**源泉徴収税グループ** と **TCS グループ** フィールドが使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="0bb2a-112">When you select a TDS group in the **TDS group** field, the **Withholding tax group** and **TCS group** fields become unavailable.</span></span>

5. <span data-ttu-id="0bb2a-113">**税金情報** クイック タブにある **PAN 情報** セクションの **ステータス** フィールドで、仕入先または顧客の納税者番号のステータスを選択します:</span><span class="sxs-lookup"><span data-stu-id="0bb2a-113">On the **Tax information** FastTab, in the **PAN information** section, in the **Status** field, select the status of the permanent account number for the vendor or customer:</span></span>

    - <span data-ttu-id="0bb2a-114">**使用不可** – 仕入先または顧客は PAN を持っていません。</span><span class="sxs-lookup"><span data-stu-id="0bb2a-114">**Not available** – The vendor or customer doesn't have a PAN.</span></span>
    - <span data-ttu-id="0bb2a-115">**受取済** – 仕入先または顧客は、PAN を持っています。</span><span class="sxs-lookup"><span data-stu-id="0bb2a-115">**Received** – The vendor or customer has a PAN.</span></span>
    - <span data-ttu-id="0bb2a-116">**申請済** – 仕入先または顧客は PAN を申請しています。</span><span class="sxs-lookup"><span data-stu-id="0bb2a-116">**Applied** – The vendor or customer has applied for a PAN.</span></span>
    - <span data-ttu-id="0bb2a-117">**無効** – 仕入先または顧客は PAN を持っていますが、有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="0bb2a-117">**Invalid** – The vendor or customer has a PAN, but it isn't valid.</span></span>

6. <span data-ttu-id="0bb2a-118">**受取済** を **ステータス** フィールドで選択し、仕入先または顧客が PAN を持っていることを示した場合は、PAN を **番号** フィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="0bb2a-118">If you selected **Received** in the **Status** field to indicate that the vendor or customer has a PAN, enter the PAN in the **Number** field.</span></span> <span data-ttu-id="0bb2a-119">PAN は、5 文字のアルファベット、4 文字の数字、1 文字のアルファベットの順で構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0bb2a-119">The PAN must consist of five alphabetic characters, then four numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="0bb2a-120">次に例を示します: **ABCDE1260A**。</span><span class="sxs-lookup"><span data-stu-id="0bb2a-120">Here is an example: **ABCDE1260A**.</span></span>
7. <span data-ttu-id="0bb2a-121">**申請済** を **ステータス** フィールドで選択し、仕入先または顧客が PAN を申請したことを示した場合は、参照番号を **参照番号** フィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="0bb2a-121">If you selected **Applied** in the **Status** field to indicate that the vendor or customer has applied for PAN, enter the reference number in the **Reference number** field.</span></span>
8. <span data-ttu-id="0bb2a-122">**課税対象の種類** フィールドで、仕入先または顧客が属する課税対象カテゴリの種類を選択します:</span><span class="sxs-lookup"><span data-stu-id="0bb2a-122">In the **Nature of assessee** field, select the nature of assessee category that the vendor or customer belongs to:</span></span>

    - <span data-ttu-id="0bb2a-123">法人</span><span class="sxs-lookup"><span data-stu-id="0bb2a-123">Company</span></span>
    - <span data-ttu-id="0bb2a-124">HUF</span><span class="sxs-lookup"><span data-stu-id="0bb2a-124">HUF</span></span>
    - <span data-ttu-id="0bb2a-125">確定</span><span class="sxs-lookup"><span data-stu-id="0bb2a-125">Firm</span></span>
    - <span data-ttu-id="0bb2a-126">個人</span><span class="sxs-lookup"><span data-stu-id="0bb2a-126">Individual</span></span>
    - <span data-ttu-id="0bb2a-127">AOP</span><span class="sxs-lookup"><span data-stu-id="0bb2a-127">AOP</span></span>
    - <span data-ttu-id="0bb2a-128">BOI</span><span class="sxs-lookup"><span data-stu-id="0bb2a-128">BOI</span></span>
    - <span data-ttu-id="0bb2a-129">地方自治体</span><span class="sxs-lookup"><span data-stu-id="0bb2a-129">Local authority</span></span>
    - <span data-ttu-id="0bb2a-130">その他</span><span class="sxs-lookup"><span data-stu-id="0bb2a-130">Others</span></span>

    <span data-ttu-id="0bb2a-131">[![税金情報クイック タブ](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span><span class="sxs-lookup"><span data-stu-id="0bb2a-131">[![Tax information FastTab](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span></span>

9. <span data-ttu-id="0bb2a-132">アクション ペインの **仕入先** タブにある **登録** グループで、**登録 ID** を選択して、**住所の管理** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="0bb2a-132">On the Action Pane, on the **Vendor** tab, in the **Registration** group, select **Registration IDs** to open the **Manage addresses** page.</span></span>
10. <span data-ttu-id="0bb2a-133">**住所の管理** ページの **税金情報** クイック タブで、**追加** または **編集** を選択して **税金情報の管理** ページを開き、税金登録エントリを管理できます。</span><span class="sxs-lookup"><span data-stu-id="0bb2a-133">On the **Manage addresses** page, on the **Tax information** FastTab, select **Add** or **Edit** to open the **Manage tax information** page, where you can maintain the tax registration entry.</span></span>
11. <span data-ttu-id="0bb2a-134">**税金情報の管理** ページの **源泉徴収税** クイック タブにある **税勘定番号 (TAN)** フィールドに TAN を入力します。</span><span class="sxs-lookup"><span data-stu-id="0bb2a-134">On the **Manage tax information** page, on the **Withholding tax** FastTab, in the **Tax Account Number (TAN)** field, enter the TAN.</span></span> <span data-ttu-id="0bb2a-135">TAN は、4 文字のアルファベット、5 文字の数字、1 文字のアルファベットの順で構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0bb2a-135">The TAN must consist of four alphabetic characters, then five numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="0bb2a-136">次に例を示します: **AFGH54821T**。</span><span class="sxs-lookup"><span data-stu-id="0bb2a-136">Here is an example: **AFGH54821T**.</span></span>
12. <span data-ttu-id="0bb2a-137">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0bb2a-137">Close the page.</span></span>
