---
title: プロセス ガイド フレームワーク
description: このトピックでは、X++ で倉庫モバイル プロセスを拡張する開発者のプロセス ガイド フレームワークに関する情報を提供します。
author: MarkusFogelberg
manager: tfehr
ms.date: 11/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: kamaybac
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 216e9d2efd6381981b42358797cea90c14704fcc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996238"
---
# <a name="process-guide-framework"></a><span data-ttu-id="e895e-103">プロセス ガイド フレームワーク</span><span class="sxs-lookup"><span data-stu-id="e895e-103">Process guide framework</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e895e-104">このトピックでは、X++ で倉庫モバイル プロセスを拡張する開発者のプロセス ガイド フレームワークに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="e895e-104">This topic provides information about the process guide framework for developers who are extending the warehouse mobile processes in X++.</span></span> <span data-ttu-id="e895e-105">倉庫モバイル プロセスは、小さなステップに分割されるプロセスの結果として拡張可能です。</span><span class="sxs-lookup"><span data-stu-id="e895e-105">The warehouse mobile processes are extensible as a result of the processes being broken into small steps.</span></span> <span data-ttu-id="e895e-106">各ステップのビジネス ロジックおよびユーザー インターフェイスの作成は、個々のクラスに抽出されたため、拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="e895e-106">The business logic and user interface building of each step has been extracted into individual classes, which allows for extensibility.</span></span>

## <a name="overview-of-the-existing-design"></a><span data-ttu-id="e895e-107">既存のデザインの概要</span><span class="sxs-lookup"><span data-stu-id="e895e-107">Overview of the existing design</span></span>

<span data-ttu-id="e895e-108">倉庫モバイル実行フローは、1 つのカスタム サービス エンドポイントを通じて公開されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-108">The warehouse mobile execution flows are exposed through a single custom service endpoint.</span></span> <span data-ttu-id="e895e-109">ユーザーが入力した値に加えて、モバイル アプリケーションで表示されるユーザー インターフェイスのメタデータが含まれている、XML 文字列の形式でモバイル アプリケーションから要求が到達します。</span><span class="sxs-lookup"><span data-stu-id="e895e-109">The request arrives from the mobile app in the form of an XML string, which contains the metadata of the user interface presented in the mobile app, as well as the values entered by the user.</span></span>

<span data-ttu-id="e895e-110">要求が受信されると、この XML を逆シリアル化するために最初の手順が実行されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-110">When the request is received, the first step is to deserialize this XML.</span></span> <span data-ttu-id="e895e-111">**WHSMobileAppServiceXMLTranslator** クラスは、コントロール情報とセッション情報の両方が含まれているコンテナーに XML を変換します。</span><span class="sxs-lookup"><span data-stu-id="e895e-111">The **WHSMobileAppServiceXMLTranslator** class converts the XML into a container, which contains both the control information, as well as session information.</span></span>

<span data-ttu-id="e895e-112">その後、コンテナーの情報は、ユーザーが作業する倉庫プロセス、開始しようとしている倉庫プロセス (**WHSWorkExecuteMode** 列挙によって表される)、それに応じて **WHSWorkExecuteDisplay** の派生クラスをインスタンス化する倉庫プロセスを推定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-112">Following this, the information in the container is used to deduce which warehouse process the user is working on, or about to start (represented by the **WHSWorkExecuteMode** enumeration), and accordingly instantiate a derived class of **WHSWorkExecuteDisplay**.</span></span> <span data-ttu-id="e895e-113">**displayform()** メソッドが呼び出された後、以下が実行されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-113">The **displayform()** method is invoked, which then does the following:</span></span>

-   <span data-ttu-id="e895e-114">ユーザーからのデータの処理 (**WHSRFControlData** クラスに委任されますが、いくつかのプロセスは、**processControl()** メソッドを上書きすることによって特定のロジックを実装します)。</span><span class="sxs-lookup"><span data-stu-id="e895e-114">Processes the data from the user (delegated to the **WHSRFControlData** class, but some processes implement specific logic by overriding the **processControl()** method).</span></span>

-   <span data-ttu-id="e895e-115">ビジネス ロジックを実行します。</span><span class="sxs-lookup"><span data-stu-id="e895e-115">Executes business logic.</span></span>

-   <span data-ttu-id="e895e-116">ステップが増加します。</span><span class="sxs-lookup"><span data-stu-id="e895e-116">Increments the step.</span></span>

-   <span data-ttu-id="e895e-117">新しいユーザー インターフェイスを表すコンテナーを構築します (一般に、**build…()** メソッドで)。</span><span class="sxs-lookup"><span data-stu-id="e895e-117">Builds the container representing the new user interface (typically in a **build…()** method).</span></span>

<span data-ttu-id="e895e-118">コンテナーは、その後、変換元に返却されて XML がシリアル化され、モバイル デバイスへの応答として返送されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-118">The container is then returned to the translator, which then serializes the XML, and sends it back as a response to the mobile device.</span></span>

<span data-ttu-id="e895e-119">次の順序図では、実行フローの概要を示します。</span><span class="sxs-lookup"><span data-stu-id="e895e-119">The following sequence diagram shows an overview of the execution flow.</span></span> <span data-ttu-id="e895e-120">図は概要図以上のものでり、実際のコードを 1:1 で表したものではないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="e895e-120">Note that the diagram is more of a schematic overview and is not a 1:1 representation of the actual code.</span></span>

![プロセスの概要図](media/schematic-overview.png)  

### <a name="reason-for-the-redesign"></a><span data-ttu-id="e895e-122">再設計の理由</span><span class="sxs-lookup"><span data-stu-id="e895e-122">Reason for the redesign</span></span>

<span data-ttu-id="e895e-123">上記の設計には、モバイル フローで使用されるプロセスを作成するための非常に単純なフレームワークが用意されています。</span><span class="sxs-lookup"><span data-stu-id="e895e-123">The above design offers a very simple framework for building processes used in mobile flows.</span></span> <span data-ttu-id="e895e-124">ただし、上記で明らかなように、**displayform()** メソッドが複数の職責を引き継ぎます。</span><span class="sxs-lookup"><span data-stu-id="e895e-124">However, as is evident above, the **displayform()** methods take over multiple responsibilities.</span></span> <span data-ttu-id="e895e-125">その他のメソッドおよびクラスに委任されますが、具体的なクラス職責がない場合は、クラス間で一貫性のある方法で実行されません。</span><span class="sxs-lookup"><span data-stu-id="e895e-125">It does delegate them to other methods and classes, but in the absence of concrete class responsibilities, it is done in an inconsistent manner across classes.</span></span> <span data-ttu-id="e895e-126">また、サポートされるシナリオの数が増えるにつれて、これらのクラスの一部には非常に複雑になります。</span><span class="sxs-lookup"><span data-stu-id="e895e-126">Also, as the number of supported scenarios grows organically, some of those classes can become quite complex.</span></span> <span data-ttu-id="e895e-127">問題をより魅力的にするために、これらのクラス/メソッドの一部が上書きされ、複数のモードで再利用されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-127">To make matters more interesting, some of those classes/methods are overridden and re-used in multiple modes.</span></span> <span data-ttu-id="e895e-128">結果は、サイクロマティック複雑度の高い非常に長いメソッドです。</span><span class="sxs-lookup"><span data-stu-id="e895e-128">The result is extremely long methods with high cyclomatic complexity.</span></span> <span data-ttu-id="e895e-129">過去には、保守の問題が生じていました。</span><span class="sxs-lookup"><span data-stu-id="e895e-129">These have posed maintenance issues in the past.</span></span> <span data-ttu-id="e895e-130">これらのメソッドのバグを修正することは危険であり、後戻りする傾向がありました。</span><span class="sxs-lookup"><span data-stu-id="e895e-130">Fixing bugs in these methods has been risky and regression prone.</span></span>
<span data-ttu-id="e895e-131">たとえば、**WhsWorkExecuteDisplay** クラス内の **processWorkLine()** メソッドは、複数のプロセス (基本的に、作業の実行が実行される任意の場所) から参照されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-131">For example, the **processWorkLine()** method in the **WhsWorkExecuteDisplay** class is referred from multiple processes (basically, anywhere where work execution is performed).</span></span>

<span data-ttu-id="e895e-132">これらを拡張可能にするため、いずれかのオプションは、**displayForm** メソッドを小さなメソッドに分割して拡張ポイントを導入するためのものです。</span><span class="sxs-lookup"><span data-stu-id="e895e-132">To make these extensible, one of the options would be to split the **displayForm** methods into smaller methods and introduce extensibility points.</span></span> <span data-ttu-id="e895e-133">ただし、シナリオ マトリックスのため、拡張機能を記述し、逆光を検証することはパートナーにとって困難です。</span><span class="sxs-lookup"><span data-stu-id="e895e-133">However, because of the scenario matrix, it would be challenging for partners to write extensions and validate against regressions.</span></span> <span data-ttu-id="e895e-134">それだけでなく、上記の構造化された責任の配分がないため、コードは徐々に予期しない方法で増加し、品質の高い拡張機能を構築することが困難になります。</span><span class="sxs-lookup"><span data-stu-id="e895e-134">Not only that, because of the lack of structured responsibility distribution noted above, the code would keep growing in unpredictable ways over time, posing challenges in building quality extensions.</span></span>

<span data-ttu-id="e895e-135">その結果、再設計は、明確に定義されたクラスに独立した職責を持たせるという目標を持つ、持続可能なオプションです。</span><span class="sxs-lookup"><span data-stu-id="e895e-135">As a result, the redesign is the sustainable option, with a goal to have clearly defined classes having independent responsibilities.</span></span> <span data-ttu-id="e895e-136">クラスの職責、変更する理由、拡張する理由は 1 つにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e895e-136">A class should have one responsibility, one reason to change, and one reason to be extended.</span></span>

## <a name="design-overview"></a><span data-ttu-id="e895e-137">設計の概要</span><span class="sxs-lookup"><span data-stu-id="e895e-137">Design overview</span></span>

