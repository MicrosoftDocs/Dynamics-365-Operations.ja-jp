---
title: "拡張可能なコードの書き込み"
description: "このトピックでは、拡張可能コードを書き込む方法について説明します。"
author: MichaelFruergaardPontoppidan
manager: AnnBe
ms.date: 09/18/2018
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
ms.sourcegitcommit: 1aae5797e37b846a38f957b02870e213da528a2d
ms.openlocfilehash: d9c2e4772fce96ffcc302794df69bf556b4d6849
ms.contentlocale: ja-jp
ms.lasthandoff: 09/20/2018

---

# <a name="write-extensible-code"></a><span data-ttu-id="17d71-103">拡張可能なコードの書き込み</span><span class="sxs-lookup"><span data-stu-id="17d71-103">Write extensible code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17d71-104">X++ およびメタデータ モデルは、ビジネス ソリューションを構築するため強力な基礎を提供します。</span><span class="sxs-lookup"><span data-stu-id="17d71-104">X++ and the metadata model provide a powerful foundation for building business solutions.</span></span> <span data-ttu-id="17d71-105">デザインの柱の 1 つは、エンジニアがビジネス ドメインに焦点を当てることができるように、できるだけ多くの技術的な問題を自動化することです。</span><span class="sxs-lookup"><span data-stu-id="17d71-105">One of the design pillars is to automate as many technical concerns as possible, so that the engineer can focus on the business domain.</span></span> <span data-ttu-id="17d71-106">たとえば、ラベル ファイルにすべてのテキスト リソースを配置した場合、心配しなくてもよい 1 つの技術的な問題はテキスト リソースのローカライズです。</span><span class="sxs-lookup"><span data-stu-id="17d71-106">For example, if you put all the text resources in label files, one technical concern that you don't have to worry about is the localization of text resources.</span></span>

<span data-ttu-id="17d71-107">拡張性は、別の技術的な問題です。</span><span class="sxs-lookup"><span data-stu-id="17d71-107">Extensibility is another technical concern.</span></span> <span data-ttu-id="17d71-108">他のユーザーが安全かつ堅牢で管理可能な方法でソリューションを拡張できるようにします。</span><span class="sxs-lookup"><span data-stu-id="17d71-108">You want other people to be able to extend your solution in a safe, robust, and maintainable way.</span></span> <span data-ttu-id="17d71-109">既定では、ソリューションの拡張性は高くなっています。</span><span class="sxs-lookup"><span data-stu-id="17d71-109">By default, your solution is highly extensible.</span></span> <span data-ttu-id="17d71-110">ただし、完全性を保証するために従う必要のある、いくつかのガイドラインがあります。</span><span class="sxs-lookup"><span data-stu-id="17d71-110">However, there are a few guidelines that you should follow to help guarantee completeness.</span></span>

## <a name="responsibilities"></a><span data-ttu-id="17d71-111">職責</span><span class="sxs-lookup"><span data-stu-id="17d71-111">Responsibilities</span></span>
<span data-ttu-id="17d71-112">どの Microsoft Dynamics 365 for Finance and Operations 環境でも、さまざまなソースからコンポーネントを含むビジネス ソリューションが実行されています。</span><span class="sxs-lookup"><span data-stu-id="17d71-112">Any Microsoft Dynamics 365 for Finance and Operations environment runs a business solution that includes components from many sources.</span></span> <span data-ttu-id="17d71-113">通常、各ソリューションにはマイクロソフト、独立系ソフトウェア ベンダー (ISV)、パートナーのコード、さらに内部開発のコードも含まれています。</span><span class="sxs-lookup"><span data-stu-id="17d71-113">Typically, each solution has code from Microsoft, independent software vendors (ISVs) and partners, and also internally developed code.</span></span> <span data-ttu-id="17d71-114">各コントリビューターは、ソリューションへの自分の貢献と、自分の貢献が他のユーザーの貢献と関わる方法に責任を負っています。</span><span class="sxs-lookup"><span data-stu-id="17d71-114">Each contributor is responsible for its own contribution to the solution and for the way that its contribution interacts with other contributions.</span></span>

<span data-ttu-id="17d71-115">拡張可能コードを作成するとき、ソリューションを操作するよう他のユーザーを招待します。</span><span class="sxs-lookup"><span data-stu-id="17d71-115">When you write extensible code, you invite other people to interact with your solution.</span></span> <span data-ttu-id="17d71-116">自分の責任は、他のユーザーを適切なゲストにすることです。</span><span class="sxs-lookup"><span data-stu-id="17d71-116">Your responsibility is to enable other people to be good guests.</span></span> <span data-ttu-id="17d71-117">この責任を果たす方法を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="17d71-117">Here is how you meet this responsibility:</span></span>

