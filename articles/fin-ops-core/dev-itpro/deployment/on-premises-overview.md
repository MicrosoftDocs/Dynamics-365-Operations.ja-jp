---
title: オンプレミス配置の概要
description: Dynamics 365 Finance + Operations (on-premises) は、顧客データ センターでビジネス プロセスの実行をサポートします。
author: faix
ms.date: 11/30/2021
ms.topic: overview
ms.prod: dynamics-365
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform Update 8
ms.custom: 23401,  ""intro-internal
ms.assetid: ''
ms.service: ''
ms.openlocfilehash: 5873e6f76cf8d3fe94c9daa60eb3a55bb4963706
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271463"
---
# <a name="on-premises-deployment-overview"></a>オンプレミス配置の概要

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Finance + Operations (on-premises) は、顧客データ センターでビジネス プロセスの実行をサポートします。 この配置オプションでは、アプリケーション サーバーおよび Microsoft SQL Server データベースは顧客のデータ センター内で実行されます。 顧客およびパートナーは、Microsoft Dynamics Lifecycle Services (LCS) を利用して、社内展開を管理します。 LCS は、クラウドおよびオンプレミスでの実装のアプリケーション ライフサイクルを管理するためのツールおよびサービスを提供するアプリケーション管理ポータルです。 業務プロセス モデリング、ソフトウェアの展開および修正、監視および診断などの LCS の機能は、オンプレミス配置をサポートするために使用されます。

> [!IMPORTANT]
> Dynamics 365 Finance + Operations (on-premises) は、Microsoft Azure クラウド サービス を含む、任意のパブリック クラウド インフラストラクチャではサポートされていません。 ただし、[Microsoft Azure Stack HCI](https://azure.microsoft.com/products/azure-stack/hci/) および [Microsoft Azure Stack Hub](https://azure.microsoft.com/products/azure-stack/hub/) での実行はサポートされています。

## <a name="architecture"></a>アーキテクチャ

オンプレミス配置オプションは、Microsoft Azure Server Service Fabric スタンドアロン クラスターを使用して、オンプレミスで実行されるクラウド コンポーネントを使用します。 Service Fabric は、企業規模の大規模なアプリケーションを構築および管理するための次世代の Microsoft ミドルウェア プラットフォームです。 Service Fabric スタンドアロン クラスターは、Windows Server を実行しているどのコンピューターにも展開することができます。 

オンプレミスの設置では、運用環境用クラスターとサンドボックス環境用クラスターの2つのタイプの Service Fabric スタンドアロン クラスターを定義します。 両方のタイプのクラスターに、次のロールまたはノード タイプが配置されます。 

- Application Object Servers (AOS) – アプリケーション機能をクライアント、バッチ、およびインポート/エクスポートのシナリオで実行する機能を提供します。 
- Management Reporter (MR) – 財務レポートの機能を提供します。 
- SQL Server Reporting Services (SSRS): ドキュメント レポート機能を提供します。 
- 環境オーケストレータ – LCS からオンプレミス環境管理を有効にします。 

図 1 は、Service Fabric スタンドアロン クラスターで配置されるノード タイプの論理的な図を示します。 

[![Service fabric スタンドアロン クラスター。](./media/on-premises-overview-01.png)](./media/on-premises-overview-01.png)

オンプレミス配置のアプリケーション ライフサイクル管理は、LCS を通じて調整されます。 顧客は、LCS の実績のあるツールと方法を使用して、社内展開を管理することができます (図2)。 開発経験は、1 ボックス VHD によるクラウド配置と同じです。 

[![ローカル ビジネス データ展開のアプリケーション ライフサイクル管理。](./media/on-premises-overview-02.png)](./media/on-premises-overview-02.png)

## <a name="data-storage"></a>データ ストレージ 
オンプレミス配置オプションは、オンプレミスのコア顧客データを格納します。 コア顧客データは、[Microsoft Trust Center](https://www.microsoft.com/trustcenter/privacy/how-microsoft-defines-customer-data) で提供される顧客データ定義のサブセットです。 表 1 では、LCS、Azure Active Directory、および Microsoft Office のサインアップ ポータルなどのサービスにより、米国内にある Microsoft Azure データ センターに格納されている顧客データのカテゴリについて説明します。 コア顧客データと呼ばれる他のすべての顧客データは、オンプレミスに保管されます。  

表 1: オンプレミス環境をサポートするサービスによって、米国内にある Microsoft Azure データ センターに格納されている顧客データ。 これらのサービスにより、サポート インシデントの初期オンボーディング、開始、追跡、サービスの更新とアップグレードが可能になります。  


| サポート サービス                   | 顧客データの定義                                                                                                                                                                                                                                                            |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Microsoft Dynamics Lifecycle Services | プロジェクトには、プロジェクトのコンテンツおよびファイルが格納されます。 これには、アプリケーション構成データ、コード、メタデータ、アプリケーションやビジネス プロセス モデルを構成するデータ アセットが含まれます。 匿名化されたユーザー活動ログおよびオンボーディング プロセス中に収集された情報に含まれます。 |
| Microsoft Office サインアップ ポータル        | オンボード プロセス中に収集された顧客情報。                                                                                                                                                                                                                                 |
| Microsoft Azure Active Directory      | LCS と Azure DevOps の認証。                                                                                                                                                                                                               |
  

追加のサービスまたはコンポーネントは、必要に応じてオンプレミス配置を拡張するためにコンフィギュレーションすることができます。ただし、コンフィギュレーションの選択により、コア顧客データが顧客データ センターの外部に転送される可能性があります。 たとえば、オンプレミス配置の外部サービスを統合するために使用されるデータ管理機能のコンフィギュレーションにより、オンプレミス配置外のコア顧客データが転送される可能性があります。 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
