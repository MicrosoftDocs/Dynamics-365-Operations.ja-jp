---
title: 源泉徴収税の支払を作成する
description: 源泉所得税の支払と転記のジョブの手順では、源泉所得税口座の未払金から源泉所得税の残高を精算し、所定の期間の源泉所得税精算口座に相殺します。 このトピックでは、源泉徴収税の支払を設定する手順を示します。
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
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
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: eae914ccafad12426cadd91c0950bada23548005
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212280"
---
# <a name="create-a-withholding-tax-payment"></a><span data-ttu-id="81745-104">源泉徴収税の支払を作成する</span><span class="sxs-lookup"><span data-stu-id="81745-104">Create a withholding tax payment</span></span>

<span data-ttu-id="81745-105">源泉所得税の支払と転記のジョブの手順では、源泉所得税口座の未払金から源泉所得税の残高を精算し、所定の期間の源泉所得税精算口座に相殺します。</span><span class="sxs-lookup"><span data-stu-id="81745-105">The Withholding tax payment job procedure settles withholding tax balances from Accounts payable on withholding tax accounts, and offsets them to the withholding tax settlement account for a given period.</span></span> <span data-ttu-id="81745-106">このトピックでは、源泉徴収税の支払を設定する手順を示します。</span><span class="sxs-lookup"><span data-stu-id="81745-106">This topic lists the steps for setting up a withholding tax payment.</span></span>

> [!NOTE] 
> <span data-ttu-id="81745-107">(売掛金管理から)源泉徴収税の支払を計算する際は、源泉徴収税の相殺は考慮されません。</span><span class="sxs-lookup"><span data-stu-id="81745-107">Withholding tax offset (from accounts receivable) is not taken into account when a withholding tax payment is calculated.</span></span>

1. <span data-ttu-id="81745-108">**ナビゲーション ウィンドウ > モジュール > 税 > 申告 > 源泉徴収税 > 源泉徴収税の支払** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="81745-108">Go to **Navigation pane > Modules > Tax > Declarations > Withholding tax > Withholding tax payment**.</span></span>
2. <span data-ttu-id="81745-109">**決済期間** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="81745-109">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="81745-110">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="81745-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="81745-111">**開始日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="81745-111">In the **From date** field, enter a date.</span></span>
5. <span data-ttu-id="81745-112">**トランザクション日付** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="81745-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="81745-113">**更新** を選択すると、源泉徴収税の支払伝票が源泉徴収税決済勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="81745-113">Select **Update** to post withholding tax payment voucher to the withholding tax settlement account.</span></span>
7. <span data-ttu-id="81745-114">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="81745-114">Click **OK**.</span></span>

![源泉徴収税支払に使用するパラメーター](media/withholding-tax-payment.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]