---
title: オファー管理の設定
description: このトピックでは、Talent でのオファーの設定方法について説明します。
author: josaw
manager: AnnBe
ms.date: 02/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43cf13d96e345747e06541267d820e17de7c1763
ms.sourcegitcommit: ea17d2e35c24a141c20ab429897eebf9fa186f61
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/26/2019
ms.locfileid: "768885"
---
# <a name="set-up-offer-management"></a><span data-ttu-id="ea4b1-103">オファー管理の設定</span><span class="sxs-lookup"><span data-stu-id="ea4b1-103">Set up offer management</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="ea4b1-104">Dynamics 365 for Talent: Attract で候補者がオファー ステージに進む場合、候補者のオファーを迅速に作成し、必要に応じて承認し、候補者に送付することを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-104">When a candidate is moved to the offer stage in Dynamics 365 for Talent: Attract, you need to ensure that the offers can be quickly created for the candidate, approved as necessary, and sent out to the candidate.</span></span> <span data-ttu-id="ea4b1-105">ほとんどのオファーが標準なので、再利用可能なテンプレートから作成することができます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-105">Because most offers are standard, they can be created from reusable templates.</span></span> <span data-ttu-id="ea4b1-106">Attract では、すべてのオファーは 1 つまたは複数のオファー ドキュメントのコレクションであるオファー パッケージにロールアップされます</span><span class="sxs-lookup"><span data-stu-id="ea4b1-106">In Attract, all offers are rolled into an offer package, which is a collection of one or more offer documents.</span></span> 

<span data-ttu-id="ea4b1-107">このトピックでは、Attract 管理者が Attract のオファー管理機能の一部としてさまざまなオファー パッケージ テンプレートを設定するために必要なすべての手順を示します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-107">This topic lists all the steps that an Attract administrator would follow to set up different offer package templates as part of the offer management capability in Attract.</span></span> <span data-ttu-id="ea4b1-108">管理者以外のユーザーには、これらの機能に対するアクセス許可がありません。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-108">Users with non-administrator roles will not have access to these capabilities.</span></span>

>[!NOTE]
> <span data-ttu-id="ea4b1-109">オファー管理機能は、包括採用アドオンの一部として使用できます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-109">Offer management capabilities are available as part of the Comprehensive Hiring Add-On.</span></span>

## <a name="offer-data"></a><span data-ttu-id="ea4b1-110">オファー データ</span><span class="sxs-lookup"><span data-stu-id="ea4b1-110">Offer data</span></span> 

<span data-ttu-id="ea4b1-111">オファー データは、オファー パッケージ テンプレート内の最小単位です。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-111">Offer data is the smallest unit inside the offer package template.</span></span> <span data-ttu-id="ea4b1-112">標準的なオファーは、標準のテキストと値のセットで構成されます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-112">A typical offer consists of standard text and a set of values.</span></span> <span data-ttu-id="ea4b1-113">値のセットは、オファー間で変更できる唯一の点です。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-113">The sets of values are the only pieces that could change between offers.</span></span> <span data-ttu-id="ea4b1-114">オファーの作成時に、オファー作成者が重視する最も重要な側面は、オファーのパッケージ テンプレートにオファー データ プレースホルダーのリストがあることです。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-114">During the offer creation, the most important aspect that the offer creator can focus on is the list of offer data placeholders present in an offer package template.</span></span> <span data-ttu-id="ea4b1-115">オファー データを設定するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-115">To set up offer data, do the following.</span></span>

1.  <span data-ttu-id="ea4b1-116">**オファー管理**へ移動します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-116">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="ea4b1-117">左のナビゲーション ウィンドウで**ライブラリ** セクションを展開して、**オファー データ**に進みます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-117">Expand the **Library** section in the left navigation pane, then go to **Offer data**.</span></span>

    >[!NOTE]
    > <span data-ttu-id="ea4b1-118">**オファー データ** ページには、**候補者の詳細**および**職務の詳細**セクションがあります。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-118">On the **Offer data** page are the **Candidate details** and **Job details** sections.</span></span> <span data-ttu-id="ea4b1-119">Attract はいくつかのオファー データ プレースホルダーをすぐに提供します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-119">Attract provides a few offer data placeholders out-of-the-box.</span></span>
    
    > <span data-ttu-id="ea4b1-120">ページには、さまざまなオファー データ プレースホルダーを論理的なグループにまとめるセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-120">There are sections on the page to organize different offer data placeholders together in logical groups.</span></span> <span data-ttu-id="ea4b1-121">これらのセクションは、オファーの作成プロセスでオファー データおよびデータ設定を維持するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-121">These sections can help with maintenance of offer data and population of data during the offer creation process.</span></span>

