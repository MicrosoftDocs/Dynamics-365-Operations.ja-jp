---
title: クレジット カード トランザクション データのアーカイブ
description: このトピックでは、クレジット カード トランザクションをアーカイブに保存することでデータベースの領域を解放できる、Microsoft Dynamics 365 Commerce のアーカイブ ジョブについて説明します。
author: rubendel
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: a36a61ab0fce83b15f22cfec69dc7b93443b5047
ms.sourcegitcommit: 245241ba80705a9c4738dba3ed812e844e81728c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/07/2021
ms.locfileid: "5131503"
---
# <a name="archive-credit-card-transaction-data"></a><span data-ttu-id="400e3-103">クレジット カード トランザクション データのアーカイブ</span><span class="sxs-lookup"><span data-stu-id="400e3-103">Archive credit card transaction data</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="400e3-104">このトピックでは、クレジット カード トランザクションをアーカイブに保存することでデータベースの領域を解放できる、Microsoft Dynamics 365 Commerce のアーカイブ ジョブについて説明します。</span><span class="sxs-lookup"><span data-stu-id="400e3-104">This topic describes an archival job in Microsoft Dynamics 365 Commerce that can help free up space in the database by archiving credit card transactions.</span></span> <span data-ttu-id="400e3-105">このジョブは、コマース バージョン 10.0.17 リリース時点で使用できます。</span><span class="sxs-lookup"><span data-stu-id="400e3-105">This job is available as of the Commerce version 10.0.17 release.</span></span>

