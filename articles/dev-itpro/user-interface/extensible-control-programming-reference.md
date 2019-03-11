---
title: 拡張可能なコントロールのプログラミング リファレンス
description: このトピックでは、拡張可能なコントロール プログラミングの参考資料を提供します。
author: TLeforMicrosoft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 50211
ms.assetid: 0a774c73-9e5d-4faa-8716-61476c1a9b6e
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 424bbcdf3e26ea3409b03894f745c5cecc4c1c70
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369863"
---
# <a name="extensible-control-programming-reference"></a><span data-ttu-id="43993-103">拡張可能なコントロールのプログラミング リファレンス</span><span class="sxs-lookup"><span data-stu-id="43993-103">Extensible control programming reference</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43993-104">このトピックでは、拡張可能なコントロール プログラミングの参考資料を提供します。</span><span class="sxs-lookup"><span data-stu-id="43993-104">This topic provides reference content for extensible control programming.</span></span>

<span data-ttu-id="43993-105">このドキュメントでは、拡張可能なコントロールを作成するための API、HTML、および JavaScript のサポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="43993-105">This document describes the API, HTML, and JavaScript support for creating extensible controls.</span></span>

## <a name="examples"></a><span data-ttu-id="43993-106">例</span><span class="sxs-lookup"><span data-stu-id="43993-106">Examples</span></span>
<span data-ttu-id="43993-107">このドキュメントには、文書化されている各 API の使用方法を示す小さなコード スニペットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="43993-107">This document contains small code snippets that show how to use each API that is documented.</span></span> <span data-ttu-id="43993-108">これらの API の多くを活用する完成したコントロールのより完全な例は Github で確認できます。</span><span class="sxs-lookup"><span data-stu-id="43993-108">More complete examples of finished controls that leverage many of these APIs can be found on Github.</span></span> [<span data-ttu-id="43993-109">Github での拡張可能コントロールの例</span><span class="sxs-lookup"><span data-stu-id="43993-109">Extensible Control Examples on Github</span></span>](http://github.com/Microsoft/Dynamics-AX-Extensible-Control-Samples)

## <a name="control-block-diagram"></a><span data-ttu-id="43993-110">コントロール ブロック図</span><span class="sxs-lookup"><span data-stu-id="43993-110">Control block diagram</span></span>
<span data-ttu-id="43993-111">この高度な図は、拡張可能なコントロールの主要コンポーネントと、それらが相互にやり取りする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="43993-111">This high-level diagram illustrates the key components of an extensible control and how they interact with each other.</span></span> <span data-ttu-id="43993-112">拡張可能なコントロール ソリューションには、コントロールを実装する 2 つの X++ クラスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="43993-112">Your extensible control solution will contain two X++ classes that implement your control.</span></span> <span data-ttu-id="43993-113">ランタイム クラスは、ランタイム データ、プレゼンテーション、コントロールの動作を実装します。</span><span class="sxs-lookup"><span data-stu-id="43993-113">The runtime class implements the runtime data, presentation, and behavior of your control.</span></span> <span data-ttu-id="43993-114">ビルド クラスは、コントロールがフォーム デザイナー、プロパティ ウィンドウ、およびアプリケーション エクスプローラーでどのように表示されるかを定義します。</span><span class="sxs-lookup"><span data-stu-id="43993-114">The build class defines how your control is displayed in Form Designer, Property Window, and Application Explorer.</span></span> <span data-ttu-id="43993-115">[![ExtensibilityArchitecture](./media/extensibilityarchitecture.png)](./media/extensibilityarchitecture.png)</span><span class="sxs-lookup"><span data-stu-id="43993-115">[![ExtensibilityArchitecture](./media/extensibilityarchitecture.png)](./media/extensibilityarchitecture.png)</span></span>

<a name="x"></a><span data-ttu-id="43993-116">X++</span><span class="sxs-lookup"><span data-stu-id="43993-116">X++</span></span>
---

<span data-ttu-id="43993-117">コントロールの X++ API は、フォーム開発者向けの API です。</span><span class="sxs-lookup"><span data-stu-id="43993-117">The X++ API of your control is the Form-developer-facing API.</span></span> <span data-ttu-id="43993-118">コントロールの X++ API を設計する際には、フォーム開発者に提供する API とビヘイビアーを考慮してください。</span><span class="sxs-lookup"><span data-stu-id="43993-118">Be sure to consider the APIs and behaviors you want to provide to the Form developer when designing the X++ APIs for your control.</span></span>

## <a name="runtime-the-x-runtime-class"></a><span data-ttu-id="43993-119">ランタイム: X++ ランタイム クラス</span><span class="sxs-lookup"><span data-stu-id="43993-119">Runtime: The X++ runtime class</span></span>
<span data-ttu-id="43993-120">ランタイム クラスは、開発者向け API をコントロール用に定義します。</span><span class="sxs-lookup"><span data-stu-id="43993-120">The runtime class defines the public, developer-facing API for your control.</span></span> <span data-ttu-id="43993-121">これには、コントロールのランタイム ロジックも含まれます。</span><span class="sxs-lookup"><span data-stu-id="43993-121">It also contains the runtime logic for your control.</span></span> <span data-ttu-id="43993-122">実行時クラスの仕事は、コントロールのプロパティを使用してコントロールの状態を維持することです。</span><span class="sxs-lookup"><span data-stu-id="43993-122">The job of the runtime class is to maintain the state of the control via the control’s properties.</span></span>

## <a name="runtime-class-declaration"></a><span data-ttu-id="43993-123">ランタイム: クラス宣言</span><span class="sxs-lookup"><span data-stu-id="43993-123">Runtime: Class declaration</span></span>
<span data-ttu-id="43993-124"><strong>FormTemplateControl</strong> または <strong>FormTemplateControl</strong><em> から派生した型を拡張する X++ クラスを宣言します。\*\**FormTemplateControl</em>* には、テンプレート ID やリソース バンドルなど、すべてのコントロールに必要な基本的なプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="43993-124">Declare an X++ class that extends <strong>FormTemplateControl</strong> or a type derived from <strong>FormTemplateControl</strong><em>. \*\**FormTemplateControl</em>* contains basic properties that are necessary for every control, such as the Template ID and the Resource Bundle.</span></span> <span data-ttu-id="43993-125">次の例では、基本コントロール クラス、<strong>FormTemplateControl</strong> を拡張しています。</span><span class="sxs-lookup"><span data-stu-id="43993-125">The following example extends the base control class, <strong>FormTemplateControl</strong>.</span></span>

    class MyControl extends FormTemplateControl

## <a name="runtime-formcontrolattribute"></a><span data-ttu-id="43993-126">ランタイム: FormControlAttribute</span><span class="sxs-lookup"><span data-stu-id="43993-126">Runtime: FormControlAttribute</span></span>
<span data-ttu-id="43993-127">**FormControlAttribute** 属性を X++ クラス宣言に適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43993-127">You must apply the **FormControlAttribute** attribute to the X++ class declaration.</span></span>

    [FormControlAttribute(<Template ID>, <Resource Bundle Path>, <Build class name>))]

<span data-ttu-id="43993-128">以下の引数を供給する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43993-128">You must supply the following arguments:</span></span>

-   <span data-ttu-id="43993-129">**テンプレート ID**: テンプレートの ID を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="43993-129">**Template ID**: A string that specifies the ID of the template.</span></span> <span data-ttu-id="43993-130">テンプレート ID は JavaScript クラス名であり、コントロールの HTML 要素 ID です。</span><span class="sxs-lookup"><span data-stu-id="43993-130">The Template ID is the JavaScript class name & the HTML element ID of the control.</span></span> <span data-ttu-id="43993-131">慣例として、TemplateID はコントロールのランタイム クラスのクラス名と一致します。</span><span class="sxs-lookup"><span data-stu-id="43993-131">By convention, the TemplateID matches the class name of the control's runtime class.</span></span>
-   <span data-ttu-id="43993-132">**リソース バンドル パス**: リソース バンドルへのパスを指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="43993-132">**Resource Bundle Path**: A string that specifies the path to the resource bundle.</span></span> <span data-ttu-id="43993-133">リソース バンドル パスは、主要な HTM ファイルが置かれている Web パスです。</span><span class="sxs-lookup"><span data-stu-id="43993-133">The Resource Bundle Path is the web path where the main HTM files are located.</span></span> <span data-ttu-id="43993-134">実行時に、クライアント フレームワークはリソース バンドル パスで指定された HTM ファイルを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="43993-134">At runtime, the Client framework will load the HTM file specified by the Resource Bundle Path.</span></span> <span data-ttu-id="43993-135">実行時に、クライアント フレームワークは指定されたテンプレート ID と一致する ID を持つ HTML 要素のリソース バンドルを検索します。</span><span class="sxs-lookup"><span data-stu-id="43993-135">At runtime, the Client framework will search the Resource Bundle for the HTML element with an ID matching the specified Template ID.</span></span> <span data-ttu-id="43993-136">実行時に、クライアント フレームワークはテンプレート ID で指定された JavaScript クラスをインスタンス化します。</span><span class="sxs-lookup"><span data-stu-id="43993-136">At runtime, the Client framework will instantiate the JavaScript class specified by the Template ID.</span></span> <span data-ttu-id="43993-137">このパスは Web ディレクトリのルートからの相対パスです。</span><span class="sxs-lookup"><span data-stu-id="43993-137">This path is relative to the root of the web directory.</span></span>
-   <span data-ttu-id="43993-138">**ビルド クラス名**: ビルド クラスの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="43993-138">**Build class name**: A string that specifies the name of the build class.</span></span> <span data-ttu-id="43993-139">ビルド クラス名は、デザイン時の動作を決定する X++ クラスです。</span><span class="sxs-lookup"><span data-stu-id="43993-139">The build class name is the X++ class that determines the design-time behavior.</span></span> <span data-ttu-id="43993-140">デザイン時に、Visual Studio のフレームワークはこの属性を反映し、デザイナー クラスとして指定された X++ クラスを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="43993-140">At design time, the Visual Studio framework reflects over this attribute and loads the specified X++ class as the designer class.</span></span> <span data-ttu-id="43993-141">実行時に、X++ フレームワークは指定した X++ クラスを applyBuild() の super のビルド クラスとしてインスタンス化します。</span><span class="sxs-lookup"><span data-stu-id="43993-141">At runtime, the X++ framework will instantiate the specified X++ class as the build class in the super of applyBuild().</span></span>

<span data-ttu-id="43993-142">次の例は、"MyControl" という名前のコントロールの標準的なクラスと属性の宣言を示しています。</span><span class="sxs-lookup"><span data-stu-id="43993-142">The following example shows a typical class and attribute declaration for a control named "MyControl".</span></span>

    [FormControlAttribute('MyControl', '/resources/html/MyControl', classStr(MyControlBuild))]
    class MyControl extends FormTemplateControl

## <a name="runtime-formcommandattribute"></a><span data-ttu-id="43993-143">ランタイム: FormCommandAttribute</span><span class="sxs-lookup"><span data-stu-id="43993-143">Runtime: FormCommandAttribute</span></span>
<span data-ttu-id="43993-144">**FormCommandAttribute** は、コントロール クラスのメソッドに適用されるため、メソッドをコントロールの JavaScript クラスから呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="43993-144">The **FormCommandAttribute** is applied to a method in your control class, which allows the method to be called from a control’s JavaScript class.</span></span> <span data-ttu-id="43993-145">この属性を適用したメソッドは**コマンド**と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="43993-145">A method with this attribute applied is called a **command.**</span></span> <span data-ttu-id="43993-146">**FormCommandAttribute** は、コントロールの JavaScript クラスから直接アクセスする必要がある X++ メソッドのみで使用します。 のみ使用します。</span><span class="sxs-lookup"><span data-stu-id="43993-146">Use the **FormCommandAttribute** on only the X++ methods that need to be accessed directly from the control’s JavaScript class.</span></span> <span data-ttu-id="43993-147">コマンドとしての役割を果たす X++ メソッドは、文字列の引数のみ受け入れることができます。</span><span class="sxs-lookup"><span data-stu-id="43993-147">An X++ method serving as a command can only accept string arguments.</span></span> <span data-ttu-id="43993-148">このメソッドは、文字列引数を他の型にシリアル化または逆シリアル化するために必要な操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43993-148">The method must perform the necessary operations to serialize or deserialize the string arguments into other types.</span></span> <span data-ttu-id="43993-149">**FormCommandAttribute** は、X++ 内からメソッドが使用される場合、X++ メソッドの動作に影響を与えません。</span><span class="sxs-lookup"><span data-stu-id="43993-149">The **FormCommandAttribute** has no effect on the behavior of the X++ method when the method is used from within X++.</span></span> <span data-ttu-id="43993-150">**FormCommandAttribute** は、JavaScript からアクセス可能な外のエンドポイントとして X++ メソッドを公開します。</span><span class="sxs-lookup"><span data-stu-id="43993-150">The **FormCommandAttribute** exposes the X++ method as an external endpoint that is accessible from JavaScript.</span></span> <span data-ttu-id="43993-151">したがって、すべてのコマンドは脅威モデル化およびエクスプロイトのためにテストされる必要があります。また、そのすべての引数について検証を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43993-151">As such, every command should be threat modeled and tested for exploits, and should perform validation on all of its arguments.</span></span> <span data-ttu-id="43993-152">基礎となる X++ メソッドは、X++ からアクセスできないようにプライベート宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43993-152">The underlying X++ method should be declared private so that it is not accessible from X++.</span></span> <span data-ttu-id="43993-153">X++ コードがこのメソッドの動作にアクセスする必要がある場合は、個別の X++ メソッドは **FormCommandAttribute** なしで public として宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43993-153">If X++ code needs to access this method’s behavior, then a separate X++ method should be declared as public without the **FormCommandAttribute.**</span></span> <span data-ttu-id="43993-154">このパブリック メソッドには、X++と JavaScript の両方で必要な共有コードが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="43993-154">This public method should contain any shared code that is needed by both X++ and JavaScript.</span></span> <span data-ttu-id="43993-155">**FormCommandAttribute** を使用した private X++ メソッドは、このパブリック メソッドを呼び出して、共有コードにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="43993-155">The private X++ method with the **FormCommandAttribute** can then call this public method to access the shared code.</span></span> <span data-ttu-id="43993-156">この方法では、コア共有 X++ ロジックを実行する前に、JavaScript (引数の型の逆シリアル化、引数の検証、セキュリティの検証など) からの呼び出しに特定なロジックをコマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="43993-156">This practice allows the command to perform logic that is specific to calls coming from JavaScript (such as argument type deserialization, argument validation, security validation, etc.) before executing the core shared X++ logic.</span></span> <span data-ttu-id="43993-157">次の引数を **FormCommandAttribute** コンストラクターに指定します。</span><span class="sxs-lookup"><span data-stu-id="43993-157">You supply the following arguments to the **FormCommandAttribute** constructor:</span></span>

-   <span data-ttu-id="43993-158">**名前**: コマンドの名前を指定する必要な文字列。</span><span class="sxs-lookup"><span data-stu-id="43993-158">**Name**: A required string that specifies the name of the command.</span></span> <span data-ttu-id="43993-159">プロパティの名前を付けるためのいくつかのベスト プラクティス。</span><span class="sxs-lookup"><span data-stu-id="43993-159">A few best practices for naming Properties:</span></span>
    -   <span data-ttu-id="43993-160">最初の文字を大文字にし、PascalCase を使用します。</span><span class="sxs-lookup"><span data-stu-id="43993-160">Capitalize the first letter, and use PascalCase.</span></span>
    -   <span data-ttu-id="43993-161">名前に動詞を使用します。</span><span class="sxs-lookup"><span data-stu-id="43993-161">Use a verb in the name.</span></span>
    -   <span data-ttu-id="43993-162">コマンドが FormProperty の読み取り/書き込みに使用される場合、プロパティ名を含めます (例: Set\_&lt;PropertyName&gt;)</span><span class="sxs-lookup"><span data-stu-id="43993-162">Include the Property name if the Command is used to read/write a FormProperty (ex: Set\_&lt;PropertyName&gt;)</span></span>
    -   <span data-ttu-id="43993-163">継承済 JavaScript プロパティの名前を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="43993-163">Do not use any of the names of inherited JavaScript properties.</span></span>
-   <span data-ttu-id="43993-164">**即時実行**: このコマンドへの呼び出しを延期するか、即時実行を必要とするかを指定するオプションのブール値。</span><span class="sxs-lookup"><span data-stu-id="43993-164">**Execute immediate**: An optional boolean that specifies whether calls to this command are deferred or require immediate execution.</span></span> <span data-ttu-id="43993-165">既定では、コマンドは**即時実行**を **true、** に設定しているため、呼び出しは延期されません。</span><span class="sxs-lookup"><span data-stu-id="43993-165">By default, commands have **Execute immediate** set to **true,** so calls are not deferred.</span></span> <span data-ttu-id="43993-166">ユーザーが次のアクションを完了できるようになる前に X++ ロジックを実行する必要があるため、ほとんどのコマンドは即時実行が必要になります。</span><span class="sxs-lookup"><span data-stu-id="43993-166">Most commands likely require immediate execution because their X++ logic must run before allowing the user to complete their next action.</span></span> <span data-ttu-id="43993-167">ただし、次のアクションを実行するユーザー機能に副作用のないコマンドは、パフォーマンス上のメリットを得るために安全に据え置かれる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="43993-167">However, commands that have no side-effects on the user’s ability to take their next action can likely be safely deferred to gain a performance benefit.</span></span> <span data-ttu-id="43993-168">延期されるコマンドについては、ネットワークおしゃべりを減らすため、即時実行を **false** に設定します。</span><span class="sxs-lookup"><span data-stu-id="43993-168">For commands that can be deferred, set Execute immediate to **false** to reduce network chattiness.</span></span>

