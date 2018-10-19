---
title: "メソッドを拡張可能にする属性"
description: "このトピックでは、メソッドを拡張可能にする属性について説明します。"
author: MichaelFruergaardPontoppidan
manager: AnnBe
ms.date: 09/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: 
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2018-09-09
ms.dyn365.ops.version: Platform update 20
ms.translationtype: HT
ms.sourcegitcommit: ad0083018d2734cb1e36cbf5f94105376c57cdf9
ms.openlocfilehash: 95d830c8ab9ac340e60acbb38f3969c812f625d3
ms.contentlocale: ja-jp
ms.lasthandoff: 10/02/2018

---

# <a name="attributes-that-make-methods-extensible"></a><span data-ttu-id="66fc4-103">メソッドを拡張可能にする属性</span><span class="sxs-lookup"><span data-stu-id="66fc4-103">Attributes that make methods extensible</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66fc4-104">このトピックでは、メソッドの拡張性機能を制御するために使用できるさまざまな属性について説明します。</span><span class="sxs-lookup"><span data-stu-id="66fc4-104">This topic describes the various attributes that can be used to control extensibility capabilities for methods.</span></span>

<span data-ttu-id="66fc4-105">次の表は、メソッドの拡張性およびアクセシビリティの既定のサポートの概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="66fc4-105">The following table provides an overview of the default support for extensibility and accessibility on methods.</span></span> <span data-ttu-id="66fc4-106">さらに、メソッド シグネチャの変更に関するガイダンスも提供します。</span><span class="sxs-lookup"><span data-stu-id="66fc4-106">The table also provides guidance on the method signature changes.</span></span>

