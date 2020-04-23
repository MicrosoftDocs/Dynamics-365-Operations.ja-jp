---
title: Warehouse Mobile App 経由のライセンス プレート受け取り
description: このトピックでは、現物在庫を受け取るためにライセンス プレート入庫プロセスの使用をサポートするように Warehouse Mobile App を設定する方法について説明します。
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 98cd608edea1d5365d0d3532244f1fcdb6293d3c
ms.sourcegitcommit: 3a823444005d316bd95fc663e2dbc8252ac7d93a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261350"
---
# <a name="license-plate-receiving-via-the-warehousing-mobile-app"></a><span data-ttu-id="6de08-103">Warehouse Mobile App 経由のライセンス プレート受け取り</span><span class="sxs-lookup"><span data-stu-id="6de08-103">License plate receiving via the Warehousing mobile app</span></span>

<span data-ttu-id="6de08-104">このトピックでは、現物在庫の受け取りにライセンス プレート入庫プロセスを使用できるように Warehouse Mobile App を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6de08-104">This topic explains how to set up the Warehousing mobile app so that it supports using a license plate receiving process to receive physical inventory.</span></span>

<span data-ttu-id="6de08-105">この機能を使用すると、事前出荷明細通知 (ASN) に関連する入庫在庫の受け取りを簡単に記録できます。</span><span class="sxs-lookup"><span data-stu-id="6de08-105">You can use this functionality to quickly record the receipt of inbound inventory that is related to an advance ship notice (ASN).</span></span> <span data-ttu-id="6de08-106">倉庫管理プロセスを使用して移動オーダーを出荷すると、システムは ASN を自動的に作成します。</span><span class="sxs-lookup"><span data-stu-id="6de08-106">The system automatically creates an ASN when warehouse management processes are used to ship a transfer order.</span></span> <span data-ttu-id="6de08-107">発注書プロセスでは、ASN は手動で記録することも、入荷 ASN データ エンティティ プロセスを使用して自動的にインポートすることもできます。</span><span class="sxs-lookup"><span data-stu-id="6de08-107">For the purchase order process, an ASN can be manually recorded, or it can be automatically imported by using an inbound ASN data entity process.</span></span>

<span data-ttu-id="6de08-108">ASN データは、*梱包構造* を使用して、積荷と出荷にリンクされ、パレット (親のライセンス プレート) にはケース (入れ子になったライセンス プレート) を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="6de08-108">The ASN data is linked to loads and shipments via the *packing structures*, where pallets (parent license plates) can contain cases (nested license plates).</span></span>

> [!NOTE]
> <span data-ttu-id="6de08-109">入れ子になったライセンス プレートを持つ梱包構造を使用する場合、在庫トランザクションの数を減らすには、システムによって親ライセンス プレート上の現物手持在庫が記録されます。</span><span class="sxs-lookup"><span data-stu-id="6de08-109">To reduce the number of inventory transactions when packing structures that have nested license plates are used, the system records the physical on-hand inventory on the parent license plate.</span></span> <span data-ttu-id="6de08-110">梱包構造データに基づいて、親ライセンス プレートから入れ子になったライセンス プレートに現物手持在庫を移動するには、モバイル デバイスはで、*入れ子になったライセンス プレートに梱包* 作業作成プロセスに基づくメニュー項目を用意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6de08-110">To trigger the movement of the physical on-hand inventory from the parent license plate to the nested license plates, based on the packing structure data, the mobile device must provide a menu item that is based on the *Pack to nested license plates* work creation process.</span></span>

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a><span data-ttu-id="6de08-111">入荷の概要ページを表示またはスキップする</span><span class="sxs-lookup"><span data-stu-id="6de08-111">Show or skip the receiving summary page</span></span>

<span data-ttu-id="6de08-112">*モバイル デバイスに入荷の概要ページを表示するかどうかを制御する* 機能を使用して、追加の詳細な倉庫アプリ フローを、ライセンス プレートの入庫プロセスの一部として利用できます。</span><span class="sxs-lookup"><span data-stu-id="6de08-112">You can use the *Control whether to display a receiving summary page on mobile devices* feature to take advantage of an additional detailed Warehouse app flow as part of the license plate receiving process.</span></span>

<span data-ttu-id="6de08-113">この機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6de08-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="6de08-114">管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して、機能の状態を確認し、有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="6de08-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="6de08-115">**機能管理** ワークスペースで、この機能は次のようにリストされています:</span><span class="sxs-lookup"><span data-stu-id="6de08-115">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="6de08-116">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="6de08-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="6de08-117">**機能名:** *モバイル デバイスに入荷の概要ページを表示するかどうかを制御する*</span><span class="sxs-lookup"><span data-stu-id="6de08-117">**Feature name:** *Control whether to display a receiving summary page on mobile devices*</span></span>

<span data-ttu-id="6de08-118">この機能を有効にすると、ライセンス プレートの受け取り、またはライセンスプレートの受け取りとプット アウェイのモバイル デバイス メニュー項目で、**入荷の概要ページを表示** 設定が提供されます。</span><span class="sxs-lookup"><span data-stu-id="6de08-118">When this feature is turned on, mobile device menu items for license plate receiving or license plate receiving and put-away will provide a **Display receiving summary page** setting.</span></span> <span data-ttu-id="6de08-119">この設定には、次のオプションがあります:</span><span class="sxs-lookup"><span data-stu-id="6de08-119">This setting has the following options:</span></span>

