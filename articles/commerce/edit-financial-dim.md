---
title: 小売トランザクションの財務分析コードの編集
description: このトピックでは、Microsoft Dynamics 365 Commerce で小売トランザクションの財務分析コードを編集する方法について説明します。
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 381d8bb0939f6c4c163477990e49382201487375
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019910"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a><span data-ttu-id="4e4a3-103">小売トランザクションの財務分析コードの編集</span><span class="sxs-lookup"><span data-stu-id="4e4a3-103">Edit financial dimensions for retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e4a3-104">このトピックでは、Microsoft Dynamics 365 Commerce で小売トランザクションの財務分析コードを編集する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4e4a3-104">This topic describes how to edit financial dimensions for retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="edit-financial-dimensions"></a><span data-ttu-id="4e4a3-105">財務分析コードの編集</span><span class="sxs-lookup"><span data-stu-id="4e4a3-105">Edit financial dimensions</span></span>

<span data-ttu-id="4e4a3-106">Commerce 本社で小売トランザクションの財務分析コードを編集するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4e4a3-106">To edit financial dimensions for retail transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="4e4a3-107">**アプリケーション統合用の財務分析コードのコンフィギュレーション** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="4e4a3-107">Open the **Financial dimensions configuration for integrating applications** page.</span></span>
1. <span data-ttu-id="4e4a3-108">有効な **既定の分析コード統合** レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="4e4a3-108">Select the active **Default dimensions integration** record.</span></span>
1. <span data-ttu-id="4e4a3-109">**財務分析コード** クイックタブで、Excel ワークシートで編集するすべての分析コードが、**選択済** リストに表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4e4a3-109">On the **Financial dimensions** FastTab, make sure that all the dimensions that you want to edit in the Excel worksheet are present in the **Selected** list.</span></span> <span data-ttu-id="4e4a3-110">詳細については、[データ エンティティ](../fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration.md#data-entities)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4e4a3-110">For more information, see [Data entities](../fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration.md#data-entities).</span></span>
1. <span data-ttu-id="4e4a3-111">**明細書** ページ、**小売トランザクション** ページ、または **店舗の財務** ワークスペースの **トランザクションの検証エラー** タイル から Excel ファイルをダウンロードして開きます。</span><span class="sxs-lookup"><span data-stu-id="4e4a3-111">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="4e4a3-112">トランザクションの財務分析コードを変更するには、**デザイン** を選択し、**トランザクション (監査可能)** 行の横にある鉛筆の記号を選択します。</span><span class="sxs-lookup"><span data-stu-id="4e4a3-112">To change the transaction financial dimension, select **Design**, and then select the pencil symbol next to the **Transaction (auditable)** row.</span></span>
1. <span data-ttu-id="4e4a3-113">**FinancialDimensionDisplayValue** フィールドを見つけて選択し、Excel ワークシートのヘッダー部分のセルを選択して、**ラベルの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4e4a3-113">Find and select the **FinancialDimensionDisplayValue** field, select a cell in the header part of the Excel worksheet, and then select **Add label**.</span></span>
1. <span data-ttu-id="4e4a3-114">前のステップで選択したセルの下のセルを選択し、**値の追加**、**最新の情報に更新** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="4e4a3-114">Select a cell below the cell that you selected in the previous step, select **Add Value**, and then select **Refresh**.</span></span> <span data-ttu-id="4e4a3-115">財務分析コードが Excel ワークシートに追加され、編集して公開できます。</span><span class="sxs-lookup"><span data-stu-id="4e4a3-115">The financial dimensions are added to the Excel worksheet, and they can then be edited and published.</span></span>
1. <span data-ttu-id="4e4a3-116">トランザクション明細行の分析コードを変更するには、**販売トランザクション (監査可能)** 行を選択し、鉛筆の記号を選択してから、手順 6 と 7 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="4e4a3-116">To change the dimensions on the transaction lines, select the **Sales transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>
1. <span data-ttu-id="4e4a3-117">払行明細行の分析コードを変更するには、**支払トランザクション (監査可能)** 行を選択し、鉛筆の記号を選択してから、手順 6 と 7 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="4e4a3-117">To change the dimensions on the payment lines, select the **Payment transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4e4a3-118">追加リソース</span><span class="sxs-lookup"><span data-stu-id="4e4a3-118">Additional resources</span></span>

[<span data-ttu-id="4e4a3-119">現金売りトランザクションと現金管理トランザクションの編集と監査</span><span class="sxs-lookup"><span data-stu-id="4e4a3-119">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="4e4a3-120">オンライン注文トランザクションと非同期顧客注文トランザクションの編集と監査</span><span class="sxs-lookup"><span data-stu-id="4e4a3-120">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="4e4a3-121">小売トランザクションを編集するために Excel ブックを作成する</span><span class="sxs-lookup"><span data-stu-id="4e4a3-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="4e4a3-122">小売トランザクションを編集するために Excel ブックにフィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="4e4a3-122">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]