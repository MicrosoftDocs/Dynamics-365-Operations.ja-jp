---
title: "法人間でのネットワーク プリンターへのアクセスの管理"
description: "このトピックでは、新しいシステム管理ユーティリティを使用してネットワーク プリンターを設定する方法に関する情報が提供されます。"
author: tjvass
manager: AnnBe
ms.date: 12/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 62333
ms.assetid: 6135bcf7-bf8f-42ae-b2c6-458f6538e6a4
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-12-04
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 18eaadf417ce6d0aacf0b13b3e4f857e06031e66
ms.openlocfilehash: 37a538b9453c05ba7288f789fa208bfcabc36d7a
ms.contentlocale: ja-jp
ms.lasthandoff: 01/22/2019

---

# <a name="manage-access-to-network-printers-across-legal-entities"></a><span data-ttu-id="2b06e-103">法人間でのネットワーク プリンターへのアクセスの管理</span><span class="sxs-lookup"><span data-stu-id="2b06e-103">Manage access to network printers across legal entities</span></span>

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="2b06e-104">新しいシステム管理ユーティリティへのアクセスは、Carbon Flighting Service によって管理されます。</span><span class="sxs-lookup"><span data-stu-id="2b06e-104">Access to the new System administration utility is managed by the Carbon Flighting Service.</span></span> <span data-ttu-id="2b06e-105">Microsoft Dynamics 365 for Finance and Operations プラットフォーム更新 23 (2018 年 12 月) には、システム管理者用の **システム ネットワーク プリンター管理** ページが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2b06e-105">Microsoft Dynamics 365 for Finance and Operations platform update 23 (December 2018) includes the **System network printers management** page for system admins.</span></span>

<span data-ttu-id="2b06e-106">ドメイン管理者は、ドキュメント回覧エージェント (DRA) を使用して、Microsoft Dynamics 365 for Finance and Operations サービスにネットワーク プリンターを登録します。</span><span class="sxs-lookup"><span data-stu-id="2b06e-106">Domain admins register network printers with the Microsoft Dynamics 365 for Finance and Operations service by using the Document Routing Agent (DRA).</span></span> <span data-ttu-id="2b06e-107">プリンターが登録されると、組織管理者がユーザーに利用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="2b06e-107">After the printers are registered, the organization admin is responsible for making them available to users.</span></span> <span data-ttu-id="2b06e-108">設定は **ネットワーク プリンターの管理**ページで管理されます (**組織管理** \> **設定** \> **ネットワーク プリンター**)。</span><span class="sxs-lookup"><span data-stu-id="2b06e-108">The settings are managed on the **Manage network printers** page (**Organization administration** \> **Setup** \> **Network printers**).</span></span>

<span data-ttu-id="2b06e-109">**ネットワーク プリンターの管理** ページの設定は、組織の管理者用であるため、データは有効な法人に限定されます。</span><span class="sxs-lookup"><span data-stu-id="2b06e-109">Because the settings on the **Manage network printers** page are intended for organization admins, the data is limited to the active legal entity.</span></span> <span data-ttu-id="2b06e-110">システム管理者は、法人間でネットワーク プリンターの設定を管理することはできないので、場合によっては、ネットワーク プリンターの変更が発生したときなど、法人間での設定の更新が困難です。</span><span class="sxs-lookup"><span data-stu-id="2b06e-110">Because system admins can't manage network printer settings across legal entities, it can be difficult to update settings across legal entities in some situations, such as when network printer changes occur.</span></span> <span data-ttu-id="2b06e-111">たとえば、ネットワーク プリンター パスが更新されたときやハードウェアを交換したとき、またはユーザーがプリンター キュー内のすべてのドキュメントを削除しようとしたときに、ネットワーク プリンター インスタンスが削除されます。</span><span class="sxs-lookup"><span data-stu-id="2b06e-111">For example, a network printer instance is deleted when a network printer path is updated or hardware is replaced, or someone tries to purge all documents in the printer queue.</span></span>

<span data-ttu-id="2b06e-112">システム管理ユーティリティは、誤った印刷手順の復旧ツールです。</span><span class="sxs-lookup"><span data-stu-id="2b06e-112">The System administration utility is a recovery tool for inadvertent print instructions.</span></span> <span data-ttu-id="2b06e-113">また、特定の法人からのアクセスなど、ネットワーク プリンター設定の管理のタスクが簡単になります。</span><span class="sxs-lookup"><span data-stu-id="2b06e-113">It also simplifies the task of managing network printer settings, such as access from specific legal entities.</span></span>

## <a name="access-the-feature"></a><span data-ttu-id="2b06e-114">機能にアクセスする</span><span class="sxs-lookup"><span data-stu-id="2b06e-114">Access the feature</span></span>
<span data-ttu-id="2b06e-115">機能がオンになると、**ネットワーク プリンターの管理** ページのアクション ウィンドウの **オプション** タブに **プレビュー** グループが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2b06e-115">After the feature has been turned on, a **Preview** group will appear on the **Options** tab of the Action Pane on the **Manage network printers** page.</span></span>

![アクション ペインのプレビュー グループ](./media/network-printer-01.png)

1. <span data-ttu-id="2b06e-117">**組織管理** > **設定** > **ネットワーク プリンター**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="2b06e-117">Select **Organization administration** > **Setup** > **Network printers**.</span></span>
2. <span data-ttu-id="2b06e-118">アクション ウィンドウの **プレビュー** グループで、**システム ネットワーク プリンター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2b06e-118">On the Action Pane, in the **Preview** group, select **System network printers**.</span></span>
3. <span data-ttu-id="2b06e-119">**システム ネットワーク プリンター** ページで、DRA を使用してサービスにネットワーク プリンターを登録します。</span><span class="sxs-lookup"><span data-stu-id="2b06e-119">On the **System network printers** page, register the network printers with the service by using the DRA.</span></span> <span data-ttu-id="2b06e-120">組織の各法人のコンフィギュレーション情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2b06e-120">You will see the configuration information for each legal entity in the organization.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="2b06e-121">サポートされている操作</span><span class="sxs-lookup"><span data-stu-id="2b06e-121">Supported operations</span></span>
<span data-ttu-id="2b06e-122">現時点では、システム管理ユーティリティでは削除工程のみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="2b06e-122">Currently, the System administration utility supports only Delete operations.</span></span> <span data-ttu-id="2b06e-123">**システム ネットワーク プリンター** ページを使用してネットワーク プリンターを削除した場合の結果を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="2b06e-123">Here are the results if you delete network printers by using the **System network printers** page:</span></span>

- <span data-ttu-id="2b06e-124">プリンターで指示されたプリンター キュー内のすべてのドキュメントが削除されます。</span><span class="sxs-lookup"><span data-stu-id="2b06e-124">All documents in the printer queue that are directed at the printer are deleted.</span></span>
- <span data-ttu-id="2b06e-125">組織内のすべての法人のネットワーク プリンターが削除されます。</span><span class="sxs-lookup"><span data-stu-id="2b06e-125">The network printer is deleted for all legal entities in the organization.</span></span>
- <span data-ttu-id="2b06e-126">ドメイン管理者は、古いプリンター名を使用してデバイスを登録することができます。</span><span class="sxs-lookup"><span data-stu-id="2b06e-126">Domain admins can register devices by using the old printer name.</span></span>
- <span data-ttu-id="2b06e-127">組織管理者、引き続き既存のツールを使用して、1 つの法人のネットワーク プリンターの設定を管理できます。</span><span class="sxs-lookup"><span data-stu-id="2b06e-127">The organization admins can continue to use the existing tools to manage network printer settings for a single legal entity.</span></span>

