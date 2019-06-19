---
title: カスタマイズをオフにして機能を廃止
description: この記事では、モデルのカスタマイズを無効にするプロセスについて説明します。 このプロセスに従うことで、オーバーレイに対して不適格となります。 開発者は引き続きそのモデルを拡張することができます。 この記事では、古い形式の機能を廃止する方法についても説明します。
author: pvillads
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 89593
ms.assetid: f3df4b82-84d9-401e-8d7f-cfd42772621c
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 284a1ab2b1cfb243c9a25e6b6927977eaa82a49b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544135"
---
# <a name="turn-off-model-customization-and-deprecate-functionality"></a><span data-ttu-id="abd76-106">カスタマイズをオフにして機能を廃止</span><span class="sxs-lookup"><span data-stu-id="abd76-106">Turn off model customization and deprecate functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="abd76-107">この記事では、モデルのカスタマイズを無効にするプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="abd76-107">This article describes the process of disabling customization of a model.</span></span> <span data-ttu-id="abd76-108">このプロセスに従うことで、オーバーレイに対して不適格となります。</span><span class="sxs-lookup"><span data-stu-id="abd76-108">By following this process, you make it ineligible for over-layering.</span></span> <span data-ttu-id="abd76-109">開発者は引き続きそのモデルを拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="abd76-109">Developers will still be able to extend that model.</span></span> <span data-ttu-id="abd76-110">この記事では、古い形式の機能を廃止する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="abd76-110">This article also describes how you can deprecate obsolete functionality.</span></span>

<span data-ttu-id="abd76-111">通常、他のモデルに依存するモデルでアプリケーションを構築します。</span><span class="sxs-lookup"><span data-stu-id="abd76-111">Typically, you build an application in models that depend on other models.</span></span> <span data-ttu-id="abd76-112">少なくとも、モデルは提供されているアプリケーション プラットフォーム モデルによって異なります。</span><span class="sxs-lookup"><span data-stu-id="abd76-112">At the very least, your models will depend on the Application Platform model that is provided.</span></span> <span data-ttu-id="abd76-113">Microsoft Dynamics 365 for Finance and Operations は、Microsoft Azure クラウド プラットフォーム上で実行されます。</span><span class="sxs-lookup"><span data-stu-id="abd76-113">Microsoft Dynamics 365 for Finance and Operations runs on the Microsoft Azure cloud platform.</span></span> <span data-ttu-id="abd76-114">つまり、Microsoft によって管理されているデータ センターでオフプレミスで実行されます。</span><span class="sxs-lookup"><span data-stu-id="abd76-114">In other words, it runs off-premises, in data centers that are managed by Microsoft.</span></span> <span data-ttu-id="abd76-115">基本的なモデルでは多数の仕入先からの変更をサポートできないため、アプリケーションはこれらのモデルのコンポーネントを重層化することができません。</span><span class="sxs-lookup"><span data-stu-id="abd76-115">Because we can’t support changes from a large number of vendors in the fundamental models, your applications can no longer over-layer artifacts in those models.</span></span> <span data-ttu-id="abd76-116">したがって、アプリケーションをビルドするには、オーバーレイの代わりに拡張機能を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="abd76-116">Therefore, to build your applications, you must use extensions instead of over-layering.</span></span> <span data-ttu-id="abd76-117">依存しているモデルのすべてのコンポーネントは、ドキュメント化のために利用可能ですが、他の人の知的財産をコンパイラし、クラウドで実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="abd76-117">Even though all the artifacts in the models that you depend on are available for documentation purposes, you can’t compile someone else’s intellectual property and run it in the cloud.</span></span>

## <a name="locking-customizations"></a><span data-ttu-id="abd76-118">カスタマイズのロック</span><span class="sxs-lookup"><span data-stu-id="abd76-118">Locking customizations</span></span>
<span data-ttu-id="abd76-119">オーバーレイヤーから拡張にモデルを移行するには、次の 3 つの手順が必要です。</span><span class="sxs-lookup"><span data-stu-id="abd76-119">Transitioning a model from over-layering to extensions involves three steps:</span></span>