|   | <span data-ttu-id="66fc4-107">フック可能</span><span class="sxs-lookup"><span data-stu-id="66fc4-107">Hookable</span></span> | <span data-ttu-id="66fc4-108">折り返し可能</span><span class="sxs-lookup"><span data-stu-id="66fc4-108">Wrappable</span></span> | <span data-ttu-id="66fc4-109">置き換え可能</span><span class="sxs-lookup"><span data-stu-id="66fc4-109">Replaceable</span></span> | <span data-ttu-id="66fc4-110">ユーザー補助</span><span class="sxs-lookup"><span data-stu-id="66fc4-110">Accessibility</span></span> | <span data-ttu-id="66fc4-111">署名</span><span class="sxs-lookup"><span data-stu-id="66fc4-111">Signature</span></span> | 
|---|----------|-----------|-------------|---------------|-----------|
| <span data-ttu-id="66fc4-112">**プライベート**</span><span class="sxs-lookup"><span data-stu-id="66fc4-112">**private**</span></span> | <span data-ttu-id="66fc4-113">無</span><span class="sxs-lookup"><span data-stu-id="66fc4-113">No</span></span> | <span data-ttu-id="66fc4-114">該当なし</span><span class="sxs-lookup"><span data-stu-id="66fc4-114">N/A</span></span> | <span data-ttu-id="66fc4-115">該当なし</span><span class="sxs-lookup"><span data-stu-id="66fc4-115">N/A</span></span> | <span data-ttu-id="66fc4-116">定義されているクラス内からアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="66fc4-116">Accessible from within class it is defined in.</span></span> | <span data-ttu-id="66fc4-117">シグネチャは変更可能</span><span class="sxs-lookup"><span data-stu-id="66fc4-117">Signature can be changed</span></span> |
| <span data-ttu-id="66fc4-118">**保護された内部**</span><span class="sxs-lookup"><span data-stu-id="66fc4-118">**protected internal**</span></span> | <span data-ttu-id="66fc4-119">無</span><span class="sxs-lookup"><span data-stu-id="66fc4-119">No</span></span> | <span data-ttu-id="66fc4-120">有</span><span class="sxs-lookup"><span data-stu-id="66fc4-120">Yes</span></span> | <span data-ttu-id="66fc4-121">無</span><span class="sxs-lookup"><span data-stu-id="66fc4-121">No</span></span> | <span data-ttu-id="66fc4-122">定義されているクラスから、および同じモデル内の派生クラスからアクセス可能</span><span class="sxs-lookup"><span data-stu-id="66fc4-122">Accessible from with the class it is defined and from derived classes in the same model</span></span> | <span data-ttu-id="66fc4-123">シグネチャは変更可能</span><span class="sxs-lookup"><span data-stu-id="66fc4-123">Signature can be changed</span></span> |
| <span data-ttu-id="66fc4-124">**パブリック内部**</span><span class="sxs-lookup"><span data-stu-id="66fc4-124">**public internal**</span></span> | <span data-ttu-id="66fc4-125">有</span><span class="sxs-lookup"><span data-stu-id="66fc4-125">Yes</span></span> | <span data-ttu-id="66fc4-126">有</span><span class="sxs-lookup"><span data-stu-id="66fc4-126">Yes</span></span> | <span data-ttu-id="66fc4-127">無</span><span class="sxs-lookup"><span data-stu-id="66fc4-127">No</span></span> | <span data-ttu-id="66fc4-128">同じモデルでアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="66fc4-128">Accessible in the same model.</span></span> | <span data-ttu-id="66fc4-129">シグネチャは変更可能</span><span class="sxs-lookup"><span data-stu-id="66fc4-129">Signature can be changed</span></span> |
| <span data-ttu-id="66fc4-130">**保護**</span><span class="sxs-lookup"><span data-stu-id="66fc4-130">**protected**</span></span> | <span data-ttu-id="66fc4-131">無</span><span class="sxs-lookup"><span data-stu-id="66fc4-131">No</span></span> | <span data-ttu-id="66fc4-132">有</span><span class="sxs-lookup"><span data-stu-id="66fc4-132">Yes</span></span> | <span data-ttu-id="66fc4-133">無</span><span class="sxs-lookup"><span data-stu-id="66fc4-133">No</span></span> | <span data-ttu-id="66fc4-134">定義されているクラスから、および派生クラスからアクセス可能</span><span class="sxs-lookup"><span data-stu-id="66fc4-134">Accessible from with the class it is defined and from derived classes</span></span> | <span data-ttu-id="66fc4-135">シグネチャでは互換性が維持されている必要があります</span><span class="sxs-lookup"><span data-stu-id="66fc4-135">Signature must remain compatibled</span></span> |
| <span data-ttu-id="66fc4-136">**パブリック**</span><span class="sxs-lookup"><span data-stu-id="66fc4-136">**public**</span></span> | <span data-ttu-id="66fc4-137">有</span><span class="sxs-lookup"><span data-stu-id="66fc4-137">Yes</span></span> | <span data-ttu-id="66fc4-138">有</span><span class="sxs-lookup"><span data-stu-id="66fc4-138">Yes</span></span> | <span data-ttu-id="66fc4-139">無</span><span class="sxs-lookup"><span data-stu-id="66fc4-139">No</span></span> | <span data-ttu-id="66fc4-140">定義されたクラス、派生クラス、および定義するクラスにアクセスできるその他のクラスないからアクセス可能</span><span class="sxs-lookup"><span data-stu-id="66fc4-140">Accessible from within the class it is defined, derived classes, and other classes that have access to the defining class</span></span> | <span data-ttu-id="66fc4-141">シグネチャでは互換性が維持されている必要があります</span><span class="sxs-lookup"><span data-stu-id="66fc4-141">Signature must remain compatible</span></span> |

## <a name="hookable"></a><span data-ttu-id="66fc4-142">フック可能</span><span class="sxs-lookup"><span data-stu-id="66fc4-142">Hookable</span></span>
<span data-ttu-id="66fc4-143">メソッドがフック可能な場合、拡張担当者はプリイベントとポストイベントにサブスクライブできます。</span><span class="sxs-lookup"><span data-stu-id="66fc4-143">If a method is hookable, extenders can subscribe to pre-events and post-events.</span></span>

<span data-ttu-id="66fc4-144">パブリック メソッドの場合、メソッドに **\[Hookable(false)\]** を追加することでオプトアウトできます。</span><span class="sxs-lookup"><span data-stu-id="66fc4-144">For public methods, you can opt out by adding **\[Hookable(false)\]** to the method.</span></span>

