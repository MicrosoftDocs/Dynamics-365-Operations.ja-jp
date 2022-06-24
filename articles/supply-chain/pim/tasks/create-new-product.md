---
title: 新しい製品の作成
description: この記事では、新しい共有製品の作成方法を説明します。
author: t-benebo
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 75490661bf6f1e3dc0655cf9bd79316194c63820
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887344"
---
# <a name="create-a-new-product"></a>新しい製品の作成

[!include [banner](../../includes/banner.md)]

この記事では、新しい共有製品の作成方法を説明します。 これは通常、製品デザイナーが実行します。 このタスクの作成に使用するデモ データの会社は USMF です。


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