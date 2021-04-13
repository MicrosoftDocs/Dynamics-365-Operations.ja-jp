---
title: データ エンティティを使用したデータの管理と統合についての概要
description: このトピックでは、同期と非同期の統合の仕組みについて簡単に説明します。
author: Sunil-Garg
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 26441
ms.assetid: 8aa25787-5920-4277-acff-7011200133f4
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f30afe7df45485ad268b2900b2867faaf0672e8b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750986"
---
# <a name="data-management-and-integration-by-using-data-entities-overview"></a>データ エンティティを使用したデータの管理と統合についての概要

[!include [banner](../includes/banner.md)]

このトピックでは、同期と非同期の統合の仕組みについて簡単に説明します。

## <a name="synchronous-services"></a>同期サービス

同期統合では、比較的簡単です。 **Is public** が有効なすべてのエンティティは、次の URL: `https://[BaseURL]/Data/<<Data Entity Public Collection Name>>` データ エンティティ パブリック コレクション名のサービス アプリケーション プログラミング インターフェイス (API) として自動的に使用できます。

現在、OData プロトコルは、すべての公開可能エンティティが相互作用できるエンドポイントを公開するために使用されます。

**サポートされているプロトコル:** OData V4.0

**データ形式:** JSON

**メタデータ URL:** `https://[BaseURL]/Data/$metadata`

## <a name="data-importexport-and-recurring-integration-scenarios"></a>データのインポート/エクスポートと定期的な統合のシナリオ
データ管理プラットフォームを通じた統合では、エンティティを介したデータの挿入/抽出に関するより多くの機能と高度なスループットが提供されます。 この統合シナリオでは通常、データは次の 3 つのフェーズに分かれています。

- **ソース** – これらは、受信データ ファイルまたはキュー内のメッセージです。 一般的なデータ形式には、CSV、XML、タブ区切りなどがあります。
- **ステージング** – これらは、データ エンティティに密接にマップして自動的に生成されたテーブルです。 **データ管理の有効化** が **true** のときは、中間記憶を提供するステージング テーブルが生成されます。 これにより、フレームワークは大量のファイルの解析、変換、およびいくつかの検証を行うことができます。
- **ターゲット** – これは、データをインポートするデータ エンティティです。

次の図は、着信フローを示しています。

![受信フロー](./media/over6.png)

## <a name="known-limitations-in-data-importexport"></a>データのインポート/エクスポートにおける既知の制限
テキスト ファイルをインポートするとき、文字列サイズは 32,768 文字に限定されます。 文字列がこれより大きい場合は、インポートされた文字列が切り捨てられます。 これは、基本的な実装の制限であり、SQL Server Integration Services (SSIS) によるものです。

32,768 文字を超える文字列をインポートする必要がある場合は、コンテナー エンティティ フィールドを使用することをお勧めします。

詳細については、FastTrack 技術解説のビデオ: [Dynamics 365 for Operations – 技術解説: 統合](https://www.youtube.com/watch?v=fooBvQhIo6I)をご覧ください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]