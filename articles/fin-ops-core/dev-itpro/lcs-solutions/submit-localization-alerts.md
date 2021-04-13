---
title: 国または地域固有の規制機能に関わる通知を送信
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して、Localization および Translation service を通じて警告を送信する方法について説明します。
author: ShylaThompson
ms.date: 02/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 27791
ms.assetid: b37140b4-5d6f-460f-ae36-f0d7bd90c0d3
ms.search.region: global
ms.author: janeaug
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e17684a686b99187c32aeb9ec7b4beb855b1a528
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745293"
---
# <a name="submit-alerts-about-countryregion-specific-regulatory-features"></a><span data-ttu-id="f6c1e-103">国または地域固有の規制機能に関わる通知を送信</span><span class="sxs-lookup"><span data-stu-id="f6c1e-103">Submit alerts about country/region-specific regulatory features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6c1e-104">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して、Dynamics 規制警告送信サービスを通じて警告を送信する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-104">This topic describes how to use Microsoft Dynamics Lifecycle Services (LCS) to submit alerts through the  Dynamics regulatory alert submission service.</span></span> <span data-ttu-id="f6c1e-105">このトピックは、計画およびリリースされた規制機能を、LCS 問題検索を使用して追跡する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-105">This topic also explains how to track planned and released regulatory features through LCS Issue search.</span></span> 

<a name="accessing-the-regulatory-alert-submission-service"></a><span data-ttu-id="f6c1e-106">規制の警告の送信サービスへのアクセス</span><span class="sxs-lookup"><span data-stu-id="f6c1e-106">Accessing the regulatory alert submission service</span></span>
-------------------------------------------------

<span data-ttu-id="f6c1e-107">Dynamics Lifecycle Services (LCS) のプロジェクトで、ページの右側までスクロールしてから、**追加ツール** の **警告サービス** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-107">In Dynamics Lifecycle Services (LCS), in your project, scroll to the right side of the page, and then, under **More tools**, click the **Alert service** tile.</span></span> 

<span data-ttu-id="f6c1e-108">**Dynamics 規制の警告の送信** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-108">The **Dynamics regulatory alert submission** page appears.</span></span> <span data-ttu-id="f6c1e-109">このページを使用すると、個人または組織が以前に提出したすべての警告を表示できます。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-109">You can use this page to view any alerts that have previously been submitted by you or your organization.</span></span>

## <a name="submitting-a-regulatory-alert"></a><span data-ttu-id="f6c1e-110">規制の警告の送信</span><span class="sxs-lookup"><span data-stu-id="f6c1e-110">Submitting a regulatory alert</span></span>
<span data-ttu-id="f6c1e-111">新しい規制アラートを入力するには、**Dynamics 規制アラートの送信** ページの上部にあるプラス記号 (**+**) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-111">To enter a new regulatory alert, click the plus sign (**+**) at the top of the **Dynamics regulatory alert submission** page, above the filter.</span></span> <span data-ttu-id="f6c1e-112">**送信を警告** ウィザードが起動します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-112">The **Alert submission** wizard starts.</span></span> <span data-ttu-id="f6c1e-113">このウィザードでは次のタスクを完了することができます。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-113">You can complete the following tasks in this wizard:</span></span>

- <span data-ttu-id="f6c1e-114">既存の規制項目を検索します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-114">Search for existing regulatory items.</span></span>
- <span data-ttu-id="f6c1e-115">業務プロセスを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-115">Attach business processes.</span></span>
- <span data-ttu-id="f6c1e-116">警告の説明をします。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-116">Describe an alert.</span></span>
- <span data-ttu-id="f6c1e-117">送信を確認します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-117">Confirm submissions.</span></span>

### <a name="search-for-existing-regulatory-items"></a><span data-ttu-id="f6c1e-118">既存の規制項目を検索</span><span class="sxs-lookup"><span data-stu-id="f6c1e-118">Search for existing regulatory items</span></span>

<span data-ttu-id="f6c1e-119">問題検索を使用して、警告に関連する規制機能が既に存在するかどうかを識別します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-119">Use Issue search to identify whether a regulatory feature, that is related to the alert, already exists.</span></span>

