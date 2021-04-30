---
title: リース仕訳帳名の設定
description: このトピックでは、リース仕訳帳の名前を定義する方法について説明します。 リース仕訳帳の名前は、資産リースで発生したエントリが転記される仕訳帳を指定します。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c139df124b249ec9dc5d16096e6f45f22d435456
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880889"
---
# <a name="set-up-lease-journal-names"></a><span data-ttu-id="83c68-104">リース仕訳帳名の設定</span><span class="sxs-lookup"><span data-stu-id="83c68-104">Set up lease journal names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83c68-105">リース仕訳帳の名前は、資産リース トランザクションが転記される仕訳帳を指定します。</span><span class="sxs-lookup"><span data-stu-id="83c68-105">Lease journal names specify the journals that Asset leasing transactions are posted to.</span></span> <span data-ttu-id="83c68-106">**資産リース** 仕訳帳タイプに割り当てられている仕訳帳名のみが、**資産リース パラメーター** ページの **初期認識** フィールドと **月次仕訳帳名** フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="83c68-106">Only journal names that are assigned to the **Asset leasing** journal type appear in the **Initial Recognition** and **Monthly Journal Name** fields on the **Asset leasing parameters** page.</span></span> <span data-ttu-id="83c68-107">**請求仕訳帳名** フィールドに割り当てることができるのは、**仕入先請求書記録** 仕訳帳タイプだけです。</span><span class="sxs-lookup"><span data-stu-id="83c68-107">Only **vendor invoice recording** journal type can be assigned to the **Invoice journal name** field.</span></span>

<span data-ttu-id="83c68-108">リース仕訳帳の名前をコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="83c68-108">To configure lease journal names, follow these steps.</span></span>

1. <span data-ttu-id="83c68-109">**資産絵イース \> 設定 \> 資産リース パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="83c68-109">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="83c68-110">**一般** タブの **初期認識仕訳帳名** フィールドで、仕訳帳を選択します。</span><span class="sxs-lookup"><span data-stu-id="83c68-110">On the **General** tab, in the **Initial recognition journal name** field, and select a journal.</span></span> <span data-ttu-id="83c68-111">すべての初期認識仕訳帳エントリは、この仕訳帳名に転記されます。</span><span class="sxs-lookup"><span data-stu-id="83c68-111">All initial recognition journal entries will be posted to this journal name.</span></span>
3. <span data-ttu-id="83c68-112">**請求書仕訳帳名** フィールドで、仕訳帳を選択します。</span><span class="sxs-lookup"><span data-stu-id="83c68-112">In the **Invoice journal name** field, select a journal.</span></span> <span data-ttu-id="83c68-113">**仕入先への支払** オプションがリース帳簿に対して **はい** に設定されている場合は、リースおよび経費の支払請求書がこの仕訳帳名に転記されます。</span><span class="sxs-lookup"><span data-stu-id="83c68-113">If the **Pay to vendor** option is set to **Yes** for the lease book, lease and expense payment invoices will be posted to this journal name.</span></span>
4. <span data-ttu-id="83c68-114">**リース仕訳帳名** フィールドで、仕訳帳を選択します。</span><span class="sxs-lookup"><span data-stu-id="83c68-114">In the **Lease journal name** field, select a journal.</span></span> <span data-ttu-id="83c68-115">すべての減価償却、利息、および短期再分類のエントリは、この仕訳帳名に転記されます。</span><span class="sxs-lookup"><span data-stu-id="83c68-115">All depreciation, interest, and short-term reclassification entries will be posted to this journal name.</span></span> <span data-ttu-id="83c68-116">**仕入先への支払** オプションがリース帳簿に対して **いいえ** に設定されている場合は、リース支払および経費エントリもこの仕訳帳名に転記されます。</span><span class="sxs-lookup"><span data-stu-id="83c68-116">If the **Pay to vendor** option is set to **No** for the lease book, lease payments and expense payment entries will also be posted to this journal name.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
