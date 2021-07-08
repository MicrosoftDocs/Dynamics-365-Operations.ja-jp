---
title: データベース移動操作ホーム ページ
description: このトピックでは、Lifecycle Services のデータベースの移動機能の使用可能なクイック スタート ガイドおよびチュートリアルへのリンクを示します。
author: laneswenka
ms.date: 06/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 3b71c7930a319f0b1ef09884d2e7e340afe5718b
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216707"
---
# <a name="database-movement-operations-home-page"></a>データベース移動操作ホーム ページ

[!include [banner](../includes/banner.md)]

データベース移動操作は、データ アプリケーション ライフ サイクル管理 (*DataALM* とも呼ばれます) の一部として使用できる一連のセルフ サービスのアクションです。  これらのアクションは、ゴールデン コンフィギュレーション プロモーション、デバッグ/診断、破壊試験、トレーニング目的での全般的な更新などの一般的な実装シナリオで構造化されたプロセスを提供します。

このトピックでは、データベース移動操作を使用して、更新、エクスポート、インポート、およびさまざまなタイプのポイントインタイム復元を実行する方法について説明します。

## <a name="database-movement-scenarios-and-quick-start-guides"></a>データベース移動シナリオとクイック スタート ガイド
次の表に、サポートされているさまざまなシナリオと、各シナリオのクイック スタート ガイドへのリンクを示します。 

| ソース環境 | ターゲット環境 | クイック スタート ガイド | API 経由で使用可能 | チュートリアル 
|---|---|---|---|---|
|実稼働|    サンドボックス|    [データベースの更新](database-refresh.md) | [更新の作成](api/v1/reference-create-refresh.md) | [トレーニング用の更新](dbmovement-scenario-general-refresh.md)<br/>[運用データベースのコピーのデバッグ](dbmovement-scenario-debugdiag.md) |
|サンドボックス|   実稼働| [データベースの更新](database-refresh.md) | サポートされていません | [ゴールデン コンフィギュレーション プロモーション](dbmovement-scenario-goldenconfig.md) |
|サンドボックス|   サンドボックス|    [データベースの更新](database-refresh.md) | [更新の作成](api/v1/reference-create-refresh.md) | [トレーニング用の更新](dbmovement-scenario-general-refresh.md)|
|サンドボックス|   DevTest|    [データベースのエクスポート](export-database.md) | [エクスポートの作成](api/v1/reference-create-export.md) | [標準ユーザー承認テスト (UAT) データベースのコピーのエクスポート](dbmovement-scenario-exportuat.md) |
|DevTest|   サンドボックス|    [データベースのインポート](import-database.md)| サポートされていません | [ゴールデン コンフィギュレーション プロモーション](dbmovement-scenario-goldenconfig.md) |
実稼働| DevTest|    直接サポートされていません | サポートされていません | [標準ユーザー承認テスト (UAT) データベースのコピーのエクスポート](dbmovement-scenario-exportuat.md)を推奨 |
|サンドボックスのポイントインタイム | サンドボックス |[ポイントインタイム復元 (PITR)](database-point-in-time-restore.md) | サポートされていません | [破壊試験](dbmovement-scenario-destructivetests.md) |
|実稼働環境のポイントインタイム| サンドボックス| [サンドボックス環境への生産データベースのポイントインタイム復元](database-pitr-prod-sandbox.md) | サポートされていません | [破壊試験](dbmovement-scenario-destructivetests.md)

> [!IMPORTANT]
> データベース移動の操作は非常に時間のかかる操作です。 これらの操作にかかる時間は、データ量やスキーマの複雑さ、およびエクスポート操作の場合の .bacpac ファイルのように、操作のターゲットがフラット ファイルかどうかによって異なります。 一般に、これらの操作は完了するまでに最大 24 時間かかる場合があり、操作中にキャンセルすることはできません。 さらに、操作のターゲットが、実稼働環境からサンドボックスへのシナリオのような環境である場合、データベースのコピー操作が完了した時、データベースの同期手順が開始される前の不定の時間にオフラインになります。 これは、環境内のエンド ユーザーに警告なしで発生します。 このため、これらのタイプの操作は、営業時間外にスケジュールするのが最善です。

## <a name="database-movement-api"></a>データベース移動 API
データベース移動アプリケーション プログラミング インターフェイス (API) を使用すると、前述のデータベース移動操作のいくつかを ALM プロセス全体に統合できます。 さらに、API を好みのスケジューリング エンジンと共に使用することで、プロセス内で繰り返しを構築し、毎日または要求時に実行することができます。

データベース移動 API の詳細については、次のトピックを参照してください。

* [概要](./api/dbmovement-api-overview.md)
* [バージョン管理とサポート](./api/dbmovement-api-versioning-support.md)
* [認証](./api/dbmovement-api-authentication.md)
* [調整](./api/dbmovement-api-throttling.md)
* [参照](./api/v1/dbmovement-api-v1-overview.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
