---
title: "コードの移行中にデリゲートを使用してモデル間の依存関係の解決"
description: "このトピックでは、デリゲート インスタンスとデリゲート ハンドラ間でコントラクトを定義する手段としてデリゲート メソッドがどのように機能するかについて説明します。"
author: maertenm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 27001
ms.assetid: 6640ae38-58f0-4a29-abca-5acd9489d45d
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 7a6329dcf8dbd0afd6f25f43b2390359569d56bf
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="solve-dependencies-among-models-by-using-delegates-during-code-migration"></a><span data-ttu-id="c6c7b-103">コードの移行中にデリゲートを使用してモデル間の依存関係の解決</span><span class="sxs-lookup"><span data-stu-id="c6c7b-103">Solve dependencies among models by using delegates during code migration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6c7b-104">このトピックでは、デリゲート インスタンスとデリゲート ハンドラ間でコントラクトを定義する手段としてデリゲート メソッドがどのように機能するかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-104">This topic explains how delegate methods serve as a means for defining a contract between the delegate instance and the delegate handler.</span></span>

<a name="overview"></a><span data-ttu-id="c6c7b-105">概要</span><span class="sxs-lookup"><span data-stu-id="c6c7b-105">Overview</span></span>
--------

<span data-ttu-id="c6c7b-106">Microsoft Dynamics 365 for Finance and Operations は、個別パッケージでの各モデルで複数のモデルに分割されます。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-106">Microsoft Dynamics 365 for Finance and Operations is split into more several models, with each model in separate package.</span></span> <span data-ttu-id="c6c7b-107">主要な 3 つのモデルは、アプリケーション プラットフォーム、アプリケーション基盤、およびアプリケーション スイートです (モデルとパッケージについては、[モデル](../dev-tools/models.md)を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-107">The principal 3 models are Application Platform, Application Foundation, and Application Suite (See [Models](../dev-tools/models.md) to learn about models and packages).</span></span> <span data-ttu-id="c6c7b-108">モデル分割を使用して、階層が作成されました。ここで上位のモデルは依存関係を持つことができ、下位のモデル内の要素にアクセスできますが、上位のモデルにはアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-108">With the model split, a hierarchy has been created where a higher model can take dependencies and access elements in the models below, but not in models above.</span></span> <span data-ttu-id="c6c7b-109">この設定では、アプリケーション スイートはその要素、アプリケーション基準の要素およびアプリケーション プラットフォームの要素にフル アクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-109">In this setup, Application Suite has full access to its elements, Application Foundation’s elements, and Application Platform’s elements.</span></span> <span data-ttu-id="c6c7b-110">アプリケーション基準は、独自の要素とアプリケーション プラットフォームの要素にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-110">Application Foundation can access its own elements and those of Application Platform.</span></span> <span data-ttu-id="c6c7b-111">最後に、アプリケーション プラットフォームは独自の要素にのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-111">Finally, Application Platform can only access its own elements.</span></span> 

<span data-ttu-id="c6c7b-112">[![Del1](./media/del1.jpg)](./media/del1.jpg)</span><span class="sxs-lookup"><span data-stu-id="c6c7b-112">[![Del1](./media/del1.jpg)](./media/del1.jpg)</span></span> 

<span data-ttu-id="c6c7b-113">モデルの分割には多くの利点がありますが、上位モデルで定義された要素にアクセスするとき問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-113">While the model split provides many benefits, it creates a problem when trying to access elements defined in higher models.</span></span> <span data-ttu-id="c6c7b-114">上位モデルの要素に下位モデルからアクセスするに、デリゲートが推奨されています。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-114">Delegates are the recommended method for accessing elements in higher models from a lower model.</span></span> <span data-ttu-id="c6c7b-115">デリゲートは、デリゲート インスタンスが呼び出されると、互換性のある署名コードを持つハンドラーが実行されるという点で、イベントと非常によく似ています。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-115">Delegates are very similar to events in that when a delegate instance is invoked, a handler with compatible signature code is executed.</span></span> <span data-ttu-id="c6c7b-116">これにより、ハンドラーである上位レイヤーコードが、デリゲート インスタンスである下位レイヤーコード (デリゲート インスタンス) によって呼び出されるようになります。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-116">This permits higher layer code, the handler, to be called by lower layer code, the delegate instance.</span></span>

