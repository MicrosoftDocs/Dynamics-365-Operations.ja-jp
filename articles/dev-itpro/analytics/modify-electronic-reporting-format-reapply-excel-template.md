---
title: Excel テンプレートの再適用による電子申告形式の変更
description: このトピックでは、変更後の Excel テンプレートを再適用することによって、ビジネス ドキュメントを生成するために使用される電子レポート (ER) 形式を変更する方法に関する情報を提供します。
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8707f7b184bb66648edd0e48672c5514a0a5caf1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545010"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a><span data-ttu-id="45669-103">Excel テンプレートの再適用による電子申告形式の変更</span><span class="sxs-lookup"><span data-stu-id="45669-103">Modify Electronic reporting formats by reapplying Excel templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45669-104">電子申告 (ER) ツールを使用して、電子的な形式でビジネス ドキュメントを生成します。</span><span class="sxs-lookup"><span data-stu-id="45669-104">The Electronic reporting (ER) tool is used to generate business documents in an electronic format.</span></span> <span data-ttu-id="45669-105">ビジネス ドキュメントを生成するには、ER 形式を作成し、ER デザイナーを使用してビジネス ドキュメントのレイアウトを定義し、それに含まれるように、データを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45669-105">To generate a business document, you must create an ER format, and then use the ER designer to define the layout of the business document and specify the data that should be included in it.</span></span> <span data-ttu-id="45669-106">ビジネス ドキュメントを生成するために ER 形式を実行できます。</span><span class="sxs-lookup"><span data-stu-id="45669-106">You can then run the ER format to generate the business document.</span></span>

<span data-ttu-id="45669-107">Microsoft Excel ファイルとしてのビジネス ドキュメントを生成するために、ER ツールを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="45669-107">The ER tool can be used to generate business documents as Microsoft Excel files.</span></span> <span data-ttu-id="45669-108">Excel ドキュメントは、これらのドキュメントをテンプレートとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="45669-108">You can use an Excel document as a template for these documents.</span></span> <span data-ttu-id="45669-109">ER デザイナーでのドキュメント レイアウトを定義するには、定義済みの ER 形式をテンプレートとして使用する Excel ドキュメントの内容をインポートできます。</span><span class="sxs-lookup"><span data-stu-id="45669-109">To define the document layout in the ER designer, you can import the contents of the Excel document that you want to use as a template into the defined ER format.</span></span> <span data-ttu-id="45669-110">このシナリオ実行の詳細については、**ER は、OPENXML 形式でレポートを生成するコンフィギュレーションを設計する** タスク ガイド (7.5.4.3 IT サービス / ソリューション コンポーネントの取得 / 開発 (10677) ビジネス プロセスの一部) を再生します。</span><span class="sxs-lookup"><span data-stu-id="45669-110">For more details, and to practice this scenario, play the task guide **ER Design a configuration for generating reports in OPENXML format** (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span>

<span data-ttu-id="45669-111">ビジネス ドキュメントのテンプレートとして使用される Excel ドキュメントを編集する場合は、新しい ER 機能では、ER 形式に更新されたテンプレートを適用することができます。</span><span class="sxs-lookup"><span data-stu-id="45669-111">If you edit the Excel document that is used as a template for a business document, new ER functionality lets you reapply the updated template to the ER format.</span></span> <span data-ttu-id="45669-112">更新されたテンプレートに準拠できるように、ER 形式が更新されます。</span><span class="sxs-lookup"><span data-stu-id="45669-112">The ER format is then updated so that it adheres to the updated template.</span></span> <span data-ttu-id="45669-113">この機能の詳細については、**ER は Excel テンプレートの更新を反映して形式を変更する** (7.5.5.3取得/作成ITサービス/ソリューション コンポーネント (10683) 業務プロセスの一部) タスクガイドを再生してください。</span><span class="sxs-lookup"><span data-stu-id="45669-113">For more details about this functionality, play the task guide **ER Modify a format by reapplying an Excel template** (part of the 7.5.5.3 Acquire/Develop IT service/solution components (10683) business process).</span></span> <span data-ttu-id="45669-114">更新されたテンプレートをインポートするタスクガイド ステップでは、支払レポート Excel ファイルの変更されたテンプレートである SampleVendPaymWsReport2 をテンプレートとして使用します。</span><span class="sxs-lookup"><span data-stu-id="45669-114">In the task guide step where you import an updated template, use the modified template of the Payment Report Excel file, SampleVendPaymWsReport2, as a template.</span></span>
