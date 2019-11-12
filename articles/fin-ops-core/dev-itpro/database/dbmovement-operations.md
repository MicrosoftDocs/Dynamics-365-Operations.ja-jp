---
title: データベース移動操作ホーム ページ
description: このトピックでは、Lifecycle Services のデータベースの移動機能の使用可能なクイック スタート ガイドおよびチュートリアルへのリンクを示します。
author: laneswenka
manager: AnnBe
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: fb88e9bdc06dbfd3bc78fc36005f1771216e2ec2
ms.sourcegitcommit: d800613020d5548d100c8f240fb81bb6258a3646
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/11/2019
ms.locfileid: "2572677"
---
# <a name="database-movement-operations-home-page"></a>データベース移動操作ホーム ページ

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

データベース移動操作は、データ アプリケーション ライフ サイクル管理 (*DataALM* とも呼ばれます) の一部として使用できる一連のセルフ サービスのアクションです。  これらのアクションは、ゴールデン コンフィギュレーション プロモーション、デバッグ/診断、破壊試験、トレーニング目的での全般的な更新などの一般的な実装シナリオで構造化されたプロセスを提供します。

このトピックでは、データベース移動操作を使用して、更新、エクスポート、インポート、およびさまざまなタイプのポイントインタイム復元を実行する方法について説明します。

## <a name="database-movement-quick-start-guides"></a>データベース移動クイック スタート ガイド
標準またはプレミア受け入れテスト環境で個々の操作を実行する方法を説明します。

* [データベースの更新](database-refresh.md)
* [データベースのエクスポート](export-database.md)
* [データベースのインポート](import-database.md)
* [ポイントインタイム復元 (PITR)](database-point-in-time-restore.md)

## <a name="step-by-step-tutorials"></a>ステップバイステップ チュートリアル
お客様に合わせて DataALM を使用して実装の一般的なシナリオを達成する方法を説明します。

* [トレーニング用の更新](dbmovement-scenario-general-refresh.md)
* [生産データベースのコピーのデバッグ](dbmovement-scenario-debugdiag.md)
* [標準ユーザー受け入れテスト (UAT) データベースのコピーのエクスポート](dbmovement-scenario-exportuat.md)
* [ゴールデン コンフィギュレーション プロモーション](dbmovement-scenario-goldenconfig.md)
* [破壊試験](dbmovement-scenario-destructivetests.md)

## <a name="database-movement-api"></a>データベース移動 API
データベース移動アプリケーション プログラミング インターフェイス (API) を使用すると、前述のデータベース移動操作のいくつかを ALM プロセス全体に統合できます。 さらに、API を好みのスケジューリング エンジンと共に使用することで、プロセス内で繰り返しを構築し、毎日または要求時に実行することができます。

* [概要](./api/dbmovement-api-overview.md)
* [バージョン管理とサポート](./api/dbmovement-api-versioning-support.md)
* [認証](./api/dbmovement-api-authentication.md)
* [調整](./api/dbmovement-api-throttling.md)
* [照会](./api/v1/dbmovement-api-v1-overview.md)

> [!IMPORTANT]
> ポイントインタイム復元の新機能と、RESTful API は、プライベート プレビューです。 プライベート プレビュー プログラムに登録するには、[プライベート プレビュー アンケート](https://aka.ms/SelfServiceDatabaseMovementPreview)に記入してください。
