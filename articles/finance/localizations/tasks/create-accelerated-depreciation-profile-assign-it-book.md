---
title: 加速減価償却プロファイルを作成し、帳簿に割り当てる
description: 日本では、ほかの減価償却方法と同様、加速償却に減価償却プロファイルが必要です。
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: AssetDepreciationProfile, AssetBookTable
ms.openlocfilehash: af22d36ec8bcd11c0e38ecfbf1afd8b989a58a3c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286958"
---
# <a name="create-accelerated-depreciation-profile-and-assign-it-to-book"></a>加速減価償却プロファイルを作成し、帳簿に割り当てる

[!include [banner](../../includes/banner.md)]

日本では、ほかの減価償却方法と同様、加速償却に減価償却プロファイルが必要です。 



この手順では、増加償却用の減価償却プロファイルの作成方法および帳簿への割り当て方法について説明します。 



この手順を完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。



この手順は、デモ データ会社 JPMF を使用して作成されました。


## <a name="create-a-depreciation-profile"></a>減価償却プロファイルの作成
1. [固定資産] > [設定] > [減価償却プロファイル] に移動します。
2. [新規] をクリックします。
3. [減価償却プロファイル] フィールドに値を入力します。
4. 後で参照できるよう [減価償却プロファイル] フィールドの値をメモします。
5. [名前] フィールドに値を入力します。
6. [方法] フィールドで「加速」を選択します。
7. [保存] をクリックします。

## <a name="assign-the-depreciation-profile-to-a-book"></a>減価償却プロファイルの帳簿への割り当て
1. [固定資産] > [設定] > [帳簿] の順に移動します。
2. 増加償却プロファイルを割り当てる帳簿を選択します。
3. [編集] をクリックします。
4. 事前にメモした値を [加速償却プロファイル] に使用します。
5. [保存] をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
