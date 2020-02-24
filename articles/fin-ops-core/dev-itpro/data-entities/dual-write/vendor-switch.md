---
title: 仕入先デザインの切り替え
description: このトピックでは、Finance and Operations アプリと Common Data Service 間の仕入先データの統合を切り替える方法について説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 587a9b98f28b11e303aff4b59e9726f220d956eb
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019873"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="67840-103">仕入先デザインの切り替え</span><span class="sxs-lookup"><span data-stu-id="67840-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="67840-104">仕入先データ フロー</span><span class="sxs-lookup"><span data-stu-id="67840-104">Vendor data flow</span></span> 

<span data-ttu-id="67840-105">仕入先のマスタリングにその他の Dynamics 365 アプリを使用し、顧客から仕入先情報を分離する場合は、この基本的な仕入先設計を使用します。</span><span class="sxs-lookup"><span data-stu-id="67840-105">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![基本的な仕入先フロー](media/dual-write-vendor-data-flow.png)
 
<span data-ttu-id="67840-107">仕入先のマスタリングにその他の Dynamics 365 アプリを使用し、仕入先情報を格納するため**アカウント** エンティティを使用し続ける場合は、この拡張された仕入先設計を使用します。</span><span class="sxs-lookup"><span data-stu-id="67840-107">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="67840-108">この設計では、仕入先の保留ステータスや仕入先のプロファイルなどの拡張仕入先情報が Common Data Service の**仕入先**エンティティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="67840-108">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![拡張された仕入先データ フロー](media/dual-write-vendor-detail.jpg)
 
<span data-ttu-id="67840-110">次の手順に従って、仕入先の拡張設計を使用します。</span><span class="sxs-lookup"><span data-stu-id="67840-110">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="67840-111">**SupplyChainCommon** ソリューション パッケージには、次の図に示すようなワークフロー プロセス テンプレートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="67840-111">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="67840-112">![ワークフロー プロセス テンプレート](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="67840-112">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="67840-113">ワークフロー プロセス テンプレートを使用して新しいワークフロー プロセスを作成します。</span><span class="sxs-lookup"><span data-stu-id="67840-113">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="67840-114">**アカウント エンティティで仕入先を作成**ワークフロー プロセス テンプレートを使用して、**仕入先**エンティティの新しいワークフロー プロセスを作成し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="67840-114">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="67840-115">このワークフローでは、**アカウント** エンティティの仕入先作成シナリオを処理します。</span><span class="sxs-lookup"><span data-stu-id="67840-115">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="67840-116">![アカウント エンティティの仕入先の作成](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="67840-116">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="67840-117">**アカウント エンティティの更新**ワークフロー プロセス テンプレートを使用して、**仕入先**エンティティの新しいワークフロー プロセスを作成し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="67840-117">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="67840-118">このワークフローでは、**アカウント** エンティティの仕入先更新シナリオを処理します。</span><span class="sxs-lookup"><span data-stu-id="67840-118">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="67840-119">![アカウント エンティティの更新](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="67840-119">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="67840-120">**アカウント** エンティティで作成されたテンプレートから新しいワークフロー プロセスを作成します。</span><span class="sxs-lookup"><span data-stu-id="67840-120">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="67840-121">![仕入先エンティティで仕入先を作成](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="67840-121">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="67840-122">![仕入先エンティティの更新](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="67840-122">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="67840-123">ワークフローは、必要に応じてリアルタイムまたはバックグラウンドのワークフローとして構成できます。</span><span class="sxs-lookup"><span data-stu-id="67840-123">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="67840-124">![バックグラウンド ワークフローへの変換](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="67840-124">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="67840-125">**アカウント** エンティティと**仕入先**エンティティで作成したワークフローを有効にして、仕入先情報を保管するために**アカウント** エンティティの使用を開始します。</span><span class="sxs-lookup"><span data-stu-id="67840-125">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the **Account** entity for storing vendor information.</span></span> 
 
