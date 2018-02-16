---
title: "見込顧客を現金化"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition、および Microsoft Dynamics 365 for Sales における見込顧客を現金化するソリューションについて概説します。"
author: ChristianRytt
manager: AnnBe
ms.date: 02/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 602873e8af976c57f27ce53b76391516351755e3
ms.openlocfilehash: 29d33d3ecf97c15fed0247d172ff6fb3bbdaa018
ms.contentlocale: ja-jp
ms.lasthandoff: 01/25/2018

---

# <a name="prospect-to-cash"></a>見込顧客を現金化

[!include[banner](../includes/banner.md)]

この見込顧客を現金化するソリューションは、Dynamics 365 for Finance and Operations、Enterprise Edition、および Dynamics 365 for Sales 間で直接同期を提供します。 データ統合機能で利用可能な見込み顧客を現金化するテンプレートは、Finance and Operations と Sales 間での勘定、連絡先、製品および販売見積、販売注文、および売上請求書のデータの流れを可能にします。 データは Finance and Operations と Sales との間を流れていますが、Sales のセールスおよびマーケティング活動を行い、Finance and Operations の在庫管理を使用して注文の履行を処理することができます。 

見込顧客を現金化することの詳細については、短い YouTube ビデオを確認してください。

> [!Video https://www.youtube.com/embed/AVV9x5x-XCg]

現在のバージョンでは、見込顧客を現金化するソリューションは次のタイプの直接同期を提供します:

- [Sales でアカウントの管理、および Sales から Finance and Operations への直接同期](accounts-template-mapping-direct.md)
- [Finance and Operations での製品の管理、および Sales への直接同期](products-template-mapping-direct.md)
- [Sales の連絡先の管理、および Finance and Operations の連絡先または顧客への直接同期](contacts-template-mapping-direct.md)
- [販売見積の Sales から Finance and Operations への直接同期 (リリース保留中のテンプレート)](sales-quotation-template-mapping-sales-fin.md)
- [販売注文の Finance and Operations から Sales への直接同期](sales-order-template-mapping-direct.md)
- [販売注文の Sales と Finance and Operations の間の直接同期 (リリース保留中のテンプレート)](sales-order-template-mapping-direct-two-ways.md)
- [売上請求書の Finance and Operations から Sales への直接同期](sales-invoice-template-mapping-direct.md)

以前のバージョンでは、見込顧客を現金化するソリューションは次のタイプの非直接同期を提供します:

- [Sales でアカウントの管理、および Finance and Operations への同期](accounts-template-mapping.md)
- [Sales での連絡先の管理、および Finance and Operations への同期](contacts-template-mapping.md)
- [Finance and Operations での製品の管理、および Sales への同期](products-template-mapping.md)
- [Sales での販売見積の作成、および Finance and Operations への同期](sales-quotation-template-mapping.md)
- [Finance and Operations での販売注文の作成、および Sales への同期](sales-order-template-mapping.md)
- [Finance and Operations での売上請求書の作成、および Sales への同期](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a>Finance and Operations のシステム要件

見込顧客の現金化は次のバージョンでサポートされています。

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a>Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 (2017 年 12 月)

- Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 12 月) - プラットフォーム アップデート 12 (7.0.4709.41129) によるアプリケーション ビルド 7.3.11971.56116

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月)

- Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月) - プラットフォーム アップデート 8 (プラットフォーム ビルド 7.0.4565.16212 によるアプリケーション ビルド 7.2.11792.56024) による。
- 次の修正プログラムが必要です。

    - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – この修正プログラムはデータ統合機能を利用した Sales から Finance and Operations への販売注文の同期を有効にします。 他のいくつかの機能拡張も提供されています。
    - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – この修正プログラムはデータ統合機能を利用した Finance and Operations から Sales への販売注文明細行の同期を有効にします。
    - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – この修正プログラムはデータ統合機能を利用した Finance and Operations から Sales への販売注文の同期を有効にします。

    > [!NOTE]
    > インストールに他の修正プログラムからの変更が含まれているため、KB4045570 のみをインストールしなければなりません。 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a>Dynamics 365 for Finance and Operations バージョン 1611 (2016 年 11月)

- プラットフォーム アップデート 8 またはそれ以降による Dynamics 365 for Finance and Operations バージョン 1611 (2016 年 11 月)

- 次の修正プログラムが必要です。

    - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Finance and Operations から Sales へのデータ インテグレーターの販売注文同期を有効にします。 
    - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Finance and Operations から Sales へのデータ インテグレーターの販売注文のヘッダーと明細行の同期を有効にします。
    - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - データ エンティティによる見込顧客を現金化する統合のサポートが必要です。
    
    > [!NOTE]
    > 修正プログラムをインストール後、[**SalesPopulateProspectToCash**] フォームから次のバッチ ジョブをトリガーしなければなりません。 このフォームは一度しか必要ではないので非表示になります。 フォームにアクセスするには、環境にログインし、次の事項をブラウザーのアドレス内のURLに追加します。&mi=action:SalesPopulateProspectToCash、たとえば、https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash。 このフォームを開くには、[OK] をクリックします。 これにより固有値を持つ新しい [**SalesLine**]、[**SalesQuotationLine**] および [**CustInvoiceTrans**] テーブルに [**LineCreationSequnceNumber**] フィールドが設定され、製品リストが更新されます。 これは見込顧客が現金化の統合を作業するために必要です。


## <a name="system-requirements-for-sales"></a>Sales のシステム要件

見込顧客を現金化するソリューションを使用するには、以下のコンポーネントをインストールする必要があります:

- Dynamics 365 for Sales バージョン 1612 (8.2.1.207) (DB 8.2.1.207) オンライン
- Dynamics 365 for Sales バージョン 1.15.0.0 (v15) の見込顧客を現金化するソリューション 

   > [!NOTE]
   >
   > テンプレート バージョン 1.0.0.0 および 1.0.0.1 は Dynamics 365 for Sales、バージョン 1.14.1.0 の見込顧客を現金化するソリューションでサポートされています。
   >
   > テンプレート バージョン 2.0.0.0 および 2.1.0.0 は Dynamics 365 for Sales、バージョン 1.15.0.0 の見込顧客を現金化するソリューションでサポートされています。

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>Sales の見込顧客を現金化するソリューションのインストール

1. CustomerSource から [Dynamics 365 for Sales の見込顧客を現金化ソリューション パッケージ zip ファイル](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) をダウンロードします。
2. zip ファイルがブロックされていないことを確認します。 それ以外の場合、ソリューション パッケージをインストールする際に次のエラー メッセージを受け取るかもしれません [「インポート パッケージ見つかりませんでした」]。 zip ファイルのブロックを解除するには、ファイルを右クリックし [**プロパティ**] を選択します。 [**ブロック解除**] を選択します。
3. 解凍して、**PackageDeployer.exe** を実行します。
4. 売上インスタンスで見込顧客を現金化するソリューションのインストール:

    1. 配置タイプとして [**Office 365**] を選択します。
    2. [**高度な表示**] を選択します。
    3. クイック インストールするには、[地域] を選択します。 [**わからない**] を選択する場合、システムはすべての地域を検索するためインストールに時間がかかります。
    4. インストールする権限を持つ管理者ユーザーの [ユーザー名] および [パスワード] を入力します。



