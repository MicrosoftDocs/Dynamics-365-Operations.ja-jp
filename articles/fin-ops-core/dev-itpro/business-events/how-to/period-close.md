---
title: 財務期間終了のビジネス イベント
description: このトピックでは、財務期間終了の業務プロセスでビジネス イベントを使用して、情報を取得し、内部コントロールを提供する方法について説明します。
author: suhasrao1985
manager: AnnBe
ms.date: 10/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: Platform update 26
ms.dyn365.ops.version: 2019-6-30
ms.openlocfilehash: 3584ccec8827c36cba8a02ca8c419c8f4b49b404
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893261"
---
# <a name="business-events-in-financial-period-close"></a><span data-ttu-id="d8a42-103">財務期間終了のビジネス イベント</span><span class="sxs-lookup"><span data-stu-id="d8a42-103">Business events in financial period close</span></span>
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d8a42-104">このトピックでは、財務期間終了の業務プロセスでビジネス イベントを使用して、情報を取得し、内部コントロールを提供する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d8a42-104">This topic explains how to use business events in the financial period close business process to gain insights and provide internal controls.</span></span>

<span data-ttu-id="d8a42-105">このトピックを完了するには、プラットフォーム アップデート 26 以降で、バージョン 10.0.2 (2019 年 5 月) を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8a42-105">To complete this topic, you must be running version 10.0.2 (May 2019) with Platform update 26 or later.</span></span>

## <a name="scenario-overview"></a><span data-ttu-id="d8a42-106">シナリオの概要</span><span class="sxs-lookup"><span data-stu-id="d8a42-106">Scenario overview</span></span>

<span data-ttu-id="d8a42-107">タスク管理は、業界全体にわたる業務プロセスを管理するための基本となる要素です。</span><span class="sxs-lookup"><span data-stu-id="d8a42-107">Task management is fundamental to managing business processes across industries.</span></span> <span data-ttu-id="d8a42-108">最初から用意されている機能により、ユーザーは業務プロセス タスクを構造化された方法で管理できるようになります。</span><span class="sxs-lookup"><span data-stu-id="d8a42-108">Out-of-box capabilities let users manage business process tasks in a structured manner.</span></span> <span data-ttu-id="d8a42-109">**財務期間終了**ワークスペースは、会社の会計期間の終了プロセスでのタスクを管理するため中心となる場所を提供することにより、これらの機能を示しています。</span><span class="sxs-lookup"><span data-stu-id="d8a42-109">The **Financial period close** workspace illustrates these capabilities by offering a central location for managing tasks in a company's accounting period close process.</span></span>

<span data-ttu-id="d8a42-110">このトピックでは、**財務期間終了**ワークスペースを使用して、すべての期間終了に関連付けられたタスクを追跡およびレポートする方法を調査することに最近決めた組織について取り上げます。</span><span class="sxs-lookup"><span data-stu-id="d8a42-110">This topic looks at an organization that recently decided to explore how it can use the **Financial period close** workspace to track and report tasks that are associated with every period close.</span></span> <span data-ttu-id="d8a42-111">パフォーマンス管理とトレーサビリティは、現在の設定でこの組織が直面する課題の一部です。</span><span class="sxs-lookup"><span data-stu-id="d8a42-111">Performance management and traceability are some of the challenges that this organization faces in the current setup.</span></span> <span data-ttu-id="d8a42-112">そのため、組織は業務プロセスの変革に取り組み、**財務期間終了**ワークスペースの機能を識別しました。</span><span class="sxs-lookup"><span data-stu-id="d8a42-112">Therefore, the organization undertook an exercise in business process transformation to identify the capabilities of the **Financial period close** workspace.</span></span> <span data-ttu-id="d8a42-113">この演習では、次のような業務要件が明らかになりました。</span><span class="sxs-lookup"><span data-stu-id="d8a42-113">This exercise revealed the following business requirements:</span></span>

