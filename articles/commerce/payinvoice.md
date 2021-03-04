---
title: 請求書の支払シナリオを設定する
description: このトピックでは、請求書の支払に関するさまざまなシナリオに対応できるように、Dynamics 365 Commerce を構成する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8b65fe3968698da1c5b76cf2d0ef706f3f1ec4bb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972660"
---
# <a name="set-up-pay-invoice-scenarios"></a><span data-ttu-id="36d25-103">請求書の支払シナリオを設定する</span><span class="sxs-lookup"><span data-stu-id="36d25-103">Set up pay invoice scenarios</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="36d25-104">Dynamics 365 Commerce の請求書の支払機能は拡張され、以下の機能がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="36d25-104">The Pay invoice functionality in Dynamics 365 Commerce has been expanded to support:</span></span>

- <span data-ttu-id="36d25-105">1 回の POS トランザクションでの複数の販売注文の請求書の支払。</span><span class="sxs-lookup"><span data-stu-id="36d25-105">Payoff of multiple sales order invoices in a single POS transaction.</span></span>
- <span data-ttu-id="36d25-106">自由書式の請求書、プロジェクト ベースの請求書、訂正表を含む、さまざまな種類の顧客請求書の支払。</span><span class="sxs-lookup"><span data-stu-id="36d25-106">Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</span></span>

<span data-ttu-id="36d25-107">これらのシナリオに対応するには、以下に説明するように、店舗用の機能プロファイルを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="36d25-107">To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</span></span>

1. <span data-ttu-id="36d25-108">**Retail と Commerce \> チャネル設定 \> POS の設定 \> POS プロファイル \> 機能プロファイル** の順にクリックし、変更する店舗にリンクされているプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="36d25-108">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles** and select a profile that's linked to the stores that you want to make the changes for.</span></span>
2. <span data-ttu-id="36d25-109">**機能** タブで、必要に応じて、以下のパラメーターを構成します。</span><span class="sxs-lookup"><span data-stu-id="36d25-109">On the **Functions** tab, configure the following parameters as needed.</span></span>

    - <span data-ttu-id="36d25-110">**販売注文請求書** – 単一の POS トランザクションで 1 つ以上の販売注文に基づく請求書の支払をユーザーが行えるようにするには、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="36d25-110">**Sales order invoice** – Select **Yes** to allow users to pay one or more sales order-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="36d25-111">**自由書式の請求書** – 単一の POS トランザクションで 1 つ以上の自由書式の請求書の支払をユーザーが行えるようにするには、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="36d25-111">**Free text invoice** – Select **Yes** to allow users to pay one or more free text-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="36d25-112">**プロジェクト請求書** – 単一の POS トランザクションで 1 つ以上のプロジェクト ベースの請求書の支払をユーザーが行えるようにするには、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="36d25-112">**Project invoice** – Select **Yes** to allow users to pay one or more project-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="36d25-113">**販売注文 - 訂正票** – 未処理の請求書に対する複数の販売注文ベースの訂正表の決済をユーザーができるようにする、または未処理の訂正表について顧客への払戻を処理できるようにするには、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="36d25-113">**Sales order credit note** – Select **Yes** to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</span></span>

> [!NOTE]
> <span data-ttu-id="36d25-114">金額の部分的な支払や決済は、まだサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="36d25-114">Payment or settlement of partial amounts is not yet supported.</span></span>
