---
title: ルックアップのコンテキスト データ入力
description: このトピックでは、コンテキスト データ入力の仕組みについて説明し、ルックアップにこの動作が必要な開発者向けの実装の詳細とヒントを提供します。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 13631
ms.assetid: 5c41c565-5f83-47f9-a75e-ca5bb4b062e7
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d31699aa7501201f986994747fe94caf2635876
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189220"
---
# <a name="contextual-data-entry-for-lookups"></a><span data-ttu-id="875b2-103">ルックアップのコンテキスト データ入力</span><span class="sxs-lookup"><span data-stu-id="875b2-103">Contextual data entry for lookups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="875b2-104">データ入力のシナリオでは、そのエンティティが番号順序などの統合キーによって正式に識別される場合、ユーザーは詳細な内容を示す属性や自然言語属性でエンティティを識別しようとすることが一般的です。</span><span class="sxs-lookup"><span data-stu-id="875b2-104">In data entry scenarios, it is common for a user to attempt to identify an entity in terms of some more descriptive or natural language attribute if that entity is formally identified by a synthetic key, such as a number sequence.</span></span> <span data-ttu-id="875b2-105">コンテキスト データ入力機能を使用すると、統合キーまたはより記述的な属性のいずれかを検索フィールドに直接入力できます。</span><span class="sxs-lookup"><span data-stu-id="875b2-105">The contextual data entry feature allows users to type in either the synthetic key or a more descriptive attribute directly into a lookup field.</span></span> <span data-ttu-id="875b2-106">このページでは、コンテキスト データ入力の仕組みについて説明し、ルックアップにこの動作が必要な開発者向けの実装の詳細とヒントを提供します。</span><span class="sxs-lookup"><span data-stu-id="875b2-106">This page explains how contextual data entry works and also provides implementation details and tips for developers who want their lookups to have this behavior.</span></span>

## <a name="introduction"></a><span data-ttu-id="875b2-107">はじめに</span><span class="sxs-lookup"><span data-stu-id="875b2-107">Introduction</span></span>

<span data-ttu-id="875b2-108">データ入力のシナリオでは、そのエンティティが番号順序などの統合キーによって正式に識別される場合、ユーザーは詳細な内容を示す属性や自然言語属性でエンティティを識別しようとすることが一般的です。</span><span class="sxs-lookup"><span data-stu-id="875b2-108">In data entry scenarios, it is common for a user to attempt to identify an entity in terms of some more descriptive or natural language attribute if that entity is formally identified by a synthetic key, such as a number sequence.</span></span> <span data-ttu-id="875b2-109">ユーザーは、通常、Sales Order の作成時に **顧客口座** の **アカウント ID** の代わりに **アカウント名** を入力しようとします。</span><span class="sxs-lookup"><span data-stu-id="875b2-109">A user will typically attempt to enter an **Account Name** instead of an **Account ID** for the **Customer Account** when creating a Sales Order.</span></span> <span data-ttu-id="875b2-110">これは、顧客とのほとんどのやり取りは、何らかの統合識別子の代わりに実際の名前を使用して行われるためです。</span><span class="sxs-lookup"><span data-stu-id="875b2-110">This is because most interaction with a customer is done using their actual name instead of some synthetic identifier.</span></span> <span data-ttu-id="875b2-111">ただし、**顧客 ID** コントロールの基礎となる外部キーが、合成キー (数字のシーケンス) であるフィールドに関連するため、**アカウント名** を入力しようとすると失敗します。AX 2012 (およびそれ以前) は、入力された値を常に直接検証しようとします。</span><span class="sxs-lookup"><span data-stu-id="875b2-111">Unfortunately, any user’s attempt to enter an **Account Name** will fail because the **Customer account** control’s underlying foreign key relates to a field that is a synthetic key—a number sequence—and Dynamics AX 2012 (and older) will always attempt to validate the entered value directly.</span></span> <span data-ttu-id="875b2-112">したがって、正しい **アカウント ID** を特定するために、**顧客アカウント** コントロールのルックアップを開き、**アカウント名** 列をフィルタリングするなど、**アカウント ID** がユーザーに知られていない場合、ユーザーは何らかのタイプの検索ステップを実行することを余儀なくされます (次の画像を参照)。</span><span class="sxs-lookup"><span data-stu-id="875b2-112">Therefore, if the **Account ID** was unknown to the user, the user would be forced to perform some type of searching step, such as opening the **Customer account** control’s lookup and filtering on the **Account Name** column to identify the correct **Account ID** (see the image below).</span></span> 

<span data-ttu-id="875b2-113">[![正しいアカウント ID を識別するためのアカウント名でのフィルタリングの例](./media/howtocontextuallookups-3.png)](./media/howtocontextuallookups-3.png)</span><span class="sxs-lookup"><span data-stu-id="875b2-113">[![Example of filtering on Account name to identify correct Account ID](./media/howtocontextuallookups-3.png)](./media/howtocontextuallookups-3.png)</span></span> 

<span data-ttu-id="875b2-114">このユーザー エクスペリエンスは最適ではないため、データ入力の効率性と生産性によって対処されています。</span><span class="sxs-lookup"><span data-stu-id="875b2-114">This user experience is not optimal and is being addressed by data entry efficiency and productivity.</span></span> <span data-ttu-id="875b2-115">このプラットフォームは、コンテキスト データ入力の初期サポートを追加します。コンテキスト データ入力では、システムは、ユーザーが入力したデータがキー フィールドであるか、あるいはその他のより記述的またはよく分かっているフィールドであるかという状況を理解し、それを適切に処理することを自動的に試みます。</span><span class="sxs-lookup"><span data-stu-id="875b2-115">The platform adds initial support for contextual data entry, where the system automatically attempts to understand whether the user’s entered data is in the context of the key field or some other more descriptive or well-understood field, and handle it appropriately.</span></span> <span data-ttu-id="875b2-116">**このドキュメントの残りの部分では、これらのタイプのフィールドをそれぞれ ID (統合) フィールドと NAME (内容を示す) フィールドと総称して参照します。**</span><span class="sxs-lookup"><span data-stu-id="875b2-116">**For the remainder of this document, we’ll generically refer to these types of fields as ID (synthetic) and NAME (descriptive) fields, respectively.**</span></span>

## <a name="contextual-lookup-forms"></a><span data-ttu-id="875b2-117">コンテキストのルックアップ フォーム</span><span class="sxs-lookup"><span data-stu-id="875b2-117">Contextual lookup forms</span></span>
<span data-ttu-id="875b2-118">キーボード データの入力と同じように、システム生成のすべてのルックアップ フォームでもコンテキストを持つようになり、ユーザーが入力したデータのコンテキストでフィルター処理および並べ替えが発生します。</span><span class="sxs-lookup"><span data-stu-id="875b2-118">Just like keyboard data entry, all system-generated lookup forms are also now contextual, meaning that filtering and sorting occur in the context of the data the user has entered.</span></span> <span data-ttu-id="875b2-119">販売注文シナリオの作成を例として使用すると、ID が入力された場合、ユーザーには次のようにルックアップが表示されます。</span><span class="sxs-lookup"><span data-stu-id="875b2-119">Using the create a Sales Order scenario as an example, the user will see the lookup shown below if an ID is entered.</span></span> 