<span data-ttu-id="66fc4-145">**\[Hookable(true)\]** をメソッドに追加して、プライベートおよび保護されたメソッドをオプトインできます。</span><span class="sxs-lookup"><span data-stu-id="66fc4-145">You can opt in for private and protected methods by adding **\[Hookable(true)\]** to the method.</span></span>

## <a name="final-keyword"></a><span data-ttu-id="66fc4-146">final キーワード</span><span class="sxs-lookup"><span data-stu-id="66fc4-146">Final keyword</span></span>
<span data-ttu-id="66fc4-147">**final** キーワードで実装されたメソッドは上書き不可、フック不可、折り返し不可です。</span><span class="sxs-lookup"><span data-stu-id="66fc4-147">Methods adorned with the **final** keyword can't be overridden, are not hookable, and are not wrappable.</span></span>

### <a name="best-practices-when-you-write-code"></a><span data-ttu-id="66fc4-148">コードの作成時のベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="66fc4-148">Best practices when you write code</span></span>
<span data-ttu-id="66fc4-149">メソッドがフック可能な場合、コンパイラは拡張ポイントでメソッドを有効にするために特別な中間言語 (IL) コードを生成します。</span><span class="sxs-lookup"><span data-stu-id="66fc4-149">When a method is hookable, the compiler generates extra intermediate language (IL) code to enable the method as an extension point.</span></span> <span data-ttu-id="66fc4-150">余分なコードにはパフォーマンスのオーバーヘッドがありますが、このオーバーヘッドはほとんどの場合は無視できます。</span><span class="sxs-lookup"><span data-stu-id="66fc4-150">Although the extra code has performance overhead, this overhead is negligible in most cases.</span></span> <span data-ttu-id="66fc4-151">ただし、パフォーマンスが重要なメソッドでは、フック不能としてメソッドをマーキングすることを検討してください。</span><span class="sxs-lookup"><span data-stu-id="66fc4-151">However, for performance-critical methods, consider marking the method as non-hookable.</span></span>

## <a name="wrappable"></a><span data-ttu-id="66fc4-152">折り返し可能</span><span class="sxs-lookup"><span data-stu-id="66fc4-152">Wrappable</span></span>
<span data-ttu-id="66fc4-153">メソッドが折り返し可能な場合は、拡張担当者はコマンド チェーン (CoC) を使用して折り返すことができます。</span><span class="sxs-lookup"><span data-stu-id="66fc4-153">If a method is wrappable, extenders can wrap it by using Chain of Command (CoC).</span></span> <span data-ttu-id="66fc4-154">拡張担当者は、CoC を中断することが許可されていないため、次を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="66fc4-154">Extenders must call next, because they aren't allowed to break the CoC.</span></span>

<span data-ttu-id="66fc4-155">折り返し可能にするには、メソッドもフック可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="66fc4-155">To be wrappable, a method must also be hookable.</span></span> <span data-ttu-id="66fc4-156">したがって、折り返し可能なメソッドはフック可能です。</span><span class="sxs-lookup"><span data-stu-id="66fc4-156">Therefore, methods that are wrappable are hookable.</span></span>

<span data-ttu-id="66fc4-157">保護されたパブリック メソッドの場合、メソッドに **\[Wrappable(false)\]** を追加することでオプトアウトできます。</span><span class="sxs-lookup"><span data-stu-id="66fc4-157">For protected and public methods, you can opt out by adding **\[Wrappable(false)\]** to the method.</span></span>

<span data-ttu-id="66fc4-158">プライベート メソッドをオプトインすることはできません。</span><span class="sxs-lookup"><span data-stu-id="66fc4-158">You can't opt in for private methods.</span></span>

### <a name="best-practices-when-you-write-code"></a><span data-ttu-id="66fc4-159">コードの作成時のベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="66fc4-159">Best practices when you write code</span></span>
<span data-ttu-id="66fc4-160">CoC は、さまざまな点で継承に似ています。</span><span class="sxs-lookup"><span data-stu-id="66fc4-160">CoC resembles inheritance in many ways.</span></span> <span data-ttu-id="66fc4-161">通常、他のユーザーが変更するのではなくメソッドを呼び出すことができるようにするには、最終としてメソッドをマークします。</span><span class="sxs-lookup"><span data-stu-id="66fc4-161">Typically, if you want other people to be able to call your method but not change it, you mark the method as final.</span></span> <span data-ttu-id="66fc4-162">これらのメソッドを折り返し不可またはフック不可としてマーキングすることを検討してください。</span><span class="sxs-lookup"><span data-stu-id="66fc4-162">Consider marking these methods as non-wrappable or non-hookable.</span></span>

