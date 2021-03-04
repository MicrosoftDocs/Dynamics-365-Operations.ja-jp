---
title: アプリケーション モジュール
description: アプリケーションとはその内部で使用される概念とデータの周りにサンドボックス化されたランタイム実行の単位です。
author: robinarh
manager: AnnBe
ms.date: 09/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: b49766eab69b02f6bf6c9207d3e883b0fb29572b
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130511"
---
# <a name="application-module"></a>アプリケーション モジュール

[!include [banner](../../../../includes/banner.md)]

アプリケーションとはその内部で使用される概念とデータの周りにサンドボックス化されたランタイム実行の単位です。 各アプリケーションは、ページ、アクション、データ クエリおよびそれらを結合するロジックで構成されています。 アプリケーションは主に宣言型メタデータ システムで記述され、付随的な拡張モデルを持つことができます。

アプリケーションの付随的な拡張は、一般に指定されたエントリポイントである [主な関数](#main) を持つスクリプト モジュールで定義されます。これにより、付随的なロジックをアプリケーション ライフ サイクルと統合できます。

## <a name="index"></a>指数

### <a name="types"></a>種類

* [アプリケーション](../interfaces/services-application-iapplication.md)
* [ApplicationMetadata](../interfaces/services-application-iapplicationmetadata.md)

### <a name="functions"></a>関数

* [main](services-application.md#main)

## <a name="types"></a>種類


### <a name="application"></a>申請

#### <a name="hierarchy"></a>階層

申請 <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [minVersion](../interfaces/services-application-iapplication.md#minversion) |minVersion: string (省略可)  <br>|このコンポーネントで必要な最小プラットフォーム バージョンを示すオプション マーカーです。 この値が指定され、プラットフォームの以前のバージョンでコンポーネントの読み込みが試行されるとき、対応するワークスペースは読み込まれず、ユーザーはプラットフォームの新しいバージョンのインストールを指示されます。<br>  |

#### <a name="methods"></a>メソッド

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [appInit](../interfaces/services-application-iapplication.md#appinit) |appInit(metadata: [ApplicationMetadata](../interfaces/services-application-iapplicationmetadata.md)): any|このメソッドは、アプリケーションが実行される時点で呼び出され、アプリケーション メタデータのインスタンスが読み込まれます。 渡されたメタデータは、このメソッドが戻る前に動作を変更するために変更できます。<br>  |


### <a name="applicationmetadata"></a>ApplicationMetadata

#### <a name="hierarchy"></a>階層

ApplicationMetadata <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [ColorName](../interfaces/services-application-iapplicationmetadata.md#colorname) |ColorName: 文字列 (オプション)  <br>|アプリケーションのテーマ色。<br>  |
| [Configs](../interfaces/services-application-iapplicationmetadata.md#configs) |Configs: [名前: 文字列]: 任意 (オプション)  <br>|アプリケーションは作成者またはリソース プロバイダーにより指定された名前付き構成のセットを持つことができます<br>  |
| [説明](../interfaces/services-application-iapplicationmetadata.md#description) |説明:文字列 (オプション)  <br>|アプリケーションの説明<br>  |
| [IconName](../interfaces/services-application-iapplicationmetadata.md#iconname) |IconName: 文字列 (オプション)  <br>|アプリケーションの代表的なアイコン<br>  |
| [ID](../interfaces/services-application-iapplicationmetadata.md#id) |ID: 文字列 <br>|アプリケーションの一意の識別子<br>  |
| [肩書き](../interfaces/services-application-iapplicationmetadata.md#title) |タイトル: 文字列 <br>|アプリケーションのタイトル。<br>  |

## <a name="functions"></a>関数


### <a name="main"></a>main
main(metadataService: [MetadataService](../interfaces/services-business-logic-services-imetadataservice.md), dataService: [DataService](../interfaces/services-business-logic-services-idataservice.md), cacheService: [CacheService](../interfaces/services-business-logic-services-icacheservice.md), asyncService: [AsyncService](../interfaces/services-business-logic-services-iasyncservice.md)): [Application](../interfaces/services-application-iapplication.md)

ビジネス ロジック モジュールの main メソッド。 各ビジネス ロジック モジュール (JavaScript ファイルとして) では、1 つの主要な方法を記述する必要があります。 このメソッドは、モジュールが読み込まれ、初期化されるときに呼び出されます。 メソッドは、このモジュールから実行するコンポーネントを返す必要があります。


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| metadataService|[MetadataService](../interfaces/services-business-logic-services-imetadataservice.md)||
| dataService|[DataService](../interfaces/services-business-logic-services-idataservice.md)||
| cacheService|[CacheService](../interfaces/services-business-logic-services-icacheservice.md)||
| asyncService|[AsyncService](../interfaces/services-business-logic-services-iasyncservice.md)||

#### <a name="returns-application"></a>[Application](../interfaces/services-application-iapplication.md) を返します

