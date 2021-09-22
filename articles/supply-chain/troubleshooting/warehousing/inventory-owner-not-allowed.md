---
title: 移動の処理時に在庫所有者が許可されない
description: 「在庫所有者 %1 は許可されません」というエラーが表示される場合があります。 Warehouse Management プロセスでは、法人によって所有されている在庫のみがサポートされています。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4ee29cfc7bad990cd1ee5deaa98fca217af772ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476852"
---
# <a name="inventory-owner-not-allowed-when-processing-movements-in-the-warehouse-app"></a>Warehouse アプリで、移動の処理時に在庫所有者が許可されない

## <a name="symptoms"></a>現象

Warehouse Management モバイル アプリで、移動の処理を行うと、次のエラー メッセージが表示されることがあります。

> このプロセスでは、在庫所有者 %1 は許可されません。

## <a name="cause"></a>原因

これは、Warehouse Management モバイル アプリを使用して移動を行うときに、**所有者** 追跡用分析コードが見つからないために生じます。 Supply Chain Management クライアントからの通常の在庫移動仕訳帳が意図したとおりに機能し、**所有者** 分析コードが入力されている場合にのみ転記できます。

## <a name="resolution"></a>解決策

Microsoft は、この問題を評価し、それが機能上の制限であることを確認しました。 現在、倉庫管理プロセスでは、法人によって所有されている在庫のみがサポートされています。
