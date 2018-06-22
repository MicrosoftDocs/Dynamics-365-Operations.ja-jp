---
title: "AX 2012 からのアップグレード - Go-Live の準備"
description: "このトピックでは、ソース AX 2012 システムとアップグレード プロセスの安定した状態を保ち、運用の一貫性を保証する方法について説明します。"
author: tariqbell
manager: AnnBe
ms.date: 01/31/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 4f1c1dfc7f177d026eb1fd9af873f7aeb4de7087
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="upgrade-from-ax-2012---prepare-for-go-live"></a><span data-ttu-id="8f823-103">AX 2012 からのアップグレード - Go-Live の準備</span><span class="sxs-lookup"><span data-stu-id="8f823-103">Upgrade from AX 2012 - Prepare for go-live</span></span>

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

<span data-ttu-id="8f823-104">稼動日が近づくにつれ、一連の手順を実装しソース Microsoft Dynamics AX 2012 システムとアップグレード プロセスが安定した状態を保ち運用の一貫性があることを保証することが重要です。</span><span class="sxs-lookup"><span data-stu-id="8f823-104">As the go-live date approaches, it's important that you implement this series of steps to help guarantee that the source Microsoft Dynamics AX 2012 system and the upgrade process both remain stable and consistent for go-live.</span></span>

<span data-ttu-id="8f823-105">このプロセスの一環として、最終的な切替テストを実行する前にコード変更やアプリケーションの設定の変更をすべてロック ダウンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f823-105">As part of this process, you must lock down any further code changes or application setup changes before you run the final cutover test.</span></span>

## <a name="code-freeze"></a><span data-ttu-id="8f823-106">コード凍結</span><span class="sxs-lookup"><span data-stu-id="8f823-106">Code freeze</span></span>

<span data-ttu-id="8f823-107">AX 2012 環境のすべてのコード変更を凍結する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f823-107">All code changes in the AX 2012 environment should be frozen.</span></span> <span data-ttu-id="8f823-108">AX 2012 で発生する重大な問題を処理するためにエスカレーション プロセスを実装します。</span><span class="sxs-lookup"><span data-stu-id="8f823-108">Implement an escalation process to handle any critical issues that appear in AX 2012.</span></span> <span data-ttu-id="8f823-109">既定では、必要な新しいコード変更は AX 2012 環境ではなく、新しいシステムでのみ実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f823-109">By default, any new code changes that are required should be implemented only in the new system, not in the AX 2012 environment.</span></span> <span data-ttu-id="8f823-110">AX 2012 環境での提案されたコードの変更の実装は、管理レベルで説明する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f823-110">Implementation of proposed code changes in the AX 2012 environment should be discussed at the management level.</span></span> <span data-ttu-id="8f823-111">AX 2012 でコードを変更した場合、同じ変更は、新しいシステムで行われる必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f823-111">If a code change is made in AX 2012, the same change must be made in the new system.</span></span> <span data-ttu-id="8f823-112">その場合、切替テストと機能テストをもう 1 回繰り返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f823-112">In that case, another iteration of cutover testing and functional testing might be required.</span></span>

## <a name="application-configuration-freeze"></a><span data-ttu-id="8f823-113">アプリケーション コンフィギュレーションの凍結</span><span class="sxs-lookup"><span data-stu-id="8f823-113">Application configuration freeze</span></span>

<span data-ttu-id="8f823-114">これらの変更は、新しいシステムの動作やデータアップグレード スクリプトの動作に影響を与える可能性があるため、すべてのアプリケーション構成の変更を AX 2012 環境で固定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f823-114">All application configuration changes should be frozen in the AX 2012 environment, because these changes could affect how the new system behaves or how the data upgrade scripts behave.</span></span> <span data-ttu-id="8f823-115">コンフィギュレーションの変更は、システム機能のコンフィギュレーションに関連する AX 2012 アプリケーションの変更です。</span><span class="sxs-lookup"><span data-stu-id="8f823-115">Configuration changes are changes in the AX 2012 application that are related to the configuration of system functionality.</span></span> <span data-ttu-id="8f823-116">これらの変更を凍結することで、データのアップグレード プロセスの安定性を保証します。</span><span class="sxs-lookup"><span data-stu-id="8f823-116">By freezing these changes, you help guarantee the stability of the data upgrade process.</span></span>

