---
title: 予算に基づく発注書の作成
description: この手順を使用して、利用可能な予算の確認をする発注書を作成します。
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a79b19ce4ff35ecc1f691edea1bdc5e30010b433
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821372"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>予算に基づく発注書の作成

[!include [banner](../../includes/banner.md)]

この手順を使用して、利用可能な予算の確認をする発注書を作成します。 この記録では、USMF デモ データ会社を使用します。


## <a name="review-the-budget-control-configuration"></a>予算管理コンフィギュレーションを確認する
1. [予算作成] > [設定] > [予算管理] > [予算管理コンフィギュレーション] に移動します。
2. [利用可能な予算財源] タブをクリックします。
3. [伝票と仕訳帳] タブをクリックします。
4. [予算管理ルールの定義] タブをクリックします。
5. [予算グループの定義] タブをクリックします。
6. ページを閉じます。

## <a name="create-the-purchase-order-header"></a>発注ヘッダーの作成
1. [調達] > [発注書] > [すべての発注書] の順に移動します。
2. [新規] をクリックします。
3. [仕入先] フィールドで、値を入力または選択します。
4. [一般] セクションを展開します。
5. [転記日] フィールドで、日付を「2016-01-01」に設定します。
6. [OK] をクリックします。

## <a name="add-a-purchase-order-line"></a>発注明細行の追加
1. [調達カテゴリ] フィールドで、値を入力または選択します。
2. [数量] を「2」に設定します。
3. [単位] フィールドで、値を入力または選択します。
4. [単価] を「10000」に設定します。
5. [財務] をクリックします。
6. [金額の配分] をクリックします。
7. [勘定科目] フィールドで、値「601300-001-023--」を指定します。
8. ページを閉じます。

## <a name="perform-budget-checking"></a>予算確認の実行
1. [財務] をクリックします。
2. [予算確認の実行] をクリックします。
3. [財務] をクリックします。
4. [予算確認のエラーまたは警告] をクリックします。
5. [閉じる] をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]