<span data-ttu-id="400e3-106">クレジット カードの認証ごとに、認証バイナリ ラージ オブジェクト ([auth BLOB](#key-terms)) がデータベースに格納されます。</span><span class="sxs-lookup"><span data-stu-id="400e3-106">For every credit card authorization, the authentication binary large object ([auth blob](#key-terms)) is stored in the database.</span></span> <span data-ttu-id="400e3-107">Auth BLOB には、認証に関連するデータが含まれます。</span><span class="sxs-lookup"><span data-stu-id="400e3-107">Auth blobs contain data that is related to the authorization.</span></span> <span data-ttu-id="400e3-108">時間が経過すると、これらの auth BLOB は増加し、データベースの容量を大量に得ることができます。</span><span class="sxs-lookup"><span data-stu-id="400e3-108">Over time, these auth blobs can grow and take up a significant amount of space in the database.</span></span> <span data-ttu-id="400e3-109">このトピックに説明されているジョブを使用すると、Azure Blob Storage にエクスポートしデータベースからデータを削除することで、auth BLOB データをアーカイブすることができます。</span><span class="sxs-lookup"><span data-stu-id="400e3-109">The job that is described in this topic lets you archive auth blob data by exporting it to Azure Blob storage and then deleting the data from the database.</span></span>

<span data-ttu-id="400e3-110">アーカイブ ジョブのパラメータは、トランザクションの日数に基づいて指定されます。</span><span class="sxs-lookup"><span data-stu-id="400e3-110">The parameters for the archival job are based on the age of the transaction in days.</span></span> <span data-ttu-id="400e3-111">つまり、ジョブの **最小トランザクションの日数** フィールドが **365** 日に設定されている場合、たとえば 365 日以上経過しているクレジット カード認証に関するすべての XML データが、ジョブの実行時にアーカイブの対象になります。</span><span class="sxs-lookup"><span data-stu-id="400e3-111">In other words, if the **Minimum transaction age in days** field for the job is set to **365**, for example, all XML data about credit card authorizations that is older than 365 days will be subject to archiving when the job is run.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="400e3-112">アーカイブしたデータを簡単に復元できません。</span><span class="sxs-lookup"><span data-stu-id="400e3-112">Data can't easily be restored after it has been archived.</span></span> <span data-ttu-id="400e3-113">したがって、[リンクされた払戻し](#key-terms) の対象となるトランザクションはアーカイブする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="400e3-113">Therefore, transactions that are subject to [linked refunds](#key-terms) should not be archived.</span></span> <span data-ttu-id="400e3-114">たとえば、販売者の返品ポリシーで、2 日以内に同じクレジット カードへの払戻しをトランザクションで許可している場合、ジョブの **トランザクションの最小期間** フィールドは 730 日 (2年) に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="400e3-114">For example, if a merchant's returns policy allows transactions to be returned for refund to the same credit card within two years, the **Minimum transaction age in days** field for the job should be set to 730 days (two years).</span></span> <span data-ttu-id="400e3-115">この場合、730 日後にトランザクションが戻された場合、リンクされた払戻しを実行する必要がある XML は検出されません。</span><span class="sxs-lookup"><span data-stu-id="400e3-115">In this case, if a transaction is returned after 730 days, the XML that is required to do a linked refund won't be found.</span></span> <span data-ttu-id="400e3-116">したがって、顧客はクレジット カードまたはクレジット メモやギフト カードなどの他の支払方法に対する[スタンドアロンの払戻し](#key-terms) を通じて、払戻しを受け取る必要があります。</span><span class="sxs-lookup"><span data-stu-id="400e3-116">Therefore, the customer will have to be refunded via a [standalone refund](#key-terms) to either a credit card or some other payment method, such as a credit memo or gift card.</span></span>

## <a name="key-terms"></a><span data-ttu-id="400e3-117">重要な用語</span><span class="sxs-lookup"><span data-stu-id="400e3-117">Key terms</span></span>

| <span data-ttu-id="400e3-118">相談</span><span class="sxs-lookup"><span data-stu-id="400e3-118">Term</span></span> | <span data-ttu-id="400e3-119">説明</span><span class="sxs-lookup"><span data-stu-id="400e3-119">Description</span></span> |
|---|---|
| <span data-ttu-id="400e3-120">Auth BLOB</span><span class="sxs-lookup"><span data-stu-id="400e3-120">Auth blob</span></span> | <span data-ttu-id="400e3-121">クレジット カード プロセッサが支払要求に対して返す応答。</span><span class="sxs-lookup"><span data-stu-id="400e3-121">The response that a credit card processor returns for a payment request.</span></span> <span data-ttu-id="400e3-122">この応答は XML ファイルに格納され、時間の節約に基いてデータベースの容量を大量に使用できます。</span><span class="sxs-lookup"><span data-stu-id="400e3-122">This response is stored in as an XML blob and, over time, can take up a large amount of space in the database.</span></span> |
| <span data-ttu-id="400e3-123">リンクされた払戻</span><span class="sxs-lookup"><span data-stu-id="400e3-123">Linked refund</span></span> | <span data-ttu-id="400e3-124">前のトランザクションを参照する払戻し要求。</span><span class="sxs-lookup"><span data-stu-id="400e3-124">A refund request that references a previous transaction.</span></span> <span data-ttu-id="400e3-125">クレジット カード プロセッサは、リンクされた払戻しのリスクを伴と見なし、関連する手数料が低くなります。</span><span class="sxs-lookup"><span data-stu-id="400e3-125">Credit card processors consider linked refunds to carry lower risk, and they have lower associated fees.</span></span> |
| <span data-ttu-id="400e3-126">スタンドアロンの払戻し</span><span class="sxs-lookup"><span data-stu-id="400e3-126">Standalone refund</span></span> | <span data-ttu-id="400e3-127">以前のトランザクションを参照しない払戻し要求。</span><span class="sxs-lookup"><span data-stu-id="400e3-127">A refund request that doesn't reference a previous transaction.</span></span> <span data-ttu-id="400e3-128">スタンドアロンの払戻ではリスクが高く、処理手数料も高くなります。</span><span class="sxs-lookup"><span data-stu-id="400e3-128">Standalone refunds carry higher risk and have higher processing fees.</span></span> |

## <a name="document-management-dependency"></a><span data-ttu-id="400e3-129">ドキュメント管理の依存関係</span><span class="sxs-lookup"><span data-stu-id="400e3-129">Document management dependency</span></span>

<span data-ttu-id="400e3-130">アーカイブ ジョブを実行すると、ドキュメント管理を使用して、zip ファイル内の古いクレジット カード認証に関する XML データがエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="400e3-130">When the archival job is run, document management is used to export XML data about aged credit card authorizations in a zip file.</span></span> <span data-ttu-id="400e3-131">ドキュメント管理が環境で設定されていない場合、アーカイブ ジョブを正常に実行できません。</span><span class="sxs-lookup"><span data-stu-id="400e3-131">If document management isn't set up in an environment, the archival job can't successfully be run.</span></span> <span data-ttu-id="400e3-132">詳細については、[ドキュメント管理のコンフィギュレーション](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="400e3-132">For more information, see [Configure document management](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management).</span></span>

<span data-ttu-id="400e3-133">アーカイブ ジョブでは、**トランザクションの最小日数** の値で定義されている条件を満たすすべてのクレジット カード支払データが処理されます。</span><span class="sxs-lookup"><span data-stu-id="400e3-133">The archival job processes all credit card payment data that meets the criterion that is defined by the **Minimum transaction age in days** value.</span></span> <span data-ttu-id="400e3-134">ジョブが有効であり、定義された基準に基づいて大量のレコードを処理する必要がある場合、ジョブの実行に数日かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="400e3-134">If the job is active and, based on the defined criterion, a large number of records must be processed, job execution might take several days.</span></span> <span data-ttu-id="400e3-135">ただし、支払のバックログがアーカイブされた後は、ジョブの実行に時間はかかりません。</span><span class="sxs-lookup"><span data-stu-id="400e3-135">However, after the backlog of payments has been archived, the job won't take as long to run.</span></span>

## <a name="data-that-is-in-scope-for-archiving"></a><span data-ttu-id="400e3-136">アーカイブの対象範囲にあるデータ</span><span class="sxs-lookup"><span data-stu-id="400e3-136">Data that is in scope for archiving</span></span>

<span data-ttu-id="400e3-137">アーカイブ ジョブはデータを **RetailTransactionPaymentTrans** タブの **PaymentAuthorization**、**PaymentCaptureToken** および **PaymentCardToken** フィールドにアーカイブします。</span><span class="sxs-lookup"><span data-stu-id="400e3-137">The archival job archives data in the **PaymentAuthorization**, **PaymentCaptureToken**, and **PaymentCardToken** fields of the **RetailTransactionPaymentTrans** table.</span></span> <span data-ttu-id="400e3-138">アーカイブされたトランザクションには、これらのフィールドに関連付けられたデータは存在しないが、リンクされた払戻しは一度も行わずに返品できます。</span><span class="sxs-lookup"><span data-stu-id="400e3-138">Although transactions that have been archived don't have associated data in these fields, they can still be returned without linked refunds.</span></span>

## <a name="batch-job-setup"></a><span data-ttu-id="400e3-139">バッチ ジョブの設定</span><span class="sxs-lookup"><span data-stu-id="400e3-139">Batch job setup</span></span>

<span data-ttu-id="400e3-140">**小売とコマース \> 小売とコマース IT \> クリーン アップ \> クレジット カードのトランザクション データをアーカイブ** を実行すると、コマース本社のアーカイブ ジョブにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="400e3-140">You can access the archival job in Commerce headquarters by going to **Retail and commerce \> Retail and Commerce IT \> Clean up \> Archive credit card transaction data**.</span></span> <span data-ttu-id="400e3-141">**クレジット カード トランザクション データのアーカイブ** ダイアログ ボックスでは、**トランザクションの最小日数** フィールドが必須フィールドです。</span><span class="sxs-lookup"><span data-stu-id="400e3-141">In the **Archive credit card transaction data** dialog box, the **Minimum transaction age in days** field is a required field.</span></span> <span data-ttu-id="400e3-142">アーカイブの対象となるクレジット カード認証の日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="400e3-142">Enter the age, in days, of credit card authorizations that will be subject to archiving.</span></span> <span data-ttu-id="400e3-143">入力する値は、顧客が元のクレジット カード認証にリンクされている払戻しを受け取る時間数である必要があります。</span><span class="sxs-lookup"><span data-stu-id="400e3-143">The value that you enter should be the amount of time that customers can have refunds linked to their original credit card authorization.</span></span> <span data-ttu-id="400e3-144">このフィールドを 365 日に設定した場合、たとえば販売者のポリシーによっては、366 日後のトランザクションに対する返品は払戻しの対象となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="400e3-144">If you set the field to 365 days, for example, a return for a transaction that is 366 days old might still be eligible for refund, depending on the merchant's policies.</span></span> <span data-ttu-id="400e3-145">ただし、リンクされた払戻しを実行するために必要なデータは使用できため、実行された払戻しはスタンドアロンの払戻しである必要があります。</span><span class="sxs-lookup"><span data-stu-id="400e3-145">However, because the data that is required to do a linked refund won't be available, any refund that is done will have to be a standalone refund.</span></span>

<span data-ttu-id="400e3-146">**トランザクションの最小日数** フィールド加えて、**クレジット カード トランザクション データのアーカイブ** ダイアログ ボックスでは、ジョブの繰り返しオプションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="400e3-146">In addition to the **Minimum transaction age in days** field, the **Archive credit card transaction data** dialog box includes options for job recurrence.</span></span> <span data-ttu-id="400e3-147">既定では、ジョブのバッチ処理が有効で、無効にできない必要があります。</span><span class="sxs-lookup"><span data-stu-id="400e3-147">Batch processing for the job is turned on by default and can't be turned off.</span></span>

<span data-ttu-id="400e3-148">次の図では、**クレジット カード トランザクション データをアーカイブ** ダイアログ ボックスのパラメータ設定例を示しています。</span><span class="sxs-lookup"><span data-stu-id="400e3-148">The following illustration shows an example of parameter settings in the **Archive credit card transaction data** dialog box.</span></span>

![クレジット カード トランザクション データのアーカイブ ダイアログ ボックスのパラメータ設定](media/PAYMENTS/Batch1.png)

<span data-ttu-id="400e3-150">**最小トランザクションの日数** フィールドおよびバッチ詳細が設定された後、**次へ** を選び、エクスポートされるデータ サンプルを表示します。</span><span class="sxs-lookup"><span data-stu-id="400e3-150">After the **Minimum transaction age in days** field and batch details have been set, select **Next** to view a sample of the data that will be exported.</span></span> <span data-ttu-id="400e3-151">次の図は、例を示します。</span><span class="sxs-lookup"><span data-stu-id="400e3-151">The following illustration shows an example.</span></span> <span data-ttu-id="400e3-152">このサンプルのデータは限られていますが、アーカイブの対象となるすべてのデータをエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="400e3-152">Although the data in this sample is limited, all data that is subject to archiving can be exported.</span></span>

![エクスポートされるデータのサンプル](media/PAYMENTS/Batch2.png)

> [!IMPORTANT]
> <span data-ttu-id="400e3-154">アーカイブの対象となるデータには、カード所有者の名前など、個人を特定できる顧客情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="400e3-154">The data that is subject to archiving includes personally identifiable customer information such as the name of the cardholder.</span></span> <span data-ttu-id="400e3-155">この機密データは、地域の規制要件に従って処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="400e3-155">This sensitive data should be handled according to your local regulatory requirements.</span></span>

<span data-ttu-id="400e3-156">次の図に示すように、アーカイブする必要があるデータのパラメータを確認した後、アーカイブされているデータを簡単に復元できないという確認を求めるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="400e3-156">After you confirm the parameters for data that must be archived, you're prompted to confirm that you understand that the data that is being archived can't easily be restored, as shown in the following illustration.</span></span>

![確認用メッセージボックス](media/PAYMENTS/Batch3.png)

<span data-ttu-id="400e3-158">**はい** を選び、アーカイブ ジョブが有効になると、**トランザクションの最小日数** 値よりも古いクレジット カードの認証に関するすべての XML データはアーカイブの対象になります。</span><span class="sxs-lookup"><span data-stu-id="400e3-158">After you select **Yes**, the archival job becomes active, and all XML data about credit card authorizations that is older than the **Minimum transaction age in days** value will be subject to archiving.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="400e3-159">追加リソース</span><span class="sxs-lookup"><span data-stu-id="400e3-159">Additional resources</span></span>

[<span data-ttu-id="400e3-160">支払に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="400e3-160">Payments FAQ</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/payments-retail)

[<span data-ttu-id="400e3-161">Adyen 向け Dynamics 365 Payment Connector</span><span class="sxs-lookup"><span data-stu-id="400e3-161">Dynamics 365 Payment Connector for Adyen</span></span>](adyen-connector.md?tabs=8-1-3)

[<span data-ttu-id="400e3-162">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="400e3-162">Checkout module</span></span>](../add-checkout-module.md)
