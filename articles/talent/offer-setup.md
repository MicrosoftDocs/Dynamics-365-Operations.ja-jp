---
title: "オファー管理の設定"
description: "このトピックでは、Talent でのオファーの設定方法について説明します。"
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: fa2f2f9f67562524961352a87a7db49992776e46
ms.contentlocale: ja-jp
ms.lasthandoff: 10/22/2018

---
# <a name="set-up-offer-management"></a><span data-ttu-id="f1532-103">オファー管理の設定</span><span class="sxs-lookup"><span data-stu-id="f1532-103">Set up offer management</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="f1532-104">Dynamics 365 for Talent: Attract で候補者がオファー ステージに進む場合、候補者のオファーを迅速に作成し、必要に応じて承認し、候補者に送付することを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f1532-104">When a candidate is moved to the offer stage in Dynamics 365 for Talent: Attract, you need to ensure that the offers can be quickly created for the candidate, approved as necessary, and sent out to the candidate.</span></span> <span data-ttu-id="f1532-105">ほとんどのオファーが標準なので、再利用可能なテンプレートから作成することができます。</span><span class="sxs-lookup"><span data-stu-id="f1532-105">Because most offers are standard, they can be created from reusable templates.</span></span> <span data-ttu-id="f1532-106">Attract では、すべてのオファーは 1 つまたは複数のオファー ドキュメントのコレクションであるオファー パッケージにロールアップされます</span><span class="sxs-lookup"><span data-stu-id="f1532-106">In Attract, all offers are rolled into an offer package, which is a collection of one or more offer documents.</span></span> 

<span data-ttu-id="f1532-107">このトピックでは、Attract 管理者が Attract のオファー管理機能の一部としてさまざまなオファー パッケージ テンプレートを設定するために必要なすべての手順を示します。</span><span class="sxs-lookup"><span data-stu-id="f1532-107">This topic lists all the steps that an Attract administrator would follow to set up different offer package templates as part of the offer management capability in Attract.</span></span> <span data-ttu-id="f1532-108">管理者以外のユーザーには、これらの機能に対するアクセス許可がありません。</span><span class="sxs-lookup"><span data-stu-id="f1532-108">Users with non-administrator roles will not have access to these capabilities.</span></span>

>[!NOTE]
> <span data-ttu-id="f1532-109">オファー管理機能は、包括採用アドオンの一部として使用できます。</span><span class="sxs-lookup"><span data-stu-id="f1532-109">Offer management capabilities are available as part of the Comprehensive Hiring Add-On.</span></span>

## <a name="offer-data"></a><span data-ttu-id="f1532-110">オファー データ</span><span class="sxs-lookup"><span data-stu-id="f1532-110">Offer data</span></span> 

<span data-ttu-id="f1532-111">オファー データは、オファー パッケージ テンプレート内の最小単位です。</span><span class="sxs-lookup"><span data-stu-id="f1532-111">Offer data is the smallest unit inside the offer package template.</span></span> <span data-ttu-id="f1532-112">標準的なオファーは、標準のテキストと値のセットで構成されます。</span><span class="sxs-lookup"><span data-stu-id="f1532-112">A typical offer consists of standard text and a set of values.</span></span> <span data-ttu-id="f1532-113">値のセットは、オファー間で変更できる唯一の点です。</span><span class="sxs-lookup"><span data-stu-id="f1532-113">The sets of values are the only pieces that could change between offers.</span></span> <span data-ttu-id="f1532-114">オファーの作成時に、オファー作成者が重視する最も重要な側面は、オファーのパッケージ テンプレートにオファー データ プレースホルダーのリストがあることです。</span><span class="sxs-lookup"><span data-stu-id="f1532-114">During the offer creation, the most important aspect that the offer creator can focus on is the list of offer data placeholders present in an offer package template.</span></span> <span data-ttu-id="f1532-115">オファー データを設定するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="f1532-115">To set up offer data, do the following.</span></span>

