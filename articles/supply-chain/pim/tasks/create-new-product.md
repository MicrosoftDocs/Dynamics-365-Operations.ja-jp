---
title: 新しい製品の作成
description: このトピックでは、新しい共有製品の作成方法を説明します。
author: ShylaThompson
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6d33a13920e1881cdc69ad7c100180d3b3b441d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820037"
---
# <a name="create-a-new-product"></a>新しい製品の作成

[!include [banner](../../includes/banner.md)]

このトピックでは、新しい共有製品の作成方法を説明します。 これは通常、製品デザイナーが実行します。 このタスクの作成に使用するデモ データの会社は USMF です。


## <a name="create-a-product"></a>製品の作成
1. ナビゲーション ウィンドウで、**モジュール > 製品情報管理 > 製品 > 製品** の順に移動します。
2. **新規** を選択します。
3. **製品番号** フィールドに値を入力します。 番号順序が製品番号に対して設定されていない場合は、手動で入力する必要があります。  
4. **製品名** フィールドに値を入力します。 製品名が検索名の既定値になります。 必要に応じて手動でこれを変更できます。  
5. **OK** を選択します。

## <a name="set-up-dimension-groups"></a>分析コード グループの設定
1. **分析コード グループ** を選択して、ドロップ ダイアログを開きます。
2. **保管分析コード グループ** フィールドで、値を入力または選択します。 保管分析コード グループにより、製品の各トランザクションに入力する必要がある保管分析コードと、在庫で追跡される方法が決まります。  
3. **追跡用分析コード グループ** フィールドで、値を入力または選択します。 追跡用分析コード グループにより、製品の各トランザクションに入力する必要がある追跡用分析コードと、在庫で処理される方法が決まります。  
4. **OK** を選択します。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]