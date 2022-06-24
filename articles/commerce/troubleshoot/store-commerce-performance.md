---
title: Store Commerce のパフォーマンスの問題のトラブルシューティング
description: この記事では、Microsoft Dynamics 365 Commerce Store Commerce アプリのパフォーマンスの問題に関するトラブルシューティングの方法について説明します。
author: mugunthanm
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2022-05-12
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: b690e35b2df736f3e277260e6f752ef5240b0938
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870495"
---
# <a name="troubleshoot-store-commerce-performance-issues"></a>Store Commerce のパフォーマンスの問題のトラブルシューティング

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

この記事では、Microsoft Dynamics 365 Commerce Store Commerce アプリのパフォーマンスの問題に関するトラブルシューティングの方法について説明します。

- Store Commerce のパフォーマンスの問題のトラブルシューティングを行う場合は、リモート サインインを避ける必要があります。 代わりに、Store Commerce デバイスに直接ログインします。
- Store Commerce アプリの速度が遅い場合、タスク マネージャーまたはリソース モニターを使用して CPU、メモリ、ネットワーク、およびディスクの使用状況を確認します。 デバイスのリソースが大きく消費されていないことを確認します。
- ネットワーク接続のステータスを確認し、HTTPS 要求/応答に数秒以上かかっていないことを確認します。
