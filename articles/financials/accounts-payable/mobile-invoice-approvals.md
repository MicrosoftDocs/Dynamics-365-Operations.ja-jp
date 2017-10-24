---
title: "モバイルによる請求書承認"
description: "このトピックは、サポート案件としてモバイルのベンダー請求書の承認を取得することによる、Dynamics 365 for Finance and Operations のモバイル シナリオを設計するための実際的なアプローチを提供することを目的としています。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 661c5a14d27f3ad9df6088c2977c507ca315a998
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="mobile-invoice-approvals"></a><span data-ttu-id="9a85b-103">モバイルによる請求書承認</span><span class="sxs-lookup"><span data-stu-id="9a85b-103">Mobile invoice approvals</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9a85b-104">Microsoft Dynamics 365 for Finance and Operations のモバイル機能において、Enterprise Edition によりビジネス ユーザーはモバイル エクスペリエンスを設計できます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-104">Mobile capabilities in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition let a business user design mobile experiences.</span></span> <span data-ttu-id="9a85b-105">高度なシナリオでは、開発者はプラットフォームを使用して、必要に応じて機能を拡張することもできます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="9a85b-106">モバイルに関する新しい概念のいくつかを学ぶ最も効果的な方法は、いくつかのシナリオを設計するプロセスを経ることです。</span><span class="sxs-lookup"><span data-stu-id="9a85b-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="9a85b-107">このトピックは、サポート案件としてモバイルのベンダー請求書の承認を取得することによる、モバイル シナリオを設計するための実際的なアプローチを提供することを目的としています。</span><span class="sxs-lookup"><span data-stu-id="9a85b-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="9a85b-108">このトピックは、シナリオのさまざまなバリエーションを設計するのに役立ちますが、仕入先請求書に関連しない他のシナリオにも適用できます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="9a85b-109">前提条件</span><span class="sxs-lookup"><span data-stu-id="9a85b-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="9a85b-110">前提条件</span><span class="sxs-lookup"><span data-stu-id="9a85b-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="9a85b-111">説明</span><span class="sxs-lookup"><span data-stu-id="9a85b-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a85b-112">モバイル ハンドブックの先行読取</span><span class="sxs-lookup"><span data-stu-id="9a85b-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="9a85b-113">モバイル プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="9a85b-113">Mobile platform</span></span>](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="9a85b-114">Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9a85b-114">Dynamics 365 for Finance and Operations</span></span>                                                                             | <span data-ttu-id="9a85b-115">Microsoft Dynamics 365 for Operations バージョン 1611 および Microsoft Dynamics for Operations プラットフォーム更新プログラム 3 (2016 年 11 月) がある環境。</span><span class="sxs-lookup"><span data-stu-id="9a85b-115">An environment that has Microsoft Dynamics 365 for Operations version 1611 and Microsoft Dynamics for Operations platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="9a85b-116">更新プログラム KB 3204341 をインストールします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="9a85b-117">タスク レコーダーは誤って 2 つのドロップダウン ダイアログの Close コマンドを記録できます。これは Dynamics 365 for Operation プラットフォーム更新プログラム 3 (2016 年 11 月の更新プログラム) に含まれています。</span><span class="sxs-lookup"><span data-stu-id="9a85b-117">Task recorder can erroneously record two Close commands for dropdown dialogs this is included in Dynamics 365 for Operation platform update 3 (November 2016 update)</span></span> |
| <span data-ttu-id="9a85b-118">更新プログラム KB 3207800 をインストールします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="9a85b-119">この修正プログラムは、モバイル クライアント上で表示される添付ファイルを有効にします。これは Dynamics 365 for Operation プラットフォーム更新プログラム 3 (2016 年 11 月の更新プログラム) に含まれています。</span><span class="sxs-lookup"><span data-stu-id="9a85b-119">This hotfix enables attachments to be viewed on the mobile client this is included in Dynamics 365 for Operation platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="9a85b-120">更新プログラム KB 3208224 をインストールします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="9a85b-121">モバイル ベンダー請求書承認アプリケーションのアプリケーション コードです。これは、Microsoft Dynamics AX アプリケーション 7.0.1（2016 年 5 月）に含まれています。</span><span class="sxs-lookup"><span data-stu-id="9a85b-121">Application code for the mobile vendor invoice approval application this is included in Microsoft Dynamics AX application 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="9a85b-122">Finance and Operations 用のモバイル アプリがインストールされている Android または iOS または Windows デバイス</span><span class="sxs-lookup"><span data-stu-id="9a85b-122">An Android or iOS or a Windows device that has the mobile app installed for Finance and Operations</span></span> | <span data-ttu-id="9a85b-123">適切なアプリ ストアでアプリを検索します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="9a85b-124">はじめに</span><span class="sxs-lookup"><span data-stu-id="9a85b-124">Introduction</span></span>
<span data-ttu-id="9a85b-125">ベンダー請求書のモバイル承認には、「前提条件」セクションに記載されている 3 つの修正プログラムが必要です。</span><span class="sxs-lookup"><span data-stu-id="9a85b-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="9a85b-126">これらの修正プログラムは、請求書承認のためのワークスペースを提供しません。</span><span class="sxs-lookup"><span data-stu-id="9a85b-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="9a85b-127">ワークスペースがモバイルのコンテキストでどのようなものかを知るには、「前提条件」セクションで説明したモバイル ハンドブックをお読みください。</span><span class="sxs-lookup"><span data-stu-id="9a85b-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="9a85b-128">請求書承認ワークスペースを設計する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a85b-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="9a85b-129">すべての組織は、ベンダー請求書の異なるビジネス プロセスを調整し定義します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="9a85b-130">ベンダーの請求書承認のためのモバイル エクスペリエンスを設計する前に、ビジネス プロセスの次の側面を考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a85b-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="9a85b-131">このアイデアは、これらのデータ ポイントを可能な限り使用して、デバイス上のユーザー エクスペリエンスを最適化することです。</span><span class="sxs-lookup"><span data-stu-id="9a85b-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="9a85b-132">モバイル エクスペリエンスで、請求書ヘッダーのどのフィールドを、どのような順序で表示したいですか?</span><span class="sxs-lookup"><span data-stu-id="9a85b-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="9a85b-133">モバイル エクスペリエンスで、請求書行のどのフィールドを、どのような順序で表示したいですか?</span><span class="sxs-lookup"><span data-stu-id="9a85b-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="9a85b-134">請求書にはいくつの請求書明細行がありますか?</span><span class="sxs-lookup"><span data-stu-id="9a85b-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="9a85b-135">80-20 ルールをここで適用し、80 パーセントを最適化します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="9a85b-136">ユーザーは、レビュー中にモバイル デバイス上の勘定配賦 (請求書コーディング) を見たいでしょうか?</span><span class="sxs-lookup"><span data-stu-id="9a85b-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="9a85b-137">この質問に対する回答が「はい」の場合は、次の質問を検討してください。</span><span class="sxs-lookup"><span data-stu-id="9a85b-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="9a85b-138">請求書行にはいくつの勘定配賦 (拡張価格、消費税、料金、分割など) がありますか?</span><span class="sxs-lookup"><span data-stu-id="9a85b-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="9a85b-139">再度、80-20 ルールを適用します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="9a85b-140">請求書には請求書ヘッダーに勘定配賦も含まれていますか?</span><span class="sxs-lookup"><span data-stu-id="9a85b-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="9a85b-141">もしそうなら、これらの勘定配賦はデバイス上で利用できるはずですか?</span><span class="sxs-lookup"><span data-stu-id="9a85b-141">If so, should these accounting distributions be available on the device?</span></span>

