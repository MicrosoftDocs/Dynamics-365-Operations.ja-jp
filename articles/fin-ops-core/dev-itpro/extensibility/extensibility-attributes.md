---
title: メソッドを拡張可能にする属性
description: このトピックでは、メソッドを拡張可能にする属性について説明します。
author: MichaelFruergaardPontoppidan
manager: AnnBe
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2018-09-09
ms.dyn365.ops.version: Platform update 20
ms.openlocfilehash: 46cb82e0dbd15d9f37b1499dbe3f8319f3c5365c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183329"
---
# <a name="attributes-that-make-methods-extensible"></a><span data-ttu-id="c3575-103">メソッドを拡張可能にする属性</span><span class="sxs-lookup"><span data-stu-id="c3575-103">Attributes that make methods extensible</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3575-104">このトピックでは、メソッドの拡張性機能を制御するために使用できるさまざまな属性について説明します。</span><span class="sxs-lookup"><span data-stu-id="c3575-104">This topic describes the various attributes that can be used to control extensibility capabilities for methods.</span></span>

<span data-ttu-id="c3575-105">次の表は、メソッドの拡張性およびアクセシビリティの既定のサポートの概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="c3575-105">The following table provides an overview of the default support for extensibility and accessibility on methods.</span></span> <span data-ttu-id="c3575-106">さらに、メソッド シグネチャの変更に関するガイダンスも提供します。</span><span class="sxs-lookup"><span data-stu-id="c3575-106">The table also provides guidance on the method signature changes.</span></span>

|   | <span data-ttu-id="c3575-107">フック可能</span><span class="sxs-lookup"><span data-stu-id="c3575-107">Hookable</span></span> | <span data-ttu-id="c3575-108">折り返し可能</span><span class="sxs-lookup"><span data-stu-id="c3575-108">Wrappable</span></span> | <span data-ttu-id="c3575-109">置き換え可能</span><span class="sxs-lookup"><span data-stu-id="c3575-109">Replaceable</span></span> | <span data-ttu-id="c3575-110">ユーザー補助</span><span class="sxs-lookup"><span data-stu-id="c3575-110">Accessibility</span></span> | <span data-ttu-id="c3575-111">署名</span><span class="sxs-lookup"><span data-stu-id="c3575-111">Signature</span></span> | 
|---|----------|-----------|-------------|---------------|-----------|
| <span data-ttu-id="c3575-112">**プライベート**</span><span class="sxs-lookup"><span data-stu-id="c3575-112">**private**</span></span> | <span data-ttu-id="c3575-113">無</span><span class="sxs-lookup"><span data-stu-id="c3575-113">No</span></span> | <span data-ttu-id="c3575-114">該当なし</span><span class="sxs-lookup"><span data-stu-id="c3575-114">N/A</span></span> | <span data-ttu-id="c3575-115">該当なし</span><span class="sxs-lookup"><span data-stu-id="c3575-115">N/A</span></span> | <span data-ttu-id="c3575-116">定義されているクラス内からアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c3575-116">Accessible from within class it is defined in.</span></span> | <span data-ttu-id="c3575-117">シグネチャは変更可能</span><span class="sxs-lookup"><span data-stu-id="c3575-117">Signature can be changed</span></span> |
| <span data-ttu-id="c3575-118">**保護された内部**</span><span class="sxs-lookup"><span data-stu-id="c3575-118">**protected internal**</span></span> | <span data-ttu-id="c3575-119">いいえ</span><span class="sxs-lookup"><span data-stu-id="c3575-119">No</span></span> | <span data-ttu-id="c3575-120">はい。プラットフォーム更新 25 以降から</span><span class="sxs-lookup"><span data-stu-id="c3575-120">Yes, from Platform update 25 onward</span></span> | <span data-ttu-id="c3575-121">いいえ</span><span class="sxs-lookup"><span data-stu-id="c3575-121">No</span></span> | <span data-ttu-id="c3575-122">定義されているクラスから、および同じモデル内の派生クラスからアクセス可能です。</span><span class="sxs-lookup"><span data-stu-id="c3575-122">Accessible from with the class it is defined, from derived classes, and from classes in the same model.</span></span> | <span data-ttu-id="c3575-123">シグネチャでは互換性が維持されている必要があります</span><span class="sxs-lookup"><span data-stu-id="c3575-123">Signature must remain compatible</span></span> |
| <span data-ttu-id="c3575-124">**内部**</span><span class="sxs-lookup"><span data-stu-id="c3575-124">**internal**</span></span> | <span data-ttu-id="c3575-125">無</span><span class="sxs-lookup"><span data-stu-id="c3575-125">No</span></span> | <span data-ttu-id="c3575-126">無</span><span class="sxs-lookup"><span data-stu-id="c3575-126">No</span></span> | <span data-ttu-id="c3575-127">無</span><span class="sxs-lookup"><span data-stu-id="c3575-127">No</span></span> | <span data-ttu-id="c3575-128">同じモデルでアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c3575-128">Accessible in the same model.</span></span> | <span data-ttu-id="c3575-129">シグネチャは変更可能</span><span class="sxs-lookup"><span data-stu-id="c3575-129">Signature can be changed</span></span> |
| <span data-ttu-id="c3575-130">**保護**</span><span class="sxs-lookup"><span data-stu-id="c3575-130">**protected**</span></span> | <span data-ttu-id="c3575-131">いいえ</span><span class="sxs-lookup"><span data-stu-id="c3575-131">No</span></span> | <span data-ttu-id="c3575-132">はい。最終とマークされている場合以外</span><span class="sxs-lookup"><span data-stu-id="c3575-132">Yes, unless marked final</span></span> | <span data-ttu-id="c3575-133">いいえ</span><span class="sxs-lookup"><span data-stu-id="c3575-133">No</span></span> | <span data-ttu-id="c3575-134">定義されているクラスから、および派生クラスからアクセス可能です。</span><span class="sxs-lookup"><span data-stu-id="c3575-134">Accessible from with the class it is defined and from derived classes.</span></span> | <span data-ttu-id="c3575-135">シグネチャでは互換性が維持されている必要があります</span><span class="sxs-lookup"><span data-stu-id="c3575-135">Signature must remain compatible</span></span> |
| <span data-ttu-id="c3575-136">**パブリック**</span><span class="sxs-lookup"><span data-stu-id="c3575-136">**public**</span></span> | <span data-ttu-id="c3575-137">はい</span><span class="sxs-lookup"><span data-stu-id="c3575-137">Yes</span></span> | <span data-ttu-id="c3575-138">はい。最終とマークされている場合以外</span><span class="sxs-lookup"><span data-stu-id="c3575-138">Yes, unless marked final</span></span> | <span data-ttu-id="c3575-139">いいえ</span><span class="sxs-lookup"><span data-stu-id="c3575-139">No</span></span> | <span data-ttu-id="c3575-140">定義されたクラス、派生クラス、および定義するクラスにアクセスできるその他のクラスからアクセス可能です。</span><span class="sxs-lookup"><span data-stu-id="c3575-140">Accessible from within the class it is defined, derived classes, and other classes that have access to the defining class.</span></span> | <span data-ttu-id="c3575-141">シグネチャでは互換性が維持されている必要があります</span><span class="sxs-lookup"><span data-stu-id="c3575-141">Signature must remain compatible</span></span> |

