---
title: 在庫ブロックの作成および管理
description: このトピックでは、在庫ブロックを使用して、現物手持在庫が他の元伝票に引当されないようにする方法を説明します。
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bad7d4e5794dc543bd750912ef0d3e4460e611b1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572844"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>在庫ブロックの作成および管理

[!include [banner](../../includes/banner.md)]

このトピックでは、在庫ブロックを使用して、現物手持在庫が他の元伝票に引当されないようにする方法を説明します。 このトピックの手順を開始する前に、使用可能な現物手持在庫の品目が必要です。

## <a name="block-inventory"></a>在庫のブロック

在庫がブロックされるように在庫ブロック レコードを作成するには、次の手順に従います。

1. **在庫管理\>定期処理タスク\>在庫ブロック** の順にクリックします。
1. アクション ウィンドウで、**新規** を選択します。
1. 新しいブロック レコードのヘッダーで、**品目番号** フィールドにブロックする品目を設定し、説明を入力します。
1. **全般** クイック タブの **数量** フィールドに、ブロックする品目の数を入力します。
1. **在庫分析コード** クイック タブで、ブロックする品目が現在保管されているサイトと倉庫を指定します。
1. アクション ウィンドウで、**保存** を選択します。

## <a name="update-the-conditions-of-the-inventory-blocking"></a>在庫ブロックの条件の更新

在庫ブロック レコードを更新するには、次の手順に従います。

1. **在庫管理\>定期処理タスク\>在庫ブロック** の順にクリックします。
1. 一覧ペインで、関連するブロック レコードを選択します。
1. 必要に応じてレコードを編集します。 たとえば、**予定日** フィールドの値を変更して、ブロックされた在庫の引当可能日を指定することができます。 **入庫予定** オプションが選択されている場合、予想されるトランザクションに日付が表示されます。 (ブロック レコードを手動で作成する場合、既定で **入庫予定** オプションが選択されます。)
1. アクション ウィンドウで、**保存** を選択します。

## <a name="unblock-inventory"></a>在庫のブロック解除

在庫がブロック解除されるように在庫ブロック レコードを削除するには、次の手順に従います。

1. **在庫管理\>定期処理タスク\>在庫ブロック** の順にクリックします。
1. 一覧ペインで、関連するブロック レコードを選択します。
1. アクション ウィンドウで **削除** を選択します。
1. 操作を確認するように求められます。 **はい** を選択して続行します。
1. ページを閉じます。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
