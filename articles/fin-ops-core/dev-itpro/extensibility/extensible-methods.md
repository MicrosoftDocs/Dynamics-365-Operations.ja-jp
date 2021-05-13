---
title: 拡張可能なメソッドの書き込み
description: このトピックでは、拡張可能メソッドを書き込む方法について説明します。
author: smithanataraj
ms.date: 09/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2018-09-09
ms.dyn365.ops.version: Platform update 20
ms.openlocfilehash: 7541a773526ae9262655fa9e21c6df886bd90783
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866041"
---
# <a name="write-extensible-methods"></a><span data-ttu-id="a3487-103">拡張可能なメソッドの書き込み</span><span class="sxs-lookup"><span data-stu-id="a3487-103">Write extensible methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3487-104">メソッドを拡張する前に、メソッドの公開されている機能と、メソッドが使用されるシナリオに拡張が与える影響を評価する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3487-104">Before you make a method extensible, you should assess the exposed functionality of the method and the impact that the extensions might have on the scenario where the method is used.</span></span> <span data-ttu-id="a3487-105">たとえば、ビジネス シナリオによっては、テーブル レコードを初期化する拡張機能を有効にした場合に低リスクになりますが、固有の検証をスキップする拡張機能を有効にした場合にリスクが高くなります。</span><span class="sxs-lookup"><span data-stu-id="a3487-105">For example, depending on the business scenario, there is low risk if you enable extensions to initialize a table record but high risk if you enable extensions to skip a specific validation.</span></span> <span data-ttu-id="a3487-106">メソッドが他の機能拡張と並行して拡張される場合の影響を検討することもできます。</span><span class="sxs-lookup"><span data-stu-id="a3487-106">You might also want to consider the impact if the method is extended in parallel with other extensions.</span></span>

<span data-ttu-id="a3487-107">メソッドを拡張可能にすると、メソッドのシグネチャまたはロジックが変更された場合のユーザーへの潜在的な影響のため、メソッドのさらなる変更が制限されます。</span><span class="sxs-lookup"><span data-stu-id="a3487-107">After you've made a method extensible, future modifications to the method are restricted because of the potential user impact if the method signature or logic is changed.</span></span>
    
<span data-ttu-id="a3487-108">拡張可能コードを作成するときに準拠するべきいくつかのガイドラインを次に示します。</span><span class="sxs-lookup"><span data-stu-id="a3487-108">Here are some guidelines to follow when you write extensible code:</span></span>
    
+ <span data-ttu-id="a3487-109">**短くて簡潔なメソッドを記述**: メソッドの責任は 1 つだけにしてください。</span><span class="sxs-lookup"><span data-stu-id="a3487-109">**Write short and concise methods** – A method should have only one responsibility.</span></span> <span data-ttu-id="a3487-110">これによりでは、メソッドの拡張が簡単になり、拡張がメソッドの特定の責任でのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="a3487-110">This approach enables easy extensions of the method, where the extensions can act only on the specific responsibility of the method.</span></span> <span data-ttu-id="a3487-111">単純な例として、クラス オブジェクトの構築および初期化を 2 つの異なるメソッドに保持します。</span><span class="sxs-lookup"><span data-stu-id="a3487-111">As a simple example, keep the construction and initialization of a class object in two separate methods.</span></span>
+ <span data-ttu-id="a3487-112">**必要なものだけを公開**: 追加される新しいクラス メンバーまたはメソッドの場合、追加する新しいクラス メンバーまたはメソッドを非公開のままにし、最小限のアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="a3487-112">**Expose only what is necessary** – For any new class members or methods that are added, 'Keep any new class members or methods that you add private, to allow minimal access to them.</span></span>
+ <span data-ttu-id="a3487-113">**プライベート、保護、パブリック、最終を明示的に使用する**: メソッドおよびクラス フィールドでは、この方法により、コードの拡張担当者を拡張ポイントに導きますが、拡張担当者が注意しなかったり依存しなかった部分を完全に管理し続けることができます。</span><span class="sxs-lookup"><span data-stu-id="a3487-113">**Use private, protected, public, and final explicitly** – For methods and class fields, this approach will guide any extenders of your code to your extension points but still let you keep full control of the parts that the extenders should not care about or depend on.</span></span>
+ <span data-ttu-id="a3487-114">**メソッド parameters**</span><span class="sxs-lookup"><span data-stu-id="a3487-114">**Method parameters**</span></span>

    - <span data-ttu-id="a3487-115">このメソッドは、多くの場合長くなるため、リファクタリングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3487-115">The method is most likely long and should be refactored.</span></span> <span data-ttu-id="a3487-116">メソッド全体をクラスにリファクタリングするか、必要なパラメーターが少ないより小さいメソッドにメソッドを分割するかを検討してください。</span><span class="sxs-lookup"><span data-stu-id="a3487-116">Consider whether you should refactor the whole method into a class or split the method into smaller methods that require fewer parameters.</span></span>
    - <span data-ttu-id="a3487-117">それ以外の場合、いくつかのパラメーターが必要なときは、パラメーターには多くの場合がクラスによって表すことができる一貫性があります。</span><span class="sxs-lookup"><span data-stu-id="a3487-117">In other cases, when several parameters are required, the parameters often have a coherence that can be expressed by a class.</span></span> <span data-ttu-id="a3487-118">クラスでこれらのパラメーターをカプセル化することにより、アプリケーション プログラミング インターフェイス (API) を後で中断せずに、拡張担当者が基準メソッドにパラメーターを追加しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="a3487-118">By encapsulating these parameters in a class, you make it easy for extenders to add additional parameters to the base method, without breaking application programming interfaces (APIs) later.</span></span>

