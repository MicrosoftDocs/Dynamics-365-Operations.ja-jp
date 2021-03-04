---
title: アプリケーション タイプ
description: アプリケーションの実行時のインスタンスを表します。
author: robinarh
manager: AnnBe
ms.date: 08/01/2017
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
ms.openlocfilehash: 1066ae3b0689169cfb2836cecfb145e99f83174a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685427"
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



[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]