<span data-ttu-id="8f823-117">構成の変更は通常、AX 2012 または信頼済スーパー ユーザーの小規模なグループによって制御されるため、セキュリティ アクセスを変更して凍結を実行することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="8f823-117">Because configuration changes are typically controlled by the AX 2012 system administrator or a small group of trusted super users, we don't recommend that you enforce the freeze by changing security access.</span></span> <span data-ttu-id="8f823-118">代わりに、それらのユーザーに伝達される業務プロセスを通じて凍結を実装します。</span><span class="sxs-lookup"><span data-stu-id="8f823-118">Instead, implement the freeze through a business process that is communicated to those users.</span></span> <span data-ttu-id="8f823-119">セキュリティ アクセスの変更には、コード変更 (ロール定義自体の変更) または構成変更 (ユーザーの再割り当て) が必要な場合があり、これらの変更がアップグレード プロセスに影響する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8f823-119">Changes to security access might require a code change (changes to the role definitions themselves) or a configuration change (reassignment of users), and these changes could affect the upgrade process.</span></span>

## <a name="running-the-final-cutover-test"></a><span data-ttu-id="8f823-120">最終の切替テストの実行</span><span class="sxs-lookup"><span data-stu-id="8f823-120">Running the final cutover test</span></span>

<span data-ttu-id="8f823-121">その後のコードまたは設定の変更がない場合は、すべてのデータとコードの更新タスクが期待どおりに実行されることを確認するために、最終的な切替テストを実行します。</span><span class="sxs-lookup"><span data-stu-id="8f823-121">After no further code or setup changes will occur, run a final cutover test to make sure that all data and code upgrade tasks still run as expected.</span></span>

> [!NOTE]
> <span data-ttu-id="8f823-122">データ自体が毎日変更されるため、コードを凍結して、アップグレード プロジェクトの開始時の変更をセットアップする場合でも、このステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f823-122">You must complete this step even if you freeze code and setup changes at the beginning of the upgrade project, because the data itself changes every day.</span></span> <span data-ttu-id="8f823-123">また、この最終的な切替テストは、現在のデータが正常にアップグレードされたことを検証します。</span><span class="sxs-lookup"><span data-stu-id="8f823-123">This final cutover test also validates that the current data is upgraded successfully.</span></span>

<span data-ttu-id="8f823-124">機能テストがこの最後にアップグレードしたコピーに対して実行されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8f823-124">Make sure that functional testing is performed against this last upgraded copy.</span></span>

<span data-ttu-id="8f823-125">この時点のアップグレード プロジェクトにおいて、検出されたバグを分類することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8f823-125">At this point in the upgrade project, we recommend that you categorize any bugs that are found:</span></span>
- <span data-ttu-id="8f823-126">**ブロック** - このタイプのすべてのバグが修正されるまで、アップグレード プロジェクトは進められません。</span><span class="sxs-lookup"><span data-stu-id="8f823-126">**Blocking** – The upgrade project can't proceed until every bug of this type is fixed.</span></span> <span data-ttu-id="8f823-127">アップグレードは延期する必要があり、バグが修復され、切替テストが再度実行された後にのみ進めることができます。</span><span class="sxs-lookup"><span data-stu-id="8f823-127">The upgrade must be postponed, and can proceed only after the bug is remediated and the cutover test is run again.</span></span> <span data-ttu-id="8f823-128">バグをブロックとして分類するには、これらの条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f823-128">For a bug to be classified as blocking, it must meet these conditions:</span></span>

    - <span data-ttu-id="8f823-129">これにより、重要な業務プロセスが完了されないようにします。</span><span class="sxs-lookup"><span data-stu-id="8f823-129">It prevents a critical business process from being completed.</span></span>
    - <span data-ttu-id="8f823-130">それに対して利用できる対応策または軽減はありません。</span><span class="sxs-lookup"><span data-stu-id="8f823-130">No workaround or mitigation is available for it.</span></span>

- <span data-ttu-id="8f823-131">**ブロックなし** – アップグレード プロジェクトを進めることができます。</span><span class="sxs-lookup"><span data-stu-id="8f823-131">**Non-blocking** – The upgrade project can proceed.</span></span> <span data-ttu-id="8f823-132">このタイプのバグは、アップグレードされたシステムで修正できます。</span><span class="sxs-lookup"><span data-stu-id="8f823-132">Bugs of this type can be fixed in the upgraded system.</span></span>