1.  <span data-ttu-id="abd76-120">超過レイヤーのインスタンスが警告としてマークされるプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="abd76-120">You set a property that causes instances of over-layering to be flagged as warnings.</span></span> <span data-ttu-id="abd76-121">このステップは、「ソフトロック」と呼ばれることもあります。</span><span class="sxs-lookup"><span data-stu-id="abd76-121">This step is sometimes known as “soft-locking.”</span></span>
2.  <span data-ttu-id="abd76-122">重層化ではなく、拡張機能を使用して、警告を弱体化できる期間があります。</span><span class="sxs-lookup"><span data-stu-id="abd76-122">You have a period when you can burn down the warnings by using extensions instead of over-layering.</span></span>
3.  <span data-ttu-id="abd76-123">すべての警告を解決したときは、コンパイルの失敗の原因となるハード エラーをオーバーレイするときです。</span><span class="sxs-lookup"><span data-stu-id="abd76-123">When you have resolved all the warnings, it’s time to make over-layering a hard error that causes compilation to fail.</span></span> <span data-ttu-id="abd76-124">このステップは「ハードロック」と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="abd76-124">This step is known as “hard-locking.”</span></span> <span data-ttu-id="abd76-125">モデルがハードロックされていると、オーバーレイするために必要なツールをそのモデルに使用できません。</span><span class="sxs-lookup"><span data-stu-id="abd76-125">When a model is hard-locked, the tooling that is required for over-layering can’t be used for that model.</span></span> <span data-ttu-id="abd76-126">また、指定されたパッケージに複数のモデルを持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="abd76-126">Additionally, you can’t have more than one model in a given package.</span></span>

<span data-ttu-id="abd76-127">現在、カスタマイズを無効にするプロパティを操作するために使用できるツールはありません。</span><span class="sxs-lookup"><span data-stu-id="abd76-127">Currently, there is no tooling that you can use to manipulate the property that disables customizations.</span></span> <span data-ttu-id="abd76-128">代わりに、次の例に示すように**カスタマイズ** XML 要素をモデル記述子ファイルに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="abd76-128">Instead, you must add the **Customization** XML element to the model descriptor file, as shown in the following example.</span></span> <span data-ttu-id="abd76-129">モデル記述子ファイルは ...\\&lt;packages&gt;\\&lt;package name&gt;\\Descriptor\\&lt;model name&gt;.xml で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="abd76-129">You can find the model descriptor file at ...\\&lt;packages&gt;\\&lt;package name&gt;\\Descriptor\\&lt;model name&gt;.xml.</span></span>

    <?xml version="1.0" encoding="utf-8"?>
    <AxModelInfo xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
    <Customization>DoNotAllow</Customization>
    <Description>My cool locked application</Description>
    ...
    <</AxModelInfo>

<span data-ttu-id="abd76-130">カスタマイズ設定には次の 3 つのレベルがあります。</span><span class="sxs-lookup"><span data-stu-id="abd76-130">There are three levels of customization settings:</span></span>

-   <span data-ttu-id="abd76-131">**カスタマイズの許可** - 場合は、**カスタマイズ**要素が省略されている場合、または提供されていても**許可**というテキストが内部で使用されている場合、制限はありません。</span><span class="sxs-lookup"><span data-stu-id="abd76-131">**Allow customizations** – If the **Customization** element is omitted, or if it’s provided but the text **Allow** is used inside it, there are no restrictions.</span></span>
-   <span data-ttu-id="abd76-132">**ソフト ロック** ソフト ロックが必要な場合、**カスタマイズ** 要素内の **AllowAndWarn** というテキストを使用してください。</span><span class="sxs-lookup"><span data-stu-id="abd76-132">**Soft-locking** – If you require soft-locking, use the text **AllowAndWarn** inside the **Customization** element.</span></span>
-   <span data-ttu-id="abd76-133">**確定ロック** – モデルのカスタマイズを無効にするには、前の例に示すように、**カスタマイズ**要素内に **DoNotAllow** というテキストを使用します。</span><span class="sxs-lookup"><span data-stu-id="abd76-133">**Hard-locking** – To disable customization of the model, use the text **DoNotAllow** inside the **Customization** element, as shown in the preceding example.</span></span>

