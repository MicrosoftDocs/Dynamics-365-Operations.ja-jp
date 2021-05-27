---
title: 完了報告の取消によって、予期しないオープン トランザクションが作成される
description: マーキングが設定されている完了報告を取り消すと、取り消された数量の在庫分析コードが取り消されたトランザクションと同じオープン トランザクションが作成されます。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026689"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a>完了報告の取消によって、予期しないオープン トランザクションが作成される

KB 番号: 4612469

## <a name="symptoms"></a>現象

マーキングが設定されている完了報告を取り消すと、システムが、取り消された数量の在庫分析コードが取り消されたトランザクションと同じオープン トランザクションを作成します。

## <a name="resolution"></a>解像度

完了レポートの操作を取り消す場合、在庫分析コードは生産仕訳帳から初期化されます。 したがって、バッチ番号が取得されます。 マーキングのため、販売注文トランザクションはバッチ番号を継承します。

完了レポートが転記される際に分析コードをリセットできます。
