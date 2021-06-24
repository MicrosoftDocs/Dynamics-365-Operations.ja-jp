---
title: 使用状況管理ダッシュボード
description: このトピックでは、使用状況管理ダッシュボードを使用して電子請求サービスの使用状況を監視し、コンプライアンスを維持する方法について説明します。
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 411c2d33c81738dcacfb7c8feec991d0fd06fb78
ms.sourcegitcommit: 9069a8511dfe11d09a2b51d32547ba10fea48bed
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/02/2021
ms.locfileid: "6130509"
---
# <a name="usage-management-dashboard"></a><span data-ttu-id="24258-103">使用状況管理ダッシュボード</span><span class="sxs-lookup"><span data-stu-id="24258-103">Usage management dashboard</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24258-104">**使用状況管理** ダッシュボードを使用すると、電子請求サービスの使用状況を監視し、組織の月間使用状況に関するコンプライアンスを維持することができます。</span><span class="sxs-lookup"><span data-stu-id="24258-104">The **Usage management** dashboard helps you monitor usage of the Electronic Invoicing service, and therefore helps your organization remain compliant in terms of its monthly usage.</span></span> <span data-ttu-id="24258-105">コンプライアンスは、送信量を計算し、取得した送信量と比較して、取得した量と使用量の誤差を特定するで判断します。</span><span class="sxs-lookup"><span data-stu-id="24258-105">Compliance is determined by calculating the submission volume and comparing it with the acquired volume of submissions to identify any deviations between the acquired volume and the used volume.</span></span>

<span data-ttu-id="24258-106">ダッシュボードには次のインジケータが含まれています:</span><span class="sxs-lookup"><span data-stu-id="24258-106">The dashboard includes the following indicators:</span></span>

- <span data-ttu-id="24258-107">ライセンス準拠にあたって、消費量の監視に使用できるコスト指標の一つです。</span><span class="sxs-lookup"><span data-stu-id="24258-107">One cost indicator that you can use to monitor consumption for licensing compliance purposes:</span></span>

    - <span data-ttu-id="24258-108">1 か月あたりの使用状況 (エクスポート)</span><span class="sxs-lookup"><span data-stu-id="24258-108">Usage per month (export)</span></span>

- <span data-ttu-id="24258-109">管理目的で電子請求書発行サービスの利用状況を把握するために使用できる 3 つの運用指標です。</span><span class="sxs-lookup"><span data-stu-id="24258-109">Three operational indicators that you can use to track usage of the Electronic Invoicing service for management purposes:</span></span>

    - <span data-ttu-id="24258-110">機能別の使用状況</span><span class="sxs-lookup"><span data-stu-id="24258-110">Usage by feature</span></span>
    - <span data-ttu-id="24258-111">環境別の使用状況</span><span class="sxs-lookup"><span data-stu-id="24258-111">Usage by environment</span></span>
    - <span data-ttu-id="24258-112">1 か月あたりの使用状況 (インポート)</span><span class="sxs-lookup"><span data-stu-id="24258-112">Usage per month (import)</span></span>

## <a name="measurement-scope"></a><span data-ttu-id="24258-113">測定スコープ</span><span class="sxs-lookup"><span data-stu-id="24258-113">Measurement scope</span></span>

- <span data-ttu-id="24258-114">計量単位:</span><span class="sxs-lookup"><span data-stu-id="24258-114">Unit of measure:</span></span> 

    <span data-ttu-id="24258-115">**使用状況管理ダッシュボード** では、ビジネス ドキュメントの送信とインポートされた電子請求書がカウントされます。</span><span class="sxs-lookup"><span data-stu-id="24258-115">The **Usage management** dashboard counts the submission of business documents and imported electronic invoices.</span></span>

- <span data-ttu-id="24258-116">組織:</span><span class="sxs-lookup"><span data-stu-id="24258-116">Organization:</span></span> 

    <span data-ttu-id="24258-117">Microsoft Dynamics 365 Finance や Dynamics 365 Supply Chain Management のインスタンス数や、電子請求書発行サービスが有効な法人の数に関わらず、組織のテナント ID で集計されます。</span><span class="sxs-lookup"><span data-stu-id="24258-117">Counting is summarized by the tenant ID of your organization, regardless of the number of instances of Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management, or the number of legal entities where the Electronic Invoicing service is enabled.</span></span>


