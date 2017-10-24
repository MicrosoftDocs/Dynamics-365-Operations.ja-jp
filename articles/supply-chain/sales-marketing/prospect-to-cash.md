---
title: "見込顧客を現金化"
description: "トピックでは、Dynamics 365 for Sales and Dynamics 365 for Finance and Operations, Enterprise edition および Dynamics 365 for Sales における見込顧客を現金化するソリューションの概要を提供します。"
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a>見込顧客を現金化  

[!include[banner](../includes/banner.md)]

見込顧客を現金化ソリューションにより、[データ統合](/common-data-service/entity-reference/dynamics-365-integration)を使用し、Common Data Service (CDS) 経由で Dynamics 365 for Finance and Operations, Enterprise edition および Dynamics 365 for Sales インスタンス間でデータを同期します。 データ統合機能で利用可能な見込み顧客を現金化するテンプレートは、Finance and Operations と Sales 間での勘定、連絡先、製品および販売見積、販売注文、および売上請求書データの流れを可能にします。 データは Finance and Operations と Sales との間を流れていますが、Sales のセールスおよびマーケティング活動を行い、Finance and Operations の在庫管理で注文の履行を処理することができます。 

このソリューションは、次の領域での統合を提供します。 

-   [Sales でアカウントの管理、および Finance and Operations への同期](accounts-template-mapping.md)
-   [Sales で連絡先の管理、および Finance and Operations への同期](contacts-template-mapping.md)
-   [Finance and Operations で製品の管理、および Sales への同期](products-template-mapping.md)
-   [Sales で販売見積の作成、および Finance and Operations への同期](sales-quotation-template-mapping.md)
-   [Finance and Operations で販売注文の作成、および Sales への同期](sales-order-template-mapping.md)
-   [Finance and Operations で販売請求書の作成、および Sales への同期](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Dynamics 365 for Finance and Operations, Enterprise Edition のシステム要件

見込顧客を現金化するソリューションを使用するには、以下をインストールする必要があります。

- プラットフォーム アップデート 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212) による Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月)

- Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 ７ 月) の 2 つの修正プログラム。

    -  [KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - この修正プログラムは Finance and Operations から Sales へのデータ統合機能による販売注文明細行の同期を有効にします。
        
    -  [KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - この修正プログラムは Finance and Operations から Sales へのデータ統合機能による販売注文の同期を有効にします。
    
[**注記**]: インストールには KB4036461 からの変更が含まれているため、KB4036524 のみをインストールする必要があります。
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a>Dynamics 365 for Sales のシステム要件

見込顧客を現金化するソリューションを使用するには、以下をインストールする必要があります。

- Dynamics 365 for Sales バージョン 1612 (8.2.1.207) (DB 8.2.1.207) オンラインまたはそれ以降。
- Dynamics 365 for Sales バージョン 1.14.0.0 (v14) またはそれ以降の見込顧客を現金化するソリューション。

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>Sales の見込顧客を現金化するソリューションのインストール

- CustomerSource で [Dynamics 365 for Sales の見込顧客を現金化ソリューション パッケージ zip ファイル](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) をダウンロードします。

- zip ファイルがブロックされていないことを確認し、リューション パッケージをインストールする際に、「インポート パッケージが見つかりませんでした」のエラー メッセージが出ないようにします。 ファイルをブロック解除するには、次の点を行います。

    -  zip ファイルを右クリックします。
    -  [**プロパティ**] を選択し、次に [**ブロック解除**] を選択します。 

- 解凍して、PackageDeployer.exe を実行します。

- 売上インスタンスで見込顧客を現金化するソリューションのインストール

    - [**Office 365**] 配置タイプを選択します。
    - [**高度な表示**] を選択します。
    - クイック インストールするには、[**地域**] を選択します。 [**わからない**] を選択する場合、システムはすべての地域を検索するためインストールに時間がかかります。
    - インストールするユーザーの権限を持つ管理者ユーザーに対して [**ユーザー名**] および [**パスワード**] を入力します。

