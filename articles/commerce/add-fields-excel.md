---
title: 小売トランザクションを編集するために Excel ブックにフィールドを追加する
description: このトピックでは、Microsoft Dynamics 365 Commerce で小売トランザクションを編集できるように、Microsoft Excel ブックにフィールドを追加する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: fb0435a617585689a87caa76f80e9774182576cc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206322"
---
# <a name="add-fields-to-an-excel-workbook-to-edit-retail-transactions"></a><span data-ttu-id="c6daf-103">小売トランザクションを編集するために Excel ブックにフィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="c6daf-103">Add fields to an Excel workbook to edit retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6daf-104">このトピックでは、Microsoft Dynamics 365 Commerce で小売トランザクションを編集できるように、Microsoft Excel ブックにフィールドを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c6daf-104">This topic describes how to add fields to a Microsoft Excel workbook so that you can edit retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c6daf-105">概要</span><span class="sxs-lookup"><span data-stu-id="c6daf-105">Overview</span></span>

<span data-ttu-id="c6daf-106">小売トランザクションを編集できるように Excel ファイルを生成するときに、ファイルの一部の既定のフィールドは入力されます。</span><span class="sxs-lookup"><span data-stu-id="c6daf-106">When you generate an Excel file so that you can edit retail transactions, the file is filled with some default fields.</span></span> <span data-ttu-id="c6daf-107">生成された Excel ファイルに更新が必要なフィールドが既定で表示されない場合は、追加できます。</span><span class="sxs-lookup"><span data-stu-id="c6daf-107">If a field that must be updated isn't visible by default in the generated Excel file, you can add it.</span></span>

## <a name="add-fields-to-a-worksheet-in-an-excel-workbook"></a><span data-ttu-id="c6daf-108">Excel ブックのワークシートにフィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="c6daf-108">Add fields to a worksheet in an Excel workbook</span></span>

<span data-ttu-id="c6daf-109">小売トランザクションを編集できるように、Excel ブックにフィールドを追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c6daf-109">To add fields to an Excel workbook so that you can edit retail transactions, follow these steps.</span></span>

1. <span data-ttu-id="c6daf-110">**明細書** ページ、**小売トランザクション** ページ、または **店舗の財務** ワークスペースの **トランザクションの検証エラー** タイル から Excel ファイルをダウンロードして開きます。</span><span class="sxs-lookup"><span data-stu-id="c6daf-110">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="c6daf-111">**デザイン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6daf-111">Select **Design**.</span></span>
1. <span data-ttu-id="c6daf-112">目的のテーブルの鉛筆の記号を選択し、使用可能なフィールドの一覧で追加するフィールドを検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="c6daf-112">Select the pencil symbol for the desired table, and then, in the list of available fields, find and select the field that you want to add.</span></span>
1. <span data-ttu-id="c6daf-113">**追加** を選択してから **更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6daf-113">Select **Add**, and then select **Update**.</span></span> <span data-ttu-id="c6daf-114">フィールドの順序を変更できます。</span><span class="sxs-lookup"><span data-stu-id="c6daf-114">You can reorder fields.</span></span>
1. <span data-ttu-id="c6daf-115">更新が完了したら、**更新** を選択して新しい列のデータをフェッチします。</span><span class="sxs-lookup"><span data-stu-id="c6daf-115">After the update is completed, select **Refresh** to fetch the data for the new column.</span></span>

<span data-ttu-id="c6daf-116">これで、新しいフィールドとデータを Excel で編集できるようになります。</span><span class="sxs-lookup"><span data-stu-id="c6daf-116">The new field and data for it should now be available for editing in Excel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c6daf-117">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c6daf-117">Additional resources</span></span>

[<span data-ttu-id="c6daf-118">現金売りトランザクションと現金管理トランザクションの編集と監査</span><span class="sxs-lookup"><span data-stu-id="c6daf-118">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="c6daf-119">オンライン注文トランザクションと非同期顧客注文トランザクションの編集と監査</span><span class="sxs-lookup"><span data-stu-id="c6daf-119">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="c6daf-120">小売トランザクションの財務分析コードの編集</span><span class="sxs-lookup"><span data-stu-id="c6daf-120">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="c6daf-121">小売トランザクションを編集するために Excel ブックを作成する</span><span class="sxs-lookup"><span data-stu-id="c6daf-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]