1.  <span data-ttu-id="f1532-116">**オファー管理**へ移動します。</span><span class="sxs-lookup"><span data-stu-id="f1532-116">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="f1532-117">左のナビゲーション ウィンドウで**ライブラリ** セクションを展開して、**オファー データ**に進みます。</span><span class="sxs-lookup"><span data-stu-id="f1532-117">Expand the **Library** section in the left navigation pane, then go to **Offer data**.</span></span>

    >[!NOTE]
    > <span data-ttu-id="f1532-118">**オファー データ** ページには、**候補者の詳細**および**職務の詳細**セクションがあります。</span><span class="sxs-lookup"><span data-stu-id="f1532-118">On the **Offer data** page are the **Candidate details** and **Job details** sections.</span></span> <span data-ttu-id="f1532-119">Attract はいくつかのオファー データ プレースホルダーをすぐに提供します。</span><span class="sxs-lookup"><span data-stu-id="f1532-119">Attract provides a few offer data placeholders out-of-the-box.</span></span>
    
    > <span data-ttu-id="f1532-120">ページには、さまざまなオファー データ プレースホルダーを論理的なグループにまとめるセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="f1532-120">There are sections on the page to organize different offer data placeholders together in logical groups.</span></span> <span data-ttu-id="f1532-121">これらのセクションは、オファーの作成プロセスでオファー データおよびデータ設定を維持するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="f1532-121">These sections can help with maintenance of offer data and population of data during the offer creation process.</span></span>

1.  <span data-ttu-id="f1532-122">新しいオファー データ セクションを作成するには、**セクションを追加**をクリックし、セクションの一意の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="f1532-122">To create a new offer data section, click **Add a section** and enter a unique name for the section.</span></span>

1.  <span data-ttu-id="f1532-123">任意のセクションにオファー データ プレースホルダーを追加するには、**オファー データを追加**をクリックし、プレースホルダーの一意の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="f1532-123">To add offer data placeholders to any section, click **Add offer data** and enter a unique name for the placeholder.</span></span>

1.  <span data-ttu-id="f1532-124">任意のセクションの名前を編集するには、セクションの名前をポイントし、名前を更新します。</span><span class="sxs-lookup"><span data-stu-id="f1532-124">To edit the name of any section, hover over the section name and update the name.</span></span>

1.  <span data-ttu-id="f1532-125">既存のオファー データ プレースホルダーの名前を編集するには、まずプレースホルダーがテンプレートの一部でないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="f1532-125">To edit the name of any existing offer data placeholder, first make sure that the placeholder is not already part of any template.</span></span> <span data-ttu-id="f1532-126">次に、オファー データ プレースホルダーの名前をポイントし、必要に応じて名前を更新します。</span><span class="sxs-lookup"><span data-stu-id="f1532-126">Then, hover over the name of the offer data placeholder and update the name as needed.</span></span>

1. <span data-ttu-id="f1532-127">既存のオファー データ プレースホルダーを削除するには、まずプレースホルダーが他のテンプレートの一部でないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="f1532-127">To delete an existing offer data placeholder, first make sure that the placeholder is not part of any other template.</span></span> <span data-ttu-id="f1532-128">次に、プレースホルダー上に移動し、ごみ箱アイコンが表示されたら、ごみ箱をクリックし、オファー データ プレースホルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="f1532-128">Then, hover over the placeholder and when the trash can icon appears, click the trash can to delete the offer data placeholder.</span></span>
    >[!NOTE]
    > <span data-ttu-id="f1532-129">各オファー データの横にある数値のインジケータによって、オファー データ プレースホルダーの一部であるテンプレートの数を確認できます。</span><span class="sxs-lookup"><span data-stu-id="f1532-129">You can see how many templates an offer data placeholder is part of by the number indicator next to each offer data.</span></span> 