<span data-ttu-id="abd76-134">**注記:** 記述子ファイル内の要素は、アルファベット順に一覧表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="abd76-134">**Note:** Elements in the descriptor file must be listed in alphabetical order.</span></span>

## <a name="backward-compatibility-of-the-platform"></a><span data-ttu-id="abd76-135">プラットフォームの下位互換性</span><span class="sxs-lookup"><span data-stu-id="abd76-135">Backward compatibility of the platform</span></span>
<span data-ttu-id="abd76-136">より新しいバージョンの依存プラットフォーム モデルがインストールされていても、アプリケーションを実行し続ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="abd76-136">There is a requirement that your application must continue to run even if a newer version of a dependent platform model is installed.</span></span> <span data-ttu-id="abd76-137">したがって、これらのプラットフォーム モデルで行ったすべての変更に対して、後方互換性のための厳しい要件を適用します。</span><span class="sxs-lookup"><span data-stu-id="abd76-137">Therefore, we enforce strict requirements for backward compatibility on all the changes that we make in those platform models.</span></span> <span data-ttu-id="abd76-138">次の例を通して、この点を明確にできます。</span><span class="sxs-lookup"><span data-stu-id="abd76-138">We can clarify this point through an example.</span></span> <span data-ttu-id="abd76-139">この例では、次のクラスを含むベース モデル M があります。</span><span class="sxs-lookup"><span data-stu-id="abd76-139">For this example, you have a base model M that has the following class.</span></span>

    public void DoSomething(int arg)
    {
        // Do great stuff
    }

<span data-ttu-id="abd76-140">モデル M に依存するモデルでは、**DoSomething** クラスが提供するすべての便利な機能を活用したいと考えるでしょう。</span><span class="sxs-lookup"><span data-stu-id="abd76-140">In your model that depends on model M, you want to take advantage of all the great functionality that the **DoSomething** class offers.</span></span> <span data-ttu-id="abd76-141">したがって、次のコードがあります。</span><span class="sxs-lookup"><span data-stu-id="abd76-141">Therefore, you have the following code.</span></span>

    {
        var c = new SomeClass();
        c.DoSomething(42);
    }

<span data-ttu-id="abd76-142">後で、仕入先 (Microsoft など) が依存するモデル (モデル M) の新しく更新されたバージョンをリリースします。</span><span class="sxs-lookup"><span data-stu-id="abd76-142">Later, your vendor (perhaps Microsoft) releases a new, updated version of the model that you depend on (model M).</span></span> <span data-ttu-id="abd76-143">このモデルがリリースされるときに、再コンパイルなしで実行する必要があるため、パブリック インターフェイスをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="abd76-143">When this model is released, we must support the public interface, because things must run without recompilation.</span></span> <span data-ttu-id="abd76-144">次のように、別のパラメーターを追加してメソッド シグネチャを変更したとします。</span><span class="sxs-lookup"><span data-stu-id="abd76-144">Suppose that we changed the method signature by adding another parameter, as shown here.</span></span>

    public void DoSomething(int arg, str anotherArg)
    {
        // Do greater stuff
    }

