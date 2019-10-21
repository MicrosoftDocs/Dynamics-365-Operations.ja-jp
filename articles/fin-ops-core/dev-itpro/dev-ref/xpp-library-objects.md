---
title: X++ クラス ライブラリ
description: このトピックでは、X++ でのクラス ライブラリについて説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 150303
ms.assetid: 1b2d76d1-52d9-46b2-937f-5a3b62f2d516
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0cefc23fd27f7fbfe9fb31b806de8248aed0bfeb
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550823"
---
# <a name="x-class-library"></a><span data-ttu-id="122e1-103">X++ クラス ライブラリ</span><span class="sxs-lookup"><span data-stu-id="122e1-103">X++ class library</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="122e1-104">このトピックでは、X++ でのクラス ライブラリについて説明します。</span><span class="sxs-lookup"><span data-stu-id="122e1-104">This topic describes the library of classes in X++.</span></span> <span data-ttu-id="122e1-105">*アプリケーション クラス*および*システム クラス*の、2 種類のクラスがあります。</span><span class="sxs-lookup"><span data-stu-id="122e1-105">There are two kinds of classes: *application classes* and *system classes*.</span></span>

- <span data-ttu-id="122e1-106">**アプリケーション クラス** - これらのクラスは X++ で実装されています。</span><span class="sxs-lookup"><span data-stu-id="122e1-106">**Application classes** – These classes are implemented in X++.</span></span> <span data-ttu-id="122e1-107">これらはアプリケーション エクスプローラーの **コード > クラス** ノードで使用できます。</span><span class="sxs-lookup"><span data-stu-id="122e1-107">They are available in the **Code > Classes** node in Application Explorer.</span></span>
- <span data-ttu-id="122e1-108">**システム クラス** – これらのクラスは、*カーネル クラス* と呼ばれることもあります。</span><span class="sxs-lookup"><span data-stu-id="122e1-108">**System classes** – These classes are sometimes known as *kernel classes*.</span></span> <span data-ttu-id="122e1-109">これは、アプリケーション エクスプローラーの **システム ドキュメント > クラス** ノードの下に一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="122e1-109">They are listed under the **System Documentation > Classes** node in Application Explorer.</span></span> <span data-ttu-id="122e1-110">これらのクラスのソース コードは使用できません。</span><span class="sxs-lookup"><span data-stu-id="122e1-110">The source code for these classes isn't available.</span></span> <span data-ttu-id="122e1-111">システム クラスの一覧については、[API、クラス、およびテーブルの参照](api-reference.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="122e1-111">For a list of the system classes, see [API, class, and table reference](api-reference.md).</span></span>

## <a name="typical-structure-of-an-application-class"></a><span data-ttu-id="122e1-112">アプリケーション クラスの一般的な構造</span><span class="sxs-lookup"><span data-stu-id="122e1-112">Typical structure of an application class</span></span>

<span data-ttu-id="122e1-113">次のコード ブロック タイプは、アプリケーション クラスの標準です。</span><span class="sxs-lookup"><span data-stu-id="122e1-113">The following code block types are standard for application classes:</span></span>