## <a name="create-delegates-and-handlers"></a><span data-ttu-id="c6c7b-117">委任およびハンドラーを作成します</span><span class="sxs-lookup"><span data-stu-id="c6c7b-117">Create delegates and handlers</span></span>
<span data-ttu-id="c6c7b-118">デリゲートの宣言には、次の 3 つが必要です。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-118">A delegate declaration must have three things:</span></span>

-   <span data-ttu-id="c6c7b-119">委任キーワード</span><span class="sxs-lookup"><span data-stu-id="c6c7b-119">The delegate keyword</span></span>
-   <span data-ttu-id="c6c7b-120">無効タイプ</span><span class="sxs-lookup"><span data-stu-id="c6c7b-120">Type void</span></span>
-   <span data-ttu-id="c6c7b-121">空のメソッド</span><span class="sxs-lookup"><span data-stu-id="c6c7b-121">Empty method</span></span>

<span data-ttu-id="c6c7b-122">デリゲート メソッドは、デリゲート インスタンスとデリゲート ハンドラー間のコントラクトを定義する手段として機能します。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-122">Delegate methods serve as a means for defining a contract between the delegate instance and the delegate handler.</span></span> <span data-ttu-id="c6c7b-123">デリゲートは、アクション自体を行ないません。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-123">A delegate takes no action itself.</span></span> <span data-ttu-id="c6c7b-124">これは、void 型を持ち、メソッドにコードがないことによって適用されます。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-124">This is enforced by having a void type and having no code in the method.</span></span> 

```
delegate void applyDiscountDelegate(real _receiptTotal, EventHandlerResult _result)
{
}
```

<span data-ttu-id="c6c7b-125">メソッドに **SubscribesTo** キーワードを追加して、静的委任ハンドラーを作成します。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-125">Adding the **SubscribesTo** keyword to a method creates a static delegate handler.</span></span> <span data-ttu-id="c6c7b-126">**SubscribesTo** にはデリゲートのクラス名、およびデリゲート メソッドの文字列名が必要です。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-126">**SubscribesTo** requires the class name of the delegate, and the string name of the delegate method.</span></span> 

<span data-ttu-id="c6c7b-127">デリゲートが適切に処理されるには、デリゲート メソッドの宣言、デリゲート インスタンスおよびデリゲート ハンドラーに*同じ*メソッドの署名が必要です。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-127">In order for a delegate to be properly handled, the delegate method declaration, the delegate instance, and the delegate handler must have the *same* method signature.</span></span> <span data-ttu-id="c6c7b-128">たとえば、次に示すデリゲート インスタンスには、2 つの入力が必要です。実数および EventHandlerResult で、上記のデリゲート宣言およびハンドラー署名と一致するものです。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-128">For example, the delegate instance below takes two inputs, a real number and an EventHandlerResult, matching the delegate declaration and handler signatures above.</span></span> 

![static delegate ハンドラー](media/static-delegate-handler.png)