1. <span data-ttu-id="f1532-130">任意のセクションを削除するには、名前をポイントします。</span><span class="sxs-lookup"><span data-stu-id="f1532-130">To delete any section, hover over the name.</span></span> <span data-ttu-id="f1532-131">セクション内のオファー データ プレースホルダーのいずれもテンプレートに表示されない場合は、ごみ箱アイコンをクリックして削除することができます。</span><span class="sxs-lookup"><span data-stu-id="f1532-131">If none of the offer data placeholders inside the section appear in any template, you can click the trash can icon to delete it.</span></span> 
    >[!NOTE]
    > <span data-ttu-id="f1532-132">セクションを削除すると、そのセクション内のオファー データ プレースホルダもすべて削除されます。</span><span class="sxs-lookup"><span data-stu-id="f1532-132">Deleting the section will also delete all the offer data placeholders inside that section.</span></span>

<span data-ttu-id="f1532-133">オファー データ プレースホルダーが設定された後は、すべてのドキュメント テンプレートでそれらを使用できます。</span><span class="sxs-lookup"><span data-stu-id="f1532-133">After the offer data placeholders have been set up, you can use them across any document template.</span></span> <span data-ttu-id="f1532-134">オファー データ プレースホルダーは特定のテンプレートに限定されず、すべてのテンプレートで同じセットを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="f1532-134">Offer data placeholders are not restricted to a specific template -- the same set can be used across all templates.</span></span>

## <a name="offer-data-rules"></a><span data-ttu-id="f1532-135">オファー データ ルール</span><span class="sxs-lookup"><span data-stu-id="f1532-135">Offer data rules</span></span>

<span data-ttu-id="f1532-136">ほとんどの組織では、オファーの作成方法に関するルールがあります。</span><span class="sxs-lookup"><span data-stu-id="f1532-136">Most organization have rules for how offers must be created.</span></span> <span data-ttu-id="f1532-137">たとえば、特定の場所や勤続レベルの組み合わせに対する最大年間給与額のオファーが一定の範囲内になければならないこと、または新規採用のオファー レベルに対してはわずかな特定の値にすることなどを、組織が設定する場合があります。</span><span class="sxs-lookup"><span data-stu-id="f1532-137">For example, an organization may want to require that the maximum annual salary offer for a specific location and seniority level combination has to be within a certain range, or that there are only a few specific values possible for the offer level for the new hire.</span></span> <span data-ttu-id="f1532-138">Attract は現在、CSV ファイルを使用して、このようなデータ ルールをすべてサポートしています。</span><span class="sxs-lookup"><span data-stu-id="f1532-138">Attract currently supports all such data rules using a CSV file.</span></span>

<span data-ttu-id="f1532-139">データ ルール CSV ファイルを準備するには、次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="f1532-139">To prepare the data rules CSV file, do the following.</span></span>

1.  <span data-ttu-id="f1532-140">ルール セットのオファー データ プレースホルダーを決定します。</span><span class="sxs-lookup"><span data-stu-id="f1532-140">Determine the offer data placeholder for the rule set.</span></span> <span data-ttu-id="f1532-141">たとえば、**年間給与**。</span><span class="sxs-lookup"><span data-stu-id="f1532-141">For example, **Annual Salary**.</span></span>

1.  <span data-ttu-id="f1532-142">依存オファー データ プレースホルダーの値を識別します。</span><span class="sxs-lookup"><span data-stu-id="f1532-142">Identify the dependent offer data placeholder values.</span></span> <span data-ttu-id="f1532-143">たとえば、**勤務地**および**レベル**。</span><span class="sxs-lookup"><span data-stu-id="f1532-143">For example, **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="f1532-144">列 1 および 2 を**勤務地**および**レベル**として指定します。</span><span class="sxs-lookup"><span data-stu-id="f1532-144">Specify columns 1 and 2 as **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="f1532-145">範囲値をアップロードするには、列 3 と 4 を**年間給与**にします。</span><span class="sxs-lookup"><span data-stu-id="f1532-145">To upload a range value, make columns 3 and 4 **Annual Salary**.</span></span> <span data-ttu-id="f1532-146">範囲値ではなく特定の値をアップロードするには、列 3 のみを**年間給与**にします。</span><span class="sxs-lookup"><span data-stu-id="f1532-146">To upload a specific value instead of a range, only make column 3 **Annual Salary**.</span></span>

