---
title: 製品分類の階層の作成
description: この手順では、新しいカテゴリ階層を作成し、商品コード階層タイプを割り当てる方法を示します。
author: t-benebo
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole, EcoResProductCategory, EcoResCategorySearchList, EcoResCategoryHierarchyFactbox, EcoResCategoryFriendlyName, EcoResCategoryAddProduct
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb561647efcc21a8287d8246024fb468b8a79a71
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567106"
---
# <a name="create-a-hierarchy-of-product-classification"></a>製品分類の階層の作成

[!include [banner](../../includes/banner.md)]

この手順では、新しいカテゴリ階層を作成し、商品コード階層タイプを割り当てる方法を示します。 この手順の作成に使用するデモ データの会社は USMF です。 この手順は、カテゴリ マネージャーを対象としています。


## <a name="create-the-new-category-hierarchy"></a>新しいカテゴリ階層の作成
1. **ナビゲーション ウィンドウ > モジュール > 製品情報管理 > 設定 > カテゴリと属性 > カテゴリ階層** の順に移動します。
2. **新規** をクリックします。
3. **名前** フィールドに値を入力します。
4. **説明** フィールドで、値を入力します。
5. **作成** をクリックします。

## <a name="build-the-hierarchy"></a>階層の構築
1. **新規** カテゴリ ノードをクリックします。
2. **名前** フィールドに値を入力します。
3. **コード** フィールドに値を入力します。
4. **フレンドリ名** フィールドで、値を入力します。
5. **新規** カテゴリ ノードをクリックします。
6. **名前** フィールドに値を入力します。
7. **コード** フィールドに値を入力します。
8. **フレンドリ名** フィールドで、値を入力します。
9. **新規** カテゴリ ノードをクリックします。
10. **名前** フィールドに値を入力します。
11. **コード** フィールドに値を入力します。
12. **フレンドリ名** フィールドで、値を入力します。
13. **新規** カテゴリ ノードをクリックします。
14. **名前** フィールドに値を入力します。
15. **コード** フィールドに値を入力します。
16. **フレンドリ名** フィールドで、値を入力します。
17. ページを閉じます。

## <a name="classify-the-hierarchy"></a>階層の分類
1. 一覧で、目的のレコードを見つけ、選択します。
2. **アクション ウィンドウ** で、**カテゴリ階層** をクリックします。
3. **階層タイプの関連付け** をクリックします。
4. **新規** をクリックします。
5. **カテゴリ階層タイプ** フィールドで、オプションを選択します。 **製品分類で商品コードのカテゴリ階層タイプ** を選択します。  
6. **カテゴリ階層** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
7. 一覧で、目的のレコードを見つけ、選択します。
8. 一覧で、選択された行のリンクをクリックします。
9. ページを閉じます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]