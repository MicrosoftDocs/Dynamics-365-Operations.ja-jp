---
title: TDS 税タイプに対する源泉徴収税レポートの設定
description: 源泉徴収税レポート コードは、源泉徴収税 (TDS) のフォーム 26Q およびフォーム 27Q ステートメントを生成するために使用されます。 このトピックでは、TDS レポート コードを設定できるよう、源泉徴収税レポート コードの手順を設定する方法について説明します。
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
ms.openlocfilehash: 1f9325d182f89b98e8b943ae047c55e7e1aeb02f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023398"
---
# <a name="set-up-withholding-tax-reporting-codes-for-the-tds-tax-type"></a><span data-ttu-id="9af42-104">TDS 税タイプに対する源泉徴収税レポートの設定</span><span class="sxs-lookup"><span data-stu-id="9af42-104">Set up withholding tax reporting codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9af42-105">源泉徴収税レポート コードは、源泉徴収税 (TDS) のフォーム 26Q およびフォーム 27Q ステートメントを生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9af42-105">Withholding tax reporting codes are used to generate Form 26Q and Form 27Q statements for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="9af42-106">このトピックでは、TDS レポート コードを設定できるよう、源泉徴収税レポート コードの手順を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9af42-106">This topic explains how to set up withholding tax reporting codes steps so that you can set up TDS reporting codes.</span></span>

1. <span data-ttu-id="9af42-107">**税 \> 設定 \> 源泉徴収税 \> 源泉徴収税レポート コード** に移動します。</span><span class="sxs-lookup"><span data-stu-id="9af42-107">Go to **Tax \> Setup \> Withholding tax \> Withholding tax reporting codes**.</span></span>

    <span data-ttu-id="9af42-108">[![源泉徴収税レポート コード ページ](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span><span class="sxs-lookup"><span data-stu-id="9af42-108">[![Withholding tax reporting codes page](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span></span>

2. <span data-ttu-id="9af42-109">**税タイプ** フィールドで、**TDS** を選択して、TDS 税タイプの源泉徴収税レポート コードを定義します。</span><span class="sxs-lookup"><span data-stu-id="9af42-109">In the **Tax type** field, select **TDS** to define withholding tax reporting codes for the TDS tax type.</span></span>
3. <span data-ttu-id="9af42-110">**源泉徴収税コンポーネント** フィールドで、源泉徴収税のレポート コードを定義する TDS コンポーネントを選択します。</span><span class="sxs-lookup"><span data-stu-id="9af42-110">In the **Withholding tax component** field, select the TDS component to that you're defining the withholding tax reporting code for.</span></span> <span data-ttu-id="9af42-111">**源泉徴収税コンポーネント グループ** フィールドには、定義している TDS コンポーネントに対して定義された TDS コンポーネント グループ が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9af42-111">The **Withholding tax component group** field shows the TDS component group that was defined for the TDS component that you're defining.</span></span>

    <span data-ttu-id="9af42-112">**一般** クイック タブの **セクション コード** フィールドには、TDS コンポーネント グループに関連付けられたセクション コード が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9af42-112">The **Section code** field on the **General** FastTab shows the section code that is attached to the TDS component group.</span></span>

4. <span data-ttu-id="9af42-113">**一般** クイックタブの **レポート コード** フィールドで、TDS レポート コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="9af42-113">On the **General** FastTab, in the **Reporting code** field, select the TDS reporting code:</span></span>

    - <span data-ttu-id="9af42-114">TDS</span><span class="sxs-lookup"><span data-stu-id="9af42-114">TDS</span></span>
    - <span data-ttu-id="9af42-115">TCS</span><span class="sxs-lookup"><span data-stu-id="9af42-115">TCS</span></span>
    - <span data-ttu-id="9af42-116">割増金</span><span class="sxs-lookup"><span data-stu-id="9af42-116">Surcharge</span></span>
    - <span data-ttu-id="9af42-117">PE\_Cess</span><span class="sxs-lookup"><span data-stu-id="9af42-117">PE\_Cess</span></span>
    - <span data-ttu-id="9af42-118">SHE\_Cess</span><span class="sxs-lookup"><span data-stu-id="9af42-118">SHE\_Cess</span></span>

5. <span data-ttu-id="9af42-119">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9af42-119">Close the page.</span></span>
