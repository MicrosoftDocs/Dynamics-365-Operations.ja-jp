---
title: V2 データ エンティティを通じて入荷 ASN をインポートする
description: このトピックでは、受信 ASN V2 データ エンティティを通じて受信事前出荷明細通知 (ASN) のインポートを管理する方法について説明します。
author: GalynaFedorova
ms.date: 05/31/2021
ms.topic: article
ms.search.form: WHSInboundASNV2Entity, WHSInboundASNEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 470cc0c39f211a5d0f106c4c6e193867388e2b53
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249129"
---
# <a name="import-inbound-asns-through-the-v2-data-entity"></a><span data-ttu-id="59dea-103">V2 データ エンティティを通じて入荷 ASN をインポートする</span><span class="sxs-lookup"><span data-stu-id="59dea-103">Import inbound ASNs through the V2 data entity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="59dea-104">事前出荷明細通知 (ASN) は、仕入先の配送に関する通知を通知します。</span><span class="sxs-lookup"><span data-stu-id="59dea-104">Advanced shipping notices (ASNs) notify you about vendor deliveries.</span></span> <span data-ttu-id="59dea-105">送信者が出荷内容および品目や梱包などの追加情報を説明するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="59dea-105">They help the sender describe the contents of a shipment and additional information about it, such as the items and packaging.</span></span>

<span data-ttu-id="59dea-106">ASN は、倉庫作業員が何がいつ到着するかを知るのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="59dea-106">ASNs can help warehouse workers learn what is arriving when.</span></span> <span data-ttu-id="59dea-107">そのため、準備をすることができます。</span><span class="sxs-lookup"><span data-stu-id="59dea-107">Therefore, they can prepare.</span></span> <span data-ttu-id="59dea-108">さらに、倉庫作業者は ASN を使用して、以前に作成された関連する発注書と出荷の詳細を一致させることができます。</span><span class="sxs-lookup"><span data-stu-id="59dea-108">In addition, warehouse workers can use ASNs to match the details of a shipment to the related purchase order that was previously created.</span></span>

<span data-ttu-id="59dea-109">このトピックでは、ASN ファイルの操作方法を例を挙げて示すシナリオをまとめて紹介します。</span><span class="sxs-lookup"><span data-stu-id="59dea-109">This topic presents a collection of scenarios that show, through examples, how to work with ASN files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="59dea-110">*受信 ASN* のインポートは、高度な倉庫管理 (WMS) に対して有効な品目にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="59dea-110">*Inbound ASN* import applies only to items that are enabled for advanced warehouse management (WMS).</span></span> <span data-ttu-id="59dea-111">ASN を受け取る前に、ASN を送信する仕入先に対して発注書をシステムに登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59dea-111">Before you receive an ASN, a purchase order must be registered in the system against the vendor who is sending that ASN.</span></span>

## <a name="inbound-asn-v2-entity"></a><span data-ttu-id="59dea-112">受信 ASN V2 エンティティ</span><span class="sxs-lookup"><span data-stu-id="59dea-112">Inbound ASN V2 entity</span></span>

<span data-ttu-id="59dea-113">*受信 ASN V2* 複合データ エンティティを使用して、受信 ASN をインポートします。</span><span class="sxs-lookup"><span data-stu-id="59dea-113">You import inbound ASNs by using the *Inbound ASN V2* composite data entity.</span></span> <span data-ttu-id="59dea-114">*受信 ASN V2* は、次のエンティティを利用します。</span><span class="sxs-lookup"><span data-stu-id="59dea-114">*Inbound ASN V2* takes advantage of the following entities:</span></span>

- <span data-ttu-id="59dea-115">入庫積荷ヘッダー</span><span class="sxs-lookup"><span data-stu-id="59dea-115">Inbound load header</span></span>
- <span data-ttu-id="59dea-116">入荷ヘッダー</span><span class="sxs-lookup"><span data-stu-id="59dea-116">Inbound shipment header</span></span>
- <span data-ttu-id="59dea-117">入庫積荷梱包構造</span><span class="sxs-lookup"><span data-stu-id="59dea-117">Inbound load packing structures</span></span>
- <span data-ttu-id="59dea-118">入庫積荷梱包構造のケース</span><span class="sxs-lookup"><span data-stu-id="59dea-118">Inbound load packing structure cases</span></span>
- <span data-ttu-id="59dea-119">入庫積荷梱包構造のケース明細行</span><span class="sxs-lookup"><span data-stu-id="59dea-119">Inbound load packing structure case lines</span></span>
- <span data-ttu-id="59dea-120">入庫積荷梱包構造の明細行</span><span class="sxs-lookup"><span data-stu-id="59dea-120">Inbound load packing structure lines</span></span>

<span data-ttu-id="59dea-121">*受信 ASN V2* 複合データ エンティティは、XM Lファイル ベースのインポートが使用される非同期統合シナリオを目的としています。</span><span class="sxs-lookup"><span data-stu-id="59dea-121">The *Inbound ASN V2* composite data entity is intended for asynchronous integration scenarios where XML file–based imports are used.</span></span>

