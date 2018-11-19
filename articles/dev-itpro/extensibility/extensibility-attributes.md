---
title: "メソッドを拡張可能にする属性"
description: "このトピックでは、メソッドを拡張可能にする属性について説明します。"
author: MichaelFruergaardPontoppidan
manager: AnnBe
ms.date: 11/01/2018
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
ms.sourcegitcommit: 6514e32b100ea0169d98629fee09afaa66129217
ms.openlocfilehash: aa86766f0d1eb1f1c077fd2354cc8b35328b7cd5
ms.contentlocale: ja-jp
ms.lasthandoff: 11/01/2018

---

# <a name="attributes-that-make-methods-extensible"></a><span data-ttu-id="e8879-103">メソッドを拡張可能にする属性</span><span class="sxs-lookup"><span data-stu-id="e8879-103">Attributes that make methods extensible</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e8879-104">このトピックでは、メソッドの拡張性機能を制御するために使用できるさまざまな属性について説明します。</span><span class="sxs-lookup"><span data-stu-id="e8879-104">This topic describes the various attributes that can be used to control extensibility capabilities for methods.</span></span>

<span data-ttu-id="e8879-105">次の表は、メソッドの拡張性およびアクセシビリティの既定のサポートの概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="e8879-105">The following table provides an overview of the default support for extensibility and accessibility on methods.</span></span> <span data-ttu-id="e8879-106">さらに、メソッド シグネチャの変更に関するガイダンスも提供します。</span><span class="sxs-lookup"><span data-stu-id="e8879-106">The table also provides guidance on the method signature changes.</span></span>

|   | <span data-ttu-id="e8879-107">フック可能</span><span class="sxs-lookup"><span data-stu-id="e8879-107">Hookable</span></span> | <span data-ttu-id="e8879-108">折り返し可能</span><span class="sxs-lookup"><span data-stu-id="e8879-108">Wrappable</span></span> | <span data-ttu-id="e8879-109">置き換え可能</span><span class="sxs-lookup"><span data-stu-id="e8879-109">Replaceable</span></span> | <span data-ttu-id="e8879-110">ユーザー補助</span><span class="sxs-lookup"><span data-stu-id="e8879-110">Accessibility</span></span> | <span data-ttu-id="e8879-111">署名</span><span class="sxs-lookup"><span data-stu-id="e8879-111">Signature</span></span> | 
|---|----------|-----------|-------------|---------------|-----------|
| <span data-ttu-id="e8879-112">**プライベート**</span><span class="sxs-lookup"><span data-stu-id="e8879-112">**private**</span></span> | <span data-ttu-id="e8879-113">無</span><span class="sxs-lookup"><span data-stu-id="e8879-113">No</span></span> | <span data-ttu-id="e8879-114">該当なし</span><span class="sxs-lookup"><span data-stu-id="e8879-114">N/A</span></span> | <span data-ttu-id="e8879-115">該当なし</span><span class="sxs-lookup"><span data-stu-id="e8879-115">N/A</span></span> | <span data-ttu-id="e8879-116">定義されているクラス内からアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e8879-116">Accessible from within class it is defined in.</span></span> | <span data-ttu-id="e8879-117">シグネチャは変更可能</span><span class="sxs-lookup"><span data-stu-id="e8879-117">Signature can be changed</span></span> |
| <span data-ttu-id="e8879-118">**保護された内部**</span><span class="sxs-lookup"><span data-stu-id="e8879-118">**protected internal**</span></span> | <span data-ttu-id="e8879-119">無</span><span class="sxs-lookup"><span data-stu-id="e8879-119">No</span></span> | <span data-ttu-id="e8879-120">無</span><span class="sxs-lookup"><span data-stu-id="e8879-120">No</span></span> | <span data-ttu-id="e8879-121">無</span><span class="sxs-lookup"><span data-stu-id="e8879-121">No</span></span> | <span data-ttu-id="e8879-122">定義されているクラスから、および同じモデル内の派生クラスからアクセス可能</span><span class="sxs-lookup"><span data-stu-id="e8879-122">Accessible from with the class it is defined and from derived classes in the same model</span></span> | <span data-ttu-id="e8879-123">シグネチャは変更可能</span><span class="sxs-lookup"><span data-stu-id="e8879-123">Signature can be changed</span></span> |
| <span data-ttu-id="e8879-124">**内部**</span><span class="sxs-lookup"><span data-stu-id="e8879-124">**internal**</span></span> | <span data-ttu-id="e8879-125">無</span><span class="sxs-lookup"><span data-stu-id="e8879-125">No</span></span> | <span data-ttu-id="e8879-126">無</span><span class="sxs-lookup"><span data-stu-id="e8879-126">No</span></span> | <span data-ttu-id="e8879-127">無</span><span class="sxs-lookup"><span data-stu-id="e8879-127">No</span></span> | <span data-ttu-id="e8879-128">同じモデルでアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e8879-128">Accessible in the same model.</span></span> | <span data-ttu-id="e8879-129">シグネチャは変更可能</span><span class="sxs-lookup"><span data-stu-id="e8879-129">Signature can be changed</span></span> |
| <span data-ttu-id="e8879-130">**保護**</span><span class="sxs-lookup"><span data-stu-id="e8879-130">**protected**</span></span> | <span data-ttu-id="e8879-131">無</span><span class="sxs-lookup"><span data-stu-id="e8879-131">No</span></span> | <span data-ttu-id="e8879-132">有</span><span class="sxs-lookup"><span data-stu-id="e8879-132">Yes</span></span> | <span data-ttu-id="e8879-133">無</span><span class="sxs-lookup"><span data-stu-id="e8879-133">No</span></span> | <span data-ttu-id="e8879-134">定義されているクラスから、および派生クラスからアクセス可能</span><span class="sxs-lookup"><span data-stu-id="e8879-134">Accessible from with the class it is defined and from derived classes</span></span> | <span data-ttu-id="e8879-135">シグネチャでは互換性が維持されている必要があります</span><span class="sxs-lookup"><span data-stu-id="e8879-135">Signature must remain compatible</span></span> |
| <span data-ttu-id="e8879-136">**パブリック**</span><span class="sxs-lookup"><span data-stu-id="e8879-136">**public**</span></span> | <span data-ttu-id="e8879-137">有</span><span class="sxs-lookup"><span data-stu-id="e8879-137">Yes</span></span> | <span data-ttu-id="e8879-138">有</span><span class="sxs-lookup"><span data-stu-id="e8879-138">Yes</span></span> | <span data-ttu-id="e8879-139">無</span><span class="sxs-lookup"><span data-stu-id="e8879-139">No</span></span> | <span data-ttu-id="e8879-140">定義されたクラス、派生クラス、および定義するクラスにアクセスできるその他のクラスないからアクセス可能</span><span class="sxs-lookup"><span data-stu-id="e8879-140">Accessible from within the class it is defined, derived classes, and other classes that have access to the defining class</span></span> | <span data-ttu-id="e8879-141">シグネチャでは互換性が維持されている必要があります</span><span class="sxs-lookup"><span data-stu-id="e8879-141">Signature must remain compatible</span></span> |