- <span data-ttu-id="6de08-120">**詳細な概要の表示** – ライセンス プレートの受け取り中に、作業者は、完全な ASN 情報を示す追加のページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6de08-120">**Display a detailed summary** – During license plate receiving, workers will see an extra page that shows the full ASN information.</span></span>
- <span data-ttu-id="6de08-121">**概要のスキップ** – 作業者は完全な ASN 情報を参照することはできません。</span><span class="sxs-lookup"><span data-stu-id="6de08-121">**Skip the summary** – Workers won't see the full ASN information.</span></span> <span data-ttu-id="6de08-122">倉庫作業者は、入庫プロセス中に廃棄コードを設定したり、例外を追加したりすることもできなくなります。</span><span class="sxs-lookup"><span data-stu-id="6de08-122">Warehouse workers also won't be able to set a disposition code or add exceptions during the receiving process.</span></span>

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a><span data-ttu-id="6de08-123">移動オーダー出荷済ライセンス プレートを出荷先倉庫以外の倉庫で使用されないようにする</span><span class="sxs-lookup"><span data-stu-id="6de08-123">Prevent transfer order–shipped license plates from being used at warehouses other than the destination warehouse</span></span>

<span data-ttu-id="6de08-124">既に存在するライセンス プレート ID が ASN に含まれ、ライセンス プレート登録が行われている倉庫の場所以外の倉庫の場所に現物手持在庫データがある場合、ライセンス プレートの入庫プロセスは使用できません。</span><span class="sxs-lookup"><span data-stu-id="6de08-124">A license plate receiving process can't be used if an ASN contains a license plate ID that already exists and has physical on-hand data at a warehouse location other than the warehouse location where the license plate registration is occurring.</span></span>

<span data-ttu-id="6de08-125">流通倉庫がライセンス プレートを追跡しない (したがって、ライセンス プレートごとの現物手持在庫も追跡しない) 移動オーダーのシナリオの場合、*移動オーダー出荷済ライセンス プレートが出荷先倉庫以外の別の倉庫で使用されないようにする* 機能を使用して、輸送中のライセンス プレートを物理的に手動で更新することを防止できます。</span><span class="sxs-lookup"><span data-stu-id="6de08-125">For transfer order scenarios where the transit warehouse doesn't track license plates (and therefore also doesn't track physical on-hand inventory per license plate), you can use the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature to prevent physical on-hand updates of license plates that are in transit.</span></span>

<span data-ttu-id="6de08-126">この機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6de08-126">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="6de08-127">管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して、機能の状態を確認し、有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="6de08-127">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="6de08-128">**機能管理** ワークスペースで、この機能は次のようにリストされています:</span><span class="sxs-lookup"><span data-stu-id="6de08-128">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="6de08-129">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="6de08-129">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="6de08-130">**機能名:** *移動オーダー出荷済ライセンス プレートを出荷先倉庫以外の倉庫で使用されないようにする*</span><span class="sxs-lookup"><span data-stu-id="6de08-130">**Feature name:** *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse*</span></span>

<span data-ttu-id="6de08-131">この機能が使用可能になったときに機能を管理するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6de08-131">To manage the functionality when this feature is available, follow these steps.</span></span>

1. <span data-ttu-id="6de08-132">**倉庫管理 \> 設定 \> 倉庫管理パラメーター**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6de08-132">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="6de08-133">**一般** タブの **ライセンス プレート** クイックタブで、**流通倉庫ライセンス プレート ポリシー** フィールドを次のいずれかの値に設定します:</span><span class="sxs-lookup"><span data-stu-id="6de08-133">On the **General** tab, on the **License plates** FastTab, set the **Transit warehouse license plate policy** field to one of the following values:</span></span>

    - <span data-ttu-id="6de08-134">**追跡されていないライセンス プレート再利用の許可** – システムは、*移動オーダー出荷済ライセンス プレートを出荷先倉庫以外の倉庫で使用されないようにする* 機能が使用できない場合と同じように機能します。</span><span class="sxs-lookup"><span data-stu-id="6de08-134">**Allow reuse of non-tracked license plate** – The system works the same way that it works when the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature isn't available.</span></span> <span data-ttu-id="6de08-135">この値は、初めて機能をアクティブにしたときの既定の設定です。</span><span class="sxs-lookup"><span data-stu-id="6de08-135">This value is the default setting when you first activate the feature.</span></span>
    - <span data-ttu-id="6de08-136">**追跡されていないライセンス プレートの再利用防止** – 移動オーダーを受領するまで、出荷したライセンス プレートに関連する手動更新のみが出荷先倉庫で許可されます。</span><span class="sxs-lookup"><span data-stu-id="6de08-136">**Prevent reuse of non-tracked license plate** – Only on-hand updates that are related to a shipped license plate will be allowed at the destination warehouse until the transfer order has been received.</span></span>

## <a name="more-information"></a><span data-ttu-id="6de08-137">詳細</span><span class="sxs-lookup"><span data-stu-id="6de08-137">More information</span></span>

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

<span data-ttu-id="6de08-138">モバイル デバイス メニュー項目の詳細については、[倉庫作業用のモバイル デバイスの設定](configure-mobile-devices-warehouse.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6de08-138">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>
