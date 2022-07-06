---
title: テーブル レコードの有効期間中の業務処理の実行
description: この記事では、テーブル レコードの有効期間中に実行できる業務処理に関する情報を提供します。
author: ivanv-microsoft
ms.date: 07/11/2017
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: 5a80f9a1a3ef643ab7c364ccaf36b53fc921297e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866813"
---
# <a name="perform-business-actions-throughout-the-lifecycle-of-table-records"></a>テーブル レコードの有効期間中の業務処理の実行

[!include [banner](../includes/banner.md)]

ビジネス ワークフローの一環として、レコードは定期的に挿入、更新、および削除されます。 システムの動作をカスタマイズするために、最も頻繁に使用される一部のレコード操作にフックすることができます。 たとえば、レコードの追加のフィールドに入力、追加のデータ検証を実行、または関連するテーブルに追加データを挿入することができます。 テーブルで利用できる複数のイベントを使用して、拡張機能を通じてこれらのカスタマイズを実現できます。 コードによって、これらのイベントをサブスクライブすることが、またはイベントの実行の前後にロジックを挿入することができます。

サブスクライブできるイベントの一覧については、[拡張機能とオーバーレイによるカスタマイズ](customization-overlayering-extensions.md#table-extensions)にある「テーブルの拡張機能」セクションを参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]