1.  <span data-ttu-id="f6c1e-120">キーワード、国/地域、 Microsoft Knowledge Base (KB) 番号または Application Object Tree (AOT) オブジェクトなどの検索用語を入力します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-120">Enter a search term, such as a keyword, country/region, Microsoft Knowledge Base (KB) number, or Application Object Tree (AOT) object.</span></span> <span data-ttu-id="f6c1e-121">検索ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-121">Click the search button.</span></span> <span data-ttu-id="f6c1e-122">製品問題または規制機能のいずれかに、検索用語を含むすべての項目が検索結果に表示されます。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-122">Any items that include the search term, in either product issues or regulatory features, appear in the search results.</span></span> <span data-ttu-id="f6c1e-123">使用可能なフィルターを使用して、検索を絞ることができます。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-123">You can narrow the search by using the filters that are available.</span></span>
2.  <span data-ttu-id="f6c1e-124">ユーザーが探している規制における機能がない場合は、ブラウザー ウィンドウの下部にある **規制に関する警告を送信** をクリックし、規制に関する警告を送信します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-124">If you don't find the regulatory feature that you're looking for, you can submit a regulatory alert by clicking **Submit regulatory alert** at the bottom of the browser window.</span></span> 

### <a name="attach-business-processes"></a><span data-ttu-id="f6c1e-125">業務プロセスの関連付け</span><span class="sxs-lookup"><span data-stu-id="f6c1e-125">Attach business processes</span></span>

1.  <span data-ttu-id="f6c1e-126">**グローバル業務プロセス ライブラリ** リストで、業務プロセス ライブラリを選択できます。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-126">In the **Global business process libraries** list, select business process libraries.</span></span>
2.  <span data-ttu-id="f6c1e-127">検索語句に関連する業務プロセスを見つける検索基準を入力します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-127">Enter search criteria to find business processes that are related to the search term.</span></span> <span data-ttu-id="f6c1e-128">これらのビジネス プロセスは黄色で強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-128">These business processes are highlighted in yellow.</span></span>
3.  <span data-ttu-id="f6c1e-129">ページの右側にある一覧で、1 つまたは複数の関連する業務プロセスを選択し、左側のフィールドまでドラッグします。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-129">In the list on the right side of the page, select one or more related business processes, and drag them into the field on the left .</span></span> <span data-ttu-id="f6c1e-130">完了後、選択した業務プロセスをクリアすることでさらに編集することができます。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-130">After you've finished, you can edit them further by clearing the selection of business processes.</span></span>
4.  <span data-ttu-id="f6c1e-131">警告に選択した業務プロセスを追加します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-131">Add the selected business processes to the alert.</span></span> 

### <a name="describe-the-alert"></a><span data-ttu-id="f6c1e-132">警告の説明</span><span class="sxs-lookup"><span data-stu-id="f6c1e-132">Describe the alert</span></span>

