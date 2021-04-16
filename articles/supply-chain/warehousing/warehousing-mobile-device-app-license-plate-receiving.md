---
title: 倉庫管理モバイル アプリで受信するライセンス プレート
description: このトピックでは、現物在庫を受け取るためにライセンス プレート入庫プロセスの使用をサポートするように倉庫管理モバイル アプリを設定する方法について説明します。
author: perlynne
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSParameters, WHSRFMenuItem, WHSLicensePlate, WHSPackingStructure
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 8c662da296bea7def443cb166bd3f7e501c9abcc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823194"
---
# <a name="license-plate-receiving-via-the-warehouse-management-mobile-app"></a><span data-ttu-id="54199-103">倉庫管理モバイル アプリで受信するライセンス プレート</span><span class="sxs-lookup"><span data-stu-id="54199-103">License plate receiving via the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54199-104">このトピックでは、現物在庫の受け取りにライセンス プレート入庫プロセスを使用できるように倉庫管理モバイル アプリを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="54199-104">This topic explains how to set up the Warehouse Management mobile app so that it supports using a license plate receiving process to receive physical inventory.</span></span>

<span data-ttu-id="54199-105">この機能を使用すると、事前出荷明細通知 (ASN) に関連する入庫在庫の受け取りを簡単に記録できます。</span><span class="sxs-lookup"><span data-stu-id="54199-105">You can use this functionality to quickly record the receipt of inbound inventory that is related to an advance ship notice (ASN).</span></span> <span data-ttu-id="54199-106">倉庫管理プロセスを使用して移動オーダーを出荷すると、システムは ASN を自動的に作成します。</span><span class="sxs-lookup"><span data-stu-id="54199-106">The system automatically creates an ASN when warehouse management processes are used to ship a transfer order.</span></span> <span data-ttu-id="54199-107">発注書プロセスでは、ASN は手動で記録することも、入荷 ASN データ エンティティ プロセスを使用して自動的にインポートすることもできます。</span><span class="sxs-lookup"><span data-stu-id="54199-107">For the purchase order process, an ASN can be manually recorded, or it can be automatically imported by using an inbound ASN data entity process.</span></span>

<span data-ttu-id="54199-108">ASN データは、*梱包構造* を使用して、積荷と出荷にリンクされ、パレット (親のライセンス プレート) にはケース (入れ子になったライセンス プレート) を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="54199-108">The ASN data is linked to loads and shipments via the *packing structures*, where pallets (parent license plates) can contain cases (nested license plates).</span></span>

> [!NOTE]
> <span data-ttu-id="54199-109">入れ子になったライセンス プレートを持つ梱包構造を使用する場合、在庫トランザクションの数を減らすには、システムによって親ライセンス プレート上の現物手持在庫が記録されます。</span><span class="sxs-lookup"><span data-stu-id="54199-109">To reduce the number of inventory transactions when packing structures that have nested license plates are used, the system records the physical on-hand inventory on the parent license plate.</span></span> <span data-ttu-id="54199-110">梱包構造データに基づいて、親ライセンス プレートから入れ子になったライセンス プレートに現物手持在庫を移動するには、モバイル デバイスはで、*入れ子になったライセンス プレートに梱包* 作業作成プロセスに基づくメニュー項目を用意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54199-110">To trigger the movement of the physical on-hand inventory from the parent license plate to the nested license plates, based on the packing structure data, the mobile device must provide a menu item that is based on the *Pack to nested license plates* work creation process.</span></span>

## <a name="warehousing-mobile-device-app-processing"></a><span data-ttu-id="54199-111">倉庫管理モバイル デバイス アプリの処理</span><span class="sxs-lookup"><span data-stu-id="54199-111">Warehousing mobile device app processing</span></span>