+ <span data-ttu-id="17d71-118">**信頼性の高い拡張ポイントを作成する**: 拡張ポイントは拡張担当者のソリューションの土台部分です。</span><span class="sxs-lookup"><span data-stu-id="17d71-118">**Make robust extension points** – Extension points are the foundation of extenders' solutions.</span></span> <span data-ttu-id="17d71-119">適切に定義されていて、リリースごと堅牢である必要があります。</span><span class="sxs-lookup"><span data-stu-id="17d71-119">They must be well-defined and robust from release to release.</span></span>
+ <span data-ttu-id="17d71-120">**サイド バイ サイド カスタマイズを招待**: 複数の拡張担当者が同じ拡張ポイントを使用する場合があることを認識します。</span><span class="sxs-lookup"><span data-stu-id="17d71-120">**Invite side-by-side customizations** – Recognize that multiple extenders might use the same extension point.</span></span> <span data-ttu-id="17d71-121">1:1 (1 対 1) のやり取りではなく、1: n (1 対多) のやり取りを有効にします。</span><span class="sxs-lookup"><span data-stu-id="17d71-121">Enable 1:n (one-to-many) interactions instead of 1:1 (one-to-one) interactions.</span></span>
+ <span data-ttu-id="17d71-122">**拡張担当者が適切に行動することを信頼**: すべての責任者は、長続きする優れた顧客向けソリューションを作成するという同じ目標を共有します。</span><span class="sxs-lookup"><span data-stu-id="17d71-122">**Trust that extenders will be well-behaved** – All responsible parties share the same goal: to create great, lasting solutions for the customer.</span></span> <span data-ttu-id="17d71-123">拡張ポイントを作成するときは、コントロールを引き渡し、他のユーザーと責任を共有します。</span><span class="sxs-lookup"><span data-stu-id="17d71-123">When you create extension points, you give up control and share the responsibility with other people.</span></span> <span data-ttu-id="17d71-124">拡張担当者は慎重であり、意図した拡張ポイントを使用しているとみなします。</span><span class="sxs-lookup"><span data-stu-id="17d71-124">Assume that extenders will be cautious and use your extension points as they were intended.</span></span>

## <a name="proven-principles"></a><span data-ttu-id="17d71-125">実績のある原則</span><span class="sxs-lookup"><span data-stu-id="17d71-125">Proven principles</span></span>
<span data-ttu-id="17d71-126">既に使用している優れたエンジニアリングの手法がすべて適用されます。</span><span class="sxs-lookup"><span data-stu-id="17d71-126">All the good engineering practices that you're already using still apply.</span></span> <span data-ttu-id="17d71-127">学習したことすべても適用されます。</span><span class="sxs-lookup"><span data-stu-id="17d71-127">Everything that you've learned still applies.</span></span> <span data-ttu-id="17d71-128">新しい原則を習得したり、古い手法を忘れる必要はありません。</span><span class="sxs-lookup"><span data-stu-id="17d71-128">You don't have to learn new principles or unlearn old practices.</span></span> <span data-ttu-id="17d71-129">このトピックでは、何十年もの間求められ、教えられ続けてきた、ソフトウェア作成者が守るべき 3 つの原則だけ強調します。</span><span class="sxs-lookup"><span data-stu-id="17d71-129">This topic is just highlighting three principles of software craftmanship that have been sought and taught for decades.</span></span> <span data-ttu-id="17d71-130">これらの原則により、コードが読み取り、管理、テスト、確認、リファクタリングしやすくなるだけでなく、コードを簡単に拡張できるようにもなります。</span><span class="sxs-lookup"><span data-stu-id="17d71-130">These principles not only make your code easier to read, maintain, test, review, and refactor, but also make your code easier to extend.</span></span> <span data-ttu-id="17d71-131">これらの原則を適用して推奨します。</span><span class="sxs-lookup"><span data-stu-id="17d71-131">Apply and advocate these principles.</span></span>

