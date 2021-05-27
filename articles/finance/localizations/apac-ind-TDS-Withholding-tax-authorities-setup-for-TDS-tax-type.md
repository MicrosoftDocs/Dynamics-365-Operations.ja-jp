---
title: TDS 税タイプに対する源泉徴収税オーソリティの設定
description: このトピックでは、源泉徴収税 (TDS) オーソリティの設定方法について説明します。
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
ms.openlocfilehash: 5375363a9b1383a83e80fc3c4b841780adab4172
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023380"
---
# <a name="set-up-withholding-tax-authorities-for-the-tds-tax-type"></a><span data-ttu-id="10c3e-103">TDS 税タイプに対する源泉徴収税オーソリティの設定</span><span class="sxs-lookup"><span data-stu-id="10c3e-103">Set up withholding tax authorities for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10c3e-104">このトピックでは、源泉徴収税 (TDS) オーソリティの設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="10c3e-104">This topic explains how to set up Tax Deducted at Source (TDS) authorities.</span></span>

1. <span data-ttu-id="10c3e-105">**税 \> 間接税 \> 源泉徴収税オーソリティ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="10c3e-105">Go to **Tax \> Indirect taxes \> Withholding tax authorities**.</span></span>

    <span data-ttu-id="10c3e-106">[![源泉徴収税オーソリティ ページ](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span><span class="sxs-lookup"><span data-stu-id="10c3e-106">[![Withholding tax authorities page](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span></span>

2. <span data-ttu-id="10c3e-107">**税タイプ** フィールドで、**TDS** を選択して、TDS 税タイプの源泉徴収税オーソリティを設定します。</span><span class="sxs-lookup"><span data-stu-id="10c3e-107">In the **Tax type** field, select **TDS** to set up withholding tax authorities for the TDS tax type.</span></span>
3. <span data-ttu-id="10c3e-108">アクション ウィンドウで **新規** を選択して、明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="10c3e-108">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="10c3e-109">**源泉徴収税オーソリティ** フィールドに、TDS オーソリティの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="10c3e-109">In the **Withholding tax authority** field, enter a name for the TDS authority.</span></span>
5. <span data-ttu-id="10c3e-110">**説明** フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="10c3e-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="10c3e-111">**一般** クイックタブの、**仕入先アカウント** フィールドで、TDS オーソリティの仕入先アカウントを選択します。</span><span class="sxs-lookup"><span data-stu-id="10c3e-111">On the **General** FastTab, in the **Vendor account** field, select the vendor account for the TDS authority.</span></span>

    > [!NOTE]
    > <span data-ttu-id="10c3e-112">TDS オーソリティ仕入先に支払う必要がある預金を行う銀行の名前を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10c3e-112">You must define the name of the bank where funds that are owed to the TDS authority vendor will be deposited.</span></span> <span data-ttu-id="10c3e-113">銀行の名前は **銀行口座** ページ (**買掛金勘定 \> すべての仕入先 \> 仕入先 \> 設定 \> 銀行口座**)。</span><span class="sxs-lookup"><span data-stu-id="10c3e-113">The bank's name is defined on the **Bank accounts** page (**Accounts payable \> All vendors \> Vendor \> Set up \> Bank accounts**).</span></span>

7. <span data-ttu-id="10c3e-114">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="10c3e-114">Close the page.</span></span>