> [!NOTE]
> <span data-ttu-id="9a85b-142">このトピックでは、現在モバイル シナリオでこの機能がサポートされていないため、勘定配賦の編集方法については説明していません。</span><span class="sxs-lookup"><span data-stu-id="9a85b-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="9a85b-143">ユーザーはデバイス上の請求書の添付ファイルを見たいですか?</span><span class="sxs-lookup"><span data-stu-id="9a85b-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="9a85b-144">請求書承認のためのモバイル エクスペリエンスの設計は、これらの質問に対する回答によって異なります。</span><span class="sxs-lookup"><span data-stu-id="9a85b-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="9a85b-145">その目的は、組織内のモバイルでのビジネス プロセスのユーザー エクスペリエンスを最適化することです。</span><span class="sxs-lookup"><span data-stu-id="9a85b-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="9a85b-146"> このトピックの残りでは、前述の質問とは異なる回答に基づいた 2 つのシナリオのバリエーションを見ていきます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="9a85b-147">一般的なガイダンスとして、モバイル デザイナーと協力している場合は、アップデートを失わないように変更を「公開」してください。</span><span class="sxs-lookup"><span data-stu-id="9a85b-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="9a85b-148">Contoso の簡単な請求書承認シナリオの設計</span><span class="sxs-lookup"><span data-stu-id="9a85b-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9a85b-149">シナリオの属性</span><span class="sxs-lookup"><span data-stu-id="9a85b-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="9a85b-150">応答</span><span class="sxs-lookup"><span data-stu-id="9a85b-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a85b-151">モバイル エクスペリエンスで、請求書ヘッダーのどのフィールドを、どのような順序で表示したいですか?</span><span class="sxs-lookup"><span data-stu-id="9a85b-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="9a85b-152">仕入先名</span><span class="sxs-lookup"><span data-stu-id="9a85b-152">Vendor name</span></span></li>
<li><span data-ttu-id="9a85b-153">請求合計</span><span class="sxs-lookup"><span data-stu-id="9a85b-153">Invoice total</span></span></li>
<li><span data-ttu-id="9a85b-154">請求先/元 ID</span><span class="sxs-lookup"><span data-stu-id="9a85b-154">Invoice account</span></span></li>
<li><span data-ttu-id="9a85b-155">請求書番号</span><span class="sxs-lookup"><span data-stu-id="9a85b-155">Invoice number</span></span></li>
<li><span data-ttu-id="9a85b-156">請求日</span><span class="sxs-lookup"><span data-stu-id="9a85b-156">Invoice date</span></span></li>
<li><span data-ttu-id="9a85b-157">請求明細</span><span class="sxs-lookup"><span data-stu-id="9a85b-157">Invoice description</span></span></li>
<li><span data-ttu-id="9a85b-158">期日</span><span class="sxs-lookup"><span data-stu-id="9a85b-158">Due date</span></span></li>
<li><span data-ttu-id="9a85b-159">請求書通貨</span><span class="sxs-lookup"><span data-stu-id="9a85b-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a85b-160">モバイル エクスペリエンスで、請求書行のどのフィールドを、どのような順序で表示したいですか?</span><span class="sxs-lookup"><span data-stu-id="9a85b-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="9a85b-161">調達カテゴリ</span><span class="sxs-lookup"><span data-stu-id="9a85b-161">Procurement category</span></span></li>
<li><span data-ttu-id="9a85b-162">件数</span><span class="sxs-lookup"><span data-stu-id="9a85b-162">Quantity</span></span></li>
<li><span data-ttu-id="9a85b-163">単価</span><span class="sxs-lookup"><span data-stu-id="9a85b-163">Unit price</span></span></li>
<li><span data-ttu-id="9a85b-164">明細行の正味金額</span><span class="sxs-lookup"><span data-stu-id="9a85b-164">Line net amount</span></span></li>
<li><span data-ttu-id="9a85b-165">1099 金額</span><span class="sxs-lookup"><span data-stu-id="9a85b-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a85b-166">請求書にはいくつの請求書明細行がありますか?</span><span class="sxs-lookup"><span data-stu-id="9a85b-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="9a85b-167">80-20 ルールをここで適用し、80 パーセントを最適化します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="9a85b-168">1</span><span class="sxs-lookup"><span data-stu-id="9a85b-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a85b-169">ユーザーは、レビュー中にモバイル デバイス上の勘定配賦 (請求書コーディング) を見たいでしょうか?</span><span class="sxs-lookup"><span data-stu-id="9a85b-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="9a85b-170">有</span><span class="sxs-lookup"><span data-stu-id="9a85b-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a85b-171">請求書行にはいくつの勘定配賦 (拡張価格、消費税、料金、など) がありますか?</span><span class="sxs-lookup"><span data-stu-id="9a85b-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="9a85b-172">再度、80-20 ルールを適用します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="9a85b-173">拡張価格: 2 売上税: 0 料金: 0</span><span class="sxs-lookup"><span data-stu-id="9a85b-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a85b-174">請求書には請求書ヘッダーに勘定配賦も含まれていますか?</span><span class="sxs-lookup"><span data-stu-id="9a85b-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="9a85b-175">もしそうなら、これらの勘定配賦はデバイス上で利用できるはずですか?</span><span class="sxs-lookup"><span data-stu-id="9a85b-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="9a85b-176">不使用</span><span class="sxs-lookup"><span data-stu-id="9a85b-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a85b-177">ユーザーはデバイス上の請求書の添付ファイルを見たいですか?</span><span class="sxs-lookup"><span data-stu-id="9a85b-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="9a85b-178">有</span><span class="sxs-lookup"><span data-stu-id="9a85b-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="9a85b-179">ワークスペースの作成</span><span class="sxs-lookup"><span data-stu-id="9a85b-179">Create the workspace</span></span>