<span data-ttu-id="54199-112">作業者が着信したライセンス プレート ID をスキャンすると、ライセンス プレートの入荷プロセスが初期化されます。</span><span class="sxs-lookup"><span data-stu-id="54199-112">When a worker scans an incoming license plate ID, the system initializes a license plate receiving process.</span></span> <span data-ttu-id="54199-113">この情報に基づいて、ライセンス プレート (ASNから送られるデータ) の内容が入庫ドック場所に物理的に登録されます。</span><span class="sxs-lookup"><span data-stu-id="54199-113">Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location.</span></span> <span data-ttu-id="54199-114">この次となるフローは、業務プロセスのニーズによって異なります。</span><span class="sxs-lookup"><span data-stu-id="54199-114">The flows that follow will depend your business process needs.</span></span>

## <a name="work-policies"></a><span data-ttu-id="54199-115">作業ポリシー</span><span class="sxs-lookup"><span data-stu-id="54199-115">Work policies</span></span>

<span data-ttu-id="54199-116">(たとえば) *完了レポート* モバイル デバイス メニュー項目プロセスがおこなわれると、そのライセンス プレートの入荷プロセスは、定義された設定に基づいて複数のワークフローをサポートします。</span><span class="sxs-lookup"><span data-stu-id="54199-116">As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.</span></span>

### <a name="work-policies-with-work-creation"></a><span data-ttu-id="54199-117">作業作成での作業ポリシー</span><span class="sxs-lookup"><span data-stu-id="54199-117">Work policies with work creation</span></span>

<span data-ttu-id="54199-118">作業を作成する作業ポリシーを使用して入庫品目を登録する場合、システムは登録ごとに、プット アウェイ作業 レコードを生成し、保存します。</span><span class="sxs-lookup"><span data-stu-id="54199-118">When you register incoming items using a work policy that creates work, the system generates and saves put-away work records for each registration.</span></span> <span data-ttu-id="54199-119">*ライセンス プレートの入荷とプットアウェイ* 作業プロセスを使用する場合、登録とプット アウェイは 1 つのモバイル デバイス メニュー項目を使用して 1 つの操作として処理されます。</span><span class="sxs-lookup"><span data-stu-id="54199-119">If you use the *License plate receiving and put away* work process, then registration and put away are handled as a single operation using a single mobile device menu item.</span></span> <span data-ttu-id="54199-120">*ライセンス プレート入荷* プロセスを使用する場合は、入荷プロセスとプット アウェイ プロセスが 2 つの異なる倉庫操作として処理され、それぞれに独自のモバイル デバイス メニュー項目を持ちます。</span><span class="sxs-lookup"><span data-stu-id="54199-120">If you use the *License plate receiving* process, then the receiving and put-away processes are handled as two different warehouse operations, each with their own mobile device menu item.</span></span>

### <a name="work-policies-without-work-creation"></a><span data-ttu-id="54199-121">作業作成なしの作業ポリシー</span><span class="sxs-lookup"><span data-stu-id="54199-121">Work policies without work creation</span></span>

<span data-ttu-id="54199-122">ライセンス プレート入荷プロセスを、作業を作成せずに使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="54199-122">You can use the license plate receiving process without creating work.</span></span> <span data-ttu-id="54199-123">*移動入庫* や *発注書* の作業指示書タイプを持つ作業ポリシーを定義し、*ライセンス プレートの入荷 (およびプットアウェイ)* のプロセスを使用する場合、次の 2 つの倉庫管理モバイル アプリ プロセスは作業を作成しません。</span><span class="sxs-lookup"><span data-stu-id="54199-123">If you define work policies that have a work order type of *Transfer receipt* and/or *Purchase orders*, and you use the process for *License plate receiving (and put away)*, the following two Warehousing mobile app processes won't create work.</span></span> <span data-ttu-id="54199-124">代わりに、入庫の入荷ドックでライセンス プレートに入庫の現物在庫の登録だけをおこないます。</span><span class="sxs-lookup"><span data-stu-id="54199-124">Instead, they will just register the inbound physical inventory on the license plate at the inbound receiving dock.</span></span>

