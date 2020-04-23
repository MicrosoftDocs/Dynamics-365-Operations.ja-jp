---
title: 返品による梱包明細票の更新
description: 返品品目を在庫に入庫する前に、それらの品目が属する注文の梱包明細を更新する必要があります。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 446306237492df22e98dc1efee2bc1542cdab1ea
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202195"
---
# <a name="packing-slip-updates-for-returns"></a>返品による梱包明細票の更新  

[!include [banner](../includes/banner.md)]


返品品目を在庫に入庫する前に、それらの品目が属する注文の梱包明細を更新する必要があります。 請求書更新プロセスが財務トランザクションに対する更新であるのと同様に、梱包明細更新プロセスは在庫レコードの現物更新であり、在庫の変更をコミットすることを意味します。 返品の場合、処分アクションに割り当てられる手順は、梱包明細の更新中に実行されます。

梱包明細の更新は、着荷仕訳帳または返品注文で処理できます。

梱包明細の転記プロセスの一環として、顧客の出荷ドキュメントに記載されている梱包明細参照番号を注文明細行に関連付けることができます。 このアソシエーションはオプションであり、また参照専用です。 これによってトランザクションの更新は行われません。

予定の返品品目のうち到着してないものがある場合、梱包明細の更新対象には入庫された数量だけを含めることとします。 残りの返品荷物が到着するまで残りの品目は注文に残します。

検査担当者が在庫内のどこに品目が保管されているかわからない場合など、品目が検査から出荷および入荷部門に返送されてきた場合、対応する梱包明細を更新して、検査の結果として指定される廃棄コードを正しく登録し、それに従って行動する必要があります。

販売契約書に基づく返品品目の梱包明細を更新すると、数量または金額の変更を反映するために、その品目の販売契約書の確約が自動的に更新されます。 

## <a name="see-also"></a>参照

[返品による請求書更新の実行](perform-invoice-updates-for-returns.md)

  


