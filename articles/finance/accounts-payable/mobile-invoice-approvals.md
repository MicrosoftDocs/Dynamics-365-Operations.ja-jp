---
title: モバイルによる請求書承認
description: このトピックは、サポート案件としてモバイルのベンダー請求書の承認を取得することによる、モバイル シナリオを設計するための実際的なアプローチを提供することを目的としています。
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: abf5c2735834537fdc72f2e73fe6a415bd1b67c0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227525"
---
# <a name="mobile-invoice-approvals"></a><span data-ttu-id="7cf66-103">モバイルによる請求書承認</span><span class="sxs-lookup"><span data-stu-id="7cf66-103">Mobile invoice approvals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7cf66-104">モバイル機能により、ビジネス ユーザーはモバイル エクスペリエンスを設計できます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-104">Mobile capabilities let a business user design mobile experiences.</span></span> <span data-ttu-id="7cf66-105">高度なシナリオでは、開発者はプラットフォームを使用して、必要に応じて機能を拡張することもできます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="7cf66-106">モバイルに関する新しい概念のいくつかを学ぶ最も効果的な方法は、いくつかのシナリオを設計するプロセスを経ることです。</span><span class="sxs-lookup"><span data-stu-id="7cf66-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="7cf66-107">このトピックは、サポート案件としてモバイルのベンダー請求書の承認を取得することによる、モバイル シナリオを設計するための実際的なアプローチを提供することを目的としています。</span><span class="sxs-lookup"><span data-stu-id="7cf66-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="7cf66-108">このトピックは、シナリオのさまざまなバリエーションを設計するのに役立ちますが、仕入先請求書に関連しない他のシナリオにも適用できます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="7cf66-109">前提条件</span><span class="sxs-lookup"><span data-stu-id="7cf66-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="7cf66-110">前提条件</span><span class="sxs-lookup"><span data-stu-id="7cf66-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="7cf66-111">説明</span><span class="sxs-lookup"><span data-stu-id="7cf66-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cf66-112">モバイル ハンドブックの先行読取</span><span class="sxs-lookup"><span data-stu-id="7cf66-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="7cf66-113">モバイル プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="7cf66-113">Mobile platform</span></span>](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="7cf66-114">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="7cf66-114">Dynamics 365 Finance</span></span>                                                                              | <span data-ttu-id="7cf66-115">バージョン 1611 およびプラットフォーム更新プログラム 3 (2016 年 11 月) がある環境</span><span class="sxs-lookup"><span data-stu-id="7cf66-115">An environment that has version 1611 and Platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="7cf66-116">更新プログラム KB 3204341 をインストールします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="7cf66-117">タスク レコーダーは誤って 2 つのドロップダウン ダイアログの Close コマンドを記録できます。これはプラットフォーム更新プログラム 3 (2016 年 11 月の更新プログラム) に含まれています。</span><span class="sxs-lookup"><span data-stu-id="7cf66-117">Task recorder can erroneously record two Close commands for dropdown dialogs; this is included in Platform update 3 (November 2016 update).</span></span> |
| <span data-ttu-id="7cf66-118">更新プログラム KB 3207800 をインストールします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="7cf66-119">この修正プログラムは、モバイル クライアント上で表示される添付ファイルを有効にします。これはプラットフォーム更新プログラム 3 (2016 年 11 月の更新プログラム) に含まれています。</span><span class="sxs-lookup"><span data-stu-id="7cf66-119">This hotfix enables attachments to be viewed on the mobile client; this is included in Platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="7cf66-120">更新プログラム KB 3208224 をインストールします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="7cf66-121">モバイルの仕入先請求書承認アプリケーションのアプリケーション コードです。これはバージョン 7.0.1 (2016 年 5 月) に含まれています。</span><span class="sxs-lookup"><span data-stu-id="7cf66-121">Application code for the mobile vendor invoice approval application; this is included in version 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="7cf66-122">モバイル アプリがインストールされている Android、iOS または Windows デバイス。</span><span class="sxs-lookup"><span data-stu-id="7cf66-122">An Android or iOS or a Windows device that has the mobile app installed.</span></span> | <span data-ttu-id="7cf66-123">適切なアプリ ストアでアプリを検索します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="7cf66-124">はじめに</span><span class="sxs-lookup"><span data-stu-id="7cf66-124">Introduction</span></span>
<span data-ttu-id="7cf66-125">ベンダー請求書のモバイル承認には、「前提条件」セクションに記載されている 3 つの修正プログラムが必要です。</span><span class="sxs-lookup"><span data-stu-id="7cf66-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="7cf66-126">これらの修正プログラムは、請求書承認のためのワークスペースを提供しません。</span><span class="sxs-lookup"><span data-stu-id="7cf66-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="7cf66-127">ワークスペースがモバイルのコンテキストでどのようなものかを知るには、「前提条件」セクションで説明したモバイル ハンドブックをお読みください。</span><span class="sxs-lookup"><span data-stu-id="7cf66-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="7cf66-128">請求書承認ワークスペースを設計する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cf66-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="7cf66-129">すべての組織は、ベンダー請求書の異なるビジネス プロセスを調整し定義します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="7cf66-130">ベンダーの請求書承認のためのモバイル エクスペリエンスを設計する前に、ビジネス プロセスの次の側面を考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cf66-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="7cf66-131">このアイデアは、これらのデータ ポイントを可能な限り使用して、デバイス上のユーザー エクスペリエンスを最適化することです。</span><span class="sxs-lookup"><span data-stu-id="7cf66-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="7cf66-132">モバイル エクスペリエンスで、請求書ヘッダーのどのフィールドを、どのような順序で表示したいですか?</span><span class="sxs-lookup"><span data-stu-id="7cf66-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="7cf66-133">モバイル エクスペリエンスで、請求書行のどのフィールドを、どのような順序で表示したいですか?</span><span class="sxs-lookup"><span data-stu-id="7cf66-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="7cf66-134">請求書にはいくつの請求書明細行がありますか?</span><span class="sxs-lookup"><span data-stu-id="7cf66-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="7cf66-135">80-20 ルールをここで適用し、80 パーセントを最適化します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="7cf66-136">ユーザーは、レビュー中にモバイル デバイス上の勘定配賦 (請求書コーディング) を見たいでしょうか?</span><span class="sxs-lookup"><span data-stu-id="7cf66-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="7cf66-137">この質問に対する回答が「はい」の場合は、次の質問を検討してください。</span><span class="sxs-lookup"><span data-stu-id="7cf66-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="7cf66-138">請求書行にはいくつの勘定配賦 (拡張価格、消費税、料金、分割など) がありますか?</span><span class="sxs-lookup"><span data-stu-id="7cf66-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="7cf66-139">再度、80-20 ルールを適用します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="7cf66-140">請求書には請求書ヘッダーに勘定配賦も含まれていますか?</span><span class="sxs-lookup"><span data-stu-id="7cf66-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="7cf66-141">もしそうなら、これらの勘定配賦はデバイス上で利用できるはずですか?</span><span class="sxs-lookup"><span data-stu-id="7cf66-141">If so, should these accounting distributions be available on the device?</span></span>

    > [!NOTE]
    > <span data-ttu-id="7cf66-142">このトピックでは、現在モバイル シナリオでこの機能がサポートされていないため、勘定配賦の編集方法については説明していません。</span><span class="sxs-lookup"><span data-stu-id="7cf66-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="7cf66-143">ユーザーはデバイス上の請求書の添付ファイルを見たいですか?</span><span class="sxs-lookup"><span data-stu-id="7cf66-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="7cf66-144">請求書承認のためのモバイル エクスペリエンスの設計は、これらの質問に対する回答によって異なります。</span><span class="sxs-lookup"><span data-stu-id="7cf66-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="7cf66-145">その目的は、組織内のモバイルでのビジネス プロセスのユーザー エクスペリエンスを最適化することです。</span><span class="sxs-lookup"><span data-stu-id="7cf66-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="7cf66-146"> このトピックの残りでは、前述の質問とは異なる回答に基づいた 2 つのシナリオのバリエーションを見ていきます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="7cf66-147">一般的なガイダンスとして、モバイル デザイナーと協力している場合は、アップデートを失わないように変更を「公開」してください。</span><span class="sxs-lookup"><span data-stu-id="7cf66-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="7cf66-148">Contoso の簡単な請求書承認シナリオの設計</span><span class="sxs-lookup"><span data-stu-id="7cf66-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7cf66-149">シナリオの属性</span><span class="sxs-lookup"><span data-stu-id="7cf66-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="7cf66-150">応答</span><span class="sxs-lookup"><span data-stu-id="7cf66-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7cf66-151">モバイル エクスペリエンスで、請求書ヘッダーのどのフィールドを、どのような順序で表示したいですか?</span><span class="sxs-lookup"><span data-stu-id="7cf66-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="7cf66-152">仕入先名</span><span class="sxs-lookup"><span data-stu-id="7cf66-152">Vendor name</span></span></li>
