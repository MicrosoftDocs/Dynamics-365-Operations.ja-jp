---
title: コード別消費税支払レポートの印刷
description: このトピックでは、会計または税コードの通貨でコード別消費税支払レポートを印刷するために必要な設定とアクションについて説明します。
author: anasyash
manager: AnnBe
ms.date: 04/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 3c3b251aadfa997f453e60b0842f89a6f09eb9cb
ms.sourcegitcommit: 88347d0f0ac862a77f269a05f1801d30dc93586e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2020
ms.locfileid: "3260258"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a><span data-ttu-id="cc906-103">コード別消費税支払レポートの印刷</span><span class="sxs-lookup"><span data-stu-id="cc906-103">Print the Sales tax payment by code report</span></span> 

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="cc906-104">**コード別消費税支払** レポートを印刷するには、**税** \> **照会およびレポート** \> **消費税レポート** \> **コード別消費税支払** に移動します。</span><span class="sxs-lookup"><span data-stu-id="cc906-104">To print the **Sales tax payment by code** report, go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span> <span data-ttu-id="cc906-105">既定では、レポート金額は、**消費税レポート コード** ページで設定されたすべてのレポート コードについて法人の会計通貨で生成されます。</span><span class="sxs-lookup"><span data-stu-id="cc906-105">By default, report amounts are generated in the accounting currency of the legal entity for all reporting codes that are set up on the **Sales tax reporting codes** page.</span></span>

<span data-ttu-id="cc906-106">また、このレポートを生成して、**消費税コード** ページで消費税コードに割り当てられているすべてのレポート コードについて、消費税コードの通貨で消費税支払額を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="cc906-106">You can also generate this report so that it shows the sales tax payment amounts in the currencies of sales tax codes for all reporting codes that are assigned to sales tax codes on the **Sales tax codes** page.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="cc906-107">機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="cc906-107">Turn on the feature</span></span>

<span data-ttu-id="cc906-108">**機能管理** ワークスペースで、次の機能を有効にします: **コード別消費税支払レポートを消費税コードの通貨で生成する**。</span><span class="sxs-lookup"><span data-stu-id="cc906-108">In the **Feature management** workspace, turn on the following feature: **Generate the Sales tax payment by code report in the sales tax code currency**.</span></span>

## <a name="run-the-report"></a><span data-ttu-id="cc906-109">レポートの実行</span><span class="sxs-lookup"><span data-stu-id="cc906-109">Run the report</span></span>

1. <span data-ttu-id="cc906-110">**税** \> **照会およびレポート** \> **消費税レポート** \> **コード別消費税支払** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cc906-110">Go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span>
2. <span data-ttu-id="cc906-111">**レポート通貨** フィールドで、次のいずれかの値を選択します:</span><span class="sxs-lookup"><span data-stu-id="cc906-111">In the **Report currency** field, select one of the following values:</span></span>

    - <span data-ttu-id="cc906-112">**会計通貨** – レポート金額を会計通貨で印刷します。</span><span class="sxs-lookup"><span data-stu-id="cc906-112">**Accounting currency** – Print the report amounts in the accounting currency.</span></span>
    - <span data-ttu-id="cc906-113">**消費税コードの通貨** – 消費税コードの通貨でレポート金額を印刷します。</span><span class="sxs-lookup"><span data-stu-id="cc906-113">**Sales tax code currency** – Print the report amounts in the currencies of sales tax codes.</span></span>

    ![コード別消費税支払ダイアログ ボックス](media/Sales-tax-payment-by-code.png)

<span data-ttu-id="cc906-115">次の図で、生成されるレポートの例を示します。</span><span class="sxs-lookup"><span data-stu-id="cc906-115">The following illustration shows an example of the report that is generated.</span></span> <span data-ttu-id="cc906-116">レポート コードが割り当てられている消費税コードに対して **消費税通貨** フィールドが **EUR** に設定されている場合、レポート コード **101** が通貨 **EUR** であることがレポートに表示されます。</span><span class="sxs-lookup"><span data-stu-id="cc906-116">The report shows that reporting code **101** has the **EUR** currency if the **Sales tax currency** field is set to **EUR** for the sales tax code that the reporting code is assigned to.</span></span>

![コード別消費税支払レポートの例](media/Sales-tax-payment-by-code-2.png)
