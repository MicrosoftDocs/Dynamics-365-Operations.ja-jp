---
title: キャッシュ フロー予測に外部データを使用する (プレビュー)
description: このトピックでは、外部データを入力したり、キャッシュフロー予測にインポートしたりするために実行する必要がある設定ステップについて説明します。
author: rcarlson
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 7d5768a6cb2b3623333fab93a42ac5840e87ec68
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818621"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a><span data-ttu-id="40fa2-103">キャッシュ フロー予測に外部データを使用する (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="40fa2-103">Use external data in cash flow forecasts (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="40fa2-104">外部データを入力したり、キャッシュフロー予測にインポートしたりできます。</span><span class="sxs-lookup"><span data-stu-id="40fa2-104">External data can be entered or imported into cash flow forecasts.</span></span> <span data-ttu-id="40fa2-105">このトピックでは、外部データの使用に固有であり、外部データをキャッシュ フロー予測に含められるようにするための設定ステップについて説明します。</span><span class="sxs-lookup"><span data-stu-id="40fa2-105">This topic describes the setup steps that are specific to the use of external data and that enable the external data to be included in a cash flow forecast.</span></span>

## <a name="external-data-setup"></a><span data-ttu-id="40fa2-106">外部データの設定</span><span class="sxs-lookup"><span data-stu-id="40fa2-106">External data setup</span></span>

<span data-ttu-id="40fa2-107">**キャッシュフロー予測設定** ページ (**キャッシュおよび銀行の管理 \> キャッシュ フロー予測**) の **外部ソース** タブを使用して、キャッシュフロー予測での外部データの使用をサポートする設定を入力します。</span><span class="sxs-lookup"><span data-stu-id="40fa2-107">Use the **External source** tab on the **Cash flow forecast setup** page (**Cash and bank management \> Cash flow forecasting**) to enter settings that support the use of external data in cash flow forecasts.</span></span>

<span data-ttu-id="40fa2-108">設定の詳細については、[キャッシュ フロー予測](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="40fa2-108">For more information about the setup, see [Cash flow forecasting](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span></span>

<span data-ttu-id="40fa2-109">キャッシュフロー予測の外部データを入力するには、[Excelで開く] の機能を使用して、外部データを入力および変更します。</span><span class="sxs-lookup"><span data-stu-id="40fa2-109">To enter external data for cash flow forecasts, you can use the Open in Excel experience for entering and modifying external data.</span></span> <span data-ttu-id="40fa2-110">**外部データ** ボタンを選択し、**外部データの追加** または **既存の外部データの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="40fa2-110">Select the **External data** button, and then select either **Add External Data** or **Edit existing external data**.</span></span> <span data-ttu-id="40fa2-111">Microsoft Excel ファイルを開くと、次のフィールドに情報を入力できます。</span><span class="sxs-lookup"><span data-stu-id="40fa2-111">When the Microsoft Excel file is opened, you can enter information in the following fields:</span></span>

- <span data-ttu-id="40fa2-112">**入力 ID**</span><span class="sxs-lookup"><span data-stu-id="40fa2-112">**Entry ID**</span></span>
- <span data-ttu-id="40fa2-113">**説明** (オプション)</span><span class="sxs-lookup"><span data-stu-id="40fa2-113">**Description** (optional)</span></span>
- <span data-ttu-id="40fa2-114">**外部ソース名** - Finance 分析情報の設定時に定義した一覧の値のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="40fa2-114">**External Source name** – Select one of the values in the list that you defined when you set up Finance Insights.</span></span>
- <span data-ttu-id="40fa2-115">**法人**</span><span class="sxs-lookup"><span data-stu-id="40fa2-115">**Legal Entity**</span></span>
- <span data-ttu-id="40fa2-116">**日**</span><span class="sxs-lookup"><span data-stu-id="40fa2-116">**Date**</span></span>
- <span data-ttu-id="40fa2-117">**トランザクション通貨の金額**</span><span class="sxs-lookup"><span data-stu-id="40fa2-117">**Amount in transaction currency**</span></span>
- <span data-ttu-id="40fa2-118">**通貨コード**</span><span class="sxs-lookup"><span data-stu-id="40fa2-118">**Currency Code**</span></span>
- <span data-ttu-id="40fa2-119">**既定の分析コード** (オプション)</span><span class="sxs-lookup"><span data-stu-id="40fa2-119">**Default Dimension** (optional)</span></span>
- <span data-ttu-id="40fa2-120">**ドキュメント番号** (オプション)</span><span class="sxs-lookup"><span data-stu-id="40fa2-120">**Document number** (optional)</span></span>
- <span data-ttu-id="40fa2-121">**口座番号** (オプション)</span><span class="sxs-lookup"><span data-stu-id="40fa2-121">**Account number** (optional)</span></span>
- <span data-ttu-id="40fa2-122">**口座名** (オプション)</span><span class="sxs-lookup"><span data-stu-id="40fa2-122">**Account name** (optional)</span></span>

## <a name="importing-external-data-by-using-the-data-management-framework"></a><span data-ttu-id="40fa2-123">データ管理フレームワークを使用した外部データのインポート</span><span class="sxs-lookup"><span data-stu-id="40fa2-123">Importing external data by using the Data Management framework</span></span>

<span data-ttu-id="40fa2-124">キャッシュフロー予測の外部データは、**データ管理** ワークスペースと、**キャッシュ フロー予測の外部ソース エントリ** と呼ばれるエンティティを使用してインポートできます。</span><span class="sxs-lookup"><span data-stu-id="40fa2-124">You can import external data for cash flow forecasts by using the **Data Management** workspace and the entity that is named **Cash flow forecast external source entry**.</span></span>

<span data-ttu-id="40fa2-125">また、設定データをある環境から別の環境に移動する必要がある場合は、必要な設定テーブルに対して次のエンティティ領域が用意されています。</span><span class="sxs-lookup"><span data-stu-id="40fa2-125">Additionally, if you must move setup data from one environment to another, the following entities area available for the setup tables that are required:</span></span>

- <span data-ttu-id="40fa2-126">キャッシュ フロー予測の外部ソースの設定</span><span class="sxs-lookup"><span data-stu-id="40fa2-126">Cash flow forecast external source setup</span></span>
- <span data-ttu-id="40fa2-127">キャッシュ フロー予測の外部ソース法人の設定</span><span class="sxs-lookup"><span data-stu-id="40fa2-127">Cash flow forecast external source legal entity setup</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="40fa2-128">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="40fa2-128">Privacy notice</span></span>
<span data-ttu-id="40fa2-129">プレビューは (1) Dynamics 365 Finance and Operations サービスを下回るプライバシーおよび少ないセキュリティ対策を使用している場合があり、(2) このサービスのためにサービス レベル アグリーメント (SLA) には含まれておらず、(3) 個人データや、その他の法律上またはコンプライアンス要件の対象となるデータの処理に使用されず、(4) サポートが制限されます。</span><span class="sxs-lookup"><span data-stu-id="40fa2-129">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]