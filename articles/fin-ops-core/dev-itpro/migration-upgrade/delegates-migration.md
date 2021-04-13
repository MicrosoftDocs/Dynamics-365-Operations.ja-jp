---
title: コードの移行中にデリゲートを使用してモデル間の依存関係の解決
description: このトピックでは、デリゲート インスタンスとデリゲート ハンドラ間でコントラクトを定義する手段としてデリゲート メソッドがどのように機能するかについて説明します。
author: maertenm
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 27001
ms.assetid: 6640ae38-58f0-4a29-abca-5acd9489d45d
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ba8b156bf11df6e1271a5e44d748f6996166c699
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748409"
---
# <a name="solve-dependencies-among-models-by-using-delegates-during-code-migration"></a><span data-ttu-id="f756f-103">コードの移行中にデリゲートを使用してモデル間の依存関係の解決</span><span class="sxs-lookup"><span data-stu-id="f756f-103">Solve dependencies among models by using delegates during code migration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f756f-104">このトピックでは、デリゲート インスタンスとデリゲート ハンドラ間でコントラクトを定義する手段としてデリゲート メソッドがどのように機能するかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f756f-104">This topic explains how delegate methods serve as a means for defining a contract between the delegate instance and the delegate handler.</span></span>

<a name="overview"></a><span data-ttu-id="f756f-105">概要</span><span class="sxs-lookup"><span data-stu-id="f756f-105">Overview</span></span>
--------