1.  <span data-ttu-id="ea4b1-122">新しいオファー データ セクションを作成するには、**セクションを追加**をクリックし、セクションの一意の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-122">To create a new offer data section, click **Add a section** and enter a unique name for the section.</span></span>

1.  <span data-ttu-id="ea4b1-123">任意のセクションにオファー データ プレースホルダーを追加するには、**オファー データを追加**をクリックし、プレースホルダーの一意の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-123">To add offer data placeholders to any section, click **Add offer data** and enter a unique name for the placeholder.</span></span>

1.  <span data-ttu-id="ea4b1-124">任意のセクションの名前を編集するには、セクションの名前をポイントし、名前を更新します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-124">To edit the name of any section, hover over the section name and update the name.</span></span>

1.  <span data-ttu-id="ea4b1-125">既存のオファー データ プレースホルダーの名前を編集するには、まずプレースホルダーがテンプレートの一部でないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-125">To edit the name of any existing offer data placeholder, first make sure that the placeholder is not already part of any template.</span></span> <span data-ttu-id="ea4b1-126">次に、オファー データ プレースホルダーの名前をポイントし、必要に応じて名前を更新します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-126">Then, hover over the name of the offer data placeholder and update the name as needed.</span></span>

1. <span data-ttu-id="ea4b1-127">既存のオファー データ プレースホルダーを削除するには、まずプレースホルダーが他のテンプレートの一部でないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-127">To delete an existing offer data placeholder, first make sure that the placeholder is not part of any other template.</span></span> <span data-ttu-id="ea4b1-128">次に、プレースホルダー上に移動し、ごみ箱アイコンが表示されたら、ごみ箱をクリックし、オファー データ プレースホルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-128">Then, hover over the placeholder and when the trash can icon appears, click the trash can to delete the offer data placeholder.</span></span>
    >[!NOTE]
    > <span data-ttu-id="ea4b1-129">各オファー データの横にある数値のインジケータによって、オファー データ プレースホルダーの一部であるテンプレートの数を確認できます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-129">You can see how many templates an offer data placeholder is part of by the number indicator next to each offer data.</span></span> 

1. <span data-ttu-id="ea4b1-130">任意のセクションを削除するには、名前をポイントします。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-130">To delete any section, hover over the name.</span></span> <span data-ttu-id="ea4b1-131">セクション内のオファー データ プレースホルダーのいずれもテンプレートに表示されない場合は、ごみ箱アイコンをクリックして削除することができます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-131">If none of the offer data placeholders inside the section appear in any template, you can click the trash can icon to delete it.</span></span> 
    >[!NOTE]
    > <span data-ttu-id="ea4b1-132">セクションを削除すると、そのセクション内のオファー データ プレースホルダもすべて削除されます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-132">Deleting the section will also delete all the offer data placeholders inside that section.</span></span>

<span data-ttu-id="ea4b1-133">オファー データ プレースホルダーが設定された後は、すべてのドキュメント テンプレートでそれらを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-133">After the offer data placeholders have been set up, you can use them across any document template.</span></span> <span data-ttu-id="ea4b1-134">オファー データ プレースホルダーは特定のテンプレートに限定されず、すべてのテンプレートで同じセットを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-134">Offer data placeholders are not restricted to a specific template -- the same set can be used across all templates.</span></span>

## <a name="offer-data-rules"></a><span data-ttu-id="ea4b1-135">オファー データ ルール</span><span class="sxs-lookup"><span data-stu-id="ea4b1-135">Offer data rules</span></span>