<span data-ttu-id="43993-169">次の例では、"SetText" という名前のコマンドを宣言しています。</span><span class="sxs-lookup"><span data-stu-id="43993-169">The following example declares a command with the name of "SetText".</span></span>

    [FormCommandAttribute("SetText")]
    private void setText(str value)
    {
        // Add implementation code here.
    }

## <a name="runtime-formpropertyattribute"></a><span data-ttu-id="43993-170">ランタイム: FormPropertyAttribute</span><span class="sxs-lookup"><span data-stu-id="43993-170">Runtime: FormPropertyAttribute</span></span>
<span data-ttu-id="43993-171">**FormPropertyAttribute** は、コントロール クラスのメソッドに適用されるため、X++ メソッドをコントロールの JavaScript クラスから **FormProperty** ゲッター/セッターとして呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="43993-171">The **FormPropertyAttribute** is applied to a method in your control class, which allows an X++ method to be called as a **FormProperty** getter/setter from the control's JavaScript class.</span></span> <span data-ttu-id="43993-172">この属性を適用したメソッドは**プロパティ**と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="43993-172">A method with this attribute applied is called a **property.**</span></span> <span data-ttu-id="43993-173">コントロールの JavaScript クラスから直接アクセスする必要がある X++ メソッドの **FormPropertyAttribute** のみ使用します。</span><span class="sxs-lookup"><span data-stu-id="43993-173">Only use the **FormPropertyAttribute** on those X++ methods which need to be accessed directly from the control’s JavaScript class.</span></span> <span data-ttu-id="43993-174">**FormPropertyAttribute** は、X++ 内からメソッドが使用される場合、X++ メソッドの動作に影響を与えません。</span><span class="sxs-lookup"><span data-stu-id="43993-174">The **FormPropertyAttribute** has no effect on the behavior of the X++ method when the method is used from within X++.</span></span> <span data-ttu-id="43993-175">すべてのプロパティは、ブラウザーにエンドポイントを公開します。</span><span class="sxs-lookup"><span data-stu-id="43993-175">Every property exposes an endpoint to the browser.</span></span> <span data-ttu-id="43993-176">したがって、すべてのプロパティは脅威モデル化およびエクスプロイトのためにテストされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="43993-176">As such, every property should be threat modeled and tested for exploits.</span></span> <span data-ttu-id="43993-177">基礎となる X++ メソッドは、他の X++ コードからアクセスできないようにプライベート宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43993-177">The underlying X++ method should be declared private so that it is not accessible from other X++ code.</span></span> <span data-ttu-id="43993-178">別の X++ コードがプロパティにアクセスする必要がある場合、別のパブリック X++ メソッドを **FormPropertyAttibute** なしで宣言し、このメソッドに共有プロパティ ロジックを移動します。</span><span class="sxs-lookup"><span data-stu-id="43993-178">If other X++ code needs to access the property, then declare a separate public X++ method without the **FormPropertyAttibute,** and move the shared property logic to this method.</span></span> <span data-ttu-id="43993-179">次に、このメソッドを **FormPropertyAttribute を持つプライベート X++ メソッドから呼び出します。この方法により、コア共有 X++ ロジックを実行する前に、JavaScript からの呼び出しに固有のロジック (引数の型の逆シリアル化、引数の検証、セキュリティの検証など) をプロパティで実行できます。**</span><span class="sxs-lookup"><span data-stu-id="43993-179">Then call this method from the private X++ method with the **FormPropertyAttribute. This practice allows the property to perform logic that is specific to calls coming from JavaScript (such as argument type deserialization, argument validation, security validation, etc.) before executing the core shared X++ logic.**</span></span> <span data-ttu-id="43993-180">基本となる X++ メソッドは、必要なタイプのプロパティを受け入れて返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="43993-180">The underlying X++ method must accept and return the desired type of the property.</span></span> <span data-ttu-id="43993-181">目的の型が EDT である場合は、プロパティは、EDT の基本データ型を受け入れ、返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="43993-181">If the desired type if an EDT, the property must accept and return the base type of the EDT.</span></span> <span data-ttu-id="43993-182">サポートされているプロパティの種類は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="43993-182">The supported property types are:</span></span>