+ <span data-ttu-id="a3487-119">**ブロックの切り替え**</span><span class="sxs-lookup"><span data-stu-id="a3487-119">**Switch blocks**</span></span>

    - <span data-ttu-id="a3487-120">メソッドの途中でブロックを切り替えないでください。</span><span class="sxs-lookup"><span data-stu-id="a3487-120">Avoid switch blocks in the middle of methods.</span></span> <span data-ttu-id="a3487-121">切り替えブロックは、拡張可能になるにはそれ **自身のメソッド** になければなりません。</span><span class="sxs-lookup"><span data-stu-id="a3487-121">A switch block should be in its **own method** to enable it to be extended.</span></span> 
    - <span data-ttu-id="a3487-122">**長いケース ブロック** は、各ケース ブロックのサブクラスを持つクラス/クラス階層にリファクタリングされるのに適した候補です。</span><span class="sxs-lookup"><span data-stu-id="a3487-122">**Long case blocks** are good candidates for being refactored into a class/class hierarchy that has a subclass for each case block.</span></span> <span data-ttu-id="a3487-123">例については、**SalesLineCopyFromSource** クラス階層を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3487-123">For an example, see the **SalesLineCopyFromSource** class hierarchy.</span></span>
    - <span data-ttu-id="a3487-124">切り替えステートメントでは **既定のブロック** を回避してください。切り替えブロックを拡張不能にするメソッドを作成するためです。</span><span class="sxs-lookup"><span data-stu-id="a3487-124">Avoid **default blocks** in switch statements, because they make the method that has the switch block non-extensible.</span></span>
    - <span data-ttu-id="a3487-125">切り替えステートメントの **既定のブロックでスロー ステートメント** を回避してください。切り替えステートメントを拡張不能にするスイッチを作成するためです。</span><span class="sxs-lookup"><span data-stu-id="a3487-125">Avoid **throw statements in the default block** of a switch statement, because they make the switch statement non-extensible.</span></span> <span data-ttu-id="a3487-126">既定のケースでのスローを処理する 1 つの方法は、拡張可能な個別のメソッドに切り替えブロックをリファクタリングすることです。</span><span class="sxs-lookup"><span data-stu-id="a3487-126">One way to handle the throw in the default case is to refactor the switch block to a separate method that is extensible.</span></span> <span data-ttu-id="a3487-127">または、メソッド全体を交換可能にすることができます。</span><span class="sxs-lookup"><span data-stu-id="a3487-127">Alternatively, you can make the whole method replaceable.</span></span>
            
        <span data-ttu-id="a3487-128">次の例では、**findOrderHeader** が交換可能です。</span><span class="sxs-lookup"><span data-stu-id="a3487-128">In the following example, **findOrderHeader** is replaceable.</span></span>

        ```xpp
        private Common findOrderHeader(boolean _forUpdate)
        {
            switch (this.InventTransType)
            {
                case InventTransType::Sales:
                    return this.salesTable(_forUpdate);

                default: 
                    return this.findOrderHeaderDefault(_forUpdate);
            }
        }

        [Replaceable]
        protected Common findOrderHeaderDefault(boolean _forUpdate)
        {
            throw error(Error::wrongUseOfFunction(funcName()));
        }
        ```