1. <span data-ttu-id="d8a42-114">タスクを開始する必要があるときに通知を受ける機能</span><span class="sxs-lookup"><span data-stu-id="d8a42-114">The ability to be notified when tasks must be started</span></span>
2. <span data-ttu-id="d8a42-115">ドキュメントを添付するための機能</span><span class="sxs-lookup"><span data-stu-id="d8a42-115">The ability to attach documents</span></span>
3. <span data-ttu-id="d8a42-116">添付ファイルの記録管理と廃棄機能</span><span class="sxs-lookup"><span data-stu-id="d8a42-116">Record management and disposition capabilities for attachments</span></span>
4. <span data-ttu-id="d8a42-117">事前に定義されたロジックに基づいて、複数の承認者がタスクを承認する機能</span><span class="sxs-lookup"><span data-stu-id="d8a42-117">The ability for multiple approvers to approve tasks, based on predefined logic</span></span>
5. <span data-ttu-id="d8a42-118">監査のためのタスク アンケート</span><span class="sxs-lookup"><span data-stu-id="d8a42-118">Task questionnaires for audits</span></span>
6. <span data-ttu-id="d8a42-119">期間終了プロセスの現在のステータスを追跡し、効率を把握するためのパフォーマンス分析を行うレポート機能</span><span class="sxs-lookup"><span data-stu-id="d8a42-119">Reporting capabilities to track the current status of the period close process and do performance analysis for insights into efficiency</span></span>

## <a name="high-level-design"></a><span data-ttu-id="d8a42-120">高レベル設計</span><span class="sxs-lookup"><span data-stu-id="d8a42-120">High-level design</span></span>

<span data-ttu-id="d8a42-121">前述の要件を達成するために、組織は**財務期間終了**ワークスペースに最初から用意されている機能を使用しました。</span><span class="sxs-lookup"><span data-stu-id="d8a42-121">To achieve the previously mentioned requirements, the organization used out-of-box capabilities of the **Financial period close** workspace.</span></span> <span data-ttu-id="d8a42-122">ギャップ分析により、ワークスペースと基礎となるデータ エンティティに対してマイナーな拡張を実行することにより、組織は要件 2、5、および 6 を達成し、要件 4 を 部分的に達成できることが明らかになりました。</span><span class="sxs-lookup"><span data-stu-id="d8a42-122">A gap analysis revealed that, by doing minor extensions to the workspace and the underlying data entities, the organization could achieve requirements 2, 5, and 6, and could partially achieve requirement 4.</span></span><span data-ttu-id="d8a42-123">要件 1 と 3、および要件 4 の一部を達成するために、組織は Power Automate の使用を選択しました。</span><span class="sxs-lookup"><span data-stu-id="d8a42-123"> To achieve requirements 1 and 3, and parts of requirement 4, the organization chose to use Power Automate.</span></span> <span data-ttu-id="d8a42-124">次の図は、ソリューションのアーキテクチャの概要を表示します。</span><span class="sxs-lookup"><span data-stu-id="d8a42-124">The following illustration shows an architectural overview of the solution.</span></span>

<img alt="High-level design" src="../../media/Image1.PNG" width="70%">

## <a name="managing-attachments-by-using-microsoft-power-automate-and-sharepoint-online"></a><span data-ttu-id="d8a42-125">Microsoft Power Automate および SharePoint オンライン を使用した添付ファイルの管理</span><span class="sxs-lookup"><span data-stu-id="d8a42-125">Managing attachments by using Microsoft Power Automate and SharePoint Online</span></span>