-   [<span data-ttu-id="43993-183">X++ プリミティブ型</span><span class="sxs-lookup"><span data-stu-id="43993-183">X++ primitive types</span></span>](https://msdn.microsoft.com/en-us/library/aa602290.aspx)
-   <span data-ttu-id="43993-184">[X++ データ契約](https://msdn.microsoft.com/en-us/library/system.runtime.serialization.datacontractattribute(v=vs.110).aspx) (そのメンバーもサポートされているタイプ)</span><span class="sxs-lookup"><span data-stu-id="43993-184">[X++ data contracts](https://msdn.microsoft.com/en-us/library/system.runtime.serialization.datacontractattribute(v=vs.110).aspx) (whose members are also supported types)</span></span>
-   <span data-ttu-id="43993-185">[X++ リスト](https://msdn.microsoft.com/en-us/library/list.aspx) (その項目もサポートされているタイプ)</span><span class="sxs-lookup"><span data-stu-id="43993-185">[X++ List](https://msdn.microsoft.com/en-us/library/list.aspx) (whose items are also supported types)</span></span>

<span data-ttu-id="43993-186">次の引数を **FormPropertyAttribute** コンストラクターに指定します。</span><span class="sxs-lookup"><span data-stu-id="43993-186">You supply the following arguments to the **FormPropertyAttribute** constructor:</span></span>

-   <span data-ttu-id="43993-187">**FormPropertyKind:** プロパティの種類を示す必須の **FormProperyKind** の値。</span><span class="sxs-lookup"><span data-stu-id="43993-187">**FormPropertyKind:** A required **FormProperyKind** value that specifies the type of the property.</span></span> <span data-ttu-id="43993-188">データ ソース フィールドにバインドされないプロパティには **FormPropertyKind::Value** を使用し、データ ソース フィールドにバインドされるプロパティには **FormPropertyKind::BindableValue** を使用します。</span><span class="sxs-lookup"><span data-stu-id="43993-188">Use **FormPropertyKind::Value** for Properties not bound to a data source field, and use **FormPropertyKind::BindableValue** for properties that may be bound to a data source field.</span></span>
-   <span data-ttu-id="43993-189">**名前:** プロパティの名前を指定する必要な文字列。</span><span class="sxs-lookup"><span data-stu-id="43993-189">**Name:** A required string that specifies the name of the property.</span></span> <span data-ttu-id="43993-190">プロパティの名前を付けるためのいくつかのベスト プラクティス。</span><span class="sxs-lookup"><span data-stu-id="43993-190">A few best practices for naming properties:</span></span>
    -   <span data-ttu-id="43993-191">最初の文字を大文字にし、PascalCase を使用します。</span><span class="sxs-lookup"><span data-stu-id="43993-191">Capitalize the first letter, and use PascalCase.</span></span>
    -   <span data-ttu-id="43993-192">継承済 JavaScript プロパティの名前を使用しない</span><span class="sxs-lookup"><span data-stu-id="43993-192">Do not use any of the names of inherited JavaScript properties</span></span>
-   <span data-ttu-id="43993-193">**読み取り専用**: このプロパティをコントロールの JavaScript クラスから書き込み可能にするかどうかを指定するオプションのブール値。</span><span class="sxs-lookup"><span data-stu-id="43993-193">**Read only**: An optional boolean that specifies whether this property is writable from the control’s JavaScript class.</span></span> <span data-ttu-id="43993-194">既定のプロパティでは**読み取り専用**が **false、** に設定されているため、書き込み可能です。</span><span class="sxs-lookup"><span data-stu-id="43993-194">By default, properties have **Read only** set to **false,** so they are writeable.</span></span> <span data-ttu-id="43993-195">この引数は、X++ からこのプロパティに書き込む機能には影響しません。</span><span class="sxs-lookup"><span data-stu-id="43993-195">This argument does not affect the ability to write to this property from X++.</span></span> <span data-ttu-id="43993-196">X++ メソッドを読み取り専用にするには、メソッド宣言からすべてのメソッド引数を削除します。</span><span class="sxs-lookup"><span data-stu-id="43993-196">To make the X++ method read only, remove all method arguments from the method declaration.</span></span> <span data-ttu-id="43993-197">プロパティの大部分は、コントロールの JavaScript クラスから書き込みできません。</span><span class="sxs-lookup"><span data-stu-id="43993-197">A majority of properties should not be writable from the control’s JavaScript class.</span></span> <span data-ttu-id="43993-198">ほとんどのプロパティ値は検証を必要とするため、プロパティのセッターとしてコマンドを使用してバッキング プロパティが設定される前に検証ロジックを実行できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="43993-198">Because most property values require validation, a command should be used as a setter for the property so that validation logic is can be run before the backing property is set.</span></span>
-   <span data-ttu-id="43993-199">**即時実行**: このプロパティへの書き込みを延期するか、即時実行がひつようであるかを指定するオプションのブール値。</span><span class="sxs-lookup"><span data-stu-id="43993-199">**Execute immediate**: An optional Boolean that specifies whether writes to this property are deferred or require immediate execution.</span></span> <span data-ttu-id="43993-200">既定のプロパティでは**即時実行**が **false、** に設定されているため、書き込みは延期されます。</span><span class="sxs-lookup"><span data-stu-id="43993-200">By default, properties have **Execute immediate** set to **false,** so writes are deferred.</span></span> <span data-ttu-id="43993-201">大多数のプロパティはコントロールの JavaScript クラスに書き込み可能なフォームであってはならないため、**即時実行**フラグの既定値は **false** で、パフォーマンス上の利益を提供します。</span><span class="sxs-lookup"><span data-stu-id="43993-201">Because the majority of properties should not be writeable form the control’s JavaScript class, the **Execute immediate** flag defaults to **false** and provides performance benefits.</span></span> <span data-ttu-id="43993-202">コントロールの JavaScript クラスから書き込み可能なプロパティの場合でも、動作を有効にする前に、即時実行のパフォーマンスの副作用を慎重に検討する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43993-202">Even in the case of properties that are writable from the control’s JavaScript class, the performance side effects of immediate execution should be carefully considered before enabling the behavior.</span></span>

<span data-ttu-id="43993-203">次の例は、一般的なプロパティ宣言を示しています。</span><span class="sxs-lookup"><span data-stu-id="43993-203">The following example shows a typical property declaration.</span></span> <span data-ttu-id="43993-204">ほとんどのプロパティは、以下のように取得/設定に同じ定型コードを共有します。</span><span class="sxs-lookup"><span data-stu-id="43993-204">Most properties share the same boilerplate code for getting/setting, as shown below.</span></span> <span data-ttu-id="43993-205">textProperty 変数は、このプロパティの FormProperty の後ろにあるフィールドです。</span><span class="sxs-lookup"><span data-stu-id="43993-205">The textProperty variable is the backing FormProperty field for this property.</span></span>

```
[FormPropertyAttribute(FormPropertyKind::Value, "Text", true)
private str parmText(str _value = textProperty.parmValue())
{
    if(!prmIsDefault(_value))
    {
        textProperty.setValueOrBinding(_value);
    }
    return textProperty.parmValue();
}
```

## <a name="runtime-formproperty"></a><span data-ttu-id="43993-206">ランタイム: FormProperty</span><span class="sxs-lookup"><span data-stu-id="43993-206">Runtime: FormProperty</span></span>
##### <a name="behavior"></a><span data-ttu-id="43993-207">動作</span><span class="sxs-lookup"><span data-stu-id="43993-207">Behavior</span></span>

<span data-ttu-id="43993-208">**FormProperty** は X++ と JavaScript の間のプロパティの値の同期のために管理フレームワークによって使用される X++ [派生型](https://msdn.microsoft.com/en-us/library/esd9wew8(v=vs.100).aspx) です。</span><span class="sxs-lookup"><span data-stu-id="43993-208">**FormProperty** is an X++ [derived type](https://msdn.microsoft.com/en-us/library/esd9wew8(v=vs.100).aspx) used by the control framework for the synchronization of property values between X++ and JavaScript.</span></span> <span data-ttu-id="43993-209">**FormProperty** オブジェクトはプロパティによって内部で使用されるバックアップ フィールドと見なされます。</span><span class="sxs-lookup"><span data-stu-id="43993-209">**FormProperty** objects are considered the backing fields used internally by properties.</span></span> <span data-ttu-id="43993-210">各 **FormProperty** は、コントロールの X++ ランタイム クラスの 4 つの場所で通常使用されます。</span><span class="sxs-lookup"><span data-stu-id="43993-210">Each **FormProperty** is typically used in 4 places throughout a control’s X++ runtime class:</span></span>

1.  <span data-ttu-id="43993-211">**FormProperty** は通常クラス宣言のすぐ下で宣言されます。</span><span class="sxs-lookup"><span data-stu-id="43993-211">The **FormProperty** is declared, usually right below the class declaration</span></span>
2.  <span data-ttu-id="43993-212">**FormProperty** は、クラスの **new** メソッドでインスタンス化されます</span><span class="sxs-lookup"><span data-stu-id="43993-212">The **FormProperty** is instantiated in the **new** method of the class</span></span>
3.  <span data-ttu-id="43993-213">**FormProperty** は、クラスの **applyBuild** メソッドで初期化されます</span><span class="sxs-lookup"><span data-stu-id="43993-213">The **FormProperty** is initialized in the **applyBuild** method of the class</span></span>
4.  <span data-ttu-id="43993-214">**FormProperty** は、プロパティの X++ メソッドで読み書きされます</span><span class="sxs-lookup"><span data-stu-id="43993-214">The **FormProperty** is read and written in the X++ method for the property</span></span>

<span data-ttu-id="43993-215">次の例は、典型的なコントロールの X++ ランタイム クラスで使用されている **FormProperty** を示しています。</span><span class="sxs-lookup"><span data-stu-id="43993-215">The following example shows a **FormProperty** being used in a typical controls’ X++ runtime class.</span></span>

```
[FormControlAttribute("MyControl", "/resources/html/MyControl", classStr(BuildMyControl))]
class MyControl extends FormTemplateControl
{             
    FormProperty textProperty;          

    public void new(FormBuildControl _build, FormRun _formRun)
    {
        super(_build, _formRun);
        
        this.setTemplateId("MyControl");
        this.setResourceBundleName("/resources/html/MyControl");
        textProperty = this.addProperty(
        methodStr(MyControl, parmText), Types::String);
    }

    public void applyBuild()
    {
        BuildMyControl build;
        
        super();

        build = this.build();
        if(build)
        {
            this.parmText(build.Text());
        }
    }

    [FormPropertyAttribute(FormPropertyKind::Value, "Text", true)
    private str parmText(str _value = textProperty.parmValue())
    {
        if(!prmIsDefault(_value))
        {
            textProperty.setValueOrBinding(_value);
        }
        return textProperty.parmValue();
    }
}
```

## <a name="runtime-new-method"></a><span data-ttu-id="43993-216">ランタイム: 新しいメソッド</span><span class="sxs-lookup"><span data-stu-id="43993-216">Runtime: new method</span></span>
<span data-ttu-id="43993-217">コントロールの X++ ランタイム クラスの **new** メソッドは、フォームのコントロールのインスタンス化の一部として呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="43993-217">The **new** method on a control’s X++ runtime class is called as a part of instantiating the control on a form.</span></span> <span data-ttu-id="43993-218">**新規**メソッドがフォーム ライフ サイクルで呼び出される際の詳細については、「コントロール ライフサイクルの図」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="43993-218">For the details on when the **new** method is called in the form lifecycle, please see the Control Lifecycle Diagrams.</span></span> <span data-ttu-id="43993-219">ここのメソッドは、コントロールの FormProperties をインスタンス化し、コントロールのテンプレート ID とリソース バンドル パスを設定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="43993-219">This method is used for instantiation of a control’s FormProperties and setting the control’s Template ID and Resource Bundle Path.</span></span> <span data-ttu-id="43993-220">FormProperty の例で **new** メソッドの一般的な使用方法を参照してください。</span><span class="sxs-lookup"><span data-stu-id="43993-220">See typical use of the **new** method in the example for FormProperty.</span></span>

## <a name="runtime-applybuild-method"></a><span data-ttu-id="43993-221">ランタイム: applyBuild メソッド</span><span class="sxs-lookup"><span data-stu-id="43993-221">Runtime: applyBuild method</span></span>
<span data-ttu-id="43993-222">コントロールの X++ ランタイム クラスの **applyBuild** メソッドは、フォームのコントロールのインスタンス化の一部として呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="43993-222">The **applyBuild** method on a control’s X++ runtime class is called as a part of instantiating the control on a form.</span></span> <span data-ttu-id="43993-223">**applyBuild**メソッドがフォーム ライフ サイクルで呼び出される際の詳細については、「コントロール ライフサイクルの図」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="43993-223">For the details on when the **applyBuild** method is called in the form lifecycle, please see the Control Lifecycle Diagrams.</span></span> <span data-ttu-id="43993-224">このメソッドは、コントロールの FormProperties を既定値、またはコントロールをフォームに配置したフォーム開発者が指定した値に初期化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="43993-224">This method is used for initialization of a control’s FormProperties to their default values, or to the values specified by the form developer who placed the control on the form.</span></span> <span data-ttu-id="43993-225">FormProperty の例で **applyBuild** メソッドの一般的な使用方法を参照してください。</span><span class="sxs-lookup"><span data-stu-id="43993-225">See typical use of the \*\*applyBuild \*\*method in the example for FormProperty.</span></span>

## <a name="runtime-formbindingutilinitbinding-method"></a><span data-ttu-id="43993-226">ランタイム: FormBindingUtil::initbinding メソッド</span><span class="sxs-lookup"><span data-stu-id="43993-226">Runtime: FormBindingUtil::initbinding method</span></span>
<span data-ttu-id="43993-227">**FormBindingUtil** は、コントロール フレームワークで提供される API です。</span><span class="sxs-lookup"><span data-stu-id="43993-227">The **FormBindingUtil** is an API provided by the control framework.</span></span> <span data-ttu-id="43993-228">データ ソースで FormProperties をデータ フィールドおよびデータ メソッドにバインドするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="43993-228">It is used to bind FormProperties to data fields and data methods on a data source.</span></span> <span data-ttu-id="43993-229">次の例では、DataSource1 という名前のデータ ソース上の "Value" という名前のデータ フィールドを、ランタイムクラスの textProperty FormProperty にバインドします。</span><span class="sxs-lookup"><span data-stu-id="43993-229">The following example binds the data field with name "Value" on the data source with name "DataSource1" to the textProperty FormProperty of the runtime class.</span></span>

    [FormControlAttribute("MyControl", "/resources/html/MyControl", classStr(BuildMyControl))]
    class MyControl extends FormTemplateControl
    {
        FormProperty textProperty;

        public void new(FormBuildControl _build, FormRun _formRun)
        {
            super(_build, _formRun);
            this.setTemplateId("MyControl");
            this.setResourceBundleName("/resources/html/MyControl");
            textProperty = this.addProperty(
            methodStr(MyControl, parmText), Types::String);
        }

        public void applyBuild()
        {
            BuildMyControl build;
            
            super();
           
            build = this.build();
            if(build)
            {
                this.parmText(FormBindingUtil::initBinding(
                "DataSource1", "Value", this.formRun()));
            }
        }

        [FormPropertyAttribute(FormPropertyKind::Value, "Text", true)
        private str parmText(str _value = textProperty.parmValue())
        {
            if(!prmIsDefault(_value))
            {
                textProperty.setValueOrBinding(_value);
            }
            return textProperty.parmValue();
        }
    }

## <a name="design-time-the-x-build-class"></a><span data-ttu-id="43993-230">デザイン時間: X++ ビルド クラス</span><span class="sxs-lookup"><span data-stu-id="43993-230">Design time: The X++ build class</span></span>
<span data-ttu-id="43993-231">ビルド クラスは、コントロールのデザイン時の動作を定義します。</span><span class="sxs-lookup"><span data-stu-id="43993-231">The build class defines the design time behavior of your control.</span></span> <span data-ttu-id="43993-232">このクラスは、プロパティ シートに表示されるプロパティと、フォーム デザイナーでモデル化されたときのコントロールの動作を決定します。</span><span class="sxs-lookup"><span data-stu-id="43993-232">This class determines which properties appear in the property sheet, and how the control behaves when it is modeled in the Form designer.</span></span> <span data-ttu-id="43993-233">デザイン時クラスの仕事は、後でアクセスするために実行時クラスの設計時間情報を取り込むことです。</span><span class="sxs-lookup"><span data-stu-id="43993-233">The job of the design time class is to capture design time information for the runtime class to access later on.</span></span>

## <a name="design-time-class-declaration--formdesigncontrolattribute"></a><span data-ttu-id="43993-234">デザイン時間: クラス宣言 & FormDesignControlAttribute</span><span class="sxs-lookup"><span data-stu-id="43993-234">Design time: Class declaration & FormDesignControlAttribute</span></span>
<span data-ttu-id="43993-235">FormDesignControlAttribute は、フォームのデザイン ノードを右クリックしたときに、コントロールが Visual Studio フォーム デザイナーに表示されるために必要です。</span><span class="sxs-lookup"><span data-stu-id="43993-235">The FormDesignControlAttribute is necessary for the control to appear in the Visual Studio Form designer when right-clicking on the design node of the form.</span></span> <span data-ttu-id="43993-236">FromDesignControlAttribute が欠落している場合は、コントロールは、必須の X++ コードを介してのみフォームに追加することができます (例えば、フォームの addControlEx メソッドを介して)。</span><span class="sxs-lookup"><span data-stu-id="43993-236">If the FromDesignControlAttribute is missing, then the control can only be added to a form via imperative X++ code (i.e. via the addControlEx method on the form).</span></span>

    [FormDesignControlAttribute("MyControl")]
    class MyControlBuild extends FormBuildControl
    {

    }

## <a name="design-time-formdesignpropertyattribute"></a><span data-ttu-id="43993-237">デザイン時間: FormDesignPropertyAttribute</span><span class="sxs-lookup"><span data-stu-id="43993-237">Design time: FormDesignPropertyAttribute</span></span>
<span data-ttu-id="43993-238">デザイン時間クラスのメソッドにこの属性を配置すると、最初の引数により (および 2 番目の引数により指定されたセクションで) 指定された新しいプロパティが、プロパティの取得/設定メソッドとして動作する対応する X++ メソッドと共にこのコントロールのプロパティ シートに表示されます。</span><span class="sxs-lookup"><span data-stu-id="43993-238">Placing this attribute on a method in the design time class will result in a new property with the name specified by the first argument (and in the section specified by the second argument) appearing the property sheet for this control, with the corresponding X++ method operating as the getter/setter for the property.</span></span>

    [FormDesignControlAttribute("MyControl")]
    class MyControlBuild extends FormBuildControl
    {
        str text; 

        [FormDesignPropertyAttribute("Text", "Data")]
        public str Text(str _value = text)
        {
            if(!prmIsDefault(_value))
            {
                text = _value;
            }
            return text;
        }
    }

## <a name="design-time-formdesignproperty-attribute"></a><span data-ttu-id="43993-239">デザイン時間: FormDesignProperty\*\* \*\*属性</span><span class="sxs-lookup"><span data-stu-id="43993-239">Design time: FormDesignProperty\*\* \*\*Attribute</span></span>
<span data-ttu-id="43993-240">プロパティ シート内の特殊な動作のために、標準の FormDesignPropertyAttribute と一緒に適用できるいくつかの FormDesignProperty 属性があります。</span><span class="sxs-lookup"><span data-stu-id="43993-240">There are a number of FormDesignProperty attributes which may be applied alongside the standard FormDesignPropertyAttribute for specialized behavior in the property sheet.</span></span> <span data-ttu-id="43993-241">特殊なビヘイビアーには、プロパティを値のリストから選択できるコンボ ボックスとして有効にすることが含まれます。</span><span class="sxs-lookup"><span data-stu-id="43993-241">The specialized behavior includes enabling the property as a combobox which allows selecting from a list of a values.</span></span> <span data-ttu-id="43993-242">使用されたさまざまな種類のリストが以下に列挙されています。</span><span class="sxs-lookup"><span data-stu-id="43993-242">The different types of lists that used are enumerated below.</span></span> <span data-ttu-id="43993-243">ユーザーがコンボ ボックスから項目を選択するたびに、その項目の文字列名が、その属性を使用して X++ メソッドのゲッター/セッターに渡されます。</span><span class="sxs-lookup"><span data-stu-id="43993-243">Whenever the user selects an item from the combobox, the string name of that item is passed into the X++ method getter/setter with the attribute.</span></span>

-   <span data-ttu-id="43993-244">\[FormDesignPropertyDataSourceAttribute\] - フォームのデータ ソースのリストを表示します。</span><span class="sxs-lookup"><span data-stu-id="43993-244">\[FormDesignPropertyDataSourceAttribute\] - Shows a list of the data sources on the form.</span></span>
-   <span data-ttu-id="43993-245">\[FormDesignPropertyDataFieldAttribute (&lt;データ ソース名&gt;)\] - 指定されたデータ ソースのデータ フィールドのリストを表示します。</span><span class="sxs-lookup"><span data-stu-id="43993-245">\[FormDesignPropertyDataFieldAttribute(&lt;data source name&gt;)\] - Shows a list of the data fields on the specified data source.</span></span>
-   <span data-ttu-id="43993-246">\[FormDesignPropertyDataMethodAttribute(&lt;データ ソース名&gt;)\] - 指定されたデータ ソースのデータ メソッドのリストを表示します。</span><span class="sxs-lookup"><span data-stu-id="43993-246">\[FormDesignPropertyDataMethodAttribute(&lt;data source name&gt;)\] - Shows a list of the data methods on the specified data source.</span></span>
-   <span data-ttu-id="43993-247">\[FormDesignPropertyFieldGroupAttribute(&lt;データ ソース名&gt;)\] - 指定されたデータ ソースのフィールド グループのリストを表示します。</span><span class="sxs-lookup"><span data-stu-id="43993-247">\[FormDesignPropertyFieldGroupAttribute(&lt;data source name&gt;)\] - Shows a list of the field groups on the specified data source.</span></span>
-   <span data-ttu-id="43993-248">\[FormDesignPropertyExtendsClassAttribute (&lt;クラス名&gt;)\] - 指定されたクラスを拡張するクラスのリストを表示します。</span><span class="sxs-lookup"><span data-stu-id="43993-248">\[FormDesignPropertyExtendsClassAttribute(&lt;class name&gt;)\] - Shows a list of the classes which extend the specified class.</span></span>
-   <span data-ttu-id="43993-249">\[FormDesignPropertyImplementsAttribute (&lt;インターフェイス名&gt;)\] - 指定されたインターフェイスを実装するクラスのリストを表示します。</span><span class="sxs-lookup"><span data-stu-id="43993-249">\[FormDesignPropertyImplementsAttribute(&lt;interface name&gt;)\] - Shows a list of the classes which implement the specified interface.</span></span>
-   <span data-ttu-id="43993-250">\[FormDesignPropertyReferenceAttribute(&lt;FormDesignPropertyReferenceType::&lt;type&gt;\]) - これは、特定のタイプで指定された AOT コンポーネントのリストを表示します。</span><span class="sxs-lookup"><span data-stu-id="43993-250">\[FormDesignPropertyReferenceAttribute(&lt;FormDesignPropertyReferenceType::&lt;type&gt;)\] - Shows a list of the specified AOT artifacts with the given type.</span></span> <span data-ttu-id="43993-251">サポートされている種類は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="43993-251">The supported types are:</span></span>
    -   <span data-ttu-id="43993-252">テーブル</span><span class="sxs-lookup"><span data-stu-id="43993-252">Table</span></span>
    -   <span data-ttu-id="43993-253">表示</span><span class="sxs-lookup"><span data-stu-id="43993-253">View</span></span>
    -   <span data-ttu-id="43993-254">マップ</span><span class="sxs-lookup"><span data-stu-id="43993-254">Map</span></span>
    -   <span data-ttu-id="43993-255">EDT</span><span class="sxs-lookup"><span data-stu-id="43993-255">EDT</span></span>
    -   <span data-ttu-id="43993-256">BaseEnum</span><span class="sxs-lookup"><span data-stu-id="43993-256">BaseEnum</span></span>
    -   <span data-ttu-id="43993-257">クエリ</span><span class="sxs-lookup"><span data-stu-id="43993-257">Query</span></span>
    -   <span data-ttu-id="43993-258">クラス</span><span class="sxs-lookup"><span data-stu-id="43993-258">Class</span></span>
    -   <span data-ttu-id="43993-259">フォーム</span><span class="sxs-lookup"><span data-stu-id="43993-259">Form</span></span>
    -   <span data-ttu-id="43993-260">MenuItemDisplay</span><span class="sxs-lookup"><span data-stu-id="43993-260">MenuItemDisplay</span></span>
    -   <span data-ttu-id="43993-261">MenuItemOuput</span><span class="sxs-lookup"><span data-stu-id="43993-261">MenuItemOuput</span></span>
    -   <span data-ttu-id="43993-262">MenuItemAction</span><span class="sxs-lookup"><span data-stu-id="43993-262">MenuItemAction</span></span>
    -   <span data-ttu-id="43993-263">タイル</span><span class="sxs-lookup"><span data-stu-id="43993-263">Tile</span></span>
    -   <span data-ttu-id="43993-264">KPI</span><span class="sxs-lookup"><span data-stu-id="43993-264">KPI</span></span>

<span data-ttu-id="43993-265">次の例は、フォーム開発者がデザイン タイム クラスのデータ ソースとデータ フィールドを指定できるようにするために使用される標準プロパティを示しています。</span><span class="sxs-lookup"><span data-stu-id="43993-265">The following example shows standard properties used to allow a Form developer to specify the Data Source and Data Field for the design time class.</span></span>

    [FormDesignControlAttribute("MyControl")]
    class MyControlBuild extends FormBuildControl
    {
        str dataSource; 
        str dataField;
        str dataMethod;

        [FormDesignPropertyAttribute("Data source", "Data"),
         FormDesignPropertyDataSourceAttribute]
        public str DataSource(str _value = dataSource)
        {
            if(!prmIsDefault(_value))
            {
                dataSource = _value;
            }
            return dataSource;
        }

        [FormDesignPropertyAttribute("Data Field", "Data"),
         FormDesignPropertyDataFieldAttribute(methodStr(MyControlBuild, DataSource))]
        public str DataField(str _value = dataField)
        {
            if(!prmIsDefault(dataField))
            {
                dataField = _value;
            }
            return dataField;
        }

        [FormDesignPropertyAttribute("Data Method", "Data"),
         FormDesignPropertyDataMethodAttribute(methodStr(MyControlBuild, DataSource))]
        public str DataMethod(str _value = dataMethod)
        {
            if(!prmIsDefault(dataMethod))
            {
                dataMethod = _value;
            }
            return dataMethod;
        }
    }

<span data-ttu-id="43993-266">上記のようなデザイン時クラスを持つコントロールは、以下に示すように、指定されたデータ ソースと applyBuild メソッド内のデータ フィールドにバインドできます。</span><span class="sxs-lookup"><span data-stu-id="43993-266">A control with a design time class like the one above can then bind to the specified data source and data field inside of the applyBuild method, as show below.</span></span>

    public void applyBuild()
    {
        BuildMyControl build;

        super();

        build = this.build();
        if(build)
        {
            this.parmText(FormBindingUtil::initBinding(
            build.DataSource(), build.DataField(), this.formRun(), build.DataMethod()));
        }
    }

<span data-ttu-id="43993-267">データ フィールドとデータ メソッドの両方を FormBindingUtil::initBinding に渡すと、データ フィールド バインディングはデータ メソッド バインディングを上書きします。</span><span class="sxs-lookup"><span data-stu-id="43993-267">If you supply both a data field and data method to FormBindingUtil::initBinding, the data field binding will override the data method binding.</span></span>

## <a name="html"></a><span data-ttu-id="43993-268">HTML</span><span class="sxs-lookup"><span data-stu-id="43993-268">HTML</span></span>
## <a name="html-framework-attributes"></a><span data-ttu-id="43993-269">HTML: フレームワーク属性</span><span class="sxs-lookup"><span data-stu-id="43993-269">HTML: Framework attributes</span></span>

<span data-ttu-id="43993-270">次のセクションでは、コントロール開発のコントロール フレームワークで使用される HTML 属性について説明します。</span><span class="sxs-lookup"><span data-stu-id="43993-270">The following section documents the HTML attributes that are used in the control framework for control development.</span></span>

### <a name="data-dyn-bind"></a><span data-ttu-id="43993-271">data-dyn-bind</span><span class="sxs-lookup"><span data-stu-id="43993-271">data-dyn-bind</span></span>

<span data-ttu-id="43993-272">**data-dyn-bind**、データ バインディング属性は - 宣言 HTML-based API を使用して、要素の属性、プロパティおよび CSS、または DOM イベントの処理などの変更のような、多くの一般的な DOM 操作を標準化しています。</span><span class="sxs-lookup"><span data-stu-id="43993-272">**data-dyn-bind**, the data binding attribute, standardizes many common DOM manipulations - such as modifying an element’s attributes, properties and CSS, or handling DOM events - through a declarative HTML-based API.</span></span> <span data-ttu-id="43993-273">データ バインディング属性は、複雑な JavaScript を必要とせずにこれらの動作を可能にします。</span><span class="sxs-lookup"><span data-stu-id="43993-273">The data binding attribute allows for these behaviors without requiring complex JavaScript.</span></span> <span data-ttu-id="43993-274">複雑な JavaScript を記述するのではなく、データ バインド属性を使用することで、コントロールの設計、デバッグ、および維持をより簡単にすることによって、コントロールの開発者の貴重な時間を節約することができます。</span><span class="sxs-lookup"><span data-stu-id="43993-274">Using the data binding attribute rather than writing complex JavaScript can save the control developer valuable time by making things such as designing, debugging and maintaining the control much easier.</span></span> <span data-ttu-id="43993-275">ただし、シナリオが必要とする場合、複合 JavaScript が引き続き使用可能です。</span><span class="sxs-lookup"><span data-stu-id="43993-275">However, complex JavaScript is still available when scenarios require its use.</span></span> <span data-ttu-id="43993-276">データ バインディング属性は、HTML 要素の動作をコントロール開発者が提供する値に結合します。</span><span class="sxs-lookup"><span data-stu-id="43993-276">The data binding attribute binds HTML element behaviors to values supplied by the control developer.</span></span> <span data-ttu-id="43993-277">指定された値は、単純な JavaScript [変数](http://www.w3schools.com/js/js_variables.asp)、JavaScript [比較](http://www.w3schools.com/js/js_comparisons.asp)、[算術](http://www.w3schools.com/js/js_arithmetic.asp)式、JavaScript [関数](http://www.w3schools.com/js/js_functions.asp)、JSON [オブジェクト](https://www.w3schools.com/js/js_json_objects.asp)のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="43993-277">The values supplied can be simple JavaScript [variables](http://www.w3schools.com/js/js_variables.asp), JavaScript [comparison](http://www.w3schools.com/js/js_comparisons.asp) or [arithmetic](http://www.w3schools.com/js/js_arithmetic.asp) expressions, JavaScript [functions](http://www.w3schools.com/js/js_functions.asp) and JSON [objects](https://www.w3schools.com/js/js_json_objects.asp).</span></span> <span data-ttu-id="43993-278">提供される値は、このドキュメントで説明されている API を使用して作成された、観察可能な変数でもあります。</span><span class="sxs-lookup"><span data-stu-id="43993-278">The values supplied can also be observable variables, created using the APIs described in this document.</span></span> <span data-ttu-id="43993-279">指定された値が HTML 要素にバインドされる方法は、データ バインディング属性で使用されるバインディング ハンドラーによって決まります。</span><span class="sxs-lookup"><span data-stu-id="43993-279">The way in which the supplied value is bound to the HTML element is determined by the binding handler that is used with the data binding attribute.</span></span> <span data-ttu-id="43993-280">このドキュメントでは、サポートされているすべてのバインディング ハンドラーの一覧を提供します。</span><span class="sxs-lookup"><span data-stu-id="43993-280">A list of all supported binding handlers is provided in this document.</span></span> <span data-ttu-id="43993-281">バインディング ハンドラーで使用する場合、データ バインディング属性には次の構文が必要です。</span><span class="sxs-lookup"><span data-stu-id="43993-281">The data binding attribute requires the following syntax when used with any binding handler.</span></span> <span data-ttu-id="43993-282">**data-dyn-bind** の構文は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="43993-282">The syntax for **data-dyn-bind** is:</span></span>

    data-dyn-bind="[first binding handler]: [value to bind to]"

<span data-ttu-id="43993-283">データ バインディング属性はバインディング ハンドラーと値のペアのコンマ区切りリストを受け入れます。したがって、一度に複数のバインディング ハンドラーをバインディング属性に指定できます。</span><span class="sxs-lookup"><span data-stu-id="43993-283">The data binding attribute accepts a comma-separated list of binding handler-value pairs, so you can supply more than one binding handler to the binding attribute at a time.</span></span> <span data-ttu-id="43993-284">次の例では、div 要素の **visible** プロパティを true にバインドし、div 要素の **textContent** プロパティを "Hi" にバインドします。</span><span class="sxs-lookup"><span data-stu-id="43993-284">The following example binds the **visible** property of the div element to true, and binds the **textContent** property of the div element to "Hi".</span></span>

    data-dyn-bind="text: 'Hi', visible: true"

<span data-ttu-id="43993-285">データ バインディング属性は、コントロール フレームワークによって認識されるカスタム HTML 属性です。</span><span class="sxs-lookup"><span data-stu-id="43993-285">The data binding attribute is a custom HTML attribute understood by the control framework.</span></span> <span data-ttu-id="43993-286">データ バインディング属性は、任意の HTML 要素に適用できます。</span><span class="sxs-lookup"><span data-stu-id="43993-286">The data binding attribute can be applied to any HTML element.</span></span> <span data-ttu-id="43993-287">一部の HTML 要素には、バンディング ハンドラーが変更する動作がない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="43993-287">Some HTML elements may not have the behavior which the binding handler modifies.</span></span> <span data-ttu-id="43993-288">たとえば、**&lt;svg&gt;** 要素でのテキスト バインディング ハンドラーの使用は、**&lt;svg&gt;** 要素に textContent プロパティがないため、テキストを表示しません。</span><span class="sxs-lookup"><span data-stu-id="43993-288">For example, using the text binding handler on an **&lt;svg&gt;** element will not show the text since the **&lt;svg&gt;** element does not have a textContent property.</span></span> <span data-ttu-id="43993-289">コントロール フレームワークは、実行時にコントロールのテンプレートで指定されたデータ バインディングを読み取り、実行します。</span><span class="sxs-lookup"><span data-stu-id="43993-289">The control framework reads and executes the data bindings specified in the control’s template at runtime.</span></span> <span data-ttu-id="43993-290">ブラウザーでのコントロールのライフサイクルは、次のように要約できます。</span><span class="sxs-lookup"><span data-stu-id="43993-290">The lifecycle for the control in the browser can be summarized as follows:</span></span>

1.  <span data-ttu-id="43993-291">コントロールの HTM ファイルは、ブラウザーによって読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="43993-291">The control’s HTM file is loaded by the browser.</span></span>
2.  <span data-ttu-id="43993-292">HTM ファイルで参照されているスクリプトまたはリソース ファイルも、ブラウザーによって読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="43993-292">Any script or resource files referenced in the HTM file are also loaded by the browser.</span></span> <span data-ttu-id="43993-293">手順 1 と 2 は、コントロールの複数のインスタンスがある場合でも、ユーザーのセッション中に 1 回だけ実行されます。</span><span class="sxs-lookup"><span data-stu-id="43993-293">Steps 1 and 2 are executed only once during a user’s session, even if there are multiple instances of the control.</span></span>
3.  <span data-ttu-id="43993-294">コントロールの JavaScript クラスのコンストラクターは、呼び出しであり、コントロール インスタンスの X++ プロパティを使用して渡されます。</span><span class="sxs-lookup"><span data-stu-id="43993-294">The JavaScript class's constructor for the control is call and passed with the X++ properties for the control instance.</span></span>
4.  <span data-ttu-id="43993-295">コントロールのテンプレートは、HTM ファイルからブラウザーのメモリにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="43993-295">The control’s template is copied from the HTM file and into the browser’s memory.</span></span>
5.  <span data-ttu-id="43993-296">コントロールのテンプレートでの HTML 要素は階層順に (深さ優先) データ バインディング用に処理され、各要素のデータ バインディングは左から右の順に実行されます。</span><span class="sxs-lookup"><span data-stu-id="43993-296">HTML elements in the control’s template are processed for data binding in hierarchical order (depth first), and data bindings on each element are executed in order from left-to-right</span></span>
6.  <span data-ttu-id="43993-297">元のデータ バインディング属性や、バインディング ハンドラーやフレームワークによって追加されたその他のマークアップを含む最終的な HTML は、ブラウザーの DOM に追加され、ユーザーに表示されるようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="43993-297">The final HTML, including the original data binding attributes as well as any other markup added by the binding handlers or by the framework, is added to the browser’s DOM and rendered for the user to see.</span></span>
7.  <span data-ttu-id="43993-298">後で、観測可能なオブジェクトの値が変更されると、オブザーバブルに対してサブスクライブされたバインディング ハンドラーが再実行され、稼働している DOM がリアルタイムで更新されます。</span><span class="sxs-lookup"><span data-stu-id="43993-298">Later, when the value of an observable changes, any binding handlers subscribed to the observable are re-executed and the live DOM is updated in real-time.</span></span>

## <a name="html-binding-handlers"></a><span data-ttu-id="43993-299">HTML: バインディング ハンドラー</span><span class="sxs-lookup"><span data-stu-id="43993-299">HTML: Binding handlers</span></span>
### <a name="attr"></a><span data-ttu-id="43993-300">attr</span><span class="sxs-lookup"><span data-stu-id="43993-300">attr</span></span>

<span data-ttu-id="43993-301">**attr** バンディング ハンドラーは、指定された HTML 属性と値を要素に適用します。</span><span class="sxs-lookup"><span data-stu-id="43993-301">The **attr** binding handler applies the supplied HTML attribute and value to the element.</span></span> <span data-ttu-id="43993-302">HTML 属性の一覧については、[W3 学校 – HTML 属性](http://www.w3schools.com/html/html_attributes.asp) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="43993-302">For a list of HTML attributes see [W3 Schools – HTML Attributes](http://www.w3schools.com/html/html_attributes.asp).</span></span> <span data-ttu-id="43993-303">引数は、オブジェクト配列として渡されます。</span><span class="sxs-lookup"><span data-stu-id="43993-303">The arguments are passed in as an object array.</span></span> <span data-ttu-id="43993-304">各引数は、デュアル値です。</span><span class="sxs-lookup"><span data-stu-id="43993-304">Each argument is dual-valued.</span></span> <span data-ttu-id="43993-305">最初の値は属性の名前で、2 番目の値は属性の値です。</span><span class="sxs-lookup"><span data-stu-id="43993-305">The first value is the name of the attribute, and the second value is the value of the attribute.</span></span>

-   <span data-ttu-id="43993-306">**名前**: 作成する属性の任意の名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="43993-306">**Name**: a string that specifies the desired name of the attribute to create.</span></span>
-   <span data-ttu-id="43993-307">**値または式:** 属性に設定する値を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="43993-307">**Value or Expression:** a string that specifies the value to set on the attribute.</span></span> <span data-ttu-id="43993-308">式が指定されている場合は、式を評価することによって返される値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="43993-308">If an expression is supplied, the value returned by evaluating the expression will be used.</span></span>

<span data-ttu-id="43993-309">次の例では、title 属性と name 属性を作成し、その値を設定します。</span><span class="sxs-lookup"><span data-stu-id="43993-309">The following example creates the title and name attributes and sets their value.</span></span>

```
<!-- the markup in the HTML template -->
<div data-dyn-bind="attr: {title: 'Hello', name: 'Greeting'}"></div>

<!-- the markup in the browser after the binding handler is applied -->
<div title="Hello" data-dyn-bind="attr: {title: 'Hello', name: 'Greeting'}" name="Greeting"></div>
```

<span data-ttu-id="43993-310">次の例では、式と関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="43993-310">The following example uses expressions and functions.</span></span> <span data-ttu-id="43993-311">ただし、下の例のようにインライン HTML として JavaScript 関数を使用することはお勧めできません。</span><span class="sxs-lookup"><span data-stu-id="43993-311">However, using JavaScript functions as in-line HTML like the example below is not recommended.</span></span>

```
<!-- the markup in the HTML template -->
<div data-dyn-bind="attr: {title: false? 'Hello':'World', name: function(){return 'Greetings';}()}"></div>

<!-- the markup in the browser after the binding handler is applied -->
<div title="World" data-dyn-bind="attr: {title: false? 'Hello':'World', name: function(){return 'Greetings';}()}" name="Greetings"></div>
```

#### <a name="click"></a><span data-ttu-id="43993-312">click</span><span class="sxs-lookup"><span data-stu-id="43993-312">click</span></span>

##### <a name="behavior"></a><span data-ttu-id="43993-313">動作</span><span class="sxs-lookup"><span data-stu-id="43993-313">Behavior</span></span>

<span data-ttu-id="43993-314">要素のクリック イベントに指定された関数をサブスクライブします。</span><span class="sxs-lookup"><span data-stu-id="43993-314">Subscribes the supplied function to the click event on the element.</span></span> <span data-ttu-id="43993-315">クリック イベントのサブスクライブの詳細については、[jQuery – click()](http://api.jquery.com/click/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="43993-315">For more information on subscribing to the click event see [jQuery – click()](http://api.jquery.com/click/).</span></span>

##### <a name="arguments"></a><span data-ttu-id="43993-316">引数</span><span class="sxs-lookup"><span data-stu-id="43993-316">Arguments</span></span>

###### <a name="eventhandler-function"></a><span data-ttu-id="43993-317">EventHandler (関数)</span><span class="sxs-lookup"><span data-stu-id="43993-317">EventHandler (function)</span></span>

<span data-ttu-id="43993-318">イベントが発生したときに呼び出す関数。</span><span class="sxs-lookup"><span data-stu-id="43993-318">The function to call when the event is raised.</span></span>

##### <a name="example-1"></a><span data-ttu-id="43993-319">例 1</span><span class="sxs-lookup"><span data-stu-id="43993-319">Example 1</span></span>

<span data-ttu-id="43993-320">次の例は、要素がクリックされたときの警告メッセージ「Hello」を示しています。</span><span class="sxs-lookup"><span data-stu-id="43993-320">The following example shows an alert message “Hello” when the element is clicked.</span></span>

```
// In your control’s code-behind JS file
<script>
... // boilerplate code
self.ElementClicked = function (event) {
    /* handle the click event */
    alert('Hello');
};
...
</script>

<!-- In your control’s template HTM file -->
<div data-dyn-bind="click: $control.ElementClicked"></div>
```

<span data-ttu-id="43993-321">次の例では、子要素のクリック イベントが親要素までバブル アップできなくなります。</span><span class="sxs-lookup"><span data-stu-id="43993-321">The following example prevents the click event on child elements from bubbling up to parent elements.</span></span> <span data-ttu-id="43993-322">次の例では、子要素をクリックするとメッセージ「こんにちは」を含む警告が 1 つだけ表示されます。</span><span class="sxs-lookup"><span data-stu-id="43993-322">The example below will show only one alert with message “Hello” when the child element is clicked.</span></span>

```
// In your control’s code-behind JS file
<script>
... // boilerplate code
self.ParentElementClicked = function (event) {
    /* handle the click event */
    alert('Hi');
};

self.ElementClicked = function (event) {
    /* prevents the event form bubbling up to parent elements*/
    event.stopPropagation();

    /* handle the click event */
    alert('Hello');
};

...
</script>

<!-- In your control’s template HTM file -->
<div data-dyn-bind="click: $control.ParentElementClicked">
<div data-dyn-bind="click: $control.ElementClicked"></div>
</div>
```

<span data-ttu-id="43993-323">次の例では、ブラウザの既定の動作が実行できなくなります。</span><span class="sxs-lookup"><span data-stu-id="43993-323">The following example prevents the browser default behavior from executing.</span></span> <span data-ttu-id="43993-324">アンカー タグについては、既定のハイパーリンク動作が防止されるため、要素のクリック時にブラウザーがリンクに移動しません。</span><span class="sxs-lookup"><span data-stu-id="43993-324">For anchor tags, the default hyperlink behavior is prevented, so the browser will not navigate to the link when the element is clicked.</span></span>

```
// In your control’s code-behind JS file
<script>
... // boilerplate code
self.LinkClicked = function (event) {
        /* handle the click event */
        alert($dyn.format('Navigation to ' + {0} + ' was prevented', $(event.target).attr("href")));

        /* prevents the default event behavior */
        event.preventDefault();
};
</script>

<!-- In your control’s template HTM file -->
<a href="http://www.microsoft.com" data-dyn-bind="click: $control.LinkClicked">Click here</a>
```

#### <a name="css"></a><span data-ttu-id="43993-325">css</span><span class="sxs-lookup"><span data-stu-id="43993-325">css</span></span>

##### <a name="behavior"></a><span data-ttu-id="43993-326">動作</span><span class="sxs-lookup"><span data-stu-id="43993-326">Behavior</span></span>

<span data-ttu-id="43993-327">指定された条件に基づいて、指定された CSS クラス名を追加または削除します。</span><span class="sxs-lookup"><span data-stu-id="43993-327">Adds or removes the specified CSS class name(s) to the element, based on the specified condition(s).</span></span> <span data-ttu-id="43993-328">バインディング ハンドラーに指定された式は 1 回だけ実行されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="43993-328">Note that expressions supplied to the binding handler are only executed once.</span></span>

##### <a name="arguments"></a><span data-ttu-id="43993-329">引数</span><span class="sxs-lookup"><span data-stu-id="43993-329">Arguments</span></span>

<span data-ttu-id="43993-330">引数は、オブジェクト配列として渡されます。</span><span class="sxs-lookup"><span data-stu-id="43993-330">The arguments are passed in as an object array.</span></span> <span data-ttu-id="43993-331">各引数は、デュアル値です。</span><span class="sxs-lookup"><span data-stu-id="43993-331">Each argument is dual-valued.</span></span> <span data-ttu-id="43993-332">最初の値はクラス名で、2 番目の値は条件です。</span><span class="sxs-lookup"><span data-stu-id="43993-332">The first value is the Class name, and the second value is the Condition.</span></span>

###### <a name="class-name-string"></a><span data-ttu-id="43993-333">クラス名 (文字列)</span><span class="sxs-lookup"><span data-stu-id="43993-333">Class name (string)</span></span>

<span data-ttu-id="43993-334">要素に追加する CSS クラス名。</span><span class="sxs-lookup"><span data-stu-id="43993-334">The CSS class name to add to the element.</span></span>

###### <a name="condition-expression"></a><span data-ttu-id="43993-335">条件 (式)</span><span class="sxs-lookup"><span data-stu-id="43993-335">Condition (expression)</span></span>

<span data-ttu-id="43993-336">CSS クラス名を追加する条件。</span><span class="sxs-lookup"><span data-stu-id="43993-336">The condition on which to add the CSS class name.</span></span> <span data-ttu-id="43993-337">条件が true の場合は、CSS のクラス名は追加されます。</span><span class="sxs-lookup"><span data-stu-id="43993-337">If the condition evaluates to true, the CSS class name is added.</span></span> <span data-ttu-id="43993-338">条件が false の場合は、CSS のクラス名は削除されます。</span><span class="sxs-lookup"><span data-stu-id="43993-338">If the condition evaluates to false, the CSS class name is removed.</span></span> <span data-ttu-id="43993-339">指定した条件が監視可能な値 ($ dyn.value 経由) に依存する場合、監視可能な値が変わるたびに条件が再評価され、関連する CSS クラス名が新しい条件に基づいて追加/削除されます。</span><span class="sxs-lookup"><span data-stu-id="43993-339">If a supplied condition takes a dependency on an observable (via $dyn.value), then the condition will be re-evaluated whenever the observable value changes, and the associated CSS class name will be added/removed based on the new condition.</span></span> <span data-ttu-id="43993-340">次の例では、CSS クラス名 「red」、「green」、および「yellow」を追加します。</span><span class="sxs-lookup"><span data-stu-id="43993-340">The following example adds the CSS class names "red", "green", and "yellow".</span></span>

```
// In your control’s code-behind JS file
<script>
... // boilerplate code
self.red = function () { return true; };
self.yellow = $dyn.observable(true);
...
</script>

<!-- the markup in the HTML template -->
<div data-dyn-bind="css: {green: true, red: $control.red, yellow: $dyn.value($control.yellow)}"></div>

<!-- the markup in the browser after the binding handler is applied -->
<div class="green red yellow" data-dyn-bind="css: {green: true, red: $data.red, yellow: $dyn.value($control.yellow) }"></div>
```

#### <a name="event"></a><span data-ttu-id="43993-341">イベント</span><span class="sxs-lookup"><span data-stu-id="43993-341">event</span></span>

##### <a name="behavior"></a><span data-ttu-id="43993-342">動作</span><span class="sxs-lookup"><span data-stu-id="43993-342">Behavior</span></span>

<span data-ttu-id="43993-343">指定した DOM イベントに指定されたイベントをサブスクライブします。</span><span class="sxs-lookup"><span data-stu-id="43993-343">Subscribes the supplied event handler to the specified DOM event.</span></span> <span data-ttu-id="43993-344">サポートされている DOM イベントの一覧については、[jQuery - イベント](http://api.jquery.com/Types/#Event) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="43993-344">For a list of supported DOM events, see [jQuery - Event](http://api.jquery.com/Types/#Event).</span></span>

##### <a name="arguments"></a><span data-ttu-id="43993-345">引数</span><span class="sxs-lookup"><span data-stu-id="43993-345">Arguments</span></span>

<span data-ttu-id="43993-346">イベント バインディング ハンドラーへの引数の詳細については、[jQuery - .bind()](http://api.jquery.com/bind/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="43993-346">For details on the arguments to the event binding handler, see [jQuery - .bind()](http://api.jquery.com/bind/).</span></span> <span data-ttu-id="43993-347">次の例では、mouseover イベントにサブスクライブし、要素がポイントされたときにアラートを表示します。</span><span class="sxs-lookup"><span data-stu-id="43993-347">The following example subscribes to the mouseover event and shows an alert when the element is hovered.</span></span>

```
// In your control’s code-behind JS file
<script>
... // boilerplate code
self.elementHovered = function (event) { alert($dyn.format('{0}',$(event.target).text()))};
...
</script>

<!-- the markup in the HTML template -->
<div data-dyn-bind="event: {mouseover: $data.elementHovered}">Greetings!</div>
```

#### <a name="foreach"></a><span data-ttu-id="43993-348">foreach</span><span class="sxs-lookup"><span data-stu-id="43993-348">foreach</span></span>

##### <a name="behavior"></a><span data-ttu-id="43993-349">動作</span><span class="sxs-lookup"><span data-stu-id="43993-349">Behavior</span></span>

<span data-ttu-id="43993-350">渡されたデータに基づいて各子のバインド コンテキストを更新して、子要素の内容を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="43993-350">Repeats the content of the child element, updating the binding context of each child based on the supplied data.</span></span> <span data-ttu-id="43993-351">**foreach** バインディングを持つ要素内の子要素を ***1 つだけ***指定します。</span><span class="sxs-lookup"><span data-stu-id="43993-351">Supply ***only one*** child element inside of the element with the **foreach** binding.</span></span> <span data-ttu-id="43993-352">この 1 つの要素は、複製され、繰り返される要素です。</span><span class="sxs-lookup"><span data-stu-id="43993-352">This one element is the element that will be cloned and repeated.</span></span> <span data-ttu-id="43993-353">バインディングが適用される場合に、その他の追加要素またはコンテンツは削除されます。</span><span class="sxs-lookup"><span data-stu-id="43993-353">Any other additional elements or content will be removed when the binding is applied.</span></span> <span data-ttu-id="43993-354">要素に表示される順序でバインディング ハンドラーが実行されます。</span><span class="sxs-lookup"><span data-stu-id="43993-354">Binding handlers are executed in the order in which they appear on the element.</span></span> <span data-ttu-id="43993-355">**foreach** バンディングによりバインディング コンテキストが変わるため、必ず **foreach** バインディングは要素の他のすべてのバインディングより後に配置することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="43993-355">Since the **foreach** binding changes the binding context, it is a best practice to always place the **foreach** binding after all other bindings on the element.</span></span> <span data-ttu-id="43993-356">これにより、先行するバインドは、**foreach** バインドによって作成されたバインド コンテキストの影響を受けないことが保証されます。</span><span class="sxs-lookup"><span data-stu-id="43993-356">This will ensure that preceding bindings are not affected by the binding context created by the **foreach** binding.</span></span> <span data-ttu-id="43993-357">パフォーマンスの問題を避けるために、**foreach** 内の observable に意図しない依存関係を生成しないように注意してください。</span><span class="sxs-lookup"><span data-stu-id="43993-357">To avoid performance issues, be careful to not create unintentional dependencies on observables inside of your **foreach.**</span></span> <span data-ttu-id="43993-358">**foreach** バインドが配列内の監視可能にすでにサブスクライブされている際は、**foreach** の子要素の中から **$dyn.value** を使って配列内の監視可能にアクセスしないでください。</span><span class="sxs-lookup"><span data-stu-id="43993-358">Do not access an observable in the array using **$dyn.value** from within the child elements of the **foreach,** as the **foreach** binding has already subscribed to the observables in the array.</span></span> <span data-ttu-id="43993-359">代わりに、**$dyn.peek** を使用してサブスクリプションを作成せずにオブザーバブルの値に一度アクセスします。</span><span class="sxs-lookup"><span data-stu-id="43993-359">Instead, use **$dyn.peek** to access an observable’s value once without creating a subscription.</span></span>

##### <a name="arguments"></a><span data-ttu-id="43993-360">引数</span><span class="sxs-lookup"><span data-stu-id="43993-360">Arguments</span></span>

###### <a name="data-array-list-or-json-object"></a><span data-ttu-id="43993-361">データ (配列リストまたは JSON オブジェクト)</span><span class="sxs-lookup"><span data-stu-id="43993-361">Data (array list or JSON object)</span></span>

<span data-ttu-id="43993-362">子要素をバインドする項目のリスト。</span><span class="sxs-lookup"><span data-stu-id="43993-362">The list of items to bind the child element to.</span></span> <span data-ttu-id="43993-363">配列リストを指定する場合は、配列内の品目はバインド コンテキストです。</span><span class="sxs-lookup"><span data-stu-id="43993-363">If an array list is supplied, the binding context is an item in the array.</span></span> <span data-ttu-id="43993-364">JSON オブジェクト配列が指定されている場合、拘束力のあるコンテキストは、オブジェクトのプロパティのいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="43993-364">If a JSON object array is supplied, the binding context is one of the object’s properties.</span></span>

##### <a name="scope-variables"></a><span data-ttu-id="43993-365">スコープ変数</span><span class="sxs-lookup"><span data-stu-id="43993-365">Scope variables</span></span>

<span data-ttu-id="43993-366">**foreach** のスコープの範囲内では、次のスコープ変数が有用であり、反復可能な子要素である $data、インデックス、コントロール、ユーザー独自のスコープ変数で使用できます。</span><span class="sxs-lookup"><span data-stu-id="43993-366">When inside the scope of the **foreach,** the following scope variables are useful and can be used on the repeatable child element: $data, index, control, your own scope variables.</span></span> <span data-ttu-id="43993-367">次の例では、**foreach** を使用して配列の各色の期間要素を表示します。</span><span class="sxs-lookup"><span data-stu-id="43993-367">The following example uses **foreach** to render a span element for each color in the array.</span></span>

```
// In your control’s code-behind JS file
<script>
... // boilerplate code
self.colors = ['Red','Blue','Green'];
...
</script>

<!-- the markup in the HTML template -->
<div data-dyn-bind="foreach: $control.Colors">
<span data-dyn-bind="text: $data"></span>
</div>

<!-- the markup in the browser after the binding handler is applied -->
<div data-dyn-bind="foreach: $control.colors">
<span data-dyn-bind="text: $data">Red</span>
<span data-dyn-bind="text: $data">Blue</span>
<span data-dyn-bind="text: $data">Green</span>
</div>
```

<span data-ttu-id="43993-368">次の例では、入れ子になった **foreach** バインディングを示しています。</span><span class="sxs-lookup"><span data-stu-id="43993-368">The following examples shows a nested **foreach** binding.</span></span> <span data-ttu-id="43993-369">この例では、インデックス フレームワーク スコープ変数とカスタム スコープ変数を使用して、親要素からバインド コンテキストにアクセスする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="43993-369">This example showcases how to use the index framework scope variable and custom scope variables to access the binding context from the parent element.</span></span>

```
    // In your control’s code-behind JS file
<script>
... // boilerplate code
self.colors = [
    {
        Name: 'Red',
        Variants: ['Maroon','Burgundy','Sunrise']
    },
    {
        Name: 'Green',
        Variants: ['Sage','Forest','Lime']
    },
    {
        Name: 'Blue',
        Variants: ['Navy','Sky','Ice']
    }
];
...
</script>
<!-- the markup in the HTML template -->
<div data-dyn-bind="foreach: $control.colors">
<div data-dyn-bind="vars: {$BaseIndex: $index, $BaseColor: $data.Name}">
<div data-dyn-bind="foreach: $data.Variants">
<div data-dyn-bind="text: $BaseIndex+'.'+$index+' '+$data+' '+$BaseColor"></div>
</div>
</div>
</div>
<!-- the markup in the browser after the binding handler is applied -->
<div data-dyn-bind="foreach...">
<div data-dyn-bind="vars...">
<div data-dyn-bind="foreach...">
<div data-dyn-bind="vars...foreach...">
<div data-dyn-bind="text...">1.1 (0.2552) X++ Language</div>
<div data-dyn-bind="text...">1.2 (0.7) Applications</div>
</div>
</div>
<div data-dyn-bind="vars...">
<div data-dyn-bind="text...">2. (600) Technology</div>
<div data-dyn-bind="vars... foreach...">
<div data-dyn-bind="text...">2.1 (600.343) Microsoft Corporation</div>
<div data-dyn-bind="text...">2.2 (600.117) Enterprise Resource Planning</div>
</div>
</div>
</div>
```

#### <a name="if"></a><span data-ttu-id="43993-370">if</span><span class="sxs-lookup"><span data-stu-id="43993-370">if</span></span>

##### <a name="behavior"></a><span data-ttu-id="43993-371">動作</span><span class="sxs-lookup"><span data-stu-id="43993-371">Behavior</span></span>

<span data-ttu-id="43993-372">このバインドで要素の子要素を条件付きでレンダリングおよびバインドします。</span><span class="sxs-lookup"><span data-stu-id="43993-372">Conditionally renders and binds the child elements of the element with this binding.</span></span> <span data-ttu-id="43993-373">このバインディング ハンドラーは、子要素に対してのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="43993-373">This binding handler only operates on the child elements.</span></span> <span data-ttu-id="43993-374">バインディングのある要素を表示/非表示せず、このバインディングもバインディングのある要素のテキスト内容を表示/非表示しません。</span><span class="sxs-lookup"><span data-stu-id="43993-374">It will not show/hide the element with the binding, nor will this binding show/hide the text content of the element with the binding.</span></span> <span data-ttu-id="43993-375">子要素のバインディングは条件が true と評価される場合にのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="43993-375">Bindings on the child elements will only be executed if the condition evaluates to true.</span></span> <span data-ttu-id="43993-376">子要素のバインディングが一度評価されると、条件が false に変更されてもデータ バインドされたままになります。</span><span class="sxs-lookup"><span data-stu-id="43993-376">Once the bindings on child elements have been evaluated once they will remain data bound even if the condition changes to false.</span></span> <span data-ttu-id="43993-377">これは、子要素へのバインディングによって引き起こされる計算は、子要素が非表示になった後でも引き続き動作することを意味します。</span><span class="sxs-lookup"><span data-stu-id="43993-377">This means that any calculations caused by bindings on child elements will continue to operate even after the child elements are hidden.</span></span> <span data-ttu-id="43993-378">コントロールのパフォーマンスを評価する際にこれを考慮してください。</span><span class="sxs-lookup"><span data-stu-id="43993-378">Consider this when evaluating the performance of your control.</span></span>

##### <a name="arguments"></a><span data-ttu-id="43993-379">引数</span><span class="sxs-lookup"><span data-stu-id="43993-379">Arguments</span></span>

###### <a name="condition-expression"></a><span data-ttu-id="43993-380">条件 (式)</span><span class="sxs-lookup"><span data-stu-id="43993-380">Condition (expression)</span></span>

<span data-ttu-id="43993-381">子要素を表示するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="43993-381">Determines whether to render the children elements.</span></span> <span data-ttu-id="43993-382">次の例では、**show** および **text** 要素を条件付きでバインドしています。</span><span class="sxs-lookup"><span data-stu-id="43993-382">The following example conditionally binds the **show** and **text** elements.</span></span>

```
    // In your control’s code-behind JS file
<script>
... // boilerplate code
self.show = $dyn.observable(false);
self.text = "Hello";
...
</script>
<!-- the markup in the HTML template -->
<div data-dyn-bind="if: $control.show">
<div data-dyn-bind="text: $control.text"></div>
</div>
<!-- the markup in the browser after the binding handler is applied -->
<div data-dyn-bind="if: $control.show">
</div>
// Later on, the value of the “show” observable changes to true
<script>
...
self.show(true);
...
</script>
<!-- the markup in the browser after the binding handler is re-applied due to the observable value changing -->
<div data-dyn-bind="if: $control.show">
<div data-dyn-bind="text: $control.text">Hello</div>
</div>
```

#### <a name="sizing"></a><span data-ttu-id="43993-383">sizing</span><span class="sxs-lookup"><span data-stu-id="43993-383">sizing</span></span>

##### <a name="behavior"></a><span data-ttu-id="43993-384">動作</span><span class="sxs-lookup"><span data-stu-id="43993-384">Behavior</span></span>

<span data-ttu-id="43993-385">コントロールの高さと幅を指定します。</span><span class="sxs-lookup"><span data-stu-id="43993-385">Specifies the height and width of the control.</span></span> <span data-ttu-id="43993-386">サイズ変更バインド ハンドラーは、常にテンプレートのルート要素 (id 属性を持つ要素) に適用し、$dyn.layout.sizing ヘルパー関数を使用してコントロールの X++ インスタンスから height 値と width 値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43993-386">The sizing binding handler should always be applied to the root element of the template (the element that has the id attribute), and supplied the height and width values from the X++ instance of the control by using the $dyn.layout.sizing helper function.</span></span> <span data-ttu-id="43993-387">例 1 を参照してください。</span><span class="sxs-lookup"><span data-stu-id="43993-387">See Example 1.</span></span>

##### <a name="arguments"></a><span data-ttu-id="43993-388">引数</span><span class="sxs-lookup"><span data-stu-id="43993-388">Arguments</span></span>

<span data-ttu-id="43993-389">引数には、高さと幅のプロパティを含むオブジェクトが渡されます。</span><span class="sxs-lookup"><span data-stu-id="43993-389">The arguments are passed an object containing height and width properties.</span></span>

###### <a name="height-int"></a><span data-ttu-id="43993-390">高さ (int)</span><span class="sxs-lookup"><span data-stu-id="43993-390">Height (int)</span></span>

<span data-ttu-id="43993-391">バインディング ハンドラーが適用される要素の高さをピクセル単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="43993-391">Determines the height in pixels of the element on which the binding handler is applied.</span></span>

###### <a name="width-int"></a><span data-ttu-id="43993-392">幅 (整数)</span><span class="sxs-lookup"><span data-stu-id="43993-392">Width (int)</span></span>

<span data-ttu-id="43993-393">バインディング ハンドラーが適用される要素の幅をピクセル単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="43993-393">Determines the width in pixels of the element on which the binding handler is applied.</span></span> <span data-ttu-id="43993-394">次の例では、**MyControl** のサイズを指定しています。</span><span class="sxs-lookup"><span data-stu-id="43993-394">The following example specifies the size of **MyControl.**</span></span>

```
<!-- the markup in the HTML template -->
<!-- this boilerplate binding ensures that the control’s container is sized based on the height and width properties -->
<div id="MyControl" data-dyn-bind="sizing: $dyn.layout.sizing($control)"></div>
<!-- the markup in browser after the binding handler is applied will vary based on the height and width properties defined in $control -->
```

<span data-ttu-id="43993-395">次の例では、**bigbox** 変数の値に応じてコントロールを大きくまたは小さくします。</span><span class="sxs-lookup"><span data-stu-id="43993-395">The following example makes the control large or small depending on the value of the **bigbox** variable.</span></span>

```
// Later on, the value of the “show” observable changes to true
<script>
...
self.bigBox = true;
...
</script>
<!-- the markup in the HTML template -->
<div data-dyn-bind="sizing: {height: $control.bigBox?50:10, width: $control.bigBox?50:10}"></div>
<!-- the markup in the browser after the binding handler is applied -->
<div style="width: 50px; height: 50px;" data-dyn-bind="sizing: {height: $control.bigBox?50:10, width: $control.bigBox?50:10}"></div>
```

#### <a name="text"></a><span data-ttu-id="43993-396">テキスト</span><span class="sxs-lookup"><span data-stu-id="43993-396">text</span></span>

##### <a name="behavior"></a><span data-ttu-id="43993-397">動作</span><span class="sxs-lookup"><span data-stu-id="43993-397">Behavior</span></span>

<span data-ttu-id="43993-398">要素の textContent プロパティにバインドします。</span><span class="sxs-lookup"><span data-stu-id="43993-398">Binds to the textContent property of the element.</span></span> <span data-ttu-id="43993-399">テキスト バインド ハンドラーは、UI テキストで使用するためのものです。</span><span class="sxs-lookup"><span data-stu-id="43993-399">The text binding handler is meant to be used with UI text.</span></span> <span data-ttu-id="43993-400">要素に文字列ではない値 (数値、日付、またはブール値など) をバインドすることはありません。</span><span class="sxs-lookup"><span data-stu-id="43993-400">It is not meant to bind non-string values (such as numbers, dates or Booleans) to the element.</span></span> <span data-ttu-id="43993-401">dyn.format 関数を使用して、すべての値を文字列に変換してからバインディング ハンドラーに渡します。</span><span class="sxs-lookup"><span data-stu-id="43993-401">Convert all values into strings before supplying them to the binding handler, by using the dyn.format function.</span></span> <span data-ttu-id="43993-402">テキスト バインド ハンドラーは、既存のコンテンツが HTML であるかシンプル テキストであるかにかかわらず、要素内のすべてのコンテンツをバインドで置き換えます。</span><span class="sxs-lookup"><span data-stu-id="43993-402">The text binding handler will replace all of the content inside of the element with the binding, whether or not the existing content is HTML or simple text.</span></span>

##### <a name="arguments"></a><span data-ttu-id="43993-403">引数</span><span class="sxs-lookup"><span data-stu-id="43993-403">Arguments</span></span>

###### <a name="text-string"></a><span data-ttu-id="43993-404">テキスト (文字列)</span><span class="sxs-lookup"><span data-stu-id="43993-404">Text (string)</span></span>

<span data-ttu-id="43993-405">バインドするテキスト。</span><span class="sxs-lookup"><span data-stu-id="43993-405">The text to bind to.</span></span> <span data-ttu-id="43993-406">次の例では、div 要素の textContext プロパティをコントロールの text プロパティにバインドします。</span><span class="sxs-lookup"><span data-stu-id="43993-406">The following example binds the textContext property of the div element to the text property on the control.</span></span>

```
// In your control’s code-behind JS file
<script>
... // boilerplate code
self.text = "Hello";
...
</script>
<!-- the markup in the HTML template -->
<div data-dyn-bind="text: $dyn.format('{0}',$control.text)"></div>
<!-- the markup in browser after the binding handler is applied -->
<div data-dyn-bind="text: $dyn.format('{0}',$control.text)">Hello</div>
```

#### <a name="vars"></a><span data-ttu-id="43993-407">vars</span><span class="sxs-lookup"><span data-stu-id="43993-407">vars</span></span>

##### <a name="behavior"></a><span data-ttu-id="43993-408">動作</span><span class="sxs-lookup"><span data-stu-id="43993-408">Behavior</span></span>

<span data-ttu-id="43993-409">指定された名前と値を持つ HTML スコープ変数を作成します。</span><span class="sxs-lookup"><span data-stu-id="43993-409">Creates an HTML scope variable with the supplied name and value.</span></span> <span data-ttu-id="43993-410">作成されたスコープ変数は、テンプレート内のバインドからのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="43993-410">The created scope variable is accessible only from bindings in the template.</span></span> <span data-ttu-id="43993-411">さらに、スコープ変数は子要素によって継承されます。</span><span class="sxs-lookup"><span data-stu-id="43993-411">In addition, the scope variable is inherited by child elements.</span></span> <span data-ttu-id="43993-412">要素に表示される順序でバインディング ハンドラーが実行されます。</span><span class="sxs-lookup"><span data-stu-id="43993-412">Binding handlers are executed in the order in which they appear on the element.</span></span> <span data-ttu-id="43993-413">vars バンディングによりバインディング コンテキストに変数が追加されるため、必ず vars バインディングは要素の他のすべてのバインディングより前に配置することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="43993-413">Since the vars binding adds variables to the binding context, it is a best practice to always place the vars binding before all other bindings on the element.</span></span> <span data-ttu-id="43993-414">これにより、後続のバインドが vars バインドによって追加されたスコープ変数に確実にアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="43993-414">This will ensure that the subsequent bindings can access scope variables added by the vars binding.</span></span> <span data-ttu-id="43993-415">以下の名前でスコープ変数を作成しないでください。$control、$data、$index、および $value は、フレームワーク スコープ変数に対して既に引当されています。</span><span class="sxs-lookup"><span data-stu-id="43993-415">Do not create scope variables with any of the following names, as these names are reserved for framework scope variables: $control, $data, $index, and $value.</span></span>

##### <a name="arguments"></a><span data-ttu-id="43993-416">引数</span><span class="sxs-lookup"><span data-stu-id="43993-416">Arguments</span></span>

###### <a name="scope-variables-object-array"></a><span data-ttu-id="43993-417">スコープ変数 (オブジェクト配列)</span><span class="sxs-lookup"><span data-stu-id="43993-417">Scope variables (object array)</span></span>

<span data-ttu-id="43993-418">スコープ変数名をキーとし、その値がスコープ変数の初期値であるオブジェクト配列。</span><span class="sxs-lookup"><span data-stu-id="43993-418">The object array whose keys are the scope variable names and whose values are the initial values for the scope variables.</span></span> <span data-ttu-id="43993-419">次の例では、"Hello" および "World" という名前のスコープ変数を作成し、その値を表示します。</span><span class="sxs-lookup"><span data-stu-id="43993-419">The following example creates scope variables named "Hello" and "World" and displays their values.</span></span>

```
<!-- the markup in the HTML template -->
<div data-dyn-bind="vars: {$myVar: 'Hello', $myObs: $dyn.observable('World')}">
<span data-dyn-bind="text: $dyn.format('{0} {1}!', $myVar, $myObs)">
</span>
</div>
<!-- the markup in browser after the binding handler is applied -->
<div data-dyn-bind="vars: {$myVar: 'Hello', $myObs: $dyn.observable('World')}">
<span data-dyn-bind="text: $dyn.format('{0} {1}!', $myVar, $myObs)">
Hello World!
</span>
</div>
```

##### <a name="example-2"></a><span data-ttu-id="43993-420">例 2</span><span class="sxs-lookup"><span data-stu-id="43993-420">Example 2</span></span>

<span data-ttu-id="43993-421">例については、foreach バインド ハンドラーの例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="43993-421">For an example, see the foreach binding handler examples.</span></span>

#### <a name="visible"></a><span data-ttu-id="43993-422">表示</span><span class="sxs-lookup"><span data-stu-id="43993-422">visible</span></span>

##### <a name="behavior"></a><span data-ttu-id="43993-423">動作</span><span class="sxs-lookup"><span data-stu-id="43993-423">Behavior</span></span>

<span data-ttu-id="43993-424">要素の表示を設定します。</span><span class="sxs-lookup"><span data-stu-id="43993-424">Sets the visibility of the element.</span></span> <span data-ttu-id="43993-425">常にテンプレートのルート要素に表示されているバインディング ハンドラーを供給し、X++ コントロールの*表示*プロパティからバインドします。</span><span class="sxs-lookup"><span data-stu-id="43993-425">Always supply the visible binding handler on the root element of the template, and bind to the *Visible* property from the X++ control.</span></span> <span data-ttu-id="43993-426">これにより、コントロールがフォーム開発者によって設定されている場合、またはフレームワークによって設定されている場合に、コントロールが*Visible* プロパティを確実に使用するようになります。</span><span class="sxs-lookup"><span data-stu-id="43993-426">This will ensure that the control respects the *Visible* property when it is set by a form developer or when it is set by the framework.</span></span> <span data-ttu-id="43993-427">*表示* X++ プロパティを false に設定してコントロールを初期化すると、フォームにコントロールが表示されず、コントロールのテンプレートがブラウザに読み込まれません。</span><span class="sxs-lookup"><span data-stu-id="43993-427">If a control is initialized with its *Visible* X++ property set to false, then the control will not appear on the form, and it the control’s template will not be loaded in the browser.</span></span> <span data-ttu-id="43993-428">コントロールの *Visible* X++ プロパティを後で true 設定する場合、コントロールのテンプレートが読み込まれ、その時点で、ブラウザーがインスタンス化されます。</span><span class="sxs-lookup"><span data-stu-id="43993-428">If the control’s *Visible* X++ property is set to true at a later time, then the control’s template will be loaded and instantiated in the browser at that time.</span></span> <span data-ttu-id="43993-429">コントロールの *Visible* X++ プロパティは、フォーム上の親コントロールから継承できます。</span><span class="sxs-lookup"><span data-stu-id="43993-429">A control’s *Visible* X++ property can be inherited from its parent controls on the form.</span></span> <span data-ttu-id="43993-430">要素の可視性は表示されているバインディング ハンドラーが適用されるかどうかにかかわりなく、親要素、コントロールおよびコンテナーに制御されます。</span><span class="sxs-lookup"><span data-stu-id="43993-430">An element’s visibility may be controlled by its parent elements, controls and containers, regardless of whether the visible binding handler is applied.</span></span> <span data-ttu-id="43993-431">カスケード表示の性質は標準的な HTML 動作であり、コントロール フレームワークに固有のものではありません。</span><span class="sxs-lookup"><span data-stu-id="43993-431">The cascading nature of visibility is a standard HTML behavior and is not specific to the control framework.</span></span>

##### <a name="arguments"></a><span data-ttu-id="43993-432">引数</span><span class="sxs-lookup"><span data-stu-id="43993-432">Arguments</span></span>

###### <a name="visible-boolean"></a><span data-ttu-id="43993-433">Visible (ブール値)</span><span class="sxs-lookup"><span data-stu-id="43993-433">Visible (boolean)</span></span>

<span data-ttu-id="43993-434">要素が表示されるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="43993-434">Determines whether the element is visible or not.</span></span> <span data-ttu-id="43993-435">次の例では、コントロールの最も外側の div 要素の可視性を設定します。</span><span class="sxs-lookup"><span data-stu-id="43993-435">The following example sets the visibility of the control's outermost div element.</span></span>

```
// In your control’s code-behind JS file
<script>
... // boilerplate code
self.Visible(false); // set the X++ observable property to false
...
</script>
<!-- the markup on the root element of the HTML template -->
<div id="MyControl" data-dyn-bind="visible: $control.Visible">Hello World!</div>
<!-- the markup in browser after the binding handler is applied -->
<div id="MyControl" style="display: none;" data-dyn-bind="visible: $control.Visible">Hello World!</div>
```

## <a name="html-scope-variables"></a><span data-ttu-id="43993-436">HTML: スコープ変数</span><span class="sxs-lookup"><span data-stu-id="43993-436">HTML: Scope variables</span></span>
<span data-ttu-id="43993-437">値をバインディング ハンドラーにバインドする場合に、スコープ変数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="43993-437">Scope variables can be used when binding values to binding handlers.</span></span> <span data-ttu-id="43993-438">スコープ変数には、コントロールの HTML テンプレート内からのみアクセスでき、データ バインディング属性でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="43993-438">Scope variables are only accessible from within the control’s HTML template, and can only be used with the data binding attribute.</span></span> <span data-ttu-id="43993-439">スコープ変数は、他の HTML 属性からもコントロールの JavaScript クラスからもアクセスできませんが、スコープ変数は、バインディング ハンドラーに渡されたインライン JavaScript 式、関数、JSON オブジェクトで使用できます。</span><span class="sxs-lookup"><span data-stu-id="43993-439">Scope variables are neither accessible from other HTML attributes nor from the control’s JavaScript class, but scope variables can be used in inline JavaScript expressions, functions and JSON objects that are passed to binding handlers.</span></span>

#### <a name="control"></a><span data-ttu-id="43993-440">$control</span><span class="sxs-lookup"><span data-stu-id="43993-440">$control</span></span>

<span data-ttu-id="43993-441">*$control* スコープ変数は、コントロールの JavaScript インスタンスのプロパティと関数にアクセスできる HTML テンプレートでバインドを提供します。</span><span class="sxs-lookup"><span data-stu-id="43993-441">The *$control* scope variable provides the bindings in the HTML template with access to the properties and functions on the control’s JavaScript instance.</span></span> <span data-ttu-id="43993-442">次の例では、div 要素の表示をコントロールの表示プロパティにバインドします。</span><span class="sxs-lookup"><span data-stu-id="43993-442">The following example binds visibility of the div element to the of Visible property of the control.</span></span>

```
<div id="MyControl" data-dyn-bind="visible: $control.Visible"></div>
```

#### <a name="data"></a><span data-ttu-id="43993-443">$data</span><span class="sxs-lookup"><span data-stu-id="43993-443">$data</span></span>

<span data-ttu-id="43993-444">*$data* スコープ変数は、現在のバンディング コンテキストへのアクセスを持つ要素を提供します。</span><span class="sxs-lookup"><span data-stu-id="43993-444">The *$data* scope variable provides elements with access to their current binding context.</span></span> <span data-ttu-id="43993-445">$data 内で定義される変数 (バインド コンテキスト) またはスコープ変数のみ HTML バインディング内で使用されます。</span><span class="sxs-lookup"><span data-stu-id="43993-445">Only variables defined in $data (the binding context) or scope variables, can be used inside of HTML bindings.</span></span> <span data-ttu-id="43993-446">現在のバインディング コンテキストに存在せず、現在のスコープ変数として存在しない変数は、HTML バインディングからアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="43993-446">Variables that do not exist in the current binding context and do not exist as current scope variable cannot be accessed from an HTML binding.</span></span> <span data-ttu-id="43993-447">ほとんどの場合、バインド コンテキストはコントロールの JavaScript インスタンスとなるので、*$data* および *$control* と同じになります。</span><span class="sxs-lookup"><span data-stu-id="43993-447">In most cases the binding context will be the control’s JavaScript instance, so *$data* and *$control* will be equivalent.</span></span> <span data-ttu-id="43993-448">ただし、場合によってはバインド コンテキストを変更できます。</span><span class="sxs-lookup"><span data-stu-id="43993-448">However, in some cases the binding context can change.</span></span> <span data-ttu-id="43993-449">たとえば、**foreach**バインディング内の要素に対して、*$data* は現在の配列品目へのアクセスによる要素を提供します。</span><span class="sxs-lookup"><span data-stu-id="43993-449">For example, for elements inside of a **foreach** binding, *$data* provides the elements with access to the current array item.</span></span> <span data-ttu-id="43993-450">複数の入れ子になった **foreach** バインドが関連する場合、入れ子になったバインドの要素は親の **foreach** バインドの配列品目へのアクセスを必要とする場合があります。</span><span class="sxs-lookup"><span data-stu-id="43993-450">In cases involving multiple nested **foreach** bindings, elements in a nested binding may need access to the array item in a parent **foreach** binding.</span></span> <span data-ttu-id="43993-451">親の **foreach** バインドの項目にアクセスするには、入れ子になった **foreach** バインドの要素にアクセス可能なスコープ変数を作成できます。</span><span class="sxs-lookup"><span data-stu-id="43993-451">To access items in the parent **foreach** binding, you may create a scope variable which will be accessible to elements in the nested **foreach** biding.</span></span> <span data-ttu-id="43993-452">例については、foreach バインド ハンドラーの例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="43993-452">For an example, see the foreach binding handler examples.</span></span>

#### <a name="index"></a><span data-ttu-id="43993-453">$index</span><span class="sxs-lookup"><span data-stu-id="43993-453">$index</span></span>

<span data-ttu-id="43993-454">$index スコープ変数は、**foreach** バインディングに含まれる場合、配列項目の 0 から始まるインデックスを提供します。</span><span class="sxs-lookup"><span data-stu-id="43993-454">The $index scope variable provides a 0-based index of the array item when in a **foreach** binding.</span></span> <span data-ttu-id="43993-455">例については、foreach バインド ハンドラーの例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="43993-455">For an example, see the foreach binding handler examples.</span></span>

## <a name="javascript-inherited-properties"></a><span data-ttu-id="43993-456">JavaScript: 継承されたプロパティ</span><span class="sxs-lookup"><span data-stu-id="43993-456">JavaScript: Inherited properties</span></span>
#### <a name="visible"></a><span data-ttu-id="43993-457">表示</span><span class="sxs-lookup"><span data-stu-id="43993-457">Visible</span></span>

<span data-ttu-id="43993-458">**Visible** プロパティは、ベース JavaScript クラスから継承されます (**$dyn.ui.Controls.apply** 経由)。</span><span class="sxs-lookup"><span data-stu-id="43993-458">The **Visible** property is inherited from the base JavaScript class (via **$dyn.ui.Controls.apply**).</span></span> <span data-ttu-id="43993-459">ランタイムクラスが基本 **FormControl** X++ クラスから継承する X++ には、**Visible** プロパティもあります。</span><span class="sxs-lookup"><span data-stu-id="43993-459">There is also a **Visible** property in X++ that the runtime class in inherits from the base **FormControl** X++ class.</span></span> <span data-ttu-id="43993-460">このプロパティを表示されたバインディング ハンドラーにそのままバインドし、コントロールの HTML テンプレートのルート要素に配置します。</span><span class="sxs-lookup"><span data-stu-id="43993-460">Simply bind this property to the visible binding handler and place it on the root element of the HTML template for your control.</span></span> <span data-ttu-id="43993-461">このフレームワークは残りの部分を処理します。</span><span class="sxs-lookup"><span data-stu-id="43993-461">The framework takes care of the rest.</span></span> <span data-ttu-id="43993-462">次の例は、表示プロパティの使用方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="43993-462">The following example shows how to use the Visible property.</span></span>

```
<!-- the markup in the HTML template -->
<div id="MyControl" data-dyn-bind="visible: $control.Visible"></div>
```

## <a name="observable-framework"></a><span data-ttu-id="43993-463">監視可能なフレームワーク</span><span class="sxs-lookup"><span data-stu-id="43993-463">Observable framework</span></span>
#### <a name="dynobserve"></a><span data-ttu-id="43993-464">$dyn.observe</span><span class="sxs-lookup"><span data-stu-id="43993-464">$dyn.observe</span></span>

##### <a name="usage"></a><span data-ttu-id="43993-465">用途</span><span class="sxs-lookup"><span data-stu-id="43993-465">Usage</span></span>

<span data-ttu-id="43993-466">オブザーバブルの変更に関数をサブスクライブします。</span><span class="sxs-lookup"><span data-stu-id="43993-466">Subscribes a function to changes of an observable.</span></span> <span data-ttu-id="43993-467">廃棄を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="43993-467">We recommend that you use dispose.</span></span>

```
$dyn.observe(observable, observer, [context], [disposableObserver])
```

##### <a name="arguments"></a><span data-ttu-id="43993-468">引数</span><span class="sxs-lookup"><span data-stu-id="43993-468">Arguments</span></span>

###### <a name="observable-observable"></a><span data-ttu-id="43993-469">オブザーバブル (オブザーバブル)</span><span class="sxs-lookup"><span data-stu-id="43993-469">Observable (observable)</span></span>

<span data-ttu-id="43993-470">オブザーバブルのインスタンスです。</span><span class="sxs-lookup"><span data-stu-id="43993-470">Instance of an observable.</span></span> <span data-ttu-id="43993-471">または、関数 ($dyn.computed になります)。</span><span class="sxs-lookup"><span data-stu-id="43993-471">Or a function, which will become a $dyn.computed.</span></span>

###### <a name="observer-function"></a><span data-ttu-id="43993-472">オブザーバー (関数)</span><span class="sxs-lookup"><span data-stu-id="43993-472">Observer (function)</span></span>

<span data-ttu-id="43993-473">登録時およびのちにオブザーバブルが更新される際にも、関数が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="43993-473">Function is invoked upon registration and also later when the observable is updated.</span></span> <span data-ttu-id="43993-474">関数は 1 つの引数、オブザーバブルの値で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="43993-474">Function is invoked with one argument, the value of the observable.</span></span> <span data-ttu-id="43993-475">オブザーバーが false の場合、自動的に購読を解除します。</span><span class="sxs-lookup"><span data-stu-id="43993-475">If Observer returns false, then we un-subscribed automatically.</span></span>

###### <a name="context-options-optional"></a><span data-ttu-id="43993-476">コンテキスト (選択可、オプション)</span><span class="sxs-lookup"><span data-stu-id="43993-476">Context (options, optional)</span></span>

<span data-ttu-id="43993-477">オブザーバーに渡すコンテキスト。</span><span class="sxs-lookup"><span data-stu-id="43993-477">Context to pass to the Observer.</span></span> <span data-ttu-id="43993-478">コンテキストは、オブザーバーの内部で ***this*** 変数になります。</span><span class="sxs-lookup"><span data-stu-id="43993-478">The Context becomes the ***this*** variable inside of the observer.</span></span>

###### <a name="disposableobserver-options-optional"></a><span data-ttu-id="43993-479">DisposableObserver (選択可、オプション)</span><span class="sxs-lookup"><span data-stu-id="43993-479">DisposableObserver (options, optional)</span></span>

<span data-ttu-id="43993-480">付属の DisposableObserver の購読を取り消します</span><span class="sxs-lookup"><span data-stu-id="43993-480">Unsubscribes the supplied DisposableObserver</span></span>

##### <a name="returns"></a><span data-ttu-id="43993-481">返品</span><span class="sxs-lookup"><span data-stu-id="43993-481">Returns</span></span>

###### <a name="subscription-object"></a><span data-ttu-id="43993-482">サブスクリプション (オブジェクト)</span><span class="sxs-lookup"><span data-stu-id="43993-482">Subscription (object)</span></span>

<span data-ttu-id="43993-483">サブスクライブ解除に使用されたオブザーバブル、ID、Dispose 関数 (パブリック)。次の例は、myObs オブザーバブルをサブスクライブし、myObs オブザーバブルの値が変化すると必ず指定された関数を実行します。</span><span class="sxs-lookup"><span data-stu-id="43993-483">Observable, ID, Dispose function (public) used to unsubscribe The following example subscribes to the myObs observable, and executes the supplied function whenever the myObs observable value changes.</span></span>

```
$dyn.observe(myObs, function (value) { console.log(value);});
```

<span data-ttu-id="43993-484">次の例は、$dyn.value を使用してオブザーバブルの値にアクセスするだけで、関数がオブザーバブルの値に自動的にサブスクライブする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="43993-484">The following example shows how a function can automatically subscribe to observables simply by accessing the observable using $dyn.value.</span></span> <span data-ttu-id="43993-485">最初の関数は、他の 2 つの監視可能な値 (FirstName と LastName) の値に依存する監視可能な値のように扱われます。</span><span class="sxs-lookup"><span data-stu-id="43993-485">The first function is treated like an observable whose value is dependent upon the value of two other observables (FirstName and LastName).</span></span> <span data-ttu-id="43993-486">観測可能なオブジェクト (FirstName または LastName) のいずれかが値を変更するたびに、最初の関数の値も変更されます。</span><span class="sxs-lookup"><span data-stu-id="43993-486">Every time one of the observables  (FirstName or LastName) changes its value, then the first function has also changed its value.</span></span> <span data-ttu-id="43993-487">この場合、2 つ目の関数 (コールバック関数) は、観察可能な値の連結をコンソールに記録します。</span><span class="sxs-lookup"><span data-stu-id="43993-487">When this happens, the second function (the callback function) will log the concatenation of the observable values to the console.</span></span>

```
self.FirstName = $dyn.observable("Joanne");
self.LastName = $dyn.observable("Gordon");
$dyn.observe(
    function () {
        // Joann + " " + Gordon
        return $dyn.value(self.FirstName) + " " + $dyn.value(self.LastName);
    },
    function (value) {
        // "Joanne Gordon"
        console.log(value);
    }
);
```

<span data-ttu-id="43993-488">次の例は、前の例と同様に実行されます。</span><span class="sxs-lookup"><span data-stu-id="43993-488">The following example performs similarly to the previous example.</span></span> <span data-ttu-id="43993-489">ただし、この例では、連結を処理するために、myComp という名前の計算されたオブザーバブルを使用します。</span><span class="sxs-lookup"><span data-stu-id="43993-489">However, this example uses a computed observable, named myComp, to handle the concatenation.</span></span>

```
self.FirstName = $dyn.observable("Joanne");
self.LastName = $dyn.observable("Gordon");
self.myComp = $dyn.computed(function () {
    // Joanne + " " + Gordon
    return $dyn.value(self.FirstName) + " " + $dyn.value(self.LastName);
});
$dyn.observe(
    self.myComp,
    function (value) {
        // "Joanne Gordon"
        console.log(value)
    );
},
{FirstNameLabel: label1, LastNameLabel: label2}
);
```

#### <a name="dynobservable"></a><span data-ttu-id="43993-490">$dyn.observable</span><span class="sxs-lookup"><span data-stu-id="43993-490">$dyn.observable</span></span>

##### <a name="usage"></a><span data-ttu-id="43993-491">用途</span><span class="sxs-lookup"><span data-stu-id="43993-491">Usage</span></span>

<span data-ttu-id="43993-492">監視可能な変数を作成します。</span><span class="sxs-lookup"><span data-stu-id="43993-492">Creates an observable variable.</span></span>

```
$dyn.observable([initial value])
```

##### <a name="arguments"></a><span data-ttu-id="43993-493">引数</span><span class="sxs-lookup"><span data-stu-id="43993-493">Arguments</span></span>

###### <a name="initial-value-optional"></a><span data-ttu-id="43993-494">初期値 (オプション)</span><span class="sxs-lookup"><span data-stu-id="43993-494">Initial value (optional)</span></span>

<span data-ttu-id="43993-495">観測値を初期化する値。</span><span class="sxs-lookup"><span data-stu-id="43993-495">The value to initialize the observable to.</span></span>

##### <a name="returns"></a><span data-ttu-id="43993-496">返品</span><span class="sxs-lookup"><span data-stu-id="43993-496">Returns</span></span>

###### <a name="observable-function"></a><span data-ttu-id="43993-497">オブザーバブル (関数)</span><span class="sxs-lookup"><span data-stu-id="43993-497">Observable (function)</span></span>

<span data-ttu-id="43993-498">新しく作成された observable。次の例では、「Hello」という名前の変数を作成し、それを監視します。</span><span class="sxs-lookup"><span data-stu-id="43993-498">The newly created observable The following example creates and observable variable named "Hello".</span></span>

    var greeting = $dyn.observable("Hello");

#### <a name="dynvalue"></a><span data-ttu-id="43993-499">$dyn.value</span><span class="sxs-lookup"><span data-stu-id="43993-499">$dyn.value</span></span>

##### <a name="usage"></a><span data-ttu-id="43993-500">用途</span><span class="sxs-lookup"><span data-stu-id="43993-500">Usage</span></span>

<span data-ttu-id="43993-501">監視可能な変数の値にアクセス。</span><span class="sxs-lookup"><span data-stu-id="43993-501">Accesses the value of an observable variable.</span></span> <span data-ttu-id="43993-502">オブサーバー関数 (バインディング ハンドラーへ渡されるバインディング式だけでなく、**$dyn.observe** または **$dyn.computed** に渡されるオブザーバーなど) の内部から **$dyn.value** が呼び出されると、 観測可能なオブジェクトへの依存関係が作成されます。</span><span class="sxs-lookup"><span data-stu-id="43993-502">When **$dyn.value** is called from inside of an observer function (such as an observer passed to **$dyn.observe** or **$dyn.computed**, as well as the binding expression passed to a binding handler) a dependency on the observable is created.</span></span> <span data-ttu-id="43993-503">これにより、オブザーバブルの値が変更されるたびにバインディング ハンドラーまたはコールバックが再実行されます。</span><span class="sxs-lookup"><span data-stu-id="43993-503">This will cause the binding handler or callback to re-execute whenever the value of the observable changes.</span></span> <span data-ttu-id="43993-504">この依存関係は **$dyn.value** を使用すると自動的に作成されるため、このような依存関係を意図的に作成する場合は **$dyn.value** のみを使用することが重要です。</span><span class="sxs-lookup"><span data-stu-id="43993-504">Because this dependency is created automatically when using **$dyn.value**, it is important to only use **$dyn.value** when you intentionally wish to create such a dependency.</span></span> <span data-ttu-id="43993-505">依存関係を作成せずに observable の値にアクセスするには、$dyn.peek を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43993-505">If you wish to access the value of an observable without creating a dependency, you should use $dyn.peek.</span></span>

```
$dyn.value(observable)
```

##### <a name="arguments"></a><span data-ttu-id="43993-506">引数</span><span class="sxs-lookup"><span data-stu-id="43993-506">Arguments</span></span>

###### <a name="observable"></a><span data-ttu-id="43993-507">オブザーバブル</span><span class="sxs-lookup"><span data-stu-id="43993-507">Observable</span></span>

<span data-ttu-id="43993-508">値にアクセスできる監視可能なプロパティ。</span><span class="sxs-lookup"><span data-stu-id="43993-508">The observable property whose value to access.</span></span>

##### <a name="returns"></a><span data-ttu-id="43993-509">返品</span><span class="sxs-lookup"><span data-stu-id="43993-509">Returns</span></span>

###### <a name="value"></a><span data-ttu-id="43993-510">先頭値</span><span class="sxs-lookup"><span data-stu-id="43993-510">Value</span></span>

<span data-ttu-id="43993-511">監視可能なプロパティの現在の値。次の例では、observable という名前の変数を返し、コンソールに出力します。</span><span class="sxs-lookup"><span data-stu-id="43993-511">The current value in the observable property The following example returns the value of variable named observable and prints it to the console.</span></span>

```
console.log($dyn.value(observable));
```

#### <a name="dynpeek"></a><span data-ttu-id="43993-512">$dyn.peek</span><span class="sxs-lookup"><span data-stu-id="43993-512">$dyn.peek</span></span>

##### <a name="usage"></a><span data-ttu-id="43993-513">用途</span><span class="sxs-lookup"><span data-stu-id="43993-513">Usage</span></span>

<span data-ttu-id="43993-514">依存関係の作成なしで、監視可能な変数の値にアクセス。</span><span class="sxs-lookup"><span data-stu-id="43993-514">Accesses the value of an observable variable, without creating a dependency.</span></span> <span data-ttu-id="43993-515">依存関係の詳細については、$dyn.value 機能を参照してください。</span><span class="sxs-lookup"><span data-stu-id="43993-515">For more information about dependency, see the $dyn.value function.</span></span>

```
$dyn.peek(observable)
```

##### <a name="arguments"></a><span data-ttu-id="43993-516">引数</span><span class="sxs-lookup"><span data-stu-id="43993-516">Arguments</span></span>

###### <a name="observable"></a><span data-ttu-id="43993-517">オブザーバブル</span><span class="sxs-lookup"><span data-stu-id="43993-517">Observable</span></span>

<span data-ttu-id="43993-518">値にアクセスできる observable。</span><span class="sxs-lookup"><span data-stu-id="43993-518">The observable whose value to access.</span></span>

##### <a name="returns"></a><span data-ttu-id="43993-519">返品</span><span class="sxs-lookup"><span data-stu-id="43993-519">Returns</span></span>

###### <a name="value"></a><span data-ttu-id="43993-520">先頭値</span><span class="sxs-lookup"><span data-stu-id="43993-520">Value</span></span>

<span data-ttu-id="43993-521">監視可能な値の現在の値。次の例では、observable という名前の変数を返し、コンソールに出力します。</span><span class="sxs-lookup"><span data-stu-id="43993-521">The current value in the observable The following example returns the value of variable named observable and prints it to the console.</span></span>

```
console.log($dyn.peek(observable));
```

#### <a name="dyncomputed"></a><span data-ttu-id="43993-522">$dyn.computed</span><span class="sxs-lookup"><span data-stu-id="43993-522">$dyn.computed</span></span>

##### <a name="usage"></a><span data-ttu-id="43993-523">用途</span><span class="sxs-lookup"><span data-stu-id="43993-523">Usage</span></span>

<span data-ttu-id="43993-524">機能を監視範囲と共にラッピングします。</span><span class="sxs-lookup"><span data-stu-id="43993-524">Wraps a function with an observability scope.</span></span> <span data-ttu-id="43993-525">観測可能なオブジェクトを、**$dyn.value** 機能を使用して機能からアクセスする場合、その観測可能なオブジェクトの値が変更されるたびにこの機能を再度実行するようになります。</span><span class="sxs-lookup"><span data-stu-id="43993-525">If observables are accessed from inside of the function by using the **$dyn.value** function, then the function will re-execute whenever the values of those observables change.</span></span> <span data-ttu-id="43993-526">**$dyn.peek** を使用してアクセスされるオブザーバブルは、値が変わったときに関数を再実行しません。</span><span class="sxs-lookup"><span data-stu-id="43993-526">Observables that are accessed by using **$dyn.peek** will not cause the function to re-execute when their values change.</span></span>

```
$dyn.computed(observer, [context], [disposableObserver])
```

##### <a name="arguments"></a><span data-ttu-id="43993-527">引数</span><span class="sxs-lookup"><span data-stu-id="43993-527">Arguments</span></span>

###### <a name="observer-function"></a><span data-ttu-id="43993-528">オブザーバー (関数)</span><span class="sxs-lookup"><span data-stu-id="43993-528">Observer (function)</span></span>

<span data-ttu-id="43993-529">関数は登録時に呼び出され、および後に監視可能な値の変更のためにも呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="43993-529">Function is invoked upon registration and can also be invoked later due to an observable value change.</span></span> <span data-ttu-id="43993-530">オブザーバーは、関数の範囲内から $dyn.value を使用してアクセスされる任意の観測可能オブジェクトを自動的に監視します。</span><span class="sxs-lookup"><span data-stu-id="43993-530">The Observer automatically observes any observables that are accessed using $dyn.value from within the scope of the function.</span></span>

###### <a name="context-options-optional"></a><span data-ttu-id="43993-531">コンテキスト (選択可、オプション)</span><span class="sxs-lookup"><span data-stu-id="43993-531">Context (options, optional)</span></span>

<span data-ttu-id="43993-532">オブザーバーに渡すコンテキスト。</span><span class="sxs-lookup"><span data-stu-id="43993-532">Context to pass to the Observer.</span></span> <span data-ttu-id="43993-533">コンテキストは、オブザーバーの内部で *this* 変数になります。</span><span class="sxs-lookup"><span data-stu-id="43993-533">The Context becomes the *this* variable inside of the observer.</span></span>

###### <a name="disposableobserver-options-optional"></a><span data-ttu-id="43993-534">DisposableObserver (選択可、オプション)</span><span class="sxs-lookup"><span data-stu-id="43993-534">DisposableObserver (options, optional)</span></span>

<span data-ttu-id="43993-535">付属の DisposableObserver の購読を取り消します</span><span class="sxs-lookup"><span data-stu-id="43993-535">Unsubscribes the supplied DisposableObserver</span></span>

##### <a name="returns"></a><span data-ttu-id="43993-536">返品</span><span class="sxs-lookup"><span data-stu-id="43993-536">Returns</span></span>

###### <a name="anything-optional"></a><span data-ttu-id="43993-537">何でも (オプション)</span><span class="sxs-lookup"><span data-stu-id="43993-537">Anything (optional)</span></span>

<span data-ttu-id="43993-538">オブザーバーが値を返すと、その値は、最初に **$dyn.computed** への呼び出しによって返されます。**$dyn.computed** は、オブザーバーが呼び出されるたびに (登録時に) 呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="43993-538">If the Observer returns a value, then that value will also be returned by the call to **$dyn.computed** on the first time **$dyn.computed** is called (upon registration) as well every time the observer is invoked.</span></span>

## <a name="framework-functions"></a><span data-ttu-id="43993-539">フレームワーク機能</span><span class="sxs-lookup"><span data-stu-id="43993-539">Framework functions</span></span>
#### <a name="dyncallfunction"></a><span data-ttu-id="43993-540">$dyn.callFunction</span><span class="sxs-lookup"><span data-stu-id="43993-540">$dyn.callFunction</span></span>

##### <a name="usage"></a><span data-ttu-id="43993-541">用途</span><span class="sxs-lookup"><span data-stu-id="43993-541">Usage</span></span>

<span data-ttu-id="43993-542">指定された関数で適用メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="43993-542">Calls the apply method on specified function.</span></span> <span data-ttu-id="43993-543">インタラクション中は使用できません。</span><span class="sxs-lookup"><span data-stu-id="43993-543">Is cannot be used during an interaction.</span></span>

##### <a name="arguments"></a><span data-ttu-id="43993-544">引数</span><span class="sxs-lookup"><span data-stu-id="43993-544">Arguments</span></span>

###### <a name="function-function-or-observable"></a><span data-ttu-id="43993-545">関数 (関数またはオブザーバブル)</span><span class="sxs-lookup"><span data-stu-id="43993-545">Function (function or observable)</span></span>

<span data-ttu-id="43993-546">呼び出す関数。</span><span class="sxs-lookup"><span data-stu-id="43993-546">The function to call.</span></span> <span data-ttu-id="43993-547">監視可能なオブジェクトが指定されている場合、監視可能なオブジェクトの現在の値が取得され、関数として使用されます。</span><span class="sxs-lookup"><span data-stu-id="43993-547">If an observable is supplied, the current value of the observable will be retrieved and used as the function.</span></span>

###### <a name="this-object-optional"></a><span data-ttu-id="43993-548">この (オブジェクト、オプション)</span><span class="sxs-lookup"><span data-stu-id="43993-548">This (object, optional)</span></span>

<span data-ttu-id="43993-549">関数のスコープ内で、*this* に割り当てるオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="43993-549">The object to assign to *this* within the scope of the function.</span></span>

###### <a name="arguments-array-optional"></a><span data-ttu-id="43993-550">引数 (配列、省略可)</span><span class="sxs-lookup"><span data-stu-id="43993-550">Arguments (array, optional)</span></span>

<span data-ttu-id="43993-551">指定された関数に渡す引数。</span><span class="sxs-lookup"><span data-stu-id="43993-551">The arguments to pass to the supplied function.</span></span>

###### <a name="callback-function-optional"></a><span data-ttu-id="43993-552">コールバック (関数、オプション)</span><span class="sxs-lookup"><span data-stu-id="43993-552">Callback (function, optional)</span></span>

<span data-ttu-id="43993-553">指定された関数が返されたときに呼び出すコールバック関数。</span><span class="sxs-lookup"><span data-stu-id="43993-553">The callback function to call when the supplied Function has returned.</span></span> <span data-ttu-id="43993-554">コールバックには、呼び出された関数が返す値が渡されます。</span><span class="sxs-lookup"><span data-stu-id="43993-554">The callback will be passed any values that are returned by the function that is called.</span></span> <span data-ttu-id="43993-555">次の例では、**printName** 関数で **apply** 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="43993-555">The following example calls the **apply** function on the **printName** function.</span></span>

```
self.Name = "Joanne M Gordon";
var printName = function () {
    console.log(this.Name);
};
$dyn.callFunction(printName, self);
```

<span data-ttu-id="43993-556">次の例では、**getWholeName** 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="43993-556">The following example calls the **getWholeName** function.</span></span>

```
var getWholeName = function (first, middle, last) {
    var wholeName = first + " " + middle + " " + last;
    return wholeName;
};
var printName = function (wholeName) {
    console.log("Your name is: " + wholeName);
};
var firstName = "Joanne";
var middleName = "M";
var lastName = "Gordon";
$dyn.callFunction(getWholeName, null, [firstName , middleName, lastName], printName);
```

#### <a name="dynformat"></a><span data-ttu-id="43993-557">$dyn.format</span><span class="sxs-lookup"><span data-stu-id="43993-557">$dyn.format</span></span>

##### <a name="usage"></a><span data-ttu-id="43993-558">用途</span><span class="sxs-lookup"><span data-stu-id="43993-558">Usage</span></span>

<span data-ttu-id="43993-559">指定された形式に基づいて指定された値を使用する文字列を作成します。</span><span class="sxs-lookup"><span data-stu-id="43993-559">Builds a string using the supplied values according to the supplied format.</span></span>

##### <a name="arguments"></a><span data-ttu-id="43993-560">引数</span><span class="sxs-lookup"><span data-stu-id="43993-560">Arguments</span></span>

###### <a name="format-string"></a><span data-ttu-id="43993-561">形式 (文字列)</span><span class="sxs-lookup"><span data-stu-id="43993-561">Format (string)</span></span>

<span data-ttu-id="43993-562">文字列を作成する形式。</span><span class="sxs-lookup"><span data-stu-id="43993-562">The format in which to build the string.</span></span> <span data-ttu-id="43993-563">プレースホルダーにはブラケット表記を使用します。</span><span class="sxs-lookup"><span data-stu-id="43993-563">Use bracket notation for placeholders.</span></span>

###### <a name="values-optional"></a><span data-ttu-id="43993-564">値 (省略可)</span><span class="sxs-lookup"><span data-stu-id="43993-564">Values (optional)</span></span>

<span data-ttu-id="43993-565">このフォーマットで使用するコンマ区切りの値</span><span class="sxs-lookup"><span data-stu-id="43993-565">The comma separated values to use in the format</span></span>

##### <a name="returns"></a><span data-ttu-id="43993-566">返品</span><span class="sxs-lookup"><span data-stu-id="43993-566">Returns</span></span>

###### <a name="formattedstring-string"></a><span data-ttu-id="43993-567">FormattedString (文字列)</span><span class="sxs-lookup"><span data-stu-id="43993-567">FormattedString (string)</span></span>

<span data-ttu-id="43993-568">書式設定が適用された後の文字列次の例では、最初の文字列、中間の最初の文字列、最後の文字列を含む文字列を作成します。</span><span class="sxs-lookup"><span data-stu-id="43993-568">The string after formatting has been applied The following example builds a string with the first, middle initial, and the last name.</span></span>

##### <a name="example-1"></a><span data-ttu-id="43993-569">例 1</span><span class="sxs-lookup"><span data-stu-id="43993-569">Example 1</span></span>

```
var first = "Joanne";
var middle = "M";
var last = "Gordon";
var $dyn.format("Your name is : {0} {1} {2}", first, middle, last);
```

#### <a name="dynlabel"></a><span data-ttu-id="43993-570">$dyn.label</span><span class="sxs-lookup"><span data-stu-id="43993-570">$dyn.label</span></span>

##### <a name="usage"></a><span data-ttu-id="43993-571">用途</span><span class="sxs-lookup"><span data-stu-id="43993-571">Usage</span></span>

<span data-ttu-id="43993-572">グローバリゼーション API 経由で保存されている任意のラベルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="43993-572">Provides access to any labels stored via the Globalization API.</span></span>

##### <a name="arguments"></a><span data-ttu-id="43993-573">引数</span><span class="sxs-lookup"><span data-stu-id="43993-573">Arguments</span></span>

###### <a name="identifier-string"></a><span data-ttu-id="43993-574">ID (文字列)</span><span class="sxs-lookup"><span data-stu-id="43993-574">Identifier (string)</span></span>

<span data-ttu-id="43993-575">グローバリゼーション API に指定されているラベル ID。</span><span class="sxs-lookup"><span data-stu-id="43993-575">The label ID, as specified to the Globalization API.</span></span>

##### <a name="returns"></a><span data-ttu-id="43993-576">返品</span><span class="sxs-lookup"><span data-stu-id="43993-576">Returns</span></span>

###### <a name="value-string"></a><span data-ttu-id="43993-577">値 (文字列)</span><span class="sxs-lookup"><span data-stu-id="43993-577">Value (string)</span></span>

<span data-ttu-id="43993-578">識別子が見つかった場合の、現在のカルチャ内のラベル文字列。</span><span class="sxs-lookup"><span data-stu-id="43993-578">The label string in the current culture, if the Identifier is found.</span></span> <span data-ttu-id="43993-579">それ以外の場合、提供された識別子を文字列として返します。</span><span class="sxs-lookup"><span data-stu-id="43993-579">Otherwise, returns the supplied Identifier as a string.</span></span> <span data-ttu-id="43993-580">次の例では、"greeting" という名前のラベルを返して出力します。</span><span class="sxs-lookup"><span data-stu-id="43993-580">The following example returns and prints the label named "greeting".</span></span>

```
Globalize.addCultureInfo("en", {
    messages: {
        "greeting": "Hello!"
    },
});
console.log($dyn.label("greeting"));
```

## <a name="css"></a><span data-ttu-id="43993-581">CSS</span><span class="sxs-lookup"><span data-stu-id="43993-581">CSS</span></span>

<span data-ttu-id="43993-582">コントロールのテンプレート ID を持つクラス名を付加して、すべての CSS クラス名に名前空間を追加します。</span><span class="sxs-lookup"><span data-stu-id="43993-582">Add namespaces to all CSS class names by prepending the class name with the control’s template ID.</span></span> <span data-ttu-id="43993-583">これにより、コントロールとそのスタイルがクライアントの他のコントロールと競合するのを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="43993-583">This will prevent your control and its styles from conflicting with other controls in the client.</span></span>

## <a name="flexbox"></a><span data-ttu-id="43993-584">Flexbox</span><span class="sxs-lookup"><span data-stu-id="43993-584">Flexbox</span></span>
<span data-ttu-id="43993-585">高度なレイアウト シナリオでは、Flexbox の使用をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="43993-585">For advanced layout scenarios we encourage using Flexbox.</span></span> <span data-ttu-id="43993-586">Flexbox は、拡張可能な管理フレームワークと互換性があります。</span><span class="sxs-lookup"><span data-stu-id="43993-586">Flexbox is compatible with the Extensible Control framework.</span></span> <span data-ttu-id="43993-587">[CSS 変動ボックス (Mozilla 開発者ネットワーク) を使用する](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Using_CSS_flexible_boxes) 次のトピックの説明と例については [パブリック Flexbox ドキュメント](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Using_CSS_flexible_boxes) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="43993-587">[Using CSS flexible boxes (Mozilla Developer Network)](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Using_CSS_flexible_boxes) Please see the [public Flexbox documentation](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Using_CSS_flexible_boxes) for explanations and examples of the following topics:</span></span>

-   <span data-ttu-id="43993-588">反応の敏感なレイアウト</span><span class="sxs-lookup"><span data-stu-id="43993-588">Responsive layouts</span></span>
-   <span data-ttu-id="43993-589">列および行の構築</span><span class="sxs-lookup"><span data-stu-id="43993-589">Building columns and rows</span></span>
-   <span data-ttu-id="43993-590">水平垂直方向に要素を配置する</span><span class="sxs-lookup"><span data-stu-id="43993-590">Arranging elements horizontally or vertically</span></span>
-   <span data-ttu-id="43993-591">入れ子要素の階層化</span><span class="sxs-lookup"><span data-stu-id="43993-591">Arranging nesting elements</span></span>
-   <span data-ttu-id="43993-592">伸縮し縮小する要素の自動サイズ変更</span><span class="sxs-lookup"><span data-stu-id="43993-592">Auto-sizing elements to stretch and shrink</span></span>
-   <span data-ttu-id="43993-593">要素のロック/凍結</span><span class="sxs-lookup"><span data-stu-id="43993-593">Locking/Freezing elements</span></span>
-   <span data-ttu-id="43993-594">スクロール可能な要素の作成</span><span class="sxs-lookup"><span data-stu-id="43993-594">Building scrollable elements</span></span>

## <a name="control-lifecycle-diagrams"></a><span data-ttu-id="43993-595">制御ライフサイクル図</span><span class="sxs-lookup"><span data-stu-id="43993-595">Control Lifecycle Diagrams</span></span>

### <a name="control-instantiation"></a><span data-ttu-id="43993-596">インスタンス化の制御</span><span class="sxs-lookup"><span data-stu-id="43993-596">Control Instantiation</span></span>
<span data-ttu-id="43993-597">[![ExtensibilityProcess](./media/extensibilityprocess-951x1024.png)](./media/extensibilityprocess.png)</span><span class="sxs-lookup"><span data-stu-id="43993-597">[![ExtensibilityProcess](./media/extensibilityprocess-951x1024.png)](./media/extensibilityprocess.png)</span></span>