<span data-ttu-id="ea4b1-136">ほとんどの組織では、オファーの作成方法に関するルールがあります。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-136">Most organization have rules for how offers must be created.</span></span> <span data-ttu-id="ea4b1-137">たとえば、特定の場所や勤続レベルの組み合わせに対する最大年間給与額のオファーが一定の範囲内になければならないこと、または新規採用のオファー レベルに対してはわずかな特定の値にすることなどを、組織が設定する場合があります。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-137">For example, an organization may want to require that the maximum annual salary offer for a specific location and seniority level combination has to be within a certain range, or that there are only a few specific values possible for the offer level for the new hire.</span></span> <span data-ttu-id="ea4b1-138">Attract は現在、CSV ファイルを使用して、このようなデータ ルールをすべてサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-138">Attract currently supports all such data rules using a CSV file.</span></span>

<span data-ttu-id="ea4b1-139">データ ルール CSV ファイルを準備するには、次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-139">To prepare the data rules CSV file, do the following.</span></span>

1.  <span data-ttu-id="ea4b1-140">ルール セットのオファー データ プレースホルダーを決定します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-140">Determine the offer data placeholder for the rule set.</span></span> <span data-ttu-id="ea4b1-141">たとえば、**年間給与**。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-141">For example, **Annual Salary**.</span></span>

1.  <span data-ttu-id="ea4b1-142">依存オファー データ プレースホルダーの値を識別します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-142">Identify the dependent offer data placeholder values.</span></span> <span data-ttu-id="ea4b1-143">たとえば、**勤務地**および**レベル**。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-143">For example, **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="ea4b1-144">列 1 および 2 を**勤務地**および**レベル**として指定します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-144">Specify columns 1 and 2 as **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="ea4b1-145">範囲値をアップロードするには、列 3 と 4 を**年間給与**にします。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-145">To upload a range value, make columns 3 and 4 **Annual Salary**.</span></span> <span data-ttu-id="ea4b1-146">範囲値ではなく特定の値をアップロードするには、列 3 のみを**年間給与**にします。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-146">To upload a specific value instead of a range, only make column 3 **Annual Salary**.</span></span>

1.  <span data-ttu-id="ea4b1-147">必要なロールに基づいて Microsoft Excel ファイルを設定します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-147">Populate the Microsoft Excel file based on your required roles.</span></span>

1.  <span data-ttu-id="ea4b1-148">各行が、すべての値がまとめられた一意の組み合わせであることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-148">Ensure that each row is a unique combination of all the values put together.</span></span>

1.  <span data-ttu-id="ea4b1-149">ファイルを CSV フォーマットで保存します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-149">Save the file as a CSV format.</span></span>

<span data-ttu-id="ea4b1-150">オファー データ ルール ファイルをアップロードするには、次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-150">To upload the offer data rules file, do the following.</span></span>

1.  <span data-ttu-id="ea4b1-151">**オファー管理**へ移動します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-151">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="ea4b1-152">左のナビゲーション ウィンドウで**ライブラリ** セクションを展開して、**オファー データ ルール**に移動します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-152">Expand the **Library** section in the left navigation panel, then go to **Offer data rules**.</span></span>

1.  <span data-ttu-id="ea4b1-153">**新しいデータ セット**をクリックして、**アップロード** ダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-153">Click **New data set** to display the **Upload** dialog box.</span></span>

1.  <span data-ttu-id="ea4b1-154">ルール セットの一意の名前を指定し、保存した CSV ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-154">Specify a unique name for the rule set and then upload the saved CSV file.</span></span>

1.  <span data-ttu-id="ea4b1-155">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-155">Click **Add**.</span></span>
    <span data-ttu-id="ea4b1-156">ルール セットがバックグラウンドで処理され、完了後にアプリもしくは電子メールで通知されます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-156">The rule set will be processed in the background and you will be notified in-app and via email once it completes.</span></span>

    <span data-ttu-id="ea4b1-157">アップロードの処理中にエラーがある場合は、通知されます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-157">You will be notified if there are errors while processing the upload.</span></span> <span data-ttu-id="ea4b1-158">その後、エラー ログをダウンロードしてファイルを修正し、再度アップロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-158">You can then download the error log, fix the file, and upload it again.</span></span>