- <span data-ttu-id="122e1-114">**クラスおよび変数宣言**: このクラス宣言には、**パブリック**、**プライベート**、および**拡張**などのモディファイアーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="122e1-114">**class and variable declarations**: The class declaration contains modifiers such as **public**, **private**, and **extends**.</span></span> 
- <span data-ttu-id="122e1-115">**変数宣言**: これらは、このクラスから構築されたオブジェクトのフィールド メンバーです。</span><span class="sxs-lookup"><span data-stu-id="122e1-115">**variable declarations**: These are the field members for objects that are constructed from the class.</span></span> <span data-ttu-id="122e1-116">**this** というキーワードをクラス インスタンス変数に入力すると、IntelliSense でこのメンバーを一覧表示できます。</span><span class="sxs-lookup"><span data-stu-id="122e1-116">When you type the keyword **this** on a class instance variable, IntelliSense can show a list of the members.</span></span>
- <span data-ttu-id="122e1-117">**新規** メソッド: このメソッドは、クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="122e1-117">**new** method: This method creates an instance of the class.</span></span> <span data-ttu-id="122e1-118">コンストラクターは、**新しい**キーワードを使用することによってのみ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="122e1-118">The constructor can be called only by using the **new** keyword.</span></span> <span data-ttu-id="122e1-119">派生クラスは、**super** メソッドの参照を呼ぶことにとって、コントラクターの**新しい**メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="122e1-119">Derived classes can call the **new** method of their constructor by calling the **super** method reference.</span></span> <span data-ttu-id="122e1-120">詳細については、[X++ 継承](xpp-inheritance.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="122e1-120">For more information, see [X++ inheritance](xpp-inheritance.md).</span></span>
- <span data-ttu-id="122e1-121">**ファイナライズ** メソッド: このメソッドは、クラスのインスタンスをファイナライズします。</span><span class="sxs-lookup"><span data-stu-id="122e1-121">**finalize** method: This method finalizes an instance of the class.</span></span> <span data-ttu-id="122e1-122">このメソッドはデストラクター メソッドです。</span><span class="sxs-lookup"><span data-stu-id="122e1-122">This method is the destructor method.</span></span> <span data-ttu-id="122e1-123">ただし、規則のみのデストラクタです。</span><span class="sxs-lookup"><span data-stu-id="122e1-123">However, it's a destructor by convention only.</span></span> <span data-ttu-id="122e1-124">ガベージ コレクション中に **finalize** メソッドが自動的に呼び出されることはありません。</span><span class="sxs-lookup"><span data-stu-id="122e1-124">The system doesn't automatically call the **finalize** method during garbage collection.</span></span>

<span data-ttu-id="122e1-125">クラスの追加メソッドには、次のタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="122e1-125">Additional methods for a class have the following types:</span></span>

+ <span data-ttu-id="122e1-126">インスタンス メソッド</span><span class="sxs-lookup"><span data-stu-id="122e1-126">Instance methods</span></span>
+ <span data-ttu-id="122e1-127">静的メソッド</span><span class="sxs-lookup"><span data-stu-id="122e1-127">Static methods</span></span>
+ <span data-ttu-id="122e1-128">主要メソッド</span><span class="sxs-lookup"><span data-stu-id="122e1-128">Main methods</span></span>

<span data-ttu-id="122e1-129">さまざまな種類の項目でメソッドを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="122e1-129">Methods can be created on many kinds of items.</span></span> <span data-ttu-id="122e1-130">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="122e1-130">Here are some examples:</span></span>

+ <span data-ttu-id="122e1-131">クラス</span><span class="sxs-lookup"><span data-stu-id="122e1-131">Classes</span></span>
+ <span data-ttu-id="122e1-132">マップ</span><span class="sxs-lookup"><span data-stu-id="122e1-132">Maps</span></span>
+ <span data-ttu-id="122e1-133">ビュー</span><span class="sxs-lookup"><span data-stu-id="122e1-133">Views</span></span>
+ <span data-ttu-id="122e1-134">データ セット</span><span class="sxs-lookup"><span data-stu-id="122e1-134">Data Sets</span></span>
+ <span data-ttu-id="122e1-135">フォーム</span><span class="sxs-lookup"><span data-stu-id="122e1-135">Forms</span></span>
+ <span data-ttu-id="122e1-136">クエリ</span><span class="sxs-lookup"><span data-stu-id="122e1-136">Queries</span></span>

## <a name="substituting-application-classes-for-system-classes"></a><span data-ttu-id="122e1-137">システム クラス用のアプリケーション クラスの置き換え</span><span class="sxs-lookup"><span data-stu-id="122e1-137">Substituting application classes for system classes</span></span>

<span data-ttu-id="122e1-138">拡張するシステム クラスの代わりに *アプリケーション クラスの置き換え* を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="122e1-138">You should use the *substitute application classes* instead of the system classes that they extend.</span></span> <span data-ttu-id="122e1-139">アプリケーション エクスプローラーの、**システム ドキュメント > クラス** では、いくつかのカーネルまたはシステム クラスの名前は小文字の *x* で始まります。</span><span class="sxs-lookup"><span data-stu-id="122e1-139">In Application Explorer, under **System Documentation > Classes**, several kernel or system classes have names that begin with a lowercase *x*.</span></span> <span data-ttu-id="122e1-140">これらのクラスは、*x-system classes* とも呼ばれています。</span><span class="sxs-lookup"><span data-stu-id="122e1-140">These classes are known as *x-system classes*.</span></span> <span data-ttu-id="122e1-141">これらのシステム クラスの例には、**xApplication** および **xVersionControl** が存在します。</span><span class="sxs-lookup"><span data-stu-id="122e1-141">Examples of these system classes are **xApplication** and **xVersionControl**.</span></span> <span data-ttu-id="122e1-142">これらのクラスのいくつかは、アプリケーション クラスによって拡張されます。</span><span class="sxs-lookup"><span data-stu-id="122e1-142">Some of these classes are extended by application classes.</span></span> <span data-ttu-id="122e1-143">たとえば、**アプリケーション**クラスは **xApplication** システム クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="122e1-143">For example, the **Application** class extends the **xApplication** system class.</span></span> <span data-ttu-id="122e1-144">X システム クラスから派生するクラスは、*アプリケーション クラスの代用* として知られています。</span><span class="sxs-lookup"><span data-stu-id="122e1-144">The classes that derive from x-system classes are known as *substitute application classes*.</span></span> <span data-ttu-id="122e1-145">アプリケーション エクスプローラーの**クラス** ノードで、代替アプリケーション クラスの横にあるアイコンは標準のアイコンと異なります。</span><span class="sxs-lookup"><span data-stu-id="122e1-145">In Application Explorer, under the **Classes** node, the icon next to the substitute application classes differs from the standard icon.</span></span>

### <a name="x-system-classes"></a><span data-ttu-id="122e1-146">x システム クラス</span><span class="sxs-lookup"><span data-stu-id="122e1-146">x-system classes</span></span>

<span data-ttu-id="122e1-147">代替アプリケーション クラスの一部は、クラスのインスタンスを表す特殊なグローバル変数に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="122e1-147">Some of the substitute application classes are associated with a special global variable that represents an instance of the class.</span></span> <span data-ttu-id="122e1-148">たとえば、**appl** 変数は、**アプリケーション**クラスから事前にインスタンス化されたオブジェクトを参照します。</span><span class="sxs-lookup"><span data-stu-id="122e1-148">For example, the **appl** variable references a pre-instantiated object from the **Application** class.</span></span> <span data-ttu-id="122e1-149">**appl** 変数の利点は、セッションの範囲全体にわたってシステムがオブジェクトを保持することです。</span><span class="sxs-lookup"><span data-stu-id="122e1-149">The advantage of the **appl** variable is that the system maintains the object throughout the scope of your session.</span></span> <span data-ttu-id="122e1-150">**Application** クラスのインスタンスを取得するために **new Application()** 構文を繰り返し使用した場合、コードの効率が低下します。</span><span class="sxs-lookup"><span data-stu-id="122e1-150">Your code would be less efficient if it repeatedly used the **new Application()** syntax to obtain an instance of the **Application** class.</span></span> <span data-ttu-id="122e1-151">**xApplication** システム クラスは使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="122e1-151">You should not use the **xApplication** system class.</span></span> <span data-ttu-id="122e1-152">代わりに、**アプリケーション**の代替アプリケーション クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="122e1-152">Instead, use the **Application** substitute application class.</span></span> <span data-ttu-id="122e1-153">標準構文 **Application::checkForNewBatchJobs()** を使用することにより、**アプリケーション** クラスの静的メンバーを参照することができます。</span><span class="sxs-lookup"><span data-stu-id="122e1-153">You can reference the static members of the **Application** class by using the following standard syntax: **Application::checkForNewBatchJobs()**.</span></span> <span data-ttu-id="122e1-154">ただし、**アプリケーション**クラスのインスタンス メンバーを参照するには、そのクラスの **appl** 変数 (存在する場合) を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="122e1-154">However, to reference the instance members of the **Application** class, you should use that class's **appl** variable, if it exists.</span></span> <span data-ttu-id="122e1-155">このパターンは、ほとんどの x システム クラスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="122e1-155">This pattern applies to most of the x-system classes.</span></span> <span data-ttu-id="122e1-156">**セッション** 代替アプリケーション クラスは、**セッション** の特殊なグローバル変数がないため 1 つの例外です。</span><span class="sxs-lookup"><span data-stu-id="122e1-156">The **Session** substitute application class is one exception, because there is no special global variable for **Session**.</span></span> <span data-ttu-id="122e1-157">次のテーブルは、対応するアプリケーション クラスの代用を持つ x システム クラスの一覧です。</span><span class="sxs-lookup"><span data-stu-id="122e1-157">The following table lists the x-system classes that have a corresponding substitute application class.</span></span> <span data-ttu-id="122e1-158">特殊なグローバル変数は、それらを持つクラスに対しても表示されます。</span><span class="sxs-lookup"><span data-stu-id="122e1-158">The special global variables are also shown for those classes that have one.</span></span>

| <span data-ttu-id="122e1-159">アプリケーション クラス</span><span class="sxs-lookup"><span data-stu-id="122e1-159">Application class</span></span> | <span data-ttu-id="122e1-160">x システム クラス</span><span class="sxs-lookup"><span data-stu-id="122e1-160">x-system class</span></span>  | <span data-ttu-id="122e1-161">グローバル変数</span><span class="sxs-lookup"><span data-stu-id="122e1-161">Global variable</span></span>    |
|-------------------|-----------------|--------------------|
| <span data-ttu-id="122e1-162">引数</span><span class="sxs-lookup"><span data-stu-id="122e1-162">Args</span></span>              | <span data-ttu-id="122e1-163">xArgs</span><span class="sxs-lookup"><span data-stu-id="122e1-163">xArgs</span></span>           | <span data-ttu-id="122e1-164">該当なし</span><span class="sxs-lookup"><span data-stu-id="122e1-164">Not applicable</span></span>     |
| <span data-ttu-id="122e1-165">申請</span><span class="sxs-lookup"><span data-stu-id="122e1-165">Application</span></span>       | <span data-ttu-id="122e1-166">xApplication</span><span class="sxs-lookup"><span data-stu-id="122e1-166">xApplication</span></span>    | <span data-ttu-id="122e1-167">**appl**</span><span class="sxs-lookup"><span data-stu-id="122e1-167">**appl**</span></span>           |
| <span data-ttu-id="122e1-168">ClassFactory</span><span class="sxs-lookup"><span data-stu-id="122e1-168">ClassFactory</span></span>      | <span data-ttu-id="122e1-169">xClassFactory</span><span class="sxs-lookup"><span data-stu-id="122e1-169">xClassFactory</span></span>   | <span data-ttu-id="122e1-170">**classFactory**</span><span class="sxs-lookup"><span data-stu-id="122e1-170">**classFactory**</span></span>   |
| <span data-ttu-id="122e1-171">法人</span><span class="sxs-lookup"><span data-stu-id="122e1-171">Company</span></span>           | <span data-ttu-id="122e1-172">xCompany</span><span class="sxs-lookup"><span data-stu-id="122e1-172">xCompany</span></span>        | <span data-ttu-id="122e1-173">**appl.company**</span><span class="sxs-lookup"><span data-stu-id="122e1-173">**appl.company**</span></span>   |
| <span data-ttu-id="122e1-174">グローバル</span><span class="sxs-lookup"><span data-stu-id="122e1-174">Global</span></span>            | <span data-ttu-id="122e1-175">xGlobal</span><span class="sxs-lookup"><span data-stu-id="122e1-175">xGlobal</span></span>         | <span data-ttu-id="122e1-176">該当なし</span><span class="sxs-lookup"><span data-stu-id="122e1-176">Not applicable</span></span>     |
| <span data-ttu-id="122e1-177">情報</span><span class="sxs-lookup"><span data-stu-id="122e1-177">Info</span></span>              | <span data-ttu-id="122e1-178">xInfo</span><span class="sxs-lookup"><span data-stu-id="122e1-178">xInfo</span></span>           | <span data-ttu-id="122e1-179">**情報ログ**</span><span class="sxs-lookup"><span data-stu-id="122e1-179">**Infolog**</span></span>        |
| <span data-ttu-id="122e1-180">MenuFunction</span><span class="sxs-lookup"><span data-stu-id="122e1-180">MenuFunction</span></span>      | <span data-ttu-id="122e1-181">xMenuFunction</span><span class="sxs-lookup"><span data-stu-id="122e1-181">xMenuFunction</span></span>   | <span data-ttu-id="122e1-182">該当なし</span><span class="sxs-lookup"><span data-stu-id="122e1-182">Not applicable</span></span>     |
| <span data-ttu-id="122e1-183">セッション</span><span class="sxs-lookup"><span data-stu-id="122e1-183">Session</span></span>           | <span data-ttu-id="122e1-184">xSession</span><span class="sxs-lookup"><span data-stu-id="122e1-184">xSession</span></span>        | <span data-ttu-id="122e1-185">該当なし</span><span class="sxs-lookup"><span data-stu-id="122e1-185">Not applicable</span></span>     |
| <span data-ttu-id="122e1-186">VersionControl</span><span class="sxs-lookup"><span data-stu-id="122e1-186">VersionControl</span></span>    | <span data-ttu-id="122e1-187">xVersionControl</span><span class="sxs-lookup"><span data-stu-id="122e1-187">xVersionControl</span></span> | <span data-ttu-id="122e1-188">**versionControl**</span><span class="sxs-lookup"><span data-stu-id="122e1-188">**versionControl**</span></span> |

### <a name="example-of-x-system-classes"></a><span data-ttu-id="122e1-189">x システム クラスの例</span><span class="sxs-lookup"><span data-stu-id="122e1-189">Example of x-system classes</span></span>

<span data-ttu-id="122e1-190">次の例は、代替アプリケーション クラスのインスタンスを参照するいくつかの特殊な変数を使用するための構文を示しています。</span><span class="sxs-lookup"><span data-stu-id="122e1-190">The following example shows the syntax for using several special variables that reference instances of the substitute application classes.</span></span>

```X++
TreeNode treeNode;
Args     args;
FormRun  formRun;

// appl variable
info(appl.buildNo());

// company variable
appl.company().reloadRights();

// infolog variable
treeNode = infolog.findNode("\\forms\\custTable");
info(treeNode.AOTgetProperty("Name"));
// Output is "CustTable".

// classFactory variable
args = new Args(formstr(Batch));
formRun = classFactory.formRunClass(args);
formRun.init();
formRun.run();
formRun.detach();
info("Method is ending. This is a message in the Infolog.");
// Output is "Method is ending. This is a message in the Infolog."
```

## <a name="batch-processing-classes"></a><span data-ttu-id="122e1-191">バッチ処理クラス</span><span class="sxs-lookup"><span data-stu-id="122e1-191">Batch processing classes</span></span>
<span data-ttu-id="122e1-192">クラスを実装するには、バッチ処理システムを使用し、**RunBase** および **RunBaseBatch** クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="122e1-192">You implement classes by using the batch processing system, and by extending the **RunBase** and **RunBaseBatch** classes.</span></span> <span data-ttu-id="122e1-193">**バッチ処理**ダイアログ ボックスから**繰り返し**ボタンを削除するには、**Args::parmEnum** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="122e1-193">To remove the **Recurrence** button from the **Batch processing** dialog box, you use the **Args::parmEnum** method.</span></span> <span data-ttu-id="122e1-194">サーバー バインド バッチ メソッドとして実行するクラスを指定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="122e1-194">We recommend that you designate a class to run as a server-bound batch method.</span></span> <span data-ttu-id="122e1-195">サーバー バインド バッチ メソッドは、以下の理由のため、サーバー バインドでないバッチ メソッドより安全です。</span><span class="sxs-lookup"><span data-stu-id="122e1-195">Server-bound batch methods are more secure than batch methods that aren't server-bound for the following reasons:</span></span>

-   <span data-ttu-id="122e1-196">このメソッドは、メソッドを送信したユーザーのアクセス許可を使用して実行されます。</span><span class="sxs-lookup"><span data-stu-id="122e1-196">The method is run by using the permissions of the user who submitted the method.</span></span>
-   <span data-ttu-id="122e1-197">このメソッドは、特定の **情報** および **グローバル** クラス メソッドのみを使用して、それを処理しているクライアントと対話できます。</span><span class="sxs-lookup"><span data-stu-id="122e1-197">The method can use only specific **Info** and **Global** class methods to interact with the client that is processing it.</span></span> <span data-ttu-id="122e1-198">この制限により、クライアントとのやり取りが制限されます。</span><span class="sxs-lookup"><span data-stu-id="122e1-198">This restriction limits interaction with the client.</span></span>

### <a name="enable-a-class-to-run-as-a-server-bound-batch-method"></a><span data-ttu-id="122e1-199">サーバー バインド バッチ メソッドとして実行するクラスを有効化</span><span class="sxs-lookup"><span data-stu-id="122e1-199">Enable a class to run as a server-bound batch method</span></span>

1.  <span data-ttu-id="122e1-200">**RunBaseBatch** クラスを拡張するクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="122e1-200">Create a class that extends the **RunBaseBatch** class.</span></span>
2.  <span data-ttu-id="122e1-201">次の例に示すように、**RunBaseBatch.runsImpersonated** メソッドをオーバーライドし、値 **true** を返します。</span><span class="sxs-lookup"><span data-stu-id="122e1-201">Override the **RunBaseBatch.runsImpersonated** method to return a value of **true**, as shown in the following example.</span></span>

    ```X++
    public boolean runsImpersonated()
    {
        return true;
    }
    ```
    
3.  <span data-ttu-id="122e1-202">クラスが次の**情報**および**グローバル**クラスのメソッドのみを呼び出すことを確認します。</span><span class="sxs-lookup"><span data-stu-id="122e1-202">Confirm that the class calls only the following **Info** and **Global** class methods:</span></span>
    -   <span data-ttu-id="122e1-203">追加</span><span class="sxs-lookup"><span data-stu-id="122e1-203">add</span></span>
    -   <span data-ttu-id="122e1-204">Info.copy</span><span class="sxs-lookup"><span data-stu-id="122e1-204">Info.copy</span></span>
    -   <span data-ttu-id="122e1-205">Info.cut</span><span class="sxs-lookup"><span data-stu-id="122e1-205">Info.cut</span></span>
    -   <span data-ttu-id="122e1-206">Info.import</span><span class="sxs-lookup"><span data-stu-id="122e1-206">Info.import</span></span>
    -   <span data-ttu-id="122e1-207">Info.export</span><span class="sxs-lookup"><span data-stu-id="122e1-207">Info.export</span></span>
    -   <span data-ttu-id="122e1-208">Info.line</span><span class="sxs-lookup"><span data-stu-id="122e1-208">Info.line</span></span>
    -   <span data-ttu-id="122e1-209">Info.num</span><span class="sxs-lookup"><span data-stu-id="122e1-209">Info.num</span></span>
    -   <span data-ttu-id="122e1-210">Global::error</span><span class="sxs-lookup"><span data-stu-id="122e1-210">Global::error</span></span>
    -   <span data-ttu-id="122e1-211">Global::info</span><span class="sxs-lookup"><span data-stu-id="122e1-211">Global::info</span></span>
    -   <span data-ttu-id="122e1-212">Global::warning</span><span class="sxs-lookup"><span data-stu-id="122e1-212">Global::warning</span></span>

    <span data-ttu-id="122e1-213">**Info.line** および **Info.num** メソッドは、**xInfo** クラスから継承されます。</span><span class="sxs-lookup"><span data-stu-id="122e1-213">The **Info.line** and **Info.num** methods are inherited from the **xInfo** class.</span></span>

### <a name="removing-the-recurrence-button-from-the-batch-processing-dialog-box"></a><span data-ttu-id="122e1-214">バッチ処理ダイアログ ボックスから定期的なアイテムを削除</span><span class="sxs-lookup"><span data-stu-id="122e1-214">Removing the Recurrence button from the batch processing dialog box</span></span>

<span data-ttu-id="122e1-215">バッチ処理システムを使用してクラスを実装するときは、**Args.parmEnum** メソッドを呼び出し、**NoYes::Yes** システム列挙値を渡して、**再実行**ボタンを削除できます。</span><span class="sxs-lookup"><span data-stu-id="122e1-215">When you implement a class by using the batch processing system, you can remove the **Recurrence** button by calling the **Args.parmEnum** method and passing the **NoYes::Yes** system enumeration value.</span></span> <span data-ttu-id="122e1-216">**NoYes** システム列挙は、**繰り返し** ボタンがダイアログ ボックスから削除されるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="122e1-216">The **NoYes** system enumeration determines whether the **Recurrence** button is removed from the dialog box.</span></span> <span data-ttu-id="122e1-217">既定値は **NoYes::No** です。</span><span class="sxs-lookup"><span data-stu-id="122e1-217">The default value is **NoYes::No**.</span></span> <span data-ttu-id="122e1-218">次の例では、**InventTransferMultiShip** クラスが実装されています。</span><span class="sxs-lookup"><span data-stu-id="122e1-218">In the following example, the **InventTransferMultiShip** class is implemented.</span></span> <span data-ttu-id="122e1-219">**BatchDialog::main** メソッドは、**バッチ処理**ダイアログ ボックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="122e1-219">The **BatchDialog::main** method creates the **Batch processing** dialog box.</span></span>

```X++
static void noRecurrenceButton(Args _args)
{
    Args a;
    InventTransferMultiShip inventTransferMultiShip;
    a = new Args();
    inventTransferMultiShip = InventTransferMultiShip::construct();
    a.caller(inventTransferMultiShip);
    a.parmEnum(NoYes::Yes);
    BatchDialog::main(a);
}
```

## <a name="image-manipulation-classes"></a><span data-ttu-id="122e1-220">イメージ操作クラス</span><span class="sxs-lookup"><span data-stu-id="122e1-220">Image manipulation classes</span></span>
<span data-ttu-id="122e1-221">**Image** と **Imagelist** の 2 つのシステム クラスにより、グラフィックスとアイコンを操作できます。</span><span class="sxs-lookup"><span data-stu-id="122e1-221">Two system classes let you to manipulate graphics and icons: **Image** and **Imagelist**.</span></span>

- <span data-ttu-id="122e1-222">**Image** – このクラスでは、個々の画像の読み込み、保存、操作などができます。</span><span class="sxs-lookup"><span data-stu-id="122e1-222">**Image** – This class lets you load, save, and manipulate individual images.</span></span> <span data-ttu-id="122e1-223">たとえば、画面をキャプチャして画像として保存し、画像をトリミングまたは回転させる、または色深度を操作します。</span><span class="sxs-lookup"><span data-stu-id="122e1-223">For example, you can capture a screen and save it as an image, crop or rotate an image, or manipulate the color depth.</span></span>
- <span data-ttu-id="122e1-224"><strong>Imagelist</strong> - このクラスを使用すると、サイズや透明色などの一般的なプロパティを持つ一連の画像を操作できます。</span><span class="sxs-lookup"><span data-stu-id="122e1-224"><strong>Imagelist</strong> – This class lets you work with a set of images that have common properties, such as the size and transparency color.</span></span> <span data-ttu-id="122e1-225">ImageListAppl\* アプリケーション クラスで使用されるイメージ リストを表示できます。</span><span class="sxs-lookup"><span data-stu-id="122e1-225">You can view the image lists that are used in the ImageListAppl\* application classes.</span></span>

## <a name="query-object-model"></a><span data-ttu-id="122e1-226">クエリ オブジェクト モデル</span><span class="sxs-lookup"><span data-stu-id="122e1-226">Query object model</span></span>
<span data-ttu-id="122e1-227">クエリ オブジェクト モデルには、クエリの定義と実行に使用されるクラスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="122e1-227">The query object model contains classes that are used to define and run a query.</span></span> <span data-ttu-id="122e1-228">クエリ オブジェクトは、クエリ データ ソース、返されるフィールド、レコード範囲、子データ ソースとの関係を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="122e1-228">The query objects are used to define the query data source, the fields that are returned, record ranges, and relations to child data sources.</span></span> <span data-ttu-id="122e1-229">動的クエリをコードで作成すると、クエリ クラスの可視性が高まります。さらに、これらは、アプリケーション エクスプローラーで静的クエリを作成するときにもシーン裏で使用されます。</span><span class="sxs-lookup"><span data-stu-id="122e1-229">The query classes are more visible when you create a dynamic query in code, but they are also used behind the scenes when you create a static query in Application Explorer.</span></span> <span data-ttu-id="122e1-230">次のテーブルでは、クエリ オブジェクト モデルのクラスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="122e1-230">The following table describes the classes in the query object model.</span></span>

| <span data-ttu-id="122e1-231">システム クラス</span><span class="sxs-lookup"><span data-stu-id="122e1-231">System class</span></span>         | <span data-ttu-id="122e1-232">説明</span><span class="sxs-lookup"><span data-stu-id="122e1-232">Description</span></span>      |
|----------------------|------------------|
| <span data-ttu-id="122e1-233">QueryRun</span><span class="sxs-lookup"><span data-stu-id="122e1-233">QueryRun</span></span>             | <span data-ttu-id="122e1-234">このクラスは、クエリを実行し、データをフェッチします。</span><span class="sxs-lookup"><span data-stu-id="122e1-234">This class runs the query and fetches the data.</span></span> |
| <span data-ttu-id="122e1-235">クエリ</span><span class="sxs-lookup"><span data-stu-id="122e1-235">Query</span></span>                | <span data-ttu-id="122e1-236">このクラスはいくつかのプロパティを保持し、1 つ以上の関連するデータ ソースを持ちます。</span><span class="sxs-lookup"><span data-stu-id="122e1-236">This class holds some properties, and has one or more related data sources.</span></span> <span data-ttu-id="122e1-237">クエリの定義の最上位です。</span><span class="sxs-lookup"><span data-stu-id="122e1-237">It's the top level of the query definition.</span></span>    |
| <span data-ttu-id="122e1-238">QueryBuildDataSource</span><span class="sxs-lookup"><span data-stu-id="122e1-238">QueryBuildDataSource</span></span> | <span data-ttu-id="122e1-239">このクラスは、クエリ内の単一のデータ ソースへのアクセスを定義します。</span><span class="sxs-lookup"><span data-stu-id="122e1-239">This class defines access to a single data source in the query.</span></span> <span data-ttu-id="122e1-240">クエリに同じレベルの 1 つ以上のデータ ソースある場合、独立した SQL ステートメントが生産され、順番に実行されます。</span><span class="sxs-lookup"><span data-stu-id="122e1-240">If there is more than one data source at the same level in a query, separate SQL statements are produced and are run sequentially.</span></span> <span data-ttu-id="122e1-241">データ ソースが別のデータ ソースの子である場合は、2 つのデータ ソース間に結合が作成されます。</span><span class="sxs-lookup"><span data-stu-id="122e1-241">If one data source is a child of another data source, a join is created between the two data sources.</span></span> |
| <span data-ttu-id="122e1-242">QueryBuildFieldList</span><span class="sxs-lookup"><span data-stu-id="122e1-242">QueryBuildFieldList</span></span>  | <span data-ttu-id="122e1-243">このクラスは、データベースから返されるフィールドを定義します。</span><span class="sxs-lookup"><span data-stu-id="122e1-243">This class defines the fields that are returned from the database.</span></span> <span data-ttu-id="122e1-244">既定では、フィールド リストは動的であり、すべてのフィールドはデータ ソース テーブル、マップ、またはビューから戻されます。</span><span class="sxs-lookup"><span data-stu-id="122e1-244">By default, the field list is dynamic, and all fields are returned from the data source table, map, or view.</span></span> <span data-ttu-id="122e1-245">各データ ソースには、**QueryBuildFieldList** オブジェクトが 1 つだけあります。</span><span class="sxs-lookup"><span data-stu-id="122e1-245">Each data source has only one **QueryBuildFieldList** object.</span></span> <span data-ttu-id="122e1-246">このオブジェクトには、選択したすべてのフィールドに関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="122e1-246">This object contains information about all selected fields.</span></span> <span data-ttu-id="122e1-247">フィールド リスト オブジェクトで、**SUM**、**COUNT**、および **AVG** などの、集計関数を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="122e1-247">You can specify aggregate functions, such as **SUM**, **COUNT**, and **AVG**, on the field list object.</span></span> |
| <span data-ttu-id="122e1-248">QueryBuildRange</span><span class="sxs-lookup"><span data-stu-id="122e1-248">QueryBuildRange</span></span>      | <span data-ttu-id="122e1-249">このクラスは、単一フィールドに基づいて、返されるレコードのサブセットを定義します。</span><span class="sxs-lookup"><span data-stu-id="122e1-249">This class defines a subset of records that is returned, based on a single field.</span></span> <span data-ttu-id="122e1-250">範囲は、クエリ SQL ステートメントの **WHERE** 句に変換されます。</span><span class="sxs-lookup"><span data-stu-id="122e1-250">A range is translated into a **WHERE** clause in the query SQL statement.</span></span> <span data-ttu-id="122e1-251">クエリを制限するために 1 つ以上のフィールドが使用されている場合 (**WHERE**句)、データ ソースには 1 つ以上の範囲が含まれます。</span><span class="sxs-lookup"><span data-stu-id="122e1-251">If more than one field is used to limit the query (**WHERE** clause), the data source will contain more than one range.</span></span> |
| <span data-ttu-id="122e1-252">QueryBuildDynalink</span><span class="sxs-lookup"><span data-stu-id="122e1-252">QueryBuildDynalink</span></span>   | <span data-ttu-id="122e1-253">このクラスには、外部レコードとの関係 (制限) に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="122e1-253">This class contains information about a relation (limitation) to an external record.</span></span> <span data-ttu-id="122e1-254">クエリを実行すると、この情報は、クエリ SQL ステートメントの **WHERE** 句内で追加のエントリに変換されます。</span><span class="sxs-lookup"><span data-stu-id="122e1-254">When the query is run, this information is converted to additional entries in the **WHERE** clause of the query SQL statement.</span></span> <span data-ttu-id="122e1-255">このクラスは、クエリの親データ ソースにのみ存在できます。</span><span class="sxs-lookup"><span data-stu-id="122e1-255">This class can exist only on the parent data source of a query.</span></span> <span data-ttu-id="122e1-256">フォームは、2 つのデータ ソースが同期されるときにこの機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="122e1-256">Forms use the function when two data sources are synchronized.</span></span> <span data-ttu-id="122e1-257">子データ ソースは、親データ ソース に対する 1 つ以上の DLL を格納します。</span><span class="sxs-lookup"><span data-stu-id="122e1-257">The child data source will then contain one or more DLLs to the parent data source.</span></span> <span data-ttu-id="122e1-258">この関数は、2 つのデータソースが 2 つの異なる形式になっていて、まだ同期されている場合でも使用されます。</span><span class="sxs-lookup"><span data-stu-id="122e1-258">The function is used even if the two data sources are put in two different forms but are still synchronized.</span></span> |
| <span data-ttu-id="122e1-259">QueryBuildLink</span><span class="sxs-lookup"><span data-stu-id="122e1-259">QueryBuildLink</span></span>       | <span data-ttu-id="122e1-260">このクラスは、結合に 2 つのデータ ソースの間の関係を指定します。</span><span class="sxs-lookup"><span data-stu-id="122e1-260">This class specifies the relation between the two data sources in the join.</span></span> <span data-ttu-id="122e1-261">このクラスは、子データ ソースにのみ存在できます。</span><span class="sxs-lookup"><span data-stu-id="122e1-261">This class can exist only on a child data source.</span></span> |

<span data-ttu-id="122e1-262">また、[SysDa API](sysda.md)を使用してデータを照会することもできます。</span><span class="sxs-lookup"><span data-stu-id="122e1-262">You can also use the [SysDa API](sysda.md) to query data.</span></span>

## <a name="system-classes-overview"></a><span data-ttu-id="122e1-263">システム クラスの概要</span><span class="sxs-lookup"><span data-stu-id="122e1-263">System classes overview</span></span>
<span data-ttu-id="122e1-264">システム クラスのこのソースは使用できません。</span><span class="sxs-lookup"><span data-stu-id="122e1-264">The source for system classes isn't available.</span></span> <span data-ttu-id="122e1-265">システム クラスは、次の特性を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="122e1-265">A system class can have the following characteristics:</span></span>

+ <span data-ttu-id="122e1-266">静的メソッド (またはクラス メソッド)</span><span class="sxs-lookup"><span data-stu-id="122e1-266">Static methods (or class methods)</span></span>
+ <span data-ttu-id="122e1-267">動的メソッド</span><span class="sxs-lookup"><span data-stu-id="122e1-267">Dynamic methods</span></span>
+ <span data-ttu-id="122e1-268">プロパティ - これらのプロパティは、プロパティを設定するために使用されるメンバー関数です。</span><span class="sxs-lookup"><span data-stu-id="122e1-268">Properties – These properties are member functions that are used to set properties.</span></span> <span data-ttu-id="122e1-269">たとえば **LeftMargin** です。</span><span class="sxs-lookup"><span data-stu-id="122e1-269">An example is **LeftMargin**.</span></span>

<span data-ttu-id="122e1-270">システム クラスのメソッドをオーバーライドすることはできません。</span><span class="sxs-lookup"><span data-stu-id="122e1-270">You can't override system class methods.</span></span> <span data-ttu-id="122e1-271">最初からアプリケーション オブジェクトをデザインするためにシステム クラスを使用することを意図していません。</span><span class="sxs-lookup"><span data-stu-id="122e1-271">It isn't our intention that you will use the system classes to design your application objects from scratch.</span></span> <span data-ttu-id="122e1-272">代わりに、アプリケーション エクスプローラーで既存の機能を拡張または変更するために使用します。</span><span class="sxs-lookup"><span data-stu-id="122e1-272">Instead, use them to extend or modify the default functionality in Application Explorer.</span></span> <span data-ttu-id="122e1-273">たとえば、既存のレポートに追加情報を動的に追加することができます。</span><span class="sxs-lookup"><span data-stu-id="122e1-273">For example, you can dynamically add extra information to an existing report.</span></span> <span data-ttu-id="122e1-274">または、前のページでのユーザーの選択に基づいて、ページ上で使用可能なオプションを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="122e1-274">Alternatively, you can change the options that are available on a page, based on the user's selection on a previous page.</span></span>

### <a name="collection-classes"></a><span data-ttu-id="122e1-275">コレクション クラス</span><span class="sxs-lookup"><span data-stu-id="122e1-275">Collection classes</span></span>

<span data-ttu-id="122e1-276">*コレクション クラス*を使用すると、リスト、セット、構造体、マップ、および配列を作成できます。</span><span class="sxs-lookup"><span data-stu-id="122e1-276">The *collection classes* let you create lists, sets, structs, maps, and arrays.</span></span>

### <a name="application-object-classes"></a><span data-ttu-id="122e1-277">アプリケーション オブジェクト クラス</span><span class="sxs-lookup"><span data-stu-id="122e1-277">Application object classes</span></span>

<span data-ttu-id="122e1-278">これらのシステム クラスは、アプリケーション エクスプローラーを使用してアプリケーションを作成するたびにアクティブ化される関数を保持します。</span><span class="sxs-lookup"><span data-stu-id="122e1-278">These system classes hold functions that are activated whenever you use Application Explorer to create your application.</span></span> <span data-ttu-id="122e1-279">たとえば、システムは、アプリケーション エクスプローラーの**設計**ノードでフォームのレイアウトを定義する時、**FormDesign** クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="122e1-279">For example, the system uses the **FormDesign** class when you define the layout of your form in the **Designs** node in Application Explorer.</span></span> <span data-ttu-id="122e1-280">これらのクラスを使用すると、アプリケーション オブジェクトを作成したり変更したりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="122e1-280">These classes also let you to create and modify application objects.</span></span>

### <a name="integration-classes"></a><span data-ttu-id="122e1-281">統合クラス</span><span class="sxs-lookup"><span data-stu-id="122e1-281">Integration classes</span></span>

<span data-ttu-id="122e1-282">環境との統合は、通常、クラスによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="122e1-282">The integration with the environment is typically implemented by classes.</span></span> <span data-ttu-id="122e1-283">このカテゴリ内のクラスの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="122e1-283">Here are some examples of the classes in this category:</span></span>

-   <span data-ttu-id="122e1-284">**COM** - COM オブジェクトのメソッドの呼び出しです。</span><span class="sxs-lookup"><span data-stu-id="122e1-284">**COM** – The call of methods on COM objects.</span></span>
-   <span data-ttu-id="122e1-285">**DLL** – Microsoft Windows DLL 関数の呼び出し。</span><span class="sxs-lookup"><span data-stu-id="122e1-285">**DLL** – The call of Microsoft Windows DLL functions.</span></span>
-   <span data-ttu-id="122e1-286">**IO** – 外部ファイルの読み取りと書き込みを行います。</span><span class="sxs-lookup"><span data-stu-id="122e1-286">**IO** – Read and write external files.</span></span>
-   <span data-ttu-id="122e1-287">**ODBCConnection** – 外部データベースへの Open Database Connectivity (ODBC) インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="122e1-287">**ODBCConnection** – An Open Database Connectivity (ODBC) interface to a foreign database.</span></span>