<span data-ttu-id="abd76-145">この場合、アプリを中断します。</span><span class="sxs-lookup"><span data-stu-id="abd76-145">In this case, we break the app.</span></span> <span data-ttu-id="abd76-146">コールで前提となるパラメーター プロファイルが呼び出し先のパラメーター プロファイルと同じではないため、共通言語ランタイム (CLR) はメソッドを呼び出すことができません (呼び出しコードは 1 つのパラメーターが提供しましたが、現在は 2 つのパラメーターが必要です)。</span><span class="sxs-lookup"><span data-stu-id="abd76-146">The common language runtime (CLR) can’t call the method, because the parameter profile that is assumed in the call isn’t the same as the parameter profile of the callee (the calling code provided one parameter, but two are now required).</span></span> <span data-ttu-id="abd76-147">したがって、公的に消費可能なものを制限することは良い考えです。</span><span class="sxs-lookup"><span data-stu-id="abd76-147">Therefore, it’s a good idea to limit what is publicly consumable.</span></span> <span data-ttu-id="abd76-148">内容がプライベートである場合は、モデルの外部から誰も使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="abd76-148">If something is private, nobody can use it from outside your model.</span></span> <span data-ttu-id="abd76-149">ただし、コンポーネントを内部にするというオプションもあります。</span><span class="sxs-lookup"><span data-stu-id="abd76-149">However, another option is to make the artifact internal.</span></span> <span data-ttu-id="abd76-150">**内部**モディファイアーをクラスまたはメソッドに適用する場合、コンポーネントはモデルの内部でのみ表示され、外部からアクセスされることはありません。</span><span class="sxs-lookup"><span data-stu-id="abd76-150">If you apply the **internal** modifier to a class or method, the artifact is visible only inside your model and can’t be reached from the outside.</span></span> <span data-ttu-id="abd76-151">基本的に、モデルの外部からは、内部でもプライベートでもないものが使用されると想定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="abd76-151">Essentially, you must assume that anything that isn’t internal or private will be used from outside your model.</span></span> <span data-ttu-id="abd76-152">したがって、永続的にサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="abd76-152">Therefore, you must support it forever.</span></span> <span data-ttu-id="abd76-153">絶対にパブリックまたは保護済みにする必要がある場合を除き、パブリックまたは保護済みにせずに、インターフェイスを使用して、モデルの境界の外部にある関係のない実装の詳細を非表示にします。</span><span class="sxs-lookup"><span data-stu-id="abd76-153">Never make anything public or protected unless it absolutely must be public or protected, and use interfaces to hide implementation details that aren’t relevant outside the boundary of your model.</span></span> <span data-ttu-id="abd76-154">内部の可視性指定子でメタデータ (コードとは逆に) をマークする方法はありません。</span><span class="sxs-lookup"><span data-stu-id="abd76-154">There is no way to mark metadata (as opposed to code) with the internal visibility specifier.</span></span>

## <a name="testing-internal-functionality"></a><span data-ttu-id="abd76-155">内部機能のテスト</span><span class="sxs-lookup"><span data-stu-id="abd76-155">Testing internal functionality</span></span>
<span data-ttu-id="abd76-156">モデルの表面積を制限することによって、カスタマイズを許可しないモデルで問題を解決できるようになり、アプリケーションが円滑に実行されることを保証します。</span><span class="sxs-lookup"><span data-stu-id="abd76-156">By limiting the surface area of your model, you help guarantee that you will be able to fix issues in your models that do not allow customizations, and that the application will run smoothly.</span></span> <span data-ttu-id="abd76-157">しかし、内部化することで、コードをテストする能力が制限されてしまうと主張するかもしれません。</span><span class="sxs-lookup"><span data-stu-id="abd76-157">However, you might argue that, by making things internal, you limit the ability to test your code.</span></span> <span data-ttu-id="abd76-158">この状況を解決するには、テストするパッケージをテスト パッケージに通知します。</span><span class="sxs-lookup"><span data-stu-id="abd76-158">To remedy this situation, you can inform your test packages about the packages that they should test.</span></span> <span data-ttu-id="abd76-159">つまり、テスト パッケージは内部の項目にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="abd76-159">In other words, the test packages can access internal things.</span></span> <span data-ttu-id="abd76-160">このソリューションを実装するには、次の例のように記述子ファイルを編集します。</span><span class="sxs-lookup"><span data-stu-id="abd76-160">To implement this solution, you edit the descriptor file, as shown in the following example.</span></span>

    <?xml version="1.0" encoding="utf-8"?>
    <AxModelInfo xmlns:i=http://www.w3.org/2001/XMLSchema-instance>
    <InternalsVisibleTo xmlns:d2p1="http://schemas.microsoft.com/2003/10/Serialization/Arrays">
    <d2p1:string>ExternalPackageName</d2p1:string>
    </InternalsVisibleTo>
    ...
    </AxModelInfo>

