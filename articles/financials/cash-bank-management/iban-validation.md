---
title: "国際銀行番号 (IBAN) 口座の検証を管理"
description: "このトピックでは、国際銀行番号 (IBAN) 口座の検証を管理する方法を説明します。"
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: ja-jp
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="9c491-103">国際銀行番号 (IBAN) 口座の検証を管理</span><span class="sxs-lookup"><span data-stu-id="9c491-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c491-104">国際銀行番号 (IBAN) 口座の検証により、銀行口座に IBAN を追加するときに行われる検証の量が増加します。</span><span class="sxs-lookup"><span data-stu-id="9c491-104">International Bank Account Number (IBAN) account validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="9c491-105">IBAN の構造は、Microsoft Dynamics 365 for Finance and Operations に格納され、銀行口座で IBAN を初めて使用するときに自動的に読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="9c491-105">The structure of the IBAN is stored in Microsoft Dynamics 365 for Finance and Operation, and is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="9c491-106">銀行口座番号とは、IBAN 番号に対して定義された構造の一部です。</span><span class="sxs-lookup"><span data-stu-id="9c491-106">The bank account number is part of the structure defined for an IBAN number.</span></span> <span data-ttu-id="9c491-107">その構造に基づいて、IBAN の口座番号の長さおよび位置が、国または地域ごとの構造で定義されている位置と一致しない場合、警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9c491-107">Based on that structure, if the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you will receive warning messages.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="9c491-108">IBAN 構造の設定</span><span class="sxs-lookup"><span data-stu-id="9c491-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="9c491-109">**現金および銀行管理\>設定\> IBAN 構造**に移動します。</span><span class="sxs-lookup"><span data-stu-id="9c491-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="9c491-110">国や地域ごとの IBAN 構造は、自動的に設定されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="9c491-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="9c491-111">特定の国または地域の構造をカスタマイズする必要がある場合は、それらを編集できます。</span><span class="sxs-lookup"><span data-stu-id="9c491-111">If you must customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="9c491-112">構造定義は、それぞれの新しいリリースの一部になります。</span><span class="sxs-lookup"><span data-stu-id="9c491-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="9c491-113">**構造をリセットする**メニューを使用して、各更新後に最新の定義を読み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="9c491-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="9c491-114">銀行口座の IBAN 構造を検証</span><span class="sxs-lookup"><span data-stu-id="9c491-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="9c491-115">**現金および銀行管理\>銀行口座\>銀行口座**に移動します。</span><span class="sxs-lookup"><span data-stu-id="9c491-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="9c491-116">銀行口座を作成します。</span><span class="sxs-lookup"><span data-stu-id="9c491-116">Create a bank account.</span></span>
3. <span data-ttu-id="9c491-117">**追加情報**クイック タブで、IBAN を入力します。</span><span class="sxs-lookup"><span data-stu-id="9c491-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="9c491-118">IBAN の口座番号の長さおよび位置が、国または地域ごとの構造で定義されている位置と一致しない場合、メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9c491-118">If the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you receive a message.</span></span> <span data-ttu-id="9c491-119">IBAN の長さが IBAN 構造の長さと一致しない場合は続行できません。</span><span class="sxs-lookup"><span data-stu-id="9c491-119">You can't continue if the length of the IBAN doesn't match the length in the IBAN structure.</span></span>

    <span data-ttu-id="9c491-120">検証では、銀行口座番号が銀行口座番号を表す IBAN の一部と一致していることも確認します。</span><span class="sxs-lookup"><span data-stu-id="9c491-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="9c491-121">銀行口座番号が一致しない場合は、警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9c491-121">If the bank account number doesn't match, you receive a warning message.</span></span> <span data-ttu-id="9c491-122">このメッセージは、警告のみです。</span><span class="sxs-lookup"><span data-stu-id="9c491-122">This message is only a warning.</span></span> <span data-ttu-id="9c491-123">銀行口座番号と一致しない場合でも続行することができます。</span><span class="sxs-lookup"><span data-stu-id="9c491-123">You can continue even if the bank account number doesn't match.</span></span>