## <a name="xml-format-for-importing-asns"></a><span data-ttu-id="59dea-122">ASN をインポートする XM L形式</span><span class="sxs-lookup"><span data-stu-id="59dea-122">XML format for importing ASNs</span></span>

<span data-ttu-id="59dea-123">Microsoft Dynamics 365 Supply Chain Management は、ASN をインポートするために、次の XML 形式をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="59dea-123">Microsoft Dynamics 365 Supply Chain Management supports the following XML format for importing ASNs.</span></span> <span data-ttu-id="59dea-124">XML ファイル内の各ノードは、個々のエンティティからの属性を表しています。</span><span class="sxs-lookup"><span data-stu-id="59dea-124">Each node in the XML file represents an attribute from an individual entity.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV2Entity>
                    </WHSInboundPackingStructureCaseLineV2Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV2Entity>
                </WHSInboundLoadPackingStructureLineV2Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a><span data-ttu-id="59dea-125">例</span><span class="sxs-lookup"><span data-stu-id="59dea-125">Examples</span></span>

<span data-ttu-id="59dea-126">次のサブセクションでは、仕入先出荷の ASN XML インポート ファイルの例を示します。</span><span class="sxs-lookup"><span data-stu-id="59dea-126">The following subsections provide examples of ASN XML import files for vendor shipments.</span></span>

### <a name="example-1"></a><span data-ttu-id="59dea-127">例 1</span><span class="sxs-lookup"><span data-stu-id="59dea-127">Example 1</span></span>

<span data-ttu-id="59dea-128">次の例は、ケースの詳細が含められていない場合に、1 つの発注書に対する仕入先出荷をインポートする XML ファイルを示しています。</span><span class="sxs-lookup"><span data-stu-id="59dea-128">The following example shows an XML file for importing vendor shipments for one purchase order when no case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a><span data-ttu-id="59dea-129">例 2</span><span class="sxs-lookup"><span data-stu-id="59dea-129">Example 2</span></span>

<span data-ttu-id="59dea-130">次の例は、ケースの詳細を含む場合に、1 つの発注書に対する仕入先出荷をインポートする XML ファイルを示しています。</span><span class="sxs-lookup"><span data-stu-id="59dea-130">The following example shows an XML file for importing vendor shipments for one purchase order when case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a><span data-ttu-id="59dea-131">例 3</span><span class="sxs-lookup"><span data-stu-id="59dea-131">Example 3</span></span>

<span data-ttu-id="59dea-132">次の例は、ケースの詳細を含む場合に、複数の発注書に対する仕入先出荷をインポートする XML ファイルを示しています。</span><span class="sxs-lookup"><span data-stu-id="59dea-132">The following example shows an XML file for importing vendor shipments for multiple purchase orders when case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a><span data-ttu-id="59dea-133">ASN ファイルのインポート結果の検査</span><span class="sxs-lookup"><span data-stu-id="59dea-133">Inspect the results of importing an ASN file</span></span>

<span data-ttu-id="59dea-134">以下の手順に従って、ASN ファイルのインポート結果を検査します。</span><span class="sxs-lookup"><span data-stu-id="59dea-134">Follow these steps to inspect the results of importing an ASN file.</span></span>

1. <span data-ttu-id="59dea-135">**倉庫管理 \> 積荷 \> すべての積荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="59dea-135">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="59dea-136">ASN インポートの一部として作成された積荷を検索して開きます。</span><span class="sxs-lookup"><span data-stu-id="59dea-136">Find and open a load that was created as part of an ASN import.</span></span>
1. <span data-ttu-id="59dea-137">**積荷** クイックタブで、XML ファイルに基づく値を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59dea-137">On the **Load** FastTab, you should see values that are based on the XML file.</span></span>
1. <span data-ttu-id="59dea-138">XML ファイルに基づき、**積荷明細行** クイックタブに発注書番号と品目の詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="59dea-138">On the **Load lines** FastTab, you should see purchase order numbers and item details that are based on the XML file.</span></span>
1. <span data-ttu-id="59dea-139">アクション ウィンドウ内の **出荷と入荷** タブの **受取** グループで **梱包構造** を選択して、積荷の梱包構造を確認します。</span><span class="sxs-lookup"><span data-stu-id="59dea-139">On the Action Pane, on the **Ship and receive** tab, in the **Receive** group, select **Packing structure** to review the packing structure of the load.</span></span>
1. <span data-ttu-id="59dea-140">**パレット** クイックタブで、XML ファイルに基づくライセンス プレートを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59dea-140">On the **Pallets** FastTab, you should see license plates that are based on the XML file.</span></span>
1. <span data-ttu-id="59dea-141">**ケース** クイックタブで、XML ファイルに基づくケースを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59dea-141">On the **Cases** FastTab, you should see cases that are based on the XML file.</span></span>
1. <span data-ttu-id="59dea-142">**品目** クイックタブで、XML ファイルに基づく品目と数量を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59dea-142">On the **Items** FastTab, you should see items and quantities that are based on the XML file.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
