---
title: 国際銀行番号 (IBAN) 口座の検証を管理
description: このトピックでは、国際銀行番号 (IBAN) 口座の検証を管理する方法を説明します。
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: b206dbda56acd4fcd4aa98be4b5e0d6c839f0354
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976419"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="7c179-103">国際銀行番号 (IBAN) 口座の検証を管理</span><span class="sxs-lookup"><span data-stu-id="7c179-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c179-104">国際銀行番号 (IBAN) の検証により、銀行口座に IBAN を追加するときに行われる検証の量が増加します。</span><span class="sxs-lookup"><span data-stu-id="7c179-104">International Bank Account Number (IBAN) validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="7c179-105">IBAN の構造についての情報は、Microsoft Dynamics 365 Finance に格納されています。</span><span class="sxs-lookup"><span data-stu-id="7c179-105">Information about the structure of the IBAN is stored in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="7c179-106">銀行口座で IBAN を最初に使用するとき、その情報が自動的に読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="7c179-106">That information is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="7c179-107">これには、IBAN の長さ、銀行口座番号と銀行支店コードの開始位置、銀行口座番号と銀行支店コードの長さが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7c179-107">It contains the length of the IBAN, the starting positions of the bank account number and the routing number, and the length of the bank account number and routing number.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="7c179-108">IBAN 構造の設定</span><span class="sxs-lookup"><span data-stu-id="7c179-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="7c179-109">**現金および銀行管理\>設定\> IBAN 構造** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7c179-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="7c179-110">国や地域ごとの IBAN 構造は、自動的に設定されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="7c179-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="7c179-111">特定の国または地域の構造をカスタマイズする場合は、それらを編集できます。</span><span class="sxs-lookup"><span data-stu-id="7c179-111">If you want to customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="7c179-112">構造定義は、それぞれの新しいリリースの一部になります。</span><span class="sxs-lookup"><span data-stu-id="7c179-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="7c179-113">**構造をリセットする** メニューを使用して、各更新後に最新の定義を読み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="7c179-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="7c179-114">銀行口座の IBAN 構造を検証</span><span class="sxs-lookup"><span data-stu-id="7c179-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="7c179-115">**現金および銀行管理\>銀行口座\>銀行口座** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7c179-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="7c179-116">銀行口座を作成します。</span><span class="sxs-lookup"><span data-stu-id="7c179-116">Create a bank account.</span></span>
3. <span data-ttu-id="7c179-117">**追加情報** クイック タブで、IBAN を入力します。</span><span class="sxs-lookup"><span data-stu-id="7c179-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="7c179-118">IBAN の長さがそれぞれの国や地域に定義されている長さと一致しない場合、警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7c179-118">If the length of the IBAN doesn't match the length that is defined for each country or region, you will receive a warning message.</span></span> <span data-ttu-id="7c179-119">IBAN の長さが IBAN 構造で指定された長さと一致しない場合は続行できません。</span><span class="sxs-lookup"><span data-stu-id="7c179-119">You can't continue if the length of the IBAN doesn't match the length specified in the IBAN structure.</span></span>

    <span data-ttu-id="7c179-120">検証では、銀行口座番号が銀行口座番号を表す IBAN の一部と一致していることも確認します。</span><span class="sxs-lookup"><span data-stu-id="7c179-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="7c179-121">銀行口座番号が一致しない場合は、警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7c179-121">If the bank account number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="7c179-122">このメッセージは、警告のみです。</span><span class="sxs-lookup"><span data-stu-id="7c179-122">This message is only a warning.</span></span> <span data-ttu-id="7c179-123">銀行口座番号と一致しない場合でも続行することができます。</span><span class="sxs-lookup"><span data-stu-id="7c179-123">You can continue even if the bank account number doesn't match.</span></span>

    <span data-ttu-id="7c179-124">検証では、銀行支店コードが銀行支店コードを表す IBAN の一部と一致していることも確認します。</span><span class="sxs-lookup"><span data-stu-id="7c179-124">The validation also verifies that the bank routing number matches the part of the IBAN that represents the bank routing number.</span></span> <span data-ttu-id="7c179-125">銀行支店コードには、銀行番号と、多くの場合は追加の銀行支店が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7c179-125">The routing number includes a bank number and often an additional bank branch.</span></span> <span data-ttu-id="7c179-126">銀行支店コードが一致しない場合は、警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7c179-126">If the bank routing number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="7c179-127">このメッセージは、警告のみです。</span><span class="sxs-lookup"><span data-stu-id="7c179-127">This message is only a warning.</span></span> <span data-ttu-id="7c179-128">銀行支店コードが一致しない場合でも続行することができます。</span><span class="sxs-lookup"><span data-stu-id="7c179-128">You can continue even if the bank routing number doesn't match.</span></span>
