---
title: 計画オーダーの確定時に仕入先が指定されていない場合
description: 計画オーダーを確定しようとすると、仕入先が指定されていないというエラー メッセージが表示されます。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4d523d57a862f67fcd40edd60a0fabf40ea7dabcf058f2d11af1fe003c9e304b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741983"
---
# <a name="vendor-isnt-specified-when-planned-orders-are-firmed"></a>計画オーダーの確定時に仕入先が指定されていない場合

エラーコード: SYS23532

## <a name="symptoms"></a>現象

計画オーダーを確定しようとする際に、次のエラー メッセージが表示されます:

> 仕入先が指定されていません

## <a name="resolution"></a>解決策

仕入先を指定するには、次の手順を実行します。

1. 仕入先が欠落している計画オーダーを開きます。
1. **計画済供給** クイックタブの、**仕入先** フィールドで、仕入先を選択します。