1.  <span data-ttu-id="ea4b1-159">ルール セットをダウンロードして値のセットを更新する場合は、省略記号ボタン (**…**) オプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-159">Use the ellipses button (**…**) option if you want to download the rule set and update the set of values.</span></span> <span data-ttu-id="ea4b1-160">更新後、再度ファイルをアップロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-160">After updating, you can upload the file again.</span></span>

1.  <span data-ttu-id="ea4b1-161">定義中のプレースホルダーが別のドキュメント テンプレートで使用されていない場合は、既存のルール セットのアップロードを削除できます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-161">You can delete an existing rule set upload if the placeholder being defined is not being used in another document template.</span></span>

>[!NOTE]
> - <span data-ttu-id="ea4b1-162">各プレース ホルダーは、それが依存している一意の列セットを 1 つしか持てません。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-162">Each placeholder can only have one unique set of columns that it is dependent on.</span></span> <span data-ttu-id="ea4b1-163">たとえば、**年間給与**が**勤務地**および**レベル**に依存している場合、**年間給与**が別の列セットに依存しているルール セットをアップロードすることはできません。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-163">For example, if **Annual Salary** is dependent on **Job Location** and **Level**, you can't upload another rule set where **Annual Salary** is dependent on a different set of columns.</span></span>

> - <span data-ttu-id="ea4b1-164"> *\*オファー データ ルール** ページの*\*サンプル** タブに、サンプル オファー ルール セットをダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-164">You can download sample offer data rule sets on the **Samples** tab on the **Offer data rules** page.</span></span>

> - <span data-ttu-id="ea4b1-165">オファー作成者がオファー データ ルールで推奨される値を上書きすると、オファーは非標準としてフラグが設定され、オファーの承認ワークフローが必須になります。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-165">When an offer creator overrides the values that are recommended by the offer data rules, the offer is flagged as non-standard and offer approval workflow will be mandated.</span></span>

## <a name="document-templates"></a><span data-ttu-id="ea4b1-166">ドキュメント テンプレート</span><span class="sxs-lookup"><span data-stu-id="ea4b1-166">Document templates</span></span>

<span data-ttu-id="ea4b1-167">オファー ドキュメント テンプレートは管理者がオファー レターを作成するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-167">An offer document template can help administrators create offer letters.</span></span> <span data-ttu-id="ea4b1-168">オファー ドキュメント テンプレートは、オファーの一部となるテキストと定義されたオファー データ プレースホルダーの組み合わせです。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-168">The offer document template is a combination of the text that will be part of the offer as well as the defined offer data placeholders.</span></span> 

<span data-ttu-id="ea4b1-169">オファー ドキュメント テンプレートを作成するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-169">To create an offer document template, do the following.</span></span>

1.  <span data-ttu-id="ea4b1-170">**オファー管理**へ移動します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-170">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="ea4b1-171">左のナビゲーション ウィンドウで**ライブラリ** セクションを展開して、**テンプレート**に移動します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-171">Expand the **Library** section in the left navigation pane and go to **Templates**.</span></span>

    <span data-ttu-id="ea4b1-172">**テンプレート** ページには、既に定義されているドキュメント テンプレートのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-172">The **Templates** page will display a list of document templates that have already been defined.</span></span>

1.  <span data-ttu-id="ea4b1-173">新しいドキュメント テンプレートを作成するには、**新規テンプレート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-173">To create a new document template, click **New Template**.</span></span>

1.  <span data-ttu-id="ea4b1-174">テンプレートに一意の名前を入力し、**作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-174">Enter a unique name for the template and click **Create**.</span></span>

1.  <span data-ttu-id="ea4b1-175">リッチ テキスト エディターを使用して、オファー ドキュメントの内容を挿入または編集します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-175">Use the rich text editor to insert or edit the offer document content.</span></span> <span data-ttu-id="ea4b1-176">テキスト エディターの上部にあるオプションを使用して、表、イメージおよびハイパーリンクを挿入できます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-176">You can insert tables, images, and hyperlinks using the options available at the top of the text editor.</span></span>