## <a name="replaceable"></a><span data-ttu-id="66fc4-163">置き換え可能</span><span class="sxs-lookup"><span data-stu-id="66fc4-163">Replaceable</span></span> 
<span data-ttu-id="66fc4-164">メソッドが置き換え可能な場合は、拡張担当者は CoC を使用して折り返しできますが、無条件に次を呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="66fc4-164">If a method is replaceable, extenders can wrap it by using CoC, but they don't have to unconditionally call next.</span></span> <span data-ttu-id="66fc4-165">拡張担当者は CoC を中断できますが、条件がある場合のみ中断することが期待されます。</span><span class="sxs-lookup"><span data-stu-id="66fc4-165">Although extenders can break the CoC, the expectation is that they will only conditionally break it.</span></span> <span data-ttu-id="66fc4-166">コンパイラは、次の呼び出しを強制しません。</span><span class="sxs-lookup"><span data-stu-id="66fc4-166">The compiler doesn't enforce calls to next.</span></span>

<span data-ttu-id="66fc4-167">置き換え可能にするには、メソッドも折り返し可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="66fc4-167">To be replaceable, a method must also be wrappable.</span></span>

<span data-ttu-id="66fc4-168">折り返し可能なメソッドの場合、メソッドに **\[Replaceable\]** を追加することでオプトインできます。</span><span class="sxs-lookup"><span data-stu-id="66fc4-168">For wrappable methods, you can opt in by adding **\[Replaceable\]** to the method.</span></span>

### <a name="best-practices-when-you-write-code"></a><span data-ttu-id="66fc4-169">コードの作成時のベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="66fc4-169">Best practices when you write code</span></span>
<span data-ttu-id="66fc4-170">メソッドの置き換え可能な場合、CoC を使用して拡張することができ、次の実行をスキップできます。</span><span class="sxs-lookup"><span data-stu-id="66fc4-170">When a method is replaceable, it can be extended by using CoC, and the execution of next can be skipped.</span></span> <span data-ttu-id="66fc4-171">メソッドを置き換え可能にできるようにする前に、拡張担当者がメソッドの実行をスキップした場合の機能への影響を十分に評価する必要があります。</span><span class="sxs-lookup"><span data-stu-id="66fc4-171">Before you enable a method to be replaceable, you should thoroughly assess the functional impact if an extender skips the execution of the method.</span></span>
            
+ <span data-ttu-id="66fc4-172">**\[Replaceable\]** を持つメソッドに、メソッドの責任を説明する XML ドキュメントがあることを確認**します**。</span><span class="sxs-lookup"><span data-stu-id="66fc4-172">**Do** make sure that methods that have **\[Replaceable\]** have XML documentation that describes the responsibility of the method.</span></span>
+ <span data-ttu-id="66fc4-173">顧客が置き換えられたロジックをスキップして何もしないようにすうるには、**\[Replaceable\]** を使用**しません**。</span><span class="sxs-lookup"><span data-stu-id="66fc4-173">**Don't** use **\[Replaceable\]** to let consumers skip the replaced logic and do nothing.</span></span>
+ <span data-ttu-id="66fc4-174">**SysExtension** を代わりに使用可能な場合は、ファクトリ メソッドに **\[Replaceable\]** を使用**しません**。</span><span class="sxs-lookup"><span data-stu-id="66fc4-174">**Don't** use **\[Replaceable\]** for factory methods when **SysExtension** can be used instead.</span></span>
+ <span data-ttu-id="66fc4-175">メソッドがデータベースまたはクラスの状態を変更する場合、**\[Replaceable\]** の使用を**回避します**。</span><span class="sxs-lookup"><span data-stu-id="66fc4-175">**Avoid** using **\[Replaceable\]** when the method changes databases or class state.</span></span>
+ <span data-ttu-id="66fc4-176">メソッドが複数の工程を実行し、複数の責任を持つ場合、**\[Replaceable\]** の使用を**回避します**。</span><span class="sxs-lookup"><span data-stu-id="66fc4-176">**Avoid** using **\[Replaceable\]** if the method performs multiple operations and has multiple responsibilities.</span></span> <span data-ttu-id="66fc4-177">代わりに、それぞれが単一の責任を持つ別個のメソッドにメソッドをリファクタリングし、どのメソッドを実際に置き換え可能にする必要があるかを検討します。</span><span class="sxs-lookup"><span data-stu-id="66fc4-177">Instead, refactor the method into separate methods, each of which has a single responsibility, and consider which methods should actually be replaceable.</span></span>
+ <span data-ttu-id="66fc4-178">変換を解決するために、**\[Replaceable\]** の使用を**検討します**。</span><span class="sxs-lookup"><span data-stu-id="66fc4-178">**Consider** using **\[Replaceable\]** to solve transformations.</span></span> 

    <span data-ttu-id="66fc4-179">**例:** 既定のブロックがスローを持つ列挙値より切り替えステートメントを使う列挙変換。</span><span class="sxs-lookup"><span data-stu-id="66fc4-179">**Example:** Enum conversion that uses a switch statement over enum values, where the default block has a throw.</span></span>

