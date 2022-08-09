---
title: API スロットリングの監視
description: この記事では、サービスの保護制限に達する場合にアプリケーション プログラミング インターフェイス (API) の監視に使用できるツールについて説明します。
author: jaredha
ms.date: 05/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2022-04-16
ms.dyn365.ops.version: Platform update 52
ms.openlocfilehash: dd853bae70b212cda559cd6e27f8327216eaf306
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135374"
---
# <a name="monitor-api-throttling"></a>API スロットリングの監視

[!include [banner](../includes/banner.md)]

この記事では、サービスの保護制限に達する場合にアプリケーション プログラミング インターフェイス (API) の監視に使用できるツールについて説明します。

スロットリング機能を含むオンボード エクスペリエンスを成功させるには、Open Data Protocol (OData) およびカスタム サービス統合パターンも監視できる必要があります。 財務と運用アプリの管理センターである Microsoft Dynamics Lifecycle Services (LCS) には、管理している環境を正確に表示できることを保証する監視および診断ツールのコレクションが含まれています。 詳細については、 [Lifecycle Services (LCS) の監視および診断ツール](../lifecycle-services/monitoring-diagnostics.md)を参照してください。

一連の定義済 **調整済みの要求** クエリを使用して、問題の未加工ログを取得することができます。 さらに高度な分析を行うためにログをエクスポートすることができます。

追従する監視と診断ポータルでスロットリング活動を表示するには、次の手順に従います。

1. LCS で、適切なプロジェクトを開きます。
2. **環境** セクションで、表示する環境を選択してから **完全な詳細** を選択します。
3. **環境の詳細** ページで、**環境の監視** を選択して、監視および診断ポータルを開きます。 
4. **環境の監視** ページで、**活動** タブを選択して、**未加工ログ** ページを表示します。 
5. クエリ名を選択し、調整されたすべての OData およびカスタム サービス要求の **調整済みの要求** を選択します。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

