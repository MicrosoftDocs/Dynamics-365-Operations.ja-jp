---
title: ヘッドレス コマースのアーキテクチャ
description: この記事では、ヘッドレス コマースのアーキテクチャについて説明します。
author: josaw1
ms.date: 06/03/2021
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-02-28
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 535a1de16555f96f0073f81ba4e7e5317ec35e33
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273523"
---
# <a name="headless-commerce-architecture"></a>ヘッドレス コマースのアーキテクチャ

[!include [banner](../includes/banner.md)]

この記事では、ヘッドレス コマース (Commerce Scale Unit とも呼ばれる) のアーキテクチャについて説明します。 ヘッドレス コマースは、拡張可能で、カスタマイズされたフリクションフリーなコマース エクスペリエンス、および統合され最適化されたバック オフィス操作を可能にする API 駆動型のフレームワークです。

![Commerce Scale Unit アーキテクチャ。](media/CSUExtensionArchitecture.PNG)

## <a name="omnichannel-solution-provided-by-the-headless-commerce"></a>ヘッドレス コマースが提供するオムニチャネル ソリューション

ヘッドレス コマースのコマース API は Microsoft Dynamics 365 Commerce によって使用され (バックオフィス、ストア内、コール センター、および e コマース)、完全なオムニチャネル ソリューションを提供します。 API は、サード パーティのアプリケーションおよび Microsoft Power Platform コネクタで使用できます。

![Commerce Scale Unit のプラットフォームの統合。](./media/CSUConsumer.PNG)

## <a name="components"></a>コンポーネント

ヘッドレス コマースには、次のコンポーネントが含まれます。

+ コンシューマー API
+ Commerce Runtime (CRT)
+ チャネル データベース

### <a name="consumer-apis"></a>コンシューマー API

ヘッドレス コマースでは、Dynamics 365 Commerce 用の Open Data Protocol (OData) API と使用できるサード パーティ アプリが公開されます。 API レイヤーは、ASP.NET コアを使用して作成されます。 クライアントが API を使用できるように異なった認証オプションが提供されます。 API は、ビジネス ロジックを公開するラッパーです。 詳細については、次の記事を参照してください。

+ [Commerce Scale Unit の顧客およびコンシューマー API](retail-server-customer-consumer-api.md)
+ [API の使用](consume-retail-server-api.md)
+ [カスタム API](retail-server-icontroller-extension.md)

### <a name="commerce-runtime"></a>Commerce Runtime

CRT は、コア コマース ビジネス ロジックを含むポータブル .NET ライブラリの集合です。 コンシューマー API はクライアントに使用するビジネス ロジックを公開します。 ビジネス ロジックを追加または変更するには、CRT をカスタマイズします。 詳細については、次の記事を参照してください。

+ [Commerce Runtime (CRT) のサービス](crt-services.md)
+ [CRT 拡張機能](commerce-runtime-extensibility.md)

### <a name="channel-database"></a>チャネル データベース

チャネル データベースは、オンライン ストアまたは従来型の店舗などの 1 つ以上のコマース チャネルからのトランザクション データおよびマスター データを保持します。 マスター データは Commerce Data Exchange (CDX) を使用して、Commerce 本社からチャネル データベースにプッシュ ダウンされます。 チャネル データベースに格納されたトランザクション データは、CDX を使用して Commerce 本社に引き戻されます。 詳細については、[チャネル データベース拡張機能](channel-db-extensions.md)を参照してください。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

