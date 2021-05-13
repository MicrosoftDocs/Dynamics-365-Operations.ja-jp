---
title: 電子申告の生成および ER によるアプリケーション データの更新
description: 送信する電子ドキュメントを生成するために、アプリケーションで使用できる電子申告 (ER) 形式をデザインできます。
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f66a173c7d66f915a7802e42caf1a36f661eea1
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944320"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a><span data-ttu-id="b4db6-103">ER を使用して電子ドキュメントを生成し、アプリケーション データを更新する</span><span class="sxs-lookup"><span data-stu-id="b4db6-103">Generate electronic documents and update application data by using ER</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4db6-104">送信する電子ドキュメントを生成するために、アプリケーションで使用できる電子申告 (ER) 形式をデザインできます。</span><span class="sxs-lookup"><span data-stu-id="b4db6-104">You can design Electronic reporting (ER) formats that can be used in the application to generate outgoing electronic documents.</span></span> <span data-ttu-id="b4db6-105">受信した電子ドキュメントを解析し、これらのドキュメントの内容を使用してアプリケーション データの更新を行う ER 形式をデザインすることもできます。</span><span class="sxs-lookup"><span data-stu-id="b4db6-105">You can also design ER formats that parse incoming electronic documents and use the content in those documents to update application data.</span></span>

<span data-ttu-id="b4db6-106">この機能により、送信する電子ドキュメントを生成しアプリケーション データを更新するのに、1 つの ER 形式を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b4db6-106">With this functionality, a single ER format can be used to generate outgoing electronic documents and then update the application data.</span></span> <span data-ttu-id="b4db6-107">この機能は以下のシナリオでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="b4db6-107">This feature can be used in the following scenarios:</span></span>

- <span data-ttu-id="b4db6-108">その後のプロセスでアプリケーション データが繰り返し使用されないために、電子ドキュメントを生成するのに使用した直後にアプリケーション データをマークできます。</span><span class="sxs-lookup"><span data-stu-id="b4db6-108">To prevent repeated usage of application data in subsequent processes you can mark an application’s data immediately after it is used to generate electronic documents.</span></span> <span data-ttu-id="b4db6-109">たとえば、支払トランザクションが生成された支払メッセージに含められた直後に、既に処理済みとしてマークすることができます。</span><span class="sxs-lookup"><span data-stu-id="b4db6-109">For example, you can mark payment transactions as already processed immediately after they have been included in a generated payment message.</span></span>
- <span data-ttu-id="b4db6-110">ER ロジックを使用して生成された電子ドキュメントの処理の詳細を格納します。</span><span class="sxs-lookup"><span data-stu-id="b4db6-110">To store the processing details of electronic documents that have been generated using ER logic.</span></span> <span data-ttu-id="b4db6-111">たとえば、固有の支払メッセージ ID は ER 式を使用して生成されます。</span><span class="sxs-lookup"><span data-stu-id="b4db6-111">For example, a unique payment message identification that is generated using the ER expression.</span></span> <span data-ttu-id="b4db6-112">ER 形式がドキュメントを生成するために実行される場合、式は ER ダイアログ ボックスに入力された情報に基づいています。</span><span class="sxs-lookup"><span data-stu-id="b4db6-112">The expression is based on information entered in the ER dialog box when the ER format is run to generate documents.</span></span>

<span data-ttu-id="b4db6-113">この機能の詳細についてさらに知るには、イントラスタットのレポート作成とアーカイブの詳細について説明している、アプリケーションデータ更新のタスクガイド (7.5.4.3 ITサービス/ソリューションコンポーネントの取得/開発（10677）ビジネスプロセスの一部) を使用してER Generate ドキュメントのセットを再生します。</span><span class="sxs-lookup"><span data-stu-id="b4db6-113">To learn more about this feature, play the set of ER Generate documents with application data update Task guides (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process), which walk you through the details of Intrastat reporting and archiving.</span></span> <span data-ttu-id="b4db6-114">次のファイルでは、これらのタスク ガイド内の特定の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4db6-114">The following files are required to complete certain steps in these Task guides.</span></span> <span data-ttu-id="b4db6-115">ローカル コンピューターにダウンロードし、これらのファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="b4db6-115">Download and save these files to your local machine.</span></span>

- [<span data-ttu-id="b4db6-116">ER データ モデル コンフィギュレーション: イントラスタット (モデル)</span><span class="sxs-lookup"><span data-stu-id="b4db6-116">ER data model configuration: Intrastat (model)</span></span>](https://download.microsoft.com/download/9/c/e/9ceeacbe-c13e-422e-96f2-594c4a6b45b7/Intrastatmodel.xml)
- [<span data-ttu-id="b4db6-117">ER モデル マッピング コンフィギュレーション: イントラスタット (マッピング)</span><span class="sxs-lookup"><span data-stu-id="b4db6-117">ER model mapping configuration: Intrastat (mapping)</span></span>](https://download.microsoft.com/download/2/1/d/21ddaaeb-64c5-4408-a35f-1ccb922d40a4/Intrastatmapping.xml)
- [<span data-ttu-id="b4db6-118">ER 形式コンフィギュレーション: イントラスタット (形式)</span><span class="sxs-lookup"><span data-stu-id="b4db6-118">ER format configuration: Intrastat (format)</span></span>](https://download.microsoft.com/download/8/b/b/8bbb8891-e88d-4739-b92a-2d1d2fffcb79/Intrastatformat.xml)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