+ <span data-ttu-id="66fc4-180">ルックアップと jumpref をオーバーライドするために **\[Replaceable\]** を使用することを**検討します**。</span><span class="sxs-lookup"><span data-stu-id="66fc4-180">**Consider** using **\[Replaceable\]** to override lookups and jumprefs.</span></span>
 
### <a name="best-practices-for-extenders"></a><span data-ttu-id="66fc4-181">拡張担当者のベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="66fc4-181">Best practices for extenders</span></span>
+ <span data-ttu-id="66fc4-182">置き換えるロジックとは異なる責任を持つロジックを記述し**ません**。</span><span class="sxs-lookup"><span data-stu-id="66fc4-182">**Don't** write logic that has a different responsibility than the logic that is being replaced.</span></span>
+ <span data-ttu-id="66fc4-183">置き換えロジックが適用されない場合、基本機能を呼び出し**ます** (次を呼び出し)。</span><span class="sxs-lookup"><span data-stu-id="66fc4-183">**Do** call the base functionality (call next) when the replacement logic doesn't apply.</span></span>
+ <span data-ttu-id="66fc4-184">基本機能 (次を呼び出し) を呼び出さずにロジックを完全に置き換えることを**回避します**。</span><span class="sxs-lookup"><span data-stu-id="66fc4-184">**Avoid** replacing logic completely by not calling the base functionality (call next).</span></span>

## <a name="using-the-attributes-in-conjunction-with-each-other"></a><span data-ttu-id="66fc4-185">互いに組み合わせた属性の使用</span><span class="sxs-lookup"><span data-stu-id="66fc4-185">Using the attributes in conjunction with each other</span></span>

<span data-ttu-id="66fc4-186">一般ルールは、\[Hookable\] は、\[Replaceable\] により要求される \[Wrappable\] により要求されます。</span><span class="sxs-lookup"><span data-stu-id="66fc4-186">The general rule is that \[Hookable\] is required by \[Wrappable\], which is required by \[Replaceable\].</span></span> <span data-ttu-id="66fc4-187">次の表では、依存関係の概要について説明します。</span><span class="sxs-lookup"><span data-stu-id="66fc4-187">The following table outlines the dependencies.</span></span>

