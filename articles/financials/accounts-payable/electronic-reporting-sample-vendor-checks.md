---
title: "電子レポートのサンプル仕入先小切手"
description: "このトピックでは、電子レポートのサンプル小切手フォーマットの使い方についての一般情報を提供します。"
author: twheeloc
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c583c3d82ce7273c49144561c51cfbec932d3ae8
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

[!include [banner](../includes/banner.md)]

# <a name="electronic-reporting-sample-check-formats"></a><span data-ttu-id="34fc2-103">電子レポートのサンプル小切手フォーマット</span><span class="sxs-lookup"><span data-stu-id="34fc2-103">Electronic reporting sample check formats</span></span>

<span data-ttu-id="34fc2-104">電子レポート (ER) を使用して仕入先小切手をフォーマットすることができます。</span><span class="sxs-lookup"><span data-stu-id="34fc2-104">You can use Electronic reporting (ER) to format vendor checks.</span></span> <span data-ttu-id="34fc2-105">市場では多くの銀行固有の、および小切手プロバイダー固有の小切手フォーマットが使用可能です。</span><span class="sxs-lookup"><span data-stu-id="34fc2-105">Many bank-specific and check provider–specific check formats are available on the market.</span></span> <span data-ttu-id="34fc2-106">サンプル小切手フォーマットは、ER ツール リポジトリの支払小切手モデルに含まれています。</span><span class="sxs-lookup"><span data-stu-id="34fc2-106">Sample check formats have been included in the Payment check model in the ER tool repository.</span></span> <span data-ttu-id="34fc2-107">これらのサンプル小切手には、「**小切手中央 (米国)**」および「**小切手上控え下 (米国)**」というラベルが付いています。</span><span class="sxs-lookup"><span data-stu-id="34fc2-107">These sample checks are labeled **Check in the middle (US)** and **Check on top stub below (US)**.</span></span>

## <a name="what-check-formats-are-currently-supported"></a><span data-ttu-id="34fc2-108">どんな小切手フォーマットが現在サポートされていますか？</span><span class="sxs-lookup"><span data-stu-id="34fc2-108">What check formats are currently supported?</span></span>

<span data-ttu-id="34fc2-109">Microsoft Dynamics Lifecycle Services (LCS) の共有資産ライブラリに移動して、**GER コンフィギュレーション** という資産タイプを持つ利用可能なファイルの現在のリストを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="34fc2-109">You should always go to the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) and view the current list of available files that have an asset type of **GER configuration**.</span></span> <span data-ttu-id="34fc2-110">「何を設定する必要がありますか。」という次のセクションに、利用可能なコンフィギュレーションを確認し選択したコンフィギュレーションをインポートできるよう LCS リポジトリを作成する方法を説明するトピックへのリンクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="34fc2-110">The next section, “What do I have to set up?,” includes a link to a topic that explains how to create an LCS repository so that you can review available configurations and import selected configurations.</span></span>

<span data-ttu-id="34fc2-111">Microsoft Dynamics 365 for Finance and Operations には、上部に小切手がありその後に 2 つの送金セクションがあるサンプル フォーマットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="34fc2-111">Microsoft Dynamics 365 for Finance and Operations, includes a sample format where the check is on top, followed by two remittance sections.</span></span> <span data-ttu-id="34fc2-112">小切手が真ん中、つまり 2 つの送金セクションの間にあるサンプル フォーマットも含まれています。</span><span class="sxs-lookup"><span data-stu-id="34fc2-112">It also includes a sample format where the check is in the middle, between two remittance sections.</span></span> <span data-ttu-id="34fc2-113">これらのサンプル形式は、Deluxe 業務用小切手フォーマットに対応します。</span><span class="sxs-lookup"><span data-stu-id="34fc2-113">These sample formats correspond to Deluxe business checks formats.</span></span>

## <a name="what-do-i-have-to-set-up"></a><span data-ttu-id="34fc2-114">何を設定する必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="34fc2-114">What do I have to set up?</span></span>

