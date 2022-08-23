---
title: 割増償却を使用する固定資産の作成
description: 日本では、固定資産は特定の条件下で増加償却額を転記することができます。
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
ms.search.form: AssetTable, AssetBook
ms.openlocfilehash: 8c3d0607631560605b6bb9ed1568634be8390b8d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270563"
---
# <a name="create-a-fixed-asset-with-additional-depreciation"></a>割増償却を使用する固定資産の作成

[!include [banner](../../includes/banner.md)]

日本では、固定資産は特定の条件下で増加償却額を転記することができます。 



この手順を使用して、割増減価償却プロファイルのある固定資産の作成方法を説明します。



この手順を完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。



これはデモ データ会社 JPMF を使用して作成されました。


## <a name="create-a-fixed-assset-and-assign-an-additional-depreciation-profile-to-it"></a>固定資産の作成および割増減価償却プロファイルの割り当て
1. [固定資産] > [固定資産] > [固定資産] に移動します。
2. [新規] をクリックします。
3. [固定資産グループ] フィールドで値を選択します。
4. [名前] フィールドに値を入力します。
5. [帳簿] をクリックします。
6. [減価償却] セクションを展開します。
7. [特別減価償却プロファイル] フィールドで値を入力または選択します。
8. [特別減価償却] フィールド グループ下で、日付を入力します。
    * 割増償却は、この日の翌日から開始します。  
9. [保存] をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