<span data-ttu-id="d8a42-126">経理担当者は**財務期間終了**ワークスペースにタスクを表示して、作業を開始します。</span><span class="sxs-lookup"><span data-stu-id="d8a42-126">Accountants view their tasks in the **Financial period close** workspace and start to work on them.</span></span> <span data-ttu-id="d8a42-127">SharePoint Online ドキュメント タイプを使用して、添付ファイルがタスクに追加されます。</span><span class="sxs-lookup"><span data-stu-id="d8a42-127">Attachments are added to the task by using a SharePoint Online document type.</span></span> <span data-ttu-id="d8a42-128">Microsoft Power Automate の SharePoint トリガーは、次の図に示す Power Automate をトリガーするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d8a42-128">SharePoint triggers in Microsoft Power Automate are used to trigger the Power Automate that is shown in the following illustration.</span></span> <span data-ttu-id="d8a42-129">この Power Automate は SharePoint メタデータを、 **財務期間終了** ワークスペースのタスクからのメタデータで更新します。</span><span class="sxs-lookup"><span data-stu-id="d8a42-129">This Power Automate updates the SharePoint metadata with metadata from the task in the **Financial period close** workspace.</span></span> <span data-ttu-id="d8a42-130">この目的のために、ドキュメント ライブラリに SharePoint 列が作成されました。</span><span class="sxs-lookup"><span data-stu-id="d8a42-130">SharePoint columns were created for this purpose in the document library.</span></span> <span data-ttu-id="d8a42-131">**財務期間終了**ワークスペースに追加されるすべての添付ファイルの添付ファイル メタデータを保持するために、個別の添付ファイル データ エンティティが作成されました。</span><span class="sxs-lookup"><span data-stu-id="d8a42-131">A separate attachment data entity was created to hold the attachment metadata for every attachment that is added to the **Financial period close** workspace.</span></span> <span data-ttu-id="d8a42-132">カスタム エンティティのフィールドは、 Power Automate 内の SharePoint オンライン列にマップされました。</span><span class="sxs-lookup"><span data-stu-id="d8a42-132">Fields from the custom entity were mapped to the SharePoint Online columns in the Power Automate.</span></span> <span data-ttu-id="d8a42-133">指定されたドキュメント タイプを使用するドキュメントが定義済みの SharePoint Online ライブラリに作成されると、Power Automate がトリガーされ、カスタム データ エンティティからメタデータを取得し、SharePoint Online のドキュメントのメタデータ列を更新します。</span><span class="sxs-lookup"><span data-stu-id="d8a42-133">When documents that use the specified document type are created in the predefined SharePoint Online library, Power Automate is triggered, obtains the metadata from the custom data entity, and updates the document's metadata columns in SharePoint Online.</span></span>

<img alt="Power Automate for managing attachments" src="../../media/Image2.png" width="70%">

## <a name="enabling-internal-controls-by-using-business-events-and-power-automate"></a><span data-ttu-id="d8a42-134">ビジネス イベントと Power Automate を使用した内部コントロールの有効化</span><span class="sxs-lookup"><span data-stu-id="d8a42-134">Enabling internal controls by using business events and Power Automate</span></span>

<span data-ttu-id="d8a42-135">経理担当者がタスクを完了し、タスクのレビュー準備が整うと、**確認状態**カスタム フィールドの値が**確認準備完了**に更新されます。</span><span class="sxs-lookup"><span data-stu-id="d8a42-135">As accountants complete their tasks, and the tasks become ready for review, the value of the **Review status** custom field is updated to **Ready for review**.</span></span> <span data-ttu-id="d8a42-136">この更新が行われると **変更ベースのアラートがトリガーされる** ビジネス イベントによって Power Automate がトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="d8a42-136">The Power Automate gets triggered by the **When the change-based alert is triggered** business event when this update is made.</span></span> <span data-ttu-id="d8a42-137">このビジネス イベントのペイロードには、タスク名と領域名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d8a42-137">The payload of this business event contains the task name and the area name.</span></span> <span data-ttu-id="d8a42-138">Power Automate は、タスク名と領域名の組み合わせと **確認状態** フィールドの値を使用して、 Power Automate によって調整された電子メール ベースのワークフローを介してタスクをルーティングします。</span><span class="sxs-lookup"><span data-stu-id="d8a42-138">The Power Automate uses the combination of the task name and area name, together with the value of the **Review status** field, to route the task through an email-based workflow that is orchestrated by Power Automate.</span></span> <span data-ttu-id="d8a42-139">この Power Automate は、承認を待機し、タスク ログに新しいコメントを追加し、承認プロセスの結果と関連するメタデータの両方に基づいて **財務期間終了** ワークスペースでタスクを更新します。</span><span class="sxs-lookup"><span data-stu-id="d8a42-139">The Power Automate waits for approval, add new comments to the task log, and updates the task in the **Financial period close** workspace , based on both the outcome of the approval process and related metadata.</span></span> <span data-ttu-id="d8a42-140">カスタム データ エンティティは、Power Automate を使用して、**財務期間終了**ワークスペースをクエリおよび更新するために構築されました。</span><span class="sxs-lookup"><span data-stu-id="d8a42-140">Custom data entities were built in to query and update the **Financial period close** workspace by using Power Automate.</span></span>