1.  <span data-ttu-id="ea4b1-177">オファー テンプレート ドキュメントに、オファー データ プレースホルダを挿入するには、次を実行します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-177">You can insert offer data placeholders in the offer template document by:</span></span>

    - <span data-ttu-id="ea4b1-178">右ウィンドウからドラッグ アンド ドロップします。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-178">Dragging and dropping from the right pane.</span></span>

    - <span data-ttu-id="ea4b1-179">オファー データ プレースホルダーを直接職位にハッシュタグ付けしてください。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-179">Hashtag the offer data placeholder directly into position.</span></span> <span data-ttu-id="ea4b1-180">**\#** をタイプし、オファー データ プレースホルダーの名前を入力してください。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-180">Type **\#** and then start typing the name of the offer data placeholder.</span></span> <span data-ttu-id="ea4b1-181">オプションは、ドロップダウン リストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-181">Options will appear in the drop-down list.</span></span> <span data-ttu-id="ea4b1-182">**入力**をクリックまたは押して、オファー データ プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-182">Click or press **Enter** to insert the offer data placeholder.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="ea4b1-183">候補者にはその値を公開せずに、プレースホルダーをオファー ドキュメント テンプレートに関連付けるには、オファー データ プレースホルダーをポイントし、**固定**アイコンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-183">To associate a placeholder to the offer document template without exposing its value to the candidate, hover over the offer data placeholder and click the **Pin** icon.</span></span> <span data-ttu-id="ea4b1-184">これにより、プレースホルダーがオファー ドキュメント テンプレートの**固定されたオファー データ** セクションにプッシュされます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-184">This will push the placeholder to the **Pinned offer data** section of the offer document template.</span></span> <span data-ttu-id="ea4b1-185">固定解除するには、同じ手順を実行しますが、オファー データ プレースホルダーのリストの**固定解除**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-185">To unpin, follow the same steps but click **Unpin** in the list of offer data placeholders.</span></span>

    > - <span data-ttu-id="ea4b1-186">有効なオファー データ プレースホルダーのリストを表示するには、右ウィンドウで**有効**タブに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-186">To view the list of active offer data placeholders, switch to the **Active** tab in the right pane.</span></span>

    > - <span data-ttu-id="ea4b1-187">オファー データのルール セットにより駆動されているプレースホルダーを挿入する場合は、そのオファー データ プレースホルダーの他の値への依存関係を確認できます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-187">If you insert a placeholder that is driven by an offer data rule set, you can see the dependency of that offer data placeholder on other values.</span></span>

    > - <span data-ttu-id="ea4b1-188">または、ローカル コンピューターの .docx ファイルからコンテンツを**インポート**し、必要に応じて編集することもできます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-188">Alternatively, you can **Import** the content from a .docx file on your local machine and edit as required.</span></span> <span data-ttu-id="ea4b1-189">これにより、エディター内のすべてのコンテンツを入力する必要がなくなります。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-189">That way, you don’t have to type in all the content in the editor.</span></span>

1. <span data-ttu-id="ea4b1-190">オファー ドキュメントをプレビューするには、ページ上部にある**プレビュー** オプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-190">To preview the offer document, use the **Preview** option at the top of the page.</span></span>

1. <span data-ttu-id="ea4b1-191">オファー作成者がオファー ドキュメントの内容を編集できるかどうかを管理するには、ページ上部の**アクセス許可の管理**オプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-191">To control whether an offer creator can edit the offer document content, use the **Manage permission** option at the top of the page.</span></span> <span data-ttu-id="ea4b1-192">オファー作成者がプレースホルダーの値のみを挿入し、テキストを編集しないようにする場合は、アクセス許可の値を**いいえ**に設定します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-192">If you want the offer creator to only insert placeholder values and not edit text, set the permission value to **No**.</span></span>

