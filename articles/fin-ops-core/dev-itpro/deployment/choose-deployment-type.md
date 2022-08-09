---
title: 展開オプション
description: 財務と運用アプリは、クラウドまたはオンプレミスで実行することができます。 この記事では、各種の展開オプションについて説明します。
author: sericks007
ms.date: 11/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform Update 8
ms.custom:
- "60373"
ms.assetid: ''
ms.openlocfilehash: 59a38dad319f8737d10deed6f5b0a388c74a434a
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/28/2022
ms.locfileid: "9205912"
---
# <a name="deployment-options"></a>展開オプション

[!include [banner](../includes/banner.md)]

財務と運用アプリをクラウドまたはオンプレミスで展開することができます。 クラウド配置では、顧客のデータ センター内にオンプレミス配置がローカルに配置されたときに、Microsoft で完全に管理されている ERP サービスが提供されます。 
> [!IMPORTANT]
> オンプレミス配置は、Azure を含む、任意のパブリック クラウド インフラストラクチャでサポートされていません。 ただし、[Microsoft Azure Stack HCI](https://azure.microsoft.com/products/azure-stack/hci/) および [Microsoft Azure Stack Hub](https://azure.microsoft.com/products/azure-stack/hub/) での実行はサポートされています。

次のテーブルは、2 つの配置オプションによって提供される機能の比較を示しています。

[![配置オプション テーブル。](./media/deployment-options.png)](./media/deployment-options.png)


## <a name="why-cloud"></a>クラウドを使用する理由
クラウド展開では、Microsoft が完全に管理するデータ センターだけでなく、必要に応じて簡単にスケールアップまたはスケールダウンできるクラウド サービスを提供します。 財務と運用アプリの実装に費やされる時間を大幅に短縮し、必要なカスタマイズを減らします。IT ハードウェアやインフラストラクチャのコストも削減できます。 

クラウド展開には、インテリジェンス、インフラストラクチャ、コンピューティング、およびデータベース サービスのクラウドベースのシステムを組み合わせた高可用性、障害復旧、サンドボックス環境、アプリケーション ライフサイクル管理が含まれます。 必要に応じて、クラウドでのデータ フェールオーバー、自動配置と継続的な更新、および柔軟な処理能力を使用できます。 クラウド配置では、データの集計、財務報告およびインテリジェンスも提供されます。

クラウド サービスは、顧客に最大の価値、幅広い機能、最高のアプリケーション ライフサイクル エクスペリエンス、Microsoft Azure サービスとの最も簡単で広範な統合、ビジネス インサイトとインテリジェンスのための最良のオプション、そして顧客のテクノロジー投資に対する最大の価値を提供します。 

## <a name="why-on-premises"></a>オンプレミスを使用する理由
オンプレミス展開では、既存のデータ センター投資を活用することができます。 顧客は、ビジネスの規制およびコンプライアンスのニーズを満たすため、Azure データ センターがない地域のデータ主権ルールに準拠するように、または限られた公共インフラストラクチャを持つ地域でビジネス継続性を確保するように、企業のプリファレンスを構成することもできます。 

顧客のビジネス データとプロセスはクラウドから切断され、顧客やパートナーのデータ センターのローカルで保存、および実行されます。 なんらかの接続が、クラウド ベースのアプリケーション ライフサイクル管理サービスである Microsoft Dynamics Lifecycle Services (LCS) を通じて有効になるシステムの管理と更新に必要です。 コンフィギュレーションおよびアプリケーションのカスタマイズに関連する顧客データは、クラウドに格納されている場合があります。 

独自のデータ センターで財務と運用アプリを実行する選択をした顧客は、オンプレミス配置オプションはその他の配置オプションと同様のユーザー インターフェイスおよびアプリケーション機能を持ちます。 ただし、顧客は次の責任を負う必要があります。

- 独自のインフラストラクチャを立ち上げます。 
- 独自の高可用性および障害回復ソリューションをコンフィギュレーションします。 
- サンドボックス環境を立ち上げます。
- オペレーティング システム更新のスケジュール設定を含む、インフラストラクチャを管理します。

これらの機能を配置および管理するための原価が増えると、配置コストおよび総保有コスト (TCO) の増大につながる可能性があります。 財務と運用アプリおよび更新プログラムを展開するためのツールは、Lifecycle Services を通じてパートナーおよび顧客に提供されます。 クラウド展開オプションとは異なり、Advanced Analytics と Azure Machine Learning はオンプレミス展開オプションには含まれていません。 





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