+ <span data-ttu-id="a3487-129">**While** – メソッドの途中では **while** ブロックを回避してください。**while** ブロックを拡張しにくくなるからです。</span><span class="sxs-lookup"><span data-stu-id="a3487-129">**While** – Avoid **while** blocks in the middle of methods, because it becomes more difficult to extend the **while** blocks.</span></span> <span data-ttu-id="a3487-130">理想的には、**while** ブロックのロジックは、拡張機能を有効にする別のメソッドに置く必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3487-130">Ideally, logic in a **while** block should be in a separate method that enables extensions.</span></span>

    <span data-ttu-id="a3487-131">**while ループ内でのリファクタリング ロジック**</span><span class="sxs-lookup"><span data-stu-id="a3487-131">**Refactoring logic within a while loop**</span></span>

    ![while ブロックのリファクタリング (以前)](media/ExtensibleMethods1.png)

    <span data-ttu-id="a3487-133">**リファクタリング後の拡張可能メソッド**</span><span class="sxs-lookup"><span data-stu-id="a3487-133">**Extensible method after refactoring**</span></span>

    ![while ブロックのリファクタリング (以後)](media/ExtensibleMethods2.png)

+ <span data-ttu-id="a3487-135">**If..else ステートメント**</span><span class="sxs-lookup"><span data-stu-id="a3487-135">**If..else statements**</span></span>

    - <span data-ttu-id="a3487-136">if ステートメントで条件を拡張できるようにするには、if 条件のロジックを別のメソッドに抽出します。</span><span class="sxs-lookup"><span data-stu-id="a3487-136">To enable extension of the conditions in an if statement, extract the logic in the if condition into a separate method.</span></span>
    - <span data-ttu-id="a3487-137">入れ子になった if..else ブロックは回避してください。いずれかのロジックでの変更がむずかしくなるためです。</span><span class="sxs-lookup"><span data-stu-id="a3487-137">Avoid nested if..else blocks, because they make it difficult to change the logic in one of the blocks.</span></span> <span data-ttu-id="a3487-138">この問題を解決するための 1 つの方法は、各条件および各ブロックのロジックを個別のメソッドにリファクタリングすることです。</span><span class="sxs-lookup"><span data-stu-id="a3487-138">One way to resolve this issue is to refactor each condition and the logic in each block into a separate method.</span></span> <span data-ttu-id="a3487-139">この方法では、条件または各ブロックのロジックを拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="a3487-139">In this way, you can extend the conditions or the logic in each block.</span></span>
    - <span data-ttu-id="a3487-140">if..else ブロックが特殊化を処理する場合、ロジックをクラス階層に移動することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="a3487-140">When the if..else blocks handle specialization, consider moving the logic into a class hierarchy.</span></span> <span data-ttu-id="a3487-141">例については、**SalesLineCopyFromSource** を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3487-141">For an example, see **SalesLineCopyFromSource**.</span></span>
    - <span data-ttu-id="a3487-142">一部のシナリオでは、メソッドの "else" ブロックでのスロー (メソッドに if.. else のみある場合) によってメソッドが拡張不能になります。</span><span class="sxs-lookup"><span data-stu-id="a3487-142">In some scenarios, a throw in an 'else' block of a method (when the method only has an if..else) makes the method non-extensible.</span></span> <span data-ttu-id="a3487-143">else でのスローを処理する 1 つの方法は、スローの条件を個別のメソッドにリファクタリングすることです。</span><span class="sxs-lookup"><span data-stu-id="a3487-143">One way to handle the throw in the else is to refactor the conditions for the throw into a separate method.</span></span>