<span data-ttu-id="e895e-138">再設計されたフレームワークでは、中核的な戦略は 2 つの原則を中心に展開しています。実行フローを明確に定義された責任を持つ個々のコンポーネントに分割することと、各コンポーネントに適切に定義された拡張点を持つことです。</span><span class="sxs-lookup"><span data-stu-id="e895e-138">In the redesigned framework, the core strategy revolves around two principles: divide the execution flow into individual components with well-defined responsibilities and have well-defined extension points in each of the components.</span></span>

<span data-ttu-id="e895e-139">新しいフレームワークの名前は、"ProcessGuide" です。</span><span class="sxs-lookup"><span data-stu-id="e895e-139">The name for the new framework is “ProcessGuide”.</span></span> <span data-ttu-id="e895e-140">これは、これらのクラスの目的が、業務プロセスを通じてユーザーをガイドすることだからです (データとやり取りする方法、またはタスクを実行する順序に関してユーザーがさらに柔軟性を持っているフォーム ベースのエクスペリエンスであるリッチ クライアントとは対照的)。</span><span class="sxs-lookup"><span data-stu-id="e895e-140">This is because the aim of these classes is to guide a user through a business process (as opposed to the rich client which is a form-based experiences where the user has more flexibility in how they interact with the data or in which order they perform tasks).</span></span>

> [!NOTE]
> <span data-ttu-id="e895e-141">1 つの重要な詳細は、"WHS" 接頭語の意図的な省略です。</span><span class="sxs-lookup"><span data-stu-id="e895e-141">One notable detail is the deliberate omission of the “WHS” prefix.</span></span> <span data-ttu-id="e895e-142">モバイル プロセスは当初倉庫管理に導入されましたが、その結果、さまざまな生産および在庫管理プロセスをサポートするための超越した境界が生じました。</span><span class="sxs-lookup"><span data-stu-id="e895e-142">While the mobile processes were initially introduced for warehousing, subsequently they have transcended boundaries to support various production and inventory management processes.</span></span> <span data-ttu-id="e895e-143">その結果、倉庫の参照はフレームワークの名前から除外されました。</span><span class="sxs-lookup"><span data-stu-id="e895e-143">As a result, the warehouse reference was excluded in the name of the framework.</span></span>

<span data-ttu-id="e895e-144">コンポーネントを識別するために、まず、プロセスの生産の開始を調べます (**WhsWorkExecuteDisplayProdStart** クラス)。</span><span class="sxs-lookup"><span data-stu-id="e895e-144">To identify the components, the first step is to look at the Production Start process (**WhsWorkExecuteDisplayProdStart** class).</span></span> <span data-ttu-id="e895e-145">次にプロセスの概要図を示します。</span><span class="sxs-lookup"><span data-stu-id="e895e-145">Here is a schematic of the process.</span></span>

![プロセスの概要図の画像](media/production-start-process-schematic.png)

<span data-ttu-id="e895e-147">制御フローを見ると、次のコンポーネントが必要です。</span><span class="sxs-lookup"><span data-stu-id="e895e-147">Looking at the control flow, the following are components needed:</span></span>

-   <span data-ttu-id="e895e-148">ビジネス プロセス全体を通じて合成するコントローラー。</span><span class="sxs-lookup"><span data-stu-id="e895e-148">A controller to stitch through the entire business process.</span></span>
-   <span data-ttu-id="e895e-149">プロセスでステップの実行を担当するステップ。</span><span class="sxs-lookup"><span data-stu-id="e895e-149">A step responsible for execution of a step in the process.</span></span>
-   <span data-ttu-id="e895e-150">ステップ内のデータを処理するためのデータ プロセッサ。</span><span class="sxs-lookup"><span data-stu-id="e895e-150">A data processor for processing the data in a step.</span></span>
-   <span data-ttu-id="e895e-151">ステップのユーザー インターフェイスの作成を担当するページ ビルダー。</span><span class="sxs-lookup"><span data-stu-id="e895e-151">A page builder responsible for building the user interface for a step.</span></span>
-   <span data-ttu-id="e895e-152">ステップの移行を担当するナビゲーション エージェント。</span><span class="sxs-lookup"><span data-stu-id="e895e-152">A navigation agent responsible for step transition.</span></span>
-   <span data-ttu-id="e895e-153">業務プロセスの実行を担当するクラス。</span><span class="sxs-lookup"><span data-stu-id="e895e-153">A class responsible for executing the business process.</span></span>

<span data-ttu-id="e895e-154">上のプロセス フロー図では、手順 1 から開始し、前の手順からのデータの処理を開始した後、最後に UI を構築した場合、データは次の手順で処理され続けます。</span><span class="sxs-lookup"><span data-stu-id="e895e-154">In the process flow diagram above, if you begin at step 1 and start processing the data from the previous step, and then end with building a UI, data would continue to be processed in the next step.</span></span> <span data-ttu-id="e895e-155">これにより、連続したステップ間に厳密な結合が生まれ、その結果、高レベルの新しい概略図は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="e895e-155">This introduces a tight coupling between consecutive steps, as a result, our new high-level schematic would look like the following:</span></span>

![高レベルのプロセス概略図の画像](media/high-level-schematic.png)

<span data-ttu-id="e895e-157">以下は、再設計されたプロセスの重要なコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="e895e-157">The following are the key components in the redesigned process:</span></span>

-   <span data-ttu-id="e895e-158">**ProcessGuideController** - このクラスは、業務プロセスの全体的な実行を調整します。</span><span class="sxs-lookup"><span data-stu-id="e895e-158">**ProcessGuideController** - This class orchestrates the overall execution of the business process.</span></span> <span data-ttu-id="e895e-159">これは、ステップとナビゲーション エージェントのインスタンスを作成し、その結果、プロセスの実行と、キャンセルまたはプロセスの終了のためのクリーンアップ ロジックを構成するファクトリを定義します。</span><span class="sxs-lookup"><span data-stu-id="e895e-159">It defines the factories that instantiate the step and the navigation agent, which subsequently constitute the process execution, as well as the clean-up logic for cancellation or exiting the process.</span></span>

-   <span data-ttu-id="e895e-160">**ProcessGuideStep** - このクラスは、業務プロセスの 1 つのステップを表します。</span><span class="sxs-lookup"><span data-stu-id="e895e-160">**ProcessGuideStep** - This class represents one single step in the business process.</span></span> <span data-ttu-id="e895e-161">このクラスは、ページ ビルダー、アクション、およびデータ プロセッサのインスタンスを作成するファクトリの定義を含み、それらを正しい順序で呼び出することを担当します。</span><span class="sxs-lookup"><span data-stu-id="e895e-161">This class contains a definition of the factories that instantiate a page builder, actions, and data processors and is responsible for invoking them in the correct sequence.</span></span>

-   <span data-ttu-id="e895e-162">**ProcessGuideNavigationAgent** - このクラスは、手順間の移動を担当します。</span><span class="sxs-lookup"><span data-stu-id="e895e-162">**ProcessGuideNavigationAgent** - This class is responsible for navigation between the steps.</span></span> <span data-ttu-id="e895e-163">ステップが完了したら、ナビゲーション エージェントは、次のステップの定義を担当し、前の手順が次の手順に伝達する必要があるすべてのパラメーターを渡します。</span><span class="sxs-lookup"><span data-stu-id="e895e-163">When a step is completed, the navigation agent is responsible for defining the next step and passes any parameters that the previous step may need to communicate to the next one.</span></span>

-   <span data-ttu-id="e895e-164">**ProcessGuidePageBuilder** - このクラスは、ユーザー インターフェイスのインスタンス化を担当します。</span><span class="sxs-lookup"><span data-stu-id="e895e-164">**ProcessGuidePageBuilder** - This class is responsible for instantiating the user interface.</span></span>

-   <span data-ttu-id="e895e-165">**ProcessGuideAction** - このクラスは、ユーザーにボタンとして表示される、アクションを表します。</span><span class="sxs-lookup"><span data-stu-id="e895e-165">**ProcessGuideAction** - This class represents an action, shown as a button to the user.</span></span>

-   <span data-ttu-id="e895e-166">**ProcessGuideDataProcessor** - このクラスは、フィールド内のユーザーが入力したデータの処理を担当します。</span><span class="sxs-lookup"><span data-stu-id="e895e-166">**ProcessGuideDataProcessor** - This class is responsible for processing the user entered data in a field.</span></span>

## <a name="execution-flow"></a><span data-ttu-id="e895e-167">実行フロー</span><span class="sxs-lookup"><span data-stu-id="e895e-167">Execution flow</span></span>

<span data-ttu-id="e895e-168">実行フローの開始点は変更されないままです。</span><span class="sxs-lookup"><span data-stu-id="e895e-168">The starting point of the execution flow remains unchanged.</span></span> <span data-ttu-id="e895e-169">そのため、要求は引き続き同じエンドポイントに到着し、その後、コンテナーに XML が逆シリアル化されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-169">So, the request still arrives through the same endpoints, followed by deserializing the XML into the container.</span></span> <span data-ttu-id="e895e-170">このコンテナーは、**getNextFormState()** にに渡されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-170">This container is then passed to **getNextFormState()**.</span></span>

<span data-ttu-id="e895e-171">注目すべき次の 3 つの重要なクラスがあります。</span><span class="sxs-lookup"><span data-stu-id="e895e-171">There are three important classes to note:</span></span>

-  <span data-ttu-id="e895e-172">**ProcessGuideSessionState** - これは、セッション状態情報 (モード、合格、コントローラー、および実行される手順など) を含みます。</span><span class="sxs-lookup"><span data-stu-id="e895e-172">**ProcessGuideSessionState** – This contains the session state information – mode, pass, controller, and step being executed, and so on.</span></span>

-  <span data-ttu-id="e895e-173">**ProcessGuidePage** - これには、ユーザー インターフェイス メタデータの厳密に表したものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="e895e-173">**ProcessGuidePage** – This contains a strongly-typed representation of the user interface metadata.</span></span>