## <a name="indicator-usage-per-month-export"></a><span data-ttu-id="24258-118">インジケータ: 月ごとの使用 (エクスポート)</span><span class="sxs-lookup"><span data-stu-id="24258-118">Indicator: Usage per month (export)</span></span>

<span data-ttu-id="24258-119">この指標は、定義された期間中に組織が発行した電子請求書の詳細を提供します。</span><span class="sxs-lookup"><span data-stu-id="24258-119">This indicator provides details about the electronic invoices that your organization issues during a defined period.</span></span>

### <a name="scope"></a><span data-ttu-id="24258-120">スコープ</span><span class="sxs-lookup"><span data-stu-id="24258-120">Scope</span></span>
- <span data-ttu-id="24258-121">Finance および Supply Chain Management から E電子請求サービスに提出されたビジネス ドキュメントの数です。ビジネス ドキュメントに含まれる行数は加味されません。</span><span class="sxs-lookup"><span data-stu-id="24258-121">The number of business documents that are submitted from Finance and Supply Chain Management to the Electronic Invoicing service, regardless of number of lines that those business documents contain.</span></span>
- <span data-ttu-id="24258-122">提出されたビジネス ドキュメントのうち、電子請求書発行サービスで正常に処理された数です。</span><span class="sxs-lookup"><span data-stu-id="24258-122">The number of submitted business documents that are successfully processed by the Electronic Invoicing service.</span></span> <span data-ttu-id="24258-123">機能の設定で定義されたアクションの流れを完了すると、ドキュメントが正常に処理されたと見なされます。</span><span class="sxs-lookup"><span data-stu-id="24258-123">A document is considered successfully processed when the flow of actions that are defined in the feature setup is completed.</span></span>

> [!NOTE]
> <span data-ttu-id="24258-124">電子請求書が外部の Web サービスに送信された場合、Web サービスの処理結果 (受け入れ済、否認済、スキーマ検証のエラー) とは独立してカウントされます。</span><span class="sxs-lookup"><span data-stu-id="24258-124">When an electronic invoice is submitted to an external web service, counting is independent of the results of web service processing (accepted, rejected, or schema validation error).</span></span> <span data-ttu-id="24258-125">Web サービスが電子請求サービスからのリクエストを受信して応答した場合、その送信は有効なカウントとみなされます。</span><span class="sxs-lookup"><span data-stu-id="24258-125">If the web service received and responded to the request from the Electronic Invoicing service, the submission is considered a valid counting.</span></span>

- <span data-ttu-id="24258-126">**例外** : ビジネス ドキュメントは、Finance および Supply Chain Management から電子請求サービスに再送信される場合 (電子請求書のステータスを変更するために同じビジネス ドキュメントの再送信が必要な場合など) にはカウントされません。</span><span class="sxs-lookup"><span data-stu-id="24258-126">**Exception:** Business documents aren't counted if they are resubmitted from Finance and Supply Chain Management to the Electronic Invoicing service, such as in the scenarios where a resubmission of the same business document is required to change the status of the electronic invoice.</span></span> <span data-ttu-id="24258-127">たとえば、ブラジルの電子請求書 (会計文書) の発行は有効とカウントされますが、それに対するキャンセル申請はカウントされません。</span><span class="sxs-lookup"><span data-stu-id="24258-127">For example, issuance of a Brazilian electronic invoice (fiscal document) is counted as valid, but the cancellation request for it isn't counted.</span></span>


### <a name="calculation"></a><span data-ttu-id="24258-128">計算</span><span class="sxs-lookup"><span data-stu-id="24258-128">Calculation</span></span>

<span data-ttu-id="24258-129">残高の計算は次のように計算されます。</span><span class="sxs-lookup"><span data-stu-id="24258-129">The calculation of the balance is calculated as follows:</span></span>

<span data-ttu-id="24258-130">残高 ＝ 無料 + 購入 - 使用</span><span class="sxs-lookup"><span data-stu-id="24258-130">Balance = Free + Purchased – Used</span></span>

<span data-ttu-id="24258-131">場所:</span><span class="sxs-lookup"><span data-stu-id="24258-131">Where:</span></span>