### <a name="subscribing-to-the-business-event"></a><span data-ttu-id="d8a42-141">ビジネス イベントの購読</span><span class="sxs-lookup"><span data-stu-id="d8a42-141">Subscribing to the business event</span></span>

<span data-ttu-id="d8a42-142">次の例は、変更ベースのアラート ビジネス イベントをサブスクライブする一般的な手順を示しています。</span><span class="sxs-lookup"><span data-stu-id="d8a42-142">The following example describes the general steps for subscribing to a change-based alert business event.</span></span>

1. <span data-ttu-id="d8a42-143">コネクタ トリガーを Power Automate アプリに追加し、変更ベースのアラート ビジネス イベントをサブスクライブします。</span><span class="sxs-lookup"><span data-stu-id="d8a42-143">Add the connector trigger to the Power Automate app, and subscribe to the change-based alert business event.</span></span>

    <img alt="Subscribing to the business event" src="../../media/Image3.png" width="70%">

2. <span data-ttu-id="d8a42-144">ビジネス イベントのペイロードを解析します。</span><span class="sxs-lookup"><span data-stu-id="d8a42-144">Parse the business event payload.</span></span>

    <span data-ttu-id="d8a42-145">ビジネス イベントがトリガーされると、それは Power Automate をトリガーします。</span><span class="sxs-lookup"><span data-stu-id="d8a42-145">When the business event is triggered, it triggers Power Automate.</span></span> <span data-ttu-id="d8a42-146">このビジネス イベントにはペイロードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d8a42-146">This business event contains a payload.</span></span> <span data-ttu-id="d8a42-147">この手順では、ペイロードを解析し、必要な変数を初期化します。</span><span class="sxs-lookup"><span data-stu-id="d8a42-147">In this step, the payload is parsed, and the required variables are initialized.</span></span>

    <img alt="Parsing the business event payload" src="../../media/Image4.PNG" width="70%">

3. <span data-ttu-id="d8a42-148">ペイロードの値に基づいてタスクを取得します。</span><span class="sxs-lookup"><span data-stu-id="d8a42-148">Retrieve the task, based on the values from the payload.</span></span>

    <span data-ttu-id="d8a42-149">タスクが更新されると、ビジネスイベントは Power Automate をトリガーします。</span><span class="sxs-lookup"><span data-stu-id="d8a42-149">When the task is updated, the business event triggers Power Automate.</span></span> <span data-ttu-id="d8a42-150">この時点で、ペイロードが解析された後、タスクに関する基本情報がわかります。</span><span class="sxs-lookup"><span data-stu-id="d8a42-150">At that point, after the payload has been parsed, you will know basic information about the task.</span></span> <span data-ttu-id="d8a42-151">この手順では、カスタム データ エンティティを使用して、タスクに関する詳細情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="d8a42-151">In this step, the custom data entity is used to retrieve more information about the task.</span></span>

    <img alt="Retrieving the task" src="../../media/Image5.png" width="70%">