1. <span data-ttu-id="f6c1e-133">適切なフィールドに警告に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-133">Enter information about the alert in the appropriate fields.</span></span> <span data-ttu-id="f6c1e-134">必須フィールドは赤いアスタリスクで示されます。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-134">Required fields are indicated by a red asterisk.</span></span> <span data-ttu-id="f6c1e-135">次のテーブルでは、**警告の説明** ページのフィールドの詳細について説明します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-135">The following table provides more information about the fields on the **Describe the alert** page.</span></span>

    <table >
            <tr>
                <td >
                <p><span data-ttu-id="f6c1e-136"><strong>フィールド</strong></span><span class="sxs-lookup"><span data-stu-id="f6c1e-136"><strong>Field</strong></span></span></p>
                </td>
                <td >
                <p><span data-ttu-id="f6c1e-137"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="f6c1e-137"><strong>Description</strong></span></span></p>
                </td>
            </tr>
            <tr>
                <td>
                <p><span data-ttu-id="f6c1e-138">肩書き</span><span class="sxs-lookup"><span data-stu-id="f6c1e-138">Title</span></span></p>
                </td>
                <td>
                <p><span data-ttu-id="f6c1e-139">影響の区分を識別するために、内容を示すタイトルを入力します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-139">Enter a descriptive title to identify the area of impact.</span></span> <span data-ttu-id="f6c1e-140">たとえば、<strong>2018 年 1 月 1 日時点での請求書ドキュメントの変更</strong>を入力します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-140">For example, enter <strong>Changes in invoice document as of January 1, 2018</strong>.</span></span></p>
                </td>
            </tr>
            <tr>
                <td>
                <p><span data-ttu-id="f6c1e-141">説明</span><span class="sxs-lookup"><span data-stu-id="f6c1e-141">Description</span></span></p>
                </td>
                <td>
                <p><span data-ttu-id="f6c1e-142">法律の簡単な概要を入力します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-142">Enter a brief overview of the law.</span></span> <span data-ttu-id="f6c1e-143">説明は、エンタープライズ リソース プランニング (ERP) に関連する問題に重点を置く必要があります。これにより、ユーザーは、最初に法律を読むことなく、要件を高いレベルで理解することができます。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-143">Your description should focus on issues that are relevant to enterprise resource planning (ERP), so that users can understand the requirements at a high level without having to read the legislation first.</span></span> </p>
                </td>
            </tr>
            <tr>
                <td>
                <p><span data-ttu-id="f6c1e-144">国</span><span class="sxs-lookup"><span data-stu-id="f6c1e-144">Country</span></span></p>
                </td>
                <td>
                <p><span data-ttu-id="f6c1e-145">法律が適用される国または地域を選択します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-145">Select the country or region that the legislation applies to.</span></span> </p>
                </td>
            </tr>
            <tr>
                <td>
                <p><span data-ttu-id="f6c1e-146">業</span><span class="sxs-lookup"><span data-stu-id="f6c1e-146">Industry</span></span></p>
                </td>
                <td>
                <p><span data-ttu-id="f6c1e-147">要件が特定の業界にのみ適用される場合は、業界を選択します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-147">Select the industry, if the requirement applies only to specific industries.</span></span> <span data-ttu-id="f6c1e-148">たとえば、<strong>公的機関</strong>、<strong>コマース</strong>、または<strong>製造</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-148">For example, select <strong>Public sector</strong>, <strong>Commerce</strong>, or <strong>Manufacturing</strong>.</span></span> </p><br/>            </td>
            </tr>
            <tr>
                <td>
                <p><span data-ttu-id="f6c1e-149">機能リファレンス</span><span class="sxs-lookup"><span data-stu-id="f6c1e-149">Feature reference</span></span></p>
                </td>
                <td>
                <p><span data-ttu-id="f6c1e-150">分かっている場合は、機能リファレンスを入力します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-150">Enter the feature reference, if you know it.</span></span></p>
                </td>
            </tr>
            <tr>
                <td>
                <p><span data-ttu-id="f6c1e-151">法執行日</span><span class="sxs-lookup"><span data-stu-id="f6c1e-151">Law enforcement date</span></span></p>
                </td>
                <td>
                <p><span data-ttu-id="f6c1e-152">影響を受ける顧客が法律に準拠し始める必要がある日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-152">Select the date when affected customers must start to comply with the law.</span></span>  </p>
                </td>
            </tr>
            <tr>
                <td>
                <p><span data-ttu-id="f6c1e-153">政府発表日</span><span class="sxs-lookup"><span data-stu-id="f6c1e-153">Government announcement date</span></span></p>
                </td>
                <td>
                <p><span data-ttu-id="f6c1e-154">所轄官庁が変更を発表した日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-154">Select the date when the authority announced the change.</span></span> </p>
                </td>
            </tr>
            <tr>
                <td>
                <p><span data-ttu-id="f6c1e-155">最新の提出日</span><span class="sxs-lookup"><span data-stu-id="f6c1e-155">Latest filing date</span></span></p>
                </td>
                <td>
                <p><span data-ttu-id="f6c1e-156">新しいまたは変更されたレポートの最初の提出期限を選択します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-156">Select the deadline for the first submission of the new or changed report.</span></span>     </p>
                </td>
            </tr>
            <tr>
                <td>
                <p><span data-ttu-id="f6c1e-157">法律へのリンク</span><span class="sxs-lookup"><span data-stu-id="f6c1e-157">Link to legislation</span></span> </p>
                </td>
                <td>
                <p><span data-ttu-id="f6c1e-158">発行済みの法律、解釈規定、実装ガイダンスまたはユーザーが要件を理解または実装するのに役立つその他の有用な文書へのリンクを 1 つ以上入力します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-158">Enter one or more links to the published law, interpretation guideline, implementation guidance, or any other useful documentation that will help users understand or implement the requirement.</span></span></p>
                </td>
            </tr>
            <tr>
                <td>
                <p><span data-ttu-id="f6c1e-159">屋号</span><span class="sxs-lookup"><span data-stu-id="f6c1e-159">Company name</span></span></p>
                </td>
                <td>
                <p><span data-ttu-id="f6c1e-160">警告を送信しているユーザーの会社名を入力します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-160">Enter the company name for the person who is submitting the alert.</span></span>         </p>
                </td>
            </tr>
            <tr>
                <td>
                <p><span data-ttu-id="f6c1e-161">連絡先名</span><span class="sxs-lookup"><span data-stu-id="f6c1e-161">Contact name</span></span></p>
                </td>
                <td>
                <p><span data-ttu-id="f6c1e-162">警告を送信している担当者の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-162">Enter the name of the person who is submitting the alert.</span></span>     </p>
                </td>
            </tr>
            <tr>
                <td>
                <p><span data-ttu-id="f6c1e-163">連絡先の電子メール</span><span class="sxs-lookup"><span data-stu-id="f6c1e-163">Contact email</span></span></p>
                </td>
                <td>
                <p><span data-ttu-id="f6c1e-164">警告の送信者の電子メール アドレス。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-164">The email address of the person who is submitting the alert.</span></span>   </p>
                </td>
            </tr>
            <tr>
                <td>
                <p><span data-ttu-id="f6c1e-165">業務プロセス</span><span class="sxs-lookup"><span data-stu-id="f6c1e-165">Business process</span></span></p>
                </td>
                <td>
                <p><span data-ttu-id="f6c1e-166"><strong>警告の送信</strong> ウィザードで選択したビジネスプロセス。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-166">The business processes that you selected through the <strong>Alert submission</strong> wizard.</span></span></p>
                </td>
            </tr>
            <tr>
                <td><span data-ttu-id="f6c1e-167">コメント</span><span class="sxs-lookup"><span data-stu-id="f6c1e-167">Comments</span></span></td>
                <td>
                <p><span data-ttu-id="f6c1e-168">ユーザーが要件を理解または実装するのに役立つ追加情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-168">Enter any additional information that might be help users understand or implement the requirement.</span></span> <span data-ttu-id="f6c1e-169"><strong>送信</strong>をクリックしてコメントを保存します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-169">Click <strong>Submit</strong> to save your comment.</span></span> <span data-ttu-id="f6c1e-170">複数のコメントを追加でき、個別に提出する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-170">Multiple comments can be added and should be submitted separately.</span></span> <span data-ttu-id="f6c1e-171">コメントは追加された順に保存されます。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-171">Comments are saved in the order that they are added.</span></span> </p>
                </td>
            </tr>
            <tr>
                <td> <span data-ttu-id="f6c1e-172">アタッチメント</span><span class="sxs-lookup"><span data-stu-id="f6c1e-172">Attachments</span></span> </td>
                <td> <p><span data-ttu-id="f6c1e-173"><strong>アップロード</strong> ボタンをクリックし、添付ファイルとして追加するファイルを選択して参照します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-173">Click the <strong>Upload</strong> button, and then browse to select a file to add as an attachment.</span></span> <span data-ttu-id="f6c1e-174">ファイルを選択した後、アップロードされリンクされたファイルとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-174">After you select the file, it&#39;s uploaded and appears as a linked file.</span></span> <span data-ttu-id="f6c1e-175">各サイズが 5 MB のファイルを、最大 3 つ追加することができます。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-175">You can add up to three files that have a size of 5 MB each.</span></span> <span data-ttu-id="f6c1e-176">添付されたファイルを削除するには、ファイルのタイトルの下にある <strong>削除</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-176">To delete files that have been attached, click <strong>Remove</strong> under the title of the file.</span></span> <span data-ttu-id="f6c1e-177"><strong>注記:</strong> 添付ファイルは公開されているものでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-177"><strong>Note</strong> Attachments must be publicly available materials.</span></span> <span data-ttu-id="f6c1e-178">これらは妥当性や顧客固有/パートナー固有のものではありません。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-178">They can&#39;t be propriety or customer-specific/partner-specific.</span></span></p>
                </td>
            </tr>
    </table>