1.  <span data-ttu-id="f1532-147">必要なロールに基づいて Microsoft Excel ファイルを設定します。</span><span class="sxs-lookup"><span data-stu-id="f1532-147">Populate the Microsoft Excel file based on your required roles.</span></span>

1.  <span data-ttu-id="f1532-148">各行が、すべての値がまとめられた一意の組み合わせであることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="f1532-148">Ensure that each row is a unique combination of all the values put together.</span></span>

1.  <span data-ttu-id="f1532-149">ファイルを CSV フォーマットで保存します。</span><span class="sxs-lookup"><span data-stu-id="f1532-149">Save the file as a CSV format.</span></span>

<span data-ttu-id="f1532-150">オファー データ ルール ファイルをアップロードするには、次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="f1532-150">To upload the offer data rules file, do the following.</span></span>

1.  <span data-ttu-id="f1532-151">**オファー管理**へ移動します。</span><span class="sxs-lookup"><span data-stu-id="f1532-151">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="f1532-152">左のナビゲーション ウィンドウで**ライブラリ** セクションを展開して、**オファー データ ルール**に移動します。</span><span class="sxs-lookup"><span data-stu-id="f1532-152">Expand the **Library** section in the left navigation panel, then go to **Offer data rules**.</span></span>

1.  <span data-ttu-id="f1532-153">**新しいデータ セット**をクリックして、**アップロード** ダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="f1532-153">Click **New data set** to display the **Upload** dialog box.</span></span>

1.  <span data-ttu-id="f1532-154">ルール セットの一意の名前を指定し、保存した CSV ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="f1532-154">Specify a unique name for the rule set and then upload the saved CSV file.</span></span>

1.  <span data-ttu-id="f1532-155">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1532-155">Click **Add**.</span></span>
    <span data-ttu-id="f1532-156">ルール セットがバックグラウンドで処理され、完了後にアプリもしくは電子メールで通知されます。</span><span class="sxs-lookup"><span data-stu-id="f1532-156">The rule set will be processed in the background and you will be notified in-app and via email once it completes.</span></span>

    <span data-ttu-id="f1532-157">アップロードの処理中にエラーがある場合は、通知されます。</span><span class="sxs-lookup"><span data-stu-id="f1532-157">You will be notified if there are errors while processing the upload.</span></span> <span data-ttu-id="f1532-158">その後、エラー ログをダウンロードしてファイルを修正し、再度アップロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="f1532-158">You can then download the error log, fix the file, and upload it again.</span></span>

1.  <span data-ttu-id="f1532-159">ルール セットをダウンロードして値のセットを更新する場合は、省略記号ボタン (**…**) オプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="f1532-159">Use the ellipses button (**…**) option if you want to download the rule set and update the set of values.</span></span> <span data-ttu-id="f1532-160">更新後、再度ファイルをアップロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="f1532-160">After updating, you can upload the file again.</span></span>

1.  <span data-ttu-id="f1532-161">定義中のプレースホルダーが別のドキュメント テンプレートで使用されていない場合は、既存のルール セットのアップロードを削除できます。</span><span class="sxs-lookup"><span data-stu-id="f1532-161">You can delete an existing rule set upload if the placeholder being defined is not being used in another document template.</span></span>

>[!NOTES]
> - <span data-ttu-id="f1532-163">各プレース ホルダーは、それが依存している一意の列セットを 1 つしか持てません。</span><span class="sxs-lookup"><span data-stu-id="f1532-163">Each placeholder can only have one unique set of columns that it is dependent on.</span></span> <span data-ttu-id="f1532-164">たとえば、**年間給与**が**勤務地**および**レベル**に依存している場合、**年間給与**が別の列セットに依存しているルール セットをアップロードすることはできません。</span><span class="sxs-lookup"><span data-stu-id="f1532-164">For example, if **Annual Salary** is dependent on **Job Location** and **Level**, you can't upload another rule set where **Annual Salary** is dependent on a different set of columns.</span></span>