4. <span data-ttu-id="d8a42-152">基準に基づいて Microsoft Excel ファイルから承認者を取得します。</span><span class="sxs-lookup"><span data-stu-id="d8a42-152">Retrieve approvers from the Microsoft Excel file, based on the criteria.</span></span>

    <span data-ttu-id="d8a42-153">次に、承認者の一覧を決定して、適切な方法で承認要求を送信できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8a42-153">Next, you must determine the list of approvers, so that you can send the approval request in the appropriate manner.</span></span> <span data-ttu-id="d8a42-154">このリストは、SharePoint Online ライブラリ内のカスタム Excel ファイルです。</span><span class="sxs-lookup"><span data-stu-id="d8a42-154">This list is a custom Excel file in a SharePoint Online library.</span></span> <span data-ttu-id="d8a42-155">この手順では、Excel ファイルをクエリして承認者の一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="d8a42-155">In this step, you query the Excel file to get the list of approvers.</span></span> <span data-ttu-id="d8a42-156">また、各タスクの添付ファイルへのリンクを取得して、添付ファイルを承認者に送信できるようにします。</span><span class="sxs-lookup"><span data-stu-id="d8a42-156">You also get the links to the attachments for each task, so that you can send the attachments to the approvers.</span></span>

    <img alt="Retrieving approvers" src="../../media/Image6.png" width="70%">

5. <span data-ttu-id="d8a42-157">承認要求を送信するための準備を行います。</span><span class="sxs-lookup"><span data-stu-id="d8a42-157">Prepare to send the request for approval.</span></span>

    <span data-ttu-id="d8a42-158">このステップでは、前の手順で収集および組み立てたすべての情報を使用して、承認要求を送信するように Power Automate を準備します。</span><span class="sxs-lookup"><span data-stu-id="d8a42-158">In this step, you prepare Power Automate to send the approval request by using all the information that was gathered and assembled in the previous step.</span></span>

    <img alt="Preparing to send the request for approval, part 1" src="../../media/Image7.png" width="70%">

    <img alt="Preparing to send the request for approval, part 2" src="../../media/Image8.png" width="70%">

    <img alt="Preparing to send the request for approval, part 3" src="../../media/Image9.png" width="70%">

6. <span data-ttu-id="d8a42-159">承認プロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="d8a42-159">Start the approval process.</span></span>

    <span data-ttu-id="d8a42-160">このステップでは、承認要求は Power Automate から送信されます。</span><span class="sxs-lookup"><span data-stu-id="d8a42-160">In this step, the approval request is sent from Power Automate.</span></span>

    <img alt="Starting the approval process" src="../../media/Image10.png" width="70%">

7. <span data-ttu-id="d8a42-161">承認者が実行する承認アクションを処理します。</span><span class="sxs-lookup"><span data-stu-id="d8a42-161">Process the approval action that is taken by approvers.</span></span>

    <span data-ttu-id="d8a42-162">承認者が承認要求を受信し、アクションを実行すると、 Power Automate が通知され、追加の処理が行われます。</span><span class="sxs-lookup"><span data-stu-id="d8a42-162">After the approvers receive the approval request and take action, the Power Automate is notified, and additional processing is done.</span></span>

    <img alt="Processing the approval action" src="../../media/Image11.png" width="70%">

8. <span data-ttu-id="d8a42-163">承認結果を使用してタスクを更新します。</span><span class="sxs-lookup"><span data-stu-id="d8a42-163">Update the task with the approval outcome.</span></span>

    <span data-ttu-id="d8a42-164">承認プロセスの結果に基づいて、タスクがその結果で更新されます。</span><span class="sxs-lookup"><span data-stu-id="d8a42-164">Based on the outcome of the approval process, the task is updated with the result.</span></span>

    <img alt="Updating the task, part 1" src="../../media/Image12.png" width="70%">

    <img alt="Updating the task, part 2" src="../../media/Image13.png" width="70%">

## <a name="conclusion"></a><span data-ttu-id="d8a42-165">まとめ</span><span class="sxs-lookup"><span data-stu-id="d8a42-165">Conclusion</span></span>

