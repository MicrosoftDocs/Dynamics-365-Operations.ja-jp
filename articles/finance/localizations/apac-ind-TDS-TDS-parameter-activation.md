---
title: TDS パラメーターの設定
description: このトピックでは、パラメーターを設定して、指定されたトランザクションで源泉徴収税 (TDS) 機能を有効にする方法について説明します。 これは、源泉徴収税 TDS 機能を使用するために必要な手順です。
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
ms.openlocfilehash: dda276b7d634317aae26728f7d9f51af9ccfb896
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023386"
---
# <a name="set-the-tds-parameters"></a><span data-ttu-id="752c9-104">TDS パラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="752c9-104">Set the TDS parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="752c9-105">このトピックでは、パラメーターを設定して、指定されたトランザクションで源泉徴収税 (TDS) 機能を有効にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="752c9-105">This topic explains how to set parameters to activate Tax Deducted at Source (TDS) functionality in specified transactions.</span></span> <span data-ttu-id="752c9-106">これは、源泉徴収税 TDS 機能を使用するために必要な手順です。</span><span class="sxs-lookup"><span data-stu-id="752c9-106">This is a necessary step to use the Tax Deducted at Source TDS feature.</span></span>

1. <span data-ttu-id="752c9-107">**一般会計 \> 元帳の設定 \> 一般会計パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="752c9-107">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="752c9-108">**直接税** タブの **源泉徴収税** セクションで、**TDS の有効化** オプションを **はい** に設定して、TDS 機能とそれに使用されるページおよびフィールドを有効にします。</span><span class="sxs-lookup"><span data-stu-id="752c9-108">On the **Direct taxes** tab, in the **Tax Deducted at Source** section, set the **Activate TDS** option to **Yes** to activate the TDS functionality, and the pages and fields that are used for it.</span></span>
3. <span data-ttu-id="752c9-109">**請求書** オプションを **はい** に設定して、請求書レベルで TDS の計算および控除に使用されるフィールドを有効にします。</span><span class="sxs-lookup"><span data-stu-id="752c9-109">Set the **Invoice** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the invoice level.</span></span>
4. <span data-ttu-id="752c9-110">**支払** オプションを **はい** に設定して、支払レベルで TDS の計算および控除に使用されるフィールドを有効にします。</span><span class="sxs-lookup"><span data-stu-id="752c9-110">Set the **Payment** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the payment level.</span></span>

    <span data-ttu-id="752c9-111">[![直接税タブ](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span><span class="sxs-lookup"><span data-stu-id="752c9-111">[![Direct taxes tab](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span></span>

5. <span data-ttu-id="752c9-112">**番号順序** タブで、**参照** フィールドが **源泉徴収税の支払** に設定されている行を検索します。</span><span class="sxs-lookup"><span data-stu-id="752c9-112">On the **Number sequences** tab, find the row where the **Reference** field is set to **Withholding tax payment**.</span></span> <span data-ttu-id="752c9-113">行の **番号順序コード** フィールドで、番号順序コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="752c9-113">In the **Number sequence code** field for the row, select the number sequence code.</span></span> <span data-ttu-id="752c9-114">番号順序コードは、定期的な TDS 決済プロセスの伝票番号を生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="752c9-114">The number sequence code is used to generate voucher numbers for the periodic TDS settlement process.</span></span>

    > [!NOTE]
    > <span data-ttu-id="752c9-115">定期的な TDS 決済プロセスを実行するには、**税 \> 申告 \> 源泉徴収税 \> 源泉徴収税の支払** に移動します。</span><span class="sxs-lookup"><span data-stu-id="752c9-115">To run the periodic TDS settlement process, go to **Tax \> Declarations \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="752c9-116">[![番号順序タブ](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span><span class="sxs-lookup"><span data-stu-id="752c9-116">[![Number sequences tab](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span></span>

6. <span data-ttu-id="752c9-117">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="752c9-117">Close the page.</span></span>