## <a name="hookable"></a><span data-ttu-id="e8879-142">フック可能</span><span class="sxs-lookup"><span data-stu-id="e8879-142">Hookable</span></span>
<span data-ttu-id="e8879-143">メソッドがフック可能な場合、拡張担当者はプリイベントとポストイベントにサブスクライブできます。</span><span class="sxs-lookup"><span data-stu-id="e8879-143">If a method is hookable, extenders can subscribe to pre-events and post-events.</span></span>

<span data-ttu-id="e8879-144">パブリック メソッドの場合、メソッドに **\[Hookable(false)\]** を追加することでオプトアウトできます。</span><span class="sxs-lookup"><span data-stu-id="e8879-144">For public methods, you can opt out by adding **\[Hookable(false)\]** to the method.</span></span>

<span data-ttu-id="e8879-145">**\[Hookable(true)\]** をメソッドに追加して、プライベートおよび保護されたメソッドをオプトインできます。</span><span class="sxs-lookup"><span data-stu-id="e8879-145">You can opt in for private and protected methods by adding **\[Hookable(true)\]** to the method.</span></span>

<span data-ttu-id="e8879-146">メソッドが明示的に **\[Hookable(false)\]** とマークされている場合、折り返しはできません。</span><span class="sxs-lookup"><span data-stu-id="e8879-146">If a method is explicitly marked as **\[Hookable(false)\]**, then it is not wrappable.</span></span>

## <a name="final-keyword"></a><span data-ttu-id="e8879-147">final キーワード</span><span class="sxs-lookup"><span data-stu-id="e8879-147">Final keyword</span></span>
<span data-ttu-id="e8879-148">**final** キーワードで実装されたメソッドは上書き不可、フック不可、折り返し不可です。</span><span class="sxs-lookup"><span data-stu-id="e8879-148">Methods adorned with the **final** keyword can't be overridden, are not hookable, and are not wrappable.</span></span>

