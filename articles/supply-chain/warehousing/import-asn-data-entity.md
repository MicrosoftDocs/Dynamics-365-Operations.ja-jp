---
title: V3 データ エンティティを通じて受信 ASN をインポートする
description: この記事では、受信 ASN データ エンティティを通じて受信事前出荷明細通知 (ASN) のインポートを管理する方法について説明します。
author: GalynaFedorova
ms.date: 05/11/2022
ms.topic: article
ms.search.form: WHSInboundASNV3Entity, WHSInboundASNEntity, DMFEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0ac45e070d0473547c48da1380377de3d4bf60bd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907119"
---
# <a name="import-inbound-asns-through-the-v3-data-entity"></a>V3 データ エンティティを通じて受信 ASN をインポートする

[!include [banner](../../includes/banner.md)]

事前出荷明細通知 (ASN) は、仕入先の配送に関する通知を通知します。 送信者が出荷内容および品目や梱包などの追加情報を説明するのに役立ちます。

ASN は、倉庫作業員が何がいつ到着するかを知るのに役立ちます。 そのため、準備をすることができます。 さらに、倉庫作業者は ASN を使用して、以前に作成された関連する発注書と出荷の詳細を一致させることができます。

この記事では、ASN ファイルの操作方法を例を挙げて示すシナリオをまとめて紹介します。

> [!IMPORTANT]
> *受信 ASN* のインポートは、高度な倉庫管理 (WMS) に対して有効な品目にのみ適用されます。 ASN を受け取る前に、ASN を送信する仕入先に対して発注書をシステムに登録する必要があります。

## <a name="inbound-asn-v3-entity"></a>受信 ASN V3 エンティティ

*受信 ASN V3* 複合データ エンティティを使用して、受信 ASN をインポートします。 *受信 ASN V3* は、次のエンティティを利用します。

- 入庫積荷ヘッダー
- 入荷ヘッダー
- 入庫積荷梱包構造
- 入庫積荷梱包構造のケース
- 入庫積荷梱包構造のケース明細行
- 入庫積荷梱包構造の明細行

*受信 ASN V3* 複合データ エンティティは、XML ファイル ベースのインポートが使用される非同期統合シナリオを目的としています。

## <a name="xml-format-for-importing-asns"></a>ASN をインポートする XM L形式

Microsoft Dynamics 365 Supply Chain Management は、ASN をインポートするために、次の XML 形式をサポートしています。 XML ファイル内の各ノードは、個々のエンティティからの属性を表しています。

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV3Entity>
                    </WHSInboundPackingStructureCaseLineV3Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV3Entity>
                </WHSInboundLoadPackingStructureLineV3Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a>例

次のサブセクションでは、仕入先出荷の ASN XML インポート ファイルの例を示します。

### <a name="example-1"></a>例 1

次の例は、ケースの詳細が含められていない場合に、1 つの発注書に対する仕入先出荷をインポートする XML ファイルを示しています。

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a>例 2

次の例は、ケースの詳細を含む場合に、1 つの発注書に対する仕入先出荷をインポートする XML ファイルを示しています。

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLine3Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a>例 3

次の例は、ケースの詳細を含む場合に、複数の発注書に対する仕入先出荷をインポートする XML ファイルを示しています。

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a>ASN ファイルのインポート結果の検査

以下の手順に従って、ASN ファイルのインポート結果を検査します。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. ASN インポートの一部として作成された積荷を検索して開きます。
1. **積荷** クイックタブで、XML ファイルに基づく値を確認する必要があります。
1. XML ファイルに基づき、**積荷明細行** クイックタブに発注書番号と品目の詳細が表示されます。
1. アクション ウィンドウ内の **出荷と入荷** タブの **受取** グループで **梱包構造** を選択して、積荷の梱包構造を確認します。
1. **パレット** クイックタブで、XML ファイルに基づくライセンス プレートを確認する必要があります。
1. **ケース** クイックタブで、XML ファイルに基づくケースを確認する必要があります。
1. **品目** クイックタブで、XML ファイルに基づく品目と数量を確認する必要があります。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
