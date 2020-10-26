---
title: 消費税レポート コードを設定します
description: 売上税レポート コードは、売上税レポートのフィールド番号です。
author: twheeloc
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6c18f4fb0db31a959647bb10d2b99d940646676e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976796"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="8ba53-103">消費税レポート コードを設定します</span><span class="sxs-lookup"><span data-stu-id="8ba53-103">Set up sales tax reporting codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8ba53-104">売上税レポート コードは、売上税レポートのフィールド番号です。</span><span class="sxs-lookup"><span data-stu-id="8ba53-104">The Sales tax reporting codes refer to a field number on a sales tax report.</span></span> <span data-ttu-id="8ba53-105">これらは国固有のレポートのレイアウトやコード別売上税支払レポートで使用され、決済期間の売上税金額をレポート コードごとに集計して印刷します。</span><span class="sxs-lookup"><span data-stu-id="8ba53-105">They are used on country specific report layouts and the Sales tax payment by code report to print sales tax amounts for a settlement period summarized per reporting code.</span></span> <span data-ttu-id="8ba53-106">作成した売上税レポート コードは、[売上税コード] ページの [レポートの設定] クイック タブで参照できます。</span><span class="sxs-lookup"><span data-stu-id="8ba53-106">After you create Sales tax reporting codes, you can refer to them on the Report setup FastTabs in the Sales tax code page.</span></span> 

<span data-ttu-id="8ba53-107">このレコードでは、USMF デモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="8ba53-107">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="8ba53-108">**ナビゲーション ウィンドウ**で、 **税 > 設定 > 売上税 > 売上税レポート コード**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8ba53-108">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="8ba53-109">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ba53-109">Click **New**.</span></span>
3. <span data-ttu-id="8ba53-110">レポート コードが所属するレポート レイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="8ba53-110">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="8ba53-111">このレイアウトは、売上税コードに使用できるレポート コードをフィルター処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8ba53-111">This layout is used to filter the available reporting codes for a Sales tax code.</span></span> <span data-ttu-id="8ba53-112">各売上税コードは、レポートのレイアウトを使用する売上税所轄官庁に属する決済期間に属します。</span><span class="sxs-lookup"><span data-stu-id="8ba53-112">Each Sales tax code belongs to a settlement period which belongs to a Sales tax authority which uses a Report layout.</span></span>  
4. <span data-ttu-id="8ba53-113">**レポート コード** フィールドに数を入力します。</span><span class="sxs-lookup"><span data-stu-id="8ba53-113">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="8ba53-114">**レポート テキスト** フィールドに、レポートに表示する説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="8ba53-114">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="8ba53-115">**簡単な説明**フィールドに、社内用の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="8ba53-115">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="8ba53-116">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ba53-116">Click **Save**.</span></span>