2.  <span data-ttu-id="f6c1e-179">すべての情報入力が完了したら、同意チェック ボックスを選択します (**この規制の警告を送信することで、Microsoft がこの警告に関する追加の情報を入手する目的で私に連絡することに同意します。Microsoft のプライバシーに関する声明**) 。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-179">After you've finished entering all the information, select the consent check box (**By submitting this regulatory alert, I consent to Microsoft contacting me for additional information about this alert. Microsoft Privacy Statement.**).</span></span> <span data-ttu-id="f6c1e-180">チェック ボックスを選択すると、**送信** ボタンが使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-180">When you select the check box, the **Submit** button becomes available.</span></span>
3.  <span data-ttu-id="f6c1e-181">警告を保存して送信するには、**送信** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-181">Click **Submit** to save and submit the alert.</span></span>

<span data-ttu-id="f6c1e-182">すべての必要な情報を持っていない場合、または警告を送信する準備が整っていない場合は、部分的に完了した警告を保存することができます。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-182">If you don't have all of the required information, or if you're not yet ready to submit the alert, you can save a partially completed alert.</span></span>

### <a name="confirm-your-submission"></a><span data-ttu-id="f6c1e-183">送信を確認する</span><span class="sxs-lookup"><span data-stu-id="f6c1e-183">Confirm your submission</span></span>