1.  <span data-ttu-id="9a85b-180">ブラウザで、Finance and Operations を開いてサインインします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-180">In a browser, open Finance and Operations, and sign in.</span></span>
2.  <span data-ttu-id="9a85b-181">サインインした後、次の例のように **&mode=mobile** を URL に追加し、ページを更新します。https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard**&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="9a85b-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard**&mode=mobile**</span></span>
3.  <span data-ttu-id="9a85b-182">ページの右上角にある [**設定**] (歯車) ボタンをクリックし、次に [**モバイル アプリ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="9a85b-183">モバイル アプリのデザイナーは、タスク レコーダーが表示されるのと同じように表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a85b-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="9a85b-184">新しいワークスペース作成するには、[**追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="9a85b-185">この例として、ワークスペースを [**自分の承認**] と名付けます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="9a85b-186">説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-186">Enter a description.</span></span>
6.  <span data-ttu-id="9a85b-187">ワークスペースの色を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-187">Select a workspace color.</span></span> <span data-ttu-id="9a85b-188">ワークスペースの色は、このワークスペースのモバイル エクスペリエンスの全体的なスタイルに使用されます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="9a85b-189">ワークスペースのアイコンを選択します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="9a85b-190">[**完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-190">Click **Done**</span></span>
9.  <span data-ttu-id="9a85b-191">変更を保存するには、[**ワークスペースを公開**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="9a85b-192">自分に割り当てられている仕入先請求書</span><span class="sxs-lookup"><span data-stu-id="9a85b-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="9a85b-193">設計する必要がある最初のモバイル ページは、レビューのためにユーザーに割り当てられている請求書の一覧です。</span><span class="sxs-lookup"><span data-stu-id="9a85b-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="9a85b-194">このモバイル ページを設計するには、Finance and Operations で [**VendMobileInvoiceAssignedToMeListPage**] ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page in Finance and Operations.</span></span> <span data-ttu-id="9a85b-195">この手順を完了する前に、少なくとも 1 つの仕入先請求書がレビューのために割り当てられていること、および請求書行に 2 つの配布があることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9a85b-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="9a85b-196">この設定は、このシナリオの要件を満たしています。</span><span class="sxs-lookup"><span data-stu-id="9a85b-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="9a85b-197">Finance and Operations URL で、メニューの名前を [**VendMobileInvoiceAssignedToMeListPage**] に置き換え、[**買掛金勘定**] モジュールの [**私に割り当てられた保留中の仕入先請求書**] リスト ページのモバイル版を開きます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-197">In the Finance and Operations URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="9a85b-198">システムに割り当てられている請求書の数に応じて、このページにこれらの請求書が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="9a85b-199">特定の請求書を検索するには、左側のフィルターを使用します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="9a85b-200">ただし、この例では特定の請求書は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="9a85b-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="9a85b-201">割り当てられた請求書を要求するだけで、モバイル ページをデザインすることができます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="9a85b-202">利用可能な新しいページは、ベンダーの請求書のモバイル シナリオを開発するために特別に設計されています。</span><span class="sxs-lookup"><span data-stu-id="9a85b-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="9a85b-203">したがって、これらのページを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a85b-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="9a85b-204">URL は次のようなものでなければなりません。また、入力後、イラストに示されているページが表示されます。https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="9a85b-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
2.  <span data-ttu-id="9a85b-205">ページの右上角にある [**設定**] (歯車) ボタンをクリックし、次に [**モバイル アプリ**] をクリックします</span><span class="sxs-lookup"><span data-stu-id="9a85b-205">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="9a85b-206">ワークスペースを選択し、[**編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-206">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="9a85b-207">[**ページを追加**] をクリックして、最初のモバイル ページを作成します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-207">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="9a85b-208">**私のベンダーの請求書**などの名前と、**レビュー用に割り当てられたベンダーの請求書**などの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-208">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="9a85b-209">**[完了]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-209">Click **Done**.</span></span>
7.  <span data-ttu-id="9a85b-210">モバイル デザイナーの [**フィールド**] タブで [**フィールドの選択**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-210">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="9a85b-211">リスト ページの列は、次の図のようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a85b-211">The columns on the list page must resemble the following illustration.</span></span> <span data-ttu-id="9a85b-212">[![自分に割り当てられた保留中の仕入先請求書ページ](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="9a85b-212">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
8.  <span data-ttu-id="9a85b-213">リスト ページから、モバイル ページのユーザーに表示する必要がある列を追加します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-213">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="9a85b-214">追加する順序は、フィールドがエンド ユーザーに表示される順序です。</span><span class="sxs-lookup"><span data-stu-id="9a85b-214">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="9a85b-215">フィールドの順序を変更する唯一の方法は、すべてのフィールドを再選択することです。</span><span class="sxs-lookup"><span data-stu-id="9a85b-215">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="9a85b-216">このシナリオの要件に基づいて、次の 8 つのフィールドが必要です。</span><span class="sxs-lookup"><span data-stu-id="9a85b-216">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="9a85b-217">しかし、一部のユーザは、8 つのフィールドが多くの情報をモバイル デバイス上に持つと考える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9a85b-217">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="9a85b-218">したがって、モバイル リスト ビューで最も重要なフィールドのみを表示します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-218">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="9a85b-219">残りのフィールドは、後で設計する詳細ビューに表示されます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-219">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="9a85b-220">今のところ、次のフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-220">For now, we will add the following fields.</span></span> <span data-ttu-id="9a85b-221">モバイル ページに追加するには、これらの列のプラス記号 (**+**) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-221">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="9a85b-222">仕入先名</span><span class="sxs-lookup"><span data-stu-id="9a85b-222">Vendor name</span></span>
    - <span data-ttu-id="9a85b-223">請求合計</span><span class="sxs-lookup"><span data-stu-id="9a85b-223">Invoice total</span></span>
    - <span data-ttu-id="9a85b-224">請求先/元 ID</span><span class="sxs-lookup"><span data-stu-id="9a85b-224">Invoice account</span></span>
    - <span data-ttu-id="9a85b-225">請求書番号</span><span class="sxs-lookup"><span data-stu-id="9a85b-225">Invoice number</span></span>
    - <span data-ttu-id="9a85b-226">請求日</span><span class="sxs-lookup"><span data-stu-id="9a85b-226">Invoice date</span></span>

    <span data-ttu-id="9a85b-227">フィールドが追加されると、モバイル ページは次の図のようになります。</span><span class="sxs-lookup"><span data-stu-id="9a85b-227">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    <span data-ttu-id="9a85b-228">[![フィールドの後ページが表示される](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="9a85b-228">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>
9.  <span data-ttu-id="9a85b-229">ワークフロー アクションを後で有効にできるように、次の列も追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a85b-229">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="9a85b-230">完了したタスクを表示する</span><span class="sxs-lookup"><span data-stu-id="9a85b-230">Show complete task</span></span>
    - <span data-ttu-id="9a85b-231">委任タスクを表示する</span><span class="sxs-lookup"><span data-stu-id="9a85b-231">Show delegate task</span></span>
    - <span data-ttu-id="9a85b-232">リコールタスクを表示する</span><span class="sxs-lookup"><span data-stu-id="9a85b-232">Show recall task</span></span>
    - <span data-ttu-id="9a85b-233">拒否タスクを表示する</span><span class="sxs-lookup"><span data-stu-id="9a85b-233">Show reject task</span></span>
    - <span data-ttu-id="9a85b-234">リクエスト完了タスクを表示する</span><span class="sxs-lookup"><span data-stu-id="9a85b-234">Show request completion task</span></span>
    - <span data-ttu-id="9a85b-235">再送信タスクを表示する</span><span class="sxs-lookup"><span data-stu-id="9a85b-235">Show resubmit task</span></span>

10. <span data-ttu-id="9a85b-236">[**完了**] をクリックして、編集モードを終了します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-236">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="9a85b-237">[**戻る**]、次に [**完了**] をクリックして、ワークスペースを終了します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-237">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="9a85b-238">[**ワークスペースの公開**] をクリックして作業を保存します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-238">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="9a85b-239">**請求書**の買掛金勘定パラメータ フォームの**仕入先請求書一覧の請求書総額の表示**を有効化します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-239">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="9a85b-240">このパラメータを有効にすることによってのみ、請求書合計が計算され、保留中の仕入先請求一覧ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-240">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="9a85b-241">これは前提条件の修正プログラム 3208224 の一部の新しい機能です。</span><span class="sxs-lookup"><span data-stu-id="9a85b-241">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="9a85b-242">ベンダー請求書の詳細</span><span class="sxs-lookup"><span data-stu-id="9a85b-242">Vendor invoice details</span></span>

<span data-ttu-id="9a85b-243">モバイル用の請求書の詳細ページを設計するには、Finance and Operations の [**VendMobileInvoiceHeaderDetails**] ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-243">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page in Finance and Operations.</span></span> <span data-ttu-id="9a85b-244">システムに登録されている請求書の数に応じて、このページには最も古い請求書（最初に作成された請求書）が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-244">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="9a85b-245">特定の請求書を検索するには、左側のフィルターを使用します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-245">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="9a85b-246">ただし、この例では特定の請求書は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="9a85b-246">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="9a85b-247">モバイルページを設計できるように、請求書データが必要です。</span><span class="sxs-lookup"><span data-stu-id="9a85b-247">We just require some invoice data so that we can design the mobile page.</span></span> <span data-ttu-id="9a85b-248">[![ワークフロー ページ](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="9a85b-248">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1.  <span data-ttu-id="9a85b-249">Finance and Operations URL で、メニュー アイテムの名前を [**VendMobileInvoiceHeaderDetails**] に置き換えてフォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-249">In the Finance and Operations URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>
2.  <span data-ttu-id="9a85b-250">**設定** (ギア) ボタンからモバイル デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-250">Open the mobile designer from the **Settings** (gear) button.</span></span>
3.  <span data-ttu-id="9a85b-251">ワークスペースで編集モードを開始するには、[**編集**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-251">Click the **Edit** button to start edit mode in the workspace.</span></span>
4.  <span data-ttu-id="9a85b-252">前に作成した**私のベンダーの請求書**ページを選択し、[**編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-252">Select the **My vendor invoices **page that you created earlier, and then click **Edit**.</span></span>
5.  <span data-ttu-id="9a85b-253">[**フィールド**] タブで、[**グリッド**] 列見出しをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-253">On the **Fields** tab, click the **Grid** column heading.</span></span>
6.  <span data-ttu-id="9a85b-254">[**プロパティ**] &gt; [**ページの追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-254">Click **Properties** &gt; **Add page**.</span></span> <span data-ttu-id="9a85b-255">**注:** **グリッド**見出しをクリックしてページを追加すると、詳細ページとの関係が自動的に確立されます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-255">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>
7.  <span data-ttu-id="9a85b-256">**請求書の詳細**などのページタイトルと、**請求書ヘッダーと行の詳細の表示**などの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-256">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>
8.  <span data-ttu-id="9a85b-257">[**フィールドの選択**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-257">Click **Select fields**.</span></span> <span data-ttu-id="9a85b-258">追加する順序は、フィールドがエンド ユーザーに表示される順序に留意してください。</span><span class="sxs-lookup"><span data-stu-id="9a85b-258">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="9a85b-259">フィールドの順序を変更する唯一の方法は、すべてのフィールドを再選択することです。</span><span class="sxs-lookup"><span data-stu-id="9a85b-259">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 
9.  <span data-ttu-id="9a85b-260">このシナリオの要件に基づいて、ヘッダーから次のフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-260">Add the following fields from the header, based on the requirements for this scenario:</span></span>
    - <span data-ttu-id="9a85b-261">仕入先名</span><span class="sxs-lookup"><span data-stu-id="9a85b-261">Vendor name</span></span>
    - <span data-ttu-id="9a85b-262">請求合計</span><span class="sxs-lookup"><span data-stu-id="9a85b-262">Invoice total</span></span>
    - <span data-ttu-id="9a85b-263">請求先/元 ID</span><span class="sxs-lookup"><span data-stu-id="9a85b-263">Invoice account</span></span>
    - <span data-ttu-id="9a85b-264">請求書番号</span><span class="sxs-lookup"><span data-stu-id="9a85b-264">Invoice number</span></span>
    - <span data-ttu-id="9a85b-265">請求日</span><span class="sxs-lookup"><span data-stu-id="9a85b-265">Invoice date</span></span>
    - <span data-ttu-id="9a85b-266">請求明細</span><span class="sxs-lookup"><span data-stu-id="9a85b-266">Invoice description</span></span>
    - <span data-ttu-id="9a85b-267">期日</span><span class="sxs-lookup"><span data-stu-id="9a85b-267">Due date</span></span>
    - <span data-ttu-id="9a85b-268">請求書通貨</span><span class="sxs-lookup"><span data-stu-id="9a85b-268">Invoice currency</span></span>

10. <span data-ttu-id="9a85b-269">ページの行グリッドから次のフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-269">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="9a85b-270">調達カテゴリ</span><span class="sxs-lookup"><span data-stu-id="9a85b-270">Procurement category</span></span>
    - <span data-ttu-id="9a85b-271">件数</span><span class="sxs-lookup"><span data-stu-id="9a85b-271">Quantity</span></span>
    - <span data-ttu-id="9a85b-272">単価</span><span class="sxs-lookup"><span data-stu-id="9a85b-272">Unit price</span></span>
    - <span data-ttu-id="9a85b-273">明細行の正味金額</span><span class="sxs-lookup"><span data-stu-id="9a85b-273">Line net amount</span></span>
    - <span data-ttu-id="9a85b-274">1099 金額</span><span class="sxs-lookup"><span data-stu-id="9a85b-274">1099 amount</span></span>

11. <span data-ttu-id="9a85b-275">前の 2 つの手順のすべてのフィールドが追加されたら、[**完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-275">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="9a85b-276">ページは次の図のようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a85b-276">The page must resemble the following illustration.</span></span>
<span data-ttu-id="9a85b-277">[![フィールドの後ページが表示される](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="9a85b-277">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>
12. <span data-ttu-id="9a85b-278">[**完了**] をクリックして、編集モードを終了します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-278">Click **Done** to exit edit mode.</span></span>
13. <span data-ttu-id="9a85b-279">[**戻る**]、次に [**完了**] をクリックして、ワークスペースを終了します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-279">Click **Back** and then **Done** to exit the workspace</span></span>
14. <span data-ttu-id="9a85b-280">[**ワークスペースの公開**] をクリックして作業を保存します</span><span class="sxs-lookup"><span data-stu-id="9a85b-280">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="9a85b-281">ワークフロー アクション</span><span class="sxs-lookup"><span data-stu-id="9a85b-281">Workflow actions</span></span>

<span data-ttu-id="9a85b-282">ワークフロー アクションを追加するには、Finance and Operations の [**VendMobileInvoiceHeaderDetails**] ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-282">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page in Finance and Operations.</span></span> <span data-ttu-id="9a85b-283">このページを開くには、先ほどと同様に、URL 内のメニュー項目の名前を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-283">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="9a85b-284">次に、[**設定**] (ギア) ボタンからモバイル デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-284">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="9a85b-285"> 詳細ページにワークフロー アクションを追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9a85b-285">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="9a85b-286">ワークフローアクションを利用できるようにするため、請求書は適切な状態で割り当てられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a85b-286">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="9a85b-287">ワークフロー アクションを記録</span><span class="sxs-lookup"><span data-stu-id="9a85b-287">Record workflow actions</span></span>
1.  <span data-ttu-id="9a85b-288">ワークスペースで編集モードを開始するには、[**編集**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-288">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="9a85b-289">前に作成した**請求書の詳細**ページを選択し、[**編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-289">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="9a85b-290">[**アクション**] タブで、[**アクションの 追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-290">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="9a85b-291">**承認​​**などのアクションタイトルと、**請求書の承認**などの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-291">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="9a85b-292">ここに入力するアクション タイトルは、モバイル アプリでユーザーに表示されるアクションの名前になります。</span><span class="sxs-lookup"><span data-stu-id="9a85b-292">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="9a85b-293">**[完了]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-293">Click **Done**.</span></span>
6.  <span data-ttu-id="9a85b-294">[**フィールドの選択**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-294">Click **Select fields**.</span></span>
7.  <span data-ttu-id="9a85b-295">**VendMobileInvoiceHeaderDetails**ページのワークフロー プロセスを実行し、記録するアクションを完了します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-295">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="9a85b-296">このプロセス中にワークフロー コメントを入力して、コメント フィールドもモバイル エクスペリエンスに含めるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="9a85b-296">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="9a85b-297">ワークフロー アクションの実行後、[**完了**] をクリックしてフィールドの選択タスクを完了します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-297">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="9a85b-298">[**完了**] をクリックして、編集モードを終了します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-298">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="9a85b-299">[**戻る**]、次に [**完了**] をクリックして、ワークスペースを終了します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-299">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="9a85b-300">[**ワークスペースの公開**] をクリックして作業を保存します</span><span class="sxs-lookup"><span data-stu-id="9a85b-300">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="9a85b-301">必要なすべてのワークフロー アクションを記録するには、前の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-301">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="9a85b-302">.js ファイルの作成</span><span class="sxs-lookup"><span data-stu-id="9a85b-302">Create a .js file</span></span>
1. <span data-ttu-id="9a85b-303">メモ帳または Microsoft Visual Studio を開き、次のコードを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-303">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="9a85b-304">ファイルを .js ファイルとして保存します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-304">Save the file as a .js file.</span></span> <span data-ttu-id="9a85b-305">このコードを使い、次の処理を行います。</span><span class="sxs-lookup"><span data-stu-id="9a85b-305">This code does the following:</span></span>
    - <span data-ttu-id="9a85b-306">以前にモバイル リスト ページに追加した追加のワークフロー関連の列は非表示になっています。</span><span class="sxs-lookup"><span data-stu-id="9a85b-306">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="9a85b-307">アプリケーションがコンテキスト内にその情報を持ち、次のステップを実行できるように、これらの列を追加しました。</span><span class="sxs-lookup"><span data-stu-id="9a85b-307">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="9a85b-308">アクティブなワークフロー ステップに基づいて、それらのアクションのみを表示するロジックが適用されます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-308">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

> [!NOTE]
> <span data-ttu-id="9a85b-309">コード内のページおよび他のコントロールの名前は、ワークスペース内で同じ名前でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="9a85b-309">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

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

2.  <span data-ttu-id="9a85b-310">[**ロジック**] タブを選択して、コード ファイルをワークスペースにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-310">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="9a85b-311">[**完了**] をクリックして、編集モードを終了します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-311">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="9a85b-312">[**戻る**]、次に [**完了**] をクリックして、ワークスペースを終了します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-312">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="9a85b-313">[**ワークスペースの公開**] をクリックして作業を保存します</span><span class="sxs-lookup"><span data-stu-id="9a85b-313">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="9a85b-314">ベンダー請求書の添付</span><span class="sxs-lookup"><span data-stu-id="9a85b-314">Vendor invoice attachments</span></span>

1.  <span data-ttu-id="9a85b-315">ページの右上角にある [**設定**] (歯車) ボタンをクリックし、次に [**モバイル アプリ**] をクリックします</span><span class="sxs-lookup"><span data-stu-id="9a85b-315">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
2.  <span data-ttu-id="9a85b-316">ワークスペースで編集モードを開始するには、[**編集**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-316">Click the **Edit** button to start edit mode in the workspace.</span></span>
3.  <span data-ttu-id="9a85b-317">前に作成した**請求書の詳細**ページを選択し、[**編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-317">Select the **Invoice details **page that you created earlier, and then click **Edit**.</span></span>
4.  <span data-ttu-id="9a85b-318">以下のように、[**文書管理**] オプションを [**はい**] に設定します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-318">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="9a85b-319">**注:** モバイル デバイスに添付ファイルを表示する必要がない場合は、このオプションをデフォルト設定の [**いいえ**] に設定しておくことができます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-319">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
<span data-ttu-id="9a85b-320">![ドキュメント管理](./media/docmanagement-216x300.png)</span><span class="sxs-lookup"><span data-stu-id="9a85b-320">![Document management](./media/docmanagement-216x300.png)</span></span>
6.  <span data-ttu-id="9a85b-321">[**完了**] をクリックして、編集モードを終了します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-321">Click **Done** to exit edit mode.</span></span>
7.  <span data-ttu-id="9a85b-322">[**戻る**]、次に [**完了**] をクリックして、ワークスペースを終了します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-322">Click **Back** and then **Done** to exit the workspace</span></span>
8.  <span data-ttu-id="9a85b-323">[**ワークスペースの公開**] をクリックして作業を保存します</span><span class="sxs-lookup"><span data-stu-id="9a85b-323">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="9a85b-324">ベンダー請求書行の配布</span><span class="sxs-lookup"><span data-stu-id="9a85b-324">Vendor invoice line distributions</span></span>

<span data-ttu-id="9a85b-325">このシナリオの要件により、行レベルの配布のみが存在し、請求書には常に 1 行しか含まれないことが確認されます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-325">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="9a85b-326">このシナリオは単純なので、モバイル デバイスのユーザー エクスペリエンスは、配布を表示するためにユーザーが複数のレベルをドリルダウンする必要がないほど単純でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="9a85b-326">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="9a85b-327">Finance and Operations のベンダーの請求書には、請求書のヘッダーからすべての配布を表示するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="9a85b-327">Vendor invoices in Finance and Operations include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="9a85b-328">この経験は、モバイル シナリオに必要なものです。</span><span class="sxs-lookup"><span data-stu-id="9a85b-328">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="9a85b-329">したがって、**VendMobileInvoiceAllDistributionTree** ページを使用してモバイル シナリオのこの部分を設計します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-329">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="9a85b-330">要件を知ることで、使用する特定のページと、シナリオを設計する際にユーザーのモバイル エクスペリエンスをどのように最適化するかを決定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-330">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="9a85b-331">2 番目のシナリオでは、そのシナリオの要件が異なるため、異なるページを使用して配布を表示します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-331">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="9a85b-332">URL で、前と同じように、メニュー項目の名前を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-332">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="9a85b-333">表示されるページは、次の図のようになります。</span><span class="sxs-lookup"><span data-stu-id="9a85b-333">The page that appears should resemble the following illustration.</span></span>
<span data-ttu-id="9a85b-334">[![すべての配分ページ](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="9a85b-334">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>
2.  <span data-ttu-id="9a85b-335">**設定** (ギア) ボタンからモバイル デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-335">Open the mobile designer from the **Settings** (gear) button.</span></span>
3.  <span data-ttu-id="9a85b-336">ワークスペースで編集モードを開始するには、[**編集**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-336">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="9a85b-337">**注:** 2 つの新しいページが自動的に作成されたことがわかります。</span><span class="sxs-lookup"><span data-stu-id="9a85b-337">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="9a85b-338">前のセクションでドキュメント管理を有効にしたため、システムがこれらのページを作成します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-338">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="9a85b-339">これらの新しいページは無視できます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-339">You can ignore these new pages.</span></span>
4.  <span data-ttu-id="9a85b-340">[**ページの追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-340">Click **Add page**.</span></span>
5.  <span data-ttu-id="9a85b-341">**会計の表示**などのページ タイトルと、**請求書の会計の表示**などの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-341">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>
6.  <span data-ttu-id="9a85b-342">[**完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-342">Click **Done**.</span></span>
7.  <span data-ttu-id="9a85b-343">[**フィールド**] タブで、[**フィールドの選択**] をクリックし、配布ページから次のフィールドを選択して、[**完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-343">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="9a85b-344">金額</span><span class="sxs-lookup"><span data-stu-id="9a85b-344">Amount</span></span>
    2.  <span data-ttu-id="9a85b-345">通貨</span><span class="sxs-lookup"><span data-stu-id="9a85b-345">Currency</span></span>
    3.  <span data-ttu-id="9a85b-346">勘定科目</span><span class="sxs-lookup"><span data-stu-id="9a85b-346">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="9a85b-347">このシナリオの要件では、拡張価格だけで配布が行われることが確認されているため、ディストリビューション グリッドから**説明**列を選択しませんでした。</span><span class="sxs-lookup"><span data-stu-id="9a85b-347">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="9a85b-348">したがって、ユーザーは、その配信が対象とする金額タイプを決定するために別のフィールドを必要としません。</span><span class="sxs-lookup"><span data-stu-id="9a85b-348">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="9a85b-349">ただし、次のシナリオでは、このシナリオの要件によって、他の金額タイプに配賦 (たとえば、消費税) があることが指定されているため、この情報を使用**します**。</span><span class="sxs-lookup"><span data-stu-id="9a85b-349">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>
8.  <span data-ttu-id="9a85b-350">[**完了**] をクリックして、編集モードを終了します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-350">Click **Done** to exit edit mode.</span></span>
9.  <span data-ttu-id="9a85b-351">[**戻る**]、次に [**完了**] をクリックして、ワークスペースを終了します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-351">Click **Back** and then **Done** to exit the workspace</span></span>
10. <span data-ttu-id="9a85b-352">[**ワークスペースの公開**] をクリックして作業を保存します</span><span class="sxs-lookup"><span data-stu-id="9a85b-352">Click **Publish workspace** to save your work</span></span>

> [!NOTE] 
> <span data-ttu-id="9a85b-353">[**会計の表示**] モバイル ページは、現在のところ私たちが設計したモバイル ページのいずれにもリンクしていません。</span><span class="sxs-lookup"><span data-stu-id="9a85b-353">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="9a85b-354">ユーザーはモバイル デバイスの**請求書の詳細**ページから**会計の表示**ページに移動できる必要があるため、**請求書の詳細**ページから**会計の表示**ページまでのナビゲーションを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a85b-354">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="9a85b-355">このナビゲーションは JavaScript を介する追加のロジックを使用して確立します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-355">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="9a85b-356">前に作成した .js ファイルを開き、次のコードで強調表示されている行を追加します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-356">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="9a85b-357">このコードは 2 つのことを行います:</span><span class="sxs-lookup"><span data-stu-id="9a85b-357">This code does two things:</span></span>
    1.  <span data-ttu-id="9a85b-358">ユーザーがワークスペースから**会計の表示**ページに直接ナビゲートできないようにします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-358">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="9a85b-359">**請求書の詳細**ページから**会計の表示**ページへのナビゲーション制御を確立します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-359">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

> [!NOTE] 
> <span data-ttu-id="9a85b-360">コード内のページおよび他のコントロールの名前は、ワークスペース内で同じ名前でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="9a85b-360">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

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

2.  <span data-ttu-id="9a85b-361">前のコードを上書きするには、[**ロジック**] タブを選択してコード ファイルをワークスペースにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="9a85b-361">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="9a85b-362">[**完了**] をクリックして、編集モードを終了します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-362">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="9a85b-363">[**戻る**]、次に [**完了**] をクリックして、ワークスペースを終了します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-363">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="9a85b-364">[**ワークスペースの公開**] をクリックして作業を保存します</span><span class="sxs-lookup"><span data-stu-id="9a85b-364">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="9a85b-365">検証</span><span class="sxs-lookup"><span data-stu-id="9a85b-365">Validation</span></span>

<span data-ttu-id="9a85b-366">モバイル デバイスからアプリを開き、Finance and Operations インスタンスに接続します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-366">From your mobile device, open the app, and connect to your Finance and Operations instance.</span></span> <span data-ttu-id="9a85b-367">ベンダーの請求書が審査のために割り当てられている会社にサインインしてください。</span><span class="sxs-lookup"><span data-stu-id="9a85b-367">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="9a85b-368">次の操作を実行できるはずです:</span><span class="sxs-lookup"><span data-stu-id="9a85b-368">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="9a85b-369">[**私の承認**] ワークスペースを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a85b-369">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="9a85b-370">[**私の承認**] ワークスペースをドリルインし、**私のベンダーの請求書**ページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a85b-370">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="9a85b-371">**私のベンダーの請求書** ページをドリルインし、割り当てられた請求書の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-371">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="9a85b-372">請求書の 1 つをドリルインし、請求書ヘッダーの詳細と行の詳細を確認します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-372">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="9a85b-373">詳細ページで、添付ファイルへのリンクを参照し、このリンクを使用して添付ファイル リストに移動し、添付ファイルを表示します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-373">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="9a85b-374">詳細ページで、**会計の表示**ページへのリンクを参照し、このリンクを使用して配布ページに移動し、配布を表示します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-374">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="9a85b-375">詳細ページで、下部にある [**操作**] メニューをクリックし、ワークフロー ステップに該当するワークフロー アクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-375">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="9a85b-376">Fabrikam の複雑な請求書承認シナリオの設計</span><span class="sxs-lookup"><span data-stu-id="9a85b-376">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9a85b-377">シナリオの属性</span><span class="sxs-lookup"><span data-stu-id="9a85b-377">Scenario attribute</span></span></th>
<th><span data-ttu-id="9a85b-378">応答</span><span class="sxs-lookup"><span data-stu-id="9a85b-378">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a85b-379">モバイル エクスペリエンスで、請求書ヘッダーのどのフィールドを、どのような順序で表示したいですか?</span><span class="sxs-lookup"><span data-stu-id="9a85b-379">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="9a85b-380">仕入先名</span><span class="sxs-lookup"><span data-stu-id="9a85b-380">Vendor name</span></span></li>
<li><span data-ttu-id="9a85b-381">請求金額</span><span class="sxs-lookup"><span data-stu-id="9a85b-381">Invoice amount</span></span></li>
<li><span data-ttu-id="9a85b-382">請求先/元 ID</span><span class="sxs-lookup"><span data-stu-id="9a85b-382">Invoice account</span></span></li>
<li><span data-ttu-id="9a85b-383">請求書番号</span><span class="sxs-lookup"><span data-stu-id="9a85b-383">Invoice number</span></span></li>
<li><span data-ttu-id="9a85b-384">請求日</span><span class="sxs-lookup"><span data-stu-id="9a85b-384">Invoice date</span></span></li>
<li><span data-ttu-id="9a85b-385">請求明細</span><span class="sxs-lookup"><span data-stu-id="9a85b-385">Invoice description</span></span></li>
<li><span data-ttu-id="9a85b-386">期日</span><span class="sxs-lookup"><span data-stu-id="9a85b-386">Due date</span></span></li>
<li><span data-ttu-id="9a85b-387">請求書通貨</span><span class="sxs-lookup"><span data-stu-id="9a85b-387">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a85b-388">モバイル エクスペリエンスで、請求書行のどのフィールドを、どのような順序で表示したいですか?</span><span class="sxs-lookup"><span data-stu-id="9a85b-388">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="9a85b-389">調達カテゴリ</span><span class="sxs-lookup"><span data-stu-id="9a85b-389">Procurement category</span></span></li>
<li><span data-ttu-id="9a85b-390">件数</span><span class="sxs-lookup"><span data-stu-id="9a85b-390">Quantity</span></span></li>
<li><span data-ttu-id="9a85b-391">単価</span><span class="sxs-lookup"><span data-stu-id="9a85b-391">Unit price</span></span></li>
<li><span data-ttu-id="9a85b-392">明細行の正味金額</span><span class="sxs-lookup"><span data-stu-id="9a85b-392">Line net amount</span></span></li>
<li><span data-ttu-id="9a85b-393">1099 金額</span><span class="sxs-lookup"><span data-stu-id="9a85b-393">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a85b-394">請求書にはいくつの請求書明細行がありますか?</span><span class="sxs-lookup"><span data-stu-id="9a85b-394">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="9a85b-395">80-20 ルールをここで適用し、80 パーセントを最適化します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-395">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="9a85b-396">5</span><span class="sxs-lookup"><span data-stu-id="9a85b-396">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a85b-397">ユーザーは、レビュー中にモバイル デバイス上の勘定配賦 (請求書コーディング) を見たいでしょうか?</span><span class="sxs-lookup"><span data-stu-id="9a85b-397">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="9a85b-398">有</span><span class="sxs-lookup"><span data-stu-id="9a85b-398">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a85b-399">請求書行にはいくつの勘定配賦 (拡張価格、消費税、料金、など) がありますか?</span><span class="sxs-lookup"><span data-stu-id="9a85b-399">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="9a85b-400">再度、80-20 ルールを適用します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-400">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="9a85b-401">拡張価格: 2 売上税: 2 料金: 2</span><span class="sxs-lookup"><span data-stu-id="9a85b-401">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a85b-402">請求書には請求書ヘッダーに勘定配賦も含まれていますか?</span><span class="sxs-lookup"><span data-stu-id="9a85b-402">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="9a85b-403">もしそうなら、これらの勘定配賦はデバイス上で利用できるはずですか?</span><span class="sxs-lookup"><span data-stu-id="9a85b-403">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="9a85b-404">不使用</span><span class="sxs-lookup"><span data-stu-id="9a85b-404">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a85b-405">ユーザーはデバイス上の請求書の添付ファイルを見たいですか?</span><span class="sxs-lookup"><span data-stu-id="9a85b-405">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="9a85b-406">有</span><span class="sxs-lookup"><span data-stu-id="9a85b-406">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="9a85b-407">次のステップ</span><span class="sxs-lookup"><span data-stu-id="9a85b-407">Next steps</span></span>

<span data-ttu-id="9a85b-408">シナリオ 2 の要件に基づいて、シナリオ 1 で以下のバリエーションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-408">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="9a85b-409">モバイル アプリ エクスペリエンスを向上するには、このセクションを使用してください。</span><span class="sxs-lookup"><span data-stu-id="9a85b-409">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="9a85b-410">シナリオ 2 では、より多くの請求書行が予想されるため、以下のデザイン変更により、モバイル デバイスのユーザー エクスペリエンスが最適化されます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-410">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="9a85b-411">(シナリオ 1 のように) 詳細ページで請求書の行を表示する代わりに、別のモバイル ページに行を表示することを選択できます。</span><span class="sxs-lookup"><span data-stu-id="9a85b-411">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="9a85b-412">このシナリオでは複数の請求書行が予想されるため、**VendMobileInvoiceAllDistributionTree** ページを使用してモバイルの配布ページを設計すると (シナリオ 1 のように)、ユーザーは行を配布に関連付けるのが紛らわしく感じる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9a85b-412">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="9a85b-413">したがって、**VendMobileInvoiceLineDistributionTree** ページを使用して配布ページを設計します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-413">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="9a85b-414">理想的には、このシナリオでは、配布を請求明細行のコンテキストで表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a85b-414">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="9a85b-415">したがって、ユーザーが行にドリルダウンして配布ページを表示できることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9a85b-415">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="9a85b-416">シナリオ 1 のヘッダーおよび詳細ページの場合と同様に、ページ リンク機能を使用してドリルスルーを確立します。</span><span class="sxs-lookup"><span data-stu-id="9a85b-416">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="9a85b-417">シナリオ 2 の配布では、複数の金額タイプ (消費税、請求など) が予想されるため、金額タイプの説明を表示すると便利です。</span><span class="sxs-lookup"><span data-stu-id="9a85b-417">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="9a85b-418">(この情報はシナリオ 1 では省略しました。)</span><span class="sxs-lookup"><span data-stu-id="9a85b-418">(We omitted this information in scenario 1.)</span></span>





