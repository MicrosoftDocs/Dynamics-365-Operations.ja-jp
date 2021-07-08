---
title: メソッドを拡張可能にする属性
description: このトピックでは、メソッドを拡張可能にする属性について説明します。
author: MichaelFruergaardPontoppidan
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2018-09-09
ms.dyn365.ops.version: Platform update 20
ms.openlocfilehash: 705c6e16dde82771dadffcf9c057a1713fda5d14
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193632"
---
# <a name="attributes-that-make-methods-extensible"></a><span data-ttu-id="d575a-103">メソッドを拡張可能にする属性</span><span class="sxs-lookup"><span data-stu-id="d575a-103">Attributes that make methods extensible</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d575a-104">このトピックでは、メソッドの拡張性機能を制御するために使用できるさまざまな属性について説明します。</span><span class="sxs-lookup"><span data-stu-id="d575a-104">This topic describes the various attributes that can be used to control extensibility capabilities for methods.</span></span>

<span data-ttu-id="d575a-105">次の表は、メソッドの拡張性およびアクセシビリティの既定のサポートの概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="d575a-105">The following table provides an overview of the default support for extensibility and accessibility on methods.</span></span> <span data-ttu-id="d575a-106">さらに、メソッド シグネチャの変更に関するガイダンスも提供します。</span><span class="sxs-lookup"><span data-stu-id="d575a-106">The table also provides guidance on the method signature changes.</span></span>

| <span data-ttu-id="d575a-107">属性</span><span class="sxs-lookup"><span data-stu-id="d575a-107">Attribute</span></span>  | <span data-ttu-id="d575a-108">フック可能</span><span class="sxs-lookup"><span data-stu-id="d575a-108">Hookable</span></span> | <span data-ttu-id="d575a-109">折り返し可能</span><span class="sxs-lookup"><span data-stu-id="d575a-109">Wrappable</span></span> | <span data-ttu-id="d575a-110">置き換え可能</span><span class="sxs-lookup"><span data-stu-id="d575a-110">Replaceable</span></span> | <span data-ttu-id="d575a-111">アクセシビリティ</span><span class="sxs-lookup"><span data-stu-id="d575a-111">Accessibility</span></span> | <span data-ttu-id="d575a-112">署名</span><span class="sxs-lookup"><span data-stu-id="d575a-112">Signature</span></span> | 
|---|----------|-----------|-------------|---------------|-----------|
| <span data-ttu-id="d575a-113">**プライベート**</span><span class="sxs-lookup"><span data-stu-id="d575a-113">**private**</span></span> | <span data-ttu-id="d575a-114">無</span><span class="sxs-lookup"><span data-stu-id="d575a-114">No</span></span> | <span data-ttu-id="d575a-115">該当なし</span><span class="sxs-lookup"><span data-stu-id="d575a-115">N/A</span></span> | <span data-ttu-id="d575a-116">該当なし</span><span class="sxs-lookup"><span data-stu-id="d575a-116">N/A</span></span> | <span data-ttu-id="d575a-117">定義されているクラス内からアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="d575a-117">Accessible from within class it is defined in.</span></span> | <span data-ttu-id="d575a-118">シグネチャは変更可能</span><span class="sxs-lookup"><span data-stu-id="d575a-118">Signature can be changed</span></span> |
| <span data-ttu-id="d575a-119">**保護された内部**</span><span class="sxs-lookup"><span data-stu-id="d575a-119">**protected internal**</span></span> | <span data-ttu-id="d575a-120">いいえ</span><span class="sxs-lookup"><span data-stu-id="d575a-120">No</span></span> | <span data-ttu-id="d575a-121">はい。プラットフォーム更新 25 以降から</span><span class="sxs-lookup"><span data-stu-id="d575a-121">Yes, from Platform update 25 onward</span></span> | <span data-ttu-id="d575a-122">いいえ</span><span class="sxs-lookup"><span data-stu-id="d575a-122">No</span></span> | <span data-ttu-id="d575a-123">定義されているクラスから、および同じモデル内の派生クラスからアクセス可能です。</span><span class="sxs-lookup"><span data-stu-id="d575a-123">Accessible from with the class it is defined, from derived classes, and from classes in the same model.</span></span> | <span data-ttu-id="d575a-124">シグネチャでは互換性が維持されている必要があります</span><span class="sxs-lookup"><span data-stu-id="d575a-124">Signature must remain compatible</span></span> |
| <span data-ttu-id="d575a-125">**内部**</span><span class="sxs-lookup"><span data-stu-id="d575a-125">**internal**</span></span> | <span data-ttu-id="d575a-126">無</span><span class="sxs-lookup"><span data-stu-id="d575a-126">No</span></span> | <span data-ttu-id="d575a-127">無</span><span class="sxs-lookup"><span data-stu-id="d575a-127">No</span></span> | <span data-ttu-id="d575a-128">無</span><span class="sxs-lookup"><span data-stu-id="d575a-128">No</span></span> | <span data-ttu-id="d575a-129">同じモデルでアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="d575a-129">Accessible in the same model.</span></span> | <span data-ttu-id="d575a-130">シグネチャは変更可能</span><span class="sxs-lookup"><span data-stu-id="d575a-130">Signature can be changed</span></span> |
| <span data-ttu-id="d575a-131">**保護**</span><span class="sxs-lookup"><span data-stu-id="d575a-131">**protected**</span></span> | <span data-ttu-id="d575a-132">いいえ</span><span class="sxs-lookup"><span data-stu-id="d575a-132">No</span></span> | <span data-ttu-id="d575a-133">はい。最終とマークされている場合以外</span><span class="sxs-lookup"><span data-stu-id="d575a-133">Yes, unless marked final</span></span> | <span data-ttu-id="d575a-134">いいえ</span><span class="sxs-lookup"><span data-stu-id="d575a-134">No</span></span> | <span data-ttu-id="d575a-135">定義されているクラスから、および派生クラスからアクセス可能です。</span><span class="sxs-lookup"><span data-stu-id="d575a-135">Accessible from with the class it is defined and from derived classes.</span></span> | <span data-ttu-id="d575a-136">シグネチャでは互換性が維持されている必要があります</span><span class="sxs-lookup"><span data-stu-id="d575a-136">Signature must remain compatible</span></span> |
| <span data-ttu-id="d575a-137">**パブリック**</span><span class="sxs-lookup"><span data-stu-id="d575a-137">**public**</span></span> | <span data-ttu-id="d575a-138">はい</span><span class="sxs-lookup"><span data-stu-id="d575a-138">Yes</span></span> | <span data-ttu-id="d575a-139">はい。最終とマークされている場合以外</span><span class="sxs-lookup"><span data-stu-id="d575a-139">Yes, unless marked final</span></span> | <span data-ttu-id="d575a-140">いいえ</span><span class="sxs-lookup"><span data-stu-id="d575a-140">No</span></span> | <span data-ttu-id="d575a-141">定義されたクラス、派生クラス、および定義するクラスにアクセスできるその他のクラスからアクセス可能です。</span><span class="sxs-lookup"><span data-stu-id="d575a-141">Accessible from within the class it is defined, derived classes, and other classes that have access to the defining class.</span></span> | <span data-ttu-id="d575a-142">シグネチャでは互換性が維持されている必要があります</span><span class="sxs-lookup"><span data-stu-id="d575a-142">Signature must remain compatible</span></span> |

