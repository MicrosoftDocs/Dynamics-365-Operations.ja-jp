---
title: 顧客の与信グループ
description: このトピックでは、顧客の与信グループに関する情報を提供します。
author: JodiChristiansen
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0815aa41b034d8ba5c9b09f4003ff3df7311190a
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735495"
---
# <a name="customer-credit-groups"></a>顧客の与信グループ

[!include [banner](../includes/banner.md)]

与信限度額を共有する顧客のグループを定義できます。 顧客請求書勘定で定義された個々の与信限度額も考慮されます。

顧客の与信グループのメンバーは、異なる法人から選択できます。 顧客の与信グループに含まれる顧客リストに顧客を追加すると、各顧客の与信限度額の有効期限は、グループに割り当てられている有効期限に変更されます。

顧客の与信グループは、**顧客の与信グループ** ページ (**与信管理\>顧客の与信グループ\>顧客の与信グループ**) で設定できます。

1. **グループ番号** フィールドと **説明** フィールドに、グループの ID と説明を入力します。
2. **与信限度額** と **通貨** フィールドに、グループのメンバーの与信限度額がシステムによってチェックされるときに使用する与信限度額と通貨を入力します。
3. **与信限度額の有効期限** フィールドに、与信限度額の期限が切れる日付を入力します。 顧客の与信グループには有効期限が必要です。

顧客の与信グループの設定を完了した後、法人と顧客 ID を指定することにより、顧客を追加することができます。 顧客の与信グループに新しい顧客を追加すると、すべての法人間で同じ顧客 ID が検索され、顧客の与信グループにその顧客を追加するように求められます。

**指定の期間に達している残高** メニューを使用して、顧客の与信グループに含まれるすべての請求書の顧客のエイジング残高の詳細を表示します。 **エイジング残高** ページには、請求書の顧客 ID の指定の期間に達している残高の概要が表示されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
