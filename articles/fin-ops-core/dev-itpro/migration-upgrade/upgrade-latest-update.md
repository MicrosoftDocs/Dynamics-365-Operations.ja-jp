---
title: Finance and Operations で最新の更新プログラムに移行するためのプロセス
description: このトピックでは、Finance and Operations の最新の更新バージョンに移行するプロセスについて説明します。
author: laneswenka
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 102343
ms.assetid: e48d7424-371a-49ee-882c-07b7ceb00183
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: e55b2989c807b827d80b80e96e63eae5c2f7f72d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686626"
---
# <a name="process-for-moving-to-the-latest-update-of-finance-and-operations"></a>Finance and Operations で最新の更新プログラムに移行するためのプロセス

[!include [banner](../includes/banner.md)]

このトピックでは、Finance and Operations の最新のリリースに更新またはアップグレードするプロセスについて説明します。 プロセス全体とサポートされるシナリオを説明しますが、プロセスの各ステップに関する詳細な指示は提示しません。

Finance and Operations の各リリースの内容の詳細については、[Finance and Operations ホーム ページの新機能と変更点](../../fin-ops/get-started/whats-new-changed.md) を参照してください。

1 つのバージョンのサービス更新の詳細については、[1 つのバージョンのサービス更新の概要](../lifecycle-services/oneversion-overview.md) を参照してください。

> [!Note]
> Microsoft Dynamics AX 2012 から Finance and Operations へのアップグレードを検討している方は、[AX 2012 から Finance and Operations へのアップグレード](upgrade-overview-2012.md) を参照してください。

## <a name="definitions"></a>定義

- **アップグレード** – バージョン 8.0 より前のソース環境では、Finance and Operations のある公式リリースから次のリリースに移行するプロセス。 例としては、7.1 から 7.3 または 7.3 から 10.0.1 への移行があります。 プロセスには、無料サンド ボックス環境、コード アップグレード、およびデータ アップグレードの設定が含まれます。
- **更新** – バージョン 8.0 以降のソース環境で、バイナリ パッケージを環境に適用し、Finance and Operations のある公式リリースから次のリリースに移行するプロセス。 このプロセスには、低いダウンタイム要件があり、データ アップグレードは含まれません。

## <a name="paths-to-one-version"></a>1 つのバージョンへのパス
<img src="../migration-upgrade/media/OneVersion_Paths.png" width="600px" alt="Paths to One Version" />
Finance and Operations の最新バージョンを導入するには 3 つの基本パスがあります。  各パスは、詳細な手順へのリンクとともに以下で参照されます。

### <a name="self-service-upgrade"></a>セルフサービス アップグレード
*適用可能な開始バージョン: Microsoft Dynamics 365 for Finance and Operations 7.0 (RTW)、7.1 (1611)、7.2 (2017 年 7 月)、7.3。*<br/>
*スコープ: 複雑*<br/>
このパスには拡張機能へのコード リファクタリング、そして DevTest、サンドボックス、そして最終的には実稼働環境でのデータ アップグレードが含まれます。 

[最新バージョンへのセルフサービス アップグレード](../migration-upgrade/self-service-upgrade.md)

### <a name="rebuild-and-update"></a>再構築と更新
*適用可能な開始バージョン: Microsoft Dynamics 365 for Finance and Operations 8.0*<br/>
*スコープ: 中程度*<br/>
このパスは Microsoft X++ 修正プログラムを削除し、マージされた更新プログラム パッケージを作成します。

[バージョン 8.0 から 10.0.X への環境の更新](../migration-upgrade/appupdate-80-81.md)

### <a name="automatic-update"></a>自動更新
*適用可能な開始バージョン: Finance and Operations 8.1.0+*<br/>
*スコープ: 簡易*<br/>
このパスはプロジェクトを継続的に更新するように構成します。

[Lifecycle Services (LCS) によるサービスの更新の構成](../lifecycle-services/configure-service-updates.md)