### <a name="extend-code-by-using-the-solid-principles"></a><span data-ttu-id="17d71-132">SOLID を使用してコードを拡張する</span><span class="sxs-lookup"><span data-stu-id="17d71-132">Extend code by using the SOLID principles</span></span>
<span data-ttu-id="17d71-133">SOLID は、コードを簡単に拡張できるようにするために使用できる 5 つの原則の頭字語です。</span><span class="sxs-lookup"><span data-stu-id="17d71-133">SOLID is an acronym for five principles that you can use to make your code easier to extend:</span></span>

+ <span data-ttu-id="17d71-134">**1 つの責任**: クラスおよびメソッドには責任が 1 つでなければならず、副作用があってはなりません。</span><span class="sxs-lookup"><span data-stu-id="17d71-134">**Single responsibility** – Classes and method should have a single responsibility and should not have side-effects.</span></span> <span data-ttu-id="17d71-135">この原則に従うと、パブリックな保護された方法で自動的に作成される拡張ポイントが優れた拡張ポイントになることを保証することができます。</span><span class="sxs-lookup"><span data-stu-id="17d71-135">By following this principle, you help guarantee that extension points that are automatically created on public and protected methods will be great extension points.</span></span>
+ <span data-ttu-id="17d71-136">**オープン/クローズ**</span><span class="sxs-lookup"><span data-stu-id="17d71-136">**Open/closed**</span></span>

    - <span data-ttu-id="17d71-137">**拡張に対してオープン**: 拡張サーフェイスをデザインして検討することにより、拡張のソリューションを開きます。</span><span class="sxs-lookup"><span data-stu-id="17d71-137">**Open for extension** – Open your solution for extensions by designing and considering the extension surface.</span></span> <span data-ttu-id="17d71-138">拡張ポイントが使用可能になったら、管理を担当します。</span><span class="sxs-lookup"><span data-stu-id="17d71-138">After an extension point is made available, you're responsible for maintaining it.</span></span> <span data-ttu-id="17d71-139">この責任は、今後の開発に重要な制限を追加します。</span><span class="sxs-lookup"><span data-stu-id="17d71-139">This responsibility adds significant restrictions to future development.</span></span> <span data-ttu-id="17d71-140">多くの場合、需要に応じて拡張に対してソリューションを開くことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="17d71-140">It's often preferable to open a solution up for extension by demand.</span></span> <span data-ttu-id="17d71-141">たとえば、パブリック メソッドより内部メソッドを使用したり、保護されたメソッドよりプライベート メソッドを使用したりします。</span><span class="sxs-lookup"><span data-stu-id="17d71-141">For example, use internal methods over public methods or private methods over protected methods.</span></span>
    - <span data-ttu-id="17d71-142">**変更に対して閉じている**: プロパティをプライベートにし、メソッドをプライベートまたは最終保護にします。</span><span class="sxs-lookup"><span data-stu-id="17d71-142">**Closed for modification** – Make your properties private, and make your methods either private or final-protected.</span></span> <span data-ttu-id="17d71-143">この方法により、継承または拡張を通じて、ロジックで依存関係を活用できる人はいません。</span><span class="sxs-lookup"><span data-stu-id="17d71-143">In this way, no one can take advantage of a dependency on your logic, either through inheritance or extension.</span></span>

+ <span data-ttu-id="17d71-144">**リスコフ置き換え**: 派生クラスは、基本クラスの代わりに使用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="17d71-144">**Liskov substitution** – Derived classes must be able to be substituted for their base classes.</span></span> <span data-ttu-id="17d71-145">たとえば、この置き換えは、ファクトリを指定する、SysExtension を使用する、および単純なコンストラクト メソッドを使用することにより実行できます。</span><span class="sxs-lookup"><span data-stu-id="17d71-145">For example, this substitution can be done by providing factories, by using SysExtension, and by using simple construct methods.</span></span>
+ <span data-ttu-id="17d71-146">**インターフェイスの分離**: 簡単なインターフェイスを作成します。</span><span class="sxs-lookup"><span data-stu-id="17d71-146">**Interface segregation** – Create concise interfaces.</span></span> <span data-ttu-id="17d71-147">この原則により、拡張担当者は置き換えの実装を提供します。次の SOLID 原則である依存関係の反転と組み合わせて使用する場合は、特に重要です。</span><span class="sxs-lookup"><span data-stu-id="17d71-147">This principle lets extenders provide replacement implementations and is particularly valuable when it's used together with the next SOLID principle, dependency inversion.</span></span>
+ <span data-ttu-id="17d71-148">**依存関係の反転**: 具体化ではなく抽象化に依存します。</span><span class="sxs-lookup"><span data-stu-id="17d71-148">**Dependency inversion** – Depend on abstractions, not concretions.</span></span> <span data-ttu-id="17d71-149">この原則により切り離しが可能になり、拡張担当者は、ロジックが依存している抽象化に準拠している具体的なインスタンスを提供できます。</span><span class="sxs-lookup"><span data-stu-id="17d71-149">This principle enables decoupling and lets extenders provide concrete instances that conform to the abstraction that your logic depends on.</span></span>