-  <span data-ttu-id="e895e-174">**ProcessGuideRequest** - これには、メンバーとして上記の 2 つが含まれており、モバイル デバイスから受信した要求を厳密に表したものです。</span><span class="sxs-lookup"><span data-stu-id="e895e-174">**ProcessGuideRequest** – This contains the above two as members and is a strongly-typed representation of the request received from the mobile device.</span></span>

<span data-ttu-id="e895e-175">これらのクラスは、コンテナー情報を使用して作成されます (状態とユーザー入力管理データの両方)。</span><span class="sxs-lookup"><span data-stu-id="e895e-175">These classes are created using the container information (both state and user entered control data).</span></span> <span data-ttu-id="e895e-176">これにより、値にアクセスして操作するためのタイプ セーフな方法が提供されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-176">This provides a type-safe way to access and manipulate the values.</span></span> <span data-ttu-id="e895e-177">プロセス中のコンテナーの繰り返しアクセスと比較して、これは、信頼性とパフォーマンスの両方に関して利点を生み出します。</span><span class="sxs-lookup"><span data-stu-id="e895e-177">Compared to repeated access of the container during the process, this provides benefit both in terms of readability and performance.</span></span>

<span data-ttu-id="e895e-178">セッション状態情報は、適切な **ProcessGuideController** クラスのインスタンスを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-178">The session state information is used to instantiate the correct **ProcessGuideController** class.</span></span> <span data-ttu-id="e895e-179">インスタンスが作成されると、**ProcessGuideController** クラス内の **createResponse()** メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-179">Once instantiated, the **createResponse()** method in the **ProcessGuideController** class is invoked.</span></span> <span data-ttu-id="e895e-180">このメソッドは、プロセス ガイド ロジックへのエントリ ポイントであり、実行後、応答で戻ります (**ProcessGuideResponse** クラスで表される)。</span><span class="sxs-lookup"><span data-stu-id="e895e-180">This method is the entry point to the process guide logic, and after execution, comes back with the response (represented in the **ProcessGuideResponse** class).</span></span> <span data-ttu-id="e895e-181">応答は、その後コンテナーに変換されて、レガシ トピックに戻された後、XML にシリアル化され、応答がモバイル デバイスに戻されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-181">The response is then converted back to the container and handed back to the legacy logic, which then serializes it to the XML and sends the response back to the mobile device.</span></span>

<span data-ttu-id="e895e-182">次に、コントローラーは実行する次の手順を見つける必要があります。</span><span class="sxs-lookup"><span data-stu-id="e895e-182">Next, the controller needs to find the next step to execute.</span></span> <span data-ttu-id="e895e-183">これが新しいプロセスの開始である場合、コントローラーは **initialStep()** を呼び出して、プロセスの最初の手順を取得します。</span><span class="sxs-lookup"><span data-stu-id="e895e-183">If this is the start of a new process, the controller will call **initialStep()** to get the first step in the process.</span></span> <span data-ttu-id="e895e-184">その後、**ProcessGuideStep** で **execute()** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e895e-184">After that, it would call **execute()** method in the **ProcessGuideStep**.</span></span> <span data-ttu-id="e895e-185">この方法はその後、**ProcessGuidePageBuilder** クラスのインスタンスを作成し、**buildPage()** を呼び出します。これにより、ユーザーに表示されるユーザー インターフェイスの仮想表現である **ProcessGuidePage** オブジェクトが返されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-185">This method would then instantiate a **ProcessGuidePageBuilder** class and call **buildPage()**, which would return with a **ProcessGuidePage** object, which is a virtual representation of the user interface to be presented to the user.</span></span> <span data-ttu-id="e895e-186">その後、ステップは結果をコントローラーに戻します。それから、現在のセッションの状態が保存され、結果が **ProcessGuideResponse** クラスの形式で **getNextFormState()** に戻されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-186">The step would then send the result back to the controller, which would then save the current session state and then return the result back to **getNextFormState()** in the form of the **ProcessGuideResponse** class.</span></span> <span data-ttu-id="e895e-187">その後、応答はコンテナーにもう一度変換され、その結果、XML にシリアル化されて、モバイル デバイスに応答が返されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-187">Thereafter, the response is converted back to the container, and subsequently serializes to XML and sends back the response to the mobile device.</span></span>

<span data-ttu-id="e895e-188">次のシーケンス図では、この制御フローについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e895e-188">The following sequence diagram explains this control flow.</span></span> <span data-ttu-id="e895e-189">これは、設計を説明するために簡略化された、最も一般的な制御フローである点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="e895e-189">Note that this is the most common control flow, simplified for explaining the design.</span></span>

![簡略化された制御フロー](media/control-flow.png)

<span data-ttu-id="e895e-191">ユーザーがボタンをクリックして (または、通常は既定のアクションをトリガーする値をスキャンして) モバイル デバイスでアクションを実行すると、要求は同じルートを経由して **ProcessGuideController** クラス内の **createResponse()** メソッドに到着します。</span><span class="sxs-lookup"><span data-stu-id="e895e-191">When the user takes an action on the mobile device by clicking a button (or scanning a value – which typically triggers the default action) – the request arrives at the **createResponse()** method in the **ProcessGuideController** class through the same route.</span></span> <span data-ttu-id="e895e-192">ただし、このとき、コントローラーはセッション状態情報から、ユーザーがいるステップを知ります。</span><span class="sxs-lookup"><span data-stu-id="e895e-192">This time, however, the controller knows from the session state information which step the user is in.</span></span> <span data-ttu-id="e895e-193">したがって、適切な **ProcessGuideStep** クラスのインスタンスを作成し、実行メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e895e-193">Accordingly, it instantiates the appropriate **ProcessGuideStep** class and invokes the execute method.</span></span> <span data-ttu-id="e895e-194">同様に、**ProcessGuideStep** はユーザーによって呼び出されるアクション名を読み取り、適切な **ProcessGuideAction** クラスをインスタンス化して **execute()** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e895e-194">The **ProcessGuideStep**, in turn, reads the action name invoked by the user and then instantiates the appropriate **ProcessGuideAction** class and calls **execute()**.</span></span>

<span data-ttu-id="e895e-195">**ProcessGuideAction** クラスは、特定のアクションを実行することを担当しますが、2 つの重要な例外があります。</span><span class="sxs-lookup"><span data-stu-id="e895e-195">The **ProcessGuideAction** class is responsible for executing the specific action, however there are two notable exceptions.</span></span>

<span data-ttu-id="e895e-196">1 つ目は、**ProcessGuideOKAction** クラスです。</span><span class="sxs-lookup"><span data-stu-id="e895e-196">The first one is the **ProcessGuideOKAction** class.</span></span> <span data-ttu-id="e895e-197">このアクションは、ユーザーがプロセスを確認して前に動かすことを求めていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="e895e-197">This action implies that the user wants to confirm and move forward in the process.</span></span> <span data-ttu-id="e895e-198">それに従って、このメソッドは実際に ProcessGuideStep クラスへのコールバックを行います。これは、ステップが **ProcessGuideDataProcessor** で **processData()** を呼び出すことを意味します。</span><span class="sxs-lookup"><span data-stu-id="e895e-198">In accordance to that – this method actually does a callback to the ProcessGuideStep class, which means that the step invokes **processData()** in **ProcessGuideDataProcessor**.</span></span> <span data-ttu-id="e895e-199">これは、ユーザーが入力したデータを処理し、ステップの状態を更新し、結果をコントローラーに返します。</span><span class="sxs-lookup"><span data-stu-id="e895e-199">This processes the data that the user has entered, and then updates the state of the step and sends the result back to the controller.</span></span> <span data-ttu-id="e895e-200">プロセッサの結果によっては、ステップは適切なユーザー インターフェイスを構築するためのページ ビルダーを起動するか、ステップのステータスを完了に設定します。</span><span class="sxs-lookup"><span data-stu-id="e895e-200">Depending on the outcome of the processor, the step invokes the page builder to build the appropriate user interface or sets the status of the step as completed.</span></span> <span data-ttu-id="e895e-201">これは、次のシーケンス図の上半分に反映されています。</span><span class="sxs-lookup"><span data-stu-id="e895e-201">This is reflected in the top half of the sequence diagram below.</span></span>

<span data-ttu-id="e895e-202">その他の例外は、**ProcessGuideCancelResetProcessAction** および **ProcessGuideCancelExitProcessAction** クラスで実装されている取消アクションです。</span><span class="sxs-lookup"><span data-stu-id="e895e-202">The other exception is the cancellation action, implemented in the **ProcessGuideCancelResetProcessAction** and **ProcessGuideCancelExitProcessAction** classes.</span></span> <span data-ttu-id="e895e-203">これらのアクションは、処理をキャンセルする意図を表し、プロセスの開始またはプロセスの終了を完全に戻します。</span><span class="sxs-lookup"><span data-stu-id="e895e-203">These actions represent an intent to cancel the process and go back to either the start of the process or exit the process altogether.</span></span> <span data-ttu-id="e895e-204">**OK** アクションと同様、これらのアクションも、ステップにコールバックを実行します。これは、**ProcessGuideController** に意図を示します。</span><span class="sxs-lookup"><span data-stu-id="e895e-204">Similar to the **OK** action, these actions also perform a callback to the step, which signals the intent to the **ProcessGuideController**.</span></span> <span data-ttu-id="e895e-205">その後、コントローラーは状態変数の必要なクリーンアップを実行し、コントロールをプロセスにおける最初のステップに移動するか、プロセスを完全に終了します。</span><span class="sxs-lookup"><span data-stu-id="e895e-205">The controller then performs the necessary cleanup of state variables and either moves control to the initial step in the process or terminates the process altogether.</span></span>

