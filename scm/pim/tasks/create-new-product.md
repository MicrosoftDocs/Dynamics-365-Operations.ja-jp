--- 
title: "新しい製品の作成"
description: "このタスクは、新しい共有製品を作成する方法を示します。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/08/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 856ad74ce30bb58975f78aeb3fafc6e2e2805c79
ms.contentlocale: ja-jp
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-new-product"></a>新しい製品の作成

[!include[task guide banner](../../includes/task-guide-banner.md)]

このタスクは、新しい共有製品を作成する方法を示します。 これは通常、製品デザイナーが実行します。 このタスクの作成に使用するデモ データの会社は USMF です。

1. [製品情報管理] > [製品] > [製品] の順に移動します。

## <a name="create-a-product"></a>製品の作成
1. [新規] をクリックします。
2. [製品番号] フィールドに値を入力します。
    * 番号順序が製品番号に対して設定されていない場合は、手動で入力する必要があります。  
3. [製品名] フィールドに値を入力します。
    * 製品名が検索名の既定値になります。 必要に応じて手動でこれを変更できます。  
4. [OK] をクリックします。

## <a name="set-up-dimension-groups"></a>分析コード グループの設定
1. [分析コード グループ] をクリックすると、ドロップ ダイアログが開きます。
2. [保管分析コード グループ] フィールドで、値を入力または選択します。
    * 保管分析コード グループにより、製品の各トランザクションに入力する必要がある保管分析コードと、在庫で追跡される方法が決まります。  
3. [追跡用分析コード グループ] フィールドで、値を入力または選択します。
    * 追跡用分析コード グループにより、製品の各トランザクションに入力する必要がある追跡用分析コードと、在庫で処理される方法が決まります。  
4. [OK] をクリックします。


