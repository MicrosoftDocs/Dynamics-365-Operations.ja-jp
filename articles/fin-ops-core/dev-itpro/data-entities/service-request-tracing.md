---
title: サービス要求の追跡
description: このトピックでは、財務と運用サービスを通じて要求を追跡し、トラブルシューティングに役立てるため、ヘッダーに含めるべきクライアント要求 ID に関する情報を提供します。
author: jaredha
ms.date: 04/07/2022
ms.topic: article
audience: IT Pro, Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2022-04-07
ms.openlocfilehash: d68ea28af67383ed8024c0340124a5d6f3c524ef
ms.sourcegitcommit: 7faf82fa7ce269c0201abb8473af861ef7ce00bf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/19/2022
ms.locfileid: "8614202"
---
# <a name="service-request-tracing"></a>サービス要求の追跡

[!include[banner](../includes/banner.md)]

財務と運用サービス エンドポイントとのデータ統合を開発する際のベスト プラクティスとして、要求ヘッダーに要求 ID を含める必要があります。 このようにして、サービスを通じて要求を追跡できます。 クライアント アプリケーションではクライアント要求 ID (`x-ms-client-request-id`) 値を生成およびログ記録し、アプリケーション プログラミング インターフェイス (API) 要求ヘッダーに含めて送信する必要があります。 この値は、各クライアント要求を一意に識別する、グローバル一意識別子 (GUID) です。

財務と運用サービスは、要求ヘッダーに受け取った `x-ms-client-request-id`値をログ記録します。 これにより、この値はサービス テレメトリの要求に対する ID として利用可能になります。

## <a name="troubleshooting-api-operations"></a>API 操作のトラブルシューティング

要求が常に失敗し、その要求が正しく作成されていることを確認した場合は、Microsoft が問題のトラブルシューティングを支援するようサポート チケットを開くことが必要になる場合があります。 サポート チケットに、次の値を入力します:

- クライアント アプリケーションが生成し、要求ヘッダーで送信される `x-ms-client-request-id` 値。
- 財務と運用の活動 ID である、`ms-dyn-aid` 値。 財務と運用サービスは、要求に対してこの固有 ID を生成し、応答ヘッダーでクライアント アプリケーションに送り返されます。
- 要求が実行された、おおよその時間。

これらの値を使用すると、Microsoft はサービス テレメトリを通じて要求を追跡し、要求が失敗した原因をトラブルシューティングできます。 サービスがクライアントに応答を返さず、`ms-dyn-aid` 値が提供されない場合、Microsoft が API 要求を追跡できるように、少なくとも `x-ms-client-request-id` 値と要求のおおよその時間をサポート チケットに提供するようにしてください。
