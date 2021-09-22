---
title: モバイル アプリで ID をスキャンする場合にライセンス プレートが無効
description: Warehouse Management モバイル アプリでライセンス プレート ID をスキャンすると、エラー メッセージが表示されます。 このページでは、問題を解決する方法について説明します。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b7cd6a2223dfe2c7be5324e3d2ca2ab3e9fb87a9
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476853"
---
# <a name="invalid-license-plate-error-when-scanning-license-plate-id-in-the-mobile-app"></a>モバイル アプリでライセンス プレート ID をスキャンする場合にライセンス プレートが無効であるとのエラーが出る

## <a name="symptoms"></a>現象

Warehouse Management モバイル アプリでライセンス プレート ID をスキャンすると、このエラー メッセージが表示されます。

> 無効なライセンス プレートです。

## <a name="resolution"></a>解決策

ライセンス プレート ID がライセンス プレート テーブルに存在し、ライセンス プレートの品目と数量が使用可能である (つまりブロックされていない) ことを確認してください。
