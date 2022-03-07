---
title: テーブル レコードの有効期間中の業務処理の実行
description: このトピックでは、テーブル レコードの有効期間中に実行できる業務処理に関する情報を提供します。
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
ms.openlocfilehash: fca8efe82343c3bd9dc040874e68a10ec6497585
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782907"
---
# <a name="perform-business-actions-throughout-the-lifecycle-of-table-records"></a>テーブル レコードの有効期間中の業務処理の実行

[!include [banner](../includes/banner.md)]

ビジネス ワークフローの一環として、レコードは定期的に挿入、更新、および削除されます。 システムの動作をカスタマイズするために、最も頻繁に使用される一部のレコード操作にフックすることができます。 たとえば、レコードの追加のフィールドに入力、追加のデータ検証を実行、または関連するテーブルに追加データを挿入することができます。 テーブルで利用できる複数のイベントを使用して、拡張機能を通じてこれらのカスタマイズを実現できます。 コードによって、これらのイベントをサブスクライブすることが、またはイベントの実行の前後にロジックを挿入することができます。

サブスクライブできるイベントの一覧については、[拡張機能とオーバーレイによるカスタマイズ](customization-overlayering-extensions.md#table-extensions)にある「テーブルの拡張機能」セクションを参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]