<span data-ttu-id="e895e-206">ステップが完了した後、ステップのステータスが **完了** に設定されている場合、コントローラーは **ProcessGuideNavigationAgent** のインスタンスを作成し、次のステップの名前が返されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-206">After the step is completed, if the status of the step is set to **Completed**, then the controller instantiates the **ProcessGuideNavigationAgent**, which returns the name of the next step.</span></span> <span data-ttu-id="e895e-207">その後、コントローラーはこのステップをインスタンス化し、**execute()** メソッドを呼び出します。サイクルが続行します。</span><span class="sxs-lookup"><span data-stu-id="e895e-207">The controller then instantiates this step and invokes the **execute()** method – and the cycle continues.</span></span> <span data-ttu-id="e895e-208">ほとんどの場合、新しい手順は、対応する **ProcessGuidePageBuilder** を呼び出し、ユーザーに表示した後に戻される次の画面のユーザー インターフェイスを作成します。</span><span class="sxs-lookup"><span data-stu-id="e895e-208">Most commonly, the new step invokes the corresponding **ProcessGuidePageBuilder** to build the user interface for the next screen to be presented to the user, which is then sent back.</span></span> <span data-ttu-id="e895e-209">このフローは、次のシーケンス図の下半分に反映されています。</span><span class="sxs-lookup"><span data-stu-id="e895e-209">This flow is depicted in the lower half of the sequence diagram below.</span></span>

![シーケンス図](media/sequence-diagram.png)

## <a name="building-a-new-process-using-the-processguide-framework"></a><span data-ttu-id="e895e-211">ProcessGuide フレームワークを使用した新しいプロセスの構築</span><span class="sxs-lookup"><span data-stu-id="e895e-211">Building a new process using the ProcessGuide framework</span></span>

<span data-ttu-id="e895e-212">制御フローを説明する最善の方法は、アプリケーションに存在している例を使用することです (生産開始プロセス)。</span><span class="sxs-lookup"><span data-stu-id="e895e-212">The best way to explain the control flow is by using an example that exists in the application – the Production Start process.</span></span>

## <a name="overview-of-the-production-start-process"></a><span data-ttu-id="e895e-213">生産開始プロセスの概要</span><span class="sxs-lookup"><span data-stu-id="e895e-213">Overview of the production start process</span></span>

<span data-ttu-id="e895e-214">まず、プロセス フローを理解しましょう。</span><span class="sxs-lookup"><span data-stu-id="e895e-214">Let’s start by understanding the process flow.</span></span> <span data-ttu-id="e895e-215">最初の手順で、ユーザーは製造オーダー ID の入力を求められます。</span><span class="sxs-lookup"><span data-stu-id="e895e-215">In the first step, the user is prompted for production order ID.</span></span>

![生産 ID の確認](media/production-id-prompt.png)

<span data-ttu-id="e895e-217">製造オーダー ID をユーザーが入力すると、注文番号が検証されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-217">When the user enters the production order ID, the order number is validated.</span></span> <span data-ttu-id="e895e-218">実行される検証の一部は、ユーザーがログインしているのと同じ倉庫に注文があるかどうかと、注文のステータスに基づいています。</span><span class="sxs-lookup"><span data-stu-id="e895e-218">Some of the validations that are run are based on whether the order is in the same warehouse as the user is signed in to, and the status of the order.</span></span> <span data-ttu-id="e895e-219">検証が失敗すると、ユーザーにはエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-219">If the validation fails, the user is shown an error message.</span></span> <span data-ttu-id="e895e-220">検証が正常に実行された場合、ユーザーには、製造オーダーと品目の詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-220">If the validation succeeds, then the user is shown details of the production order and item.</span></span>

<span data-ttu-id="e895e-221">ユーザーはキャンセルしてプロセスの開始に戻るか、**OK** をクリックして確認できます。</span><span class="sxs-lookup"><span data-stu-id="e895e-221">The user can either cancel to go back to the start of the process or click **OK** to confirm.</span></span> <span data-ttu-id="e895e-222">後者の場合は、製造オーダーが **開始済** ステータスに設定され、対応する仕訳帳が転記され、コントロールが最初の手順に戻り、ユーザーに ”作業完了" というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-222">In the latter case, the production order is set to **Started** status, the corresponding journals are posted, the control moves back to the first step, and the “Work Completed” message is shown to the user.</span></span>


## <a name="creating-the-controller"></a><span data-ttu-id="e895e-223">コントローラーの作成</span><span class="sxs-lookup"><span data-stu-id="e895e-223">Creating the controller</span></span>

<span data-ttu-id="e895e-224">業務プロセスの作成の最初の手順は、コントローラー クラスの作成です。これは、コントローラーのデフォルトの動作を実装する **ProcessGuideController** 抽象クラスから拡張されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-224">The first step in building the business process is creating the controller class, extending from the **ProcessGuideController** abstract class which implements the default behaviors of a controller.</span></span> <span data-ttu-id="e895e-225">新しいクラスの名前は **ProdProcessGuideProductionStartController** であり、**StartProdOrder** の **WHSWorkExecuteMode** で修飾されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-225">The new class name is **ProdProcessGuideProductionStartController** and decorated with the **WHSWorkExecuteMode** value of **StartProdOrder**.</span></span> <span data-ttu-id="e895e-226">**WHSWorkExecuteDisplay** クラスで使用されたのと同じ **SysExtension** ベースのインスタンス化が使用されます。これは、ユーザーがこのモードのメニュー項目を実行するときにコントローラーをインスタンス化するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="e895e-226">The same **SysExtension** based instantiation that was used in the **WHSWorkExecuteDisplay** classes is used, which helps instantiate the controller when the user executes a menu item for this mode.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
public class ProdProcessGuideProductionStartController extends ProcessGuideController
```

> [!NOTE]
> <span data-ttu-id="e895e-227">クラスの名前付けパターンは、**\<FunctionalArea\>ProcessGuide\<Businessprocessname\>コントローラー** です。</span><span class="sxs-lookup"><span data-stu-id="e895e-227">The naming pattern of the class is **\<FunctionalArea\>ProcessGuide\<Businessprocessname\>Controller**.</span></span> <span data-ttu-id="e895e-228">これは、コントローラー クラスに使用されるパターンであり、その他のクラスを拡張するためのものです。</span><span class="sxs-lookup"><span data-stu-id="e895e-228">This is the pattern that is used for the controller classes and to extend to other classes.</span></span>


## <a name="building-the-first-step"></a><span data-ttu-id="e895e-229">最初のステップの作成</span><span class="sxs-lookup"><span data-stu-id="e895e-229">Building the first step</span></span>

<span data-ttu-id="e895e-230">次に、最初のステップを定義するには、**ProcessGuideStep** から拡張して、**ProdProcessGuidePromptProductionIdStep** クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="e895e-230">Next, to define the first step you create the **ProdProcessGuidePromptProductionIdStep** class, extending from **ProcessGuideStep**.</span></span>

<span data-ttu-id="e895e-231">クラスのインスタンス化を作成するタスクは、**ProcessGuideController** 基本クラスによって呼び出されるステップ ファクトリに委任されます。。</span><span class="sxs-lookup"><span data-stu-id="e895e-231">The task of instantiating the class is delegated to a step factory, which is invoked by the **ProcessGuideController** base class.</span></span> <span data-ttu-id="e895e-232">ファクトリの既定の実装は、名前に基づいてステップをインスタンス化します。</span><span class="sxs-lookup"><span data-stu-id="e895e-232">The default implementation of the factory instantiates the step based on name.</span></span> <span data-ttu-id="e895e-233">したがって、コントローラーの最初のステップとして **ProdProcessGuidePromptProductionIdStep** のインスタンスを作成するには、2 つの操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="e895e-233">Therefore, to instantiate **ProdProcessGuidePromptProductionIdStep** as the first step in the controller, you must do two things:</span></span>

-   <span data-ttu-id="e895e-234">**ProdProcessGuidePromptProductionIdStep** クラスを **ProcessGuideStepName** 属性で修飾します。</span><span class="sxs-lookup"><span data-stu-id="e895e-234">Decorate the **ProdProcessGuidePromptProductionIdStep** class with a **ProcessGuideStepName** attribute.</span></span>

    ```xpp
    [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))] public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
    ```

-   <span data-ttu-id="e895e-235">コントローラー クラスで、抽象メソッド **initialStepName()** を実装して、ステップの名前を戻します。</span><span class="sxs-lookup"><span data-stu-id="e895e-235">In the controller class, implement the abstract method **initialStepName()** to return the step name.</span></span>

    ```xpp
    protected final ProcessGuideStepName initialStepName()
    {
        return classStr(ProdProcessGuidePromptProductionIdStep);
    }
    ````   
    
> [!NOTE]
> <span data-ttu-id="e895e-236">**ProcessGuideStepName** 属性の値は、上記のように、クラス名と完全に一致する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e895e-236">The value in the **ProcessGuideStepName** attribute does not need to exactly match the class name as shown above.</span></span> <span data-ttu-id="e895e-237">ただし、これを実装することにより、クラスを使用する場合の相互参照に関する均一性とタイプ セーフが生じます。</span><span class="sxs-lookup"><span data-stu-id="e895e-237">However, implementing this allows for uniformity and type-safety around cross-references when using the class.</span></span> <span data-ttu-id="e895e-238">この名前付け規則を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e895e-238">Using this naming convention is recommended.</span></span>
>
> <span data-ttu-id="e895e-239">ステップの **ProcessGuideStepName** ベースのインスタンス化は、**ProcessGuideStepDefaultFactory** クラスで実装されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-239">The **ProcessGuideStepName** based instantiation of the step is implemented in the **ProcessGuideStepDefaultFactory** class.</span></span> <span data-ttu-id="e895e-240">まれに、異なる戦略でステップのインスタンス化が必要になることがありますが、その場合は次のようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e895e-240">In the rare case that you want a different strategy for instantiating the step, you need to do the following:</span></span>
> -   <span data-ttu-id="e895e-241">**ProcessGuidStepAbstractFactory** から継承する新しいファクトリ クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="e895e-241">Create a new factory class inheriting from **ProcessGuidStepAbstractFactory**.</span></span>
> -   <span data-ttu-id="e895e-242">必要に応じて、ファクトリが必要とするパラメーターを含む **ProcessGuideIStepCreationParameters** インターフェイスを実装する新しいパラメーター クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="e895e-242">Optionally, create a new parameter class implementing the **ProcessGuideIStepCreationParameters** interface, containing the parameters the factory would need.</span></span>
> -   <span data-ttu-id="e895e-243">コントローラー クラスで、**stepFactory()** および **stepCreationParameters()** メソッドを上書きし、上記のファクトリとパラメータを返します。</span><span class="sxs-lookup"><span data-stu-id="e895e-243">In your controller class, override the **stepFactory()** and **stepCreationParameters()** methods to return the above factory and parameters.</span></span>

