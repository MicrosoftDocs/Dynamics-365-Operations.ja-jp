---
title: グローバル在庫会計ホーム ページ
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management 用のグローバル在庫会計アドインのホーム ページについて解説します。
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f4434afb847104a18a2a2a2f07a7060cf01de816
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273183"
---
# <a name="global-inventory-accounting-home-page"></a><span data-ttu-id="2e5d5-103">グローバル在庫会計ホーム ページ</span><span class="sxs-lookup"><span data-stu-id="2e5d5-103">Global Inventory Accounting home page</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="2e5d5-104">国際的な組織は、当局からのローカルおよびグローバルの会計基準に準拠する必要性が高まっています。</span><span class="sxs-lookup"><span data-stu-id="2e5d5-104">International organizations are under increasing pressure from authorities to comply with local and global accounting standards.</span></span> <span data-ttu-id="2e5d5-105">在庫の評価は、コンプライアンスを保証する上で重要な役割を果たします。</span><span class="sxs-lookup"><span data-stu-id="2e5d5-105">The valuation of inventory plays a significant role in ensuring compliance.</span></span> <span data-ttu-id="2e5d5-106">Microsoft Dynamics 365 Supply Chain Management 用のグローバル在庫会計アドインは、組織 (特に国際的な組織) が複数の原価元帳を使用して在庫会計を行うことを可能にする包括的なソリューションを提供します。</span><span class="sxs-lookup"><span data-stu-id="2e5d5-106">The Global Inventory Accounting Add-in for Microsoft Dynamics 365 Supply Chain Management provides a comprehensive solution that enables organizations (especially international organizations) to use multiple costing ledgers to do inventory accounting.</span></span> <span data-ttu-id="2e5d5-107">したがって、それらの組織は複数の会計基準と内部管理会計とに同時に準拠できます。</span><span class="sxs-lookup"><span data-stu-id="2e5d5-107">Therefore, those organizations can comply with multiple accounting standards and internal management accounting at the same time.</span></span>

<span data-ttu-id="2e5d5-108">グローバル在庫会計により、適切な評価方法 (標準原価、平均、または特定の ID) と、選択した会計通貨をインスタンスごとに適用することによって、複数の表現で在庫を考慮することができます。</span><span class="sxs-lookup"><span data-stu-id="2e5d5-108">Global Inventory Accounting lets you account inventory in multiple representations by applying the appropriate valuation method (standard cost, average, or specific identification) and the selected accounting currency per instance.</span></span> <span data-ttu-id="2e5d5-109">グローバル在庫会計により、組織は多くの場合二重評価や二重通貨として参照される方法で、在庫明細書および補助元帳の値 (在庫残高および売却済商品の原価とも呼ばれます) を報告することができるようになります。</span><span class="sxs-lookup"><span data-stu-id="2e5d5-109">Global Inventory Accounting enables organizations to report inventory statements and subledger accounting values (also known as the inventory balance and the cost of goods sold) in what is often referred to as dual valuation and/or dual currency.</span></span>

<span data-ttu-id="2e5d5-110">在庫会計は個別の元帳で行われます。</span><span class="sxs-lookup"><span data-stu-id="2e5d5-110">Inventory accounting is done in individual ledgers.</span></span> <span data-ttu-id="2e5d5-111">必要に応じて、組織内の各法人に対して複数のグローバル在庫会計元帳を作成できます。</span><span class="sxs-lookup"><span data-stu-id="2e5d5-111">Several Global Inventory Accounting ledgers can be created for each legal entity in an organization, as required.</span></span> <span data-ttu-id="2e5d5-112">したがって、複数の在庫表現を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="2e5d5-112">Therefore, multiple inventory representations can be obtained.</span></span> <span data-ttu-id="2e5d5-113">法人内で転記されるドキュメントすべて (発注書、販売注文、移動オーダーなど) は、その法人に関連付けられているすべての原価元帳に計上されます。</span><span class="sxs-lookup"><span data-stu-id="2e5d5-113">All documents that are posted in a legal entity (such as purchase orders, sales orders, and transfer orders) will be accounted in all the costing ledgers that are associated with that legal entity.</span></span>