+ <span data-ttu-id="a3487-144">**PrmIsDefault の使用を避ける** – メソッドがオーバーライドされるか折り返し可能な場合、**super()** または **next()** の呼び出し元がすべてのパラメーターを提供します。</span><span class="sxs-lookup"><span data-stu-id="a3487-144">**Avoid using PrmIsDefault** – When the method is overridden or wrappable, the caller of **super()** or **next()** provides all parameters.</span></span> <span data-ttu-id="a3487-145">したがって、**prmIsDefault()** は常に false を返します。</span><span class="sxs-lookup"><span data-stu-id="a3487-145">Therefore, **prmIsDefault()** always returns false.</span></span>
+ <span data-ttu-id="a3487-146">**enumCnt の使用を避ける** – コンパイル時、このメソッドは列挙が持つ値の数の数値リテラルを使用します。</span><span class="sxs-lookup"><span data-stu-id="a3487-146">**Avoid using enumCnt** – At compile time, this method uses a numeric literal of the number of values that an enum has.</span></span> <span data-ttu-id="a3487-147">列挙が拡張されるか、後で拡張可能になった場合、コードを再コンパイルする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3487-147">If the enum is extended or made extensible later, your code will have to be recompiled.</span></span> <span data-ttu-id="a3487-148">代わりに **DictEnum.values()** を使用します。</span><span class="sxs-lookup"><span data-stu-id="a3487-148">Use **DictEnum.values()** instead.</span></span>
+ <span data-ttu-id="a3487-149">**Construct メソッド**</span><span class="sxs-lookup"><span data-stu-id="a3487-149">**Construct methods**</span></span>

    - <span data-ttu-id="a3487-150">拡張を簡単にするには、**SysExtension** フレームワークを使用します。</span><span class="sxs-lookup"><span data-stu-id="a3487-150">Use the **SysExtension** framework to enable easy extensions.</span></span>
    - <span data-ttu-id="a3487-151">ファクトリ メソッドでのスローを回避します。</span><span class="sxs-lookup"><span data-stu-id="a3487-151">Avoid a throw in factory methods.</span></span> <span data-ttu-id="a3487-152">この問題を解決するための 1 つの方法は、拡張できる別のメソッドにスローの条件を抽出することです。</span><span class="sxs-lookup"><span data-stu-id="a3487-152">One way to resolve this issue is to extract the conditions for the throw into a separate method that is extensible.</span></span> <span data-ttu-id="a3487-153">詳細については、このリストの後方にあるスロー ステートメントのガイドラインを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3487-153">For more details, see the guidelines for throw statements later in this list.</span></span>

+ <span data-ttu-id="a3487-154">**静的メソッド**: 余分な状態によって静的メソッド拡張することはできません。</span><span class="sxs-lookup"><span data-stu-id="a3487-154">**Static methods** – Static methods can't be extended with extra state.</span></span> <span data-ttu-id="a3487-155">たとえば、メソッド拡張担当者は、パラメーター メソッドを使用して設定できるプロパティを導入できます。</span><span class="sxs-lookup"><span data-stu-id="a3487-155">For example, a method extender can introduce properties that can be set by using parameter methods.</span></span> <span data-ttu-id="a3487-156">この方法が可能な場合は必ず、代わりにインスタンス メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="a3487-156">Use instance methods instead, whenever this approach is possible.</span></span>
+ <span data-ttu-id="a3487-157">**長いメソッドでロジックの一部を拡張する機能**: メソッド全体をリファクタリングすることができないが、目標がメソッドの一部を拡張可能にすることである場合、抽出メソッド リファクタリングを適用します。</span><span class="sxs-lookup"><span data-stu-id="a3487-157">**Ability to extend part of the logic in a long method** – If it isn't possible to refactor a whole method, but the goal is to make part of the method extensible, apply the extract method refactoring.</span></span> <span data-ttu-id="a3487-158">新しい保護されたメソッドには単一の責任が必要であり、その責任を概念的かつ正確に説明する名前も必要です。</span><span class="sxs-lookup"><span data-stu-id="a3487-158">The new protected method must have a single responsibility, and it must also have a name that conceptually and precisely describes that responsibility.</span></span> <span data-ttu-id="a3487-159">これにより、オーナーおよびすべての拡張担当者は互いに中断することがなくメソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a3487-159">In this way, owners and all extenders can use the method without breaking each other.</span></span> <span data-ttu-id="a3487-160">たとえば、初期化、挿入、テーブル レコードの更新、またはクラスのインスタンス化および初期化は、小さいメソッドに抽出でき、それらの小さい各メソッドで拡張を有効にできます。</span><span class="sxs-lookup"><span data-stu-id="a3487-160">For example, initialization, insertion, updates to a table record, or instantiation and initialization of a class can be extracted into smaller methods, and each of these smaller methods can be enabled for for extensions.</span></span> <span data-ttu-id="a3487-161">その後、元のメソッドがこれらの個々のメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a3487-161">The original method then calls these individual methods.</span></span> <span data-ttu-id="a3487-162">したがって、このメソッドの呼び出し元は中断されません。</span><span class="sxs-lookup"><span data-stu-id="a3487-162">Therefore, the callers to this method aren't broken.</span></span>            
+ <span data-ttu-id="a3487-163">**スロー ステートメント** : 拡張可能な既存のメソッドに追加されるスローは、拡張担当者を中断させる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a3487-163">**Throw statements** – A throw that is added to an existing method that is extensible could break extenders.</span></span> <span data-ttu-id="a3487-164">拡張可能メソッドでスローの条件を追加することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="a3487-164">Consider adding the conditions for the throw in an extensible method.</span></span> <span data-ttu-id="a3487-165">これにより、拡張担当者はメソッドを利用でき、スローを取り除くことができます。</span><span class="sxs-lookup"><span data-stu-id="a3487-165">In this way, extenders can take advantage of the method, and you can get rid of the throw.</span></span>

    <span data-ttu-id="a3487-166">**条件が保護されているメソッドにリファクタリングされる場合**</span><span class="sxs-lookup"><span data-stu-id="a3487-166">**If condition refactored out to a protected method**</span></span>

    ![スロー (前)](media/ExtensibleMethods3.png)

    <span data-ttu-id="a3487-168">**リファクタリング後の拡張可能メソッド**</span><span class="sxs-lookup"><span data-stu-id="a3487-168">**Extensible method after refactoring**</span></span>

    ![スロー (後)](media/ExtensibleMethods4.png)

