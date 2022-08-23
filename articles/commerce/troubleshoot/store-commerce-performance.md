---
title: Store Commerce のパフォーマンスの問題のトラブルシューティング
description: この記事では、Microsoft Dynamics 365 Commerce Store Commerce アプリのパフォーマンスの問題に関するトラブルシューティングの方法について説明します。
author: josaw1
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2022-05-12
ms.dyn365.ops.version: 10.0.25
ms.search.industry: Retail
ms.openlocfilehash: 0354fbac438ff00ba057993a466bbbbfdd99247d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286306"
---
# <a name="troubleshoot-store-commerce-performance-issues"></a>Store Commerce のパフォーマンスの問題のトラブルシューティング

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce Store Commerce アプリのパフォーマンスの問題に関するトラブルシューティングの方法について説明します。

- Store Commerce のパフォーマンスの問題のトラブルシューティングを行う場合は、リモート サインインを避ける必要があります。 代わりに、Store Commerce デバイスに直接ログインします。
- Store Commerce アプリの速度が遅い場合、タスク マネージャーまたはリソース モニターを使用して CPU、メモリ、ネットワーク、およびディスクの使用状況を確認します。 デバイスのリソースが大きく消費されていないことを確認します。
- ネットワーク接続のステータスを確認し、HTTPS 要求/応答に数秒以上かかっていないことを確認します。
