---
title: アプリケーション タイプ
description: アプリケーションの実行時のインスタンスを表します。
author: jasongre
ms.date: 05/24/2022
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: jasongre
ms.openlocfilehash: 9c67da21f4d98c2f2d0ae820123bfeb53a9b7b7b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268637"
---
# <a name="application-type"></a>アプリケーション タイプ

[!include [banner](../../../../includes/banner.md)]
[!include [mobile app deprecated](../../../../includes/mobile-app-deprecation-banner.md)]

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