## <a name="hookable"></a><span data-ttu-id="d575a-143">フック可能</span><span class="sxs-lookup"><span data-stu-id="d575a-143">Hookable</span></span>
<span data-ttu-id="d575a-144">メソッドがフック可能な場合、拡張担当者はプリイベントとポストイベントにサブスクライブできます。</span><span class="sxs-lookup"><span data-stu-id="d575a-144">If a method is hookable, extenders can subscribe to pre-events and post-events.</span></span>

<span data-ttu-id="d575a-145">パブリック メソッドの場合、メソッドに **\[Hookable(false)\]** を追加することでオプトアウトできます。</span><span class="sxs-lookup"><span data-stu-id="d575a-145">For public methods, you can opt out by adding **\[Hookable(false)\]** to the method.</span></span>

<span data-ttu-id="d575a-146">**\[Hookable(true)\]** をメソッドに追加して、プライベートおよび保護されたメソッドをオプトインできます。</span><span class="sxs-lookup"><span data-stu-id="d575a-146">You can opt in for private and protected methods by adding **\[Hookable(true)\]** to the method.</span></span>

<span data-ttu-id="d575a-147">メソッドが明示的に **\[Hookable(false)\]** とマークされている場合、折り返しはできません。</span><span class="sxs-lookup"><span data-stu-id="d575a-147">If a method is explicitly marked as **\[Hookable(false)\]**, then it is not wrappable.</span></span>

