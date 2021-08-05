---
title: ビジネス ロジック イベント
description: ビジネス ロジックで実行されるコードは、ページ、アクション、およびコントロールのメタデータにランタイム変更を加えることができます。
author: robinarh
ms.date: 08/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.custom:
- "255544"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: b835445ad9b41bd7c92056487d1ae17a7d6a69d9
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/03/2021
ms.locfileid: "6336231"
---
# <a name="business-logic-events"></a>ビジネス ロジック イベント

[!include [banner](../../includes/banner.md)]

モバイル ワークスペースのビジネス ロジック イベントは、開発者が能力を高めるためにワークスペースの構成を指定する場所を提供し、業務シナリオ固有の動作を実装します。 モバイル アプリのプロセスで、すべてのモバイル ビジネス ロジックを実行した場合、ビジネス ロジック実行フローは Operations モバイル アプリ フレームワークによって制御されます。 

ビジネス ロジックで実行されるコードは、ページ、アクション、およびコントロールのメタデータにランタイム変更を加えることができます。 これらのランタイムの変更は、アプリにキャッシュされている静的メタデータをオーバーレイしますが、変更はキャッシュされた静的メタデータを直接変更するものではなく、サーバーに格納されている静的メタデータにも影響しません。 これらのランタイム変更は、アプリケーションが終了するまで続きます。 

アプリケーションのビジネス ロジックで実行されるコードは、アプリケーションに格納されているビジネス データにランタイム変更を加えることができます。 これらの変更 (正しいプラクティスに従って実行される場合) は、アプリ内の他のビジネス データとして通常のデータ処理フレームワークに参加します。 これは、オフライン優先機能とフレームワークによって提供される非同期保存ビヘイビアーに従うことを意味します。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]