<span data-ttu-id="2e5d5-114">グローバル在庫会計元帳は、次の要素の組み合わせによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="2e5d5-114">A Global Inventory Accounting ledger is defined by a combination of the following elements:</span></span>

- <span data-ttu-id="2e5d5-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="2e5d5-115">Calendar</span></span>
- <span data-ttu-id="2e5d5-116">通貨</span><span class="sxs-lookup"><span data-stu-id="2e5d5-116">Currency</span></span>
- <span data-ttu-id="2e5d5-117">為替レート テーブル</span><span class="sxs-lookup"><span data-stu-id="2e5d5-117">Exchange rate table</span></span>
- <span data-ttu-id="2e5d5-118">規則</span><span class="sxs-lookup"><span data-stu-id="2e5d5-118">Convention</span></span>

<span data-ttu-id="2e5d5-119">規則は、1 つ以上の元帳に関連付けることができる在庫会計ポリシーのコレクションです。</span><span class="sxs-lookup"><span data-stu-id="2e5d5-119">A convention is a collection of inventory accounting policies that can be associated with one or more ledgers.</span></span> <span data-ttu-id="2e5d5-120">規則により、組織内で一連の共通のポリシーを共有できます。</span><span class="sxs-lookup"><span data-stu-id="2e5d5-120">Conventions let you share a common set of policies within your organization.</span></span>

## <a name="availability"></a><span data-ttu-id="2e5d5-121">適用の対象</span><span class="sxs-lookup"><span data-stu-id="2e5d5-121">Availability</span></span>

<span data-ttu-id="2e5d5-122">グローバル在庫会計は、現在、次の地理上の Azure リージョンで使用可能です。</span><span class="sxs-lookup"><span data-stu-id="2e5d5-122">Global Inventory Accounting is currently available in the following Azure geographic regions:</span></span>

- <span data-ttu-id="2e5d5-123">米国</span><span class="sxs-lookup"><span data-stu-id="2e5d5-123">United States</span></span>
- <span data-ttu-id="2e5d5-124">ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="2e5d5-124">Europe</span></span>
- <span data-ttu-id="2e5d5-125">英国</span><span class="sxs-lookup"><span data-stu-id="2e5d5-125">United Kingdom</span></span>
- <span data-ttu-id="2e5d5-126">オーストラリア</span><span class="sxs-lookup"><span data-stu-id="2e5d5-126">Australia</span></span>
- <span data-ttu-id="2e5d5-127">カナダ</span><span class="sxs-lookup"><span data-stu-id="2e5d5-127">Canada</span></span>

<span data-ttu-id="2e5d5-128">他の地域からのアドインをインストールしようとすると、Microsoft Dynamics Lifecycle Services (LCS) は、ユーザーの地理的な地域はサポートされていないというメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="2e5d5-128">If you try to install the add-in from another geographic region, Microsoft Dynamics Lifecycle Services (LCS) will show a message that your geographic region isn't supported.</span></span> <span data-ttu-id="2e5d5-129">グローバル在庫会計は、Supply Chain Management のオンプレミス配置をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="2e5d5-129">Global Inventory Accounting doesn't support on-premises deployments of Supply Chain Management.</span></span>

## <a name="licensing"></a><span data-ttu-id="2e5d5-130">ライセンス</span><span class="sxs-lookup"><span data-stu-id="2e5d5-130">Licensing</span></span>

<span data-ttu-id="2e5d5-131">グローバル在庫会計は、Supply Chain Management で使用可能な標準原価管理機能と共にライセンス供与されます。</span><span class="sxs-lookup"><span data-stu-id="2e5d5-131">Global Inventory Accounting is licensed together with the standard cost management features available for Supply Chain Management.</span></span> <span data-ttu-id="2e5d5-132">グローバル在庫会計を使用するのに、追加のライセンスを購入する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="2e5d5-132">You don't have to purchase an additional license to use Global Inventory Accounting.</span></span>
