---
title: 割増償却に対する減価償却プロファイルおよび転記プロファイルのコンフィギュレーション
description: この手順を使用して、特別償却の減価償却プロファイルと転記プロファイルを構成する方法を説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile,  AssetPosting
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45e9fdb90693bd130686325eb35020ffc8628fbe
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978564"
---
# <a name="configure-depreciation-profile-and-posting-profile-for-additional-depreciation"></a>割増償却に対する減価償却プロファイルおよび転記プロファイルのコンフィギュレーション

[!include [banner](../../includes/banner.md)]

この手順を使用して、特別償却の減価償却プロファイルと転記プロファイルを構成する方法を説明します。

日本では、特定の条件下で特別償却が許可されます。 これは特別償却として扱われます。 

この手順を完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。

この手順は、デモ データ会社 JPMF を使用して作成されました。




## <a name="configure-a-depreciation-profile"></a>減価償却プロファイルのコンフィギュレーション
1. [固定資産] > [設定] > [減価償却プロファイル] に移動します。
2. [新規] をクリックします。
3. [減価償却プロファイル] フィールドに値を入力します。
4. [名前] フィールドに値を入力します。
5. [方法] フィールドで、「特別償却」を選択します。
6. [会計方法] フィールドで、オプションを選択します。
    * 引当メソッドに [準備金] を選択し、仕分のダイレクト オフ メソッドにダイレクト オフを選択します。 通常、財務諸表で推奨される表示方法は、引当メソッドです。  
7. [特別償却適用期間] フィールドに数値を入力します。
8. [基準取得価額割合] フィールドに数値を入力します。
    * 100% として「1」を入力します。 実際の値は固定資産によって異なる場合があります。  
9. [特別償却率] フィールドに数値を入力します。
    * 特別減価償却額は、所得原価、基準取得価額割合、および特別減価償却率の結果として計算されます。  30% として「0.3」を入力します。 実際の値は固定資産によって異なる場合があります。  
10. [保存] をクリックします。

## <a name="configure-a-posting-profile"></a>転記プロファイルのコンフィギュレーション
1. [固定資産] > [設定] > [固定資産転記プロファイル] の順に移動します。
2. [編集] をクリックします。
3. [トランザクション タイプ] フィールドで「特別減価償却」を選択します。
    * 特別償却は特別減価償却として転記されます。  
    * オプション: [主勘定] および [相手勘定] をコンフィギュレーションします。  
    * これらの勘定のフィールドを変更するためには [編集] をクリックする必要があります。  

