---
title: 状態が空白の小切手の作成
description: このトピックでは、小切手ページで銀行口座に対して空白の小切手を作成する方法について説明します。
author: abruer
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 1b01daa86055156092d035d61aad78a13349f869
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815959"
---
# <a name="create-checks-that-have-blank-status"></a><span data-ttu-id="dd6c2-103">状態が空白の小切手の作成</span><span class="sxs-lookup"><span data-stu-id="dd6c2-103">Create checks that have Blank status</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd6c2-104">このトピックでは、空白の小切手を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="dd6c2-104">This topic explains how to create blank checks.</span></span> <span data-ttu-id="dd6c2-105">たとえば、破損した小切手を記録して支払いに使用できない場合は、その小切手を空白で作成することができます。</span><span class="sxs-lookup"><span data-stu-id="dd6c2-105">For example, you might create a blank check to record a check that has been damaged and can't be used for payment.</span></span>

<span data-ttu-id="dd6c2-106">**小切手** ページでは、小切手に対してメンテナンス タスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="dd6c2-106">On the **Checks** page, you perform maintenance tasks for checks.</span></span> <span data-ttu-id="dd6c2-107">たとえば、新しい小切手番号を作成したり、小切手を削除したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="dd6c2-107">For example, you can create new check numbers and delete checks.</span></span> <span data-ttu-id="dd6c2-108">また、状態が **空白** の小切手を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="dd6c2-108">You can also create checks that have a status of **Blank**.</span></span> <span data-ttu-id="dd6c2-109">空白の小切手が作成された後は、システムで削除または再利用することはできません。</span><span class="sxs-lookup"><span data-stu-id="dd6c2-109">After blank checks are created, they can't be deleted or reused in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="dd6c2-110">この機能は、**機能管理** ページの **小切手ページで状態が空白の小切手を作成する** 機能をオンにしている場合にのみ、**小切手** ページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="dd6c2-110">This feature is available on the **Checks** page only if you turn on the **Create checks with a blank status on the Checks page** feature on the **Feature management** page.</span></span> <span data-ttu-id="dd6c2-111">この機能が有効になっていない場合、状態が **空白** である小切手は、買掛金勘定の支払生成プロセス中に、**小切手による支払** ダイアログ ボックスからのみ作成できます。</span><span class="sxs-lookup"><span data-stu-id="dd6c2-111">If the feature isn't turned on, checks that have **Blank** status can be created only from the **Payment by check** dialog box during the payment generation process in Accounts payable.</span></span>

<span data-ttu-id="dd6c2-112">**小切手** ページを開くには、**現金および銀行管理 \> 銀行口座 \> 銀行口座** に移動し、アクション ペイン、**支払の管理** タブ、**関連情報** グループで、**小切手** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dd6c2-112">To open the **Checks** page, go to **Cash and bank management \> Bank accounts \> Bank accounts**, and then, on the Action Pane, on the **Manage payments** tab, in the **Related information** group, select **Checks**.</span></span> <span data-ttu-id="dd6c2-113">または、**現金および銀行管理 \> 照会およびレポート \> 小切手** に移動します。</span><span class="sxs-lookup"><span data-stu-id="dd6c2-113">Alternatively, go to **Cash and bank management \> Inquiries and reports \> Checks**.</span></span>

<span data-ttu-id="dd6c2-114">状態が **空白** の小切手を作成するには、アクション ペインで **空白の小切手の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dd6c2-114">Then, to create checks that have **Blank** status, on the Action Pane, select **Create blank checks**.</span></span> <span data-ttu-id="dd6c2-115">システムが空白の小切手を作成している間、関連付けられている銀行口座が一時的に無効化されます。</span><span class="sxs-lookup"><span data-stu-id="dd6c2-115">While the system is creating blank checks, the associated bank account is temporarily inactivated.</span></span> <span data-ttu-id="dd6c2-116">この動作により、空白の小切手が作成されたときと同時に、支払が生成されるリスクが低下します。</span><span class="sxs-lookup"><span data-stu-id="dd6c2-116">This behavior reduces the risk that payments will be generated at the same time that blank checks are created.</span></span> <span data-ttu-id="dd6c2-117">処理が完了すると、関連付けられている銀行口座が再度有効化されます。</span><span class="sxs-lookup"><span data-stu-id="dd6c2-117">When the processing is completed, the associated bank account is reactivated.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]