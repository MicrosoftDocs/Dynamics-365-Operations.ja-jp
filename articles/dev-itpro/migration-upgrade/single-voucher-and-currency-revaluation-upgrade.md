---
title: "単一伝票と通貨再評価のアップグレード"
description: "一部の組織では、複数の顧客または仕入先がある単一伝票を含む仕訳帳を入力し、売掛金勘定または買掛金勘定の外貨再評価プロセスも実行します。 このトピックでは、これらの組織が Microsoft Dynamics 365 for Operations バージョン 1611 にアップグレードする際に従うべき手順について説明します。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 13ad43cc77731727525aae1edc4d405c166acbc1
ms.contentlocale: ja-jp
ms.lasthandoff: 07/18/2017

---

# <a name="single-voucher-and-currency-revaluation-upgrade"></a><span data-ttu-id="30450-104">単一伝票と通貨再評価のアップグレード</span><span class="sxs-lookup"><span data-stu-id="30450-104">Single voucher and currency revaluation upgrade</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="30450-105">一部の組織では、複数の顧客または仕入先がある単一伝票を含む仕訳帳を入力し、売掛金勘定または買掛金勘定の外貨再評価プロセスも実行します。</span><span class="sxs-lookup"><span data-stu-id="30450-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="30450-106">このトピックでは、これらの組織が Microsoft Dynamics 365 for Operations バージョン 1611 にアップグレードする際に従うべき手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="30450-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="30450-107">Microsoft Dynamics 365 for Operations バージョン 1611 にアップグレードする際には次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="30450-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="30450-108">Dynamics 365 for Operations にアップグレードする前に、売掛金勘定または買掛金勘定用の外貨再評価プロセスを実行します。</span><span class="sxs-lookup"><span data-stu-id="30450-108">Before you upgrade to Dynamics 365 for Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="30450-109">[**メソッド**] フィールドを **請求日** に設定します。</span><span class="sxs-lookup"><span data-stu-id="30450-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="30450-110">最後の外貨再評価を取り消す再評価トランザクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="30450-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="30450-111">したがって、未処理トランザクションは元の会計通貨で評価されます。</span><span class="sxs-lookup"><span data-stu-id="30450-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="30450-112">Dynamics 365 for Operations バージョン 1611 にアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="30450-112">Upgrade to Dynamics 365 for Operations version 1611.</span></span>
3.  <span data-ttu-id="30450-113">売掛金勘定および買掛金勘定の外貨再評価プロセスを再実行します。</span><span class="sxs-lookup"><span data-stu-id="30450-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="30450-114">今回は、[**メソッド**] フィールドを **標準** に設定します。</span><span class="sxs-lookup"><span data-stu-id="30450-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="30450-115">現在の為替レートに基づいた新しい再評価トランザクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="30450-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="30450-116">このトランザクションは、含み益 / 損失と正しい集計勘定科目を記録します。</span><span class="sxs-lookup"><span data-stu-id="30450-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>





