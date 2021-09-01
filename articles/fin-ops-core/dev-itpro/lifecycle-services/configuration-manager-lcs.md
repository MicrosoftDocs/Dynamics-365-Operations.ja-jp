---
title: Lifecycle Services の設定の概要
description: 構成マネージャー (ベータ) 機能を使用すると、Microsoft Dynamics AX 2012 R3 の 1 つのインスタンスから他のインスタンスに構成をコピーすることができます。
author: RobinARH
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom:
- "62753"
- intro-internal
ms.assetid: fab3f6cf-03db-47c7-90fb-f8bc03dacf49
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 101fda96ca8aef8ec12f7e57479b306da80d72bcbacbc0e542e2f52f906aafc5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769842"
---
# <a name="configuration-in-lifecycle-services-overview"></a>Lifecycle Services の設定の概要

[!include [banner](../includes/banner.md)]

構成マネージャーを使用すると、以下の条件を満たす Dynamics AX 2012 R3 環境間で相互にコピーを実行することができます。
-   Lifecycle Services プロジェクトの一部として管理
-   システム診断の実行
-   データのインポート/エクスポート フレームワークの実行中

> [!IMPORTANT]
> この機能は、運用上の用途ではサポートされて **いません**。 構成マネージャー (ベータ) は、環境内のデータのインポート/エクスポート フレームワークからのエンティティに依存します。 これらのエンティティには現在 AX 2012 R3 のすべての機能が含まれていないため、一部の構成データは環境間でコピーされません。

詳細については、以下を参照してください。
-   [構成マネージャーの設定](set-up-configuration-manager-lcs.md)
-   [構成マネージャーを使用して構成をコピーする](copy-configuration-lcs.md)







[!INCLUDE[footer-include](../../../includes/footer-banner.md)]