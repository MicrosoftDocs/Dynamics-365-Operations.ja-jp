---
title: Lifecycle Services の設定の概要
description: Microsoft Dynamics Lifecycle Services の構成マネージャー (ベータ) 機能を使用すると、Microsoft Dynamics AX 2012 R3 の 1 つのインスタンスから他のインスタンスに構成をコピーすることができます。
author: RobinARH
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012, Operations
ms.custom: 62753
ms.assetid: fab3f6cf-03db-47c7-90fb-f8bc03dacf49
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 0f8c9bb40746bbd1ff0f5956999e707cee5e7f6b
ms.sourcegitcommit: 4ff8c2c2f3705d8045df66f2c4393253e05b49ed
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864316"
---
# <a name="configuration-in-lifecycle-services-overview"></a>Lifecycle Services の設定の概要

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