+ <span data-ttu-id="a3487-170">**作成、読み取り、更新、および削除 (CRUD) ステートメント**</span><span class="sxs-lookup"><span data-stu-id="a3487-170">**Create, read, update and delete (CRUD) statements**</span></span>

    - <span data-ttu-id="a3487-171">クエリを拡張可能にする必要のある状況でクエリ オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="a3487-171">Use Query objects in scenarios where the queries should be extensible.</span></span> <span data-ttu-id="a3487-172">クエリを構築する保護されたメソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="a3487-172">Implement a protected method that builds the query.</span></span> <span data-ttu-id="a3487-173">さらに、結合されたデータ ソース、範囲、および選択フィールドを追加するために、複数の個別のメソッドを構築できます。</span><span class="sxs-lookup"><span data-stu-id="a3487-173">In addition, you might want to build several separate methods to add joined data sources, ranges, and selection fields.</span></span> <span data-ttu-id="a3487-174">この方法では、クエリのさまざまな部分を個別に拡張できます。</span><span class="sxs-lookup"><span data-stu-id="a3487-174">In this way, different parts of the query can be extended individually.</span></span>
    - <span data-ttu-id="a3487-175">**SysQueryInsertRecordSet** を使用して、insert_recordset をクエリに変換します。</span><span class="sxs-lookup"><span data-stu-id="a3487-175">Use **SysQueryInsertRecordSet** to convert insert_recordset to a query.</span></span>
    - <span data-ttu-id="a3487-176">select ステートメントではフィールド リストは避けてください。</span><span class="sxs-lookup"><span data-stu-id="a3487-176">Avoid field lists in select statements.</span></span> <span data-ttu-id="a3487-177">この方法では、拡張することがなく、拡張担当者が追加のフィールドを取得できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="a3487-177">In this way, you enable extenders to retrieve their additional fields without having to extend.</span></span>
    - <span data-ttu-id="a3487-178">クエリ範囲で **in** キーワードを使用し、拡張担当者が値をさらにクエリ範囲に追加できるようにします。</span><span class="sxs-lookup"><span data-stu-id="a3487-178">Use the **in** keyword in query ranges to enable extenders to add more values to the query range.</span></span> <span data-ttu-id="a3487-179">この方法は特に、列挙値を持つクエリ範囲にお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a3487-179">We recommend this approach especially for query ranges that have enum values.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]