- <span data-ttu-id="54199-125">*ライセンス プレート受取*</span><span class="sxs-lookup"><span data-stu-id="54199-125">*License plate receiving*</span></span>
- <span data-ttu-id="54199-126">*ライセンス プレートの受け取りおよびプット アウェイ*</span><span class="sxs-lookup"><span data-stu-id="54199-126">*License plate receiving and put away*</span></span>

> [!NOTE]
> - <span data-ttu-id="54199-127">**在庫場所** セクションで、作業ポリシーに対して少なくとも 1 つの場所を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54199-127">You must define at least one location for a work policy in the **Inventory locations** section.</span></span> <span data-ttu-id="54199-128">複数の作業ポリシーに同じ場所を指定することはできません。</span><span class="sxs-lookup"><span data-stu-id="54199-128">You can't specify the same location for multiple work policies.</span></span>
> - <span data-ttu-id="54199-129">倉庫管理モバイル デバイス メニュー項目の **印刷ラベル** オプションは、作業の作成なしではライセンス プレートのラベルを印刷しません。</span><span class="sxs-lookup"><span data-stu-id="54199-129">The **Print label** option for Warehousing mobile device menu items won't print a license plate label without work creation.</span></span>

<span data-ttu-id="54199-130">この機能をシステムで使用できるようにするには、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) で  *ライセンス プレート入荷の拡張設定* 機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="54199-130">To make this functionality available on your system, you must turn on the *License plate receiving enhancements* feature in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

### <a name="receive-inventory-on-a-location-that-doesnt-track-license-plates"></a><span data-ttu-id="54199-131">ライセンス プレートを追跡しない場所での在庫の入荷</span><span class="sxs-lookup"><span data-stu-id="54199-131">Receive inventory on a location that doesn't track license plates</span></span>

<span data-ttu-id="54199-132">**ライセンス プレートの追跡を使用する** が有効になっていない場合でも、その場所プロファイルに割り当てられている倉庫の場所を使用することは可能です。</span><span class="sxs-lookup"><span data-stu-id="54199-132">It's possible to use a warehouse location that is assigned to a location profile even when **Use license plate tracking** isn't turned on.</span></span> <span data-ttu-id="54199-133">したがって、在庫を入荷する際に、作業を作成せずに手持在庫を直接登録することができます。</span><span class="sxs-lookup"><span data-stu-id="54199-133">Therefore, when you receive inventory, you can directly register the on-hand inventory on a location without work creation.</span></span>

## <a name="add-mobile-device-menu-items-for-each-receiving-location-in-a-warehouse"></a><span data-ttu-id="54199-134">倉庫内の入荷場所ごとにモバイル デバイス メニュー項目を追加する</span><span class="sxs-lookup"><span data-stu-id="54199-134">Add mobile device menu items for each receiving location in a warehouse</span></span>

<span data-ttu-id="54199-135">*ライセンス プレートの入荷拡張設定* 機能を使うことで、場所特有のライセンス プレート入荷 (およびプットアウェイ) メニュー項目を倉庫管理モバイル アプリに追加して、倉庫の任意の場所での入荷ができるようになります。</span><span class="sxs-lookup"><span data-stu-id="54199-135">The *License plate receiving enhancements* feature lets you receive at any location in a warehouse by adding location-specific license plate receiving (and put away) menu items to the Warehousing mobile app.</span></span> <span data-ttu-id="54199-136">以前は、システムは各倉庫に対して定義されている既定の場所のみでの入荷しかサポートされていませんでした。</span><span class="sxs-lookup"><span data-stu-id="54199-136">Previously, the system supported receiving only at the default location that is defined for each warehouse.</span></span> <span data-ttu-id="54199-137">ただし、この機能を有効にすると、ライセンス プレートの入荷 (およびプットアウェイ) のモバイル デバイス メニュー項目では、各メニュー項目に対してカスタムの "移動先" 位置を選択できる、**既定のデータを使用** オプションが提供されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="54199-137">However, when this feature is turned on, mobile device menu items for license plate receiving (and put away) now provide the **Use default data** option, which lets you select a custom "to" location for each menu item.</span></span> <span data-ttu-id="54199-138">(このオプションは、その他のタイプのメニュー項目では使用可能です。)</span><span class="sxs-lookup"><span data-stu-id="54199-138">(This option was already available for some other types of menu items.)</span></span>

