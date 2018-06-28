---
title: "データ管理とデータ エンティティを使用した統合"
description: "このトピックでは、同期と非同期の統合の仕組みについて簡単に説明します。"
author: Sunil-Garg
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 26441
ms.assetid: 8aa25787-5920-4277-acff-7011200133f4
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: fa5f295796d41e69d6c68d344ca1f9569386a977
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="data-management-and-integration-using-data-entities"></a>データ管理とデータ エンティティを使用した統合

[!include [banner](../includes/banner.md)]

このトピックでは、同期と非同期の統合の仕組みについて簡単に説明します。

<a name="synchronous-services"></a>同期サービス
--------------------

同期統合では、比較的簡単です。 <strong>パブリック</strong>が有効なすべてのエンティティは、次の URL: https://\[BaseURL\]/Data/&lt;&lt; データ エンティティ パブリック コレクション名&gt;&gt;のサービス アプリケーション プログラミング インターフェイス (API) として自動的に使用できます。

現在、OData プロトコルは、すべての公開可能エンティティが相互作用できるエンドポイントを公開するために使用されます。 <strong>サポートされているプロトコル:</strong>OData V4.0 <strong>データ形式:</strong>JSON <strong>メタデータ URL:</strong> https://\[BaseURL\]/Data/$metadata

## <a name="data-importexport-and-recurring-integration-scenarios"></a>データのインポート/エクスポートと定期的な統合のシナリオ
データ管理プラットフォームを通じた統合では、エンティティを介したデータの挿入/抽出に関するより多くの機能と高度なスループットが提供されます。 この統合シナリオでは通常、データは次の 3 つのフェーズに分かれています。

-   **ソース** – これらは、受信データ ファイルまたはキュー内のメッセージです。 一般的なデータ形式には、CSV、XML、タブ区切りなどがあります。
-   **ステージング** – これらは、データ エンティティに密接にマップして自動的に生成されたテーブルです。 **データ管理の有効化** が **true** のときは、中間記憶を提供するステージング テーブルが生成されます。 これにより、フレームワークは大量のファイルの解析、変換、およびいくつかの検証を行うことができます。
-   **ターゲット** – これは、データをインポートするデータ エンティティです。

次の図は、着信フローを示しています。 ![受信フロー](./media/over6.png)

## <a name="known-limitations-in-data-importexport"></a>データのインポート/エクスポートにおける既知の制限
テキスト ファイルをインポートするとき、文字列サイズは 32,768 文字に限定されます。 文字列がこれより大きい場合は、インポートされた文字列が切り捨てられます。 これは、基本的な実装の制限であり、SQL Server Integration Services (SSIS) によるものです。  

32,768 文字を超える文字列をインポートする必要がある場合は、コンテナー エンティティ フィールドを使用することをお勧めします。


詳細については、「FastTrack 技術解説」ビデオを確認してください。

> [!Video https://www.youtube.com/embed/fooBvQhIo6I?list=PLcakwueIHoT_BQxAZ6VFbWgX9sAWBW3Xi?ecver=1]




