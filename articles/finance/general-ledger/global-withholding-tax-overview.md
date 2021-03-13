---
title: グローバル源泉徴収税
description: このトピックでは、グローバルな源泉徴収税機能とこの設定方法に関する情報を提供します。 グローバル源泉徴収税の機能は、仕入先トランザクションと顧客トランザクションに対して機能強化されており、源泉徴収税が品目レベルで計算されます。
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 17ed1dcae97f6cd28175c483be5ca3ce96d59e05
ms.sourcegitcommit: 053f4cda6862fbcd9e3aa6e9cb009e7de833beac
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/28/2021
ms.locfileid: "5075741"
---
# <a name="global-withholding-tax"></a><span data-ttu-id="e041c-104">グローバル源泉徴収税</span><span class="sxs-lookup"><span data-stu-id="e041c-104">Global withholding tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e041c-105">このトピックでは、グローバルな源泉徴収税機能とこの設定方法について解説します。</span><span class="sxs-lookup"><span data-stu-id="e041c-105">This topic provides information about global withholding tax functionality and explains how to set it up.</span></span> <span data-ttu-id="e041c-106">この機能は、 バージョン 10.0.17 またはそれ以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="e041c-106">The new functionality is available in version 10.0.17 and later.</span></span>

<span data-ttu-id="e041c-107">グローバル源泉徴収税の機能は、仕入先トランザクションと顧客トランザクションに対して機能強化されており、源泉徴収税が品目レベルで計算されます。</span><span class="sxs-lookup"><span data-stu-id="e041c-107">Global withholding tax functionality is enhanced for vendor and customer transactions, so that withholding tax is calculated at the item level.</span></span> <span data-ttu-id="e041c-108">購入取引による源泉徴収票の残高は、源泉徴収票の決済口座に対して源泉徴収票決済のジョブを実行することで決済できます。</span><span class="sxs-lookup"><span data-stu-id="e041c-108">The balance in the withholding tax account from purchase transactions can be settled by running the withholding tax payment job against the withholding tax settlement account.</span></span>

> [!NOTE]
> <span data-ttu-id="e041c-109">グローバル源泉徴収税では、発注書、仕入先請求書、および販売注文ページの **請求金額の管理** 機能はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e041c-109">Global withholding tax doesn't support the **Maintain charges** function on the purchase order, vendor invoice, and sales order pages.</span></span>

## <a name="turn-on-global-withholding-tax"></a><span data-ttu-id="e041c-110">グローバル源泉徴収税の有効化</span><span class="sxs-lookup"><span data-stu-id="e041c-110">Turn on global withholding tax</span></span>

1. <span data-ttu-id="e041c-111">**機能の管理** ワークスペースで、一覧から **フローバル源泉徴収税** 機能を選択し、**すぐに有効化する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e041c-111">In the **Feature management** workspace, select **Global withholding tax**, and then select **Enable now**.</span></span>
2. <span data-ttu-id="e041c-112">**税 \> 設定 \> パラメータ \> 総勘定元帳のパラメータ** に移動し、**源泉徴収税** タブで、**グローバル源泉徴収税を有効にする** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e041c-112">Go to **Tax \> Setup \> Parameters \> General ledger parameters**, and then, on the **Withholding tax** tab, set the **Enable global withholding tax** option to **Yes**.</span></span>
3. <span data-ttu-id="e041c-113">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e041c-113">Select **Save**.</span></span>
4. <span data-ttu-id="e041c-114">Web ブラウザーのページを更新します。</span><span class="sxs-lookup"><span data-stu-id="e041c-114">Refresh the page in your web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="e041c-115">ローカライズされた源泉徴収税ソリューションが既に存在する国/地域では、グローバル源泉徴収税の機能を有効にできません。</span><span class="sxs-lookup"><span data-stu-id="e041c-115">Global withholding tax functionality can’t be turned on for countries/regions where localized withholding tax solutions already exist.</span></span> <span data-ttu-id="e041c-116">この領域には、インド、ブラジル、タイ、サウジアラビア、アイルランド、英国、米国が含まれますが、これに限定されないものとします。</span><span class="sxs-lookup"><span data-stu-id="e041c-116">These areas include but are not restricted to India, Brazil, Thailand, Saudi Arabia, Ireland, Great Britain and the United States.</span></span>
