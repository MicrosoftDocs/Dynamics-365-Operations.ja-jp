---
title: 単一の伝票に関するよく寄せられる質問
description: このトピックでは、単一の伝票の機能についてよく寄せられる質問に回答します。 財務仕訳帳の単一の伝票 (一般仕訳帳、固定資産仕訳帳、仕入先支払仕訳帳など) を使用して、単一の伝票のコンテキストで複数の補助元帳トランザクションを入力できます。
author: kweekley
manager: AnnBe
ms.date: 11/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerParameters, AssetProposalDepreciation
audience: Application User
ms.reviewer: roschlom
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 8.0.2
ms.openlocfilehash: 916f0172a2d7f9fad9dcd70b31f8ecf65e47b2c8
ms.sourcegitcommit: bd4763cc6088e114818e80bb1c27c6521b039743
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/02/2021
ms.locfileid: "5107752"
---
# <a name="one-voucher-faq"></a><span data-ttu-id="2ea9a-104">単一の伝票に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="2ea9a-104">One voucher FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ea9a-105">このトピックでは、単一の伝票の機能についてよく寄せられる質問に回答します。</span><span class="sxs-lookup"><span data-stu-id="2ea9a-105">This topic answers frequently asked questions about the One voucher functionality.</span></span> <span data-ttu-id="2ea9a-106">財務仕訳帳に対して単一の伝票を使用すると、単一の伝票に対して複数の小計トランザクションを入力できます。</span><span class="sxs-lookup"><span data-stu-id="2ea9a-106">One voucher for financial journals lets you enter multiple subledger transactions in the context of a single voucher.</span></span> <span data-ttu-id="2ea9a-107">その伝票に含めることができる仕訳は、一般仕訳、固定資産仕訳、ベンダー支払仕訳などがあります。</span><span class="sxs-lookup"><span data-stu-id="2ea9a-107">The journals that you can include in that voucher can be general journals, fixed asset journals, and vendor payment journals, among others.</span></span>

## <a name="when-will-the-one-voucher-functionality-be-deprecated"></a><span data-ttu-id="2ea9a-108">単一の伝票の機能が非推奨となる時期はいつでしょうか？</span><span class="sxs-lookup"><span data-stu-id="2ea9a-108">When will the One voucher functionality be deprecated?</span></span>

<span data-ttu-id="2ea9a-109">マイクロソフトでは、単一の伝票機能がいつ廃止されるかについては現時点で提供できませんが、廃止される少なくとも 2 年前にはお知らせします。</span><span class="sxs-lookup"><span data-stu-id="2ea9a-109">Although Microsoft can't provide an accurate estimate about when the One voucher functionality will be deprecated, it will likely be at least two years before the deprecation occurs.</span></span>

<span data-ttu-id="2ea9a-110">単一の伝票ドキュメントで説明されている通り、単一の伝票を使用した場合のみ、さまざまな業務要件を満たすることができます。</span><span class="sxs-lookup"><span data-stu-id="2ea9a-110">As is noted in the One voucher documentation, numerous business requirements can be met only by using One voucher.</span></span> <span data-ttu-id="2ea9a-111">マイクロソフトは、機能が廃止された後も、特定されたすべての業務要件をシステムで満たすことができるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ea9a-111">Microsoft must ensure that all the identified business requirements can still be met in the system after the functionality is deprecated.</span></span> <span data-ttu-id="2ea9a-112">したがって、機能のギャップを埋めるには新しい機能を追加が必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="2ea9a-112">Therefore, new features will probably have to be added to fill functional gaps.</span></span>

<span data-ttu-id="2ea9a-113">すべての機能のギャップを解消した後は、この機能を廃止する予定です。</span><span class="sxs-lookup"><span data-stu-id="2ea9a-113">After all functional gaps are filled, Microsoft will communicate that the feature will be deprecated.</span></span> <span data-ttu-id="2ea9a-114">解消後の少なくとも1年間は非推奨とはならない予定です。</span><span class="sxs-lookup"><span data-stu-id="2ea9a-114">However, the deprecation won't be effective for least one year after that communication.</span></span>

<span data-ttu-id="2ea9a-115">詳細については、[単一の伝票に関するドキュメント](one-voucher.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ea9a-115">For more information, see the [One voucher documentation](one-voucher.md).</span></span>

## <a name="what-will-the-solution-that-replaces-one-voucher-look-like"></a><span data-ttu-id="2ea9a-116">単一の伝票の代替機能はどのようなものになりますか？</span><span class="sxs-lookup"><span data-stu-id="2ea9a-116">What will the solution that replaces One voucher look like?</span></span>

<span data-ttu-id="2ea9a-117">マイクロソフトは、それぞれの機能のギャップが異なり、業務要件に基づいて評価する必要があるため、具体的なソリューションを提供できません。</span><span class="sxs-lookup"><span data-stu-id="2ea9a-117">Microsoft can't provide a specific solution, because each feature gap is different and must be evaluated based on the business requirements.</span></span> <span data-ttu-id="2ea9a-118">機能的なギャップの中には、特定の業務要件を満たす際に役立つ機能に置き換えられる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2ea9a-118">Some functional gaps will likely be replaced with features that help meet specific business requirements.</span></span> <span data-ttu-id="2ea9a-119">しかし、単一の伝票を利用した場合のように、仕訳帳への入力を可能にしつつ、必要に応じてより詳細に追跡できるようにシステムを強化することで、他のギャップを解消できるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="2ea9a-119">However, other gaps might be filled by continuing to allow for entry in a journal, as when One voucher is used, but enhancing the system to track more detail as required.</span></span>

## <a name="where-can-i-track-the-progress-of-the-feature-gaps-being-filled"></a><span data-ttu-id="2ea9a-120">機能のギャップを埋める進捗状況はどこで確認できますか？</span><span class="sxs-lookup"><span data-stu-id="2ea9a-120">Where can I track the progress of the feature gaps being filled?</span></span>

<span data-ttu-id="2ea9a-121">すべての新機能については、リリース計画および "新機能または変更点" のドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ea9a-121">As for every new feature, customers must watch the Release plan and "What's new or changed" documentation.</span></span> <span data-ttu-id="2ea9a-122">各機能はこれらのドキュメントに追加され、その機能が以前に単一の伝票機能を必要としていた業務要件を満たすために必要な機能が示されます。</span><span class="sxs-lookup"><span data-stu-id="2ea9a-122">Each feature will be added to these documents, and a note will indicate that the feature is required to meet a business requirement that previously required the One voucher functionality.</span></span>

## <a name="when-the-deprecation-date-is-identified-where-will-it-be-communicated"></a><span data-ttu-id="2ea9a-123">廃止予定日が決定した場合、その日付はどこで告知されるますか？</span><span class="sxs-lookup"><span data-stu-id="2ea9a-123">When the deprecation date is identified, where will it be communicated?</span></span>

<span data-ttu-id="2ea9a-124">単一の伝票の非推奨化は、広く拡散すべき大きな変更点です。</span><span class="sxs-lookup"><span data-stu-id="2ea9a-124">The deprecation of One voucher is a significant change that will be widely communicated.</span></span> <span data-ttu-id="2ea9a-125">これは、製品ドキュメント、ブログ記事、および該当するマイクロソフトの主催するカンファレンスでの発表を通じて、非推奨となる日付けよりも先立って通知されます。</span><span class="sxs-lookup"><span data-stu-id="2ea9a-125">It will be communicated through the product documentation, a blog post, and announcements at applicable Microsoft conferences, well in advance of the date when the deprecation takes effect.</span></span>