### <a name="write-clean-code"></a><span data-ttu-id="17d71-150">クリーンなコードの記述</span><span class="sxs-lookup"><span data-stu-id="17d71-150">Write clean code</span></span>
<span data-ttu-id="17d71-151">クリーンなコードは、記事のように読むことができます。</span><span class="sxs-lookup"><span data-stu-id="17d71-151">Clean code can be read like an article.</span></span> <span data-ttu-id="17d71-152">メソッドの名前は、記事の見出しを提供します。</span><span class="sxs-lookup"><span data-stu-id="17d71-152">The name of a method provides the heading of the article.</span></span> <span data-ttu-id="17d71-153">次にメソッドの本文があり、概要はわずか数行で構成されます。</span><span class="sxs-lookup"><span data-stu-id="17d71-153">The body of the method comes next and really consists of just a few lines of summary.</span></span> <span data-ttu-id="17d71-154">この概要は、適切な内容を示す名前を持つ他のいくつかのメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="17d71-154">This summary calls a few other methods that have good descriptive names.</span></span> <span data-ttu-id="17d71-155">これにより、読み手は、詳細を閲覧し続け、概念に関する情報を見逃すことなくいつでも停止することもできます。</span><span class="sxs-lookup"><span data-stu-id="17d71-155">In this way, the reader can keep exploring details and can also stop at any time without missing any conceptual information.</span></span>

<span data-ttu-id="17d71-156">この方法でコードが記述されると、メソッドは短く (多くの場合 5 ～ 10 コード行未満) なります。</span><span class="sxs-lookup"><span data-stu-id="17d71-156">When code is written like in this manner, methods are short, often less than 5 to 10 code lines.</span></span> <span data-ttu-id="17d71-157">さらに、パラメーターの数が少なくなり (通常は 2 未満)、コードの条件およびブロックが常に 1 つのコード行になります。</span><span class="sxs-lookup"><span data-stu-id="17d71-157">Additionally, the number of parameters is low, often less than two, and the conditions and blocks of code are always a single code line.</span></span>

<span data-ttu-id="17d71-158">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="17d71-158">Here is an example.</span></span>

```
public void processOrder(SalesOrder _salesOrder)
    {
        if (this.approveOrder(_salesOrder))
        {
            this.confirmOrder(_salesOrder);
        }
        else
        {
            this.rejectOrder(_salesOrder);
        }
    }
```

<span data-ttu-id="17d71-159">X++ では、すべての保護されたパブリック メソッドが拡張ポイントです。</span><span class="sxs-lookup"><span data-stu-id="17d71-159">In X++, every protected and public method is an extension point.</span></span> <span data-ttu-id="17d71-160">クリーンなコードを記述することで、拡張可能コードを自動的に生成します。</span><span class="sxs-lookup"><span data-stu-id="17d71-160">By writing clean code, you automatically produce extensible code.</span></span> <span data-ttu-id="17d71-161">前の例では、拡張担当者が、承認、確認、および否認を実装する方法を変更できます。</span><span class="sxs-lookup"><span data-stu-id="17d71-161">In the previous example, an extender can change how approval, confirmation, and rejection are implemented.</span></span> <span data-ttu-id="17d71-162">実装がインラインである場合、コードは拡張できません。</span><span class="sxs-lookup"><span data-stu-id="17d71-162">If the implementations had been inline, the code would not be extensible.</span></span>

### <a name="dont-repeat-yourself-dry"></a><span data-ttu-id="17d71-163">DRY 原則</span><span class="sxs-lookup"><span data-stu-id="17d71-163">Don't repeat yourself (DRY)</span></span>
<span data-ttu-id="17d71-164">実装の不整合を防ぐため、ロジックで冗長性を避けてください。</span><span class="sxs-lookup"><span data-stu-id="17d71-164">To help prevent misalignment of implementations, avoid redundancy in your logic.</span></span> <span data-ttu-id="17d71-165">この原則は、拡張可能コードの場合は特に重要です。拡張担当者は、必要な部分をすべて拡張するとは限らないため、意図せずソリューションが壊れたままにする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="17d71-165">This principle is especially important in the case of extensible code, because the extender might not extend all required pieces and might therefore unintentionally leave the solution broken.</span></span>

