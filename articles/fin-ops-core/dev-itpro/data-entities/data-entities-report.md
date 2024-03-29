---
title: 標準データ エンティティに関する情報を検索します。
description: この記事では、使用可能な標準データ エンティティに関する情報を取得する方法、およびレポートを実行するスクリプトをダウンロードする方法について説明します。
author: peakerbl
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.custom: 202654
ms.assetid: 6ec8ea87-ea1e-4a10-9d67-2b6565c5c62e
ms.openlocfilehash: dbd7b3d4e5bc8267576d8bc4043df1ae75cfbd6b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289800"
---
# <a name="find-information-about-standard-data-entities"></a>標準データ エンティティに関する情報の検索

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

アプリケーションには、既定のデータ エンティティが数多く含まれています。 データ エンティティは頻繁に更新されるため、ドキュメント化のために、データ エンティティ テンプレートを使用して、どのオーダーデータエンティティをインポートする必要があるかを示します。また、各リリースで出荷されるデータ エンティティのリストも使用します。

## <a name="configuration-data-packages"></a>コンフィギュレーション データ パッケージ

Microsoft Dynamics Lifecycle Services (LCS) のコンフィギュレーション データ パッケージには、コンフィギュレーション エンティティのスプレッドシートが含まれています。 コンフィギュレーション エンティティ スプレッドシートには、実装の初期ゴールド ビルドを作成するために使用できるベスト プラクティス データが含まれています。 XML ファイルを使用してデータ パッケージ内のデータ エンティティも適切に順序付けされ、1 回のクリックによるインポートを成功させるのに役立ちます。 データのインポートを指示することをどうしてお勧めしているかを理解していただくために、コンフィギュレーション データ パッケージをダウンロードして確認することをお勧めします。 詳細については、 [データ テンプレートの構成](configuration-data-templates.md) および [会社間、または法人間で構成データをコピーする](copy-configuration.md) を参照してください。

## <a name="reports"></a>レポート

Microsoft は、データ エンティティの次のレポートを提供しており、[技術参照レポート](/dynamics/s-e/global/axtechrefrep_61)からダウンロードできます。

- データ エンティティの集計: 集計するデータ エンティティと、それぞれに含まれるフィールドを一覧表示します。
- メジャーの集計: 集計するメジャーを一覧表示します。
- コンフィギュレーション キー: コンフィギュレーション キーの一覧が表示されます。 
- コンフィギュレーション キー グループ: コンフィギュレーション キー グループの一覧が表示されます。
- データ エンティティ: 各データ エンティティを一覧表示します。 レポートには、エンティティのデータ ソースとエンティティに含まれるフィールドが示されます。 このレポートは、データ エンティティが公開されているかどうかも示します。
- データ エンティティ フィールド: データ エンティティの各フィールドと、その元になったテーブルを一覧表示します。
- KPI: KPI を一覧表示します。
- ライセンス コード: 各コンフィギュレーション キーに関連付けられているライセンス コードの一覧を表示します。
- メニュー項目: 各コンフィギュレーション キーに関連付けられているメニュー項目を一覧表示します。
- SSRS レポート: 各レポートを一覧表示します。 レポートには、各レポートで使用されるデータ セットと、各レポートで使用可能なフィルターおよびフィールドが表示されます。
- テーブル: 各テーブルとそのテーブル グループの一覧を表示します。
- ワークフロー タイプ: 各種のワークフローを一覧表示します。 レポートでは、ワークフローの各タイプの使用目的を説明し、各タイプのワークフローが組織内の特定の法人または組織全体に関連付けられているかどうかも示されます。

## <a name="scripts"></a>スクリプト

これらのレポートを実行するスクリプトを、[fin-ops-doc-scripts](https://github.com/microsoft/fin-ops-doc-scripts) からダウンロードすることができます。

## <a name="additional-resources"></a>追加リソース

[データ エンティティの概要](data-entities.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
