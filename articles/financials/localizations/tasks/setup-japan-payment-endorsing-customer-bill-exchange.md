---
title: 顧客の為替手形の裏書きによって日本の支払を設定します
description: このタスクでは、日本での顧客の為替手形の裏書きによる支払いの設定について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting,  CustParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f509cada0dc12c0a2da00b85f560fc48e0be6d9e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "371010"
---
# <a name="setup-japan-payment-by-endorsing-a-customer-bill-of-exchange"></a>顧客の為替手形の裏書きによって日本の支払を設定します

[!include [task guide banner](../../includes/task-guide-banner.md)]

このタスクでは、日本での顧客の為替手形の裏書きによる支払いの設定について説明します。



このタスクは デモ データ会社 JPMF を使用してレコードされました。


## <a name="set-up-a-posting-profile-for-endorsing-bills-of-exchange"></a>為替手形の転記プロファイルの設定
1. [売掛金勘定] > [設定] > [顧客転記プロファイル] の順に移動します。
2. [新規] をクリックします。
3. [転記プロファイル] フィールドに値を入力します。
    * 例: 「新しい BoE」と入力します。  
4. [追加] をクリックします。
5. [会計コード] フィールドでオプションを選択します。
    * 例えば、「すべて」を選択します。  
6. [裏書勘定] フィールドで、任意の値を指定します。
7. [保存] をクリックします。

## <a name="set-up-bills-of-exchange-information-in-accounts-receivable-parameters"></a>売掛金勘定パラメータでの為替手形情報の設定
1. [売掛金勘定] > [設定] > [売掛金勘定パラメーター] に移動します。
2. [元帳と売上税] タブをクリックします。
3. [為替手形] セクションを展開します。
4. [裏書為替手形] フィールドで、ドロップ ダウン ボタンをクリックしてルックアップを開きます。
5. 一覧で、選択された行のリンクをクリックします。
6. [保存] をクリックします。