<span data-ttu-id="abd76-161">**InternalsVisibleTo** 要素に含めることにより、任意の数の外部パッケージを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="abd76-161">You can provide any number of external packages by including them in the **InternalsVisibleTo** element.</span></span> <span data-ttu-id="abd76-162">この情報は、テスト コードを含むパッケージではなく、テストするコードを含むパッケージに提供されます。</span><span class="sxs-lookup"><span data-stu-id="abd76-162">This information is provided for the package that contains the code to test, not for the package that contains the testing code.</span></span> <span data-ttu-id="abd76-163">つまり、パッケージは情報を共有する人物を決定します。</span><span class="sxs-lookup"><span data-stu-id="abd76-163">In other words, the package determines who it shares information with.</span></span> <span data-ttu-id="abd76-164">**注記:** **AxModelInfo** の下の要素はアルファベット順でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="abd76-164">**Note:** The elements under **AxModelInfo** must be in alphabetical order.</span></span>

## <a name="deprecating-functionality"></a><span data-ttu-id="abd76-165">非推奨機能</span><span class="sxs-lookup"><span data-stu-id="abd76-165">Deprecating functionality</span></span>
### <a name="deprecating-methods"></a><span data-ttu-id="abd76-166">非推奨メソッド</span><span class="sxs-lookup"><span data-stu-id="abd76-166">Deprecating methods</span></span>

<span data-ttu-id="abd76-167">場合によっては、パブリックなソース コードをサポートする必要がなくなります。</span><span class="sxs-lookup"><span data-stu-id="abd76-167">Sometimes, you no longer want to support source code that is public.</span></span> <span data-ttu-id="abd76-168">先に述べたように、コンポーネントに依存するユーザーがいる可能性があるため、コンポーネントがプライベートまたは内部でない限り、コンポーネントをコードから削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="abd76-168">As we mentioned earlier, you should not remove an artifact from the code unless that artifact is private or internal, because there might be users who rely on it.</span></span> <span data-ttu-id="abd76-169">代わりに、**SysObsoleteAttribute** 属性を使用して、消費者がそのコンポーネントを使用できないように指定できます。</span><span class="sxs-lookup"><span data-stu-id="abd76-169">Instead, you can use the **SysObsoleteAttribute** attribute to specify that consumers should no longer use that artifact.</span></span> <span data-ttu-id="abd76-170">次の 2 つのフェーズで古い形式としてマークすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="abd76-170">We recommend that you mark things as obsolete in two phases:</span></span>

1.  <span data-ttu-id="abd76-171">成果物の使用を警告としてマークすることを指定します。</span><span class="sxs-lookup"><span data-stu-id="abd76-171">Specify that using the artifact is flagged as a warning.</span></span>
2.  <span data-ttu-id="abd76-172">1 つまたは複数のリリース サイクルの後、コンポーネントを使用してエラーを発生させます。</span><span class="sxs-lookup"><span data-stu-id="abd76-172">After one or more release cycles, make using the artifact an error.</span></span>

<span data-ttu-id="abd76-173">次の例では、**DoSomething** メソッドはモデルの最初のリリースで定義されています。</span><span class="sxs-lookup"><span data-stu-id="abd76-173">In the following example, the **DoSomething** method is defined in the first release of a model.</span></span>

    class SomeApi
    {
        void DoSomething()
        {
            // Do great stuff
        }
    }

