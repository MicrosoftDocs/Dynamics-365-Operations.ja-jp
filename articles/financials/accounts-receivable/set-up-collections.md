---
title: "貸方転記および取立の設定"
description: "この品目では、コレクション機能の設定方法が説明されます。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustCollectionsActivitiesListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14031
ms.assetid: dcc6da2f-9af5-4f1d-abaa-b72967b66979
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 09296ae02c690fa683d853cc91a5abf243bcafa7
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-credit-and-collections"></a><span data-ttu-id="a4fc9-103">貸方転記および取立の設定</span><span class="sxs-lookup"><span data-stu-id="a4fc9-103">Set up Credit and collections</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a4fc9-104">この品目では、コレクション機能の設定方法が説明されます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-104">This article explains how to set up the collections functionality.</span></span>

<a name="set-up-aging-period-definitions"></a><span data-ttu-id="a4fc9-105">エイジング期間の定義の設定</span><span class="sxs-lookup"><span data-stu-id="a4fc9-105">Set up aging period definitions</span></span>
-------------------------------

<span data-ttu-id="a4fc9-106">エイジング期間の定義の設定</span><span class="sxs-lookup"><span data-stu-id="a4fc9-106">Set up an aging period definition.</span></span> <span data-ttu-id="a4fc9-107">エイジング期間の定義は、[**エイジングした残高**]、[**回収活動**]、および [**回収ケース**] リスト ページで表示される列で定義します。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-107">An aging period definition defines the columns that appear on the **Aged balances**, **Collections activities**, and **Collections cases** list pages.</span></span> <span data-ttu-id="a4fc9-108">また、[**コレクション**] ページに表示される期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-108">It also defines the periods that appear on the **Collections** page.</span></span> <span data-ttu-id="a4fc9-109">顧客プールを設定する場合、プールのエイジング期間の定義が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-109">If a customer pool is set up, the aging period definition for the pool is used.</span></span> <span data-ttu-id="a4fc9-110">プールが設定されていない場合、[**売掛金勘定パラメーター**] ページで指定されている既定のエイジング期間の定義が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-110">If no pools are set up, the default aging period definition that is specified on the **Accounts receivable parameters** page is used.</span></span> <span data-ttu-id="a4fc9-111">既定のエイジング期間の定義が指定されていない場合、[**エイジング期間の定義**] ページの最初のエイジング期間の定義が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-111">If no default aging period definition is specified, the first aging period definition on the **Aging period definitions** page is used.</span></span>

## <a name="create-an-aging-snapshot"></a><span data-ttu-id="a4fc9-112">経過期間スナップショットの作成</span><span class="sxs-lookup"><span data-stu-id="a4fc9-112">Create an aging snapshot</span></span>
<span data-ttu-id="a4fc9-113">すべての顧客または顧客プール内の顧客に対して経過期間スナップショット レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-113">Create aging snapshot records for all customers or for the customers in a customer pool.</span></span> <span data-ttu-id="a4fc9-114">経過期間スナップショットの情報は、[**エイジングした残高**] リスト ページと [**コレクション**] ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-114">Aging snapshot information appears on the **Aged balances** list page and on the **Collections** page.</span></span> <span data-ttu-id="a4fc9-115">リスト ページを使用する前に、経過期間スナップショットを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-115">You must create an aging snapshot before you can use the list page.</span></span> <span data-ttu-id="a4fc9-116">リスト ページでは、経過期間スナップショットを作成した顧客に対してのみ情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-116">The list page shows information only for customers that an aging snapshot has been created for.</span></span>

## <a name="optional-set-up-customer-pools"></a><span data-ttu-id="a4fc9-117">オプション: 顧客プールの設定</span><span class="sxs-lookup"><span data-stu-id="a4fc9-117">Optional: Set up customer pools</span></span>
<span data-ttu-id="a4fc9-118">顧客グループを表すための顧客プールを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-118">You can set up customer pools to represent groups of customers.</span></span> <span data-ttu-id="a4fc9-119">[**回収**] ページで、または経過期間スナップショットを作成するとき、[**回収**] リスト ページに表示される顧客情報のフィルターとして顧客プールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-119">You can use customer pools as filters for the customer information that appears on **Collections** list pages, on the **Collections** page, or when you create aging snapshots.</span></span>