<span data-ttu-id="e895e-244">次のステップでは、**ProdProcessGuidePromptProductionIdStep** クラスの機能を実装します。</span><span class="sxs-lookup"><span data-stu-id="e895e-244">The next step is to implement the functionality of the **ProdProcessGuidePromptProductionIdStep** class.</span></span> <span data-ttu-id="e895e-245">ユーザーが入力したデータを処理し、ステップがいつ完了するかを決定するためのユーザー インターフェイスを構築するためのロジックを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e895e-245">You need to implement the logic for building the user interface, processing the user-entered data, and determining when the step is complete.</span></span>

### <a name="building-the-user-interface-for-the-first-step"></a><span data-ttu-id="e895e-246">最初のステップのユーザー インターフェイスの構築</span><span class="sxs-lookup"><span data-stu-id="e895e-246">Building the user interface for the first step</span></span>

<span data-ttu-id="e895e-247">ユーザー インターフェイスは、**ProcessGuidePageBuilder** 抽象クラスからから継承するクラスを使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-247">The user interface is built using a class inheriting from the **ProcessGuidePageBuilder** abstract class.</span></span> <span data-ttu-id="e895e-248">この手順では、**ProdProcessGuidePromptProductionIdPageBuilder** が何をするかを表すクラスを指定します。</span><span class="sxs-lookup"><span data-stu-id="e895e-248">For this step, name the class to represent what it does – **ProdProcessGuidePromptProductionIdPageBuilder**.</span></span>

<span data-ttu-id="e895e-249">クラスのインスタンス化メカニズムは、ステップがコントローラーからインスタンス化された方法と似ています。</span><span class="sxs-lookup"><span data-stu-id="e895e-249">The instantiation mechanism of the class is similar to how the step was instantiated from the controller.</span></span> 

-   <span data-ttu-id="e895e-250">**ProdProcessGuidePromptProductionIdPageBuilder** クラスを **ProcessGuidePageBuilderName** 属性で修飾します。</span><span class="sxs-lookup"><span data-stu-id="e895e-250">Decorate the **ProdProcessGuidePromptProductionIdPageBuilder** class with a **ProcessGuidePageBuilderName** attribute.</span></span>

    ```xpp
    [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))] public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
    ```

-   <span data-ttu-id="e895e-251">**ProdProcessGuidePromptProductionIdStep** クラスで、抽象メソッド **pageBuilderName()** を実装してこの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="e895e-251">In the **ProdProcessGuidePromptProductionIdStep** class, implement the abstract method **pageBuilderName()** to return this name.</span></span>

    ```xpp
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
    }
    ```    

> [!TIP]
> <span data-ttu-id="e895e-252">ステップ ファクトリと同様、ページ ビルダ ファクトリに実装される抽象ファクトリ パターンもあります。</span><span class="sxs-lookup"><span data-stu-id="e895e-252">Similar to the step factory, there is also an abstract factory pattern implemented for the page builder factory.</span></span> <span data-ttu-id="e895e-253">ですから、まれに、異なる戦略でページ ビルダーのインスタンス化が必要になることがありますが、その場合は次のようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="e895e-253">So, in the rare case that you want a different strategy for instantiating the page builder, you can do the following:</span></span>
> - <span data-ttu-id="e895e-254">**ProcessGuidePageBuilderAbstractFactory** から継承する新しいファクトリ クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="e895e-254">Create a new factory class inheriting from **ProcessGuidePageBuilderAbstractFactory**.</span></span>
> - <span data-ttu-id="e895e-255">必要に応じて、ファクトリが必要とするパラメーターを含む **ProcessGuideIPageBuilderCreationParameters** インターフェイスを実装する新しいパラメーター クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="e895e-255">Optionally, create a new parameter class implementing the **ProcessGuideIPageBuilderCreationParameters** interface, containing the parameters the factory would need.</span></span>
> - <span data-ttu-id="e895e-256">ステップ クラスで、**pageBuilderFactory()** および **pageBuilderCreationParameters()** メソッドを上書きし、上記のファクトリとパラメータを返します。</span><span class="sxs-lookup"><span data-stu-id="e895e-256">In your step class, override the **pageBuilderFactory()** and **pageBuilderCreationParameters()** methods to return the above factory and parameters.</span></span>

<span data-ttu-id="e895e-257">ユーザー インターフェイスを実装するには、製造オーダー ID を入力するための 1 つのテキスト ボックスに加えて、**OK** ボタンおよび **キャンセル** ボタンがあるページが必要です。</span><span class="sxs-lookup"><span data-stu-id="e895e-257">To implement the user interface you need a page with one text box to enter the production order ID, plus an **OK** button and a **Cancel** button.</span></span> <span data-ttu-id="e895e-258">**キャンセル** ボタンは、プロセスを終了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e895e-258">The **Cancel** button should exit the process.</span></span>

<span data-ttu-id="e895e-259">これを実装するには、**ProdProcessGuidePromptProductionIdPageBuilder** クラスで 2 つのメソッドを上書きする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e895e-259">To implement this, you need to override two methods in the **ProdProcessGuidePromptProductionIdPageBuilder** class:</span></span>

-   <span data-ttu-id="e895e-260">**addDataControls()** メソッドを使用してテキスト ボックスを追加します。</span><span class="sxs-lookup"><span data-stu-id="e895e-260">Use the **addDataControls()** method to add the text box.</span></span>

    ```xpp
    protected final void addDataControls(ProcessGuidePage _page)
    {
        _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
    }
    ```   

-   <span data-ttu-id="e895e-261">**addActionControls()** メソッドを使用して **OK** および **Cancel** ボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="e895e-261">Use the **addActionControls()** method to add the **OK** and **Cancel** buttons.</span></span>

    ```xpp
    protected final void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelExitProcess));
    }
    ``` 

<span data-ttu-id="e895e-262">これは、ボタンの前に、データ コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="e895e-262">This adds the data controls, followed by the buttons.</span></span> <span data-ttu-id="e895e-263">ただし、データ コントロールとボタンが散在する画面を作成する場合、柔軟性の代わりに **addControls()** メソッドを上書きできます。</span><span class="sxs-lookup"><span data-stu-id="e895e-263">However, if you want to build a screen with interspersed data controls and buttons, you can override the **addControls()** method instead for flexibility.</span></span>

<span data-ttu-id="e895e-264">考慮すべきの追加のシナリオは、たとえば、ユーザーが正しくない製造オーダー ID を入力した場合など、検証エラーが発生した場合にページを再構築する方法です。</span><span class="sxs-lookup"><span data-stu-id="e895e-264">An additional scenario to consider is how to rebuild the page in case of validation failures, for example if the user enters an incorrect production order ID.</span></span> <span data-ttu-id="e895e-265">**ProcessGuidePageBuilder** 基本クラスは、ユーザー インターフェイスを再構築し、スキャンした値をクリアし、エラー メッセージのあるエラー コントロールを追加するという、既定の動作を実装します。</span><span class="sxs-lookup"><span data-stu-id="e895e-265">The **ProcessGuidePageBuilder** base class implements the default behavior, which rebuilds the user interface, clears out the scanned value, and adds the error control with the error message.</span></span> <span data-ttu-id="e895e-266">これは、使用する既定の動作であるため、エラーを処理するコードを追加する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e895e-266">Because this is the default behavior that you want to use, you do not need to add any code for handling errors.</span></span>

> [!TIP]
> <span data-ttu-id="e895e-267">エラー状況のカスタム UI 動作を実装する場合は、1 つまたは複数のメソッド **rebuildFromRequestPage()**、**isErrorState()**、および **reuseRequestPageOnError()** を上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="e895e-267">If you want to implement custom UI behavior for error situations, you can override one or more of the methods **rebuildFromRequestPage()**, **isErrorState()**, and **reuseRequestPageOnError()**.</span></span>

### <a name="processing-the-user-entered-data-in-the-first-step"></a><span data-ttu-id="e895e-268">最初の手順でユーザーが入力したデータの処理</span><span class="sxs-lookup"><span data-stu-id="e895e-268">Processing the user-entered data in the first step</span></span>

<span data-ttu-id="e895e-269">データの処理は、**ProcessGuideDataProcessorDefault** クラスで行われ、その後、レガシ **WhsRfControlData** クラスが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-269">The processing of the data is done in the **ProcessGuideDataProcessorDefault** class, which in turn invokes the legacy **WhsRfControlData** class.</span></span> <span data-ttu-id="e895e-270">この既定の動作を変更する必要はありません。**WhsRfControlData** には、既に **ProdId** フィールを検証するロジックがあるため、これを処理するロジックを記述する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e895e-270">No changes are needed to this default behavior, and **WhsRfControlData** already has logic for validating the **ProdId** field, so you do not need to write any logic for handling this.</span></span> <span data-ttu-id="e895e-271">検証ロジックに必要な機能拡張がある場合、**WhsControl** ベースの拡張メカニズムを使用することを検討します。</span><span class="sxs-lookup"><span data-stu-id="e895e-271">In case of required extensions for the validation logic, consider using the **WhsControl** based extension mechanism.</span></span>

### <a name="determine-if-the-first-step-is-complete"></a><span data-ttu-id="e895e-272">最初の手順が完全であるかどうかを判断</span><span class="sxs-lookup"><span data-stu-id="e895e-272">Determine if the first step is complete</span></span>

