---
title: 製品マスターの作成
description: 事前に定義されたバリアントのために製品マスターを作成します。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 612f83f2df0ca3e66aa38defa27ec34315b4b2ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001727"
---
# <a name="create-a-product-master"></a>製品マスターの作成

[!include [banner](../../includes/banner.md)]

事前に定義されたバリアントのために製品マスターを作成します。 この手順の作成に使用するデモ データの会社は USMF です。 この手順は、製品デザイナーを対象としています。


## <a name="create-a-new-product-master"></a>新しい製品マスターの作成
1. **ナビゲーション ウィンドウ > モジュール > 製品情報管理 > 製品 > 製品マスター** の順に移動します。
2. **新規** をクリックします。
3. **製品番号** フィールドに値を入力します。 番号は一意である必要があります。 **製品番号** フィールドに、番号順序を設定できます。 この場合、ユーザーは値を入力する必要はありません。
4. **製品名** フィールドに値を入力します。 製品の内容を示す名前を入力します。 既定値は検索名になりますが、これはユーザーが変更できます。
5. **製品分析コード グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。 製品分析コード グループにより、製品バリアントを作成するために使用する 4 つの製品分析コードが決まります。 この例では、色とサイズのグループを使用します。
6. 一覧で、目的のレコードを見つけ、選択します。
7. 一覧で、選択された行のリンクをクリックします。 既定の **コンフィギュレーション テクノロジ** は、「事前に定義されたバリアント」です。 これは、この例に使用されます。
8. **OK** をクリックします。

## <a name="select-product-dimension-groups"></a>製品分析コード グループの選択
1. **色グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
2. 一覧で、目的のレコードを見つけ、選択します。
3. 一覧で、選択された行のリンクをクリックします。
4. **サイズ グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
5. 一覧で、目的のレコードを見つけ、選択します。
6. 一覧で、選択された行のリンクをクリックします。

## <a name="add-dimension-groups"></a>分析コード グループの追加
1. **アクション ペイン** で、**製品** をクリックします。
2. **分析コード グループ** をクリックすると、ドロップ ダイアログが開きます。
3. **保管分析コード グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。 保管分析コードは、品目の保管方法と在庫からの取得方法を管理できます。 たとえば、保管分析コードにはサイトと倉庫を含めることができます。
4. 一覧で、目的のレコードを見つけ、選択します。
5. 一覧で、選択された行のリンクをクリックします。
6. **追跡用分析コード グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。 追跡用分析コード グループにより、製品に追加できる追跡用分析コードが決まります。 たとえば、バッチ番号とシリアル番号は、在庫品目を追跡するために使用します。
7. 一覧で、目的のレコードを見つけ、選択します。
8. 一覧で、選択された行のリンクをクリックします。
9. **OK** をクリックします。
10. **保存** をクリックします。
11. ページを閉じます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]