## <a name="hookable"></a><span data-ttu-id="c3575-142">フック可能</span><span class="sxs-lookup"><span data-stu-id="c3575-142">Hookable</span></span>
<span data-ttu-id="c3575-143">メソッドがフック可能な場合、拡張担当者はプリイベントとポストイベントにサブスクライブできます。</span><span class="sxs-lookup"><span data-stu-id="c3575-143">If a method is hookable, extenders can subscribe to pre-events and post-events.</span></span>

<span data-ttu-id="c3575-144">パブリック メソッドの場合、メソッドに **\[Hookable(false)\]** を追加することでオプトアウトできます。</span><span class="sxs-lookup"><span data-stu-id="c3575-144">For public methods, you can opt out by adding **\[Hookable(false)\]** to the method.</span></span>

<span data-ttu-id="c3575-145">**\[Hookable(true)\]** をメソッドに追加して、プライベートおよび保護されたメソッドをオプトインできます。</span><span class="sxs-lookup"><span data-stu-id="c3575-145">You can opt in for private and protected methods by adding **\[Hookable(true)\]** to the method.</span></span>

<span data-ttu-id="c3575-146">メソッドが明示的に **\[Hookable(false)\]** とマークされている場合、折り返しはできません。</span><span class="sxs-lookup"><span data-stu-id="c3575-146">If a method is explicitly marked as **\[Hookable(false)\]**, then it is not wrappable.</span></span>

