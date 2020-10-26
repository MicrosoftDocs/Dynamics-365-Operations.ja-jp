---
title: 償却率表の入力および減価償却プロファイルへの関連付け
description: 日本では、固定資産減価償却率は政府機関によって発表されます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepRate_JP, AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 48b027fc14294e3a521b4583e4d463017d89f056
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3984850"
---
# <a name="enter-depreciation-rate-schedule-and-associate-to-depreciation-profile"></a>償却率表の入力および減価償却プロファイルへの関連付け

[!include [banner](../../includes/banner.md)]

日本では、固定資産減価償却率は政府機関によって発表されます。 償却率表はシステムに入力することができます。 償却率表は、ファイルからインポートできるようデータ エンティティとして実装されます。 



このタスクでは、償却率表の変更および減価償却プロファイルとの関連付けの方法について説明します。 このタスクではインポートは実行しません。 



このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。



この手順では、JPMF デモ会社のデータを使用します。


## <a name="modify-a-depreciation-rate-schedule"></a>償却率表の変更
1. [固定資産] > [設定] > [償却率表] > [償却率表] の順に移動します。
2. [編集] をクリックします。
3. [耐用年数] フィールドに数値を入力します。
4. [減価償却レート] フィールドに数値を入力します。
5. [改定償却率] フィールドに数値を入力します。
6. [保証率] フィールドに数値を入力します。

## <a name="associate-a-depreciation-rate-schedule-to-a-depreciation-profile"></a>償却率表と減価償却プロファイルの関連付け 
1. [固定資産] > [設定] > [減価償却プロファイル] に移動します。
2. [編集] をクリックします。
3. [償却率表] フィールドで、ドロップ ダウン ボタンをクリックしてルックアップを開きます。
4. 一覧で、選択された行のリンクをクリックします。
    * 前のタスクで変更した減価償却スケジュールを選択します。  
5. [保存] をクリックします。