> - <span data-ttu-id="f1532-165"> *\*オファー データ ルール** ページの*\*サンプル** タブに、サンプル オファー ルール セットをダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="f1532-165">You can download sample offer data rule sets on the **Samples** tab on the **Offer data rules** page.</span></span>

> - <span data-ttu-id="f1532-166">オファー作成者がオファー データ ルールで推奨される値を上書きすると、オファーは非標準としてフラグが設定され、オファーの承認ワークフローが必須になります。</span><span class="sxs-lookup"><span data-stu-id="f1532-166">When an offer creator overrides the values that are recommended by the offer data rules, the offer is flagged as non-standard and offer approval workflow will be mandated.</span></span>

## <a name="document-templates"></a><span data-ttu-id="f1532-167">ドキュメント テンプレート</span><span class="sxs-lookup"><span data-stu-id="f1532-167">Document templates</span></span>

<span data-ttu-id="f1532-168">オファー ドキュメント テンプレートは管理者がオファー レターを作成するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="f1532-168">An offer document template can help administrators create offer letters.</span></span> <span data-ttu-id="f1532-169">オファー ドキュメント テンプレートは、オファーの一部となるテキストと定義されたオファー データ プレースホルダーの組み合わせです。</span><span class="sxs-lookup"><span data-stu-id="f1532-169">The offer document template is a combination of the text that will be part of the offer as well as the defined offer data placeholders.</span></span> 

<span data-ttu-id="f1532-170">オファー ドキュメント テンプレートを作成するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="f1532-170">To create an offer document template, do the following.</span></span>

1.  <span data-ttu-id="f1532-171">**オファー管理**へ移動します。</span><span class="sxs-lookup"><span data-stu-id="f1532-171">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="f1532-172">左のナビゲーション ウィンドウで**ライブラリ** セクションを展開して、**テンプレート**に移動します。</span><span class="sxs-lookup"><span data-stu-id="f1532-172">Expand the **Library** section in the left navigation pane and go to **Templates**.</span></span>

    <span data-ttu-id="f1532-173">**テンプレート** ページには、既に定義されているドキュメント テンプレートのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f1532-173">The **Templates** page will display a list of document templates that have already been defined.</span></span>

1.  <span data-ttu-id="f1532-174">新しいドキュメント テンプレートを作成するには、**新規テンプレート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1532-174">To create a new document template, click **New Template**.</span></span>

1.  <span data-ttu-id="f1532-175">テンプレートに一意の名前を入力し、**作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1532-175">Enter a unique name for the template and click **Create**.</span></span>

1.  <span data-ttu-id="f1532-176">リッチ テキスト エディターを使用して、オファー ドキュメントの内容を挿入または編集します。</span><span class="sxs-lookup"><span data-stu-id="f1532-176">Use the rich text editor to insert or edit the offer document content.</span></span> <span data-ttu-id="f1532-177">テキスト エディターの上部にあるオプションを使用して、表、イメージおよびハイパーリンクを挿入できます。</span><span class="sxs-lookup"><span data-stu-id="f1532-177">You can insert tables, images, and hyperlinks using the options available at the top of the text editor.</span></span>

