---
title: SEPA の口座引落の委任状の設定
description: 顧客が債権者に署名済み委任状を付与した場合、単一ユーロ支払地域 (SEPA) の口座引落により、債権者は顧客の銀行口座から資金を収集することができます。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 24803e7157edc87e73eb6c8af404311bdf8fc5c5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245619"
---
# <a name="set-up-sepa-direct-debit-mandate"></a><span data-ttu-id="ed7a7-103">SEPA の口座引落の委任状の設定</span><span class="sxs-lookup"><span data-stu-id="ed7a7-103">Set up SEPA direct debit mandate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed7a7-104">顧客が債権者に署名済み委任状を付与した場合、単一ユーロ支払地域 (SEPA) の口座引落により、債権者は顧客の銀行口座から資金を収集することができます。</span><span class="sxs-lookup"><span data-stu-id="ed7a7-104">A Single Euro Payment Area (SEPA) direct debit lets a creditor collect funds from a customer's bank account, provided that the customer has granted a signed mandate to the creditor.</span></span> <span data-ttu-id="ed7a7-105">債権者が支払を回収することを承認する委任状に顧客が署名し、顧客の銀行に支払の回収を指示します。</span><span class="sxs-lookup"><span data-stu-id="ed7a7-105">The mandate that the customer signs authorizes the creditor to collect a payment and instructs the customer's bank to pay the collection.</span></span> <span data-ttu-id="ed7a7-106">このトピックは、SEPA 口座引落の委任状を設定するプロセスを表示するためにまとめられています。</span><span class="sxs-lookup"><span data-stu-id="ed7a7-106">This topic is organized to show the process for setting up SEPA direct debit mandates.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ed7a7-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="ed7a7-107">Prerequisites</span></span>
<span data-ttu-id="ed7a7-108">次の表に、開始する前に準備が整っている必要のある前提条件を示します。</span><span class="sxs-lookup"><span data-stu-id="ed7a7-108">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="ed7a7-109">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="ed7a7-109">Category</span></span>       | <span data-ttu-id="ed7a7-110">前提条件</span><span class="sxs-lookup"><span data-stu-id="ed7a7-110">Prerequisite</span></span>                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed7a7-111">国/地域</span><span class="sxs-lookup"><span data-stu-id="ed7a7-111">Country/region</span></span> | <span data-ttu-id="ed7a7-112">法人の基本住所は、オーストリア、ベルギー、ドイツ、スペイン、フランス、イタリア、またはオランダである必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed7a7-112">The primary address for the legal entity must be in the following countries/regions: Austria, Belgium, Germany, Spain, France, Italy, or the Netherlands.</span></span> |

1. <span data-ttu-id="ed7a7-113">口座引落の委任状の番号順序を設定します。各口座引落の委任状には固有の番号が必要になります。</span><span class="sxs-lookup"><span data-stu-id="ed7a7-113">Set up a number sequence for direct debit mandates Each direct debit mandate must have a unique number.</span></span> <span data-ttu-id="ed7a7-114">**番号順序** ページを使用して、口座引落委任状の番号順序を作成します。</span><span class="sxs-lookup"><span data-stu-id="ed7a7-114">Use the **Number sequences** page to create a number sequence for direct debit mandates.</span></span> <span data-ttu-id="ed7a7-115">この識別子を使用して、**売掛金勘定パラメーター** ページの口座引落委任状システムに番号順序を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="ed7a7-115">You will use this identifier to assign the number sequence to the direct debit mandate system on the **Accounts receivable parameters** page.</span></span>

2. <span data-ttu-id="ed7a7-116">口座引落の委任状の売掛金勘定パラメータを設定します。口座引落の委任状のパラメータを設定するため **売掛金勘定パラメータ** ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="ed7a7-116">Set up Accounts receivable parameters for direct debit mandates Use the **Accounts receivable parameters** page to set up parameters for direct debit mandates.</span></span> <span data-ttu-id="ed7a7-117">パラメータを設定するには、**口座引落** タブで、必要に応じて既定のパラメーターを変更します。</span><span class="sxs-lookup"><span data-stu-id="ed7a7-117">To set up the parameters, on the **Direct debit** tab, change the default parameters as you require.</span></span> <span data-ttu-id="ed7a7-118">その後、**番号順序** タブで、以前に設定した番号順序で **口座引落の委任状 ID** フィールドを更新します。</span><span class="sxs-lookup"><span data-stu-id="ed7a7-118">Then, on the **Number sequences** tab, update the **Direct debit mandate ID** field with the number sequence that you set up earlier.</span></span>

3. <span data-ttu-id="ed7a7-119">口座引落委任状の支払方法を設定します。口座引落委任状の支払方法を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed7a7-119">Set up a method of payment for direct debit mandates You must set up a method of payment for direct debit mandates.</span></span> <span data-ttu-id="ed7a7-120">この支払方法を使用して、口座引落支払を生成する請求書をクエリします。</span><span class="sxs-lookup"><span data-stu-id="ed7a7-120">You use this method of payment to query for invoices to generate direct debit payments for.</span></span> <span data-ttu-id="ed7a7-121">**支払方法** ページを使用して、支払方法を設定します。</span><span class="sxs-lookup"><span data-stu-id="ed7a7-121">Use the **Methods of payment** page to set up the method of payment.</span></span> <span data-ttu-id="ed7a7-122">口座引落委任状の支払方法を設定するには、支払い方法に関する次の追加手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed7a7-122">To set up a method of payment for direct debit mandates, you must follow these additional steps for a method of payment:</span></span>

-   <span data-ttu-id="ed7a7-123">**支払タイプ** フィールドで、**電子支払** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed7a7-123">In the **Payment type** field, select **Electronic payment**.</span></span>
-   <span data-ttu-id="ed7a7-124">オプション: 顧客のそれぞれに複数の委任状があると予測される場合、**期間** フィールドで **請求書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed7a7-124">Optional: If you expect each of your customers to have multiple mandates, in the **Period** field, select **Invoice**.</span></span> <span data-ttu-id="ed7a7-125">各請求書ごとの個別の支払を作成し、支払ごとに各請求書に指定された委任状が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ed7a7-125">A separate payment will be created for each invoice, and each payment will use the mandate that is specified for the invoice.</span></span>
-   <span data-ttu-id="ed7a7-126">口座引落の委任状を使用して支払を作成するには、**委任状の要求** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ed7a7-126">Select the **Require mandate** option to create payments by using direct debit mandates.</span></span> <span data-ttu-id="ed7a7-127">**委任状の要求** オプションは、**支払タイプ** フィールドで **電子支払** を選択している場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="ed7a7-127">The **Require mandate** option is available only if you select **Electronic payment** in the **Payment type** field.</span></span>

<span data-ttu-id="ed7a7-128">追加リソース</span><span class="sxs-lookup"><span data-stu-id="ed7a7-128">Additional resources</span></span>

[<span data-ttu-id="ed7a7-129">単一ユーロ支払地域 (SEPA) 口座引落の概要</span><span class="sxs-lookup"><span data-stu-id="ed7a7-129">SEPA direct debit overview</span></span>](sepa-direct-debit-overview.md) 

[<span data-ttu-id="ed7a7-130">顧客の口座引落の委任状の作成</span><span class="sxs-lookup"><span data-stu-id="ed7a7-130">Create a direct debit mandate for a customer</span></span>](tasks/create-direct-debit-mandate-customer.md) 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]