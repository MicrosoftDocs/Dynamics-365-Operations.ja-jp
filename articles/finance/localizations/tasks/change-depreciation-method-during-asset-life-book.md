---
title: 帳簿の資産耐用年数期間中の減価償却方法の変更
description: 日本では、固定資産の耐用年数期間中、減価償却方法を変更することができます。
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: atrukawk
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form:
- AssetBookTable, AssetGroupBookSetup, AssetDepProfileChangeApply_JP
- AssetUndepreciatedBalancedSchedule_JP
ms.openlocfilehash: eabecf6fe0c850147425f7b9fd17604f92b6fe48
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292183"
---
# <a name="change-the-depreciation-method-during-the-asset-life-for-book"></a>帳簿の資産耐用年数期間中の減価償却方法の変更

[!include [banner](../../includes/banner.md)]

日本では、固定資産の耐用年数期間中、減価償却方法を変更することができます。



この手順では、固定資産グループおよび帳簿下の固定資産の減価償却プロファイルの変更について説明します。



この手順を完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。 また、この手順を完了するためには、[未償却残高表] と [経過年数表] をコンフィギュレーションする必要があります。

この手順は、デモ データ会社 JPMF を使用して作成されました。


## <a name="change-a-depreciation-profile"></a>減価償却プロファイルの変更
1. [固定資産] > [設定] > [帳簿] の順に移動します。
2. クイック フィルターを使用して、レコードを見つけます。 たとえば、[帳簿] フィールドで「250NDB_CUR」という値を指定してフィルターを実行します。
3. [固定資産グループ] をクリックします。
4. クイック フィルターを使用して、レコードを見つけます。 たとえば、[固定資産グループ] フィールドで「STRU-A」という値を指定してフィルターを実行します。
5. [減価償却プロファイルの変更] をクリックします。
6. [変更後の減価償却プロファイル] フィールドに値を入力します。
7. [開始日] フィールドに日付を入力します。
    * この日付は、現在の会計カレンダーの会計年度の開始日である必要があります。  
8. [耐用年数の更新] フィールドで、[はい] を選択します。
    * 必要に応じてアイドル期間を追加できます。  
9. [適用] をクリックします。
10. [はい] をクリックします。

## <a name="view-the-years-passed-schedule"></a>経過年数表の表示
1. [固定資産] > [設定] > [償却率表] > [経年表] に移動します。
    * 減価償却プロファイルの更新には対応するデータが必要です。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