1.  <span data-ttu-id="f1532-178">オファー テンプレート ドキュメントに、オファー データ プレースホルダを挿入するには、次を実行します。</span><span class="sxs-lookup"><span data-stu-id="f1532-178">You can insert offer data placeholders in the offer template document by:</span></span>

    - <span data-ttu-id="f1532-179">右ウィンドウからドラッグ アンド ドロップします。</span><span class="sxs-lookup"><span data-stu-id="f1532-179">Dragging and dropping from the right pane.</span></span>

    - <span data-ttu-id="f1532-180">オファー データ プレースホルダーを直接職位にハッシュタグ付けしてください。</span><span class="sxs-lookup"><span data-stu-id="f1532-180">Hashtag the offer data placeholder directly into position.</span></span> <span data-ttu-id="f1532-181">**\#** をタイプし、オファー データ プレースホルダーの名前を入力してください。</span><span class="sxs-lookup"><span data-stu-id="f1532-181">Type **\#** and then start typing the name of the offer data placeholder.</span></span> <span data-ttu-id="f1532-182">オプションは、ドロップダウン リストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f1532-182">Options will appear in the drop-down list.</span></span> <span data-ttu-id="f1532-183">**入力**をクリックまたは押して、オファー データ プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="f1532-183">Click or press **Enter** to insert the offer data placeholder.</span></span>

    >[!NOTES]
    > - <span data-ttu-id="f1532-185">候補者にはその値を公開せずに、プレースホルダーをオファー ドキュメント テンプレートに関連付けるには、オファー データ プレースホルダーをポイントし、**固定**アイコンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1532-185">To associate a placeholder to the offer document template without exposing its value to the candidate, hover over the offer data placeholder and click the **Pin** icon.</span></span> <span data-ttu-id="f1532-186">これにより、プレースホルダーがオファー ドキュメント テンプレートの**固定されたオファー データ** セクションにプッシュされます。</span><span class="sxs-lookup"><span data-stu-id="f1532-186">This will push the placeholder to the **Pinned offer data** section of the offer document template.</span></span> <span data-ttu-id="f1532-187">固定解除するには、同じ手順を実行しますが、オファー データ プレースホルダーのリストの**固定解除**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1532-187">To unpin, follow the same steps but click **Unpin** in the list of offer data placeholders.</span></span>

    > - <span data-ttu-id="f1532-188">有効なオファー データ プレースホルダーのリストを表示するには、右ウィンドウで**有効**タブに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="f1532-188">To view the list of active offer data placeholders, switch to the **Active** tab in the right pane.</span></span>

    > - <span data-ttu-id="f1532-189">オファー データのルール セットにより駆動されているプレースホルダーを挿入する場合は、そのオファー データ プレースホルダーの他の値への依存関係を確認できます。</span><span class="sxs-lookup"><span data-stu-id="f1532-189">If you insert a placeholder that is driven by an offer data rule set, you can see the dependency of that offer data placeholder on other values.</span></span>

    > - <span data-ttu-id="f1532-190">または、ローカル コンピューターの .docx ファイルからコンテンツを**インポート**し、必要に応じて編集することもできます。</span><span class="sxs-lookup"><span data-stu-id="f1532-190">Alternatively, you can **Import** the content from a .docx file on your local machine and edit as required.</span></span> <span data-ttu-id="f1532-191">これにより、エディター内のすべてのコンテンツを入力する必要がなくなります。</span><span class="sxs-lookup"><span data-stu-id="f1532-191">That way, you don’t have to type in all the content in the editor.</span></span>

1. <span data-ttu-id="f1532-192">オファー ドキュメントをプレビューするには、ページ上部にある**プレビュー** オプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="f1532-192">To preview the offer document, use the **Preview** option at the top of the page.</span></span>

1. <span data-ttu-id="f1532-193">オファー作成者がオファー ドキュメントの内容を編集できるかどうかを管理するには、ページ上部の**アクセス許可の管理**オプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="f1532-193">To control whether an offer creator can edit the offer document content, use the **Manage permission** option at the top of the page.</span></span> <span data-ttu-id="f1532-194">オファー作成者がプレースホルダーの値のみを挿入し、テキストを編集しないようにする場合は、アクセス許可の値を**いいえ**に設定します。</span><span class="sxs-lookup"><span data-stu-id="f1532-194">If you want the offer creator to only insert placeholder values and not edit text, set the permission value to **No**.</span></span>

1. <span data-ttu-id="f1532-195">**保存**をクリックして進捗状況を保存します。</span><span class="sxs-lookup"><span data-stu-id="f1532-195">Click **Save** to save your progress.</span></span> <span data-ttu-id="f1532-196">テンプレートは、ドラフト状態で保存されます。</span><span class="sxs-lookup"><span data-stu-id="f1532-196">The template will be saved in a draft state.</span></span>

