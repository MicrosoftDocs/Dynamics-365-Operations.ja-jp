---
title: 単一資産の資産耐用年数期間中の減価償却方法の変更
description: 日本では、固定資産の耐用年数期間中、減価償却方法を変更することが許可されています。
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
ms.search.form:
- AssetTable, AssetBook, AssetDepProfileChange_JP
- AssetUndepreciatedBalancedSchedule_JP
ms.openlocfilehash: c3a62394fcd2ee7786b4b14ffae2d936b4f4f9f7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270573"
---
# <a name="change-the-depreciation-method-during-the-asset-life-for-one-asset"></a>単一資産の資産耐用年数期間中の減価償却方法の変更

[!include [banner](../../includes/banner.md)]

日本では、固定資産の耐用年数期間中、減価償却方法を変更することが許可されています。



この手順では、固定資産の減価償却プロファイルの変更について説明します。



このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。 また、この手順を完了する前に、[未償却残高表] と [経過年数表] をコンフィギュレーションする必要があります。



この手順は、デモ データ会社 JPMF を使用して作成されました。


## <a name="change-the-depreciation-profile-for-a-fixed-asset"></a>固定資産の減価償却プロファイルを変更する
1. [固定資産] > [固定資産] > [固定資産] に移動します。
2. クイック フィルターを使用して、レコードを見つけます。 たとえば、[固定資産番号] フィールドを「STRUM-000001」の値でフィルタリングします。
3. [帳簿] をクリックします。
4. [機能] をクリックします。
5. [減価償却プロファイルの変更] をクリックします。
6. [新規] をクリックします。
7. [開始日] フィールドに日付を入力します。
    * この日付は、現在の会計カレンダーの会計年度の開始日である必要があります。  
8. [減価償却プロファイル] フィールドに値を入力します。
9. [耐用年数の更新] をクリックします。
    * [耐用年数]、[減価償却期間] の残りが更新されることを確認します。  

## <a name="view-the-undepreciated-balance-schedule-for-fixed-assets"></a>固定資産の未償却残高表の表示
1. [固定資産] > [設定] > [償却率表] > [未償却残額表] に移動します。
    * 償却率表の編集方法を確認する際には [償却率表] の手順を参照してください。  
    * 減価償却プロファイルの更新には対応するデータが必要です。  
    * [変更元の方法]、[変更後の方法]、[耐用年数] および [経過年数] によって資産の変更に適用されるレコードが決定されます。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