- <span data-ttu-id="24258-132">無制限:</span><span class="sxs-lookup"><span data-stu-id="24258-132">Free:</span></span>
  
    <span data-ttu-id="24258-133">顧客が月ごとに無料で送信できるビジネス ドキュメントの量です。</span><span class="sxs-lookup"><span data-stu-id="24258-133">A free volume of business documents the customer can submit per month.</span></span> <span data-ttu-id="24258-134">電子請求書発行サービスに送信可能なビジネス ドキュメントの100点をパッケージ化しています。</span><span class="sxs-lookup"><span data-stu-id="24258-134">It includes a package of 100 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="24258-135">無料分は累積されず、残量があっても次の期間に繰り越すことはできません。</span><span class="sxs-lookup"><span data-stu-id="24258-135">Free volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="24258-136">購買済:</span><span class="sxs-lookup"><span data-stu-id="24258-136">Purchased:</span></span>
  
    <span data-ttu-id="24258-137">電子請求書発行サービスに送信可能なビジネス文書1,000点をパッケージ化したものです。</span><span class="sxs-lookup"><span data-stu-id="24258-137">A package of 1,000 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="24258-138">このパッケージは、組織で月次で取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="24258-138">This package must be acquired for your organization on a monthly basis.</span></span> <span data-ttu-id="24258-139">購入分は累積されず、残量があっても次の期間に繰り越すことはできません。</span><span class="sxs-lookup"><span data-stu-id="24258-139">Purchased volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="24258-140">使用済:</span><span class="sxs-lookup"><span data-stu-id="24258-140">Used:</span></span> 

    <span data-ttu-id="24258-141">定義された基準に従って電子請求書作成サービスに提出されたビジネス文書の数です。</span><span class="sxs-lookup"><span data-stu-id="24258-141">The count of business document submissions to the Electronic Invoicing service according to defined criteria.</span></span>
   
> [!IMPORTANT]
> <span data-ttu-id="24258-142">月間100件の無料提出の枠を上回る予定の場合は、ピーク ボリュームを購入して、電子請求書作成サービスに関するマイクロソフトのライセンスポリシーに従ってください。</span><span class="sxs-lookup"><span data-stu-id="24258-142">If your organization plans to exceed the monthly volume of 100 free submissions, purchase the peak volume to ensure that you remain compliant with the Microsoft licensing policy for the Electronic Invoicing service.</span></span>
>
> <span data-ttu-id="24258-143">現在、購入したボリュームは、取得した日に応じて、1,000件単位の複数のパッケージとして手動で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="24258-143">Currently, purchased volume must be manually entered, according to the date of acquisition, as multiple packages of 1,000 submissions.</span></span>

## <a name="indicator-usage-by-feature"></a><span data-ttu-id="24258-144">インジケータ: 機能別の用途</span><span class="sxs-lookup"><span data-stu-id="24258-144">Indicator: Usage by feature</span></span>

<span data-ttu-id="24258-145">このインジケータは、定義された期間における電子請求書の発行に対する電子請求機能の使用を表します。</span><span class="sxs-lookup"><span data-stu-id="24258-145">This indicator shows the usage of electronic invoicing features for issuance of electronic invoices during a defined period.</span></span>

- <span data-ttu-id="24258-146">計算:</span><span class="sxs-lookup"><span data-stu-id="24258-146">Calculation:</span></span>
  
    <span data-ttu-id="24258-147">使用回数 = 電子請求サービスへのビジネス ドキュメントの送信中に各電子請求機能が使用された回数です。</span><span class="sxs-lookup"><span data-stu-id="24258-147">Used = The count of how many times each electronic invoicing feature was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-by-environment"></a><span data-ttu-id="24258-148">インジケータ: 環境別の使用量です</span><span class="sxs-lookup"><span data-stu-id="24258-148">Indicator: Usage by environment</span></span>

<span data-ttu-id="24258-149">このインジケータは、定められた期間における電子請求書発行サービス環境の利用状況を示すものです。</span><span class="sxs-lookup"><span data-stu-id="24258-149">This indicator shows the usage of electronic invoicing service environments during a defined period.</span></span>

- <span data-ttu-id="24258-150">計算:</span><span class="sxs-lookup"><span data-stu-id="24258-150">Calculation:</span></span>
    
    <span data-ttu-id="24258-151">使用回数 = 電子請求サービスへのビジネス ドキュメントの送信中に各電子請求のサービス環境が使用された回数です。</span><span class="sxs-lookup"><span data-stu-id="24258-151">Used = The count of how many times each electronic invoicing service environment was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-per-month-import"></a><span data-ttu-id="24258-152">インジケータ: 月ごとの使用 (インポート)</span><span class="sxs-lookup"><span data-stu-id="24258-152">Indicator: Usage per month (import)</span></span>