### <a name="best-practices-when-you-write-code"></a><span data-ttu-id="d575a-148">コードの作成時のベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="d575a-148">Best practices when you write code</span></span>
<span data-ttu-id="d575a-149">メソッドがフック可能な場合、コンパイラは拡張ポイントでメソッドを有効にするために特別な中間言語 (IL) コードを生成します。</span><span class="sxs-lookup"><span data-stu-id="d575a-149">When a method is hookable, the compiler generates extra intermediate language (IL) code to enable the method as an extension point.</span></span> <span data-ttu-id="d575a-150">余分なコードにはパフォーマンスのオーバーヘッドがありますが、このオーバーヘッドはほとんどの場合は無視できます。</span><span class="sxs-lookup"><span data-stu-id="d575a-150">Although the extra code has performance overhead, this overhead is negligible in most cases.</span></span> <span data-ttu-id="d575a-151">ただし、パフォーマンスが重要なメソッドでは、フック不能としてメソッドをマーキングすることを検討してください。</span><span class="sxs-lookup"><span data-stu-id="d575a-151">However, for performance-critical methods, consider marking the method as non-hookable.</span></span>

## <a name="wrappable"></a><span data-ttu-id="d575a-152">折り返し可能</span><span class="sxs-lookup"><span data-stu-id="d575a-152">Wrappable</span></span>
<span data-ttu-id="d575a-153">メソッドが折り返し可能な場合は、拡張担当者はコマンド チェーン (CoC) を使用して折り返すことができます。</span><span class="sxs-lookup"><span data-stu-id="d575a-153">If a method is wrappable, extenders can wrap it by using Chain of Command (CoC).</span></span> <span data-ttu-id="d575a-154">拡張担当者は、CoC を中断することが許可されていないため、次を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d575a-154">Extenders must call next, because they aren't allowed to break the CoC.</span></span>

<span data-ttu-id="d575a-155">保護されたパブリック メソッドの場合、メソッドに **\[Wrappable(false)\]** を追加することでオプトアウトできます。</span><span class="sxs-lookup"><span data-stu-id="d575a-155">For protected and public methods, you can opt out by adding **\[Wrappable(false)\]** to the method.</span></span>

<span data-ttu-id="d575a-156">プライベート メソッドをオプトインすることはできません。</span><span class="sxs-lookup"><span data-stu-id="d575a-156">You can't opt in for private methods.</span></span>

### <a name="best-practices-when-you-write-code"></a><span data-ttu-id="d575a-157">コードの作成時のベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="d575a-157">Best practices when you write code</span></span>
<span data-ttu-id="d575a-158">CoC は、さまざまな点で継承に似ています。</span><span class="sxs-lookup"><span data-stu-id="d575a-158">CoC resembles inheritance in many ways.</span></span> <span data-ttu-id="d575a-159">通常、他のユーザーが変更するのではなくメソッドを呼び出すことができるようにするには、最終としてメソッドをマークします。</span><span class="sxs-lookup"><span data-stu-id="d575a-159">Typically, if you want other people to be able to call your method but not change it, you mark the method as final.</span></span> <span data-ttu-id="d575a-160">これらのメソッドを折り返し不可またはフック不可としてマーキングすることを検討してください。</span><span class="sxs-lookup"><span data-stu-id="d575a-160">Consider marking these methods as non-wrappable or non-hookable.</span></span>

## <a name="replaceable"></a><span data-ttu-id="d575a-161">置き換え可能</span><span class="sxs-lookup"><span data-stu-id="d575a-161">Replaceable</span></span> 
<span data-ttu-id="d575a-162">メソッドが置き換え可能な場合は、拡張担当者は CoC を使用して折り返しできますが、無条件に次を呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d575a-162">If a method is replaceable, extenders can wrap it by using CoC, but they don't have to unconditionally call next.</span></span> <span data-ttu-id="d575a-163">拡張担当者は CoC を中断できますが、条件がある場合のみ中断することが期待されます。</span><span class="sxs-lookup"><span data-stu-id="d575a-163">Although extenders can break the CoC, the expectation is that they will only conditionally break it.</span></span> <span data-ttu-id="d575a-164">コンパイラは、次の呼び出しを強制しません。</span><span class="sxs-lookup"><span data-stu-id="d575a-164">The compiler doesn't enforce calls to next.</span></span>

<span data-ttu-id="d575a-165">置き換え可能にするには、メソッドも折り返し可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="d575a-165">To be replaceable, a method must also be wrappable.</span></span>

<span data-ttu-id="d575a-166">折り返し可能なメソッドの場合、メソッドに **\[Replaceable\]** を追加することでオプトインできます。</span><span class="sxs-lookup"><span data-stu-id="d575a-166">For wrappable methods, you can opt in by adding **\[Replaceable\]** to the method.</span></span>