## <a name="optional-create-a-collections-team"></a><span data-ttu-id="a4fc9-120">オプション: コレクション チームの作成</span><span class="sxs-lookup"><span data-stu-id="a4fc9-120">Optional: Create a collections team</span></span>
<span data-ttu-id="a4fc9-121">組織内の複数の回収作業を行う場合、回収チームを設定できますします。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-121">If multiple people in your organization do collections work, you can set up a collections team.</span></span> <span data-ttu-id="a4fc9-122">[**売掛金勘定パラメーター**] ページでチームを選択できます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-122">You can select the team on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="a4fc9-123">回収チームを作成しない場合、[**回収代行業者**] ページで回収代行業者を設定するとき、チームが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-123">If you don't create a collections team, a team is created automatically when you set up collections agents on the **Collections agent** page.</span></span>

## <a name="set-up-a-collections-case-category"></a><span data-ttu-id="a4fc9-124">コレクション ケース カテゴリの設定</span><span class="sxs-lookup"><span data-stu-id="a4fc9-124">Set up a collections case category</span></span>
<span data-ttu-id="a4fc9-125">ケースを使用して回収作業を整理する場合は、[**回収**] カテゴリ タイプがあるケース カテゴリを設定します。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-125">If you will use cases to organize your collections work, set up a case category that has the **Collections** category type.</span></span> <span data-ttu-id="a4fc9-126">この設定は、[**回収**] ページのケース機能を使用する場合に限られます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-126">This setup is required only if you want to use the case functionality on the **Collections** page.</span></span>

## <a name="set-up-journal-names-settlement-writeoff-and-nsf"></a><span data-ttu-id="a4fc9-127">仕訳帳名 (決済、損金処理、および NSF) の設定</span><span class="sxs-lookup"><span data-stu-id="a4fc9-127">Set up journal names (settlement, writeoff, and NSF)</span></span>
<span data-ttu-id="a4fc9-128">**回収**ページでトランザクションが処理されるときに使用する仕訳帳名を設定します。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-128">Set up the journal names that are used when transactions are processed on the **Collections** page.</span></span> <span data-ttu-id="a4fc9-129">この処理には、トランザクションの決済、トランザクションの損金処理、預金不足 (NSF) 支払の処理が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-129">This processing includes settlement of a transaction, write-off of a transaction, and processing of a not sufficient funds (NSF) payment.</span></span>

| <span data-ttu-id="a4fc9-130">説明</span><span class="sxs-lookup"><span data-stu-id="a4fc9-130">Description</span></span> | <span data-ttu-id="a4fc9-131">仕訳帳タイプ</span><span class="sxs-lookup"><span data-stu-id="a4fc9-131">Journal type</span></span>     |
|-------------|------------------|
| <span data-ttu-id="a4fc9-132">居住地</span><span class="sxs-lookup"><span data-stu-id="a4fc9-132">Settlement</span></span>  | <span data-ttu-id="a4fc9-133">顧客支払</span><span class="sxs-lookup"><span data-stu-id="a4fc9-133">Customer payment</span></span> |
| <span data-ttu-id="a4fc9-134">損金処理</span><span class="sxs-lookup"><span data-stu-id="a4fc9-134">Write-off</span></span>   | <span data-ttu-id="a4fc9-135">毎日</span><span class="sxs-lookup"><span data-stu-id="a4fc9-135">Daily</span></span>            |
| <span data-ttu-id="a4fc9-136">NSF</span><span class="sxs-lookup"><span data-stu-id="a4fc9-136">NSF</span></span>         | <span data-ttu-id="a4fc9-137">顧客支払</span><span class="sxs-lookup"><span data-stu-id="a4fc9-137">Customer payment</span></span> |

## <a name="set-up-a-reason-code-for-writeoff-transactions"></a><span data-ttu-id="a4fc9-138">損金処理トランザクションの理由コードの設定</span><span class="sxs-lookup"><span data-stu-id="a4fc9-138">Set up a reason code for writeoff transactions</span></span>
<span data-ttu-id="a4fc9-139">[**回収**] ページでトランザクションが損金処理されているときに使用する既定の理由コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-139">Set up the default reason code that is used when transactions are written off on the **Collections** page.</span></span> <span data-ttu-id="a4fc9-140">損金処理プロセス中にコードを変更できます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-140">You can change the code during the write-off process.</span></span>

