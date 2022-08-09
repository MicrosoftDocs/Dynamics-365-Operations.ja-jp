---
title: 財務と運用の最新更新プログラムへの移行の処理
description: この記事では、財務と運用の最新の更新プログラムに移行するプロセスについて説明します。
author: laneswenka
ms.date: 11/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 102343
ms.assetid: e48d7424-371a-49ee-882c-07b7ceb00183
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: b3a612ed8561a03d8cd795a861ac5e388a65998f
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124008"
---
# <a name="process-for-moving-to-the-latest-update-of-finance-and-operations"></a>財務と運用の最新更新プログラムへの移行の処理

[!include [banner](../includes/banner.md)]

この記事では、財務と運用の最新のリリースに更新またはアップグレードするプロセスについて説明します。 プロセス全体とサポートされるシナリオを説明しますが、プロセスの各ステップに関する詳細な指示は提示しません。

財務と運用の各リリースの内容については、[財務と運用ホーム ページの新機能および変更された機能](../../fin-ops/get-started/whats-new-changed.md)を参照してください。

1 つのバージョンのサービス更新の詳細については、[1 つのバージョンのサービス更新の概要](../lifecycle-services/oneversion-overview.md) を参照してください。

> [!Note]
> Microsoft Dynamics AX 2012 から財務と運用へのアップグレードを検討している方は、[AX 2012 から財務と運用へのアップグレード](upgrade-overview-2012.md)をご覧ください。

## <a name="definitions"></a>定義

- **アップグレード**: バージョン 8.0 より前のソース環境で、財務と運用のある公式リリースから次のリリースに移行するプロセス。 例としては、7.1 から 7.3 または 7.3 から 10.0.1 への移行があります。 プロセスには、無料サンド ボックス環境、コード アップグレード、およびデータ アップグレードの設定が含まれます。
- **更新**: バージョン 8.0 以降のソース環境でバイナリ パッケージを環境に適用し、財務と運用のある公式リリースから次のリリースに移行するプロセス。 このプロセスには、低いダウンタイム要件があり、データ アップグレードは含まれません。 詳細については、この記事の後半の[再構築と更新](upgrade-latest-update.md#rebuild-and-update)セクションを参照してください。

## <a name="paths-to-one-version"></a>1 つのバージョンへのパス
<img src="../migration-upgrade/media/OneVersion_Paths.png" width="600px" alt="Paths to One Version" />
財務と運用の最新バージョンを導入するには 3 つの基本パスがあります。  各パスは、詳細な手順へのリンクとともに以下で参照されます。

### <a name="self-service-upgrade"></a>セルフサービス アップグレード
*適用可能な開始バージョン: Microsoft Dynamics 365 財務と運用 7.0 (RTW)、7.1 (1611)、7.2 (2017 年 7 月)、7.3。*<br/>
*スコープ: 複雑*<br/>
このパスには拡張機能へのコード リファクタリング、そして DevTest、サンドボックス、そして最終的には運用環境でのデータ アップグレードが含まれます。 

> [!NOTE]
> このプロセスは非推奨となりました。

[最新バージョンへのセルフサービス アップグレード](../migration-upgrade/self-service-upgrade.md)

### <a name="rebuild-and-update"></a>再構築と更新
*適用可能な開始バージョン: Microsoft Dynamics 365 財務と運用 8.0*<br/>
*スコープ: 中程度*<br/>
このパスは Microsoft X++ 修正プログラムを削除し、マージされた更新プログラム パッケージを作成します。

[バージョン 8.0 から 10.0.X への環境の更新](../migration-upgrade/appupdate-80-81.md)

### <a name="automatic-update"></a>自動更新
*適用可能な開始バージョン: Finance and Operations 8.1.0+*<br/>
*スコープ: 簡易*<br/>
このパスはプロジェクトを継続的に更新するように構成します。

[Lifecycle Services (LCS) によるサービスの更新の構成](../lifecycle-services/configure-service-updates.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