- <span data-ttu-id="34fc2-115">ER を使用して小切手を印刷するには、少なくとも 1 つの有効な小切手コンフィギュレーションを ER コンフィギュレーションにインポートしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="34fc2-115">Before you can print checks by using ER, at least one active check configuration must be imported into your ER configurations.</span></span> <span data-ttu-id="34fc2-116">手順については、[Lifecycle Services の電子申告コンフィギュレーションのダウンロード](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="34fc2-116">For instructions, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>
- <span data-ttu-id="34fc2-117">銀行口座に現金および銀行管理小切手をコンフィギュレーションする時は、[一般的な電子エクスポート形式] チェック ボックスを選択してから、適切な小切手フォーマットをエクスポート形式コンフィギュレーションとして選択します。</span><span class="sxs-lookup"><span data-stu-id="34fc2-117">When you configure Cash and bank management checks for the bank account, select the **Generic electronic Export format** check box, and then select the appropriate check format as an export format configuration.</span></span>
- <span data-ttu-id="34fc2-118">送金に印刷される伝票の明細行の数を指定する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="34fc2-118">You must also specify the number of slip lines that will be printed on the remittance.</span></span> <span data-ttu-id="34fc2-119">この数を計算する際は確実にヘッダー行も含めるようにします。</span><span class="sxs-lookup"><span data-stu-id="34fc2-119">Be sure to include the header rows when you calculate this number.</span></span> <span data-ttu-id="34fc2-120">2 つのサンプル小切手フォーマットについては、推奨される明細行の数は 17 です。</span><span class="sxs-lookup"><span data-stu-id="34fc2-120">For the two sample check formats, the recommended number of slip lines is 17.</span></span> <span data-ttu-id="34fc2-121">ただし、小切手ストックおよびプリンター ドライバーによってこの番号は異なります。</span><span class="sxs-lookup"><span data-stu-id="34fc2-121">However, this number will vary, depending on your check stock and your printer drivers.</span></span>
- <span data-ttu-id="34fc2-122">テスト用小切手を印刷して小切手のレイアウトを検証することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="34fc2-122">We recommend that you print a test check to validate the check layout.</span></span> <span data-ttu-id="34fc2-123">テスト用小切手を印刷するには、[印刷テスト] オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="34fc2-123">To print a test check, select the **Print test** option.</span></span> <span data-ttu-id="34fc2-124">サンプル小切手フォーマットは、Microsoft Excel の詳細なプリンターのプロパティで [余白] を [なし] に設定すると最適に機能します。</span><span class="sxs-lookup"><span data-stu-id="34fc2-124">The sample check formats work best when **Margins** is set to **None** in the advanced printer properties for Microsoft Excel.</span></span> <span data-ttu-id="34fc2-125">テスト用小切手が生成されてから、Excel 出力の編集機能を有効にし、すべての余白が **0** (ゼロ) に設定されるようにページ レイアウトを構成します。</span><span class="sxs-lookup"><span data-stu-id="34fc2-125">After the test check has been generated, enable editing of the Excel output, and configure the page layout so that all margins are set to **0** (zero).</span></span> <span data-ttu-id="34fc2-126">小切手のテスト コピーを小切手ストックと比較し、配置に問題がなくなるまで設定を調整します。</span><span class="sxs-lookup"><span data-stu-id="34fc2-126">Compare the test copy of the checks to your check stock, and adjust the settings until you're satisfied with the alignment.</span></span>
- <span data-ttu-id="34fc2-127">支払仕訳でコンフィギュレーションしてある銀行口座に対する支払を生成する時、小切手は指定されたフォーマットを使用して印刷されます。</span><span class="sxs-lookup"><span data-stu-id="34fc2-127">When you generate payments for the configured bank account in the payment journal, the checks will be printed by using the specified format.</span></span>

<span data-ttu-id="34fc2-128">詳細については、「[電子レポートのフォーマットを修正する](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="34fc2-128">For more information, see [Modify an Electronic reporting format](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).</span></span>