## <a name="set-up-a-folder-for-email-attachments-and-create-email-templates"></a><span data-ttu-id="a4fc9-141">電子メール添付ファイルのフォルダの設定と、電子メール テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="a4fc9-141">Set up a folder for email attachments and create email templates</span></span>
<span data-ttu-id="a4fc9-142">[**回収**] ページから Microsoft Excel の添付ファイルを持つ電子メール メッセージを送信する場合、これらのメッセージのオプションの電子メール テンプレートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-142">If you will send email messages from the **Collections** page that have Microsoft Excel attachments, you can create optional email templates for those messages.</span></span>

## <a name="set-up-accounts-receivable-parameters-for-collections"></a><span data-ttu-id="a4fc9-143">コレクションの売掛金勘定モジュール パラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="a4fc9-143">Set up accounts receivable parameters for collections</span></span>
<span data-ttu-id="a4fc9-144">[**回収**] タブに表示される売掛金勘定パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-144">Set up the accounts receivable parameters that appear on the **Collections** tab.</span></span>

## <a name="optional-set-up-collections-agents"></a><span data-ttu-id="a4fc9-145">オプション: 回収代行業者の設定</span><span class="sxs-lookup"><span data-stu-id="a4fc9-145">Optional: Set up collections agents</span></span>
<span data-ttu-id="a4fc9-146">組織内の複数の者が回収作業を行う場合、回収代行業者を設定できます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-146">If multiple people in your organization do collections work, you can set up collections agents.</span></span> <span data-ttu-id="a4fc9-147">回収代行業者は、[**ユーザー関係**] ページでユーザーとして設定されている作業者です。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-147">A collections agent is a worker who is set up as a user on the **User relations** page.</span></span> <span data-ttu-id="a4fc9-148">顧客プール (顧客クエリ) を回収代行業者に割り当てて、代行業者の作業の整理を容易にすることができます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-148">You can assign customer pools (customer queries) to collections agents to help the agents organize their work.</span></span> <span data-ttu-id="a4fc9-149">回収代行業者は、[**売掛金勘定パラメーター**] ページで選択されたチームに追加されます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-149">The collections agents are added to the team that is selected on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="a4fc9-150">チームがそのページで選択されていない場合、[**回収**] という名前の新しいチームが自動的に作成され、回収代行業者はそのチームに追加されます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-150">If a team isn't selected on that page, a new team that is named **Collections** is automatically created, and the collections agents are added to that team.</span></span>

## <a name="set-up-a-writeoff-account"></a><span data-ttu-id="a4fc9-151">損金処理勘定の設定</span><span class="sxs-lookup"><span data-stu-id="a4fc9-151">Set up a writeoff account</span></span>
<span data-ttu-id="a4fc9-152">トランザクションの損金処理時に一般会計の損金処理エントリに対して使用される損金処理勘定を設定します。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-152">Set up the write-off account that is used for the general ledger write-off entry when a transaction is written off.</span></span> <span data-ttu-id="a4fc9-153">この勘定は、顧客転記プロファイルに保存されます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-153">This account is stored on the customer posting profile.</span></span>

## <a name="set-up-nsf-information-for-bank-accounts"></a><span data-ttu-id="a4fc9-154">銀行口座の NSF 情報の設定</span><span class="sxs-lookup"><span data-stu-id="a4fc9-154">Set up NSF information for bank accounts</span></span>
<span data-ttu-id="a4fc9-155">NSF 支払が [**回収**] ページで指定される時に、正しい仕訳が含まれるように銀行口座を更新します。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-155">Update bank accounts so that they have the correct journal when NSF payments are identified on the **Collections** page.</span></span> <span data-ttu-id="a4fc9-156">[**通貨管理**] タブの [**NSF 支払仕訳帳**] フィールドで、支払仕訳帳を選択します。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-156">On the **Currency management** tab,  in the **NSF payment journal** field, select a payment journal.</span></span>

## <a name="set-up-outlook-settings-for-users-of-the-collections-page"></a><span data-ttu-id="a4fc9-157">回収ページのユーザーの Outlook 設定のセットアップ</span><span class="sxs-lookup"><span data-stu-id="a4fc9-157">Set up Outlook settings for users of the Collections page</span></span>
<span data-ttu-id="a4fc9-158">[**回収**] ページを使用して作業者が活動を作成したり、電子メール メッセージを送信する前に、[**Microsoft Outlook の同期**] コンフィギュレーション キーが選択されていることと、Outlook の同期がこれらの作業者に対して設定されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-158">Before workers can create activities or send email messages by using the **Collections** page, you must verify that the **Microsoft Outlook synchronization** configuration key is selected, and that Outlook synchronization is set up for those workers.</span></span>