### <a name="best-practices-when-you-write-code"></a><span data-ttu-id="e8879-149">コードの作成時のベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="e8879-149">Best practices when you write code</span></span>
<span data-ttu-id="e8879-150">メソッドがフック可能な場合、コンパイラは拡張ポイントでメソッドを有効にするために特別な中間言語 (IL) コードを生成します。</span><span class="sxs-lookup"><span data-stu-id="e8879-150">When a method is hookable, the compiler generates extra intermediate language (IL) code to enable the method as an extension point.</span></span> <span data-ttu-id="e8879-151">余分なコードにはパフォーマンスのオーバーヘッドがありますが、このオーバーヘッドはほとんどの場合は無視できます。</span><span class="sxs-lookup"><span data-stu-id="e8879-151">Although the extra code has performance overhead, this overhead is negligible in most cases.</span></span> <span data-ttu-id="e8879-152">ただし、パフォーマンスが重要なメソッドでは、フック不能としてメソッドをマーキングすることを検討してください。</span><span class="sxs-lookup"><span data-stu-id="e8879-152">However, for performance-critical methods, consider marking the method as non-hookable.</span></span>

## <a name="wrappable"></a><span data-ttu-id="e8879-153">折り返し可能</span><span class="sxs-lookup"><span data-stu-id="e8879-153">Wrappable</span></span>
<span data-ttu-id="e8879-154">メソッドが折り返し可能な場合は、拡張担当者はコマンド チェーン (CoC) を使用して折り返すことができます。</span><span class="sxs-lookup"><span data-stu-id="e8879-154">If a method is wrappable, extenders can wrap it by using Chain of Command (CoC).</span></span> <span data-ttu-id="e8879-155">拡張担当者は、CoC を中断することが許可されていないため、次を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8879-155">Extenders must call next, because they aren't allowed to break the CoC.</span></span>

<span data-ttu-id="e8879-156">保護されたパブリック メソッドの場合、メソッドに **\[Wrappable(false)\]** を追加することでオプトアウトできます。</span><span class="sxs-lookup"><span data-stu-id="e8879-156">For protected and public methods, you can opt out by adding **\[Wrappable(false)\]** to the method.</span></span>

<span data-ttu-id="e8879-157">プライベート メソッドをオプトインすることはできません。</span><span class="sxs-lookup"><span data-stu-id="e8879-157">You can't opt in for private methods.</span></span>

### <a name="best-practices-when-you-write-code"></a><span data-ttu-id="e8879-158">コードの作成時のベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="e8879-158">Best practices when you write code</span></span>
<span data-ttu-id="e8879-159">CoC は、さまざまな点で継承に似ています。</span><span class="sxs-lookup"><span data-stu-id="e8879-159">CoC resembles inheritance in many ways.</span></span> <span data-ttu-id="e8879-160">通常、他のユーザーが変更するのではなくメソッドを呼び出すことができるようにするには、最終としてメソッドをマークします。</span><span class="sxs-lookup"><span data-stu-id="e8879-160">Typically, if you want other people to be able to call your method but not change it, you mark the method as final.</span></span> <span data-ttu-id="e8879-161">これらのメソッドを折り返し不可またはフック不可としてマーキングすることを検討してください。</span><span class="sxs-lookup"><span data-stu-id="e8879-161">Consider marking these methods as non-wrappable or non-hookable.</span></span>

## <a name="replaceable"></a><span data-ttu-id="e8879-162">置き換え可能</span><span class="sxs-lookup"><span data-stu-id="e8879-162">Replaceable</span></span> 
<span data-ttu-id="e8879-163">メソッドが置き換え可能な場合は、拡張担当者は CoC を使用して折り返しできますが、無条件に次を呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e8879-163">If a method is replaceable, extenders can wrap it by using CoC, but they don't have to unconditionally call next.</span></span> <span data-ttu-id="e8879-164">拡張担当者は CoC を中断できますが、条件がある場合のみ中断することが期待されます。</span><span class="sxs-lookup"><span data-stu-id="e8879-164">Although extenders can break the CoC, the expectation is that they will only conditionally break it.</span></span> <span data-ttu-id="e8879-165">コンパイラは、次の呼び出しを強制しません。</span><span class="sxs-lookup"><span data-stu-id="e8879-165">The compiler doesn't enforce calls to next.</span></span>

<span data-ttu-id="e8879-166">置き換え可能にするには、メソッドも折り返し可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8879-166">To be replaceable, a method must also be wrappable.</span></span>

<span data-ttu-id="e8879-167">折り返し可能なメソッドの場合、メソッドに **\[Replaceable\]** を追加することでオプトインできます。</span><span class="sxs-lookup"><span data-stu-id="e8879-167">For wrappable methods, you can opt in by adding **\[Replaceable\]** to the method.</span></span>

