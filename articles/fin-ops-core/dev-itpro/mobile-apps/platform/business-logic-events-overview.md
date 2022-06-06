---
title: ビジネス ロジック イベント
description: ビジネス ロジックで実行されるコードは、ページ、アクション、およびコントロールのメタデータにランタイム変更を加えることができます。
author: tonyafehr
ms.date: 05/24/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.custom:
- "255544"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: 16065f4a5d6c2d937ebfaa8b0d6e66164d63acc7
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811589"
---
# <a name="business-logic-events"></a>ビジネス ロジック イベント

[!include [banner](../../includes/banner.md)]
[!include [mobile app deprecated](../../includes/mobile-app-deprecation-banner.md)]

モバイル ワークスペースのビジネス ロジック イベントは、開発者が能力を高めるためにワークスペースの構成を指定する場所を提供し、業務シナリオ固有の動作を実装します。 モバイル アプリのプロセスで、すべてのモバイル ビジネス ロジックを実行した場合、ビジネス ロジック実行フローは Operations モバイル アプリ フレームワークによって制御されます。 

ビジネス ロジックで実行されるコードは、ページ、アクション、およびコントロールのメタデータにランタイム変更を加えることができます。 これらのランタイムの変更は、アプリにキャッシュされている静的メタデータをオーバーレイしますが、変更はキャッシュされた静的メタデータを直接変更するものではなく、サーバーに格納されている静的メタデータにも影響しません。 これらのランタイム変更は、アプリケーションが終了するまで続きます。 

アプリケーションのビジネス ロジックで実行されるコードは、アプリケーションに格納されているビジネス データにランタイム変更を加えることができます。 これらの変更 (正しいプラクティスに従って実行される場合) は、アプリ内の他のビジネス データとして通常のデータ処理フレームワークに参加します。 これは、オフライン優先機能とフレームワークによって提供される非同期保存ビヘイビアーに従うことを意味します。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
