---
title: "電子申告ツールを使用して、電子ドキュメントを生成し、およびアプリケーション データを更新します"
description: "送信する電子ドキュメントを生成するために、Finance and Operations アプリケーションで使用できる電子申告 (ER) 形式をデザインできます。 受信した電子ドキュメントを解析し、これらのドキュメントの内容を使用してアプリケーション データの更新を行う ER 形式をデザインすることもできます。"
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: af7f9a373496eee4df354d5dd9e5a25c51317c43
ms.openlocfilehash: e2447274016f517db3ec0eb8f55c6b3163822f50
ms.contentlocale: ja-jp
ms.lasthandoff: 02/27/2018

---

# <a name="generate-electronic-documents-and-update-application-data-using-the-electronic-reporting-tool"></a><span data-ttu-id="adfd1-104">電子申告ツールを使用して、電子ドキュメントを生成し、およびアプリケーション データを更新します</span><span class="sxs-lookup"><span data-stu-id="adfd1-104">Generate electronic documents and update application data using the Electronic reporting tool</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="adfd1-105">送信する電子ドキュメントを生成するために、Finance and Operations アプリケーションで使用できる電子申告 (ER) 形式をデザインできます。</span><span class="sxs-lookup"><span data-stu-id="adfd1-105">You can design Electronic reporting (ER) formats that can be used in the Finance and Operations application to generate outgoing electronic documents.</span></span> <span data-ttu-id="adfd1-106">受信した電子ドキュメントを解析し、これらのドキュメントの内容を使用してアプリケーション データの更新を行う ER 形式をデザインすることもできます。</span><span class="sxs-lookup"><span data-stu-id="adfd1-106">You can also design ER formats that parse incoming electronic documents and use the content in those documents to update application data.</span></span> 

<span data-ttu-id="adfd1-107">この機能により、送信する電子ドキュメントを生成しアプリケーション データを更新するのに、1 つの ER 形式を使用できます。</span><span class="sxs-lookup"><span data-stu-id="adfd1-107">With this functionality, a single ER format can be used to generate outgoing electronic documents and then update the application data.</span></span> <span data-ttu-id="adfd1-108">この機能は以下のシナリオでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="adfd1-108">This feature can be used in the following scenarios:</span></span>

- <span data-ttu-id="adfd1-109">その後のプロセスでアプリケーション データが繰り返し使用されないために、電子ドキュメントを生成するのに使用した直後にアプリケーション データをマークできます。</span><span class="sxs-lookup"><span data-stu-id="adfd1-109">To prevent repeated usage of application data in subsequent processes you can mark an application’s data immediately after it is used to generate electronic documents.</span></span> <span data-ttu-id="adfd1-110">たとえば、支払トランザクションが生成された支払メッセージに含められた直後に、既に処理済みとしてマークすることができます。</span><span class="sxs-lookup"><span data-stu-id="adfd1-110">For example, you can mark payment transactions as already processed immediately after they have been included in a generated payment message.</span></span>
- <span data-ttu-id="adfd1-111">ER ロジックを使用して生成された電子ドキュメントの処理の詳細を格納します。</span><span class="sxs-lookup"><span data-stu-id="adfd1-111">To store the processing details of electronic documents that have been generated using ER logic.</span></span> <span data-ttu-id="adfd1-112">たとえば、固有の支払メッセージ ID は ER 式を使用して生成されます。</span><span class="sxs-lookup"><span data-stu-id="adfd1-112">For example, a unique payment message identification that is generated using the ER expression.</span></span> <span data-ttu-id="adfd1-113">ER 形式がドキュメントを生成するために実行される場合、式は ER ダイアログ ボックスに入力された情報に基づいています。</span><span class="sxs-lookup"><span data-stu-id="adfd1-113">The expression is based on information entered in the ER dialog box when the ER format is run to generate documents.</span></span>

<span data-ttu-id="adfd1-114">この機能の詳細についてさらに知るには、イントラスタットのレポート作成とアーカイブの詳細について説明している、アプリケーションデータ更新のタスクガイド (7.5.4.3 ITサービス/ソリューションコンポーネントの取得/開発（10677）ビジネスプロセスの一部) を使用してER Generate ドキュメントのセットを再生します。</span><span class="sxs-lookup"><span data-stu-id="adfd1-114">To learn more about this feature, play the set of ER Generate documents with application data update Task guides (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process), which walk you through the details of Intrastat reporting and archiving.</span></span> <span data-ttu-id="adfd1-115">次のファイルでは、これらのタスク ガイド内の特定の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="adfd1-115">The following files are required to complete certain steps in these Task guides.</span></span> <span data-ttu-id="adfd1-116">ローカル コンピューターにダウンロードし、これらのファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="adfd1-116">Download and save these files to your local machine.</span></span>

- [<span data-ttu-id="adfd1-117">ER データ モデル コンフィギュレーション: イントラスタット (モデル)</span><span class="sxs-lookup"><span data-stu-id="adfd1-117">ER data model configuration: Intrastat (model)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="adfd1-118">ER モデル マッピング コンフィギュレーション: イントラスタット (マッピング)</span><span class="sxs-lookup"><span data-stu-id="adfd1-118">ER model mapping configuration: Intrastat (mapping)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="adfd1-119">ER 形式コンフィギュレーション: イントラスタット (形式)</span><span class="sxs-lookup"><span data-stu-id="adfd1-119">ER format configuration: Intrastat (format)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)

