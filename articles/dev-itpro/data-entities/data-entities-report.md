---
title: 標準データ エンティティに関する情報を検索します。
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations で使用可能な標準データ エンティティに関する情報を取得する方法について説明します。
author: margoc
manager: AnnBe
ms.date: 12/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 202654
ms.assetid: 6ec8ea87-ea1e-4a10-9d67-2b6565c5c62e
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: a09ca4e10ff83c48969edf3b9a5f107cca8f5910
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551076"
---
# <a name="find-information-about-standard-data-entities"></a>標準データ エンティティに関する情報の検索

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations には、数多くの既定のデータ エンティティが含まれています。 データ エンティティは頻繁に更新されるため、ドキュメント化のために、データ エンティティ テンプレートを使用して、どのオーダーデータエンティティをインポートする必要があるかを示します。また、各リリースで出荷されるデータ エンティティのリストも使用します。

## <a name="configuration-data-packages"></a>コンフィギュレーション データ パッケージ
Microsoft Dynamics Lifecycle Services (LCS) のコンフィギュレーション データ パッケージには、コンフィギュレーション エンティティのスプレッドシートが含まれています。 コンフィギュレーション エンティティ スプレッドシートには、Finance and Operations 実装の初期ゴールド ・ ビルドを作成するために使用できるベスト プラクティス データが含まれています。 XML ファイルを使用してデータ パッケージ内のデータ エンティティも適切に順序付けされ、1 回のクリックによるインポートを成功させるのに役立ちます。 データのインポートを指示することをどうしてお勧めしているかを理解していただくために、コンフィギュレーション データ パッケージをダウンロードして確認することをお勧めします。 詳細については、[データ テンプレートのコンフィギュレーション](configuration-data-templates.md) および [1 つの会社または法人から、別の会社または法人へのコンフィギュレーション データのコピー](copy-configuration.md) を参照してください。

## <a name="data-entity-reports"></a>データ エンティティ レポート
Microsoft は、データ エンティティの次のレポートを提供しており、[技術参照レポート](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)からダウンロードできます。

- **データ エンティティ**は、使用可能な各データ エンティティをリストします。 レポートには、エンティティのデータ ソースとエンティティに含まれるフィールドが示されます。 このレポートは、データ エンティティが公開されているかどうかも示します。
- **データ エンティティ フィールド**は、データエンティティの各フィールドと、それが発生したテーブルを一覧表示します。
- **データ エンティティの集計**集計データ エンティティと、それぞれに含まれるフィールドを一覧表示します。

各テーブルとそのテーブルのグループをリスト表示している -- 対象のテーブル レポートを検索する場合もあります。

## <a name="additional-resources"></a>その他のリソース
[データ エンティティのホーム ページ](data-entities.md)
