---
title: 承認済仕入先の有効日は変更不可能
description: 製品エンティティ別の承認済仕入先リストでは、有効日を変更することはできません
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: cb6dbd134d63daa163261cabdbd7eceb978877ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476832"
---
# <a name="cant-change-the-effective-date-for-an-approved-vendor"></a>承認済仕入先の有効日は変更不可能


## <a name="symptoms"></a>現象

たとえば、ある製品には承認済仕入先があり、有効日は 2018 年 1 月 11 日 (*01/11/2018*)、有効期限は *なし* となっています。 有効日を 2018 年 1 月 10 日 (*01/10/2018*) または 2018 年 1 月 12 日 (*01/12/2018*) に変更しようとすると、次のエラーが表示されます。

> 承認済サプライヤー リスト (PdsApproveVendorList) にレコードを作成することはできません。 '有効期限' の値は、'有効' 値以上である必要があります。

## <a name="resolution"></a>解決策

仕入先の承認期間のみ延長できます。 次のルールが適用されます。

- 有効日を、品目の仕入先の既存のレコード (期間) よりも前に変更するには、新しい期間の有効期限を既存のレコードの有効期限のすべての日付より前にする必要があります。
- 既存の期間より後の日付に有効期限を変更するには、既存のレコードの有効日が最新の有効期限の後にする必要があります。
- 仕入先が承認する合計期間を減らすには、既存のレコードを削除または変更する必要があります。 または、インポート中に **切り捨て** スイッチを使用することもできます。 このスイッチは、品目ごとに承認済仕入先のテーブル内の既存のレコードをすべて削除します。

レコードに有効日が *01/11/2018*、有効期限が *なし* となっている問題の説明で説明されているシナリオでは、有効期限が常にあるという、問題の説明で説明されているシナリオについては、有効日が *01/10/2018* で有効期限が *なし* となっている新規レコードをインポートできます。 ただし、データ管理を通じて有効日が *01/12/2018* に更新されるように期間を短縮することはできません。 この変更は UI を通じて行なわなければなりません。
