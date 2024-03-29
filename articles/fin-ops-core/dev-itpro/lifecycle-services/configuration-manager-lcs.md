---
title: Lifecycle Services の設定の概要
description: 構成マネージャー (ベータ) 機能を使用すると、Microsoft Dynamics AX 2012 R3 の 1 つのインスタンスから他のインスタンスに構成をコピーすることができます。
author: gianugo
ms.date: 07/23/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: gianura
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.custom: 62753,  ""intro-internal
ms.assetid: fab3f6cf-03db-47c7-90fb-f8bc03dacf49
ms.openlocfilehash: bc1a72e385005f153992c6506ac4110e2dcc23cd
ms.sourcegitcommit: 78d41eeef0a8a8e94ed502bd89778414231a31ae
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/17/2022
ms.locfileid: "9305144"
---
# <a name="configuration-in-lifecycle-services-overview"></a>Lifecycle Services の設定の概要

[!include [banner](../includes/banner.md)]
[!include [LCS deprecation](../includes/lcs-deprecation.md)]

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