<span data-ttu-id="e895e-273">検証に成功したらを、ステップを完了としてマークします。</span><span class="sxs-lookup"><span data-stu-id="e895e-273">When the validation is successful, it is time to mark the step as completed.</span></span> <span data-ttu-id="e895e-274">これは、基本クラスで行われますが、手順の完了を決定する条件を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e895e-274">This is done in the base class, however, you need to implement the condition to determine the step completion.</span></span> <span data-ttu-id="e895e-275">オーバーライドされた次のメソッドがそれを行います。</span><span class="sxs-lookup"><span data-stu-id="e895e-275">The following overridden method does that.</span></span>

```xpp
protected final boolean isComplete()
{
    WhsrfPassthrough pass = controller.parmSessionState().parmPass();
    ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);
        return (prodId != '');
}
```   

### <a name="step-two-view-order-details-and-confirm"></a><span data-ttu-id="e895e-276">ステップ 2: 注文の詳細を表示して確認</span><span class="sxs-lookup"><span data-stu-id="e895e-276">Step two: View order details and confirm</span></span>

<span data-ttu-id="e895e-277">プロセスの 2 番目のステップでは、ユーザーに、注文に関する詳細を含む画面が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-277">In the second step in the process, the user is shown a screen with details about the order.</span></span> <span data-ttu-id="e895e-278">ユーザーは **OK** ボタンをクリックして製造オーダーの開始を確認するか、**キャンセル** をクリックしてプロセスの開始に戻ることができます。</span><span class="sxs-lookup"><span data-stu-id="e895e-278">The user can either click the **OK** button to confirm the start of the production order, or click **Cancel** to go back to the start of the process.</span></span> <span data-ttu-id="e895e-279">この例では、ステップ **ProdProcessGuideConfirmProductionOrderStep** とページ ビルダー クラス **ProdProcessGuideConfirmProductionOrderPageBuilder** を指定します。</span><span class="sxs-lookup"><span data-stu-id="e895e-279">For this example, name the step **ProdProcessGuideConfirmProductionOrderStep** and the page builder class **ProdProcessGuideConfirmProductionOrderPageBuilder**.</span></span>

<span data-ttu-id="e895e-280">ProdProcessGuideConfirmProductionOrderStep クラスは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="e895e-280">The ProdProcessGuideConfirmProductionOrderStep class looks like the following.</span></span>

```xpp
[ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
{
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
     }
}
```     

<span data-ttu-id="e895e-281">ユーザーはここに値を入力してないため、**isComplete()** メソッドを上書きする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e895e-281">Because the user does not enter any values here, you do not need to override the **isComplete()** method.</span></span> <span data-ttu-id="e895e-282">ユーザーが **OK** をクリックすると、ステップが完了します。</span><span class="sxs-lookup"><span data-stu-id="e895e-282">The step is complete when the user clicks **OK**.</span></span>

<span data-ttu-id="e895e-283">ページ ビルダー クラスは、**addDataControls()** メソッドを上書きして 3 つのラベルを追加します。</span><span class="sxs-lookup"><span data-stu-id="e895e-283">The page builder class overrides the **addDataControls()** method to add three labels.</span></span> <span data-ttu-id="e895e-284">最初のラベルには、製造オーダー ID が表示され、2 番目には、品目情報 (品目 ID、分析コード、説明など) が表示され、3 番目には数量との測定単位が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e895e-284">The first label shows the production order ID, the second contains item information (such as item ID, dimensions, or description) and the third contains the quantity and unit of measure.</span></span>

<span data-ttu-id="e895e-285">その後、**addActionControls()** が上書きされ、2 つのボタン (**OK** ボタンと、プロセスをキャンセルしてプロセスの先頭に戻る **Cancel** ボタン) を追加します。</span><span class="sxs-lookup"><span data-stu-id="e895e-285">The **addActionControls()** is then overridden to add 2 buttons – the **OK** button, and the **Cancel** button to cancel the process and go back to the start of the process.</span></span>

```xpp
/// <summary>
/// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
/// and then confirm.
/// </summary>
[ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
{
    protected void addDataControls(ProcessGuidePage _page)
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;
        
        _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
        _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
        _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

        if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
        {
            _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
        }
    }

    protected void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelResetProcess));
    }
```

> [!NOTE]
> <span data-ttu-id="e895e-286">このトピックでは、X + + メソッドに対して同じソースコードをアプリケーションエクスプローラーを使用して検索できます。</span><span class="sxs-lookup"><span data-stu-id="e895e-286">You can find the same source code for the X++ methods in this topic by using the Application Explorer.</span></span> <span data-ttu-id="e895e-287">クラス名をフィルター処理し、クラス名を右クリックして **コードの表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e895e-287">Filter on the class name, and then right-click the class name and select **View code**.</span></span>

### <a name="step-3-start-the-production-order"></a><span data-ttu-id="e895e-288">ステップ 3: 製造オーダーを開始する</span><span class="sxs-lookup"><span data-stu-id="e895e-288">Step 3: Start the production order</span></span>

<span data-ttu-id="e895e-289">3 番目のステップでは、製造オーダーの開始のビジネス ロジックを実行します。</span><span class="sxs-lookup"><span data-stu-id="e895e-289">The third step is where the business logic of starting the production order is executed.</span></span> <span data-ttu-id="e895e-290">このステップは、ユーザー インターフェイスがないという点で前のステップとは少し異なります。</span><span class="sxs-lookup"><span data-stu-id="e895e-290">This step is somewhat different from the previous steps, in that, this step does not have a user interface.</span></span> <span data-ttu-id="e895e-291">ユーザーが前のステップで **OK** をクリックすると、このステップがサイレントで実行されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-291">This step gets executed silently when the user clicks **OK** in the previous step.</span></span>

<span data-ttu-id="e895e-292">**ProcessGuideStepWithoutPrompt** 抽象クラスは、そのようなステップの既定の動作を実装します。</span><span class="sxs-lookup"><span data-stu-id="e895e-292">The **ProcessGuideStepWithoutPrompt** abstract class implements the default behavior for such steps.</span></span> <span data-ttu-id="e895e-293">したがって、現在のステップは、**ProcessGuideStepWithoutPrompt** クラスを拡張し、**doExecute()** メソッドを上書きする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e895e-293">The current step, therefore, should extend the **ProcessGuideStepWithoutPrompt** class and override the **doExecute()** method.</span></span>

<span data-ttu-id="e895e-294">次のコード例は、そのクラスと **doExecute()** メソッドの実装を示しています。</span><span class="sxs-lookup"><span data-stu-id="e895e-294">The following code example shows the class and the **doExecute()** method implementation.</span></span> <span data-ttu-id="e895e-295">このメソッドは単に、、セッションの状態から注文 ID とユーザー ID を取得し、この製造オーダーを開始するメソッドを呼び出すだけです。</span><span class="sxs-lookup"><span data-stu-id="e895e-295">The method simply retrieves the order ID and user ID from the session state and invokes the method to start this production order.</span></span>

```xpp
/// <summary>
/// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
/// </summary>
[ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
{
    protected final void doExecute()
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        WhsWorkExecute workExecute = WhsWorkExecute::construct();
        workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

        this.addProcessCompletionMessage();

        super();
    }

}
```

<span data-ttu-id="e895e-296">例外が発生した場合、フレームワーク例外処理ロジックは、前の手順でプロセスがロールバックされることを保証します。</span><span class="sxs-lookup"><span data-stu-id="e895e-296">In case of an exception, the framework exception handling logic ensures that the process is rolled back to the previous step.</span></span>

> [!NOTE]
> <span data-ttu-id="e895e-297">**addProcessCompletionMessage()** の呼び出しは、ナビゲーション パラメーターに "作業完了" メッセージを追加します。</span><span class="sxs-lookup"><span data-stu-id="e895e-297">The invoke to **addProcessCompletionMessage()** adds the “Work completed” message to the navigation parameters.</span></span> <span data-ttu-id="e895e-298">このメッセージは、(ユーザー インターフェイスがあると仮定した場合) 次のステップで表示されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-298">The next step (assuming it has a user interface) will display this message.</span></span> <span data-ttu-id="e895e-299">基本クラスは、このロジックを処理するため、この動作を実現するために特定のコードをプロセス クラスに追加する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e895e-299">The base classes handle this logic, and no specific code needs to be added to the process classes to achieve this behavior.</span></span>


### <a name="building-the-navigation-through-the-steps"></a><span data-ttu-id="e895e-300">ステップでのナビゲーションの構築</span><span class="sxs-lookup"><span data-stu-id="e895e-300">Building the navigation through the steps</span></span>

<span data-ttu-id="e895e-301">**ProcessGuideController** 基本クラスは、**ProcessGuideNavigationAgentDefault** クラスのインスタンスを作成します。これは、ソースおよび出力先のステップの簡単なマップである事前に定義されたナビゲーション工順に依存しています。</span><span class="sxs-lookup"><span data-stu-id="e895e-301">The **ProcessGuideController** base class instantiates the **ProcessGuideNavigationAgentDefault** class, which relies on a pre-defined navigation route, which is a simple map of source and destination steps.</span></span> <span data-ttu-id="e895e-302">生産開始シナリオでは、条件分岐がないため、この実装で十分です。</span><span class="sxs-lookup"><span data-stu-id="e895e-302">For the production start scenario, because there is no conditional branching, this implementation would suffice.</span></span> <span data-ttu-id="e895e-303">したがって、必要があるのは、**initializeNavigationRoute()** メソッドをオーバーライドしてナビゲーション工順を定義することだけです。</span><span class="sxs-lookup"><span data-stu-id="e895e-303">Therefore, you only need to override the **initializeNavigationRoute()** method to define the navigation route.</span></span>

```xpp
    protected ProcessGuideNavigationRoute initializeNavigationRoute()
    {
        ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
        navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

        return navigationRoute;
    }
```