<span data-ttu-id="54199-139">この機能をシステムで使用できるようにするには、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) で  *ライセンス プレート入荷の拡張設定* 機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="54199-139">To make this functionality available on your system, you must turn on the *License plate receiving enhancements* feature in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="show-or-skip-the-receiving-summary-page"></a><span data-ttu-id="54199-140">入荷の概要ページを表示またはスキップする</span><span class="sxs-lookup"><span data-stu-id="54199-140">Show or skip the receiving summary page</span></span>

<span data-ttu-id="54199-141">*モバイル デバイスに入荷の概要ページを表示するかどうかを制御する* 機能を使用して、追加の詳細な倉庫アプリ フローを、ライセンス プレートの入庫プロセスの一部として利用できます。</span><span class="sxs-lookup"><span data-stu-id="54199-141">You can use the *Control whether to display a receiving summary page on mobile devices* feature to take advantage of an additional detailed Warehouse Management mobile app flow as part of the license plate receiving process.</span></span>

<span data-ttu-id="54199-142">この機能を有効にすると、ライセンス プレートの受け取り、またはライセンスプレートの受け取りとプット アウェイのモバイル デバイス メニュー項目で、**入荷の概要ページを表示** 設定が提供されます。</span><span class="sxs-lookup"><span data-stu-id="54199-142">When this feature is turned on, mobile device menu items for license plate receiving or license plate receiving and put-away will provide a **Display receiving summary page** setting.</span></span> <span data-ttu-id="54199-143">この設定には、次のオプションがあります:</span><span class="sxs-lookup"><span data-stu-id="54199-143">This setting has the following options:</span></span>

- <span data-ttu-id="54199-144">**詳細な概要の表示** – ライセンス プレートの受け取り中に、作業者は、完全な ASN 情報を示す追加のページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="54199-144">**Display a detailed summary** – During license plate receiving, workers will see an extra page that shows the full ASN information.</span></span>
- <span data-ttu-id="54199-145">**概要のスキップ** – 作業者は完全な ASN 情報を参照することはできません。</span><span class="sxs-lookup"><span data-stu-id="54199-145">**Skip the summary** – Workers won't see the full ASN information.</span></span> <span data-ttu-id="54199-146">倉庫作業者は、入庫プロセス中に廃棄コードを設定したり、例外を追加したりすることもできなくなります。</span><span class="sxs-lookup"><span data-stu-id="54199-146">Warehouse workers also won't be able to set a disposition code or add exceptions during the receiving process.</span></span>

<span data-ttu-id="54199-147">この機能をシステムで使用できるようにするには、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) で *モバイル デバイス上で入荷概要ページを表示するかどうかを制御する* をオンにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="54199-147">To make this functionality available on your system, you must turn on the *Control whether to display a receiving summary page on mobile devices* feature in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a><span data-ttu-id="54199-148">移動オーダー出荷済ライセンス プレートを出荷先倉庫以外の倉庫で使用されないようにする</span><span class="sxs-lookup"><span data-stu-id="54199-148">Prevent transfer order–shipped license plates from being used at warehouses other than the destination warehouse</span></span>