1. <span data-ttu-id="ea4b1-193">**保存**をクリックして進捗状況を保存します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-193">Click **Save** to save your progress.</span></span> <span data-ttu-id="ea4b1-194">テンプレートは、ドラフト状態で保存されます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-194">The template will be saved in a draft state.</span></span>

1. <span data-ttu-id="ea4b1-195">ドキュメントを確定して公開したい場合は、**完了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-195">To finalize and mark the document as published, click **Finish**.</span></span>

1. <span data-ttu-id="ea4b1-196">どのドキュメント テンプレートが現在有効か、ドラフト モードか、アーカイブされ使用されていないかを、ドキュメント テンプレート ライブラリ ランディング エクスペリエンスで確認できます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-196">You can see which document templates are currently active, in draft mode, and have been archived and are no longer in use on the document templates library landing experience.</span></span>

>[!NOTE]
> <span data-ttu-id="ea4b1-197">既存のオファー パッケージ テンプレートの一部ではないオファー ドキュメント テンプレートを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-197">You can delete any offer document template that is not part of an existing offer package template.</span></span>


## <a name="offer-package-templates"></a><span data-ttu-id="ea4b1-198">オファー パッケージ テンプレート</span><span class="sxs-lookup"><span data-stu-id="ea4b1-198">Offer package templates</span></span>

<span data-ttu-id="ea4b1-199">オファー パッケージは、候補者と共有されるオファー コンポーネントであり、1 つ以上のオファー ドキュメント テンプレートの組み合わせで構成されています。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-199">Offer packages are the offer artifacts that are shared with the candidate and consist of a combination of one or more offer document templates.</span></span> <span data-ttu-id="ea4b1-200">オファー パッケージを作成するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-200">To create an offer package, do the following.</span></span>

1.  <span data-ttu-id="ea4b1-201">**オファー管理**へ移動します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-201">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="ea4b1-202">左のナビゲーション ウィンドウから**パッケージ**に移動します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-202">Go to **Packages** from the left navigation pane.</span></span>

    <span data-ttu-id="ea4b1-203">オファー作成者が使用できる、有効なパッケージ テンプレートのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-203">A list of active package templates that are available for offer creators to use is displayed.</span></span>

1.  <span data-ttu-id="ea4b1-204">新しいオファー パッケージを作成するには、**新しいパッケージ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-204">To create a new offer package, click **New Package**.</span></span>

1.  <span data-ttu-id="ea4b1-205">一意の名前を入力し、**作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-205">Enter a unique name and click **Create**.</span></span>

1.  <span data-ttu-id="ea4b1-206">**テンプレートの追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-206">Click **Add template**.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="ea4b1-207">新しいテンプレートを作成するか、既存のテンプレートから選択するかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-207">You can choose to create a new template or choose from an existing one.</span></span>

    > - <span data-ttu-id="ea4b1-208">既存のテンプレートを追加する場合は、オファー ドキュメント テンプレートが保存され、確定され、有効とマークされていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-208">If you choose to add an existing template, you need to make sure that the   offer document template was saved, finalized, and marked as   active.</span></span>
    
    > - <span data-ttu-id="ea4b1-209">ドキュメント テンプレートを必要なだけ選択することができます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-209">You can choose as many document templates as you want.</span></span> 
    
1.  <span data-ttu-id="ea4b1-210">**完了**をクリックし、**パッケージ管理**に戻ります。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-210">Click **Done** to return to **Package management**.</span></span>

    <span data-ttu-id="ea4b1-211">ドキュメントの順序を設定したり、オファー作成中に特定のオファー ドキュメントが必要かどうかをマークすることもできます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-211">You can configure the sequence of the documents and also mark whether the specific offer document is required during offer creation.</span></span> <span data-ttu-id="ea4b1-212">オファー作成者には、**不要**とマークされているドキュメントを削除するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-212">The offer creator will have an option to delete the documents marked as **Not required**.</span></span>