## <a name="best-practices-to-create-an-extensible-solution-in-x"></a><span data-ttu-id="17d71-166">X++ で拡張可能ソリューションを作成するためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="17d71-166">Best practices to create an extensible solution in X++</span></span>
<span data-ttu-id="17d71-167">以下のベスト プラクティスは、コードのユーザーがソリューションを拡張できるように、X++ で拡張可能なソリューションを作成するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="17d71-167">The following best practices can help you create extensible solutions in X++, so that consumers of your code can extend your solution:</span></span>

+ [<span data-ttu-id="17d71-168">クラス</span><span class="sxs-lookup"><span data-stu-id="17d71-168">Classes</span></span>](extensible-classes.md)
+ [<span data-ttu-id="17d71-169">方法</span><span class="sxs-lookup"><span data-stu-id="17d71-169">Methods</span></span>](extensible-methods.md)
+ [<span data-ttu-id="17d71-170">フォーム</span><span class="sxs-lookup"><span data-stu-id="17d71-170">Forms</span></span>](extensible-forms.md)
+ [<span data-ttu-id="17d71-171">拡張データ型</span><span class="sxs-lookup"><span data-stu-id="17d71-171">Extended data types</span></span>](extensible-edts.md)
+ [<span data-ttu-id="17d71-172">拡張可能な列挙</span><span class="sxs-lookup"><span data-stu-id="17d71-172">Extensible enums</span></span>](extensible-enums.md)
+ [<span data-ttu-id="17d71-173">委任</span><span class="sxs-lookup"><span data-stu-id="17d71-173">Delegates</span></span>](extensible-code-delegates.md)
+ [<span data-ttu-id="17d71-174">テーブル</span><span class="sxs-lookup"><span data-stu-id="17d71-174">Tables</span></span>](extensible-tables.md)
+ [<span data-ttu-id="17d71-175">メソッドの拡張属性</span><span class="sxs-lookup"><span data-stu-id="17d71-175">Extensibility attributes for methods</span></span>](extensibility-attributes.md)

## <a name="breaking-changes"></a><span data-ttu-id="17d71-176">変更の分割</span><span class="sxs-lookup"><span data-stu-id="17d71-176">Breaking changes</span></span>
<span data-ttu-id="17d71-177">ソリューションを拡張可能にすると、後で拡張ポイントを壊さずに済むことにもなります。</span><span class="sxs-lookup"><span data-stu-id="17d71-177">When you make your solution extensible, you also help guarantee that you won't break extension points later.</span></span> <span data-ttu-id="17d71-178">詳細については、[重大な変更](breaking-changes.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17d71-178">For more information, see [Breaking changes](breaking-changes.md).</span></span>

## <a name="external-resources"></a><span data-ttu-id="17d71-179">外部リソース</span><span class="sxs-lookup"><span data-stu-id="17d71-179">External resources</span></span>
<span data-ttu-id="17d71-180">次の外部リソースは、クリーンなコードを作成しているかどうかを確認するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="17d71-180">The following external resources can help you make sure that you're writing clean code:</span></span>

+ [<span data-ttu-id="17d71-181">SOLID の原則</span><span class="sxs-lookup"><span data-stu-id="17d71-181">SOLID Principles</span></span>](https://en.wikipedia.org/wiki/SOLID)
+ [<span data-ttu-id="17d71-182">Pluralsight - クリーンなコード: 人間に適したコードの記述</span><span class="sxs-lookup"><span data-stu-id="17d71-182">Pluralsight - Clean Code: Writing Code for Humans</span></span>](https://www.pluralsight.com/courses/writing-clean-code-humans)
+ [<span data-ttu-id="17d71-183">クリーンなコード: アジャイル ソフトウェア作成者が守るべき事柄のハンドブック</span><span class="sxs-lookup"><span data-stu-id="17d71-183">Clean Code: A Handbook of Agile Software Craftsmanship</span></span>](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882)
+ [<span data-ttu-id="17d71-184">Clean Coders</span><span class="sxs-lookup"><span data-stu-id="17d71-184">Clean Coders</span></span>](https://cleancoders.com/)
+ [<span data-ttu-id="17d71-185">DRY 原則</span><span class="sxs-lookup"><span data-stu-id="17d71-185">Don't repeat yourself</span></span>](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself)