1. <span data-ttu-id="f1532-197">ドキュメントを確定して公開したい場合は、**完了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1532-197">To finalize and mark the document as published, click **Finish**.</span></span>

1. <span data-ttu-id="f1532-198">どのドキュメント テンプレートが現在有効か、ドラフト モードか、アーカイブされ使用されていないかを、ドキュメント テンプレート ライブラリ ランディング エクスペリエンスで確認できます。</span><span class="sxs-lookup"><span data-stu-id="f1532-198">You can see which document templates are currently active, in draft mode, and have been archived and are no longer in use on the document templates library landing experience.</span></span>

>[!NOTE]
> <span data-ttu-id="f1532-199">既存のオファー パッケージ テンプレートの一部ではないオファー ドキュメント テンプレートを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="f1532-199">You can delete any offer document template that is not part of an existing offer package template.</span></span>


## <a name="offer-package-templates"></a><span data-ttu-id="f1532-200">オファー パッケージ テンプレート</span><span class="sxs-lookup"><span data-stu-id="f1532-200">Offer package templates</span></span>

<span data-ttu-id="f1532-201">オファー パッケージは、候補者と共有されるオファー コンポーネントであり、1 つ以上のオファー ドキュメント テンプレートの組み合わせで構成されています。</span><span class="sxs-lookup"><span data-stu-id="f1532-201">Offer packages are the offer artifacts that are shared with the candidate and consist of a combination of one or more offer document templates.</span></span> <span data-ttu-id="f1532-202">オファー パッケージを作成するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="f1532-202">To create an offer package, do the following.</span></span>

1.  <span data-ttu-id="f1532-203">**オファー管理**へ移動します。</span><span class="sxs-lookup"><span data-stu-id="f1532-203">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="f1532-204">左のナビゲーション ウィンドウから**パッケージ**に移動します。</span><span class="sxs-lookup"><span data-stu-id="f1532-204">Go to **Packages** from the left navigation pane.</span></span>

    <span data-ttu-id="f1532-205">オファー作成者が使用できる、有効なパッケージ テンプレートのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f1532-205">A list of active package templates that are available for offer creators to use is displayed.</span></span>

1.  <span data-ttu-id="f1532-206">新しいオファー パッケージを作成するには、**新しいパッケージ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1532-206">To create a new offer package, click **New Package**.</span></span>

1.  <span data-ttu-id="f1532-207">一意の名前を入力し、**作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1532-207">Enter a unique name and click **Create**.</span></span>

1.  <span data-ttu-id="f1532-208">**テンプレートの追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1532-208">Click **Add template**.</span></span>

    >[!NOTES]
    > - <span data-ttu-id="f1532-210">新しいテンプレートを作成するか、既存のテンプレートから選択するかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="f1532-210">You can choose to create a new template or choose from an existing one.</span></span>

    > - <span data-ttu-id="f1532-211">既存のテンプレートを追加する場合は、オファー ドキュメント テンプレートが保存され、確定され、有効とマークされていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f1532-211">If you choose to add an existing template, you need to make sure that the   offer document template was saved, finalized, and marked as   active.</span></span>
    
    > - <span data-ttu-id="f1532-212">ドキュメント テンプレートを必要なだけ選択することができます。</span><span class="sxs-lookup"><span data-stu-id="f1532-212">You can choose as many document templates as you want.</span></span> 
    
1.  <span data-ttu-id="f1532-213">**完了**をクリックし、**パッケージ管理**に戻ります。</span><span class="sxs-lookup"><span data-stu-id="f1532-213">Click **Done** to return to **Package management**.</span></span>

    <span data-ttu-id="f1532-214">ドキュメントの順序を設定したり、オファー作成中に特定のオファー ドキュメントが必要かどうかをマークすることもできます。</span><span class="sxs-lookup"><span data-stu-id="f1532-214">You can configure the sequence of the documents and also mark whether the specific offer document is required during offer creation.</span></span> <span data-ttu-id="f1532-215">オファー作成者には、**不要**とマークされているドキュメントを削除するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="f1532-215">The offer creator will have an option to delete the documents marked as **Not required**.</span></span>

