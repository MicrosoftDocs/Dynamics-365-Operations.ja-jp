---
title: グローバル源泉徴収税の設定
description: このトピックでは、販売や購入に向けたグローバル源泉徴収税を設定する手順を説明します。
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
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7ee577651694f0553447d6e9d0851402a586f363
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060760"
---
# <a name="set-up-global-withholding-tax"></a><span data-ttu-id="423ab-103">グローバル源泉徴収税の設定</span><span class="sxs-lookup"><span data-stu-id="423ab-103">Set up global withholding tax</span></span>

<span data-ttu-id="423ab-104">このトピックでは、販売や購入に向けたグローバル源泉徴収税を設定する手順を説明します。</span><span class="sxs-lookup"><span data-stu-id="423ab-104">This topic lists the steps for setting up global withholding tax for sales and purchases.</span></span> 

1. <span data-ttu-id="423ab-105">**源泉徴収税の関係機関** ページで 、源泉徴収税の関係機関を設定します。</span><span class="sxs-lookup"><span data-stu-id="423ab-105">Set up withholding tax authorities on the **Withholding tax authorities** page.</span></span>

2. <span data-ttu-id="423ab-106">源泉徴収税精算期間を **源泉徴収税の精算期間** ページで設定 します。</span><span class="sxs-lookup"><span data-stu-id="423ab-106">Set up withholding settlement periods on the **Withholding tax settlement periods** page.</span></span>

3. <span data-ttu-id="423ab-107">**源泉徴収税 > 元帳転記グループ** ページで、源泉徴収元帳転記グループを設定 します。</span><span class="sxs-lookup"><span data-stu-id="423ab-107">Set up withholding ledger posting group on the **Withholding tax > ledger posting group** page.</span></span>

   > [!Note] 
   >
   > <span data-ttu-id="423ab-108">**源泉徴収税** の勘定は、**転記タイプ** が源泉徴収税の主要勘定に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="423ab-108">**Withholding tax** account will be assigned with a main account with **Posting type** of Withholding tax.</span></span> <span data-ttu-id="423ab-109">**源泉徴収税** オフセットの勘定は、**転記タイプ** が源泉徴収税オフセットの主要勘定に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="423ab-109">**Withholding tax offset** account will also be assigned with a main account with **Posting type** "Withholding tax offset".</span></span> <span data-ttu-id="423ab-110">**総勘定元帳 > 勘定科目表 > 勘定科目 > 主要勘定** に移動し、主要勘定の **転記の検証** サブフォームに **転記タイプ** を設定します。</span><span class="sxs-lookup"><span data-stu-id="423ab-110">Go to **General ledger > Chart of accounts > Accounts > Main accounts**, set up the **Posting type** in the **Posting validation** sub-form for the main accounts.</span></span>

4. <span data-ttu-id="423ab-111">**源泉徴収税コード** ページで 、源泉徴収税のコードを設定します。</span><span class="sxs-lookup"><span data-stu-id="423ab-111">Set up withholding tax codes on the **Withholding tax codes** page.</span></span>

5. <span data-ttu-id="423ab-112">**源泉徴収税グループ** ページで 、源泉徴収税のグループを設定します。</span><span class="sxs-lookup"><span data-stu-id="423ab-112">Set up withholding tax groups on the **Withholding tax groups** page.</span></span>

6. <span data-ttu-id="423ab-113">**源泉徴収税の収益** の **タイプ** ページで、源泉徴収税の収益タイプ を設定します。</span><span class="sxs-lookup"><span data-stu-id="423ab-113">Set up withholding tax revenue types on the **Withholding tax revenue** **types** page.</span></span>

7. <span data-ttu-id="423ab-114">品目、またはセービスの **品目の源泉徴収税グループ** ページで 、源泉徴収税のグループを設定します。</span><span class="sxs-lookup"><span data-stu-id="423ab-114">Set up withholding tax groups on the **Item withholding tax groups** page for an item or service.</span></span>

8. <span data-ttu-id="423ab-115">**総勘定元帳のパラメータ > 源泉徴収税** ページで、**請求金額の最小額** を設定します。</span><span class="sxs-lookup"><span data-stu-id="423ab-115">Set up **Minimum invoice amount** on the **General ledger parameters > Withholding tax** page.</span></span>
