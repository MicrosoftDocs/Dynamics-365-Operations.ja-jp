---
title: テーブル レコードの有効期間中の業務処理の実行
description: このトピックでは、テーブル レコードの有効期間中に実行できる業務処理に関する情報を提供します。
author: ivanv-microsoft
manager: AnnBe
ms.date: 07/11/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: f3caf7db2165ecdf3ef93c51ba9e8761854e6f87
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369149"
---
# <a name="perform-business-actions-throughout-the-lifecycle-of-table-records"></a>テーブル レコードの有効期間中の業務処理の実行

[!include [banner](../includes/banner.md)]

ビジネス ワークフローの一環として、レコードは定期的に挿入、更新、および削除されます。 システムの動作をカスタマイズするために、最も頻繁に使用される一部のレコード操作にフックすることができます。 たとえば、レコードの追加のフィールドに入力、追加のデータ検証を実行、または関連するテーブルに追加データを挿入することができます。 テーブルで利用できる複数のイベントを使用して、拡張機能を通じてこれらのカスタマイズを実現できます。 コードによって、これらのイベントをサブスクライブすることが、またはイベントの実行の前後にロジックを挿入することができます。

サブスクライブできるイベントの一覧については、[拡張機能とオーバーレイによるカスタマイズ](customization-overlayering-extensions.md#table-extensions)にある「テーブルの拡張機能」セクションを参照してください。
