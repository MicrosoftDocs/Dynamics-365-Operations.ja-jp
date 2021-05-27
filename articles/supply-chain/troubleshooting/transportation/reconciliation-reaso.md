---
title: 調整の理由から、主勘定のみを貸方勘定として追加できる
description: 輸送管理で調整理由を設定した場合、主勘定のみを貸方勘定として追加できます。
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 708081370b27fd51ef9a2329d8392f4515353dcb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026663"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a><span data-ttu-id="7d2b6-103">調整の理由から、主勘定のみを貸方勘定として追加できる</span><span class="sxs-lookup"><span data-stu-id="7d2b6-103">You can add only the main account as the credit account for reconciliation reasons</span></span>

<span data-ttu-id="7d2b6-104">KB 番号: 4603538</span><span class="sxs-lookup"><span data-stu-id="7d2b6-104">KB number: 4603538</span></span>

## <a name="symptoms"></a><span data-ttu-id="7d2b6-105">現象</span><span class="sxs-lookup"><span data-stu-id="7d2b6-105">Symptoms</span></span>

<span data-ttu-id="7d2b6-106">輸送管理で調整理由を設定した場合、主勘定のみを貸方勘定として追加できます。</span><span class="sxs-lookup"><span data-stu-id="7d2b6-106">When you set up a reconciliation reason in Transportation management, you can add only the main account as the credit account.</span></span> <span data-ttu-id="7d2b6-107">コスト センターまたは他の分析コードを貸方勘定として追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="7d2b6-107">You can't add a cost center or any other dimension as the credit account.</span></span> <span data-ttu-id="7d2b6-108">ただし、借方勘定では他の分析コードを選択できます。</span><span class="sxs-lookup"><span data-stu-id="7d2b6-108">However, the debit account lets you select other dimensions.</span></span>

## <a name="resolution"></a><span data-ttu-id="7d2b6-109">解像度</span><span class="sxs-lookup"><span data-stu-id="7d2b6-109">Resolution</span></span>

<span data-ttu-id="7d2b6-110">調整で仕入先への支払は行われなかったが、特定の主勘定の貸方に転記される場合、調整理由の設定時に貸方勘定の財務分析コードを選択することはできません。</span><span class="sxs-lookup"><span data-stu-id="7d2b6-110">If the reconciliation isn't done to pay the vendor but to credit a specific main account, the system doesn't allow you to select a financial dimension for the credit account when you set up the reconciliation reason.</span></span>

<span data-ttu-id="7d2b6-111">勘定構造で貸方主勘定に対して特定の財務分析コード値が必要な場合は、財務分析コード値が存在しないため、結果の仕入先仕訳帳を自動的に転記することはできません。</span><span class="sxs-lookup"><span data-stu-id="7d2b6-111">If the account structure requires a specific financial dimension value for the credit main account, the resulting vendor journal can't be posted automatically, because the financial dimension value is missing.</span></span> <span data-ttu-id="7d2b6-112">したがって、最初に **請求仕訳帳** ページを使用して貸方勘定を手動で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d2b6-112">Therefore, you must first manually specify the credit account by using the **Invoice journal** page.</span></span>

<span data-ttu-id="7d2b6-113">貸方勘定には分析コード値が必要なため、仕入先請求仕訳帳を自動的に転記することはできません。</span><span class="sxs-lookup"><span data-stu-id="7d2b6-113">Because a dimension value is required for the credit account, the vendor invoice journal can't be automatically posted.</span></span> <span data-ttu-id="7d2b6-114">貸方記入行の主勘定に分析コード値を手動で追加した後、手動で転記する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d2b6-114">You must manually post it after you manually add the dimension value to the main account for the credit line.</span></span>