<span data-ttu-id="abd76-174">2 回目のリリースで、目標を達成するよりよい方法があることを見つけました。</span><span class="sxs-lookup"><span data-stu-id="abd76-174">In the second release, you’ve determined that there is a better way to accomplish something.</span></span> <span data-ttu-id="abd76-175">したがって、新しい実装を追加し、古い実装を廃止します。</span><span class="sxs-lookup"><span data-stu-id="abd76-175">Therefore, you add the new implementation and make the old implementation obsolete.</span></span>

    class SomeApi
    {
        [SysObsolete("Use DoSomethingNew instead", false)]
        void DoSomething()
        {
            // Do great stuff
        }

        void DoSomethingNew()
        {
        }
    }

<span data-ttu-id="abd76-176">既存のすべての顧客は引き続き旧バージョンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="abd76-176">All your existing customers will continue to call the old version.</span></span> <span data-ttu-id="abd76-177">この状況は適切ですが、顧客は新しいバージョンの利点を活用できません。</span><span class="sxs-lookup"><span data-stu-id="abd76-177">This situation is fine, but the customers won’t be able to take advantage of the benefits of the new version.</span></span> <span data-ttu-id="abd76-178">クラスに対してコード化するユーザーは、**SysObsolete** 属性の引数で指定したメッセージと共にビルド警告を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="abd76-178">Anyone who codes against your class will receive a build warning together with the message that you provided in the **SysObsolete** attribute argument.</span></span> <span data-ttu-id="abd76-179">多くの場合、これらのクライアントは新たなメソッドを使用するようにコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="abd76-179">Presumably, these clients will update their code so that it uses the new method.</span></span> <span data-ttu-id="abd76-180">時間の経過と共に、より多くのクライアントが新しいバージョンに移行します。</span><span class="sxs-lookup"><span data-stu-id="abd76-180">As time passes, more clients will move to the new version.</span></span> <span data-ttu-id="abd76-181">したがって、ある時点では、メソッドに対してハード エラーをコーディングするのが理にかなっています。</span><span class="sxs-lookup"><span data-stu-id="abd76-181">Therefore, at some point, it will make sense for you to make coding against the method a hard error.</span></span>

    class SomeApi
    {
        [SysObsolete("Use DoSomethingNew instead", true)]
        void DoSomething()
        {
            // Do great stuff
        }

        void DoSomethingNew()
        {
        }
    }

<span data-ttu-id="abd76-182">改めて、前述の理由から、古いメソッドがプライベートまたは内部にならなかったので、完全に削除することができません。</span><span class="sxs-lookup"><span data-stu-id="abd76-182">Again, for the reasons that we mentioned earlier, you may never be able to get rid of the old method completely, because it was not made private or internal.</span></span>

### <a name="deprecating-metadata"></a><span data-ttu-id="abd76-183">非推奨メタデータ</span><span class="sxs-lookup"><span data-stu-id="abd76-183">Deprecating metadata</span></span>

<span data-ttu-id="abd76-184">モデル要素 (テーブル、データ エンティティ、EDT、列挙、など) の非推奨に関しては、すべてのモデル要素タイプで利用可能なプロパティの **IsObsolete** を使用します。</span><span class="sxs-lookup"><span data-stu-id="abd76-184">For deprecating model elements (tables, data entities, EDTs, Enums, ...etc.), use the property **IsObsolete** that is available on all model element types.</span></span> <span data-ttu-id="abd76-185">**IsObsolete** は、表、ビュー、およびデータ エンティティ フィールドでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="abd76-185">**IsObsolete** is also available on table, view, and data entity fields.</span></span> <span data-ttu-id="abd76-186">**IsObsolete** を「はい」に設定すると、その要素またはフィールドへの参照によってコンパイル警告が発生します。</span><span class="sxs-lookup"><span data-stu-id="abd76-186">When you set **IsObsolete** to Yes, references to that element or field will cause compilation warnings.</span></span>