1. <span data-ttu-id="f1532-216">オファー パッケージ テンプレートを保存し、すべてのオファー作成者がそれを使用できるようにするためには、**保存して公開**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1532-216">To save the offer package template so that it's usable by all offer creators, click **Save and publish**.</span></span>

   <span data-ttu-id="f1532-217">ドラフト オファー パッケージ テンプレートを表示するには、**ドラフト** タブに移動します。オファー パッケージ テンプレートに変更が加えられた場合は、保存し再公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f1532-217">To view draft offer package templates, go to the **Drafts** tab. If a change is made to the offer package template, it must be  saved and republished.</span></span>

## <a name="configure-an-offer-process"></a><span data-ttu-id="f1532-218">オファー プロセスのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="f1532-218">Configure an offer process</span></span>

<span data-ttu-id="f1532-219">Attract 管理者によって設定可能なオファー作成プロセスの部分がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="f1532-219">There are several parts of the offer creation process that can be configured by an Attract administrator.</span></span>

- <span data-ttu-id="f1532-220">**オファーの承認** - オファーが候補者に送付される前にオファーの承認が必要かどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="f1532-220">**Offer approvals** - Choose whether offer approvals are required before the offer can be sent to the candidate.</span></span> <span data-ttu-id="f1532-221">管理者は、すべてのオファー承認を順次または並列な承認ワークフローで行うかどうかを決定することもできます。</span><span class="sxs-lookup"><span data-stu-id="f1532-221">As an administrator, you can also decide whether all offer approvals will happen in a sequential manner or parallel approval workflow.</span></span> <span data-ttu-id="f1532-222">オファーの承認者が、オファーの承認とともにコメントを追加する必要があるかどうかを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="f1532-222">You can also mandate whether offer approvers must add a comment along with their offer approval.</span></span> <span data-ttu-id="f1532-223">すべての非標準のオファーには、オファーの承認が必須です。</span><span class="sxs-lookup"><span data-stu-id="f1532-223">Offer approvals are mandatory for all non-standard offers.</span></span>

- <span data-ttu-id="f1532-224">**候補者のオファー エクスペリエンス** - 管理者は、すべてのオファーに有効期限を設定するかどうかを決定することができます。有効期限を設定する場合は、有効期限の既定のオフセットを設定します。</span><span class="sxs-lookup"><span data-stu-id="f1532-224">**Candidate’s offer experience** - As administrator, you can choose to set whether all offers have an expiration date, and if so, what the default offset for the expiration date should be.</span></span> <span data-ttu-id="f1532-225">候補者がオファーを拒否できるかどうかも設定することができます。</span><span class="sxs-lookup"><span data-stu-id="f1532-225">You can also configure whether candidates can decline an offer.</span></span>

- <span data-ttu-id="f1532-226">**電子署名** - 候補者がオファーを承諾してオファー パッケージに名前を入力する際に、現在利用可能なオプションは、電子署名のみです。</span><span class="sxs-lookup"><span data-stu-id="f1532-226">**e-Signatures** - Currently, the only electronic signature option available is for candidates to type their name in the offer package while accepting the offer.</span></span> <span data-ttu-id="f1532-227">今後、他の電子署名プロバイダーとのパートナー統合についてもご紹介する予定です。</span><span class="sxs-lookup"><span data-stu-id="f1532-227">We will introduce partner integrations with other electronic signature providers in the future.</span></span>


<span data-ttu-id="f1532-228">オファー作成プロセスの詳細については、[作成、承認、および署名](./creating-offers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f1532-228">To learn more about the offer creation process, see [Creating, approving, and signing offers](./creating-offers.md).</span></span>

