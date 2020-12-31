---
title: 消費税レポート コードを設定します
description: 売上税レポート コードは、売上税レポートにリストされたフィールド番号です。
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
ms.openlocfilehash: 362d30e56fe35b85d50bfa2df57364733b366fef
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646184"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="a3599-103">消費税レポート コードを設定します</span><span class="sxs-lookup"><span data-stu-id="a3599-103">Set up sales tax reporting codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a3599-104">売上税レポート コードは、売上税レポートにリストされたフィールド番号です。</span><span class="sxs-lookup"><span data-stu-id="a3599-104">The Sales tax reporting codes refer to a field number that's listed on a sales tax report.</span></span> <span data-ttu-id="a3599-105">これらは、国別のレポート レイアウトで使用されます。</span><span class="sxs-lookup"><span data-stu-id="a3599-105">They are used on country-specific report layouts.</span></span> <span data-ttu-id="a3599-106">コード別売上税支払レポートでも使用されます。</span><span class="sxs-lookup"><span data-stu-id="a3599-106">They're also used on the Sales tax payment by code report.</span></span> <span data-ttu-id="a3599-107">このレポートには、レポート コードごとに集計された決済期間の売上税金額が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3599-107">That report shows sales tax amounts for a settlement period summarized for each reporting code.</span></span> <span data-ttu-id="a3599-108">作成した売上税レポート コードは、**売上税コード** ページからアクセスできるの [レポートの設定] クイック タブで参照できます。</span><span class="sxs-lookup"><span data-stu-id="a3599-108">After you create Sales tax reporting codes, you can refer to those codes on the Report setup FastTabs, which you can access from the **Sales tax code** page.</span></span> 

<span data-ttu-id="a3599-109">このレコードでは、USMF デモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="a3599-109">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="a3599-110">**ナビゲーション ウィンドウ** で、 **税 > 設定 > 売上税 > 売上税レポート コード** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a3599-110">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="a3599-111">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3599-111">Click **New**.</span></span>
3. <span data-ttu-id="a3599-112">レポート コードが所属するレポート レイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="a3599-112">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="a3599-113">このレイアウトは、売上税コードに使用できるレポート コードをフィルター処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a3599-113">This layout is used to filter the available reporting codes for a sales tax code.</span></span> <span data-ttu-id="a3599-114">各売上税コードは、レポートのレイアウトを使用する売上税所轄官庁に属する決済期間に属します。</span><span class="sxs-lookup"><span data-stu-id="a3599-114">Each sales tax code belongs to a settlement period, which belongs to a Sales tax authority, which uses a report layout.</span></span>  
4. <span data-ttu-id="a3599-115">**レポート コード** フィールドに数を入力します。</span><span class="sxs-lookup"><span data-stu-id="a3599-115">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="a3599-116">**レポート テキスト** フィールドに、レポートに表示する説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="a3599-116">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="a3599-117">**簡単な説明** フィールドに、社内用の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="a3599-117">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="a3599-118">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3599-118">Click **Save**.</span></span>

