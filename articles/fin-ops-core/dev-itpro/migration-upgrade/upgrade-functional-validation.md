---
title: AX 2012 からのアップグレード - 機能テスト パス
description: このトピックでは、機能テスト パスを実行して、アップグレードされた Finance and Operations 環境を検証する方法について説明します。
author: tariqbell
ms.date: 01/31/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: b6b717a0c46b5a2a32153ee8803081ea115b5e53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743903"
---
# <a name="upgrade-from-ax-2012---functional-test-passes"></a><span data-ttu-id="409d9-103">AX 2012 からのアップグレード - 機能テスト パス</span><span class="sxs-lookup"><span data-stu-id="409d9-103">Upgrade from AX 2012 - Functional test passes</span></span>

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

<span data-ttu-id="409d9-104">データのアップグレードが完了した後、すべての業務プロセスの完全な機能テスト パスを完了しておくことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="409d9-104">After data upgrade is completed, we recommend that you complete a full functional test pass of all business processes.</span></span> <span data-ttu-id="409d9-105">完全な機能テスト パスでは、Finance and Operations を使用して実行されるすべての業務プロセスの広範な再テストを実行します。</span><span class="sxs-lookup"><span data-stu-id="409d9-105">In a full functional test pass, you do an extensive retest of all business processes that are performed by using Finance and Operations.</span></span> <span data-ttu-id="409d9-106">テストには、Microsoft Dynamics AX 2012 から引き継がれたプロセスと Finance and Operations の機能を使用する新しいプロセスの両方を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="409d9-106">Tests should include both processes that have been brought forward from Microsoft Dynamics AX 2012 and new processes that use features from Finance and Operations.</span></span>

<span data-ttu-id="409d9-107">コードの品質によっては、バグ修正と再テストのために機能テスト パスを何回か繰り返さなければならない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="409d9-107">Depending on your code quality, bug remediation and retesting might require several iterations of the functional test pass.</span></span> <span data-ttu-id="409d9-108">バグが修正された後、関係するすべてのプロセスを再テストするために注意し、変更によって下流または上流プロセスが影響を受けないようにします。</span><span class="sxs-lookup"><span data-stu-id="409d9-108">After a bug is fixed, take care to retest all  processes that are involved, to make sure that no downstream or upstream processes are affected by the change.</span></span>

## <a name="old-data-vs-new-data"></a><span data-ttu-id="409d9-109">新しいデータ対古いデータ</span><span class="sxs-lookup"><span data-stu-id="409d9-109">Old data vs. new data</span></span>

<span data-ttu-id="409d9-110">実行するテストの一覧を作成するときは、新しいデータと対比して古いデータの影響を考慮します。</span><span class="sxs-lookup"><span data-stu-id="409d9-110">As you create a list of tests to perform, consider the impact of old data versus new data.</span></span> <span data-ttu-id="409d9-111">このタイプのテストは、データ関連のバグを発見するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="409d9-111">This type of testing will help you uncover data-related bugs.</span></span> <span data-ttu-id="409d9-112">古いデータと新しいデータを作成したコードは非常に異なっている可能性があります。この違いは、バグの共通の根本原因になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="409d9-112">The code that created the old and new data might be very different, and this difference can be a common root cause of bugs.</span></span>

<span data-ttu-id="409d9-113">たとえば、テストしている業務プロセスが発注書の取消である場合、新しいシステムにアップグレードされる前に開始された発注書を取消できますか。</span><span class="sxs-lookup"><span data-stu-id="409d9-113">For example, if the business process that you're testing is cancellation of a purchase order, can you cancel a purchase order that was started before it was upgraded to the new system?</span></span> <span data-ttu-id="409d9-114">新しいシステムへのアップグレード後に開始された発注書もキャンセルすることができますか。</span><span class="sxs-lookup"><span data-stu-id="409d9-114">Can you also cancel a purchase order that was started after the upgrade to the new system?</span></span> 

<span data-ttu-id="409d9-115">ここでは非常に単純な例を使用しましたが、システム内では多くのビジネス プロセスが連結していて、古いデータに対する新しいデータの効果が累積されるため、テスト要件がより複雑になることがあります。</span><span class="sxs-lookup"><span data-stu-id="409d9-115">We used a very simple example here, but the testing requirement can be more complex, because many business processes in the system are interconnected, and the effect of old data versus new data effect is cumulative.</span></span>

<span data-ttu-id="409d9-116">たとえば、生産テスト フローのステージを紹介します。</span><span class="sxs-lookup"><span data-stu-id="409d9-116">For example, here are the stages of a production test flow:</span></span>

1. <span data-ttu-id="409d9-117">品目マスターは設計され、法人にリリースされます。</span><span class="sxs-lookup"><span data-stu-id="409d9-117">The item master is designed and released to a legal entity.</span></span>
2. <span data-ttu-id="409d9-118">在庫品目要求が作成されます。</span><span class="sxs-lookup"><span data-stu-id="409d9-118">Item requirements are created.</span></span>
3. <span data-ttu-id="409d9-119">製造オーダーが生成されます。</span><span class="sxs-lookup"><span data-stu-id="409d9-119">Production orders are generated.</span></span>
4. <span data-ttu-id="409d9-120">発注書が生成されます。</span><span class="sxs-lookup"><span data-stu-id="409d9-120">Purchase orders are generated.</span></span>
5. <span data-ttu-id="409d9-121">製造オーダーの処理が発生します (作業現場)。</span><span class="sxs-lookup"><span data-stu-id="409d9-121">Production order processing  occurs (shop floor).</span></span>
6. <span data-ttu-id="409d9-122">仕入先支払 (発注書の支払) などが発生します。</span><span class="sxs-lookup"><span data-stu-id="409d9-122">Vendor payment (payment of purchase orders) occurs, and so on.</span></span>

<span data-ttu-id="409d9-123">この生産テスト フローでは、新しいレコードまたは古いレコードのいずれかを入力として使用することで各ステージを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="409d9-123">In this production test flow, each stage can be performed by using either new records or old records as input.</span></span> <span data-ttu-id="409d9-124">結果は、古いデータと新しいデータのすべての組み合わせをカバーする一連のテストです。</span><span class="sxs-lookup"><span data-stu-id="409d9-124">The result is a matrix of tests that covers every combination of old and new data.</span></span> <span data-ttu-id="409d9-125">いくつかのプロセスでは、テスト マトリックスは過剰に思われますし、実際に過剰である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="409d9-125">For some processes, test matrices might seem excessive, and they might actually be excessive in practice.</span></span> <span data-ttu-id="409d9-126">したがって、最も多く使用されると予測される特定の組み合わせに焦点を当てることができます。</span><span class="sxs-lookup"><span data-stu-id="409d9-126">Therefore, you can decide to focus on certain combinations that you predict will be used the most.</span></span> <span data-ttu-id="409d9-127">ただし、何に対応していないかを把握することも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="409d9-127">However, it's still helpful for you to know what you aren't covering.</span></span> <span data-ttu-id="409d9-128">所持しているもの、テストで最も焦点を当てるもの、焦点を当てないものを把握する場合に、連続した意思決定を行います。</span><span class="sxs-lookup"><span data-stu-id="409d9-128">Make a conscious decision, where you know what you have, what you’re going to focus most of the testing on, and what you’re not going to focus on.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]