<li><span data-ttu-id="7cf66-153">請求合計</span><span class="sxs-lookup"><span data-stu-id="7cf66-153">Invoice total</span></span></li>
<li><span data-ttu-id="7cf66-154">請求先/元 ID</span><span class="sxs-lookup"><span data-stu-id="7cf66-154">Invoice account</span></span></li>
<li><span data-ttu-id="7cf66-155">請求書番号</span><span class="sxs-lookup"><span data-stu-id="7cf66-155">Invoice number</span></span></li>
<li><span data-ttu-id="7cf66-156">請求日</span><span class="sxs-lookup"><span data-stu-id="7cf66-156">Invoice date</span></span></li>
<li><span data-ttu-id="7cf66-157">請求明細</span><span class="sxs-lookup"><span data-stu-id="7cf66-157">Invoice description</span></span></li>
<li><span data-ttu-id="7cf66-158">期日</span><span class="sxs-lookup"><span data-stu-id="7cf66-158">Due date</span></span></li>
<li><span data-ttu-id="7cf66-159">請求書通貨</span><span class="sxs-lookup"><span data-stu-id="7cf66-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cf66-160">モバイル エクスペリエンスで、請求書行のどのフィールドを、どのような順序で表示したいですか?</span><span class="sxs-lookup"><span data-stu-id="7cf66-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="7cf66-161">調達カテゴリ</span><span class="sxs-lookup"><span data-stu-id="7cf66-161">Procurement category</span></span></li>
<li><span data-ttu-id="7cf66-162">件数</span><span class="sxs-lookup"><span data-stu-id="7cf66-162">Quantity</span></span></li>
<li><span data-ttu-id="7cf66-163">単価</span><span class="sxs-lookup"><span data-stu-id="7cf66-163">Unit price</span></span></li>
<li><span data-ttu-id="7cf66-164">明細行の正味金額</span><span class="sxs-lookup"><span data-stu-id="7cf66-164">Line net amount</span></span></li>
<li><span data-ttu-id="7cf66-165">1099 金額</span><span class="sxs-lookup"><span data-stu-id="7cf66-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cf66-166">請求書にはいくつの請求書明細行がありますか?</span><span class="sxs-lookup"><span data-stu-id="7cf66-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="7cf66-167">80-20 ルールをここで適用し、80 パーセントを最適化します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="7cf66-168">1</span><span class="sxs-lookup"><span data-stu-id="7cf66-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cf66-169">ユーザーは、レビュー中にモバイル デバイス上の勘定配賦 (請求書コーディング) を見たいでしょうか?</span><span class="sxs-lookup"><span data-stu-id="7cf66-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="7cf66-170">有</span><span class="sxs-lookup"><span data-stu-id="7cf66-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cf66-171">請求書行にはいくつの勘定配賦 (拡張価格、消費税、料金、など) がありますか?</span><span class="sxs-lookup"><span data-stu-id="7cf66-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="7cf66-172">再度、80-20 ルールを適用します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="7cf66-173">拡張価格: 2 売上税: 0 料金: 0</span><span class="sxs-lookup"><span data-stu-id="7cf66-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cf66-174">請求書には請求書ヘッダーに勘定配賦も含まれていますか?</span><span class="sxs-lookup"><span data-stu-id="7cf66-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="7cf66-175">もしそうなら、これらの勘定配賦はデバイス上で利用できるはずですか?</span><span class="sxs-lookup"><span data-stu-id="7cf66-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="7cf66-176">不使用</span><span class="sxs-lookup"><span data-stu-id="7cf66-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cf66-177">ユーザーはデバイス上の請求書の添付ファイルを見たいですか?</span><span class="sxs-lookup"><span data-stu-id="7cf66-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="7cf66-178">はい</span><span class="sxs-lookup"><span data-stu-id="7cf66-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="7cf66-179">ワークスペースの作成</span><span class="sxs-lookup"><span data-stu-id="7cf66-179">Create the workspace</span></span>

