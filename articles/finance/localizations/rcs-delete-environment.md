---
title: Regulatory Configuration Service (RCS) - RCS 環境の削除
description: このトピックでは、Regulatory Configuration Service (RCS) システム管理者が RCS 環境および関連データを削除する方法について説明します。
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 637962cf63bfd8c2330726f33545f939ec91d58d
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295821"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a><span data-ttu-id="c0180-103">Regulatory Configuration Service (RCS) - RCS 環境の削除</span><span class="sxs-lookup"><span data-stu-id="c0180-103">Regulatory Configuration Service (RCS) - Delete an RCS environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0180-104">このトピックでは、Regulatory Configuration Service (RCS) システム管理者が RCS 環境および関連データを削除する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c0180-104">This topic explains how a Regulatory Configuration Service (RCS) system administrator can delete an RCS environment and related data.</span></span>

<span data-ttu-id="c0180-105">このトピックの手順を完了する前に、以下の前提条件を満たす必要があります:</span><span class="sxs-lookup"><span data-stu-id="c0180-105">Before you can complete the procedure in this topic, the following prerequisites must be met:</span></span>

- <span data-ttu-id="c0180-106">ユーザーには、RCS 環境の **システム管理者** ロールが割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c0180-106">You must have the **System Admin** role assigned to you for the RCS environment.</span></span>
- <span data-ttu-id="c0180-107">**システム管理者** ロールには **RCSDeleteEnvironmentDuty** ロールが割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c0180-107">The **System Admin** role must have the **RCSDeleteEnvironmentDuty** role assigned to it.</span></span>

## <a name="delete-an-rcs-environment"></a><span data-ttu-id="c0180-108">RCS 環境の削除</span><span class="sxs-lookup"><span data-stu-id="c0180-108">Delete an RCS environment</span></span>

1. <span data-ttu-id="c0180-109">RCS を開き、**電子申告** ワークスペース タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c0180-109">Open RCS, and select the **Electronic reporting** workspace tile.</span></span>
2. <span data-ttu-id="c0180-110">**関連リンク** セクションで、**RCS 環境の削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0180-110">In the **Related links** section, select **Delete RCS environment**.</span></span>

    ![関連リンク セクションで、RCS 環境リンクを削除する](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. <span data-ttu-id="c0180-112">表示されるダイアログ ボックスで、環境削除のスコープに関するメッセージを確認します。</span><span class="sxs-lookup"><span data-stu-id="c0180-112">In the dialog box that appears, review the messages about the scope of environment deletion.</span></span>

    ![RCS 環境の削除ダイアログ ボックスのメッセージ](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > <span data-ttu-id="c0180-114">RCS 環境の削除は取り消しできません。</span><span class="sxs-lookup"><span data-stu-id="c0180-114">Deletion of an RCS environment can't be reversed.</span></span>
    >
    > <span data-ttu-id="c0180-115">この操作により、選択した RCS 環境、およびグローバル リポジトリに格納されている機能やコンフィギュレーションを含む関連データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="c0180-115">The operation deletes the selected RCS environment and any related data, including features and configurations that are stored in the Global repository.</span></span> <span data-ttu-id="c0180-116">他の組織と共有する機能やコンフィギュレーションは共有解除され、依存関係がない場合は削除されます。</span><span class="sxs-lookup"><span data-stu-id="c0180-116">Features and configurations that are shared with other organizations will be unshared and deleted if they have no dependencies.</span></span> <span data-ttu-id="c0180-117">依存関係がある機能やコンフィギュレーションは、廃止としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="c0180-117">Features and configurations that have dependencies will be marked as discontinued.</span></span>

4. <span data-ttu-id="c0180-118">表示されるフィールドに、RCS 環境のグローバル一意識別子 (GUID) を入力して、削除することを確定します。</span><span class="sxs-lookup"><span data-stu-id="c0180-118">In the field that is provided, enter the globally unique identifier (GUID) of the RCS environment to confirm that you want to delete it.</span></span> <span data-ttu-id="c0180-119">環境の GUID は削除メッセージに含まれます。</span><span class="sxs-lookup"><span data-stu-id="c0180-119">The environment's GUID is included in the deletion message.</span></span>
5. <span data-ttu-id="c0180-120">**環境の削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0180-120">Select **Delete environment**.</span></span>
    
<span data-ttu-id="c0180-121">これで、RCS 環境および関連データが削除されました。</span><span class="sxs-lookup"><span data-stu-id="c0180-121">Your RCS environment and any related data are now deleted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c0180-122">RCS 環境を削除した後に、データを復旧する方法はありません。</span><span class="sxs-lookup"><span data-stu-id="c0180-122">After you delete an RCS environment, there is no way to recover the data.</span></span> <span data-ttu-id="c0180-123">使用可能な任意の RCS 地域に、新しい RCS 環境を作成できます。</span><span class="sxs-lookup"><span data-stu-id="c0180-123">A new RCS environment can be created in any available RCS region.</span></span>
