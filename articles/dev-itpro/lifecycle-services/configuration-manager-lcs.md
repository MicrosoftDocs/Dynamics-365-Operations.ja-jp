---
title: Lifecycle Services (LCS) 内での構成マネージャー
description: Microsoft Dynamics Lifecycle Services の構成マネージャー (ベータ) 機能を使用すると、Microsoft Dynamics AX 2012 R3 の 1 つのインスタンスから他のインスタンスに構成をコピーすることができます。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012, Operations
ms.custom: 62753
ms.assetid: fab3f6cf-03db-47c7-90fb-f8bc03dacf49
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 8af724108aabb477625df02a618a981858978f94
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552506"
---
# <a name="configuration-manager-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) 内での構成マネージャー

[!include [banner](../includes/banner.md)]

構成マネージャーを使用すると、以下の条件を満たす Dynamics AX 2012 R3 環境間で相互にコピーを実行することができます。
-   Lifecycle Services プロジェクトの一部として管理
-   システム診断の実行
-   データのインポート/エクスポート フレームワークの実行中

| **重要**                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| この機能は、運用上の用途ではサポートされて**いません**。  構成マネージャー (ベータ) は、環境内のデータのインポート/エクスポート フレームワークからのエンティティに依存します。 これらのエンティティには現在 AX 2012 R3 のすべての機能が含まれていないため、一部の構成データは環境間でコピーされません。 |

詳細については、以下を参照してください。
-   [構成マネージャーの設定 (Lifecycle Services、LCS)](set-up-configuration-manager-lcs.md)
-   [コンフィギュレーションのコピー (Lifecycle Services、LCS)](copy-configuration-lcs.md)





