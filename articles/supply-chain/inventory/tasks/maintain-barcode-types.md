---
title: バーコード タイプの管理
description: この手順は、ピッキング リスト レポートの一部として使用される、新しいバー コードの定義を設定する方法を示します。
author: yufeihuang
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b689d1fc85d59ac87efa1903fd7122ae5ff011da
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571116"
---
# <a name="maintain-bar-code-types"></a>バーコード タイプの管理

[!include [banner](../../includes/banner.md)]

この手順は、ピッキング リスト レポートの一部として使用される、新しいバー コードの定義を設定する方法を示します。 デモ データ会社 USMF または独自のデータを使用してこの手順の説明を見ることができます。 USMF を使用すると、表示される例の値を使用できます。 通常、これらのタスクを実施するのは、倉庫マネージャーです。

1. **バー コード** に移動します。
1. **新規** を選択します。
1. **バー コードを設定** フィールドに値をタイプします。
1. **説明** フィールドで、値を入力します。
1. **バー コード タイプ** フィールドにオプションを選択します。
    * USMF を使用している場合、「Code 39」を選択できます。
1. **マスク ID** フィールドで、バーコード マスク ID を指定します。 バーコード マスクは、バーコードを作成したり、販売時点管理 (POS) システムでスキャンされたバーコードをすばやく識別するのに使用されます。 詳細については、[バーコード マスクの設定](../../../commerce/set-up-bar-code-masks.md)を参照してください。
1. **サイズ** フィールドに数値を入力します。
1. **最大の長さ** フィールドに数値を入力します。
1. **保存** を選択します。
1. ページを閉じます。
1. **在庫および倉庫管理パラメーター** に移動します。
1. **バー コード設定** フィールドに値を入力または選択します。
    * 以前に作成したバー コード設定を選択します。しかしバーコード形式は、プロセスで使用されているレコード タイプに対する固有識別子の形式と一致している必要があることに注意してください。 たとえば、ピッキング ルートに対するバーコード形式は、通常番号順序であるピッキング ルート参照の形式と一致する必要があります。  
1. **保存** を選択します。
1. ページを閉じます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
