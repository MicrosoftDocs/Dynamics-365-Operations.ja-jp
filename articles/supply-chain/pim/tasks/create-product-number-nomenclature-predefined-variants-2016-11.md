---
title: 事前定義された製品バリアントの製品番号の分類の作成
description: このトピックでは、事前定義済製品バリアントの製品番号の分類を設定する方法、および適切な製品分析コード グループに割り当てる方法を説明します。
author: t-benebo
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5179dd54f22de11dc4c0f54113376f13b2f59c48
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569580"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>事前定義された製品バリアントの製品番号の分類の作成

[!include [banner](../../includes/banner.md)]

このトピックでは、事前定義済製品バリアントの製品番号の分類を設定する方法、および適切な製品分析コード グループに割り当てる方法を説明します。 この手順の作成に使用するデモ データの会社は USMF です。 新しい製品番号に関する分類は、色やサイズの製品分析コード グループに割り当てられます。 このタスクは、通常、製品デザイナーが行います。


## <a name="create-a-product-number-nomenclature"></a>[製品番号の分類] を作成します。

1. **製品情報管理\>設定\>製品の分類** の順にクリックします。
1. **新規** を選択します。
1. **名前** フィールドに、目標の製品分析コード グループ、たとえば、`ColorSize` を特定する用語の名前を入力します。
1. **説明** フィールドで、値を入力します。
1. **追加** を選択します。
1. **製品マスター** 番号を選択します。
1. **追加** を選択します。
1. **テキスト定数** を選択します。
1. **テキスト** フィールドに値を入力します。
1. **追加** を選択します。
1. **色** を選択します。
1. **追加** を選択します。
1. **テキスト定数** を選択します。
1. **テキスト** フィールドに値を入力します。
1. **追加** を選択します。
1. **サイズ** を選択します。
1. ページを閉じます。

## <a name="assign-the-nomenclature-to-a-product-master"></a>製品マスターに用語を割り当て

1. **製品分析コード グループ** を選択します。
2. **SizeCol 製品分析コード** グループを選択します。
3. **編集** を選択します。
4. **分類の使用** フィールドで、**はい** を選択します。
5. **製品バリアント番号の分類** フィールドに、値を入力または選択します。
6. ページを閉じます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]