<span data-ttu-id="54199-149">既に存在するライセンス プレート ID が ASN に含まれ、ライセンス プレート登録が行われる倉庫の場所以外に現物手持在庫データがある場合、ライセンス プレートの入荷プロセスは使用できません。</span><span class="sxs-lookup"><span data-stu-id="54199-149">A license plate receiving process can't be used if an ASN contains a license plate ID that already exists and has physical on-hand data at a warehouse location other than the warehouse location where the license plate registration occurs.</span></span>

<span data-ttu-id="54199-150">流通倉庫がライセンス プレートを追跡しない (したがって、ライセンス プレートごとの現物手持在庫も追跡しない) 移動オーダーのシナリオの場合、*移動オーダー出荷済ライセンス プレートが出荷先倉庫以外の別の倉庫で使用されないようにする* 機能を使用して、輸送中のライセンス プレートを物理的に手動で更新することを防止できます。</span><span class="sxs-lookup"><span data-stu-id="54199-150">For transfer order scenarios where the transit warehouse doesn't track license plates (and therefore also doesn't track physical on-hand inventory per license plate), you can use the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature to prevent physical on-hand updates of license plates that are in transit.</span></span>

<span data-ttu-id="54199-151">この機能をシステムで使用できるようにするには、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) にある *移動オーダーで出荷されたライセンス プレートが、出荷先倉庫以外の倉庫で使用されないようにする* 機能をオンにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="54199-151">To make this functionality available on your system, you must turn on the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="54199-152">この機能が使用可能になったときに機能を管理するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="54199-152">To manage the functionality when this feature is available, follow these steps.</span></span>

1. <span data-ttu-id="54199-153">**倉庫管理 \> 設定 \> 倉庫管理パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="54199-153">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="54199-154">**一般** タブの **ライセンス プレート** クイックタブで、**流通倉庫ライセンス プレート ポリシー** フィールドを次のいずれかの値に設定します:</span><span class="sxs-lookup"><span data-stu-id="54199-154">On the **General** tab, on the **License plates** FastTab, set the **Transit warehouse license plate policy** field to one of the following values:</span></span>

    - <span data-ttu-id="54199-155">**追跡されていないライセンス プレート再利用の許可** – システムは、*移動オーダー出荷済ライセンス プレートを出荷先倉庫以外の倉庫で使用されないようにする* 機能が使用できない場合と同じように機能します。</span><span class="sxs-lookup"><span data-stu-id="54199-155">**Allow reuse of non-tracked license plate** – The system works the same way that it works when the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature isn't available.</span></span> <span data-ttu-id="54199-156">この値は、初めて機能をアクティブにしたときの既定の設定です。</span><span class="sxs-lookup"><span data-stu-id="54199-156">This value is the default setting when you first activate the feature.</span></span>
    - <span data-ttu-id="54199-157">**追跡されていないライセンス プレートの再利用防止** – 移動オーダーを受領するまで、出荷したライセンス プレートに関連する手動更新のみが出荷先倉庫で許可されます。</span><span class="sxs-lookup"><span data-stu-id="54199-157">**Prevent reuse of non-tracked license plate** – Only on-hand updates that are related to a shipped license plate will be allowed at the destination warehouse until the transfer order has been received.</span></span>

## <a name="more-information"></a><span data-ttu-id="54199-158">詳細</span><span class="sxs-lookup"><span data-stu-id="54199-158">More information</span></span>

<span data-ttu-id="54199-159">モバイル デバイス メニュー項目の詳細については、[倉庫作業用のモバイル デバイスの設定](configure-mobile-devices-warehouse.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54199-159">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

<span data-ttu-id="54199-160">*完了レポート* の製造シナリオに関する詳細情報は、[倉庫作業ポリシーの概要](warehouse-work-policies.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54199-160">For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).</span></span>

<span data-ttu-id="54199-161">入庫積荷管理に関する詳細情報については、[発注書に対する入庫積荷の倉庫処理](inbound-load-handling.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54199-161">For more information about inbound load management, see [Warehouse handling of inbound loads for purchase orders](inbound-load-handling.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]