<span data-ttu-id="24258-153">このインジケータは、定義された期間中に、電子請求書発行サービスによる電子請求書の Finance および Supply Chain Management へのインポート量を示しています。</span><span class="sxs-lookup"><span data-stu-id="24258-153">This indicator shows the volume of importation of electronic invoices by Electronic Invoicing service into Finance and Supply Chain Management during a defined period.</span></span>

- <span data-ttu-id="24258-154">スコープ:</span><span class="sxs-lookup"><span data-stu-id="24258-154">Scope:</span></span>

    <span data-ttu-id="24258-155">電子請求書に含まれる明細行の数にかかわらず、Finance および Supply Chain Management にインポートされる電子請求書を表わします。</span><span class="sxs-lookup"><span data-stu-id="24258-155">Electronic invoices that are imported into Finance and Supply Chain Management, regardless of the number of lines that those electronic invoices contain.</span></span>

- <span data-ttu-id="24258-156">計算:</span><span class="sxs-lookup"><span data-stu-id="24258-156">Calculation:</span></span>

    <span data-ttu-id="24258-157">受信 = Finance および Supply Chain Management にインポートされた電子請求書の数を表わします。</span><span class="sxs-lookup"><span data-stu-id="24258-157">Received = The count of imported electronic invoices into Finance and Supply Chain Management.</span></span>

## <a name="functions"></a><span data-ttu-id="24258-158">関数</span><span class="sxs-lookup"><span data-stu-id="24258-158">Functions</span></span>
### <a name="purchase"></a><span data-ttu-id="24258-159">購買</span><span class="sxs-lookup"><span data-stu-id="24258-159">Purchase</span></span>

<span data-ttu-id="24258-160">**月ごとの使用状況 (エクスポート)** タブで、**購買** を選択して取得した送信の量を手動で登録します。</span><span class="sxs-lookup"><span data-stu-id="24258-160">On the **Usage per month (export)** tab, select **Purchase** to manually register the amount of acquired submissions.</span></span>

<span data-ttu-id="24258-161">指定した日付で **新規** を選択し、その日付で取得した **パッケージ** 数を入力します。</span><span class="sxs-lookup"><span data-stu-id="24258-161">For a given date, select **New** and enter the number of **Packages** acquired for on that date.</span></span>

<span data-ttu-id="24258-162">この **数量** は次のように計算されます:</span><span class="sxs-lookup"><span data-stu-id="24258-162">The **Quantity** is calculated as:</span></span>

<span data-ttu-id="24258-163">数量 = パッケージ \* 1.000</span><span class="sxs-lookup"><span data-stu-id="24258-163">Quantity = Packages \* 1.000</span></span>

<span data-ttu-id="24258-164">計算された **数量** は、**月ごとの使用状況 (エクスポート)** インジケータから **購買済** に反映されます。</span><span class="sxs-lookup"><span data-stu-id="24258-164">The calculated **Quantity** reflects in the **Purchased** from the indicator **Usage per month (export)**.</span></span>

### <a name="update"></a><span data-ttu-id="24258-165">Update</span><span class="sxs-lookup"><span data-stu-id="24258-165">Update</span></span>

<span data-ttu-id="24258-166">アクション ウィンドウで、**更新** を選択して計算を更新し、ページおよびグラフに表示されるデータを更新します。</span><span class="sxs-lookup"><span data-stu-id="24258-166">On the Action Pane, select **Update** to refresh the calculation and update the data shown on the page and in the chart.</span></span>

### <a name="reset-history-data"></a><span data-ttu-id="24258-167">履歴データをリセット</span><span class="sxs-lookup"><span data-stu-id="24258-167">Reset history data</span></span>

<span data-ttu-id="24258-168">アクション ウィンドウで、**履歴データの リセット** を選択し、インジケータの計算を行う場所からデータベースを更新します。</span><span class="sxs-lookup"><span data-stu-id="24258-168">On the Action Pane, select **Reset history data** to refresh the database from where the indicators are calculated.</span></span>




> [!NOTE]
> <span data-ttu-id="24258-169">**使用状況 の管理** ダッシュボードでは、金額は表示されません。</span><span class="sxs-lookup"><span data-stu-id="24258-169">The **Usage management** dashboard doesn't show monetary amounts.</span></span> <span data-ttu-id="24258-170">その代わりに、カウントされた送信とインポートされたドキュメントの量だけが表示されます。</span><span class="sxs-lookup"><span data-stu-id="24258-170">Instead, it shows only the volume of counted submissions and imported documents.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