1.  <span data-ttu-id="7cf66-180">ブラウザーで、アプリケーションにログインします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-180">In a browser, and sign in to the application.</span></span>
2.  <span data-ttu-id="7cf66-181">サインインした後、次の例のように **&mode=mobile** を URL に追加し、ページを更新します: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="7cf66-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span></span>
3.  <span data-ttu-id="7cf66-182">ページの右上角にある **設定** (歯車) ボタンをクリックし、次に **モバイル アプリ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="7cf66-183">モバイル アプリのデザイナーは、タスク レコーダーが表示されるのと同じように表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cf66-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="7cf66-184">新しいワークスペース作成するには、**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="7cf66-185">この例として、ワークスペースを **自分の承認** と名付けます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="7cf66-186">説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-186">Enter a description.</span></span>
6.  <span data-ttu-id="7cf66-187">ワークスペースの色を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-187">Select a workspace color.</span></span> <span data-ttu-id="7cf66-188">ワークスペースの色は、このワークスペースのモバイル エクスペリエンスの全体的なスタイルに使用されます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="7cf66-189">ワークスペースのアイコンを選択します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="7cf66-190">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-190">Click **Done**</span></span>
9.  <span data-ttu-id="7cf66-191">変更を保存するには、**ワークスペースを公開** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="7cf66-192">自分に割り当てられている仕入先請求書</span><span class="sxs-lookup"><span data-stu-id="7cf66-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="7cf66-193">設計する必要がある最初のモバイル ページは、レビューのためにユーザーに割り当てられている請求書の一覧です。</span><span class="sxs-lookup"><span data-stu-id="7cf66-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="7cf66-194">このモバイル ページを設計するには、**VendMobileInvoiceAssignedToMeListPage** ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page.</span></span> <span data-ttu-id="7cf66-195">この手順を完了する前に、少なくとも 1 つの仕入先請求書がレビューのために割り当てられていること、および請求書行に 2 つの配布があることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7cf66-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="7cf66-196">この設定は、このシナリオの要件を満たしています。</span><span class="sxs-lookup"><span data-stu-id="7cf66-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="7cf66-197">URL で、メニューの名前を **VendMobileInvoiceAssignedToMeListPage** に置き換え、**買掛金勘定** モジュールの **私に割り当てられた保留中の仕入先請求書** リスト ページのモバイル版を開きます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-197">In the URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="7cf66-198">システムに割り当てられている請求書の数に応じて、このページにこれらの請求書が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="7cf66-199">特定の請求書を検索するには、左側のフィルターを使用します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="7cf66-200">ただし、この例では特定の請求書は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="7cf66-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="7cf66-201">割り当てられた請求書を要求するだけで、モバイル ページをデザインすることができます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="7cf66-202">利用可能な新しいページは、ベンダーの請求書のモバイル シナリオを開発するために特別に設計されています。</span><span class="sxs-lookup"><span data-stu-id="7cf66-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="7cf66-203">したがって、これらのページを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cf66-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="7cf66-204">URL は次の URL のようになります。また、入力後、図に示されているページが表示されます: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span><span class="sxs-lookup"><span data-stu-id="7cf66-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span></span> 

    <span data-ttu-id="7cf66-205">[![自分に割り当てられた保留中の仕入先請求書ページ](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="7cf66-205">[![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
    
2.  <span data-ttu-id="7cf66-206">ページの右上角にある **設定** (歯車) ボタンをクリックし、次に **モバイル アプリ** をクリックします</span><span class="sxs-lookup"><span data-stu-id="7cf66-206">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="7cf66-207">ワークスペースを選択し、**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-207">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="7cf66-208">**ページを追加** をクリックして、最初のモバイル ページを作成します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-208">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="7cf66-209">**私のベンダーの請求書** などの名前と、**レビュー用に割り当てられたベンダーの請求書** などの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-209">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="7cf66-210">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-210">Click **Done**.</span></span>
7.  <span data-ttu-id="7cf66-211">モバイル デザイナーの **フィールド** タブで **フィールドの選択** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-211">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="7cf66-212">リスト ページの列は、次の図のようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cf66-212">The columns on the list page must resemble the following illustration.</span></span> 

    <span data-ttu-id="7cf66-213">[![自分に割り当てられた保留中の仕入先請求書ページ](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="7cf66-213">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
    
8.  <span data-ttu-id="7cf66-214">リスト ページから、モバイル ページのユーザーに表示する必要がある列を追加します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-214">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="7cf66-215">追加する順序は、フィールドがエンド ユーザーに表示される順序です。</span><span class="sxs-lookup"><span data-stu-id="7cf66-215">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="7cf66-216">フィールドの順序を変更する唯一の方法は、すべてのフィールドを再選択することです。</span><span class="sxs-lookup"><span data-stu-id="7cf66-216">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="7cf66-217">このシナリオの要件に基づいて、次の 8 つのフィールドが必要です。</span><span class="sxs-lookup"><span data-stu-id="7cf66-217">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="7cf66-218">しかし、一部のユーザは、8 つのフィールドが多くの情報をモバイル デバイス上に持つと考える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7cf66-218">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="7cf66-219">したがって、モバイル リスト ビューで最も重要なフィールドのみを表示します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-219">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="7cf66-220">残りのフィールドは、後で設計する詳細ビューに表示されます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-220">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="7cf66-221">今のところ、次のフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-221">For now, we will add the following fields.</span></span> <span data-ttu-id="7cf66-222">モバイル ページに追加するには、これらの列のプラス記号 (**+**) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-222">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="7cf66-223">仕入先名</span><span class="sxs-lookup"><span data-stu-id="7cf66-223">Vendor name</span></span>
    - <span data-ttu-id="7cf66-224">請求合計</span><span class="sxs-lookup"><span data-stu-id="7cf66-224">Invoice total</span></span>
    - <span data-ttu-id="7cf66-225">請求先/元 ID</span><span class="sxs-lookup"><span data-stu-id="7cf66-225">Invoice account</span></span>
    - <span data-ttu-id="7cf66-226">請求書番号</span><span class="sxs-lookup"><span data-stu-id="7cf66-226">Invoice number</span></span>
    - <span data-ttu-id="7cf66-227">請求日</span><span class="sxs-lookup"><span data-stu-id="7cf66-227">Invoice date</span></span>

    <span data-ttu-id="7cf66-228">フィールドが追加されると、モバイル ページは次の図のようになります。</span><span class="sxs-lookup"><span data-stu-id="7cf66-228">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    
    <span data-ttu-id="7cf66-229">[![フィールドの後ページが表示される](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="7cf66-229">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>

9.  <span data-ttu-id="7cf66-230">ワークフロー アクションを後で有効にできるように、次の列も追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cf66-230">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="7cf66-231">完了したタスクを表示する</span><span class="sxs-lookup"><span data-stu-id="7cf66-231">Show complete task</span></span>
    - <span data-ttu-id="7cf66-232">委任タスクを表示する</span><span class="sxs-lookup"><span data-stu-id="7cf66-232">Show delegate task</span></span>
    - <span data-ttu-id="7cf66-233">リコールタスクを表示する</span><span class="sxs-lookup"><span data-stu-id="7cf66-233">Show recall task</span></span>
    - <span data-ttu-id="7cf66-234">拒否タスクを表示する</span><span class="sxs-lookup"><span data-stu-id="7cf66-234">Show reject task</span></span>
    - <span data-ttu-id="7cf66-235">リクエスト完了タスクを表示する</span><span class="sxs-lookup"><span data-stu-id="7cf66-235">Show request completion task</span></span>
    - <span data-ttu-id="7cf66-236">再送信タスクを表示する</span><span class="sxs-lookup"><span data-stu-id="7cf66-236">Show resubmit task</span></span>

10. <span data-ttu-id="7cf66-237">**完了** をクリックして、編集モードを終了します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-237">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="7cf66-238">**戻る**、次に **完了** をクリックして、ワークスペースを終了します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-238">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="7cf66-239">**ワークスペースの公開** をクリックして作業を保存します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-239">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="7cf66-240">**請求書** の買掛金勘定パラメータ フォームの **仕入先請求書一覧の請求書総額の表示** を有効化します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-240">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="7cf66-241">このパラメータを有効にすることによってのみ、請求書合計が計算され、保留中の仕入先請求一覧ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-241">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="7cf66-242">これは前提条件の修正プログラム 3208224 の一部の新しい機能です。</span><span class="sxs-lookup"><span data-stu-id="7cf66-242">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="7cf66-243">ベンダー請求書の詳細</span><span class="sxs-lookup"><span data-stu-id="7cf66-243">Vendor invoice details</span></span>

<span data-ttu-id="7cf66-244">モバイル用の請求書の詳細ページを設計するには、**VendMobileInvoiceHeaderDetails** ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-244">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="7cf66-245">システムに登録されている請求書の数に応じて、このページには最も古い請求書（最初に作成された請求書）が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-245">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="7cf66-246">特定の請求書を検索するには、左側のフィルターを使用します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-246">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="7cf66-247">ただし、この例では特定の請求書は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="7cf66-247">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="7cf66-248">モバイルページを設計できるように、請求書データが必要です。</span><span class="sxs-lookup"><span data-stu-id="7cf66-248">We just require some invoice data so that we can design the mobile page.</span></span> 

<span data-ttu-id="7cf66-249">[![ワークフロー ページ](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="7cf66-249">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1. <span data-ttu-id="7cf66-250">URL で、メニュー アイテムの名前を **VendMobileInvoiceHeaderDetails** に置き換えてフォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-250">In the URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>

2. <span data-ttu-id="7cf66-251">**設定** (ギア) ボタンからモバイル デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-251">Open the mobile designer from the **Settings** (gear) button.</span></span>

3. <span data-ttu-id="7cf66-252">ワークスペースで編集モードを開始するには、**編集** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-252">Click the **Edit** button to start edit mode in the workspace.</span></span>

4. <span data-ttu-id="7cf66-253">前に作成した **私のベンダーの請求書** ページを選択して、それから **編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-253">Select the **My vendor invoices** page that you created earlier, and then click **Edit**.</span></span>

5. <span data-ttu-id="7cf66-254">**フィールド** タブで、**グリッド** 列見出しをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-254">On the **Fields** tab, click the **Grid** column heading.</span></span>

6. <span data-ttu-id="7cf66-255">**プロパティ &gt; ページの追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-255">Click **Properties &gt; Add page**.</span></span> <span data-ttu-id="7cf66-256">**注:** **グリッド** 見出しをクリックしてページを追加すると、詳細ページとの関係が自動的に確立されます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-256">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>

7. <span data-ttu-id="7cf66-257">**請求書の詳細** などのページタイトルと、**請求書ヘッダーと行の詳細の表示** などの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-257">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>

8. <span data-ttu-id="7cf66-258">**フィールドの選択** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-258">Click **Select fields**.</span></span> <span data-ttu-id="7cf66-259">追加する順序は、フィールドがエンド ユーザーに表示される順序に留意してください。</span><span class="sxs-lookup"><span data-stu-id="7cf66-259">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="7cf66-260">フィールドの順序を変更する唯一の方法は、すべてのフィールドを再選択することです。</span><span class="sxs-lookup"><span data-stu-id="7cf66-260">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 

9. <span data-ttu-id="7cf66-261">このシナリオの要件に基づいて、ヘッダーから次のフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-261">Add the following fields from the header, based on the requirements for this scenario:</span></span>
   - <span data-ttu-id="7cf66-262">仕入先名</span><span class="sxs-lookup"><span data-stu-id="7cf66-262">Vendor name</span></span>
   - <span data-ttu-id="7cf66-263">請求合計</span><span class="sxs-lookup"><span data-stu-id="7cf66-263">Invoice total</span></span>
   - <span data-ttu-id="7cf66-264">請求先/元 ID</span><span class="sxs-lookup"><span data-stu-id="7cf66-264">Invoice account</span></span>
   - <span data-ttu-id="7cf66-265">請求書番号</span><span class="sxs-lookup"><span data-stu-id="7cf66-265">Invoice number</span></span>
   - <span data-ttu-id="7cf66-266">請求日</span><span class="sxs-lookup"><span data-stu-id="7cf66-266">Invoice date</span></span>
   - <span data-ttu-id="7cf66-267">請求明細</span><span class="sxs-lookup"><span data-stu-id="7cf66-267">Invoice description</span></span>
   - <span data-ttu-id="7cf66-268">期日</span><span class="sxs-lookup"><span data-stu-id="7cf66-268">Due date</span></span>
   - <span data-ttu-id="7cf66-269">請求書通貨</span><span class="sxs-lookup"><span data-stu-id="7cf66-269">Invoice currency</span></span>

10. <span data-ttu-id="7cf66-270">ページの行グリッドから次のフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-270">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="7cf66-271">調達カテゴリ</span><span class="sxs-lookup"><span data-stu-id="7cf66-271">Procurement category</span></span>
    - <span data-ttu-id="7cf66-272">件数</span><span class="sxs-lookup"><span data-stu-id="7cf66-272">Quantity</span></span>
    - <span data-ttu-id="7cf66-273">単価</span><span class="sxs-lookup"><span data-stu-id="7cf66-273">Unit price</span></span>
    - <span data-ttu-id="7cf66-274">明細行の正味金額</span><span class="sxs-lookup"><span data-stu-id="7cf66-274">Line net amount</span></span>
    - <span data-ttu-id="7cf66-275">1099 金額</span><span class="sxs-lookup"><span data-stu-id="7cf66-275">1099 amount</span></span>

11. <span data-ttu-id="7cf66-276">前の 2 つの手順のすべてのフィールドが追加されたら、**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-276">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="7cf66-277">ページは次の図のようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cf66-277">The page must resemble the following illustration.</span></span>
    
    <span data-ttu-id="7cf66-278">[![フィールドの後ページが表示される](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="7cf66-278">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>

12. <span data-ttu-id="7cf66-279">**完了** をクリックして、編集モードを終了します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-279">Click **Done** to exit edit mode.</span></span>

13. <span data-ttu-id="7cf66-280">**戻る**、次に **完了** をクリックして、ワークスペースを終了します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-280">Click **Back** and then **Done** to exit the workspace</span></span>

14. <span data-ttu-id="7cf66-281">**ワークスペースの公開** をクリックして作業を保存します</span><span class="sxs-lookup"><span data-stu-id="7cf66-281">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="7cf66-282">ワークフロー アクション</span><span class="sxs-lookup"><span data-stu-id="7cf66-282">Workflow actions</span></span>

<span data-ttu-id="7cf66-283">ワークフロー アクションを追加するには、**VendMobileInvoiceHeaderDetails** ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-283">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="7cf66-284">このページを開くには、先ほどと同様に、URL 内のメニュー項目の名前を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-284">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="7cf66-285">次に、**設定** (ギア) ボタンからモバイル デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-285">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="7cf66-286"> 詳細ページにワークフロー アクションを追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7cf66-286">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="7cf66-287">ワークフローアクションを利用できるようにするため、請求書は適切な状態で割り当てられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cf66-287">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="7cf66-288">ワークフロー アクションを記録</span><span class="sxs-lookup"><span data-stu-id="7cf66-288">Record workflow actions</span></span>
1.  <span data-ttu-id="7cf66-289">ワークスペースで編集モードを開始するには、**編集** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-289">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="7cf66-290">前に作成した **請求書の詳細** ページを選択し、**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-290">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="7cf66-291">**アクション** タブで、**アクションの 追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-291">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="7cf66-292">**承認** などのアクションタイトルと、**請求書の承認** などの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-292">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="7cf66-293">ここに入力するアクション タイトルは、モバイル アプリでユーザーに表示されるアクションの名前になります。</span><span class="sxs-lookup"><span data-stu-id="7cf66-293">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="7cf66-294">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-294">Click **Done**.</span></span>
6.  <span data-ttu-id="7cf66-295">**フィールドの選択** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-295">Click **Select fields**.</span></span>
7.  <span data-ttu-id="7cf66-296">**VendMobileInvoiceHeaderDetails** ページのワークフロー プロセスを実行し、記録するアクションを完了します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-296">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="7cf66-297">このプロセス中にワークフロー コメントを入力して、コメント フィールドもモバイル エクスペリエンスに含めるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="7cf66-297">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="7cf66-298">ワークフロー アクションの実行後、**完了** をクリックしてフィールドの選択タスクを完了します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-298">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="7cf66-299">**完了** をクリックして、編集モードを終了します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-299">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="7cf66-300">**戻る**、次に **完了** をクリックして、ワークスペースを終了します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-300">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="7cf66-301">**ワークスペースの公開** をクリックして作業を保存します</span><span class="sxs-lookup"><span data-stu-id="7cf66-301">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="7cf66-302">必要なすべてのワークフロー アクションを記録するには、前の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-302">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="7cf66-303">.js ファイルの作成</span><span class="sxs-lookup"><span data-stu-id="7cf66-303">Create a .js file</span></span>
1. <span data-ttu-id="7cf66-304">メモ帳または Microsoft Visual Studio を開き、次のコードを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-304">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="7cf66-305">ファイルを .js ファイルとして保存します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-305">Save the file as a .js file.</span></span> <span data-ttu-id="7cf66-306">このコードを使い、次の処理を行います。</span><span class="sxs-lookup"><span data-stu-id="7cf66-306">This code does the following:</span></span>
    - <span data-ttu-id="7cf66-307">以前にモバイル リスト ページに追加した追加のワークフロー関連の列は非表示になっています。</span><span class="sxs-lookup"><span data-stu-id="7cf66-307">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="7cf66-308">アプリケーションがコンテキスト内にその情報を持ち、次のステップを実行できるように、これらの列を追加しました。</span><span class="sxs-lookup"><span data-stu-id="7cf66-308">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="7cf66-309">アクティブなワークフロー ステップに基づいて、それらのアクションのみを表示するロジックが適用されます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-309">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7cf66-310">コード内のページおよび他のコントロールの名前は、ワークスペース内で同じ名前でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="7cf66-310">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }
    ```

2.  <span data-ttu-id="7cf66-311">**ロジック** タブを選択して、コード ファイルをワークスペースにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-311">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="7cf66-312">**完了** をクリックして、編集モードを終了します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-312">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="7cf66-313">**戻る**、次に **完了** をクリックして、ワークスペースを終了します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-313">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="7cf66-314">**ワークスペースの公開** をクリックして作業を保存します</span><span class="sxs-lookup"><span data-stu-id="7cf66-314">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="7cf66-315">ベンダー請求書の添付</span><span class="sxs-lookup"><span data-stu-id="7cf66-315">Vendor invoice attachments</span></span>

1. <span data-ttu-id="7cf66-316">ページの右上角にある **設定** (歯車) ボタンをクリックし、次に **モバイル アプリ** をクリックします</span><span class="sxs-lookup"><span data-stu-id="7cf66-316">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>

2. <span data-ttu-id="7cf66-317">ワークスペースで編集モードを開始するには、**編集** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-317">Click the **Edit** button to start edit mode in the workspace.</span></span>

3. <span data-ttu-id="7cf66-318"><strong>前に作成した請求書の詳細 **ページを選択し、それから**編集</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-318">Select the <strong>Invoice details \*\*page that you created earlier, and then click \*\*Edit</strong>.</span></span>

4. <span data-ttu-id="7cf66-319">以下のように、**文書管理** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-319">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="7cf66-320">**注:** モバイル デバイスに添付ファイルを表示する必要がない場合は、このオプションをデフォルト設定の **いいえ** に設定しておくことができます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-320">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
   
   ![ドキュメント管理](./media/docmanagement-216x300.png)

5. <span data-ttu-id="7cf66-322">**完了** をクリックして、編集モードを終了します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-322">Click **Done** to exit edit mode.</span></span>

6. <span data-ttu-id="7cf66-323">**戻る**、次に **完了** をクリックして、ワークスペースを終了します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-323">Click **Back** and then **Done** to exit the workspace</span></span>

7. <span data-ttu-id="7cf66-324">**ワークスペースの公開** をクリックして作業を保存します</span><span class="sxs-lookup"><span data-stu-id="7cf66-324">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="7cf66-325">ベンダー請求書行の配布</span><span class="sxs-lookup"><span data-stu-id="7cf66-325">Vendor invoice line distributions</span></span>

<span data-ttu-id="7cf66-326">このシナリオの要件により、行レベルの配布のみが存在し、請求書には常に 1 行しか含まれないことが確認されます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-326">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="7cf66-327">このシナリオは単純なので、モバイル デバイスのユーザー エクスペリエンスは、配布を表示するためにユーザーが複数のレベルをドリルダウンする必要がないほど単純でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="7cf66-327">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="7cf66-328">仕入先請求書は、請求書のヘッダーからすべての配布を表示するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="7cf66-328">Vendor invoices include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="7cf66-329">この経験は、モバイル シナリオに必要なものです。</span><span class="sxs-lookup"><span data-stu-id="7cf66-329">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="7cf66-330">したがって、**VendMobileInvoiceAllDistributionTree** ページを使用してモバイル シナリオのこの部分を設計します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-330">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="7cf66-331">要件を知ることで、使用する特定のページと、シナリオを設計する際にユーザーのモバイル エクスペリエンスをどのように最適化するかを決定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-331">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="7cf66-332">2 番目のシナリオでは、そのシナリオの要件が異なるため、異なるページを使用して配布を表示します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-332">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="7cf66-333">URL で、前と同じように、メニュー項目の名前を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-333">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="7cf66-334">表示されるページは、次の図のようになります。</span><span class="sxs-lookup"><span data-stu-id="7cf66-334">The page that appears should resemble the following illustration.</span></span>

    <span data-ttu-id="7cf66-335">[![すべての配分ページ](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="7cf66-335">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>

2.  <span data-ttu-id="7cf66-336">**設定** (ギア) ボタンからモバイル デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-336">Open the mobile designer from the **Settings** (gear) button.</span></span>

3.  <span data-ttu-id="7cf66-337">ワークスペースで編集モードを開始するには、**編集** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-337">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="7cf66-338">**注:** 2 つの新しいページが自動的に作成されたことがわかります。</span><span class="sxs-lookup"><span data-stu-id="7cf66-338">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="7cf66-339">前のセクションでドキュメント管理を有効にしたため、システムがこれらのページを作成します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-339">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="7cf66-340">これらの新しいページは無視できます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-340">You can ignore these new pages.</span></span>

4.  <span data-ttu-id="7cf66-341">**ページの追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-341">Click **Add page**.</span></span>

5.  <span data-ttu-id="7cf66-342">**会計の表示** などのページ タイトルと、**請求書の会計の表示** などの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-342">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>

6.  <span data-ttu-id="7cf66-343">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-343">Click **Done**.</span></span>

7.  <span data-ttu-id="7cf66-344">**フィールド** タブで、**フィールドの選択** をクリックし、配布ページから次のフィールドを選択して、**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-344">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="7cf66-345">金額</span><span class="sxs-lookup"><span data-stu-id="7cf66-345">Amount</span></span>
    2.  <span data-ttu-id="7cf66-346">通貨</span><span class="sxs-lookup"><span data-stu-id="7cf66-346">Currency</span></span>
    3.  <span data-ttu-id="7cf66-347">勘定科目</span><span class="sxs-lookup"><span data-stu-id="7cf66-347">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="7cf66-348">このシナリオの要件では、拡張価格だけで配布が行われることが確認されているため、ディストリビューション グリッドから **説明** 列を選択しませんでした。</span><span class="sxs-lookup"><span data-stu-id="7cf66-348">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="7cf66-349">したがって、ユーザーは、その配信が対象とする金額タイプを決定するために別のフィールドを必要としません。</span><span class="sxs-lookup"><span data-stu-id="7cf66-349">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="7cf66-350">ただし、次のシナリオでは、このシナリオの要件によって、他の金額タイプに配賦 (たとえば、消費税) があることが指定されているため、この情報を使用 **します**。</span><span class="sxs-lookup"><span data-stu-id="7cf66-350">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>

8.  <span data-ttu-id="7cf66-351">**完了** をクリックして、編集モードを終了します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-351">Click **Done** to exit edit mode.</span></span>

9.  <span data-ttu-id="7cf66-352">**戻る**、次に **完了** をクリックして、ワークスペースを終了します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-352">Click **Back** and then **Done** to exit the workspace</span></span>

10. <span data-ttu-id="7cf66-353">**ワークスペースの公開** をクリックして作業を保存します</span><span class="sxs-lookup"><span data-stu-id="7cf66-353">Click **Publish workspace** to save your work</span></span>

#### <a name="adding-navigation-to-view-accounting-page"></a><span data-ttu-id="7cf66-354">「会計の表示」ページへのナビゲーションの追加</span><span class="sxs-lookup"><span data-stu-id="7cf66-354">Adding navigation to "View accounting" page</span></span>

<span data-ttu-id="7cf66-355">**会計の表示** モバイル ページは、現在のところ私たちが設計したモバイル ページのいずれにもリンクしていません。</span><span class="sxs-lookup"><span data-stu-id="7cf66-355">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="7cf66-356">ユーザーはモバイル デバイスの **請求書の詳細** ページから **会計の表示** ページに移動できる必要があるため、**請求書の詳細** ページから **会計の表示** ページまでのナビゲーションを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cf66-356">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="7cf66-357">このナビゲーションは JavaScript を介する追加のロジックを使用して確立します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-357">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="7cf66-358">前に作成した .js ファイルを開き、次のコードで強調表示されている行を追加します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-358">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="7cf66-359">このコードは 2 つのことを行います:</span><span class="sxs-lookup"><span data-stu-id="7cf66-359">This code does two things:</span></span>
    1.  <span data-ttu-id="7cf66-360">ユーザーがワークスペースから **会計の表示** ページに直接ナビゲートできないようにします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-360">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="7cf66-361">**請求書の詳細** ページから **会計の表示** ページへのナビゲーション制御を確立します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-361">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="7cf66-362">コード内のページおよび他のコントロールの名前は、ワークスペース内で同じ名前でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="7cf66-362">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }
    ```
    
2.  <span data-ttu-id="7cf66-363">前のコードを上書きするには、**ロジック** タブを選択してコード ファイルをワークスペースにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="7cf66-363">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="7cf66-364">**完了** をクリックして、編集モードを終了します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-364">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="7cf66-365">**戻る**、次に **完了** をクリックして、ワークスペースを終了します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-365">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="7cf66-366">**ワークスペースの公開** をクリックして作業を保存します</span><span class="sxs-lookup"><span data-stu-id="7cf66-366">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="7cf66-367">妥当性確認</span><span class="sxs-lookup"><span data-stu-id="7cf66-367">Validation</span></span>

<span data-ttu-id="7cf66-368">モバイル デバイスからアプリを開き、インスタンスに接続します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-368">From your mobile device, open the app, and connect to your instance.</span></span> <span data-ttu-id="7cf66-369">ベンダーの請求書が審査のために割り当てられている会社にサインインしてください。</span><span class="sxs-lookup"><span data-stu-id="7cf66-369">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="7cf66-370">次の操作を実行できるはずです:</span><span class="sxs-lookup"><span data-stu-id="7cf66-370">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="7cf66-371">**私の承認** ワークスペースを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7cf66-371">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="7cf66-372">**私の承認** ワークスペースをドリルインし、**私のベンダーの請求書** ページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7cf66-372">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="7cf66-373">**私のベンダーの請求書** ページをドリルインし、割り当てられた請求書の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-373">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="7cf66-374">請求書の 1 つをドリルインし、請求書ヘッダーの詳細と行の詳細を確認します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-374">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="7cf66-375">詳細ページで、添付ファイルへのリンクを参照し、このリンクを使用して添付ファイル リストに移動し、添付ファイルを表示します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-375">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="7cf66-376">詳細ページで、**会計の表示** ページへのリンクを参照し、このリンクを使用して配布ページに移動し、配布を表示します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-376">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="7cf66-377">詳細ページで、下部にある **操作** メニューをクリックし、ワークフロー ステップに該当するワークフロー アクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-377">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="7cf66-378">Fabrikam の複雑な請求書承認シナリオの設計</span><span class="sxs-lookup"><span data-stu-id="7cf66-378">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7cf66-379">シナリオの属性</span><span class="sxs-lookup"><span data-stu-id="7cf66-379">Scenario attribute</span></span></th>
<th><span data-ttu-id="7cf66-380">応答</span><span class="sxs-lookup"><span data-stu-id="7cf66-380">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7cf66-381">モバイル エクスペリエンスで、請求書ヘッダーのどのフィールドを、どのような順序で表示したいですか?</span><span class="sxs-lookup"><span data-stu-id="7cf66-381">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="7cf66-382">仕入先名</span><span class="sxs-lookup"><span data-stu-id="7cf66-382">Vendor name</span></span></li>
<li><span data-ttu-id="7cf66-383">請求金額</span><span class="sxs-lookup"><span data-stu-id="7cf66-383">Invoice amount</span></span></li>
<li><span data-ttu-id="7cf66-384">請求先/元 ID</span><span class="sxs-lookup"><span data-stu-id="7cf66-384">Invoice account</span></span></li>
<li><span data-ttu-id="7cf66-385">請求書番号</span><span class="sxs-lookup"><span data-stu-id="7cf66-385">Invoice number</span></span></li>
<li><span data-ttu-id="7cf66-386">請求日</span><span class="sxs-lookup"><span data-stu-id="7cf66-386">Invoice date</span></span></li>
<li><span data-ttu-id="7cf66-387">請求明細</span><span class="sxs-lookup"><span data-stu-id="7cf66-387">Invoice description</span></span></li>
<li><span data-ttu-id="7cf66-388">期日</span><span class="sxs-lookup"><span data-stu-id="7cf66-388">Due date</span></span></li>
<li><span data-ttu-id="7cf66-389">請求書通貨</span><span class="sxs-lookup"><span data-stu-id="7cf66-389">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cf66-390">モバイル エクスペリエンスで、請求書行のどのフィールドを、どのような順序で表示したいですか?</span><span class="sxs-lookup"><span data-stu-id="7cf66-390">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="7cf66-391">調達カテゴリ</span><span class="sxs-lookup"><span data-stu-id="7cf66-391">Procurement category</span></span></li>
<li><span data-ttu-id="7cf66-392">件数</span><span class="sxs-lookup"><span data-stu-id="7cf66-392">Quantity</span></span></li>
<li><span data-ttu-id="7cf66-393">単価</span><span class="sxs-lookup"><span data-stu-id="7cf66-393">Unit price</span></span></li>
<li><span data-ttu-id="7cf66-394">明細行の正味金額</span><span class="sxs-lookup"><span data-stu-id="7cf66-394">Line net amount</span></span></li>
<li><span data-ttu-id="7cf66-395">1099 金額</span><span class="sxs-lookup"><span data-stu-id="7cf66-395">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cf66-396">請求書にはいくつの請求書明細行がありますか?</span><span class="sxs-lookup"><span data-stu-id="7cf66-396">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="7cf66-397">80-20 ルールをここで適用し、80 パーセントを最適化します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-397">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="7cf66-398">5</span><span class="sxs-lookup"><span data-stu-id="7cf66-398">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cf66-399">ユーザーは、レビュー中にモバイル デバイス上の勘定配賦 (請求書コーディング) を見たいでしょうか?</span><span class="sxs-lookup"><span data-stu-id="7cf66-399">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="7cf66-400">有</span><span class="sxs-lookup"><span data-stu-id="7cf66-400">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cf66-401">請求書行にはいくつの勘定配賦 (拡張価格、消費税、料金、など) がありますか?</span><span class="sxs-lookup"><span data-stu-id="7cf66-401">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="7cf66-402">再度、80-20 ルールを適用します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-402">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="7cf66-403">拡張価格: 2 売上税: 2 料金: 2</span><span class="sxs-lookup"><span data-stu-id="7cf66-403">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cf66-404">請求書には請求書ヘッダーに勘定配賦も含まれていますか?</span><span class="sxs-lookup"><span data-stu-id="7cf66-404">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="7cf66-405">もしそうなら、これらの勘定配賦はデバイス上で利用できるはずですか?</span><span class="sxs-lookup"><span data-stu-id="7cf66-405">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="7cf66-406">不使用</span><span class="sxs-lookup"><span data-stu-id="7cf66-406">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cf66-407">ユーザーはデバイス上の請求書の添付ファイルを見たいですか?</span><span class="sxs-lookup"><span data-stu-id="7cf66-407">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="7cf66-408">有</span><span class="sxs-lookup"><span data-stu-id="7cf66-408">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="7cf66-409">次のステップ</span><span class="sxs-lookup"><span data-stu-id="7cf66-409">Next steps</span></span>

<span data-ttu-id="7cf66-410">シナリオ 2 の要件に基づいて、シナリオ 1 で以下のバリエーションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-410">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="7cf66-411">モバイル アプリ エクスペリエンスを向上するには、このセクションを使用してください。</span><span class="sxs-lookup"><span data-stu-id="7cf66-411">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="7cf66-412">シナリオ 2 では、より多くの請求書行が予想されるため、以下のデザイン変更により、モバイル デバイスのユーザー エクスペリエンスが最適化されます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-412">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="7cf66-413">(シナリオ 1 のように) 詳細ページで請求書の行を表示する代わりに、別のモバイル ページに行を表示することを選択できます。</span><span class="sxs-lookup"><span data-stu-id="7cf66-413">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="7cf66-414">このシナリオでは複数の請求書行が予想されるため、**VendMobileInvoiceAllDistributionTree** ページを使用してモバイルの配布ページを設計すると (シナリオ 1 のように)、ユーザーは行を配布に関連付けるのが紛らわしく感じる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7cf66-414">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="7cf66-415">したがって、**VendMobileInvoiceLineDistributionTree** ページを使用して配布ページを設計します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-415">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="7cf66-416">理想的には、このシナリオでは、配布を請求明細行のコンテキストで表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cf66-416">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="7cf66-417">したがって、ユーザーが行にドリルダウンして配布ページを表示できることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7cf66-417">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="7cf66-418">シナリオ 1 のヘッダーおよび詳細ページの場合と同様に、ページ リンク機能を使用してドリルスルーを確立します。</span><span class="sxs-lookup"><span data-stu-id="7cf66-418">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="7cf66-419">シナリオ 2 の配布では、複数の金額タイプ (消費税、請求など) が予想されるため、金額タイプの説明を表示すると便利です。</span><span class="sxs-lookup"><span data-stu-id="7cf66-419">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="7cf66-420">(この情報はシナリオ 1 では省略しました。)</span><span class="sxs-lookup"><span data-stu-id="7cf66-420">(We omitted this information in scenario 1.)</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]