### <a name="best-practices-when-you-write-code"></a><span data-ttu-id="c3575-147">コードの作成時のベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="c3575-147">Best practices when you write code</span></span>
<span data-ttu-id="c3575-148">メソッドがフック可能な場合、コンパイラは拡張ポイントでメソッドを有効にするために特別な中間言語 (IL) コードを生成します。</span><span class="sxs-lookup"><span data-stu-id="c3575-148">When a method is hookable, the compiler generates extra intermediate language (IL) code to enable the method as an extension point.</span></span> <span data-ttu-id="c3575-149">余分なコードにはパフォーマンスのオーバーヘッドがありますが、このオーバーヘッドはほとんどの場合は無視できます。</span><span class="sxs-lookup"><span data-stu-id="c3575-149">Although the extra code has performance overhead, this overhead is negligible in most cases.</span></span> <span data-ttu-id="c3575-150">ただし、パフォーマンスが重要なメソッドでは、フック不能としてメソッドをマーキングすることを検討してください。</span><span class="sxs-lookup"><span data-stu-id="c3575-150">However, for performance-critical methods, consider marking the method as non-hookable.</span></span>

## <a name="wrappable"></a><span data-ttu-id="c3575-151">折り返し可能</span><span class="sxs-lookup"><span data-stu-id="c3575-151">Wrappable</span></span>
<span data-ttu-id="c3575-152">メソッドが折り返し可能な場合は、拡張担当者はコマンド チェーン (CoC) を使用して折り返すことができます。</span><span class="sxs-lookup"><span data-stu-id="c3575-152">If a method is wrappable, extenders can wrap it by using Chain of Command (CoC).</span></span> <span data-ttu-id="c3575-153">拡張担当者は、CoC を中断することが許可されていないため、次を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3575-153">Extenders must call next, because they aren't allowed to break the CoC.</span></span>

<span data-ttu-id="c3575-154">保護されたパブリック メソッドの場合、メソッドに **\[Wrappable(false)\]** を追加することでオプトアウトできます。</span><span class="sxs-lookup"><span data-stu-id="c3575-154">For protected and public methods, you can opt out by adding **\[Wrappable(false)\]** to the method.</span></span>

<span data-ttu-id="c3575-155">プライベート メソッドをオプトインすることはできません。</span><span class="sxs-lookup"><span data-stu-id="c3575-155">You can't opt in for private methods.</span></span>

### <a name="best-practices-when-you-write-code"></a><span data-ttu-id="c3575-156">コードの作成時のベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="c3575-156">Best practices when you write code</span></span>
<span data-ttu-id="c3575-157">CoC は、さまざまな点で継承に似ています。</span><span class="sxs-lookup"><span data-stu-id="c3575-157">CoC resembles inheritance in many ways.</span></span> <span data-ttu-id="c3575-158">通常、他のユーザーが変更するのではなくメソッドを呼び出すことができるようにするには、最終としてメソッドをマークします。</span><span class="sxs-lookup"><span data-stu-id="c3575-158">Typically, if you want other people to be able to call your method but not change it, you mark the method as final.</span></span> <span data-ttu-id="c3575-159">これらのメソッドを折り返し不可またはフック不可としてマーキングすることを検討してください。</span><span class="sxs-lookup"><span data-stu-id="c3575-159">Consider marking these methods as non-wrappable or non-hookable.</span></span>

## <a name="replaceable"></a><span data-ttu-id="c3575-160">置き換え可能</span><span class="sxs-lookup"><span data-stu-id="c3575-160">Replaceable</span></span> 
<span data-ttu-id="c3575-161">メソッドが置き換え可能な場合は、拡張担当者は CoC を使用して折り返しできますが、無条件に次を呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c3575-161">If a method is replaceable, extenders can wrap it by using CoC, but they don't have to unconditionally call next.</span></span> <span data-ttu-id="c3575-162">拡張担当者は CoC を中断できますが、条件がある場合のみ中断することが期待されます。</span><span class="sxs-lookup"><span data-stu-id="c3575-162">Although extenders can break the CoC, the expectation is that they will only conditionally break it.</span></span> <span data-ttu-id="c3575-163">コンパイラは、次の呼び出しを強制しません。</span><span class="sxs-lookup"><span data-stu-id="c3575-163">The compiler doesn't enforce calls to next.</span></span>

<span data-ttu-id="c3575-164">置き換え可能にするには、メソッドも折り返し可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3575-164">To be replaceable, a method must also be wrappable.</span></span>

<span data-ttu-id="c3575-165">折り返し可能なメソッドの場合、メソッドに **\[Replaceable\]** を追加することでオプトインできます。</span><span class="sxs-lookup"><span data-stu-id="c3575-165">For wrappable methods, you can opt in by adding **\[Replaceable\]** to the method.</span></span>

