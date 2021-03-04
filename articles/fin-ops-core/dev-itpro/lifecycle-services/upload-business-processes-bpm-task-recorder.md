---
title: 独自の業務プロセスからビジネス プロセス モデラー (BPM) へのアップロード
description: Microsoft Dynamics Lifecycle Services では、タスク レコーダーの更新されたバージョンを使用して独自の業務プロセスに関する情報を記録できます。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 18991
ms.assetid: 74808085-e971-4e7b-8547-d3549273d14a
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d9ffc334b39bce6c2c07a33217cfdaf054a3870
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129691"
---
# <a name="upload-custom-business-processes-to-business-process-modeler-bpm"></a><span data-ttu-id="82a76-103">独自の業務プロセスからビジネス プロセス モデラー (BPM) へのアップロード</span><span class="sxs-lookup"><span data-stu-id="82a76-103">Upload custom business processes to Business process modeler (BPM)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82a76-104">Microsoft Dynamics Lifecycle Services では、タスク レコーダーの更新されたバージョンを使用して独自の業務プロセスに関する情報を記録できます。</span><span class="sxs-lookup"><span data-stu-id="82a76-104">In Microsoft Dynamics Lifecycle Services, you can record information about custom business processes by using an updated version of Task recorder.</span></span> <span data-ttu-id="82a76-105">記録するファイルをビジネス プロセス モデラーにアップロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="82a76-105">You can then upload the files that you record to Business process modeler.</span></span>

<span data-ttu-id="82a76-106">このトピックでは、タスク レコーダーの更新バージョンの場所と、記録するカスタム ビジネス プロセス ファイルをアップロードする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="82a76-106">This topic explains where to find the updated version of Task recorder and how to upload the custom business process files that you record.</span></span> <span data-ttu-id="82a76-107">タスク レコーダーの更新されたバージョンは修正プログラムとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="82a76-107">The updated version of Task recorder is available as a hotfix.</span></span> <span data-ttu-id="82a76-108">以下のサイトから修正プログラムをダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="82a76-108">You can download the hotfix from the following sites:</span></span>

-   <span data-ttu-id="82a76-109">Microsoft Dynamics AX 2012 および Microsoft Dynamics AX 2012 Feature Pack – サポート技術情報の記事 [2863182](https://go.microsoft.com/fwlink/?LinkId=309910)</span><span class="sxs-lookup"><span data-stu-id="82a76-109">Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 Feature Pack – Knowledgebase article [2863182](https://go.microsoft.com/fwlink/?LinkId=309910)</span></span>
-   <span data-ttu-id="82a76-110">Microsoft Dynamics AX 2012 R2 – サポート技術情報の記事 [2863182](https://go.microsoft.com/fwlink/?LinkId=309911)</span><span class="sxs-lookup"><span data-stu-id="82a76-110">Microsoft Dynamics AX 2012 R2 – Knowledgebase article [2863182](https://go.microsoft.com/fwlink/?LinkId=309911)</span></span>

<span data-ttu-id="82a76-111">更新されたタスク レコーダーを操作する方法の詳細については、[Microsoft Dynamics AX 2012 のタスク レコーダー更新](https://go.microsoft.com/fwlink/?LinkID=310185) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82a76-111">For more information about how to work with the updated Task recorder, see [Task recorder update for Microsoft Dynamics AX 2012](https://go.microsoft.com/fwlink/?LinkID=310185).</span></span>

## <a name="upload-custom-recorded-business-processes"></a><span data-ttu-id="82a76-112">カスタムで記録した業務プロセスのアップロード</span><span class="sxs-lookup"><span data-stu-id="82a76-112">Upload custom recorded business processes</span></span>
<span data-ttu-id="82a76-113">業務プロセス コンポーネント (\*.axbpm ファイル) を業務プロセス ライブラリにアップロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="82a76-113">You can upload business process artifacts (\*.axbpm files) to the business process library.</span></span> <span data-ttu-id="82a76-114">これらのファイルは、タスク レコーダーから生成されます。</span><span class="sxs-lookup"><span data-stu-id="82a76-114">These files are generated from Task recorder.</span></span> <span data-ttu-id="82a76-115">アップロード後、ビジネス プロセス モデラーに記録されたプロセスを表示および変更できます。</span><span class="sxs-lookup"><span data-stu-id="82a76-115">After they are uploaded, you can view and modify the recorded processes in Business process modeler.</span></span> <span data-ttu-id="82a76-116">記録したカスタム ビジネス プロセスをアップロードするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="82a76-116">To upload custom business processes that you recorded, follow these steps:</span></span>

1.  <span data-ttu-id="82a76-117">**プロジェクト** ホーム ページで、**業務プロセス モデラー** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="82a76-117">On the **Project** home page, click the **Business process modeler** tile.</span></span>
2.  <span data-ttu-id="82a76-118">**業務プロセスのライブラリ** ページで、**自分のライブラリ** セクションまたは **コーポレート ライブラリ** で、**アップロード** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="82a76-118">On the **Business process library** page, click **Upload** in the **My libraries** section or the **Corporate libraries** section.</span></span>
3.  <span data-ttu-id="82a76-119">**アップロード** ページで、業種を選択し、名前と説明をアップロードするファイルを入力します。</span><span class="sxs-lookup"><span data-stu-id="82a76-119">On the **Upload** page, select the industry and enter a name and description for the file that you are uploading.</span></span> <span data-ttu-id="82a76-120">**アップロード** をクリックし、.axbpm ファイルを選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="82a76-120">Click **Upload**, select the .axbpm file, and then click **OK**.</span></span> <span data-ttu-id="82a76-121">アップロード プロセスには少し時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="82a76-121">The upload process can take some time.</span></span> <span data-ttu-id="82a76-122">**管理** ページでは、アップロードの状態を表示できます。</span><span class="sxs-lookup"><span data-stu-id="82a76-122">You can view the status of the upload on the **Administration** page.</span></span>
4.  <span data-ttu-id="82a76-123">業務プロセスのファイルをアップロードした後、**業務プロセスのライブラリ** ページから業務プロセス フレームワークを表示できます。</span><span class="sxs-lookup"><span data-stu-id="82a76-123">After the business process file has been uploaded, you can view the business process framework from the **Business process library** page.</span></span>


<a name="additional-resources"></a><span data-ttu-id="82a76-124">追加リソース</span><span class="sxs-lookup"><span data-stu-id="82a76-124">Additional resources</span></span>
--------

[<span data-ttu-id="82a76-125">Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM)</span><span class="sxs-lookup"><span data-stu-id="82a76-125">Business process modeler (BPM) in Lifecycle Services (LCS)</span></span>](./ax-2012/business-process-modeler-lcs.md)

[<span data-ttu-id="82a76-126">ビジネス プロセス モデラー (BPM) ビジネス プロセス ライブラリ</span><span class="sxs-lookup"><span data-stu-id="82a76-126">Business process libraries in Business process modeler (BPM)</span></span>](business-process-libraries-business-process-modeler.md)

[<span data-ttu-id="82a76-127">ビジネス プロセス モデラー (BPM) のフローチャート</span><span class="sxs-lookup"><span data-stu-id="82a76-127">Flowcharts in Business process modeler (BPM)</span></span>](flowcharts-business-process-modeler.md)



