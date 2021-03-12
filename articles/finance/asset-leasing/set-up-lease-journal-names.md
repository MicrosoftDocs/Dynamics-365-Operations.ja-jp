---
title: リース仕訳帳名の設定
description: このトピックでは、リース仕訳帳の名前を定義する方法について説明します。 リース仕訳帳の名前は、資産リースで発生したエントリが転記される仕訳帳を指定します。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 89c5fc768aafe9e5de9adcde32e7b4d0a084941b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990920"
---
# <a name="set-up-lease-journal-names"></a><span data-ttu-id="bd84f-104">リース仕訳帳名の設定</span><span class="sxs-lookup"><span data-stu-id="bd84f-104">Set up lease journal names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd84f-105">リース仕訳帳の名前は、資産リース トランザクションが転記される仕訳帳を指定します。</span><span class="sxs-lookup"><span data-stu-id="bd84f-105">Lease journal names specify the journals that Asset leasing transactions are posted to.</span></span> <span data-ttu-id="bd84f-106">**資産リース** 仕訳帳タイプに割り当てられている仕訳帳名のみが、**資産リース パラメーター** ページの **初期認識** フィールドと **月次仕訳帳名** フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="bd84f-106">Only journal names that are assigned to the **Asset leasing** journal type appear in the **Initial Recognition** and **Monthly Journal Name** fields on the **Asset leasing parameters** page.</span></span> <span data-ttu-id="bd84f-107">**請求仕訳帳名** フィールドに割り当てることができるのは、**仕入先請求書記録** 仕訳帳タイプだけです。</span><span class="sxs-lookup"><span data-stu-id="bd84f-107">Only **vendor invoice recording** journal type can be assigned to the **Invoice journal name** field.</span></span>

<span data-ttu-id="bd84f-108">リース仕訳帳の名前をコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="bd84f-108">To configure lease journal names, follow these steps.</span></span>

1. <span data-ttu-id="bd84f-109">**資産絵イース \> 設定 \> 資産リース パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bd84f-109">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="bd84f-110">**一般** タブの **初期認識仕訳帳名** フィールドで、仕訳帳を選択します。</span><span class="sxs-lookup"><span data-stu-id="bd84f-110">On the **General** tab, in the **Initial recognition journal name** field, and select a journal.</span></span> <span data-ttu-id="bd84f-111">すべての初期認識仕訳帳エントリは、この仕訳帳名に転記されます。</span><span class="sxs-lookup"><span data-stu-id="bd84f-111">All initial recognition journal entries will be posted to this journal name.</span></span>
3. <span data-ttu-id="bd84f-112">**請求書仕訳帳名** フィールドで、仕訳帳を選択します。</span><span class="sxs-lookup"><span data-stu-id="bd84f-112">In the **Invoice journal name** field, select a journal.</span></span> <span data-ttu-id="bd84f-113">**仕入先への支払** オプションがリース帳簿に対して **はい** に設定されている場合は、リースおよび経費の支払請求書がこの仕訳帳名に転記されます。</span><span class="sxs-lookup"><span data-stu-id="bd84f-113">If the **Pay to vendor** option is set to **Yes** for the lease book, lease and expense payment invoices will be posted to this journal name.</span></span>
4. <span data-ttu-id="bd84f-114">**リース仕訳帳名** フィールドで、仕訳帳を選択します。</span><span class="sxs-lookup"><span data-stu-id="bd84f-114">In the **Lease journal name** field, select a journal.</span></span> <span data-ttu-id="bd84f-115">すべての減価償却、利息、および短期再分類のエントリは、この仕訳帳名に転記されます。</span><span class="sxs-lookup"><span data-stu-id="bd84f-115">All depreciation, interest, and short-term reclassification entries will be posted to this journal name.</span></span> <span data-ttu-id="bd84f-116">**仕入先への支払** オプションがリース帳簿に対して **いいえ** に設定されている場合は、リース支払および経費エントリもこの仕訳帳名に転記されます。</span><span class="sxs-lookup"><span data-stu-id="bd84f-116">If the **Pay to vendor** option is set to **No** for the lease book, lease payments and expense payment entries will also be posted to this journal name.</span></span>