### <a name="best-practices-when-you-write-code"></a><span data-ttu-id="e8879-168">コードの作成時のベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="e8879-168">Best practices when you write code</span></span>
<span data-ttu-id="e8879-169">メソッドの置き換え可能な場合、CoC を使用して拡張することができ、次の実行をスキップできます。</span><span class="sxs-lookup"><span data-stu-id="e8879-169">When a method is replaceable, it can be extended by using CoC, and the execution of next can be skipped.</span></span> <span data-ttu-id="e8879-170">メソッドを置き換え可能にできるようにする前に、拡張担当者がメソッドの実行をスキップした場合の機能への影響を十分に評価する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8879-170">Before you enable a method to be replaceable, you should thoroughly assess the functional impact if an extender skips the execution of the method.</span></span>
            
+ <span data-ttu-id="e8879-171">**\[Replaceable\]** を持つメソッドに、メソッドの責任を説明する XML ドキュメントがあることを確認**します**。</span><span class="sxs-lookup"><span data-stu-id="e8879-171">**Do** make sure that methods that have **\[Replaceable\]** have XML documentation that describes the responsibility of the method.</span></span>
+ <span data-ttu-id="e8879-172">顧客が置き換えられたロジックをスキップして何もしないようにすうるには、**\[Replaceable\]** を使用**しません**。</span><span class="sxs-lookup"><span data-stu-id="e8879-172">**Don't** use **\[Replaceable\]** to let consumers skip the replaced logic and do nothing.</span></span>
+ <span data-ttu-id="e8879-173">**SysExtension** を代わりに使用可能な場合は、ファクトリ メソッドに **\[Replaceable\]** を使用**しません**。</span><span class="sxs-lookup"><span data-stu-id="e8879-173">**Don't** use **\[Replaceable\]** for factory methods when **SysExtension** can be used instead.</span></span>
+ <span data-ttu-id="e8879-174">メソッドがデータベースまたはクラスの状態を変更する場合、**\[Replaceable\]** の使用を**回避します**。</span><span class="sxs-lookup"><span data-stu-id="e8879-174">**Avoid** using **\[Replaceable\]** when the method changes databases or class state.</span></span>
+ <span data-ttu-id="e8879-175">メソッドが複数の工程を実行し、複数の責任を持つ場合、**\[Replaceable\]** の使用を**回避します**。</span><span class="sxs-lookup"><span data-stu-id="e8879-175">**Avoid** using **\[Replaceable\]** if the method performs multiple operations and has multiple responsibilities.</span></span> <span data-ttu-id="e8879-176">代わりに、それぞれが単一の責任を持つ別個のメソッドにメソッドをリファクタリングし、どのメソッドを実際に置き換え可能にする必要があるかを検討します。</span><span class="sxs-lookup"><span data-stu-id="e8879-176">Instead, refactor the method into separate methods, each of which has a single responsibility, and consider which methods should actually be replaceable.</span></span>
+ <span data-ttu-id="e8879-177">変換を解決するために、**\[Replaceable\]** の使用を**検討します**。</span><span class="sxs-lookup"><span data-stu-id="e8879-177">**Consider** using **\[Replaceable\]** to solve transformations.</span></span> 

    <span data-ttu-id="e8879-178">**例:** 既定のブロックがスローを持つ列挙値より切り替えステートメントを使う列挙変換。</span><span class="sxs-lookup"><span data-stu-id="e8879-178">**Example:** Enum conversion that uses a switch statement over enum values, where the default block has a throw.</span></span>

+ <span data-ttu-id="e8879-179">ルックアップと jumpref をオーバーライドするために **\[Replaceable\]** を使用することを**検討します**。</span><span class="sxs-lookup"><span data-stu-id="e8879-179">**Consider** using **\[Replaceable\]** to override lookups and jumprefs.</span></span>
 
### <a name="best-practices-for-extenders"></a><span data-ttu-id="e8879-180">拡張担当者のベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="e8879-180">Best practices for extenders</span></span>
+ <span data-ttu-id="e8879-181">置き換えるロジックとは異なる責任を持つロジックを記述し**ません**。</span><span class="sxs-lookup"><span data-stu-id="e8879-181">**Don't** write logic that has a different responsibility than the logic that is being replaced.</span></span>
+ <span data-ttu-id="e8879-182">置き換えロジックが適用されない場合、基本機能を呼び出し**ます** (次を呼び出し)。</span><span class="sxs-lookup"><span data-stu-id="e8879-182">**Do** call the base functionality (call next) when the replacement logic doesn't apply.</span></span>
+ <span data-ttu-id="e8879-183">基本機能 (次を呼び出し) を呼び出さずにロジックを完全に置き換えることを**回避します**。</span><span class="sxs-lookup"><span data-stu-id="e8879-183">**Avoid** replacing logic completely by not calling the base functionality (call next).</span></span>