## <a name="set-up-email-and-address-settings-for-collections-customer-contacts"></a><span data-ttu-id="a4fc9-159">回収の顧客連絡先の電子メールとアドレスの設定のセットアップ</span><span class="sxs-lookup"><span data-stu-id="a4fc9-159">Set up email and address settings for collections customer contacts</span></span>
<span data-ttu-id="a4fc9-160">[**回収**] ページから顧客連絡先に電子メール メッセージを送信する場合は、それらの連絡先の電子メール アドレスを設定します。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-160">Set up email addresses for customer contacts if you want to send email messages to those contacts from the **Collections** page.</span></span> <span data-ttu-id="a4fc9-161">回収連絡先は、[**回収**] ページで既定の連絡先として使用されます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-161">The collections contact is used as the default contact on the **Collections** page.</span></span> <span data-ttu-id="a4fc9-162">明細書の住所を基本住所以外の住所にする必要がある場合は、顧客の明細書の住所を設定できます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-162">You can set up a statement address for a customer if statements should use an address other than the primary address.</span></span> 

<span data-ttu-id="a4fc9-163">顧客の [**貸方および取立**] クイック タブの [**回収連絡先**] フィールドで回収代行業者を使用する顧客の組織の従業員を選択します。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-163">On the **Credit and Collections** FastTab for a customer, in the **Collections contact** field, select the person in the customer organization who works with your collections agent.</span></span> <span data-ttu-id="a4fc9-164">この担当者は、[**回収**] ページで既定の連絡先として使用され、電子メール メッセージの送信先となります。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-164">This person is used as the default contact on the **Collections** page, and email messages are sent to him or her.</span></span> 

> [!NOTE] 
> <span data-ttu-id="a4fc9-165">顧客の回収連絡先が指定されていない場合、顧客の基本連絡先が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-165">If a collections contact isn't specified for a customer, the primary contact for the customer is used.</span></span> <span data-ttu-id="a4fc9-166">基本連絡先が指定されていない場合は、電子メール メッセージは、[**連絡先**] ページに記載されている最初のアドレスに送信されます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-166">If a primary contact isn't specified, email messages are sent to the first address that is listed on the **Contacts** page.</span></span>

## <a name="set-up-email-settings-for-salespeople"></a><span data-ttu-id="a4fc9-167">販売担当者の電子メール設定のセットアップ</span><span class="sxs-lookup"><span data-stu-id="a4fc9-167">Set up email settings for salespeople</span></span>
<span data-ttu-id="a4fc9-168">[**回収**] ページから販売担当者に電子メール メッセージを送信する場合は、販売担当者の電子メール アドレスを設定します。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-168">Set up email addresses for salespeople if you want to send email messages to salespeople from the **Collections** page.</span></span> <span data-ttu-id="a4fc9-169">各コミッション売上グループの各販売担当者の電子メール アドレスを設定します。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-169">Set up an email address for each sales representative in each commission sales group.</span></span> <span data-ttu-id="a4fc9-170">[**連絡先**] オプションで選択されている販売担当者は、電子メール メッセージが送信される既定の販売担当者です。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-170">The sales representative who has the **Contact** option selected is the default salesperson that email messages are sent to.</span></span> 

<span data-ttu-id="a4fc9-171">販売担当者が指定されていない場合、顧客の組織の主要販売担当者が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-171">If a sales representative isn't specified, the primary salesperson for the customer organization is used.</span></span> <span data-ttu-id="a4fc9-172">主要販売担当者が指定されていない場合は、電子メール メッセージは、ページに記載されている最初の販売担当者に送信されます。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-172">If a primary salesperson isn't specified, email messages are sent to the first salesperson who is listed on the page.</span></span>


<span data-ttu-id="a4fc9-173">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a4fc9-173">For more information, see the following topics:</span></span>

 - [<span data-ttu-id="a4fc9-174">督促状順序の作成</span><span class="sxs-lookup"><span data-stu-id="a4fc9-174">Create a collection letter sequence</span></span>](tasks/create-collection-letter-sequence.md)
 
 - [<span data-ttu-id="a4fc9-175">督促状の処理</span><span class="sxs-lookup"><span data-stu-id="a4fc9-175">Process collection letters</span></span>](tasks/process-collection-letters.md)
 
 - [<span data-ttu-id="a4fc9-176">取立情報の確認</span><span class="sxs-lookup"><span data-stu-id="a4fc9-176">Review collections information</span></span>](tasks/review-collections-information.md)


