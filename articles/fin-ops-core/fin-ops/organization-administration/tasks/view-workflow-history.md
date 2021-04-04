---
title: ワークフロー履歴の表示
description: このトピックでは、処理および承認のためにワークフロー システムに送信されたドキュメントの状態を表示する手順について説明します。
author: jasongre
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a7c6edd53ebafb0bab894fec9c50d834d24b990
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568007"
---
# <a name="view-workflow-history"></a><span data-ttu-id="89789-103">ワークフロー履歴の表示</span><span class="sxs-lookup"><span data-stu-id="89789-103">View workflow history</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="89789-104">このトピックでは、処理および承認のためにワークフロー システムに送信されたドキュメントの状態を表示する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="89789-104">This topic describes the steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="89789-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="89789-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="89789-106">**ナビゲーション ウィンドウ > モジュール > 共通 > 照会 > ワークフロー > ワークフロー履歴** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="89789-106">Go to **Navigation pane > Modules > Common > Inquiries > Workflow > Workflow history**.</span></span>
    - <span data-ttu-id="89789-107">処理および承認のためにワークフロー システムに送信されたドキュメントの状態を表示するには、このフォームを使用します。</span><span class="sxs-lookup"><span data-stu-id="89789-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    - <span data-ttu-id="89789-108">**インスタンス ID** は、ドキュメントを処理中または処理済のワークフロー インスタンスにおける ID コードです。</span><span class="sxs-lookup"><span data-stu-id="89789-108">The **Instance ID** is the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="89789-109">**状態** はドキュメントのワークフローの状態です。</span><span class="sxs-lookup"><span data-stu-id="89789-109">The **Status** is the workflow status of the document.</span></span>  
    - <span data-ttu-id="89789-110">**ワークフロー ID** はドキュメントを処理中のワークフロー、またはドキュメントを処理したワークフローの ID コードです。</span><span class="sxs-lookup"><span data-stu-id="89789-110">The **Workflow ID** is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="89789-111">**ドキュメント** はドキュメントの ID コードです。</span><span class="sxs-lookup"><span data-stu-id="89789-111">The **Document** is the identification code of the document.</span></span>  
    - <span data-ttu-id="89789-112">**ドキュメント タイプ** は、処理用に送信されたドキュメントのタイプです。</span><span class="sxs-lookup"><span data-stu-id="89789-112">The **Document type** is the type of document that was submitted for processing.</span></span>  
    - <span data-ttu-id="89789-113">**ワークフロー** はドキュメントを処理中のワークフロー、またはドキュメントを処理したワークフローの名前です。</span><span class="sxs-lookup"><span data-stu-id="89789-113">The **Workflow** is the name of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="89789-114">**バージョン** はドキュメントを処理中のワークフロー、またはこのドキュメントを処理したワークフローのバージョン番号です。</span><span class="sxs-lookup"><span data-stu-id="89789-114">The **Version** is the version number of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="89789-115">**作成日時** はドキュメントを送信した日時です。</span><span class="sxs-lookup"><span data-stu-id="89789-115">The **Created date and time** is the date and time that the document was submitted.</span></span>  
    - <span data-ttu-id="89789-116">**経過時間** はドキュメントが送信されてからの経過時間です。</span><span class="sxs-lookup"><span data-stu-id="89789-116">The **Elapsed time** is the time that has passed since the document was submitted.</span></span>  
    - <span data-ttu-id="89789-117">**再開** ボタンを使用すると、選択したドキュメントのワークフロー プロセスを再開することができます。</span><span class="sxs-lookup"><span data-stu-id="89789-117">The **Resume** button allows you to resume the workflow process for the selected document.</span></span>  
    - <span data-ttu-id="89789-118">**取り消し** ボタンはを使用すると、選択したドキュメントが処理されないように取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="89789-118">The **Recall** button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="89789-119">一覧で、目的の行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="89789-119">In the list, select the link in the desired row.</span></span>
    - <span data-ttu-id="89789-120">**作業項目** セクションが展開されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="89789-120">Make sure the **Work items** section is expanded.</span></span> <span data-ttu-id="89789-121">このセクションでは、選択したドキュメントに関連付けられている作業項目を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="89789-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="89789-122">たとえば、完了する必要があるタスクや、承認する必要があるドキュメントが表示されます。</span><span class="sxs-lookup"><span data-stu-id="89789-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    - <span data-ttu-id="89789-123">**再割り当て** ボタンは、作業項目を別のユーザーに再度割り当てることができるダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="89789-123">The **Reassign** button will open a dialog box where you can reassign a work item to another user.</span></span>  
    - <span data-ttu-id="89789-124">**追跡の詳細** セクションが展開されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="89789-124">Make sure the **Tracking details** section is expanded.</span></span> <span data-ttu-id="89789-125">このセクションでは、選択したドキュメントのワークフロー履歴を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="89789-125">In this section you can view the workflow history of the selected document.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]