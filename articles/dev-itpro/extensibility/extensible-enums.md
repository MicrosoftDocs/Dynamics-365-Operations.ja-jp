---
title: "拡張可能列挙の書き込み"
description: "このトピックでは、拡張可能列挙を書き込む方法について説明します。"
author: smithanataraj
manager: AnnBe
ms.date: 09/26/2018
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
ms.author: smithanataraj
ms.search.validFrom: 2018-09-09
ms.dyn365.ops.version: Platform update 20
ms.translationtype: HT
ms.sourcegitcommit: f526a4bf7cb7c0a48f3d7b1c4f53705f0cdb41b5
ms.openlocfilehash: 04c1a7dd5430fbb0476ad0889dbf8d2a2e7a07e2
ms.contentlocale: ja-jp
ms.lasthandoff: 09/26/2018

---

# <a name="write-extensible-enums"></a><span data-ttu-id="a3b9b-103">拡張可能列挙の書き込み</span><span class="sxs-lookup"><span data-stu-id="a3b9b-103">Write extensible enums</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3b9b-104">列挙を拡張可能にするには、以下の列挙プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-104">An enumeration (enum) is made extensible by setting the following enum properties:</span></span>

- <span data-ttu-id="a3b9b-105">Is Extensible = True</span><span class="sxs-lookup"><span data-stu-id="a3b9b-105">Is Extensible = True</span></span>
- <span data-ttu-id="a3b9b-106">UseEnumValue = No</span><span class="sxs-lookup"><span data-stu-id="a3b9b-106">UseEnumValue = No</span></span>

<span data-ttu-id="a3b9b-107">これらのプロパティを設定する場合、下位の実装者がより多くの要素で列挙を拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-107">If you set these properties, downstream implementors can extend the enum with more elements.</span></span> <span data-ttu-id="a3b9b-108">要素の値は、展開時に決定され、システム間で同じになりません。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-108">The values of the elements are determined at deployment time and won't be identical across systems.</span></span> <span data-ttu-id="a3b9b-109">ただし、次の動作が確認されます。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-109">However, the following behavior is ensured:</span></span>

+ <span data-ttu-id="a3b9b-110">データ アップグレード スクリプトは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-110">Data upgrade scripts aren't required.</span></span> <span data-ttu-id="a3b9b-111">列挙値は、拡張される列挙に関係なく、データベースに保存されます。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-111">Enum values are persisted in the database, regardless of the enum that is extended.</span></span> <span data-ttu-id="a3b9b-112">したがって、列挙が拡張可能になると、すべてのシステムで使用されている列挙が優先されます。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-112">Therefore, when an enum is made extensible, the enum values that are used on any system will prevail.</span></span>
+ <span data-ttu-id="a3b9b-113">列挙の最初の要素は、0 (ゼロ) の値を取得します。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-113">The first element in the enum gets a value of 0 (zero).</span></span> <span data-ttu-id="a3b9b-114">したがって、拡張可能列挙は **not** 演算子にも使用できます。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-114">Therefore, an extensible enum can still be used with the **not** operator.</span></span> <span data-ttu-id="a3b9b-115">唯一の例外は、列挙が拡張可能になる前に、列挙の最初の要素がゼロ以外の値を持っていた場合です。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-115">The only exception is when the first element of the enum had a non-zero value before the enum was made extensible.</span></span>
    
## <a name="using-extensible-enums-in-code"></a><span data-ttu-id="a3b9b-116">コードでの拡張可能列挙の使用</span><span class="sxs-lookup"><span data-stu-id="a3b9b-116">Using extensible enums in code</span></span>
<span data-ttu-id="a3b9b-117">列挙値は開発者により制御されなくなったため、列挙値に関する確実性はありません。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-117">Because enum values are no longer controlled by the developer, there is no certainty about the enum values.</span></span> <span data-ttu-id="a3b9b-118">コードで拡張可能列挙を使用する場合は、比較で拡張可能列挙を使用することはできない点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-118">When you use extensible enums in code, remember that extensible enums can't be used in comparisons.</span></span> <span data-ttu-id="a3b9b-119">たとえば、**MyEnum::Value1 \> MyEnum::Value2** などです。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-119">For example, **MyEnum::Value1 \> MyEnum::Value2**.</span></span>

<span data-ttu-id="a3b9b-120">さらに、整数と列挙の間のすべての変換を探します。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-120">Also, look for any conversions between integers and enums.</span></span> <span data-ttu-id="a3b9b-121">たとえば、ビューとクエリのモデル化された範囲、比較を使用するか比較でハードコード化された整数値を使用してコードから作成したクエリ (**\<** や **\>** など) などです。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-121">For example, modeled ranges in views and queries, and queries that are created from code by using comparisons, such as **\<** and **\>** or by using hardcoded integer values in comparisons.</span></span>