<span data-ttu-id="875b2-120">[![ID のコンテキストで開かれた顧客アカウントの検索フォーム](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)</span><span class="sxs-lookup"><span data-stu-id="875b2-120">[![Customer account lookup form opened in the context of ID](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)</span></span> 

<span data-ttu-id="875b2-121">NAME が入力された場合は、次のルックアップが表示されます。</span><span class="sxs-lookup"><span data-stu-id="875b2-121">If a NAME is entered, then the user will see the following lookup.</span></span> <span data-ttu-id="875b2-122">ユーザーのデータが名前のコンテキストにあるときに、グリッドで最初に名前の列が移動する方法と、ルックアップの並べ替えおよびフィルターの方法を確認します。</span><span class="sxs-lookup"><span data-stu-id="875b2-122">Notice how the NAME column is moved first in the Grid, and how the lookup is sorted and filtered upon when the user’s data is in the context of NAME.</span></span> 

![顧客 ID のルックアップ フォームを名前のコンテキストで開く](./media/howtocontextuallookups-2.png)

## <a name="contextual-data-entry-implementation-details"></a><span data-ttu-id="875b2-124">コンテキスト データ入力の実装の詳細</span><span class="sxs-lookup"><span data-stu-id="875b2-124">Contextual data entry implementation details</span></span>
### <a name="behavior"></a><span data-ttu-id="875b2-125">動作</span><span class="sxs-lookup"><span data-stu-id="875b2-125">Behavior</span></span>

<span data-ttu-id="875b2-126">上記の販売注文の作成シナリオのコンテキストでは、コンテキストでのデータ入力機能により、ユーザーは手間のかかる検索プロセスを実行せずに ID または名前を自由に入力できます。</span><span class="sxs-lookup"><span data-stu-id="875b2-126">In the context of the Sales order create scenario mentioned above, the contextual data entry feature will allow the user to be able to freely type in either the ID or NAME without performing any laborious search process.</span></span> <span data-ttu-id="875b2-127">詳細には、次のような挙動が発生します。</span><span class="sxs-lookup"><span data-stu-id="875b2-127">In detail, the following behaviors will occur:</span></span>

1.  <span data-ttu-id="875b2-128">完全な ID の参照を入力すると、値が直接適用されます。</span><span class="sxs-lookup"><span data-stu-id="875b2-128">If the user enters a complete ID reference, the value will be taken directly.</span></span>
2.  <span data-ttu-id="875b2-129">ユーザーが完全且つ固有の名前の参照を入力すると、値は ID に自動的に変換され、処理されます。</span><span class="sxs-lookup"><span data-stu-id="875b2-129">If the user enters a complete and unique NAME reference, the value will be automatically translated into an ID and then processed.</span></span>
3.  <span data-ttu-id="875b2-130">ユーザーが完全でない ID または NAME 参照を入力した場合 (次のように *Micro* の代わりに *Microsoft*)、BEGINS WITH 述部を介して ID または NAME のいずれかと一意に一致する場合、その値は完全 ID に変換されて処理されます。</span><span class="sxs-lookup"><span data-stu-id="875b2-130">If the user enters a non-complete ID or NAME reference (such as *Micro* instead of *Microsoft*), but it still uniquely matches either ID or NAME via a BEGINS WITH predicate, then the value will be translated into its complete ID and then processed.</span></span>
4.  <span data-ttu-id="875b2-131">ユーザーが完全でない ID または一意ではない NAME を入力し、複数の一致がある場合、*一義化* ルックアップがユーザーに提示され、実際にどの値が意図されたかを選択します。</span><span class="sxs-lookup"><span data-stu-id="875b2-131">If the user enters a non-complete ID or a non-unique NAME and there are multiple matches, then a *disambiguation* lookup will be presented to the user to select which value was actually intended.</span></span>

<span data-ttu-id="875b2-132">コンテキスト データ入力の詳細な使用シナリオについては、付録 A を参照してください。</span><span class="sxs-lookup"><span data-stu-id="875b2-132">See Appendix A for more detailed sample scenarios of contextual data entry.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="875b2-133">前提条件</span><span class="sxs-lookup"><span data-stu-id="875b2-133">Prerequisites</span></span>

<span data-ttu-id="875b2-134">機能の正確性と適切なパフォーマンスを管理するために、前のセクションで説明した動作の適用に以下の制約が追加されました。</span><span class="sxs-lookup"><span data-stu-id="875b2-134">To maintain functional correctness and reasonable performance, the following constraints were added to the application of the behaviors described in the previous section:</span></span>

1. <span data-ttu-id="875b2-135">**タイトル フィールド 2** が名前フィールドです\*\*。</span><span class="sxs-lookup"><span data-stu-id="875b2-135">**Title Field 2** is the NAME field\*\*.</span></span>
2. <span data-ttu-id="875b2-136">NAME フィールドは、インデックスでカバーされているか***または** Cache Lookup* プロパティが *EntireTable* に設定されているテーブルに属している必要があります。</span><span class="sxs-lookup"><span data-stu-id="875b2-136">The NAME field must either be covered by an index ***OR** _ belong to a Table whose _Cache Lookup* property is set to *EntireTable*.</span></span> <span data-ttu-id="875b2-137">すべてのコンテキスト ルックアップ動作がパフォーマンス上の理由でこの要件に満たされていない場合は無効になります。</span><span class="sxs-lookup"><span data-stu-id="875b2-137">All contextual lookup behavior will be disabled if this requirement is not met for performance reasons.</span></span> <span data-ttu-id="875b2-138">**注: インデックスの保守コストのために、NON TRANSACTIONAL テーブルに対してのみインデックスを追加する必要があります。**</span><span class="sxs-lookup"><span data-stu-id="875b2-138">**NOTE: An index should only be added for NON TRANSACTIONAL tables because of index maintenance costs**.</span></span> <span data-ttu-id="875b2-139">また **このインデックスを一意ではないとマークする可能性が高い** (重複を許可 = はい) に注意してください。</span><span class="sxs-lookup"><span data-stu-id="875b2-139">Also note that you will **likely want to mark this index as non-unique** (Allow Duplicates = Yes).</span></span>
3. <span data-ttu-id="875b2-140">コントロールでカスタム検索フォーム (EDT 上の SysTableLookup; FormHelp など) が使用されている場合、前述の曖昧さ回避の動作は既定でオンになりません。</span><span class="sxs-lookup"><span data-stu-id="875b2-140">If a control is using a custom lookup form (such as SysTableLookup; FormHelp on an EDT) then the disambiguation behavior described previously will not be turned on by default.</span></span> <span data-ttu-id="875b2-141">これは、これらのカスタム ルックアップ フォーム (および周囲の修正メソッドやルックアップ メソッドのオーバーライドさえも) は、コンテキストのルックアップのコンテキストでは望ましくないダイアログを提示するなどの高度な処理を行うことができるためです。</span><span class="sxs-lookup"><span data-stu-id="875b2-141">This is because these custom lookup forms (and even surrounding modified and lookup method overrides) can and will do advanced things such as presenting a dialog, which are not desirable in the context of contextual lookups.</span></span>

<span data-ttu-id="875b2-142">カスタム ルックアップ フォームの処理には追加の情報が必要で、独自のセクションで対象となります。</span><span class="sxs-lookup"><span data-stu-id="875b2-142">Handling custom lookup forms requires additional knowledge and will be covered in its own section.</span></span>

### <a name="programming-model-additions"></a><span data-ttu-id="875b2-143">プログラミング モデルの追加</span><span class="sxs-lookup"><span data-stu-id="875b2-143">Programming model additions</span></span>

<span data-ttu-id="875b2-144">*一覧 1* および *一覧 2* に表される動作およびルールは、*FormControlAmbiguousReferenceResolver* と呼ばれる新しい X++ クラスに主に含まれています。</span><span class="sxs-lookup"><span data-stu-id="875b2-144">The behaviors and rules expressed in *Listings 1* and *2* are contained primarily by a new X++ class called *FormControlAmbiguousReferenceResolver*.</span></span> <span data-ttu-id="875b2-145">*FormControlAmbiguousReferenceResolver* より高度なシナリオでは、アプリケーション コードの取得が必要になります。</span><span class="sxs-lookup"><span data-stu-id="875b2-145">*FormControlAmbiguousReferenceResolver* uptake in application code will be necessary in more advanced scenarios.</span></span> <span data-ttu-id="875b2-146">その使用についてはドキュメントの後半で説明します。</span><span class="sxs-lookup"><span data-stu-id="875b2-146">Its use will be described later in the document.</span></span> <span data-ttu-id="875b2-147">*FormControlAmbiguousReferenceResolver* クラスに加えて、*resolveAmbiguousReference* と呼ばれる新しいコントロールのオーバーライドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="875b2-147">In addition to the *FormControlAmbiguousReferenceResolver* class, a new control override called *resolveAmbiguousReference* has been added.</span></span> <span data-ttu-id="875b2-148">R *esolveAmbiguousReference* は、システムで発生している値にユーザーが入力した内容を変換するために、システムでフック ポイントとして機能します。</span><span class="sxs-lookup"><span data-stu-id="875b2-148">R *esolveAmbiguousReference* acts as a hook point in the system for translating what the user typed into a value that the system is expecting.</span></span> <span data-ttu-id="875b2-149">基本的なフローは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="875b2-149">The basic flow is as follows:</span></span>

1.  <span data-ttu-id="875b2-150">ユーザーがコントロールに値を入力し、フォーカスを削除します。</span><span class="sxs-lookup"><span data-stu-id="875b2-150">The user enters a value into a control and removes focus.</span></span>
2.  <span data-ttu-id="875b2-151">インタラクションはクライアントからサーバーへ送信され、新しい値が入力されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="875b2-151">An interaction is sent from the client to the server, indicating that a new value has been entered.</span></span> <span data-ttu-id="875b2-152">適切なコマンドがサーバーで実行されます。</span><span class="sxs-lookup"><span data-stu-id="875b2-152">The appropriate command is executed on the server.</span></span>
3.  <span data-ttu-id="875b2-153">コマンドがユーザーによって入力された値をプロセスしようとする前に、*resolveAmbiguousReference* を呼び出して、システムが値を予想されるドメインに変換できるようにします。</span><span class="sxs-lookup"><span data-stu-id="875b2-153">Before the command attempts to process the value entered by the user, it makes a call to *resolveAmbiguousReference* to give the system a chance to translate the value into the expected domain.</span></span>
4.  <span data-ttu-id="875b2-154">resolveAmbiguousReference のスーパー実装は、上記のルールを実行する *FormControlAmbiguousReferenceResolver* インスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="875b2-154">The super implementation of resolveAmbiguousReference creates an instance of *FormControlAmbiguousReferenceResolver* which executes the rules described above.</span></span>

<span data-ttu-id="875b2-155">*resolveAmbiguousReference* から返される値は、コマンドの実行の残りの部分に使用します。</span><span class="sxs-lookup"><span data-stu-id="875b2-155">The value returned from *resolveAmbiguousReference* is used for the remainder of the command’s execution.</span></span> <span data-ttu-id="875b2-156">Validate() および modified() は、返された値に対して機能します。</span><span class="sxs-lookup"><span data-stu-id="875b2-156">Validate() and modified() operate against the returned value.</span></span>

## <a name="standard-lookup-uptake"></a><span data-ttu-id="875b2-157">標準参照の取得</span><span class="sxs-lookup"><span data-stu-id="875b2-157">Standard lookup uptake</span></span>
### <a name="add-an-index-that-covers-titlefield2"></a><span data-ttu-id="875b2-158">TitleField2 の対象となるインデックスの追加</span><span class="sxs-lookup"><span data-stu-id="875b2-158">Add an index that covers TitleField2</span></span>

<span data-ttu-id="875b2-159">*TitleField2* 名前のデフォルト定義を定義します。</span><span class="sxs-lookup"><span data-stu-id="875b2-159">*TitleField2* defines the default definition of NAME.</span></span> <span data-ttu-id="875b2-160">ID と名前のコンテキストのデータ入力を有効にするために、*TitleField2* をインデックスするか、*EntireTable* に対して *CacheLookup* を設定したテーブルに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="875b2-160">In order to enable ID and NAME contextual data entry, *TitleField2* must be either indexed OR belong to a table with *CacheLookup* set to *EntireTable*.</span></span> <span data-ttu-id="875b2-161">*TitleField2* を含むテーブルで *TitleField2* **をカバーするインデックスを定義しない場合、重要な事は、テーブルに大量の CUD (作成/更新/削除\*)** がないため、*TitleField2* をカバーする **一意ではない** インデックス (重複を許可する = はい) を追加します。</span><span class="sxs-lookup"><span data-stu-id="875b2-161">If the table containing *TitleField2* does not yet define an index covering *TitleField2* **and, importantly, the table does not have a high volume of CUD (Creates/Updates/Deletes\*)**, then add a **non-unique** index (Allow Duplicates = Yes) covering *TitleField2*.</span></span> <span data-ttu-id="875b2-162">これにより、前提条件のセクションで説明したカスタム ルックアップの制限を除いて、システムはコンテキスト データ入力動作の実行を開始します。</span><span class="sxs-lookup"><span data-stu-id="875b2-162">This will cause the system to start executing the contextual data entry behavior, except for the custom lookup limitation described in the Prerequisites section.</span></span> <span data-ttu-id="875b2-163">\*大量のトランザクション テーブルにインデックスを追加すると、インデックス保守コストのために顕著なパフォーマンス ペナルティが発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="875b2-163">\*Adding an index on high-volume transactional tables may incur a noticeable performance penalty due to index maintenance costs.</span></span>

### <a name="enable-disambiguation-behavior-for-custom-lookup-scenarios"></a><span data-ttu-id="875b2-164">カスタム ルックアップ シナリオの曖昧性解消動作の有効化</span><span class="sxs-lookup"><span data-stu-id="875b2-164">Enable disambiguation behavior for custom lookup scenarios</span></span>

<span data-ttu-id="875b2-165">カスタム ルックアップの実装では、ダイアログの提示など、高度な動作や非典型的な動作を提供できます。</span><span class="sxs-lookup"><span data-stu-id="875b2-165">Custom lookup implementations can provide advanced or non-typical behaviors, such as presenting dialogs.</span></span> <span data-ttu-id="875b2-166">したがって、カスタム ルックアップ シナリオが検出されると、システムは既定の曖昧さ回避動作を無効にします。</span><span class="sxs-lookup"><span data-stu-id="875b2-166">Therefore, the system disables the default disambiguation behavior when a custom lookup scenario is detected.</span></span> <span data-ttu-id="875b2-167">既定の曖昧性解消動作を有効にするには、**ルックアップをホストするコントロール** で *resolveAmbiguousReference* メソッド (下記参照) をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="875b2-167">To opt into the default disambiguation behavior, override the *resolveAmbiguousReference* method (as shown below) **on the control hosting the lookup**.</span></span> <span data-ttu-id="875b2-168">*resolveAmbiguousReferenceForControl* の呼び出しに対する 2 つ目のパラメーターは、カスタム ルックアップ シナリオについて曖昧性解消を実行しないという既定の動作をオーバーライドするものであることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="875b2-168">Note that the second parameter to the *resolveAmbiguousReferenceForControl* call is what overrides the default behavior of not performing disambiguation for custom lookup scenarios.</span></span>

```xpp
public str resolveAmbiguousReference()
{
    FormControlAmbiguousReferenceResolver::resolveAmbiguousReferenceForControl (this, true);
}
```

### <a name="make-custom-lookup-forms-contextual"></a><span data-ttu-id="875b2-169">カスタム ルックアップ フォームをコンテキストにする</span><span class="sxs-lookup"><span data-stu-id="875b2-169">Make custom lookup forms contextual</span></span>

<span data-ttu-id="875b2-170">先に述べたように、システム生成のルックアップ フォームはすべて、ホスト コントロールに入力されたデータのコンテキストを自動的に考慮します。</span><span class="sxs-lookup"><span data-stu-id="875b2-170">As mentioned earlier, all system-generated lookup forms automatically consider the context of the data entered into their host control.</span></span> <span data-ttu-id="875b2-171">これには、*SysTableLookup* によって生成されるほとんどのルックアップ フォームが含まれます。</span><span class="sxs-lookup"><span data-stu-id="875b2-171">This includes most lookup forms generated via *SysTableLookup*.</span></span> <span data-ttu-id="875b2-172">モデル化されたカスタム ルックアップ フォームは、その性質によってシステムで完全に処理することはできず、コンテキストのルックアップ フォームの動作およびビジュアルと一致するように変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="875b2-172">Modeled custom lookup forms, by their nature, cannot be fully-handled by the system and must be modified to match the behavior and visuals of contextual lookups forms.</span></span>

1.  <span data-ttu-id="875b2-173">ホスト コントロールに含まれるデータが ID のコンテキスト内にある場合:</span><span class="sxs-lookup"><span data-stu-id="875b2-173">If the data contained by the host control is in the context of ID, then:</span></span>
    1.  <span data-ttu-id="875b2-174">グリッドにまず ID 列を作成します。</span><span class="sxs-lookup"><span data-stu-id="875b2-174">Make the ID column first in the Grid.</span></span>
    2.  <span data-ttu-id="875b2-175">ID により並べ替えてフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="875b2-175">Sort and filter by ID.</span></span>

2.  <span data-ttu-id="875b2-176">ホスト コントロールに含まれるデータが NAME のコンテキスト内にある場合:</span><span class="sxs-lookup"><span data-stu-id="875b2-176">If the data contained by the host control is in the context of NAME, then:</span></span>
    1.  <span data-ttu-id="875b2-177">グリッドにまず名前列を作成します。</span><span class="sxs-lookup"><span data-stu-id="875b2-177">Make the NAME column first in the Grid,</span></span>
    2.  <span data-ttu-id="875b2-178">NAME により並べ替えてフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="875b2-178">Sort and filter by NAME,</span></span>

<span data-ttu-id="875b2-179">次のシナリオでは、カスタム ルックアップと、これらの場合のコンテキストでのデータ入力を有効にする方法の推奨事項を示しています。</span><span class="sxs-lookup"><span data-stu-id="875b2-179">The following scenarios illustrate some custom lookups, along with the recommendation for how to enable contextual data entry in these cases.</span></span>

#### <a name="scenario-1-custom-lookup-defined-via-the-formhelp-property-on-an-edt"></a><span data-ttu-id="875b2-180">シナリオ 1: EDT で FormHelp プロパティ経由で定義されたユーザー設定のルックアップ</span><span class="sxs-lookup"><span data-stu-id="875b2-180">Scenario 1: Custom lookup defined via the FormHelp property on an EDT</span></span>

<span data-ttu-id="875b2-181">FormHelp で定義されたカスタム ルックアップ (モデル化されていても) は、通常のカーネル ベースのルックアップ生成ルーティンをそのまま使います。</span><span class="sxs-lookup"><span data-stu-id="875b2-181">Custom lookups defined via FormHelp (even though modeled) still go through normal kernel-based lookup generation routines.</span></span> <span data-ttu-id="875b2-182">したがって、カーネルには引き続きルックアップ フォームを変更するためのフックがあります。</span><span class="sxs-lookup"><span data-stu-id="875b2-182">Therefore, the kernel still has hooks to make some changes to the lookup form.</span></span> <span data-ttu-id="875b2-183">具体的には、ルックアップ システムに、正しいフィルターおよび並べ替えを適用するための十分な情報があります。ただし、ルックアップのグリッドで移動すべきコントロールは既知ではありません。</span><span class="sxs-lookup"><span data-stu-id="875b2-183">Specifically, the lookup system has enough information to apply the correct filters and sorts; however, it is NOT known which controls should be moved in the lookup's grid.</span></span>  <span data-ttu-id="875b2-184">(バインディングに基づいて推測することは可能ですが、その推測はより高度なルックアップ フォーム デザインでは不正確である可能性があります)。カスタム ルックアップ フォームが `SysTableLookup::filterLookupPreRun` メソッドおよび `SysTableLookup::filterLookupPostRun` メソッドを利用している場合、`filterLookupPostRun` で (新しい) オプション パラメーターを取得して、名前コントロールを次のように自動的に移動させます。</span><span class="sxs-lookup"><span data-stu-id="875b2-184">(While an educated guess could be made based on bindings, that guess may be incorrect in more advanced lookup form designs.) If your custom lookup form is leveraging the `SysTableLookup::filterLookupPreRun` and `SysTableLookup::filterLookupPostRun` methods, then uptake the (new) optional parameters on `filterLookupPostRun` to have the NAME control moved automatically, as shown.</span></span>

```xpp
public class MyCustomLookupForm extends FormRun
{
    public void run()
    {
        FormStringControl lookupHostControl = SysTableLookup::getCallerStringControl(this.args());
        boolean isFiltered = SysTableLookup::filterLookupPreRun(lookupHostControl, ID_Control, FormDataSourceToFilter);

        super();

        SysTableLookup::filterLookupPostRun(isFiltered, lookupHostControl.text(), ID_Control, FormDataSourceToFilter, 
            new FormControlAmbiguousReferenceResolver(callingControl), NAME_Control);
    }
}
```

<span data-ttu-id="875b2-185">ルックアップ フォームが *SysTableLookup::filterLookup\** メソッドを使用しておらず、それらのメソッドを取得しない場合、以下のように、単にコントロール移動を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="875b2-185">If your lookup form isn’t using the *SysTableLookup::filterLookup\** methods, and you don’t want to uptake those methods, then you can simply add a control move as shown below.</span></span>

```xpp
public class MyCustomLookupForm extends FormRun
{
    public void init()
    {
        super();
        this.applyControlOrdering();
    }

    private void applyControlOrdering()
    {
        FormControl callerControl = SysTableLookup::getCallerControl(this.args());
        if (FormControlAmbiguousReferenceResolver::isControlValueMappedToAlternativeField(callerControl))
        {
            Grid.moveControl(ID_Control.id(), NAME_control.id());
        }
        else
        {
            Grid.moveControl(NAME_Control.id(), ID_Control.id());
        }
    }
}
```

#### <a name="scenario-2-override-of-lookup-method-manually-launching-a-form"></a><span data-ttu-id="875b2-186">シナリオ 2: フォームを手動で起動するルックアップ メソッドの上書き</span><span class="sxs-lookup"><span data-stu-id="875b2-186">Scenario 2: Override of lookup method manually launching a form</span></span>

<span data-ttu-id="875b2-187">シナリオ 1 とは異なり、クラス ファクトリなどの完全な手動メカニズムによって起動されるルックアップ フォームにはカーネル フックはありません。</span><span class="sxs-lookup"><span data-stu-id="875b2-187">Unlike Scenario 1, lookup forms launched by completely manual mechanisms, such as the class factory, have no kernel hooks.</span></span> <span data-ttu-id="875b2-188">したがって、コンテキスト データ入力動作を遵守するのはルックアップ フォームの責任です。</span><span class="sxs-lookup"><span data-stu-id="875b2-188">Therefore, it is the responsibility of the lookup form to adhere to the contextual data entry behaviors.</span></span> <span data-ttu-id="875b2-189">これを行う最も簡単な方法は、並べ替えを維持する必要があることを示す 1 つの追加パラメーターを含めることを除いて、(シナリオ 1 と同様の) SysTableLookup::filterLookup\* メソッドを活用することです。</span><span class="sxs-lookup"><span data-stu-id="875b2-189">The easiest way to do this is to leverage the SysTableLookup::filterLookup\* methods (similar to Scenario 1) except include one additional parameter to indicate that sorting should also be maintained.</span></span> <span data-ttu-id="875b2-190">例として以下に表示します。</span><span class="sxs-lookup"><span data-stu-id="875b2-190">An example is shown below.</span></span>

```xpp
public class MyCustomLookupForm extends FormRun
{
    public void run()
    {
        FormStringControl lookupHostControl = SysTableLookup::getCallerStringControl(this.args());
        boolean isFiltered = SysTableLookup::filterLookupPreRun(lookupHostControl, ID_Control, FormDataSourceToFilter);

        super();

        SysTableLookup::filterLookupPostRun(isFiltered, lookupHostControl.text(), ID_Control, FormDataSourceToFilter, 
            new FormControlAmbiguousReferenceResolver(callingControl), NAME_Control, true);
    }
}
```

## <a name="advanced-lookup-uptake"></a><span data-ttu-id="875b2-191">高度なルックアップの取得</span><span class="sxs-lookup"><span data-stu-id="875b2-191">Advanced lookup uptake</span></span>
### <a name="scenario-1-overriding-id-and-name-bindings"></a><span data-ttu-id="875b2-192">シナリオ 1: ID と NAME バインドの上書き</span><span class="sxs-lookup"><span data-stu-id="875b2-192">Scenario 1: Overriding ID and NAME bindings</span></span>

<span data-ttu-id="875b2-193">既定で選択されている以外のフィールドのセットを使用する場合は、*FormControlAmbiguousReferenceResolver* のインスタンスを手動で構築し、カスタム バインドを表すオプションのパラメーターを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="875b2-193">If you want to use a set of fields other than what is chosen by default, you must manually construct an instance of *FormControlAmbiguousReferenceResolver* and provide the optional parameters representing the custom bindings.</span></span> <span data-ttu-id="875b2-194">この特別なインスタンスは、*resolveAmbiguousReference* のオーバーライドおよびカスタム ルックアップ フォーム (*FormControlAmbiguousReferenceResolver* のインスタンスも受け入れる *SysTableLookup* など) で使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="875b2-194">This specialized instance must be used in an override of *resolveAmbiguousReference* and in a custom lookup form (including *SysTableLookup*, which also accepts an instance of *FormControlAmbiguousReferenceResolver*).</span></span> <span data-ttu-id="875b2-195">カスタム バインディングは、現在カーネルによって生成されるルックアップで指定できません。</span><span class="sxs-lookup"><span data-stu-id="875b2-195">A custom binding cannot currently be specified in kernel-generated lookups.</span></span> <span data-ttu-id="875b2-196">現在カスタムの ID と名前のバインディングを受け入れているメソッド:</span><span class="sxs-lookup"><span data-stu-id="875b2-196">Methods currently accepting custom ID and NAME bindings:</span></span>

1.  <span data-ttu-id="875b2-197">FormControlAmbiguousReferenceResolver</span><span class="sxs-lookup"><span data-stu-id="875b2-197">FormControlAmbiguousReferenceResolver</span></span>
    -   <span data-ttu-id="875b2-198">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="875b2-198">Constructor</span></span>
    -   <span data-ttu-id="875b2-199">resolveAmbiguousReferenceForControl</span><span class="sxs-lookup"><span data-stu-id="875b2-199">resolveAmbiguousReferenceForControl</span></span>
    -   <span data-ttu-id="875b2-200">surrogateFKHelperForAlternativeFieldMapping</span><span class="sxs-lookup"><span data-stu-id="875b2-200">surrogateFKHelperForAlternativeFieldMapping</span></span>
    -   <span data-ttu-id="875b2-201">isControlValueMappedToAlternativeField</span><span class="sxs-lookup"><span data-stu-id="875b2-201">isControlValueMappedToAlternativeField</span></span>

<span data-ttu-id="875b2-202">カスタム バインドを提供する方法のエンド ツー エンドの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="875b2-202">Here's an end-to-end example of how to provide custom bindings.</span></span>

```xpp
[Control Hosting Lookup]
public str resolveAmbiguousReference()
{
    return FormControlAmbiguousReferenceResolver::resolveAmbiguousReferenceForControl(
        this, true, AbsoluteFieldBinding::construct(IDField, Table), 
        AbsoluteFieldBinding::construct(SomeOtherNAMEField, Table));
}

[Custom Lookup Form]
public class MyCustomLookupForm extends FormRun
{
    public void run()
    {
        FormStringControl lookupHostControl = SysTableLookup::getCallerStringControl(this.args());
        boolean isFiltered = SysTableLookup::filterLookupPreRun(lookupHostControl, ID_Control, FormDataSourceToFilter);

        super();

        SysTableLookup::filterLookupPostRun(isFiltered, lookupHostControl.text(), ID_Control, FormDataSourceToFilter, 
            new FormControlAmbiguousReferenceResolver(callingControl, AbsoluteFieldBinding::construct(IDField, Table),
            AbsoluteFieldBinding::construct(SomeOtherNAMEField, Table)), NAME_Control, true);
    }
}
```

### <a name="scenario-2-custom-resolution-logic"></a><span data-ttu-id="875b2-203">シナリオ 2: カスタム解像度ロジック</span><span class="sxs-lookup"><span data-stu-id="875b2-203">Scenario 2: Custom resolution logic</span></span>

<span data-ttu-id="875b2-204">resolveAmbiguousReference をオーバーライドし、FormControlAmbiguousReferenceResolver 以外のものを活用することによってカスタム解決ロジックを使用できます。</span><span class="sxs-lookup"><span data-stu-id="875b2-204">It’s possible to use custom resolution logic by overriding resolveAmbiguousReference and leveraging something other than FormControlAmbiguousReferenceResolver.</span></span> <span data-ttu-id="875b2-205">このロジックは、キーボードおよびルックアップ ベースのエントリが常に同期されるように、ホストされているルックアップ フォームと共通にする必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="875b2-205">Note that this logic needs to be common to the hosted lookup form so that keyboard and lookup-based entry stay in sync.</span></span>

```xpp
public str resolveAmbiguousReference()
{
    // In this sample, allow “looser” data entry by simply picking the first record that matches, if any.
    CLI_Job _job;
    str mappedValue = this.text();
    if (strLen(mappedValue) > 0)
    {
        select firstonly _job order by _job.Title where _job.Title like mappedValue + “*”;
    }

    if (_job.RecId)
    {
        mappedValue = _job.Title;
    }

    return mappedValue;
}
```

## <a name="appendix--detailed-usage-scenarios-for-contextual-data-entry"></a><span data-ttu-id="875b2-206">付録コンテキスト データ入力の詳細な使用シナリオ</span><span class="sxs-lookup"><span data-stu-id="875b2-206">Appendix  Detailed usage scenarios for contextual data entry</span></span>
<span data-ttu-id="875b2-207">シナリオでは、PK フィールド「ID」およびインデックス フィールド「名」を持つ「TableA」と呼ばれるテーブルがあり、FK で ID (ユーザーは最終的には ID をピックする必要がある) に関連するものを入力しようとしていると仮定します。</span><span class="sxs-lookup"><span data-stu-id="875b2-207">For the scenarios, assume there is a table called "TableA" with PK field "ID" and index field "Name", with the FK we're trying to enter that is related to the ID (the user ultimately needs to pick an ID).</span></span> <span data-ttu-id="875b2-208">類似または始まる値に依存するアルゴリズムは、文字列フィールドを想定していることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="875b2-208">Note that any algorithms that depend on like/begins with are assuming string fields.</span></span> <span data-ttu-id="875b2-209">たとえば、整数型では、高品質の解決の動作を提供することはできません。</span><span class="sxs-lookup"><span data-stu-id="875b2-209">We won't be able to provide high fidelity resolution behavior on, for example, integral types.</span></span> 

<span data-ttu-id="875b2-210">**シナリオ 1: ユーザーが 有効な ID 「1234」を入力する** resolveReference の super() 実装は、適切な述部で TableA.ID を最初に照会します。</span><span class="sxs-lookup"><span data-stu-id="875b2-210">**Scenario 1: User enters a valid ID of "1234"** The super() implementation of resolveReference first queries against TableA.ID with the appropriate predicate.</span></span> <span data-ttu-id="875b2-211">クエリは単一のレコードを検索し、ユーザーの入力値を返して、検証および変更によって追加の処理に進みます。</span><span class="sxs-lookup"><span data-stu-id="875b2-211">The query finds a single record, and returns the user's entered value to be further processed by validate and modified.</span></span> <span data-ttu-id="875b2-212">検証が成功すると、UI に「1234」と表示されます。</span><span class="sxs-lookup"><span data-stu-id="875b2-212">Validation passes and the user sees "1234" in the UI.</span></span> 

<span data-ttu-id="875b2-213">**シナリオ 2: ユーザーが 無効な ID 「4321」を入力します** resolveReference の super() 実装が TableA.ID に対する最初のクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="875b2-213">**Scenario 2: User enters an invalid ID of "4321"** The super() implementation of resolveReference first queries against TableA.ID.</span></span> <span data-ttu-id="875b2-214">クエリはレコードを検索しないため、2 番目のクエリは Name フィールドに対して実行されます (SELECT TOP 2 FROM TableA WHERE TableA.Name LIKE "4321％")。</span><span class="sxs-lookup"><span data-stu-id="875b2-214">The query does not find any records, so a second query is performed against the Name field (SELECT TOP 2 FROM TableA WHERE TableA.Name LIKE "4321%").</span></span> <span data-ttu-id="875b2-215">それでもレコードが見つからないため、検証を通じて「4321」が渡されますが、失敗します。</span><span class="sxs-lookup"><span data-stu-id="875b2-215">Still, no record is found, so "4321" is passed through to validation, which fails.</span></span> <span data-ttu-id="875b2-216">ユーザーはブラウザーで「4321」と表示され、検証エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="875b2-216">The user sees "4321" in the browser as well as a validation error.</span></span> 

<span data-ttu-id="875b2-217">**シナリオ 3: ユーザーが「ACME」の有効な名前を入力する** resolveReference の super() 実装が TableA.ID に対する最初のクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="875b2-217">**Scenario 3: User enters a valid Name of "ACME"** The super() implementation of resolveReference first queries against TableA.ID.</span></span> <span data-ttu-id="875b2-218">クエリはレコードを検索しないため、2 番目のクエリは Name フィールドに対して実行されます (SELECT TOP 2 FROM TableA WHERE TableA.Name LIKE "ACME％")。</span><span class="sxs-lookup"><span data-stu-id="875b2-218">The query does not find any records, so a second query is performed against the Name field (SELECT TOP 2 FROM TableA WHERE TableA.Name LIKE "ACME%").</span></span> <span data-ttu-id="875b2-219">このクエリは単一のレコード (一意の参照) を検索するので、ルックアップは対応する TableA.ID を自動的に返します。</span><span class="sxs-lookup"><span data-stu-id="875b2-219">This query does find a single record (unique reference), so the lookup automatically returns the corresponding TableA.ID.</span></span> <span data-ttu-id="875b2-220">その値のコンテキストでの実行を検証および変更継続します。</span><span class="sxs-lookup"><span data-stu-id="875b2-220">Validate and modified continue executing in the context of that value.</span></span> <span data-ttu-id="875b2-221">検証が成功すると、最終的にはブラウザーに ACME の ID 値が表示されます (たとえば、ブラウザーで ACME は 1234 に切り替わります)。</span><span class="sxs-lookup"><span data-stu-id="875b2-221">Validation passes, and ultimately the user sees the ID value for ACME in the browser (for example, ACME would switch to 1234 in the browser).</span></span> 

<span data-ttu-id="875b2-222">**シナリオ 4: ユーザーが「ACNE」の無効な名前を入力する** resolveReference の super() 実装が TableA.ID に対する最初のクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="875b2-222">**Scenario 4: User enters an invalid Name of "ACNE"** The super() implementation of resolveReference first queries against TableA.ID.</span></span> <span data-ttu-id="875b2-223">クエリはレコードを検索しないため、2 番目のクエリは Name フィールドに対して実行されます (SELECT TOP 2 FROM TableA WHERE TableA.Name LIKE "ACNE％")。</span><span class="sxs-lookup"><span data-stu-id="875b2-223">The query does not find any records, so a second query is performed against the Name field (SELECT TOP 2 FROM TableA WHERE TableA.Name LIKE "ACNE%").</span></span> <span data-ttu-id="875b2-224">このクエリではレコードが見つからないため、ルックアップによって ACNE が検証に渡されますが検出できません。</span><span class="sxs-lookup"><span data-stu-id="875b2-224">This query does not find any records, so the lookup passes ACNE through to validation, which fails.</span></span> <span data-ttu-id="875b2-225">ユーザーはブラウザーで「ACNE」と表示され、検証エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="875b2-225">The user sees "ACNE" in the browser as well as a validation error.</span></span> 

<span data-ttu-id="875b2-226">**シナリオ 5: ユーザーが「ACME」のあいまいな名前を入力する** この場合は、データベース内に 2 つのレコードがあると仮定 : 1 つは「ACME W」という名前で、もう 1 つは「ACME E」とします。</span><span class="sxs-lookup"><span data-stu-id="875b2-226">**Scenario 5: User enters an ambiguous Name of "ACME"** In this case, assume there are two records in the database: one with Name "ACME W" and another with "ACME E".</span></span> <span data-ttu-id="875b2-227">TableA.ID に対する resolveReference の最初のクエリの super() 実装。</span><span class="sxs-lookup"><span data-stu-id="875b2-227">The super() implementation of resolveReference first queries against TableA.ID.</span></span> <span data-ttu-id="875b2-228">クエリはレコードを検索しないため、2 番目のクエリは Name フィールドに対して実行されます (SELECT TOP 2 FROM TableA WHERE TableA.Name LIKE "ACME％")。</span><span class="sxs-lookup"><span data-stu-id="875b2-228">The query does not find any records, so a second query is performed against the Name field (SELECT TOP 2 FROM TableA WHERE TableA.Name LIKE "ACME%").</span></span> <span data-ttu-id="875b2-229">このクエリは 2 つのレコードを検出します。それ以上の仮定はできません。</span><span class="sxs-lookup"><span data-stu-id="875b2-229">This query finds two records, so it cannot make any further assumptions.</span></span> <span data-ttu-id="875b2-230">曖昧性解消ルックアップは、"ACME W" と "ACME E" を示すユーザーに選択肢として表示されます。</span><span class="sxs-lookup"><span data-stu-id="875b2-230">A disambiguation lookup is presented to the user showing "ACME W" and "ACME E" as choices.</span></span> <span data-ttu-id="875b2-231">ユーザーは「ACME E」を選択します。</span><span class="sxs-lookup"><span data-stu-id="875b2-231">The user picks "ACME E".</span></span> <span data-ttu-id="875b2-232">resolveReference を選択してから、選択したレコードを取得して "ACME E" の ID にリダイレクトします。</span><span class="sxs-lookup"><span data-stu-id="875b2-232">resolveReference then takes the records selected by the user and redirects it to the ID of "ACME E".</span></span> <span data-ttu-id="875b2-233">"ACME E" の ID コンテキストでの実行を検証および変更継続します。</span><span class="sxs-lookup"><span data-stu-id="875b2-233">Validate and modified continue execution in the context of the ID of "ACME E".</span></span> <span data-ttu-id="875b2-234">ブラウザーは最終的に "ACME E" の ID を表示します (たとえば、1234)。</span><span class="sxs-lookup"><span data-stu-id="875b2-234">The browser ultimately displays the ID of "ACME E" (for example, 1234).</span></span> 

<span data-ttu-id="875b2-235">**シナリオ 6: ユーザーが「ACME」のあいまいな名前を入力し、非不明瞭ルックアップで選択しないこと** この場合は、データベース内に 2 つのレコードがあると仮定 : 1 つは「ACME W」という名前で、もう 1 つは「ACME E」とします。</span><span class="sxs-lookup"><span data-stu-id="875b2-235">**Scenario 6: User enters an ambiguous Name of "ACME" and doesn't make a choice in the disambiguation lookup** In this case, assume there are two records in the database: one with Name "ACME W" and another with "ACME E".</span></span> <span data-ttu-id="875b2-236">TableA.ID に対する resolveReference の最初のクエリの super() 実装。</span><span class="sxs-lookup"><span data-stu-id="875b2-236">The super() implementation of resolveReference first queries against TableA.ID.</span></span> <span data-ttu-id="875b2-237">クエリはレコードを検索しないため、2 番目のクエリは Name フィールドに対して実行されます (SELECT TOP 2 FROM TableA WHERE TableA.Name LIKE "ACME％")。</span><span class="sxs-lookup"><span data-stu-id="875b2-237">The query does not find any records, so a second query is performed against the Name field (SELECT TOP 2 FROM TableA WHERE TableA.Name LIKE "ACME%").</span></span> <span data-ttu-id="875b2-238">このクエリは 2 つのレコードを検出します。それ以上の仮定はできません。</span><span class="sxs-lookup"><span data-stu-id="875b2-238">This query finds two records, so it cannot make any further assumptions.</span></span> <span data-ttu-id="875b2-239">曖昧性解消ルックアップは、"ACME W" と "ACME E" を示すユーザーに選択肢として表示されます。</span><span class="sxs-lookup"><span data-stu-id="875b2-239">A disambiguation lookup is presented to the user showing "ACME W" and "ACME E" as choices.</span></span> <span data-ttu-id="875b2-240">ユーザーはルックアップから選択しません。</span><span class="sxs-lookup"><span data-stu-id="875b2-240">The user doesn't make a selection from the lookup.</span></span> <span data-ttu-id="875b2-241">したがって、「ACME」が検証され、変更されます。</span><span class="sxs-lookup"><span data-stu-id="875b2-241">Therefore "ACME" is passed through to validate and modified.</span></span> <span data-ttu-id="875b2-242">検証が失敗し、ユーザーに検証エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="875b2-242">Validation fails and the user is presented with a validation failure message.</span></span> <span data-ttu-id="875b2-243">ブラウザーには "ACME" という値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="875b2-243">The browser still displays a value of "ACME".</span></span> 

<span data-ttu-id="875b2-244">**シナリオ 7: ユーザーはが有効な ID「12」を入力し、ルックアップ フォームを提示します** ルックアップを提示する前に、システムは TableA.ID (「12%」のような TableA の ID からトップ 1 を選ぶ) に対して照会します。</span><span class="sxs-lookup"><span data-stu-id="875b2-244">**Scenario 7: User enters a "valid" ID of "12" and presents the lookup form** Prior to presenting the lookup, the system queries against TableA.ID (SELECT TOP 1 FROM TableA WHERE TableA.ID LIKE '12%').</span></span> <span data-ttu-id="875b2-245">クエリはレコードを検出するため、ユーザーが ID のコンテキストで操作しているものと想定されます。</span><span class="sxs-lookup"><span data-stu-id="875b2-245">The query finds a record and therefore assumes the user must be operating in the context of ID.</span></span> <span data-ttu-id="875b2-246">これは、ID でのルックアップ、フィルターや並べ替えを提供します。</span><span class="sxs-lookup"><span data-stu-id="875b2-246">It presents the lookup, filtering and sorting by ID.</span></span> 

<span data-ttu-id="875b2-247">**シナリオ 8: ユーザーが無効な ID 「4321」を入力し、ルックアップ フォームを提示します** ルックアップを提示する前に、システムは TableA.ID (「4321%」 のような TableA の ID からトップ 1 を選ぶ) に対して照会します。</span><span class="sxs-lookup"><span data-stu-id="875b2-247">**Scenario 8: User enters an invalid ID of "4321" and presents the lookup form** Prior to presenting the lookup, the system queries against TableA.ID (SELECT TOP 1 FROM TableA WHERE TableA.ID LIKE '4321%').</span></span> <span data-ttu-id="875b2-248">クエリで一致するレコードが見つからないため、ユーザーが名前を入力していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="875b2-248">The query does not find a matching record and therefore assumes the user is entering a Name.</span></span> <span data-ttu-id="875b2-249">ルックアップは、フィルタリングされ、名前 (この場合はレコードは表示されません) で並べ替えられて表示されます。</span><span class="sxs-lookup"><span data-stu-id="875b2-249">The lookup is presented as filtered and sorted by Name (no records shown in this case).</span></span> 

<span data-ttu-id="875b2-250">**シナリオ 9: ユーザーが「AC」の「有効な」名前を入力し、ルックアップ フォームを提示します** ルックアップを提示する前に、システムは TableA.ID(「AC%」のような TableA.ID からトップ 1 を選ぶ) に対して照会します。</span><span class="sxs-lookup"><span data-stu-id="875b2-250">**Scenario 9: User enters a "valid" Name of "AC" and presents the lookup form** Prior to presenting the lookup, the system queries against TableA.ID (SELECT TOP 1 FROM TableA WHERE TableA.ID LIKE 'AC%').</span></span> <span data-ttu-id="875b2-251">クエリで一致するレコードが見つからないため、ユーザーが名前を入力していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="875b2-251">The query does not find a matching record and therefore assumes the user is entering a Name.</span></span> <span data-ttu-id="875b2-252">ルックアップは、フィルタリングされたもの (「AC で始まる」に一致するレコード) とアルファベット順の名前で並べ替えられて表示されます。</span><span class="sxs-lookup"><span data-stu-id="875b2-252">The lookup is presented as filtered (those records matching "begins with AC") and sorted by Name in alphabetical order.</span></span> 

<span data-ttu-id="875b2-253">**シナリオ 10: ユーザーが無効な「EM」という名前を入力し、ルックアップ フォームを提示します** ルックアップを提示する前に、システムは TableA.ID (「EM%」のような TableA の ID からトップ 1 を選ぶ)に対して照会します。</span><span class="sxs-lookup"><span data-stu-id="875b2-253">**Scenario 10: User enters an invalid Name of "EM" and presents the lookup form** Prior to presenting the lookup, the system queries against TableA.ID (SELECT TOP 1 FROM TableA WHERE TableA.ID LIKE 'EM%').</span></span> <span data-ttu-id="875b2-254">クエリで一致するレコードが見つからないため、ユーザーが名前を入力していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="875b2-254">The query does not find a matching record and therefore assumes the user is entering a Name.</span></span> <span data-ttu-id="875b2-255">ルックアップは、フィルタリングされ、名前で並べ替えられて表示されます。</span><span class="sxs-lookup"><span data-stu-id="875b2-255">The lookup is presented as filtered and sorted by Name.</span></span> <span data-ttu-id="875b2-256">レコードが見つからないため、空白のルックアップがユーザーを表示されます。</span><span class="sxs-lookup"><span data-stu-id="875b2-256">No records are found and therefore the user is presented with an empty lookup.</span></span>





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]