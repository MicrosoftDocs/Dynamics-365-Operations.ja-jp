---
title: 仕入先請求書の自動化の結果を表示する (プレビュー)
description: このトピックでは、自動化されたワークフローへの送信プロセスにある仕入先請求書の状態を表示する方法について説明します。
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3b87af4c64f8021a1b23cca5d8f38ac21c8efbd4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248095"
---
# <a name="view-vendor-invoice-automation-results"></a><span data-ttu-id="3286a-103">仕入先請求書の自動化の結果を表示</span><span class="sxs-lookup"><span data-stu-id="3286a-103">View vendor invoice automation results</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3286a-104">このトピックでは、自動化されたワークフローへの送信プロセスにある仕入先請求書の状態を表示する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3286a-104">This topic explains how to view the status of vendor invoices that are in the automated submit-to-workflow process.</span></span> <span data-ttu-id="3286a-105">自動化履歴の詳細は、インポートされた仕入先請求書ごとに管理されます。</span><span class="sxs-lookup"><span data-stu-id="3286a-105">Details of the automation history are maintained for each imported vendor invoice.</span></span> <span data-ttu-id="3286a-106">自動化した業務プロセスに応じて、**保留中の仕入先請求書** ページには **自動受領書照合状態** と **自動化されたワークフローへの送信状態** の値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3286a-106">Depending on the business processes that you've automated, the **Pending vendor invoices** page shows **Automated receipt match status** and **Automated submit to workflow status** values.</span></span> <span data-ttu-id="3286a-107">詳細を表示して、自動化された手順が失敗した請求書に注目する計画を立てることができます。</span><span class="sxs-lookup"><span data-stu-id="3286a-107">You can view the details and make a plan to focus on the invoices that failed an automated step.</span></span> <span data-ttu-id="3286a-108">その後、問題を修正した後、インポートされた請求書の自動化プロセスを再開できます。</span><span class="sxs-lookup"><span data-stu-id="3286a-108">Then, after you correct the issue, you can resume the automated process for the imported invoice.</span></span>

<span data-ttu-id="3286a-109">送信済の請求書を編集する前に、自動化プロセスを一時停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3286a-109">Before you can edit an invoice that has been submitted, you must pause the automated processing.</span></span> <span data-ttu-id="3286a-110">自動化されたワークフローへの送信プロセスの請求書を一時停止する必要がある場合は、**仕入先請求書** ページの **自動化プロセスに含める** フィールドを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="3286a-110">If an invoice in the automated submit-to-workflow process must be paused, set the **Include in Automated processing** field to **No** on the **Vendor invoices** page.</span></span> <span data-ttu-id="3286a-111">その後、**自動化されたプロセス** が **はい** に設定されるまで、自動化は実行されません。</span><span class="sxs-lookup"><span data-stu-id="3286a-111">Automation then won't run until **Include in Automated processing** is set to **Yes**.</span></span> <span data-ttu-id="3286a-112">まだ請求書がワークフロー システムになく、自動化されたプロセスで使用されていない場合は、請求書をその後の自動化から一時停止することができます。</span><span class="sxs-lookup"><span data-stu-id="3286a-112">An invoice can be paused from further automation if it isn't yet in the workflow system and isn't used by the automated process.</span></span>

<span data-ttu-id="3286a-113">インポートされた請求書がワークフローへの送信プロセスの対象になる場合は、**仕入先請求書** ページでその **自動化の状態** の値を表示できます。</span><span class="sxs-lookup"><span data-stu-id="3286a-113">If an imported invoice is subject to the submit-to-workflow process, you can view its **Automation status** value on the **Vendor invoices** page.</span></span> <span data-ttu-id="3286a-114">次の状態が追跡されます。</span><span class="sxs-lookup"><span data-stu-id="3286a-114">The following statuses are tracked:</span></span>

- <span data-ttu-id="3286a-115">**指定済** – **買掛金勘定パラメーター** ページで定義されている自動化されたプロセスは、正常に実行されていますが、まだ完了していません。</span><span class="sxs-lookup"><span data-stu-id="3286a-115">**Included** – The automated processes that are defined on the **Accounts payable parameters** page are running correctly but haven't yet been completed.</span></span>
- <span data-ttu-id="3286a-116">**一時停止** – **買掛金勘定パラメーター** ページで定義されている自動化されたプロセスが実行されましたが、プロセスの少なくとも 1 つの手順が失敗しました。</span><span class="sxs-lookup"><span data-stu-id="3286a-116">**Paused** – The automated processes that are defined on the **Accounts payable parameters** page have run, but at least one step in the process failed.</span></span> <span data-ttu-id="3286a-117">**一時停止** 状態は、**自動化された処理に含める** フィールドが **いいえ** に設定されている場合にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="3286a-117">The **Paused** status is also applied if the **Include in automated processing** field is set to **No**.</span></span> <span data-ttu-id="3286a-118">**最新の結果の表示** を選択すると、失敗を表示できます。</span><span class="sxs-lookup"><span data-stu-id="3286a-118">You can view the failures by selecting **View most recent results**.</span></span>
- <span data-ttu-id="3286a-119">**ワークフロー内** – インポートした請求書は、自動化されたワークフローへの送信プロセスまたは手動でワークフロー システムに送信されました。</span><span class="sxs-lookup"><span data-stu-id="3286a-119">**In workflow** – The imported invoice has been submitted to the workflow system, either by the automated submit-to-workflow process or manually.</span></span>
- <span data-ttu-id="3286a-120">**ワークフローの完了** – インポートされた請求書に対してのワークフロー プロセスが完了しました。</span><span class="sxs-lookup"><span data-stu-id="3286a-120">**Workflow complete** – The workflow process has been completed for the imported invoice.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]