### <a name="best-practices-when-you-write-code"></a><span data-ttu-id="d575a-167">コードの作成時のベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="d575a-167">Best practices when you write code</span></span>
<span data-ttu-id="d575a-168">メソッドの置き換え可能な場合、CoC を使用して拡張することができ、次の実行をスキップできます。</span><span class="sxs-lookup"><span data-stu-id="d575a-168">When a method is replaceable, it can be extended by using CoC, and the execution of next can be skipped.</span></span> <span data-ttu-id="d575a-169">メソッドを置き換え可能にできるようにする前に、拡張担当者がメソッドの実行をスキップした場合の機能への影響を十分に評価する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d575a-169">Before you enable a method to be replaceable, you should thoroughly assess the functional impact if an extender skips the execution of the method.</span></span>
            
+ <span data-ttu-id="d575a-170">**\[Replaceable\]** を持つメソッドに、メソッドの責任を説明する XML ドキュメントがあることを確認 **します**。</span><span class="sxs-lookup"><span data-stu-id="d575a-170">**Do** make sure that methods that have **\[Replaceable\]** have XML documentation that describes the responsibility of the method.</span></span>
+ <span data-ttu-id="d575a-171">顧客が置き換えられたロジックをスキップして何もしないようにすうるには、**\[Replaceable\]** を使用 **しません**。</span><span class="sxs-lookup"><span data-stu-id="d575a-171">**Don't** use **\[Replaceable\]** to let consumers skip the replaced logic and do nothing.</span></span>
+ <span data-ttu-id="d575a-172">**SysExtension** を代わりに使用可能な場合は、ファクトリ メソッドに **\[Replaceable\]** を使用 **しません**。</span><span class="sxs-lookup"><span data-stu-id="d575a-172">**Don't** use **\[Replaceable\]** for factory methods when **SysExtension** can be used instead.</span></span>
+ <span data-ttu-id="d575a-173">メソッドがデータベースまたはクラスの状態を変更する場合、**\[Replaceable\]** の使用を **回避します**。</span><span class="sxs-lookup"><span data-stu-id="d575a-173">**Avoid** using **\[Replaceable\]** when the method changes databases or class state.</span></span>
+ <span data-ttu-id="d575a-174">メソッドが複数の工程を実行し、複数の責任を持つ場合、**\[Replaceable\]** の使用を **回避します**。</span><span class="sxs-lookup"><span data-stu-id="d575a-174">**Avoid** using **\[Replaceable\]** if the method performs multiple operations and has multiple responsibilities.</span></span> <span data-ttu-id="d575a-175">代わりに、それぞれが単一の責任を持つ別個のメソッドにメソッドをリファクタリングし、どのメソッドを実際に置き換え可能にする必要があるかを検討します。</span><span class="sxs-lookup"><span data-stu-id="d575a-175">Instead, refactor the method into separate methods, each of which has a single responsibility, and consider which methods should actually be replaceable.</span></span>
+ <span data-ttu-id="d575a-176">変換を解決するために、**\[Replaceable\]** の使用を **検討します**。</span><span class="sxs-lookup"><span data-stu-id="d575a-176">**Consider** using **\[Replaceable\]** to solve transformations.</span></span> 

    <span data-ttu-id="d575a-177">**例:** 既定のブロックがスローを持つ列挙値より切り替えステートメントを使う列挙変換。</span><span class="sxs-lookup"><span data-stu-id="d575a-177">**Example:** Enum conversion that uses a switch statement over enum values, where the default block has a throw.</span></span>

+ <span data-ttu-id="d575a-178">ルックアップと jumpref をオーバーライドするために **\[Replaceable\]** を使用することを **検討します**。</span><span class="sxs-lookup"><span data-stu-id="d575a-178">**Consider** using **\[Replaceable\]** to override lookups and jumprefs.</span></span>
 
### <a name="best-practices-for-extenders"></a><span data-ttu-id="d575a-179">拡張担当者のベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="d575a-179">Best practices for extenders</span></span>
+ <span data-ttu-id="d575a-180">置き換えるロジックとは異なる責任を持つロジックを記述し **ません**。</span><span class="sxs-lookup"><span data-stu-id="d575a-180">**Don't** write logic that has a different responsibility than the logic that is being replaced.</span></span>
+ <span data-ttu-id="d575a-181">置き換えロジックが適用されない場合、基本機能を呼び出し **ます** (次を呼び出し)。</span><span class="sxs-lookup"><span data-stu-id="d575a-181">**Do** call the base functionality (call next) when the replacement logic doesn't apply.</span></span>
+ <span data-ttu-id="d575a-182">基本機能 (次を呼び出し) を呼び出さずにロジックを完全に置き換えることを **回避します**。</span><span class="sxs-lookup"><span data-stu-id="d575a-182">**Avoid** replacing logic completely by not calling the base functionality (call next).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]