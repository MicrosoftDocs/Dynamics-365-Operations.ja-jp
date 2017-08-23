--- 
title: "増加償却プロファイルの作成および帳簿への割り当て (日本)"
description: "日本では、ほかの減価償却方法と同様、加速償却に減価償却プロファイルが必要です。"
author: ShylaThompson
manager: AnnBe
ms.date: 09/22/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 2a113032aeac7d603fa769f8672a7505f45f9b19
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="create-an-accelerated-depreciation-profile-and-assign-it-to-book-japan"></a>増加償却プロファイルの作成および帳簿への割り当て (日本)

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