<span data-ttu-id="d8a42-166">このトピックで説明する組織の業務要件については、このソリューションの開発は最小限であり、主に**財務期間終了**ワークスペース、ビジネス イベント、SharePoint Online、および Power Automate に依存して機能を推進しています。</span><span class="sxs-lookup"><span data-stu-id="d8a42-166">For the business requirements of the organization that is described in this topic, this solution involves minimal development and relies mostly on the **Financial period close** workspace, business events, SharePoint Online, and Power Automate to drive functionality.</span></span> <span data-ttu-id="d8a42-167">開発は、ページへのフィールドの追加、カスタム データ エンティティの作成、およびページ ラベルの変更に制限されています。</span><span class="sxs-lookup"><span data-stu-id="d8a42-167">Development is restricted to the addition of fields to pages, the creation of custom data entities, and changes to page labels.</span></span> <span data-ttu-id="d8a42-168">Power Automate は、承認プロセスの柔軟性も高めています。</span><span class="sxs-lookup"><span data-stu-id="d8a42-168">Power Automate also provides greater flexibility in the approval process.</span></span> <span data-ttu-id="d8a42-169">このソリューションは Microsoft 365 スイート内のさまざまなアプリケーションを利用するため、内部ユーザーは既に使い慣れているアプリケーションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d8a42-169">Because the solution takes advantage of the various applications in the Microsoft 365 suite, internal users can use applications that they are already familiar with.</span></span> <span data-ttu-id="d8a42-170">したがって、必要な変更管理の量は限られています。</span><span class="sxs-lookup"><span data-stu-id="d8a42-170">Therefore, the amount of change management that is required is limited.</span></span>

<span data-ttu-id="d8a42-171">結論として、ビジネス イベントは機能を拡張する固有の機会を提供しますが、アプリ内での広範なカスタマイズを回避させることもできます。</span><span class="sxs-lookup"><span data-stu-id="d8a42-171">In conclusion, business events offer unique opportunities for extending functionality but also let you avoid extensive in-app customizations.</span></span> <span data-ttu-id="d8a42-172">ビジネス イベントの使用を開始する前に、以下の点について考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8a42-172">Here are some things to consider before you start to use business events:</span></span>

- <span data-ttu-id="d8a42-173">ソリューションのセキュリティ要件を設定します。</span><span class="sxs-lookup"><span data-stu-id="d8a42-173">Establish the security requirements of your solution.</span></span> <span data-ttu-id="d8a42-174">ビジネス イベントはロールベースのセキュリティを遵守します。</span><span class="sxs-lookup"><span data-stu-id="d8a42-174">Business events honor role-based security.</span></span> <span data-ttu-id="d8a42-175">この動作は、一部のユース ケースでは有益な場合があります。</span><span class="sxs-lookup"><span data-stu-id="d8a42-175">This behavior can be beneficial in some use cases.</span></span>
- <span data-ttu-id="d8a42-176">ビジネス イベント機能は、今後も拡張されます。</span><span class="sxs-lookup"><span data-stu-id="d8a42-176">Business events functionality continues to get enhanced.</span></span> <span data-ttu-id="d8a42-177">新しい機能に注目してください。</span><span class="sxs-lookup"><span data-stu-id="d8a42-177">Be on the lookout for new capabilities.</span></span>

<span data-ttu-id="d8a42-178">ビジネスイベントおよび Power Automate はローコードまたはコードなしの拡張機能を実装するための優れた機会を提供します。</span><span class="sxs-lookup"><span data-stu-id="d8a42-178">Business events and Power Automate offer great opportunities for implementing low-code or no-code extensions.</span></span> <span data-ttu-id="d8a42-179">重要な点は、このフレームワークが役立つ機会を特定することですが、いくつかの制限事項についても理解しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8a42-179">The important thing is that you identify opportunities where this framework can help, but that you also understand some of the limitations.</span></span>