<span data-ttu-id="f756f-106">Finance and Operations は、各モデルが個別のパッケージにある、複数のモデルに分割されます。</span><span class="sxs-lookup"><span data-stu-id="f756f-106">Finance and Operations is split into several models, with each model in separate package.</span></span> <span data-ttu-id="f756f-107">主要な 3 つのモデルは、アプリケーション プラットフォーム、アプリケーション基盤、アプリケーション スイートです。</span><span class="sxs-lookup"><span data-stu-id="f756f-107">The principal 3 models are Application Platform, Application Foundation, and Application Suite.</span></span> <span data-ttu-id="f756f-108">モデル分割を使用して、階層が作成されました。ここで上位のモデルは依存関係を持つことができ、下位のモデル内の要素にアクセスできますが、上位のモデルにはアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="f756f-108">With the model split, a hierarchy has been created where a higher model can take dependencies and access elements in the models below, but not in models above.</span></span> <span data-ttu-id="f756f-109">たとえば、この設定では、アプリケーション スイートはその要素、アプリケーション基盤の要素およびアプリケーション プラットフォームの要素にフル アクセスできます。</span><span class="sxs-lookup"><span data-stu-id="f756f-109">For example, in this setup, Application Suite has full access to its elements, Application Foundation’s elements, and Application Platform’s elements.</span></span> <span data-ttu-id="f756f-110">アプリケーション基準は、独自の要素とアプリケーション プラットフォームの要素にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="f756f-110">Application Foundation can access its own elements and those of Application Platform.</span></span> <span data-ttu-id="f756f-111">最後に、アプリケーション プラットフォームは独自の要素にのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="f756f-111">Finally, Application Platform can only access its own elements.</span></span> <span data-ttu-id="f756f-112">モデルとパッケージについては、 [モデル と パッケージ](../dev-tools/models.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f756f-112">To learn about models and packages, see [Models and packages](../dev-tools/models.md).</span></span>

<span data-ttu-id="f756f-113">[![Del1](./media/del1.jpg)](./media/del1.jpg)</span><span class="sxs-lookup"><span data-stu-id="f756f-113">[![Del1](./media/del1.jpg)](./media/del1.jpg)</span></span> 

<span data-ttu-id="f756f-114">モデルの分割には多くの利点がありますが、上位モデルで定義された要素にアクセスするとき問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="f756f-114">While the model split provides many benefits, it creates a problem when trying to access elements defined in higher models.</span></span> <span data-ttu-id="f756f-115">上位モデルの要素に下位モデルからアクセスするに、デリゲートが推奨されています。</span><span class="sxs-lookup"><span data-stu-id="f756f-115">Delegates are the recommended method for accessing elements in higher models from a lower model.</span></span> <span data-ttu-id="f756f-116">デリゲートは、デリゲート インスタンスが呼び出されると、互換性のある署名コードを持つハンドラーが実行されるという点で、イベントと非常によく似ています。</span><span class="sxs-lookup"><span data-stu-id="f756f-116">Delegates are very similar to events in that when a delegate instance is invoked, a handler with compatible signature code is executed.</span></span> <span data-ttu-id="f756f-117">これにより、ハンドラーである上位レイヤーコードが、デリゲート インスタンスである下位レイヤーコード (デリゲート インスタンス) によって呼び出されるようになります。</span><span class="sxs-lookup"><span data-stu-id="f756f-117">This permits higher layer code, the handler, to be called by lower layer code, the delegate instance.</span></span>

## <a name="create-delegates-and-handlers"></a><span data-ttu-id="f756f-118">委任およびハンドラーを作成します</span><span class="sxs-lookup"><span data-stu-id="f756f-118">Create delegates and handlers</span></span>
<span data-ttu-id="f756f-119">デリゲートの宣言には、次の 3 つが必要です。</span><span class="sxs-lookup"><span data-stu-id="f756f-119">A delegate declaration must have three things:</span></span>

-   <span data-ttu-id="f756f-120">委任キーワード</span><span class="sxs-lookup"><span data-stu-id="f756f-120">The delegate keyword</span></span>
-   <span data-ttu-id="f756f-121">無効タイプ</span><span class="sxs-lookup"><span data-stu-id="f756f-121">Type void</span></span>
-   <span data-ttu-id="f756f-122">空のメソッド</span><span class="sxs-lookup"><span data-stu-id="f756f-122">Empty method</span></span>

<span data-ttu-id="f756f-123">デリゲート メソッドは、デリゲート インスタンスとデリゲート ハンドラー間のコントラクトを定義する手段として機能します。</span><span class="sxs-lookup"><span data-stu-id="f756f-123">Delegate methods serve as a means for defining a contract between the delegate instance and the delegate handler.</span></span> <span data-ttu-id="f756f-124">デリゲートは、アクション自体を行ないません。</span><span class="sxs-lookup"><span data-stu-id="f756f-124">A delegate takes no action itself.</span></span> <span data-ttu-id="f756f-125">これは、void 型を持ち、メソッドにコードがないことによって適用されます。</span><span class="sxs-lookup"><span data-stu-id="f756f-125">This is enforced by having a void type and having no code in the method.</span></span> 

```xpp
delegate void applyDiscountDelegate(real _receiptTotal, EventHandlerResult _result)
{
}
```

<span data-ttu-id="f756f-126">メソッドに **SubscribesTo** キーワードを追加して、静的委任ハンドラーを作成します。</span><span class="sxs-lookup"><span data-stu-id="f756f-126">Adding the **SubscribesTo** keyword to a method creates a static delegate handler.</span></span> <span data-ttu-id="f756f-127">**SubscribesTo** にはデリゲートのクラス名、およびデリゲート メソッドの文字列名が必要です。</span><span class="sxs-lookup"><span data-stu-id="f756f-127">**SubscribesTo** requires the class name of the delegate, and the string name of the delegate method.</span></span> 

<span data-ttu-id="f756f-128">デリゲートが適切に処理されるには、デリゲート メソッドの宣言、デリゲート インスタンスおよびデリゲート ハンドラーに *同じ* メソッドの署名が必要です。</span><span class="sxs-lookup"><span data-stu-id="f756f-128">In order for a delegate to be properly handled, the delegate method declaration, the delegate instance, and the delegate handler must have the *same* method signature.</span></span> <span data-ttu-id="f756f-129">たとえば、次に示すデリゲート インスタンスには、2 つの入力が必要です。実数および EventHandlerResult で、上記のデリゲート宣言およびハンドラー署名と一致するものです。</span><span class="sxs-lookup"><span data-stu-id="f756f-129">For example, the delegate instance below takes two inputs, a real number and an EventHandlerResult, matching the delegate declaration and handler signatures above.</span></span> 

![static delegate ハンドラー](media/static-delegate-handler.png)

<span data-ttu-id="f756f-131">デリゲートに戻り値がないため、EventHandlerResult がパラメーターとして渡され、デリゲートが返された後に必要な結果値にアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="f756f-131">Due to the fact that delegates do not have a return value, an EventHandlerResult is passed as a parameter to provide access to the needed result value after the delegate has returned.</span></span> <span data-ttu-id="f756f-132">このトピックでは、SubscribesTo を使用する静的委任ハンドラーについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f756f-132">This topic focuses on static delegate handlers using the SubscribesTo.</span></span> <span data-ttu-id="f756f-133">Dynamics AX 2012 からのデリゲート機能が保持されます。</span><span class="sxs-lookup"><span data-stu-id="f756f-133">The delegate functionality from Dynamics AX 2012 remains.</span></span> <span data-ttu-id="f756f-134">[Dynamics AX 2012 で X++ デリゲートを使用する方法](https://blogs.msdn.com/b/x/archive/2011/08/02/how-to-use-x-delegates-in-dynamics-ax-2012.aspx) は Dynamics AX 2012 のデリゲートの概念について、Microsoft の開発者 Marcos Calderon が MSDN に投稿した素晴らしいブログです。</span><span class="sxs-lookup"><span data-stu-id="f756f-134">[How to use X++ Delegates in Dynamics AX 2012](https://blogs.msdn.com/b/x/archive/2011/08/02/how-to-use-x-delegates-in-dynamics-ax-2012.aspx) is a great blog post on MSDN by Microsoft developer Marcos Calderon on delegate concepts in Dynamics AX 2012.</span></span> <span data-ttu-id="f756f-135">これらの概念が引き続き適用されます。</span><span class="sxs-lookup"><span data-stu-id="f756f-135">These concepts still apply.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="f756f-136">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="f756f-136">Example scenarios</span></span>
### <a name="overlaying-an-existing-delegate"></a><span data-ttu-id="f756f-137">既存の委任のオーバーレイ</span><span class="sxs-lookup"><span data-stu-id="f756f-137">Overlaying an existing delegate</span></span>

<span data-ttu-id="f756f-138">デリゲートが必要な多くの場合、以前にオーバーレイされたコードは既に Microsoft によってデリゲート ハンドラーに移動されています。</span><span class="sxs-lookup"><span data-stu-id="f756f-138">In many cases where delegates are needed, the code that was formerly overlayed has already been moved to a delegate handler by Microsoft.</span></span> <span data-ttu-id="f756f-139">これらのインスタンスで、Microsoft は利用できるデリゲートを作成し、デリゲート ハンドラーで同様の方法でコードをオーバーレイできます。</span><span class="sxs-lookup"><span data-stu-id="f756f-139">In these instances, Microsoft created delegates that can be leveraged and the code can be overlayed in a similar manner in the delegate handler.</span></span> <span data-ttu-id="f756f-140">このシナリオでは、独立系ソフトウェア ベンダー (ISV) が、LogisticsEntityPostalAddressFormHandler クラスで showSalesTax() メソッドをオーバーレイした Dynamics AX 2012 R3 からコードを移行しています。</span><span class="sxs-lookup"><span data-stu-id="f756f-140">In this scenario, an Independent Software Vendor (ISV) is migrating code from Dynamics  AX 2012 R3 where they have overlayed the showSalesTax() method in the LogisticsEntityPostalAddressFormHandler class.</span></span> <span data-ttu-id="f756f-141">移行後に、CodeUpgrade プロジェクトは、*Your Solution*、*Microsoft AX 2012*、*Microsoft AX* セクションを使用する LogisticsEntityPostalAddressFormHandler が含まれ、showSalesTax() メソッドを解決します。</span><span class="sxs-lookup"><span data-stu-id="f756f-141">After migration, the CodeUpgrade project will contain the LogisticsEntityPostalAddressFormHandler with the *Your Solution*, *Microsoft AX 2012,* and *Microsoft AX* sections to resolve for the showSalesTax() method.</span></span> <span data-ttu-id="f756f-142">コメントされた Your Solution セクションには、売上税の表示を承認するための追加のテーブルを追加することによって、showSalesTax() メソッドがオーバーレイされたことが示されています。</span><span class="sxs-lookup"><span data-stu-id="f756f-142">The commented Your Solution section shows that the showSalesTax() method was overlayed by adding an additional table to approve showing sales tax from.</span></span> <span data-ttu-id="f756f-143">このオーバーレイは、赤で丸で囲まれた &lt;isv&gt; タグの間に表示されます。</span><span class="sxs-lookup"><span data-stu-id="f756f-143">This overlay is shown between the &lt;isv&gt; tags circled in red below.</span></span> 

<span data-ttu-id="f756f-144">[![4](./media/41.png)](./media/41.png)</span><span class="sxs-lookup"><span data-stu-id="f756f-144">[![4](./media/41.png)](./media/41.png)</span></span>

<span data-ttu-id="f756f-145">このオーバーレイを Dynamics AX 2012 のコードと比較するとき、これは単純な変更です。</span><span class="sxs-lookup"><span data-stu-id="f756f-145">When comparing this overlay with the code from Dynamics AX 2012, this is a simple change.</span></span> <span data-ttu-id="f756f-146">オーバーレイによって、switch ステートメントに追加のテーブルが追加されました。</span><span class="sxs-lookup"><span data-stu-id="f756f-146">The overlay has added an additional table to the switch statement.</span></span> 

<span data-ttu-id="f756f-147">[![5](./media/51.png)](./media/51.png)</span><span class="sxs-lookup"><span data-stu-id="f756f-147">[![5](./media/51.png)](./media/51.png)</span></span> 

<span data-ttu-id="f756f-148">ただし、Finance and Operations のセクションでは、Dynamics AX 2012 コード スニペットのいずれかと同じようには表示されません。</span><span class="sxs-lookup"><span data-stu-id="f756f-148">However, the section for Finance and Operations does not appear to resemble either of the Dynamics AX 2012 code snippets.</span></span> 

<span data-ttu-id="f756f-149">[![6](./media/61.png)](./media/61.png)</span><span class="sxs-lookup"><span data-stu-id="f756f-149">[![6](./media/61.png)](./media/61.png)</span></span> 

<span data-ttu-id="f756f-150">詳細な点検を行う際、コードはデリゲート メソッド showSalesTax\_delegate() を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f756f-150">Upon deeper inspection, the code is calling a delegate method, showSalesTax\_delegate().</span></span> 

<span data-ttu-id="f756f-151">[![this.showSalesTax\_delegate(this.getCallerRecord().TableId, result);](./media/showsalestax_delegate.png)](./media/showsalestax_delegate.png)</span><span class="sxs-lookup"><span data-stu-id="f756f-151">[![this.showSalesTax\_delegate(this.getCallerRecord().TableId, result);](./media/showsalestax_delegate.png)](./media/showsalestax_delegate.png)</span></span> 

<span data-ttu-id="f756f-152">デリゲートの使用は、コードが別の場所に移動されたことを意味します。</span><span class="sxs-lookup"><span data-stu-id="f756f-152">The use of a delegate implies that code has been moved to another location.</span></span> <span data-ttu-id="f756f-153">showSalesTax\_delegate() は、アプリケーション基準で宣言され、Application Suite で処理されました。</span><span class="sxs-lookup"><span data-stu-id="f756f-153">The showSalesTax\_delegate() has been declared in the Application Foundation and handled in the Application Suite.</span></span> <span data-ttu-id="f756f-154">移動されたコードを表示するには、デリゲート ハンドラを探します。</span><span class="sxs-lookup"><span data-stu-id="f756f-154">To view the code that has been moved, find the delegate handler.</span></span> <span data-ttu-id="f756f-155">**デリゲートとハンドラーの検索** セクションには、デリゲートとハンドラーを検索するメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="f756f-155">The **Finding Delegates and Handlers** section contains methods to locate delegates and handlers.</span></span> <span data-ttu-id="f756f-156">アプリケーション スイートでデリゲート ハンドラー メソッドを検索した後、showSalesTax() メソッドからから移動されたコードを参照します。</span><span class="sxs-lookup"><span data-stu-id="f756f-156">After finding the delegate handler method in the Application Suite, we see the code that has been moved from the showSalesTax() method.</span></span> <span data-ttu-id="f756f-157">Dynamics AX 2012 で適用されているオーバーレイされた同じ変更を、デリゲート ハンドラーに適用できます。</span><span class="sxs-lookup"><span data-stu-id="f756f-157">The same overlayered changes applied in Dynamics AX 2012 can be applied in the delegate handler.</span></span> 

<span data-ttu-id="f756f-158">[![委任とハンドラーのコード サンプルの検索](./media/findingdelegatesandhandles.png)](./media/findingdelegatesandhandles.png)</span><span class="sxs-lookup"><span data-stu-id="f756f-158">[![Finding delegates and handlers code sample](./media/findingdelegatesandhandles.png)](./media/findingdelegatesandhandles.png)</span></span> 

<span data-ttu-id="f756f-159">デリゲート ハンドラーで switch ステートメントに新しいテーブルを追加した後、コードは Dynamics AX 2012 の場合と同じように機能します。</span><span class="sxs-lookup"><span data-stu-id="f756f-159">After adding the new table to the switch statement in the delegate handler, the code will function as it did in Dynamics AX 2012.</span></span> 

<span data-ttu-id="f756f-160">[![ShowSalesTax メソッド コード](./media/showsalestaxmethod.png)](./media/showsalestaxmethod.png)</span><span class="sxs-lookup"><span data-stu-id="f756f-160">[![ShowSalesTax method code](./media/showsalestaxmethod.png)](./media/showsalestaxmethod.png)</span></span>

### <a name="adding-a-new-delegate"></a><span data-ttu-id="f756f-161">新しい委任の追加</span><span class="sxs-lookup"><span data-stu-id="f756f-161">Adding a new delegate</span></span>

<span data-ttu-id="f756f-162">このシナリオでは、アプリケーション スイートで作成された割引を考慮するために、アプリケーション基準に存在する既存の税計算方法を変更します。</span><span class="sxs-lookup"><span data-stu-id="f756f-162">In this scenario, we will modify an existing tax calculation method that resides in the Application Foundation to account for discounts created in the Application Suite.</span></span> <span data-ttu-id="f756f-163">Foundation レイヤーの次のクラスは、総額に基づいて税金を計算します。</span><span class="sxs-lookup"><span data-stu-id="f756f-163">The following class in the Foundation layer calculates the tax based on the gross total.</span></span> 

![SimpleTax クラス](media/simple-tax.png)

<span data-ttu-id="f756f-165">アプリケーション スイートでは、現在の割引を含む ProductDiscount クラスを追加することで割引の概念を導入しました。</span><span class="sxs-lookup"><span data-stu-id="f756f-165">In the Application Suite, we have introduced the notion of discounts by adding a ProductDiscount class that contains the current discount.</span></span> 

<span data-ttu-id="f756f-166">[![11](./media/112.png)](./media/112.png)</span><span class="sxs-lookup"><span data-stu-id="f756f-166">[![11](./media/112.png)](./media/112.png)</span></span> 

<span data-ttu-id="f756f-167">Foundation レイヤー下部にある TaxCalculator クラスには、Suite レイヤーの DiscountRate へのアクセス権がないため、委任を使用して受領合計を更新し、税計算に使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f756f-167">The TaxCalculator class, in the lower Foundation layer, does not have access to the DiscountRate in the Suite layer and must use a delegate to update receipt total to use in the tax calculation.</span></span> <span data-ttu-id="f756f-168">SimpleTax クラスでは、署名のハンドラーによって必要な状態情報とともにデリゲート メソッド applyDiscountDelegate を作成します。</span><span class="sxs-lookup"><span data-stu-id="f756f-168">In the SimpleTax class, we create a delegate method, applyDiscountDelegate, with the state information that is needed by the handler in the signature.</span></span> <span data-ttu-id="f756f-169">デリゲート メソッドは、デリゲート インスタンスとハンドラー間のコントラクトを定義することが唯一の目的のため、常に空です。</span><span class="sxs-lookup"><span data-stu-id="f756f-169">A delegate method is always empty because its only purpose is to define the contract between the delegate instance and the handler.</span></span> 

```xpp
delegate void applyDiscountDelegate(real _receiptTotal, EventHandlerResult _result)
{
} 
```

> [!NOTE]
> <span data-ttu-id="f756f-170">デリゲートの宣言、デリゲート インスタンスおよびデリゲート ハンドラーの署名は一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f756f-170">The signature for the delegate declaration, the delegate instance, and the delegate handler must match.</span></span> <span data-ttu-id="f756f-171">デリゲート ハンドラーを実行するコード内の箇所に、デリゲートのインスタンスを作成することが必要になりました。</span><span class="sxs-lookup"><span data-stu-id="f756f-171">We now have to create an instance of the delegate at the point in the code where we would like the delegate handler to be run.</span></span> <span data-ttu-id="f756f-172">&lt;isv&gt; タグ間での変更は追加されたコードを表します。</span><span class="sxs-lookup"><span data-stu-id="f756f-172">The changes in between the &lt;isv&gt; tags represent the added code.</span></span> 

![calculateTotalTax method](media/calculate-total-tax.png)

<span data-ttu-id="f756f-174">デリゲートの環境が整い、割引情報へのアクセス権を持つアプリケーション スイート レイヤーに、ハンドラー メソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="f756f-174">With the delegate in place, we now add a handler method in the Application Suite layer that has access to the discount information.</span></span> 

![applyDiscountDelegateHandler メソッド](media/apply-discount-delegate-handler.png)

<span data-ttu-id="f756f-176">SubscribesTo キーワードを使用して、applyDiscountDelegateHandler メソッドを applyDiscountDelegate デリゲートにハンドラーとして結合します。</span><span class="sxs-lookup"><span data-stu-id="f756f-176">Using the SubscribesTo keyword, we tie the applyDiscountDelegateHandler method as a handler to the applyDiscountDelegate delegate.</span></span>

> [!NOTE]
> <span data-ttu-id="f756f-177">デリゲートごとに複数のハンドラーが存在する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f756f-177">There can be more than one handler per delegate.</span></span> <span data-ttu-id="f756f-178">ハンドラー メソッドの処理には、定義された順序は **ありません**。</span><span class="sxs-lookup"><span data-stu-id="f756f-178">There is **not** a defined order in the processing of handler methods.</span></span> <span data-ttu-id="f756f-179">注文が重要な場合は、代行ハンドラーのペアは一緒に連鎖する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f756f-179">If order is important, delegate handler pairs should be chained together.</span></span> <span data-ttu-id="f756f-180">以下の最終クラスでは、calculateTotalTax() メソッドが実行されるとき、applyDiscountDelegate が起動および処理され、receiptTotal が更新されて正確な税計算が提供されます。</span><span class="sxs-lookup"><span data-stu-id="f756f-180">With the final classes below, when the calculateTotalTax() method is run, the applyDiscountDelegate is fired and handled, updating the receiptTotal to provide an accurate tax calculation.</span></span>

#### <a name="full-code"></a><span data-ttu-id="f756f-181">完全なコード</span><span class="sxs-lookup"><span data-stu-id="f756f-181">Full Code</span></span>

##### <a name="simpletax-class-in-the-application-foundation-layer"></a><span data-ttu-id="f756f-182">Application Foundation Layer の SimpleTax クラス</span><span class="sxs-lookup"><span data-stu-id="f756f-182">SimpleTax class in the Application Foundation Layer</span></span>

![SimpleTax クラス](media/simple-tax-full-code.png)

##### <a name="productdiscount-class-in-the-application-suite-layer"></a><span data-ttu-id="f756f-184">アプリケーション スイート レイヤーの ProductDiscount クラス</span><span class="sxs-lookup"><span data-stu-id="f756f-184">ProductDiscount class in the Application Suite layer</span></span>

![ProductDiscount クラス](media/product-discount-full-code.png)

## <a name="find-delegates-and-handlers"></a><span data-ttu-id="f756f-186">委任およびハンドラーを検索します</span><span class="sxs-lookup"><span data-stu-id="f756f-186">Find delegates and handlers</span></span>
<span data-ttu-id="f756f-187">デリゲートとハンドラーを見つける主要な 3 つの方法があります</span><span class="sxs-lookup"><span data-stu-id="f756f-187">There are three key ways to find delegates and handlers</span></span>

-   <span data-ttu-id="f756f-188">メタデータ検索</span><span class="sxs-lookup"><span data-stu-id="f756f-188">Metadata search</span></span>
-   <span data-ttu-id="f756f-189">クラス参照</span><span class="sxs-lookup"><span data-stu-id="f756f-189">Class references</span></span>
-   <span data-ttu-id="f756f-190">SubscribesTo 参照</span><span class="sxs-lookup"><span data-stu-id="f756f-190">SubscribesTo references</span></span>

<span data-ttu-id="f756f-191">[メタデータ検索と Visual Studio](../dev-tools/metadata-search-visual-studio.md) ページで説明されているメタデータ検索ツールは、デリゲート、またはそのハンドラーを検索するための優れた方法です。</span><span class="sxs-lookup"><span data-stu-id="f756f-191">The Metadata search tool, described on the [Metadata search in Visual Studio](../dev-tools/metadata-search-visual-studio.md) page, is the best way to find either delegates or their handlers.</span></span> <span data-ttu-id="f756f-192">Visual Studio で、 **Dynamics 365 &gt; メタデータ検索** に移動してメタデータ検索ツールを開きます。</span><span class="sxs-lookup"><span data-stu-id="f756f-192">In Visual Studio, go to **Dynamics 365 &gt; Metadata Search** to open the metadata search tool.</span></span> 

<span data-ttu-id="f756f-193">[![Del15](./media/del15.png)](./media/del15.png)</span><span class="sxs-lookup"><span data-stu-id="f756f-193">[![Del15](./media/del15.png)](./media/del15.png)</span></span> 

<span data-ttu-id="f756f-194">検索フィールドに、「code:&lt;デリゲート名&gt;」を入力して検索をコードに制限し、デリゲート名の使用を見つけると、デリゲートとハンドラーの両方を返します。</span><span class="sxs-lookup"><span data-stu-id="f756f-194">In the search field, type “code:&lt;delegate name&gt;” which will restrict the search to code and find any use of the delegate name, returning both the delegate and handler.</span></span> <span data-ttu-id="f756f-195">メタデータ検索は全体のコード ベースを検索し、完了に時間がかかる場合がありますが、コードにあるすべての検索用語の使用を返します。</span><span class="sxs-lookup"><span data-stu-id="f756f-195">Metadata search will search the entire code base and may take some time to complete, but will return any use of the search term in code.</span></span> 

<span data-ttu-id="f756f-196">[![Del16](./media/del16.png)](./media/del16.png)</span><span class="sxs-lookup"><span data-stu-id="f756f-196">[![Del16](./media/del16.png)](./media/del16.png)</span></span> 

<span data-ttu-id="f756f-197">メソッド 2 および 3 はメタデータ検索に並行して使用できます。</span><span class="sxs-lookup"><span data-stu-id="f756f-197">Methods two and three can be used in parallel to the metadata search.</span></span> <span data-ttu-id="f756f-198">デリゲートが定義されているクラスは、デリゲートまたはハンドラーの検索を絞り込む手段としても機能します。</span><span class="sxs-lookup"><span data-stu-id="f756f-198">The class where a delegate is defined can also serve as a means to narrow down the search for a delegate or handler.</span></span> <span data-ttu-id="f756f-199">SubscribesTo キーワードには、デリゲートが定義されているクラス名が必要です。</span><span class="sxs-lookup"><span data-stu-id="f756f-199">The SubscribesTo keyword requires the class name where the delegate was defined.</span></span> <span data-ttu-id="f756f-200">Visual Studio の 参照の検索 (クラス名の右クリック &gt; 参照の検索) により、クラスを参照するファイルの一覧が返されます。</span><span class="sxs-lookup"><span data-stu-id="f756f-200">Visual Studio’s find references (right-click the class name &gt; find references) will return a list of files that reference the class.</span></span> <span data-ttu-id="f756f-201">このリストには、デリゲートが宣言されているクラス定義とそのクラスを参照するハンドラーの両方が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f756f-201">This list will include both the class definition where the delegate is declared and the handler referencing the class.</span></span> <span data-ttu-id="f756f-202">クラス参照の検索は完全な方法ではなく、クラス参照によるいくつかの手動検索を必要とします。</span><span class="sxs-lookup"><span data-stu-id="f756f-202">Finding class references is not a perfect method and will require some manual searching through class references.</span></span> <span data-ttu-id="f756f-203">ただし、少さいサブセットのファイルが生成され、メタデータ検索よりも早くなる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f756f-203">However, it produces a smaller subset of files and can be faster than a metadata search.</span></span> 

<span data-ttu-id="f756f-204">[![Del17](./media/del17-1024x300.png)](./media/del17.png)</span><span class="sxs-lookup"><span data-stu-id="f756f-204">[![Del17](./media/del17-1024x300.png)](./media/del17.png)</span></span> 

<span data-ttu-id="f756f-205">クラス参照の検索と同様、すべての参照の検索は、SubscribesTo キーワードで行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f756f-205">Similar to finding class references, finding all references can be done on the SubscribesTo keyword.</span></span> <span data-ttu-id="f756f-206">結果リストには、すべての静的デリゲート ハンドラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f756f-206">The resulting list will include all static delegate handlers.</span></span> <span data-ttu-id="f756f-207">この一覧を手動で移動することで、静的デリゲート ハンドラーを検索できます。</span><span class="sxs-lookup"><span data-stu-id="f756f-207">Manually going through this list provides another means for finding static delegate handlers.</span></span> <span data-ttu-id="f756f-208">これは、SubscribesTo キーワードを使用しない動的に宣言された代理ハンドラを返しません。</span><span class="sxs-lookup"><span data-stu-id="f756f-208">This will not return dynamically declared delegate handlers that do not use the SubscribesTo keyword.</span></span> 

<span data-ttu-id="f756f-209">[![Del18](./media/del18-1024x328.png)](./media/del18.png)</span><span class="sxs-lookup"><span data-stu-id="f756f-209">[![Del18](./media/del18-1024x328.png)](./media/del18.png)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]