<span data-ttu-id="e895e-304">条件付き分岐が配置されるプロセスがあります (ユーザーの操作、またはその他の条件に基づく)。</span><span class="sxs-lookup"><span data-stu-id="e895e-304">There are processes where there will be conditional branching (based on user actions, or any other conditions).</span></span> <span data-ttu-id="e895e-305">このようなプロセスは、次の操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="e895e-305">Such processes need to do the following:</span></span>

-   <span data-ttu-id="e895e-306">**ProcessGuideNavigationAgent** クラスから継承された特定のナビゲーション エージェントを実装します。</span><span class="sxs-lookup"><span data-stu-id="e895e-306">Implement specific navigation agents inherited from the **ProcessGuideNavigationAgent** class.</span></span>

-   <span data-ttu-id="e895e-307">現在のステップ、セッションの状態、ユーザーのアクション、または他のロジックに基づいて適切なナビゲーション エージェントのインスタンスを作成するためのロジックを含む、**ProcessGuideNavigationAgentAbstractFactory** クラスから継承された特定のナビゲーション エージェント ファクトリを実装します。</span><span class="sxs-lookup"><span data-stu-id="e895e-307">Implement the specific navigation agent factory inherited from the **ProcessGuideNavigationAgentAbstractFactory** class, containing logic to instantiate the correct navigation agent based on current step, session state, user action, or other logic.</span></span>

-   <span data-ttu-id="e895e-308">必要に応じて、コントローラー クラスで **navigationAgentCreationParameters()** をオーバーライドして、適切なパラメーターを渡します。</span><span class="sxs-lookup"><span data-stu-id="e895e-308">Optionally, override **navigationAgentCreationParameters()** in the controller class to pass suitable parameters.</span></span>

-   <span data-ttu-id="e895e-309">コントローラーで **navigationAgentFactory()** をオーバーライドして、上で作成したナビゲーション エージェント ファクトリのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="e895e-309">Override **navigationAgentFactory()** in the controller to instantiate the navigation agent factory created above.</span></span>

### <a name="action-classes"></a><span data-ttu-id="e895e-310">アクション クラス</span><span class="sxs-lookup"><span data-stu-id="e895e-310">Action classes</span></span>

<span data-ttu-id="e895e-311">アクション クラスはユーザーの操作を表すため、この例では、 **OK** アクションを使用して、アクションの作成方法を表示します。</span><span class="sxs-lookup"><span data-stu-id="e895e-311">Action classes represent user actions, so this example uses the **OK** action to show how the actions are created.</span></span>

```xpp
[ProcessGuideActionName(#ActionOK)]
public class ProcessGuideOKAction extends ProcessGuideAction
{
    public final str label()
    {
        return "@SYS5473";
     }
     protected final void doExecute()
     {
        step.executeOKAction();
      }
}
```    

<span data-ttu-id="e895e-312">クラスは 2 つの抽象メソッドを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e895e-312">The class must implement 2 abstract methods:</span></span>

-   <span data-ttu-id="e895e-313">**label()**: この操作に関連付けられているボタン コントロールに表示するためのラベルを返します。</span><span class="sxs-lookup"><span data-stu-id="e895e-313">**label()**, which returns the label to be displayed in a button control tied to this action.</span></span>

-   <span data-ttu-id="e895e-314">**doExecute()**: アクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="e895e-314">**doExecute()**, which performs the action.</span></span> <span data-ttu-id="e895e-315">既に述べたように、**OK** ボタンはステップでコールバックを実行するだけです。</span><span class="sxs-lookup"><span data-stu-id="e895e-315">As mentioned earlier, the **OK** button simply performs a callback to the step.</span></span> <span data-ttu-id="e895e-316">ただし、その他のアクションにはここにより複雑なロジックがある場合があります。</span><span class="sxs-lookup"><span data-stu-id="e895e-316">However, other actions might have more complex logic here.</span></span>

<span data-ttu-id="e895e-317">アクションは、**ProcessGuideActionName** 属性に基づいて **SysExtension** フレームワークを使用してインスタンス化されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-317">The actions are instantiated using **SysExtension** framework based on the **ProcessGuideActionName** attribute.</span></span> <span data-ttu-id="e895e-318">ページ ビルダーのインスタンス化と同様、ステップ クラスは、既定のアクション ファクトリを実装し、それを上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="e895e-318">Similar to the instantiation of page builders, the step class implements the default action factory, and it is possible to override that.</span></span> <span data-ttu-id="e895e-319">ページ ビルダーは、次のようにボタン コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="e895e-319">The page builder adds a button control like this.</span></span>

```xpp
_page.addButton(step.createAction(#ActionOK), true);
```

<span data-ttu-id="e895e-320">これを行うことにより、渡された名前のアクション クラスを作成するようステップに求め、そのアクションをボタンに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="e895e-320">In doing so, it asks the step to create an action class for the passed name and ties that action to the button.</span></span>

### <a name="summary"></a><span data-ttu-id="e895e-321">集計</span><span class="sxs-lookup"><span data-stu-id="e895e-321">Summary</span></span>

<span data-ttu-id="e895e-322">このトピックで説明したことをすべてまとめるため、プロセスに必要なコードの包括的な概要をここに示します。</span><span class="sxs-lookup"><span data-stu-id="e895e-322">To summarize everything that's been explained in this topic, here's a comprehensive summary of the code needed for the process:</span></span>

1.  <span data-ttu-id="e895e-323">**ProdProcessGuideProductionStartController**</span><span class="sxs-lookup"><span data-stu-id="e895e-323">**ProdProcessGuideProductionStartController**</span></span>

    1.  <span data-ttu-id="e895e-324">**initialStepName()** を上書きして、最初のステップの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="e895e-324">Override **initialStepName()** to provide the name of the first step.</span></span>
    2.  <span data-ttu-id="e895e-325">**initializeNavigationRoute()** を上書きして、ナビゲーション マップを作成します。</span><span class="sxs-lookup"><span data-stu-id="e895e-325">Override **initializeNavigationRoute()** to construct the navigation map.</span></span>

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideProductionStartController</c> class is the controller class for the production order start process guide.
        /// </summary>
        [WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
        public class ProdProcessGuideProductionStartController extends ProcessGuideController
        {
            protected ProcessGuideStepName initialStepName()
            {
                return classStr(ProdProcessGuidePromptProductionIdStep);
            }

            protected ProcessGuideNavigationRoute initializeNavigationRoute()
            {
                ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
                navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

                return navigationRoute;
            }

        }
        ```

2.  <span data-ttu-id="e895e-326">**ProdProcessGuidePromptProductionIdStep**</span><span class="sxs-lookup"><span data-stu-id="e895e-326">**ProdProcessGuidePromptProductionIdStep**</span></span>

    1.  <span data-ttu-id="e895e-327">**isComplete()** を上書きし、ステップが完了と見なされるタイミングを指定します。</span><span class="sxs-lookup"><span data-stu-id="e895e-327">Override **isComplete()** to specify when the step is considered complete.</span></span>
    2.  <span data-ttu-id="e895e-328">**pageBuilderName()** を上書きし、使用するページ ビルダーを指定します。</span><span class="sxs-lookup"><span data-stu-id="e895e-328">Override **pageBuilderName()** to specify the page builder to be used.</span></span>

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdStep</c> represents a step that 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))]
        public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
        {
            protected boolean isComplete()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);

                return (prodId != '');
            }

            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
            }

        }
        ```

3.  <span data-ttu-id="e895e-329">**ProdProcessGuidePromptProductionIdPageBuilder**</span><span class="sxs-lookup"><span data-stu-id="e895e-329">**ProdProcessGuidePromptProductionIdPageBuilder**</span></span>

    1.  <span data-ttu-id="e895e-330">**addDataControls()** を上書きし、**製品 ID** テキスト ボックスを追加します。</span><span class="sxs-lookup"><span data-stu-id="e895e-330">Override **addDataControls()** to add the **Prod ID** textbox.</span></span>
    2.  <span data-ttu-id="e895e-331">**addActionControls()** をオーバーライドして **OK** および **Cancel** ボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="e895e-331">Override **addActionControls()** to add the **OK** and **Cancel** buttons.</span></span>
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdPageBuilder</c> class builds a page 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))]
        public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelExitProcess));
            }

        }
        ```

4.  <span data-ttu-id="e895e-332">**ProdProcessGuideConfirmProductionOrderStep**</span><span class="sxs-lookup"><span data-stu-id="e895e-332">**ProdProcessGuideConfirmProductionOrderStep**</span></span>

    1.  <span data-ttu-id="e895e-333">**pageBuilderName()** を上書きし、使用するページ ビルダーを指定します。</span><span class="sxs-lookup"><span data-stu-id="e895e-333">Override **pageBuilderName()** to specify the page builder to be used.</span></span>
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderStep</c> class represents the step for viewing production order
        /// details and confirming the same.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
        public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
        {    
            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
            }

        }
        ```