|   | <span data-ttu-id="66fc4-188">フック可能</span><span class="sxs-lookup"><span data-stu-id="66fc4-188">Hookable</span></span> | <span data-ttu-id="66fc4-189">折り返し可能</span><span class="sxs-lookup"><span data-stu-id="66fc4-189">Wrappable</span></span> | <span data-ttu-id="66fc4-190">置き換え可能</span><span class="sxs-lookup"><span data-stu-id="66fc4-190">Replaceable</span></span> |
|---|----------|-----------|-------------|
| <span data-ttu-id="66fc4-191">**\[Hookable(true)\]**</span><span class="sxs-lookup"><span data-stu-id="66fc4-191">**\[Hookable(true)\]**</span></span> | <span data-ttu-id="66fc4-192">有</span><span class="sxs-lookup"><span data-stu-id="66fc4-192">Yes</span></span> | <span data-ttu-id="66fc4-193">無</span><span class="sxs-lookup"><span data-stu-id="66fc4-193">No</span></span> | <span data-ttu-id="66fc4-194">無</span><span class="sxs-lookup"><span data-stu-id="66fc4-194">No</span></span> |
| <span data-ttu-id="66fc4-195">**\[Hookable(false)\]**</span><span class="sxs-lookup"><span data-stu-id="66fc4-195">**\[Hookable(false)\]**</span></span> | <span data-ttu-id="66fc4-196">無</span><span class="sxs-lookup"><span data-stu-id="66fc4-196">No</span></span> | <span data-ttu-id="66fc4-197">無</span><span class="sxs-lookup"><span data-stu-id="66fc4-197">No</span></span> | <span data-ttu-id="66fc4-198">無</span><span class="sxs-lookup"><span data-stu-id="66fc4-198">No</span></span> |
| <span data-ttu-id="66fc4-199">**\[Wrappable(true)\]**</span><span class="sxs-lookup"><span data-stu-id="66fc4-199">**\[Wrappable(true)\]**</span></span> | <span data-ttu-id="66fc4-200">有</span><span class="sxs-lookup"><span data-stu-id="66fc4-200">Yes</span></span> | <span data-ttu-id="66fc4-201">有</span><span class="sxs-lookup"><span data-stu-id="66fc4-201">Yes</span></span> | <span data-ttu-id="66fc4-202">無</span><span class="sxs-lookup"><span data-stu-id="66fc4-202">No</span></span> |
| <span data-ttu-id="66fc4-203">**\[Wrappable(false)\]**</span><span class="sxs-lookup"><span data-stu-id="66fc4-203">**\[Wrappable(false)\]**</span></span> | <span data-ttu-id="66fc4-204">可能性あり。メソッドがフック可能であるかどうかによる (このトピックの表を参照)</span><span class="sxs-lookup"><span data-stu-id="66fc4-204">Maybe, depending on whether the method is hookable (see the table earlier in this topic)</span></span> | <span data-ttu-id="66fc4-205">無</span><span class="sxs-lookup"><span data-stu-id="66fc4-205">No</span></span> | <span data-ttu-id="66fc4-206">無</span><span class="sxs-lookup"><span data-stu-id="66fc4-206">No</span></span> |
| <span data-ttu-id="66fc4-207">**\[Replaceable(true)\]**</span><span class="sxs-lookup"><span data-stu-id="66fc4-207">**\[Replaceable(true)\]**</span></span> | <span data-ttu-id="66fc4-208">有</span><span class="sxs-lookup"><span data-stu-id="66fc4-208">Yes</span></span> | <span data-ttu-id="66fc4-209">有</span><span class="sxs-lookup"><span data-stu-id="66fc4-209">Yes</span></span> | <span data-ttu-id="66fc4-210">有</span><span class="sxs-lookup"><span data-stu-id="66fc4-210">Yes</span></span> |
| <span data-ttu-id="66fc4-211">**\[Replaceable(false)\]**</span><span class="sxs-lookup"><span data-stu-id="66fc4-211">**\[Replaceable(false)\]**</span></span> | <span data-ttu-id="66fc4-212">可能性あり。メソッドがフック可能であるかどうかによる (このトピックの表を参照)</span><span class="sxs-lookup"><span data-stu-id="66fc4-212">Maybe, depending on whether the method is hookable (see the table earlier in this topic)</span></span> | <span data-ttu-id="66fc4-213">可能性あり。メソッドが折り返し可能であるかどうかによる (このトピックの表を参照)</span><span class="sxs-lookup"><span data-stu-id="66fc4-213">Maybe, depending on whether the method is wrappable (see the table earlier in this topic)</span></span> | <span data-ttu-id="66fc4-214">無</span><span class="sxs-lookup"><span data-stu-id="66fc4-214">No</span></span> |