### <a name="best-practices-when-you-write-code"></a><span data-ttu-id="c3575-166">コードの作成時のベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="c3575-166">Best practices when you write code</span></span>
<span data-ttu-id="c3575-167">メソッドの置き換え可能な場合、CoC を使用して拡張することができ、次の実行をスキップできます。</span><span class="sxs-lookup"><span data-stu-id="c3575-167">When a method is replaceable, it can be extended by using CoC, and the execution of next can be skipped.</span></span> <span data-ttu-id="c3575-168">メソッドを置き換え可能にできるようにする前に、拡張担当者がメソッドの実行をスキップした場合の機能への影響を十分に評価する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3575-168">Before you enable a method to be replaceable, you should thoroughly assess the functional impact if an extender skips the execution of the method.</span></span>
            
+ <span data-ttu-id="c3575-169">**\[Replaceable\]** を持つメソッドに、メソッドの責任を説明する XML ドキュメントがあることを確認**します**。</span><span class="sxs-lookup"><span data-stu-id="c3575-169">**Do** make sure that methods that have **\[Replaceable\]** have XML documentation that describes the responsibility of the method.</span></span>
+ <span data-ttu-id="c3575-170">顧客が置き換えられたロジックをスキップして何もしないようにすうるには、**\[Replaceable\]** を使用**しません**。</span><span class="sxs-lookup"><span data-stu-id="c3575-170">**Don't** use **\[Replaceable\]** to let consumers skip the replaced logic and do nothing.</span></span>
+ <span data-ttu-id="c3575-171">**SysExtension** を代わりに使用可能な場合は、ファクトリ メソッドに **\[Replaceable\]** を使用**しません**。</span><span class="sxs-lookup"><span data-stu-id="c3575-171">**Don't** use **\[Replaceable\]** for factory methods when **SysExtension** can be used instead.</span></span>
+ <span data-ttu-id="c3575-172">メソッドがデータベースまたはクラスの状態を変更する場合、**\[Replaceable\]** の使用を**回避します**。</span><span class="sxs-lookup"><span data-stu-id="c3575-172">**Avoid** using **\[Replaceable\]** when the method changes databases or class state.</span></span>
+ <span data-ttu-id="c3575-173">メソッドが複数の工程を実行し、複数の責任を持つ場合、**\[Replaceable\]** の使用を**回避します**。</span><span class="sxs-lookup"><span data-stu-id="c3575-173">**Avoid** using **\[Replaceable\]** if the method performs multiple operations and has multiple responsibilities.</span></span> <span data-ttu-id="c3575-174">代わりに、それぞれが単一の責任を持つ別個のメソッドにメソッドをリファクタリングし、どのメソッドを実際に置き換え可能にする必要があるかを検討します。</span><span class="sxs-lookup"><span data-stu-id="c3575-174">Instead, refactor the method into separate methods, each of which has a single responsibility, and consider which methods should actually be replaceable.</span></span>
+ <span data-ttu-id="c3575-175">変換を解決するために、**\[Replaceable\]** の使用を**検討します**。</span><span class="sxs-lookup"><span data-stu-id="c3575-175">**Consider** using **\[Replaceable\]** to solve transformations.</span></span> 

    <span data-ttu-id="c3575-176">**例:** 既定のブロックがスローを持つ列挙値より切り替えステートメントを使う列挙変換。</span><span class="sxs-lookup"><span data-stu-id="c3575-176">**Example:** Enum conversion that uses a switch statement over enum values, where the default block has a throw.</span></span>

+ <span data-ttu-id="c3575-177">ルックアップと jumpref をオーバーライドするために **\[Replaceable\]** を使用することを**検討します**。</span><span class="sxs-lookup"><span data-stu-id="c3575-177">**Consider** using **\[Replaceable\]** to override lookups and jumprefs.</span></span>
 
### <a name="best-practices-for-extenders"></a><span data-ttu-id="c3575-178">拡張担当者のベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="c3575-178">Best practices for extenders</span></span>
+ <span data-ttu-id="c3575-179">置き換えるロジックとは異なる責任を持つロジックを記述し**ません**。</span><span class="sxs-lookup"><span data-stu-id="c3575-179">**Don't** write logic that has a different responsibility than the logic that is being replaced.</span></span>
+ <span data-ttu-id="c3575-180">置き換えロジックが適用されない場合、基本機能を呼び出し**ます** (次を呼び出し)。</span><span class="sxs-lookup"><span data-stu-id="c3575-180">**Do** call the base functionality (call next) when the replacement logic doesn't apply.</span></span>
+ <span data-ttu-id="c3575-181">基本機能 (次を呼び出し) を呼び出さずにロジックを完全に置き換えることを**回避します**。</span><span class="sxs-lookup"><span data-stu-id="c3575-181">**Avoid** replacing logic completely by not calling the base functionality (call next).</span></span>