1. <span data-ttu-id="ea4b1-213">オファー パッケージ テンプレートを保存し、すべてのオファー作成者がそれを使用できるようにするためには、**保存して公開**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-213">To save the offer package template so that it's usable by all offer creators, click **Save and publish**.</span></span>

   <span data-ttu-id="ea4b1-214">ドラフト オファー パッケージ テンプレートを表示するには、**ドラフト** タブに移動します。オファー パッケージ テンプレートに変更が加えられた場合は、保存し再公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-214">To view draft offer package templates, go to the **Drafts** tab. If a change is made to the offer package template, it must be  saved and republished.</span></span>

## <a name="configure-an-offer-process"></a><span data-ttu-id="ea4b1-215">オファー プロセスのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="ea4b1-215">Configure an offer process</span></span>

<span data-ttu-id="ea4b1-216">Attract 管理者によって設定可能なオファー作成プロセスの部分がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-216">There are several parts of the offer creation process that can be configured by an Attract administrator.</span></span>

- <span data-ttu-id="ea4b1-217">**オファーの承認** - オファーが候補者に送付される前にオファーの承認が必要かどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-217">**Offer approvals** - Choose whether offer approvals are required before the offer can be sent to the candidate.</span></span> <span data-ttu-id="ea4b1-218">管理者は、すべてのオファー承認を順次または並列な承認ワークフローで行うかどうかを決定することもできます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-218">As an administrator, you can also decide whether all offer approvals will happen in a sequential manner or parallel approval workflow.</span></span> <span data-ttu-id="ea4b1-219">オファーの承認者が、オファーの承認とともにコメントを追加する必要があるかどうかを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-219">You can also mandate whether offer approvers must add a comment along with their offer approval.</span></span> <span data-ttu-id="ea4b1-220">すべての非標準のオファーには、オファーの承認が必須です。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-220">Offer approvals are mandatory for all non-standard offers.</span></span>

- <span data-ttu-id="ea4b1-221">**候補者のオファー エクスペリエンス** - 管理者は、すべてのオファーに有効期限を設定するかどうかを決定することができます。有効期限を設定する場合は、有効期限の既定のオフセットを設定します。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-221">**Candidate’s offer experience** - As administrator, you can choose to set whether all offers have an expiration date, and if so, what the default offset for the expiration date should be.</span></span> <span data-ttu-id="ea4b1-222">候補者がオファーを拒否できるかどうかも設定することができます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-222">You can also configure whether candidates can decline an offer.</span></span>

- <span data-ttu-id="ea4b1-223">**電子署名** - 管理者として、候補者が署名に使用できる方法を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-223">**e-Signatures** - As an administrator, you can also choose the method that candidates can use to sign offers.</span></span>
    - <span data-ttu-id="ea4b1-224">Adobe Sign - すべてのオファー パッケージは、Adobe Sign 経由で送信および署名されます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-224">Adobe Sign - All offer packages will be sent and signed via Adobe Sign.</span></span> <span data-ttu-id="ea4b1-225">オファーを公開する各オファー作成者は、Adobe Sign アカウントを Attract に接続する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-225">Each offer creator publishing the offer needs to have their Adobe Sign account connected to Attract.</span></span> <span data-ttu-id="ea4b1-226">Adobe Sign ライセンスおよび無料試用版については、この[リンク](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-226">For Adobe Sign licenses and a free Trial, please visit this [link](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span></span>

    - <span data-ttu-id="ea4b1-227">DocuSign - すべてのオファー パッケージは、DocuSign 経由で送信および署名されます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-227">DocuSign - All offer packages will be sent and signed via DocuSign.</span></span> <span data-ttu-id="ea4b1-228">オファーを公開する各オファー作成者は、DocuSign アカウントを Attract に接続する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-228">Each offer creator publishing the offer needs to have their DocuSign account connected to Attract.</span></span> 
    
    - <span data-ttu-id="ea4b1-229">ESign - これは、すぐに使用できる既定のオプションで、ユーザーは名前とイニシャルを入力してオファーに署名することができます。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-229">ESign - This is the default option, provided out of the box, where the user can sign an offer by typing their name and initials.</span></span>


<span data-ttu-id="ea4b1-230">オファー作成プロセスの詳細については、[作成、承認、および署名](./creating-offers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ea4b1-230">To learn more about the offer creation process, see [Creating, approving, and signing offers](./creating-offers.md).</span></span>
