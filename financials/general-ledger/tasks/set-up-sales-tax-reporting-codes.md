--- 
title: "消費税レポート コードを設定します"
description: "売上税レポート コードは、売上税レポートのフィールド番号です。"
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e3863ef8d5d334c6d12e77e61d50043e5d053464
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="5d789-103">消費税レポート コードを設定します</span><span class="sxs-lookup"><span data-stu-id="5d789-103">Set up sales tax reporting codes</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5d789-104">売上税レポート コードは、売上税レポートのフィールド番号です。</span><span class="sxs-lookup"><span data-stu-id="5d789-104">The Sales tax reporting codes refer to a field number on a sales tax report.</span></span> <span data-ttu-id="5d789-105">これらは国固有のレポートのレイアウトやコード別売上税支払レポートで使用され、決済期間の売上税金額をレポート コードごとに集計して印刷します。</span><span class="sxs-lookup"><span data-stu-id="5d789-105">They are used on country specific report layouts and the Sales tax payment by code report to print sales tax amounts for a settlement period summarized per reporting code.</span></span> <span data-ttu-id="5d789-106">作成した売上税レポート コードは、[売上税コード] ページの [レポートの設定] クイック タブで参照できます。</span><span class="sxs-lookup"><span data-stu-id="5d789-106">After you create Sales tax reporting codes, you can refer to them on the Report setup FastTabs in the Sales tax code page.</span></span> 

<span data-ttu-id="5d789-107">このレコードでは、USMF デモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="5d789-107">This recording uses the DEMF demo company.</span></span>



1. <span data-ttu-id="5d789-108">[税] > [設定] > [売上税] > [売上税レポート コード] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5d789-108">Go to Tax > Setup > Sales tax > Sales tax reporting codes.</span></span>
2. <span data-ttu-id="5d789-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d789-109">Click New.</span></span>
3. <span data-ttu-id="5d789-110">レポート コードが所属するレポート レイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="5d789-110">Select the report layout that the reporting code belongs to.</span></span>
    * <span data-ttu-id="5d789-111">このレイアウトは、売上税コードに使用できるレポート コードをフィルター処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5d789-111">This layout is used to filter the available reporting codes for a Sales tax code.</span></span> <span data-ttu-id="5d789-112">各売上税コードは、レポートのレイアウトを使用する売上税所轄官庁に属する決済期間に属します。</span><span class="sxs-lookup"><span data-stu-id="5d789-112">Each Sales tax code belongs to a settlement period which belongs to a Sales tax authority which uses a Report layout.</span></span>  
4. <span data-ttu-id="5d789-113">売上税レポートのフィールドを参照する番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="5d789-113">Enter a number that refers to a field on a sales tax report.</span></span>
5. <span data-ttu-id="5d789-114">[レポート テキスト] フィールドに、レポートに表示する説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="5d789-114">In the Report text field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="5d789-115">[簡単な説明] フィールドに、社内用の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="5d789-115">In the Brief description field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="5d789-116">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d789-116">Click Save.</span></span>


