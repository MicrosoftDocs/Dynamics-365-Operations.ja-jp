---
title: 見込顧客の現金化
description: この記事には、Dynamics 365 Supply Chain Management と Dynamics 365 Sales における見込顧客を現金化するソリューションの概要が含まれます。
author: Henrikan
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: ea07b40c0a1a7eae7cd167f46796556b1e0ecc46
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103597"
---
# <a name="prospect-to-cash"></a>見込顧客を現金化

[!include [banner](../includes/banner.md)]

見込顧客を現金化するソリューションは、Dynamics 365 Supply Chain Management および Dynamics 365 Sales 間で直接同期を提供します。 データ統合機能で利用可能な見込み顧客を現金化するテンプレートにより、勘定、連絡先、製品および販売見積、販売注文、および売上請求書のデータの流れが可能になります。 データが流れている間、Sales で販売およびマーケティング活動を行い、Supply Chain Management の在庫管理を使用して注文の履行を処理することができます。 

見込顧客の現金化への統合の詳細については、短い YouTube ビデオ[見込顧客の現金化への統合](https://www.youtube.com/watch?v=AVV9x5x-XCg)をご覧ください。

現在のバージョンでは、見込顧客を現金化するソリューションは次のタイプの直接同期を提供します:

- [Supply Chain Management の顧客への Sales の勘定の直接同期](accounts-template-mapping-direct.md)
- [製品を Supply Chain Management から Sales の製品に直接同期する](products-template-mapping-direct.md)
- [Supply Chain Management の連絡先または顧客への Sales の連絡先の直接同期](contacts-template-mapping-direct.md)
- [販売見積のヘッダーおよび明細行の Sales から Supply Chain Management への直接同期](sales-quotation-template-mapping-sales-fin.md)
- [販売注文の Sales と Supply Chain Management の間の直接同期](sales-order-template-mapping-direct-two-ways.md)
- [売上請求書のヘッダーおよび明細行の Supply Chain Management から Sales への直接同期](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-supply-chain-management"></a>Supply Chain Management のシステム要件
見込顧客の現金化は次のバージョンでサポートされています。

### <a name="microsoft-dynamics-365-finance-and-operations-enterprise-edition-73-december-2017"></a>Microsoft Dynamics 365 財務と運用、Enterprise Edition 7.3 (2017 年 12 月)

- Dynamics 365 財務と運用、Enterprise edition (2017 年 12 月) - プラットフォーム 更新プログラム 12 (7.0.4709.41129) によるアプリケーション ビルド 7.3.11971.56116

### <a name="dynamics-365-finance-enterprise-edition-july-2017"></a>Dynamics 365 Finance、Enterprise Edition (2017 年 7 月)

- Dynamics 365 財務と運用、Enterprise edition (2017 年 7 月) - プラットフォーム 更新プログラム 8 (プラットフォーム ビルド 7.0.4565.16212 によるアプリケーション ビルド 7.2.11792.56024) による。
- 次の修正プログラムが必要です。

  - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – この修正プログラムはデータ統合機能を利用した Sales から Supply Chain Management への販売注文の同期を有効にします。 他のいくつかの機能拡張も提供されています。
  - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – この修正プログラムはデータ統合機能を利用した Supply Chain Management から Sales への販売注文明細行の同期を有効にします。
  - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – この修正プログラムはデータ統合機能を利用した Supply Chain Management から Sales への販売注文の同期を有効にします。

    > [!NOTE]
    > インストールに他の修正プログラムからの変更が含まれているため、KB4045570 のみをインストールしなければなりません。 

### <a name="dynamics-365-finance-and-operations-version-1611-november-2016"></a>Dynamics 365財務と運用バージョン 1611 (2016 年 11 月)

- プラットフォーム 更新プログラム 8 またはそれ以降による Dynamics 365 財務と運用バージョン 1611 (2016 年 11 月)

- 次の修正プログラムが必要です。

  - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Supply Chain Management から Sales へのデータ インテグレーターの販売注文同期を有効にします。 
  - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - データ インテグレーターによる Supply Chain Management から Sales への販売注文ヘッダーと明細行の同期を有効にします。
  - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - データ エンティティによる見込顧客を現金化する統合のサポートが必要です。
    
    > [!NOTE]
    > 修正プログラムをインストール後、**SalesPopulateProspectToCash** フォームから次のバッチ ジョブをトリガーしなければなりません。 このフォームは一度しか必要ではないので非表示になります。 フォームにアクセスするためには、環境にログインし、ブラウザのアドレスに以下の URL を追加してください:*&mi=action:SalesPopulateProspectToCash*、たとえば、`https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`。 このフォームを開くには、[OK] をクリックします。 これにより固有値を持つ新しい **SalesLine**、**SalesQuotationLine** および **CustInvoiceTrans** テーブルに **LineCreationSequnceNumber** フィールドが設定され、製品リストが更新されます。 これは見込顧客が現金化の統合を作業するために必要です。


## <a name="system-requirements-for-sales"></a>Sales のシステム要件

見込顧客を現金化するソリューションを使用するには、以下のコンポーネントをインストールする必要があります:

- Dynamics 365 Sales バージョン 1612 (8.2.1.207) (DB 8.2.1.207) オンラインまたはそれ以降のバージョン
- Dynamics 365 Sales バージョン 1.15.0.0 またはそれ以降のバージョンの見込顧客を現金化するソリューション。 このソリューションは、AppSource からダウンロードできます。 [Dynamics 365、見込顧客を現金化のダウンロード](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
