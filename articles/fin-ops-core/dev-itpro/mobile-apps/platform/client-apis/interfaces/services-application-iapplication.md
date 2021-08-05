---
title: アプリケーション タイプ
description: アプリケーションの実行時のインスタンスを表します。
author: robinarh
ms.date: 08/01/2017
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.openlocfilehash: 013693e26961533b19456c4486a3eeaa5f73f7c3
ms.sourcegitcommit: ff5e892a91a1585472af2191ae45d6291cceb7f6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/24/2021
ms.locfileid: "6661514"
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