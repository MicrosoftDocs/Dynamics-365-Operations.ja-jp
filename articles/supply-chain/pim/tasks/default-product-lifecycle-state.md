---
title: 既定の製品のライフサイクルの状態を作成
description: この手順では、既定の製品ライフサイクルの状態の作成方法、およびリリースされた製品に既定状態を関連付ける方法を示します。
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b62d47f52da7f9e18bce401578a5e2a629ac5eb8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818136"
---
# <a name="create-a-default-product-lifecycle-state"></a>既定の製品のライフサイクルの状態を作成

[!include [banner](../../includes/banner.md)]

この手順では、既定の製品ライフサイクルの状態の作成方法、およびリリースされた製品に既定状態を関連付ける方法を示します。


## <a name="create-a-default-lifecycle-state"></a>既定のライフサイクルの状態を作成
1. [製品情報管理] > [設定] > [製品ライフサイクルの状態] の順に移動します。
2. [新規] をクリックします。
3. [状態] フィールドに値を入力します。
4. 法人フィールドへのリリース時には既定で [はい] を選択します。
5. [説明] フィールドに値を入力します。
6. [計画に対して有効] フィールドで [いいえ] を選択します。

> [!NOTE]
> 新たにリリースされた製品をマスター プランに含めない場合は、[いいえ] を選択します。 マスター プランに含める必要がある場合は、コントロールを既定値の [はい] のままにします。  

## <a name="create-a-new-released-product"></a>新しくリリースされた製品の作成
1. ページを閉じます。
2. [製品情報管理] > [製品] > [リリースされた製品] の順に移動します。
3. [新規] をクリックします。
4. [製品番号] フィールドに値を入力します。
5. [製品名] フィールドに値を入力します。
6. [検索名] フィールドに値を入力します。
7. [品目モデル グループ] フィールドで、値を入力または選択します。
8. [品目グループ] フィールドで、値を入力または選択します。
9. [保管分析コード グループ] フィールドで、値を入力または選択します。
10. [追跡用分析コード グループ] フィールドで、値を入力または選択します。
11. [OK] をクリックします。

> [!NOTE]
> 既定の製品のライフサイクルの状態は、グローバル定義です。  

## <a name="change-the-product-to-an-active-state"></a>製品を有効な状態に変更する
1. [製品ライフサイクルの状態] フィールドで値を入力または選択します。

> [!NOTE]
> アクティブな状態を設定したと仮定して、アクティブな状態を選択し、マスター プランおよび BOM レベルの計算で製品を使用できるようになります。 当然、一貫した計画に必要なすべての製品の詳細が指定されている場合にのみ意味があります。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]