-   <span data-ttu-id="f6c1e-184">警告が正常に送信されると、確認メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-184">When the alert is successfully submitted, you receive a confirmation message.</span></span> <span data-ttu-id="f6c1e-185">**完了** をクリックし、ウィザードを終了します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-185">Click **Done** to exit the wizard.</span></span>
-   <span data-ttu-id="f6c1e-186">送信する前に警告を保存すると、警告 ID が生成され、警告が保存されたという確認を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-186">If you save the alert before you submit it, an alert ID is generated, and you receive confirmation that the alert has been saved.</span></span>

## <a name="track-the-status-of-regulatory-features-in-issue-search"></a><span data-ttu-id="f6c1e-187">問題検索の規制機能の状態を追跡する</span><span class="sxs-lookup"><span data-stu-id="f6c1e-187">Track the status of regulatory features in Issue search</span></span>
<span data-ttu-id="f6c1e-188">LCS で問題検索を使用して計画済みおよびリリース済みの規制フィーチャー、および任意の関連ローカライズ ドキュメント、証明、およびレポートを見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-188">You can use Issue search in LCS to find planned and released regulatory features, and any associated localization documentation, certifications, and reports.</span></span> <span data-ttu-id="f6c1e-189">検索を規制機能に絞り込むには、次のフィルターを使用します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-189">To narrow your search to regulatory features, use the following filters:</span></span>

-   <span data-ttu-id="f6c1e-190">**カテゴリ** - **規制機能** のみを選択します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-190">**Category** - Select **Regulatory feature** only.</span></span>
-   <span data-ttu-id="f6c1e-191">**国/地域** - **&gt;** をクリックして、目的の国/地域を選択します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-191">**Country/region** - Click **&gt;** to select the country/region that you're interested in.</span></span>

<span data-ttu-id="f6c1e-192">検索範囲をさらに絞り込むには、次の追加フィルターを適用します</span><span class="sxs-lookup"><span data-stu-id="f6c1e-192">To narrow the search even more, you can apply the following additional filters</span></span>

-   <span data-ttu-id="f6c1e-193">**製品** - 興味のある製品と製品のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-193">**Product** - Select the products and product versions that you're interested in.</span></span>
-   <span data-ttu-id="f6c1e-194">**ステータス** - 特定のステータスを選択してください。</span><span class="sxs-lookup"><span data-stu-id="f6c1e-194">**Status** - Select specific statuses.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
