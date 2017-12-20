---
title: "見込顧客を現金化"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition、および Microsoft Dynamics 365 for Sales における見込顧客を現金化するソリューションについて概説します。"
author: ChristianRytt
manager: AnnBe
ms.date: 11/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 788e64476094e84eb4d438890776306c05b20582
ms.openlocfilehash: 762699cf68ec8a9df5db20d7dd33bc9248f0a36e
ms.contentlocale: ja-jp
ms.lasthandoff: 12/11/2017

---

# <a name="prospect-to-cash"></a>見込顧客を現金化

[!include[banner](../includes/banner.md)]

この見込顧客を現金化するソリューションは、Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition、および Microsoft Dynamics 365 for Sales 間で直接同期を提供します。 データ統合機能で利用可能な見込み顧客を現金化するテンプレートは、Finance and Operations と Sales 間での勘定、連絡先、製品および販売見積、販売注文、および売上請求書のデータの流れを可能にします。 データは Finance and Operations と Sales との間を流れていますが、Sales のセールスおよびマーケティング活動を行い、Finance and Operations の在庫管理を使用して注文の履行を処理することができます。

現在のバージョンでは、見込顧客を現金化するソリューションは次のタイプの直接同期を提供します:

- [Sales でアカウントの管理、および Sales から Finance and Operations への直接同期](accounts-template-mapping-direct.md)
- [Finance and Operations で製品の管理、および Sales への直接同期](products-template-mapping-direct.md)
- [Sales の連絡先を管理し、Finance and Operations の連絡先または顧客に直接同期させる](contacts-template-mapping-direct.md)
- [販売見積の Sales から Finance and Operations への直接同期](sales-quotation-template-mapping-sales-fin.md)
- [販売注文の Finance and Operations から Sales への直接同期](sales-order-template-mapping-direct.md)
- [販売注文の Sales と Finance and Operations の間の直接同期](sales-order-template-mapping-direct-two-ways.md)
- [売上請求書の Finance and Operations から Sales への直接同期](sales-invoice-template-mapping-direct.md)

以前のバージョンでは、見込顧客を現金化するソリューションは次のタイプの非直接同期を提供します:

- [Sales でアカウントの管理、および Finance and Operations への同期](accounts-template-mapping.md)
- [Sales で連絡先の管理、および Finance and Operations への同期](contacts-template-mapping.md)
- [Finance and Operations で製品の管理、および Sales への同期](products-template-mapping.md)
- [Sales で販売見積の作成、および Finance and Operations への同期](sales-quotation-template-mapping.md)
- [Finance and Operations で販売注文の作成、および Sales への同期](sales-order-template-mapping.md)
- [Finance and Operations で販売請求書の作成、および Sales への同期](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a>Finance and Operations のシステム要件

見込顧客を現金化するソリューションを使用するには、以下のコンポーネントをインストールする必要があります:

### <a name="july-2017"></a>2017 年 7 月 

- プラットフォーム アップデート 8 (プラットフォーム ビルド 7.0.4565.16212 によるアプリケーション ビルド 7.2.11792.56024 ) による Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月)
- Finance and Operations の次の修正プログラム。

    - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – この修正プログラムはデータ統合機能を利用した Sales から Finance and Operations への販売注文の同期を有効にします。 他のいくつかの機能拡張も提供されています。
    - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – この修正プログラムはデータ統合機能を利用した Finance and Operations から Sales への販売注文明細行の同期を有効にします。
    - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – この修正プログラムはデータ統合機能を利用した Finance and Operations から Sales への販売注文の同期を有効にします。

    > [!NOTE]
    > インストールに他の Microsoft サポート技術情報 (KB) からの変更が含まれているため、KB4045570 のみをインストールする必要があります。

### <a name="november-2016-version-1611"></a>2016 年 11 月 (バージョン 1611)

- プラットフォーム アップデート 8 またはそれ以降による Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (2016 年 11 月)

- Finance and Operations の次の修正プログラム。

    - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Microsoft Dynamics 365 for Finance and Operations から Sales へのデータ インテグレーターの販売注文同期を有効にします。 
    - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Microsoft Dynamics 365 for Finance and Operations から Sales へのデータ インテグレーターの販売注文ヘッダーと明細行の同期を有効にします。
    - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - データ エンティティによる見込顧客を現金化する統合のサポートが必要です
    
    > [!NOTE]
    > 修正プログラムをインストール後、に SalesPopulateProspectToCash フォームから次のバッチ ジョブをトリガーする必要があります。 このフォームは 1 度しか必要ではないので非表示になります。 これにアクセスするためには、環境にログインした時に、ブラウザのアドレスに以下を追加してください: &mi=action:SalesPopulateProspectToCash E.g. https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash オープンするフォームで OK をクリックします。
    これにより固有値を持つ新しい 「SalesLine」、「SalesQuotationLine」 および 「CustInvoiceTrans」 テーブルに 「LineCreationSequnceNumber」 フィールドが設定され、製品リストが更新されます。 これは P2C の統合が 7.1 で機能するために必要です。


## <a name="system-requirements-for-sales"></a>Sales のシステム要件

見込顧客を現金化するソリューションを使用するには、以下のコンポーネントをインストールする必要があります:

- Microsoft Dynamics 365 for Sales バージョン 1612 (8.2.1.207) (DB 8.2.1.207) オンライン
- Microsoft Dynamics 365 for Sales バージョン 1.15.0.0 (v15) の見込顧客を現金化するソリューション 

   > [!NOTE]
   >
   > テンプレート バージョン 1.0.0.0 および 1.0.0.1 は Microsoft Dynamics 365 for Sales、バージョン 1.14.1.0 の見込顧客を現金化するソリューションでサポートされています。
   >
   > テンプレート バージョン 2.0.0.0 および 2.1.0.0 は Microsoft Dynamics 365 for Sales、バージョン 1.15.0.0 の見込顧客を現金化するソリューションでサポートされています。

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>Sales の見込顧客を現金化するソリューションのインストール

1. CustomerSource から [Dynamics 365 for Sales の見込顧客を現金化ソリューション パッケージ zip ファイル](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) をダウンロードします。
2. zip ファイルがブロックされていないことを確認します。 それ以外の場合、ソリューション パッケージをインストールするさいに次のエラー メッセージを受け取ります: [「インポート パッケージ見つかりませんでした」]。 zip ファイルのブロックを解除するには、ファイルを右クリックし [**プロパティ**] を選択します。 次に [**ブロック解除**] を選択します。
3. 解凍して、**PackageDeployer.exe** を実行します。
4. 売上インスタンスで見込顧客を現金化するソリューションのインストール:

    1. 配置タイプとして [**Office 365**] を選択します。
    2. [**高度な表示**] を選択します。
    3. クイック インストールするには、[地域] を選択します。 [**わからない**] を選択する場合、システムはすべての地域を検索するためインストールに時間がかかります。
    4. インストールする権限を持つ管理者ユーザーの [ユーザー名] および [パスワード] を入力します。