<span data-ttu-id="a3b9b-122">モデルと依存しているすべてのモデルをコンパイルすると、比較および整数への変換がコンパイラによってエラーとして検出されます。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-122">When the model and all dependent models are compiled, the comparisons and conversions to integers will be detected by the compiler as errors.</span></span>
    
<span data-ttu-id="a3b9b-123">列挙値が使用されているロジックがで**小さなメソッド**で抽出されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-123">Make sure that logic where the enum values are used is extracted in **smaller methods**.</span></span> <span data-ttu-id="a3b9b-124">この方法により、コマンド チェーン (CoC) を使用する拡張が、追加された列挙値を処理できます。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-124">In that way, an extension that uses Chain of Command (CoC) can handle the enum values that are added.</span></span>

<span data-ttu-id="a3b9b-125">インスタンス化が列挙値に基づいている**構築**メソッドの場合、可能な場合は必ず切り替えブロックを **SysExtension** に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-125">For **construct** methods where the instantiation is based on enum values, replace switch blocks with **SysExtension** wherever such a replacement is possible.</span></span> <span data-ttu-id="a3b9b-126">それ以外の場合、既定のブロックが拡張可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-126">In other cases, make sure that the default block is extensible.</span></span> <span data-ttu-id="a3b9b-127">例については、**PurchRFQCaseCopying** クラスを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-127">For an example, see the **PurchRFQCaseCopying** class.</span></span>

<span data-ttu-id="a3b9b-128">列挙が**切り替えブロック**で使用される場合、拡張可能ではないスローを持つか持たない既定のブロックを回避します。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-128">If the enum is used in **switch blocks**, avoid having default blocks that either have or don't have throws that aren't extensible.</span></span> <span data-ttu-id="a3b9b-129">列挙値に**長い切り替えケース ブロック**または **if...else ブロック**がある場合、列挙に関連する特定のロジックを処理するクラス階層を作成することを検討します。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-129">When there are **long switch case blocks** or **if...else blocks** for the enum values, consider creating a class hierarchy to handle specific logic that is related to the enum.</span></span> <span data-ttu-id="a3b9b-130">例については、**PriceGroupTypeTradeAgreementMapping** クラス階層を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-130">For an example, see the **PriceGroupTypeTradeAgreementMapping** class hierarchy.</span></span>

<span data-ttu-id="a3b9b-131">列挙値を使用するクエリ範囲に **in** キーワードを使用し、**in** キーワードが使用するコンテナーを拡張可能にします。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-131">Use the **in** keyword for query ranges that use the enum values, and make the container that the **in** keyword uses extensible.</span></span>

## <a name="potential-issues"></a><span data-ttu-id="a3b9b-132">潜在的な問題</span><span class="sxs-lookup"><span data-stu-id="a3b9b-132">Potential issues</span></span>
<span data-ttu-id="a3b9b-133">いくつかの列挙では、要素が特定の順序または特定の値を持つ必要があり、拡張可能にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-133">Some enums require the elements to have a certain order or value, and cannot be made extensible.</span></span> <span data-ttu-id="a3b9b-134">これは、ドラフト、承認済み、完了、またはアーカイブなど、値が論理的な連続する順序を表すステータス列挙の可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-134">This could be status enums, where the values represent a logical progressive sequence, like: Draft, Approved, Completed, or Archived.</span></span> <span data-ttu-id="a3b9b-135">別の列挙またはタブページ コントロールの番号など、別のコンポーネントと一致する固定整数値が値に必要な列挙の可能性もあります。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-135">It could also be enums where the values must have a fixed integral value to match another artifact, like another enum or a tabpage control's number.</span></span>   

<span data-ttu-id="a3b9b-136">いくつかの列挙には、多くの要素があります。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-136">Some enums have many elements.</span></span> <span data-ttu-id="a3b9b-137">列挙は、最大 250 の要素をサポートします。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-137">Enums support up to 250 elements.</span></span> <span data-ttu-id="a3b9b-138">列挙に多くの要素がある場合 (100 を超えるなど)、列挙を拡張可能にするのではなく、ソリューションを再設計することを検討します。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-138">If your enum has many elements, such as more than 100, consider redesigning the solution instead of making the enum extensible.</span></span> <span data-ttu-id="a3b9b-139">列挙が拡張可能である場合、後で要素を追加すると、追加が制限を超える可能性があるため、顧客の結合ソリューションが壊れる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a3b9b-139">If the enum is extensible, then adding more elements in the future might break customers's combined solution as the addition might exceed the limit.</span></span>