3.  <span data-ttu-id="e895e-334">**ProdProcessGuideConfirmProductionOrderPageBuilder**</span><span class="sxs-lookup"><span data-stu-id="e895e-334">**ProdProcessGuideConfirmProductionOrderPageBuilder**</span></span>

    1.  <span data-ttu-id="e895e-335">**addDataControls()** をオーバーライドし、注文、品目、および数量情報ラベルを追加します。</span><span class="sxs-lookup"><span data-stu-id="e895e-335">Override **addDataControls()** to add the order, item, and quantity information labels.</span></span>

    2.  <span data-ttu-id="e895e-336">**addActionControls()** をオーバーライドして **OK** および **Cancel** ボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="e895e-336">Override **addActionControls()** to add the **OK** and **Cancel** buttons.</span></span>
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
        /// and then confirm.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
        public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;

                _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
                _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
                _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

                if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
                {
                    _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
                }
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelResetProcess));
            }

        ```

        > [!NOTE]
        > <span data-ttu-id="e895e-337">品目情報のラベルを生成するために使用される **generateItemInfoForProdId()** メソッドは、このトピックから除外されます。</span><span class="sxs-lookup"><span data-stu-id="e895e-337">The **generateItemInfoForProdId()** method, which is used for generating the item information labels, is excluded from this topic.</span></span> <span data-ttu-id="e895e-338">このメソッドは、品目 ID、説明、および分析コードを取得するいくつかのテーブルを照会します。</span><span class="sxs-lookup"><span data-stu-id="e895e-338">This method queries a few tables to get item ID, description, and dimensions.</span></span> <span data-ttu-id="e895e-339">**generateItemInfoForProdId()** についてよく理解する場合、ソース コードを確認します。</span><span class="sxs-lookup"><span data-stu-id="e895e-339">If you want a better understanding of **generateItemInfoForProdId()**, look at the source code.</span></span>

4.  <span data-ttu-id="e895e-340">**ProdProcessGuideStartProductionOrderStep**</span><span class="sxs-lookup"><span data-stu-id="e895e-340">**ProdProcessGuideStartProductionOrderStep**</span></span>

    1.  <span data-ttu-id="e895e-341">**doExecute()** を上書きして生産プロセスの開始を実行し、プロセスの完了メッセージを追加します。</span><span class="sxs-lookup"><span data-stu-id="e895e-341">Override **doExecute()** to perform the production start process and add the process completion message.</span></span>

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
        public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
        {
            protected final void doExecute()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                WhsWorkExecute workExecute = WhsWorkExecute::construct();
                workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

                this.addProcessCompletionMessage();

                super();
            }

        }
        ```

> [!NOTE]
> <span data-ttu-id="e895e-342">多くの一般的なパターン (エラー時の UI の再生成、設定プロセスの完了メッセージ、**OK** および **キャンセル** 動作) がフレームワークに移動された点に注意してください。したがって、エラーの発生しやすい定型コードと、プロセス間で不整合な動作をする危険性を備えた定型コードの両方をアプリケーション開発者が記述しなくてよくなります。</span><span class="sxs-lookup"><span data-stu-id="e895e-342">Note that a lot of the common patterns (regeneration of UI on error, setting process completion message, **OK** and **Cancel** behavior) have been moved to the framework – thus saving the application developer from writing boilerplate code that is both error prone, and has a risk of inconsistent behavior across processes.</span></span> <span data-ttu-id="e895e-343">ただし、共通するパスとは異なるシナリオが必要な場合、アプリケーション開発者には、適切なメソッドをオーバーライドするオプションが用意されていますが、その場合、それは明示的なかつ追跡可能な意図的な誤差です。</span><span class="sxs-lookup"><span data-stu-id="e895e-343">Where the scenario needs to deviate from the common path, though, the application developer is provided the option of overriding suitable methods – but then that is an intentional deviation that is both explicit and trackable.</span></span>


### <a name="extending-a-business-process"></a><span data-ttu-id="e895e-344">業務プロセスの拡張</span><span class="sxs-lookup"><span data-stu-id="e895e-344">Extending a business process</span></span>

<span data-ttu-id="e895e-345">これまでのところ、このトピックでは **ProcessGuide** フレームワークを使用して新しいプロセスを作成する方法が強調表示されています。</span><span class="sxs-lookup"><span data-stu-id="e895e-345">So far, this topic has highlighted how to build a new process using the **ProcessGuide** framework.</span></span> <span data-ttu-id="e895e-346">この最後のセクションでは、このビジネス プロセスを拡張する方法の例をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="e895e-346">In this final section, you will find some examples of how this business process can be extended.</span></span>

### <a name="add-a-step-in-a-flow-using-processguidenavigationagentdefault"></a><span data-ttu-id="e895e-347">フローにおけるステップの追加 (ProcessGuideNavigationAgentDefault を使用)</span><span class="sxs-lookup"><span data-stu-id="e895e-347">Add a step in a flow (using ProcessGuideNavigationAgentDefault)</span></span>

<span data-ttu-id="e895e-348">拡張場所:</span><span class="sxs-lookup"><span data-stu-id="e895e-348">Where to extend:</span></span>

-   <span data-ttu-id="e895e-349">プロセスの **ProcessGuideController** クラスの子。</span><span class="sxs-lookup"><span data-stu-id="e895e-349">Child of **ProcessGuideController** class for the process.</span></span>

<span data-ttu-id="e895e-350">拡張方法:</span><span class="sxs-lookup"><span data-stu-id="e895e-350">How to extend:</span></span>

-   <span data-ttu-id="e895e-351">コントローラー クラスで **initializeNavigationRoute()** メソッドを拡張し、**ProcessGuideNavigationRoute** クラスで **addFollowingStep()** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e895e-351">Extend the **initializeNavigationRoute()** method in the controller class, and invoke **addFollowingStep()** in the **ProcessGuideNavigationRoute** class.</span></span>

### <a name="add-a-step-in-a-flow-using-custom-navigation-agent"></a><span data-ttu-id="e895e-352">フローにおけるステップの追加 (カスタム ナビゲーション エージェントを使用)</span><span class="sxs-lookup"><span data-stu-id="e895e-352">Add a step in a flow (using custom navigation agent)</span></span>

<span data-ttu-id="e895e-353">拡張場所:</span><span class="sxs-lookup"><span data-stu-id="e895e-353">Where to extend:</span></span>

-   <span data-ttu-id="e895e-354">**ProdProcessGuideNavigationAgentFactory/ProdProcessGuideNavigationAgent** の子。</span><span class="sxs-lookup"><span data-stu-id="e895e-354">Child of **ProdProcessGuideNavigationAgentFactory/ProdProcessGuideNavigationAgent**.</span></span>

<span data-ttu-id="e895e-355">拡張方法:</span><span class="sxs-lookup"><span data-stu-id="e895e-355">How to extend:</span></span>

-   <span data-ttu-id="e895e-356">必要なステップの名前を返す **ProcessGuideNavigationAgent** の新しい子クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="e895e-356">Create a new child class of **ProcessGuideNavigationAgent** that returns the desired step name.</span></span>

-   <span data-ttu-id="e895e-357">上で作成したナビゲーション エージェントを条件付きで返す **ProcessGuideNavigationAgentFactory** から派生した新しいクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="e895e-357">Create a new class deriving from **ProcessGuideNavigationAgentFactory** that conditionally returns the navigation agent created above.</span></span>

-   <span data-ttu-id="e895e-358">コントローラー クラスで **navigationAgentFactory()** メソッドを拡張し、上で作成したファクトリを返します。</span><span class="sxs-lookup"><span data-stu-id="e895e-358">Extend the **navigationAgentFactory()** method in the controller class to return the factory created above.</span></span>

### <a name="add-a-new-control-in-the-ui-of-an-existing-step"></a><span data-ttu-id="e895e-359">既存のステップの UI で新しいコントロールを追加</span><span class="sxs-lookup"><span data-stu-id="e895e-359">Add a new control in the UI of an existing step</span></span> 

<span data-ttu-id="e895e-360">拡張場所:</span><span class="sxs-lookup"><span data-stu-id="e895e-360">Where to extend:</span></span>

-   <span data-ttu-id="e895e-361">ステップの **ProdProcessGuidePageBuilder** の子。</span><span class="sxs-lookup"><span data-stu-id="e895e-361">Child of **ProdProcessGuidePageBuilder** for the step.</span></span>

<span data-ttu-id="e895e-362">拡張方法:</span><span class="sxs-lookup"><span data-stu-id="e895e-362">How to extend:</span></span>

-   <span data-ttu-id="e895e-363">**addDataControls()** メソッドを拡張し、その他のコントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="e895e-363">Extend the **addDataControls()** method and add the additional control.</span></span>

### <a name="complete-overhaul-of-the-user-interface-in-an-existing-step"></a><span data-ttu-id="e895e-364">既存のステップでのユーザー インターフェイスの全体的な修正</span><span class="sxs-lookup"><span data-stu-id="e895e-364">Complete overhaul of the user interface in an existing step</span></span>

<span data-ttu-id="e895e-365">拡張場所:</span><span class="sxs-lookup"><span data-stu-id="e895e-365">Where to extend:</span></span>

-   <span data-ttu-id="e895e-366">**ProdProcessGuideStep** の子。</span><span class="sxs-lookup"><span data-stu-id="e895e-366">Child of **ProdProcessGuideStep**.</span></span>

<span data-ttu-id="e895e-367">拡張方法:</span><span class="sxs-lookup"><span data-stu-id="e895e-367">How to extend:</span></span>

-   <span data-ttu-id="e895e-368">**ProdProcessGuidePageBuilder** クラスの新しい子クラスを作成し、目的のユーザー インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="e895e-368">Create a new child class of **ProdProcessGuidePageBuilder** class, and implement the desired user interface.</span></span>

-   <span data-ttu-id="e895e-369">ステップ クラスで **pageBuildeName()** メソッドを拡張し、上で作成したクラスの **ProcessGuidePageBuilderNameAttribute** を返します。</span><span class="sxs-lookup"><span data-stu-id="e895e-369">Extend the **pageBuildeName()** method in the step class to return the **ProcessGuidePageBuilderNameAttribute** for the class created above.</span></span>

### <a name="alter-logic-when-a-step-is-considered-complete"></a><span data-ttu-id="e895e-370">ステップが完了と見なされたときにロジックを変更します。</span><span class="sxs-lookup"><span data-stu-id="e895e-370">Alter logic when a step is considered complete</span></span>

<span data-ttu-id="e895e-371">拡張場所:</span><span class="sxs-lookup"><span data-stu-id="e895e-371">Where to extend:</span></span>

-   <span data-ttu-id="e895e-372">**ProdProcessGuideStep** の子。</span><span class="sxs-lookup"><span data-stu-id="e895e-372">Child of **ProdProcessGuideStep**.</span></span>

<span data-ttu-id="e895e-373">拡張方法:</span><span class="sxs-lookup"><span data-stu-id="e895e-373">How to extend:</span></span>

-   <span data-ttu-id="e895e-374">**isComplete()** メソッドを拡張し、追加ロジックを構築します。</span><span class="sxs-lookup"><span data-stu-id="e895e-374">Extend the **isComplete()** method to build the additional logic.</span></span>
