---
title: 日本の消費税レポートの設定
description: このタスクでは、日本の消費税申告をサポートするシステムの設定について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, LedgerBadDebtAccounts_JP, OMLegalEntity, TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 277451e505183d0ae2221ac1d5396ce22424d44c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "371119"
---
# <a name="setup-japan-consumption-tax-report"></a><span data-ttu-id="5d112-103">日本の消費税レポートの設定</span><span class="sxs-lookup"><span data-stu-id="5d112-103">Setup Japan consumption tax report</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5d112-104">このタスクでは、日本の消費税申告をサポートするシステムの設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="5d112-104">This task walks you through setting up the system to support the Japan consumption tax report.</span></span> <span data-ttu-id="5d112-105">このタスクでは、一般会計パラメータ、法人、売上税申告勘定および売上税コードを修正します。</span><span class="sxs-lookup"><span data-stu-id="5d112-105">In this task, you will modify General ledger parameters, a legal entity, sales tax reporting accounts and a sales tax code.</span></span> 

<span data-ttu-id="5d112-106">このタスクは デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="5d112-106">This task was created using the demo data company JPMF.</span></span>




## <a name="enable-the-consumption-tax-report"></a><span data-ttu-id="5d112-107">消費税申告を有効にする</span><span class="sxs-lookup"><span data-stu-id="5d112-107">Enable the consumption tax report</span></span>
1. <span data-ttu-id="5d112-108">[税] > [設定] > [パラメーター] > [総勘定元帳パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5d112-108">Go to Tax > Setup > Parameters > General ledger parameters.</span></span>
2. <span data-ttu-id="5d112-109">[売上税] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d112-109">Click the Sales tax tab.</span></span>
3. <span data-ttu-id="5d112-110">[日本の税申告] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="5d112-110">Expand the Japanese tax reporting section.</span></span>
4. <span data-ttu-id="5d112-111">[消費税申告] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d112-111">Select Yes in the Consumption tax reports field.</span></span>

## <a name="tax-reporting-accounts"></a><span data-ttu-id="5d112-112">税申告勘定</span><span class="sxs-lookup"><span data-stu-id="5d112-112">Tax reporting accounts</span></span>
1. <span data-ttu-id="5d112-113">[税] > [設定] > [売上税] > [税申告勘定] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5d112-113">Go to Tax > Setup > Sales tax > Tax reporting accounts.</span></span>
2. <span data-ttu-id="5d112-114">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d112-114">Click Edit.</span></span>
3. <span data-ttu-id="5d112-115">[貸倒損失] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="5d112-115">In the Bad debt field, specify the desired values.</span></span>
    * <span data-ttu-id="5d112-116">例: 84720</span><span class="sxs-lookup"><span data-stu-id="5d112-116">Example: 84720</span></span>  
4. <span data-ttu-id="5d112-117">[償却債権取立益] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="5d112-117">In the Collected bad debt field, specify the desired values.</span></span>
    * <span data-ttu-id="5d112-118">例: 84710</span><span class="sxs-lookup"><span data-stu-id="5d112-118">Example: 84710</span></span>  

## <a name="enter-japan-reporting-information-for-a-legal-entity"></a><span data-ttu-id="5d112-119">法人の日本報告書情報を入力</span><span class="sxs-lookup"><span data-stu-id="5d112-119">Enter Japan reporting information for a legal entity</span></span>
1. <span data-ttu-id="5d112-120">[組織管理] > [組織] > [法人] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5d112-120">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="5d112-121">[登録番号] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="5d112-121">Expand the Registration numbers section.</span></span>
3. <span data-ttu-id="5d112-122">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d112-122">Click Edit.</span></span>
4. <span data-ttu-id="5d112-123">[経理担当者] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5d112-123">In the Accounting personnel field, type a value.</span></span>
5. <span data-ttu-id="5d112-124">[代表者氏名または氏名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5d112-124">In the Company representative field, type a value.</span></span>

## <a name="enter-report-setup-information-for-a-sales-tax-code"></a><span data-ttu-id="5d112-125">売上税コードのレポート設定情報を入力</span><span class="sxs-lookup"><span data-stu-id="5d112-125">Enter report setup information for a sales tax code</span></span>
1. <span data-ttu-id="5d112-126">[税] > [間接税] > [売上税] > [売上税コード] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5d112-126">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="5d112-127">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="5d112-127">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5d112-128">たとえば、 [売上税コード] フィールドを「JP」の値でフィルタリングします。</span><span class="sxs-lookup"><span data-stu-id="5d112-128">For example, filter on the Sales tax code field with a value of 'JP Cons'.</span></span>
3. <span data-ttu-id="5d112-129">[レポートの設定] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="5d112-129">Expand the Report setup section.</span></span>
4. <span data-ttu-id="5d112-130">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d112-130">Click Edit.</span></span>
    * <span data-ttu-id="5d112-131">レポート コードが正しくコンフィギュレーションされたか確認します。</span><span class="sxs-lookup"><span data-stu-id="5d112-131">Confirm the reporting codes were configured properly.</span></span>   