<span data-ttu-id="c6c7b-130">デリゲートに戻り値がないため、EventHandlerResult がパラメーターとして渡され、デリゲートが返された後に必要な結果値にアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-130">Due to the fact that delegates do not have a return value, an EventHandlerResult is passed as a parameter to provide access to the needed result value after the delegate has returned.</span></span> <span data-ttu-id="c6c7b-131">このトピックでは、SubscribesTo を使用する静的委任ハンドラーについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-131">This topic focuses on static delegate handlers using the SubscribesTo.</span></span> <span data-ttu-id="c6c7b-132">Dynamics AX 2012 からのデリゲート機能が保持されます。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-132">The delegate functionality from Dynamics AX 2012 remains.</span></span> <span data-ttu-id="c6c7b-133">[Dynamics AX 2012で X++ の委任を使用する方法](http://blogs.msdn.com/b/x/archive/2011/08/02/how-to-use-x-delegates-in-dynamics-ax-2012.aspx) は Dynamics AX 2012 の委任の概念について、 Microsoft の開発者 Marcos Calderon が MSDN に投稿した素晴らしいブログです。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-133">[How to use X++ Delegates in Dynamics AX 2012](http://blogs.msdn.com/b/x/archive/2011/08/02/how-to-use-x-delegates-in-dynamics-ax-2012.aspx) is a great blog post on MSDN by Microsoft developer Marcos Calderon on delegate concepts in Dynamics AX 2012.</span></span> <span data-ttu-id="c6c7b-134">これらの概念が引き続き適用されます。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-134">These concepts still apply.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="c6c7b-135">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="c6c7b-135">Example scenarios</span></span>
### <a name="overlaying-an-existing-delegate"></a><span data-ttu-id="c6c7b-136">既存の委任のオーバーレイ</span><span class="sxs-lookup"><span data-stu-id="c6c7b-136">Overlaying an existing delegate</span></span>

<span data-ttu-id="c6c7b-137">デリゲートが必要な多くの場合、以前にオーバーレイされたコードは既に Microsoft によってデリゲート ハンドラーに移動されています。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-137">In many cases where delegates are needed, the code that was formerly overlayed has already been moved to a delegate handler by Microsoft.</span></span> <span data-ttu-id="c6c7b-138">これらのインスタンスで、Microsoft は利用できるデリゲートを作成し、デリゲート ハンドラーで同様の方法でコードをオーバーレイできます。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-138">In these instances, Microsoft created delegates that can be leveraged and the code can be overlayed in a similar manner in the delegate handler.</span></span> <span data-ttu-id="c6c7b-139">このシナリオでは、独立系ソフトウェア ベンダー (ISV) が、LogisticsEntityPostalAddressFormHandler クラスで showSalesTax() メソッドをオーバーレイした Dynamics AX 2012 R3 からコードを移行しています。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-139">In this scenario, an Independent Software Vendor (ISV) is migrating code from Dynamics  AX 2012 R3 where they have overlayed the showSalesTax() method in the LogisticsEntityPostalAddressFormHandler class.</span></span> <span data-ttu-id="c6c7b-140">移行後に、CodeUpgrade プロジェクトは、*Your Solution*、*Microsoft AX 2012*、*Microsoft AX* セクションを使用する LogisticsEntityPostalAddressFormHandler が含まれ、showSalesTax() メソッドを解決します。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-140">After migration, the CodeUpgrade project will contain the LogisticsEntityPostalAddressFormHandler with the *Your Solution*, *Microsoft AX 2012,* and *Microsoft AX* sections to resolve for the showSalesTax() method.</span></span> <span data-ttu-id="c6c7b-141">コメントされた Your Solution セクションには、売上税の表示を承認するための追加のテーブルを追加することによって、showSalesTax() メソッドがオーバーレイされたことが示されています。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-141">The commented Your Solution section shows that the showSalesTax() method was overlayed by adding an additional table to approve showing sales tax from.</span></span> <span data-ttu-id="c6c7b-142">このオーバーレイは、赤で丸で囲まれた &lt;isv&gt; タグの間に表示されます。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-142">This overlay is shown between the &lt;isv&gt; tags circled in red below.</span></span> 

<span data-ttu-id="c6c7b-143">[![4](./media/41.png)](./media/41.png)</span><span class="sxs-lookup"><span data-stu-id="c6c7b-143">[![4](./media/41.png)](./media/41.png)</span></span>

<span data-ttu-id="c6c7b-144">このオーバーレイを Dynamics AX 2012 のコードと比較するとき、これは単純な変更です。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-144">When comparing this overlay with the code from Dynamics AX 2012, this is a simple change.</span></span> <span data-ttu-id="c6c7b-145">オーバーレイによって、switch ステートメントに追加のテーブルが追加されました。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-145">The overlay has added an additional table to the switch statement.</span></span> 

<span data-ttu-id="c6c7b-146">[![5](./media/51.png)](./media/51.png)</span><span class="sxs-lookup"><span data-stu-id="c6c7b-146">[![5](./media/51.png)](./media/51.png)</span></span> 

<span data-ttu-id="c6c7b-147">ただし、Finance and Operations セクションでは、Dynamics AX 2012 コード スニペットのいずれかと同じようには表示されません。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-147">However, the Finance and Operations section does not appear to resemble either of the Dynamics AX 2012 code snippets.</span></span> 

<span data-ttu-id="c6c7b-148">[![6](./media/61.png)](./media/61.png)</span><span class="sxs-lookup"><span data-stu-id="c6c7b-148">[![6](./media/61.png)](./media/61.png)</span></span> 

<span data-ttu-id="c6c7b-149">詳細な点検を行う際、コードはデリゲート メソッド showSalesTax\_delegate() を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-149">Upon deeper inspection, the code is calling a delegate method, showSalesTax\_delegate().</span></span> 

<span data-ttu-id="c6c7b-150">[![this.showSalesTax\_delegate(this.getCallerRecord().TableId, result);](./media/showsalestax_delegate.png)](./media/showsalestax_delegate.png)</span><span class="sxs-lookup"><span data-stu-id="c6c7b-150">[![this.showSalesTax\_delegate(this.getCallerRecord().TableId, result);](./media/showsalestax_delegate.png)](./media/showsalestax_delegate.png)</span></span> 

<span data-ttu-id="c6c7b-151">デリゲートの使用は、コードが別の場所に移動されたことを意味します。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-151">The use of a delegate implies that code has been moved to another location.</span></span> <span data-ttu-id="c6c7b-152">showSalesTax\_delegate() は、アプリケーション基準で宣言され、Application Suite で処理されました。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-152">The showSalesTax\_delegate() has been declared in the Application Foundation and handled in the Application Suite.</span></span> <span data-ttu-id="c6c7b-153">移動されたコードを表示するには、デリゲート ハンドラを探します。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-153">To view the code that has been moved, find the delegate handler.</span></span> <span data-ttu-id="c6c7b-154">**デリゲートとハンドラーの検索** セクションには、デリゲートとハンドラーを検索するメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-154">The **Finding Delegates and Handlers** section contains methods to locate delegates and handlers.</span></span> <span data-ttu-id="c6c7b-155">アプリケーション スイートでデリゲート ハンドラー メソッドを検索した後、showSalesTax() メソッドからから移動されたコードを参照します。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-155">After finding the delegate handler method in the Application Suite, we see the code that has been moved from the showSalesTax() method.</span></span> <span data-ttu-id="c6c7b-156">Dynamics AX 2012 で適用されているオーバーレイされた同じ変更を、デリゲート ハンドラーに適用できます。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-156">The same overlayered changes applied in Dynamics AX 2012 can be applied in the delegate handler.</span></span> 

<span data-ttu-id="c6c7b-157">[![委任とハンドラーのコード サンプルの検索](./media/findingdelegatesandhandles.png)](./media/findingdelegatesandhandles.png)</span><span class="sxs-lookup"><span data-stu-id="c6c7b-157">[![Finding delegates and handlers code sample](./media/findingdelegatesandhandles.png)](./media/findingdelegatesandhandles.png)</span></span> 

<span data-ttu-id="c6c7b-158">委任ハンドラーで switch ステートメントに新しいテーブルを追加した後、コードは Dynamics AX 2012 の場合と同じように機能します。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-158">After adding the new table to the switch statement in the delegate handler, the code will function as it did in Dynamics AX 2012.</span></span> 

<span data-ttu-id="c6c7b-159">[![ShowSalesTax メソッド コード](./media/showsalestaxmethod.png)](./media/showsalestaxmethod.png)</span><span class="sxs-lookup"><span data-stu-id="c6c7b-159">[![ShowSalesTax method code](./media/showsalestaxmethod.png)](./media/showsalestaxmethod.png)</span></span>

### <a name="adding-a-new-delegate"></a><span data-ttu-id="c6c7b-160">新しい委任の追加</span><span class="sxs-lookup"><span data-stu-id="c6c7b-160">Adding a new delegate</span></span>

<span data-ttu-id="c6c7b-161">このシナリオでは、アプリケーション スイートで作成された割引を考慮するために、アプリケーション基準に存在する既存の税計算方法を変更します。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-161">In this scenario, we will modify an existing tax calculation method that resides in the Application Foundation to account for discounts created in the Application Suite.</span></span> <span data-ttu-id="c6c7b-162">Foundation レイヤーの次のクラスは、総額に基づいて税金を計算します。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-162">The following class in the Foundation layer calculates the tax based on the gross total.</span></span> 

![SimpleTax クラス](media/simple-tax.png)

<span data-ttu-id="c6c7b-164">アプリケーション スイートでは、現在の割引を含む ProductDiscount クラスを追加することで割引の概念を導入しました。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-164">In the Application Suite, we have introduced the notion of discounts by adding a ProductDiscount class that contains the current discount.</span></span> 

<span data-ttu-id="c6c7b-165">[![11](./media/112.png)](./media/112.png)</span><span class="sxs-lookup"><span data-stu-id="c6c7b-165">[![11](./media/112.png)](./media/112.png)</span></span> 

<span data-ttu-id="c6c7b-166">Foundation レイヤー下部にある TaxCalculator クラスには、Suite レイヤーの DiscountRate へのアクセス権がないため、委任を使用して受領合計を更新し、税計算に使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-166">The TaxCalculator class, in the lower Foundation layer, does not have access to the DiscountRate in the Suite layer and must use a delegate to update receipt total to use in the tax calculation.</span></span> <span data-ttu-id="c6c7b-167">SimpleTax クラスでは、署名のハンドラーによって必要な状態情報とともにデリゲート メソッド applyDiscountDelegate を作成します。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-167">In the SimpleTax class, we create a delegate method, applyDiscountDelegate, with the state information that is needed by the handler in the signature.</span></span> <span data-ttu-id="c6c7b-168">デリゲート メソッドは、デリゲート インスタンスとハンドラー間のコントラクトを定義することが唯一の目的のため、常に空です。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-168">A delegate method is always empty because its only purpose is to define the contract between the delegate instance and the handler.</span></span> 

```
delegate void applyDiscountDelegate(real _receiptTotal, EventHandlerResult _result)
{
} 
```


<span data-ttu-id="c6c7b-169">**注記:** デリゲートの宣言、デリゲート インスタンスおよびデリゲート ハンドラーの署名は一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-169">**Note:** The signature for the delegate declaration, the delegate instance, and the delegate handler must match.</span></span> <span data-ttu-id="c6c7b-170">デリゲート ハンドラーを実行するコード内の箇所に、デリゲートのインスタンスを作成することが必要になりました。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-170">We now have to create an instance of the delegate at the point in the code where we would like the delegate handler to be run.</span></span> <span data-ttu-id="c6c7b-171">&lt;isv&gt; タグ間での変更は追加されたコードを表します。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-171">The changes in between the &lt;isv&gt; tags represent the added code.</span></span> 

![calculateTotalTax method](media/calculate-total-tax.png)

<span data-ttu-id="c6c7b-173">デリゲートの環境が整い、割引情報へのアクセス権を持つアプリケーション スイート レイヤーに、ハンドラー メソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-173">With the delegate in place, we now add a handler method in the Application Suite layer that has access to the discount information.</span></span> 

![applyDiscountDelegateHandler メソッド](media/apply-discount-delegate-handler.png)

<span data-ttu-id="c6c7b-175">SubscribesTo キーワードを使用して、applyDiscountDelegateHandler メソッドを applyDiscountDelegate デリゲートにハンドラーとして結合します。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-175">Using the SubscribesTo keyword, we tie the applyDiscountDelegateHandler method as a handler to the applyDiscountDelegate delegate.</span></span> <span data-ttu-id="c6c7b-176">**注記:** 委任ごとに複数のハンドラーが存在する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-176">**Note:** There can be more than one handler per delegate.</span></span> <span data-ttu-id="c6c7b-177">ハンドラー メソッドの処理には、定義された順序は**ありません**。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-177">There is **not** a defined order in the processing of handler methods.</span></span> <span data-ttu-id="c6c7b-178">注文が重要な場合は、代行ハンドラーのペアは一緒に連鎖する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-178">If order is important, delegate handler pairs should be chained together.</span></span> <span data-ttu-id="c6c7b-179">以下の最終クラスでは、calculateTotalTax() メソッドが実行されるとき、applyDiscountDelegate が起動および処理され、receiptTotal が更新されて正確な税計算が提供されます。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-179">With the final classes below, when the calculateTotalTax() method is run, the applyDiscountDelegate is fired and handled, updating the receiptTotal to provide an accurate tax calculation.</span></span>

#### <a name="full-code"></a><span data-ttu-id="c6c7b-180">完全なコード</span><span class="sxs-lookup"><span data-stu-id="c6c7b-180">Full Code</span></span>

##### <a name="simpletax-class-in-the-application-foundation-layer"></a><span data-ttu-id="c6c7b-181">Application Foundation Layer の SimpleTax クラス</span><span class="sxs-lookup"><span data-stu-id="c6c7b-181">SimpleTax class in the Application Foundation Layer</span></span>

![SimpleTax クラス](media/simple-tax-full-code.png)

##### <a name="productdiscount-class-in-the-application-suite-layer"></a><span data-ttu-id="c6c7b-183">アプリケーション スイート レイヤーの ProductDiscount クラス</span><span class="sxs-lookup"><span data-stu-id="c6c7b-183">ProductDiscount class in the Application Suite layer</span></span>

![ProductDiscount クラス](media/product-discount-full-code.png)

## <a name="find-delegates-and-handlers"></a><span data-ttu-id="c6c7b-185">委任およびハンドラーを検索します</span><span class="sxs-lookup"><span data-stu-id="c6c7b-185">Find delegates and handlers</span></span>
<span data-ttu-id="c6c7b-186">デリゲートとハンドラーを見つける主要な 3 つの方法があります</span><span class="sxs-lookup"><span data-stu-id="c6c7b-186">There are three key ways to find delegates and handlers</span></span>

-   <span data-ttu-id="c6c7b-187">メタデータ検索</span><span class="sxs-lookup"><span data-stu-id="c6c7b-187">Metadata search</span></span>
-   <span data-ttu-id="c6c7b-188">クラス参照</span><span class="sxs-lookup"><span data-stu-id="c6c7b-188">Class references</span></span>
-   <span data-ttu-id="c6c7b-189">SubscribesTo 参照</span><span class="sxs-lookup"><span data-stu-id="c6c7b-189">SubscribesTo references</span></span>

<span data-ttu-id="c6c7b-190">[Visual Studio でのメタデータ検索](../dev-tools/metadata-search-visual-studio.md) ページで説明されているメタデータ検索ツールは、デリゲート、またはそのハンドラーを検索するための優れた方法です。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-190">The Metadata search tool, described on the [Metadata search in Visual Studio](../dev-tools/metadata-search-visual-studio.md) page, is the best way to find either delegates or their handlers.</span></span> <span data-ttu-id="c6c7b-191">Visual Studio で、<strong>Dynamics 365 **&gt;** メタデータ検索</strong>に移動してメタデータ検索ツールを開きます。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-191">In Visual Studio, go to <strong>Dynamics 365 **&gt; **Metadata Search</strong> to open the metadata search tool.</span></span> 

<span data-ttu-id="c6c7b-192">[![Del15](./media/del15.png)](./media/del15.png)</span><span class="sxs-lookup"><span data-stu-id="c6c7b-192">[![Del15](./media/del15.png)](./media/del15.png)</span></span> 

<span data-ttu-id="c6c7b-193">検索フィールドに、「code:&lt;デリゲート名&gt;」を入力して検索をコードに制限し、デリゲート名の使用を見つけると、デリゲートとハンドラーの両方を返します。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-193">In the search field, type “code:&lt;delegate name&gt;” which will restrict the search to code and find any use of the delegate name, returning both the delegate and handler.</span></span> <span data-ttu-id="c6c7b-194">メタデータ検索は全体のコード ベースを検索し、完了に時間がかかる場合がありますが、コードにあるすべての検索用語の使用を返します。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-194">Metadata search will search the entire code base and may take some time to complete, but will return any use of the search term in code.</span></span> 

<span data-ttu-id="c6c7b-195">[![Del16](./media/del16.png)](./media/del16.png)</span><span class="sxs-lookup"><span data-stu-id="c6c7b-195">[![Del16](./media/del16.png)](./media/del16.png)</span></span> 

<span data-ttu-id="c6c7b-196">メソッド 2 および 3 はメタデータ検索に並行して使用できます。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-196">Methods two and three can be used in parallel to the metadata search.</span></span> <span data-ttu-id="c6c7b-197">デリゲートが定義されているクラスは、デリゲートまたはハンドラーの検索を絞り込む手段としても機能します。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-197">The class where a delegate is defined can also serve as a means to narrow down the search for a delegate or handler.</span></span> <span data-ttu-id="c6c7b-198">SubscribesTo キーワードには、デリゲートが定義されているクラス名が必要です。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-198">The SubscribesTo keyword requires the class name where the delegate was defined.</span></span> <span data-ttu-id="c6c7b-199">Visual Studio の 参照の検索 (クラス名の右クリック &gt; 参照の検索) により、クラスを参照するファイルの一覧が返されます。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-199">Visual Studio’s find references (right-click the class name &gt; find references) will return a list of files that reference the class.</span></span> <span data-ttu-id="c6c7b-200">このリストには、デリゲートが宣言されているクラス定義とそのクラスを参照するハンドラーの両方が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-200">This list will include both the class definition where the delegate is declared and the handler referencing the class.</span></span> <span data-ttu-id="c6c7b-201">クラス参照の検索は完全な方法ではなく、クラス参照によるいくつかの手動検索を必要とします。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-201">Finding class references is not a perfect method and will require some manual searching through class references.</span></span> <span data-ttu-id="c6c7b-202">ただし、少さいサブセットのファイルが生成され、メタデータ検索よりも早くなる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-202">However, it produces a smaller subset of files and can be faster than a metadata search.</span></span> 

<span data-ttu-id="c6c7b-203">[![Del17](./media/del17-1024x300.png)](./media/del17.png)</span><span class="sxs-lookup"><span data-stu-id="c6c7b-203">[![Del17](./media/del17-1024x300.png)](./media/del17.png)</span></span> 

<span data-ttu-id="c6c7b-204">クラス参照の検索と同様、すべての参照の検索は、SubscribesTo キーワードで行うことができます。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-204">Similar to finding class references, finding all references can be done on the SubscribesTo keyword.</span></span> <span data-ttu-id="c6c7b-205">結果リストには、すべての静的デリゲート ハンドラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-205">The resulting list will include all static delegate handlers.</span></span> <span data-ttu-id="c6c7b-206">この一覧を手動で移動することで、静的デリゲート ハンドラーを検索できます。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-206">Manually going through this list provides another means for finding static delegate handlers.</span></span> <span data-ttu-id="c6c7b-207">これは、SubscribesTo キーワードを使用しない動的に宣言された代理ハンドラを返しません。</span><span class="sxs-lookup"><span data-stu-id="c6c7b-207">This will not return dynamically declared delegate handlers that do not use the SubscribesTo keyword.</span></span> 

<span data-ttu-id="c6c7b-208">[![Del18](./media/del18-1024x328.png)](./media/del18.png)</span><span class="sxs-lookup"><span data-stu-id="c6c7b-208">[![Del18](./media/del18-1024x328.png)](./media/del18.png)</span></span>




