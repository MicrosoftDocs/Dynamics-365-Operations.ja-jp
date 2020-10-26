---
title: アプリケーション タイプ
description: アプリケーションの実行時のインスタンスを表します。
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: b6f75076a6e263542542d05df72eb367c245f8a7
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983965"
---
# <a name="application-type"></a>アプリケーション タイプ

[!include [banner](../../../../includes/banner.md)]

アプリケーションの実行時のインスタンスを表します。

### <a name="hierarchy"></a>階層

申請 <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [minVersion](services-application-iapplication.md#minversion)

### <a name="methods"></a>メソッド

* [appInit](services-application-iapplication.md#appinit)

## <a name="properties"></a>プロパティ

### <a name="minversion"></a>minVersion

minVersion: string (省略可) 

このコンポーネントで必要な最小プラットフォーム バージョンを示すオプション マーカーです。 これが指定され、プラットフォームの以前のバージョンへのコンポーネントの読み込みが試行されるとき、対応するワークスペースは読み込まれず、ユーザーはプラットフォームの新しいバージョンのインストールを指示されます。


## <a name="methods"></a>メソッド

### <a name="appinit"></a>appInit


appInit(metadata: [ApplicationMetadata](services-application-iapplicationmetadata.md)): any

このメソッドは、アプリケーションが実行される時点で呼び出され、アプリケーション メタデータのインスタンスが読み込まれます。
渡されたメタデータは、このメソッドが戻る前に動作を変更するために変更できます。


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| metadata|[ApplicationMetadata](services-application-iapplicationmetadata.md)||

#### <a name="returns-any"></a>any を返します

