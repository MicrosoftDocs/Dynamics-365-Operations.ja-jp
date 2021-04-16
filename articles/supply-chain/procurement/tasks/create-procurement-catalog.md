---
title: 調達カタログの作成
description: このトピックでは、調達カタログの作成方法を説明します。
author: kamaybac
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59117df519b7aa525713d3acd70195cc42614b9a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812401"
---
# <a name="create-a-procurement-catalog"></a>調達カタログの作成

[!include [banner](../../includes/banner.md)]

このトピックでは、調達カタログの作成方法を説明します。 通常、このタスクを実行するのは、調達担当者です。 さらに従業員が要求を作成する際にカタログを使用する方法も参照できます。 カタログを作成する前に、システム内に調達カテゴリ階層が必要です。 階層は、階層にあるすべての製品とともに、新しいカタログによって継承されます。 調達カテゴリ階層を使用する場合、さらに手順ステップで使用される例にも、このガイドをデモ データ会社 USMF で使用することができます。


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>調達カテゴリ階層が存在することを確認します。
1. **ナビゲーション ウィンドウ > モジュール > 調達 > 調達カテゴリ** の順に移動します。 調達カテゴリ階層は USMF のデモ データ会社内で使用でき、製品は **オフィス機器/コンピュータ** カテゴリに追加されました。 この手順をタスク ガイドとして実行している場合は、カテゴリを参照するときガイドのロックを解除する必要があります。 階層を使用できない場合は、**新規** をクリックして階層を作成します。 これが実行可能な回数は一度だけです。  
2. ページを閉じます。

## <a name="create-a-catalog"></a>カタログの作成
1. **ナビゲーション ウィンドウ > モジュール > 調達 > カタログ > 調達カタログ** の順に移動します。
2. **新しい調達カタログ** を選択して、ドロップ ダイアログを開きます。
3. **名前** フィールドに値を入力します。
4. **OK** を選択します。
5. ツリーで、**CORP PROCUREMENT CATEGORIES** を展開します。
6. ツリーで、**OFFICE MACHINES** を展開します。
7. ツリーで、**コンピューター** を選択します。

  - 調達カテゴリからの製品が一覧に表示されます。 製品をカテゴリに追加する場合は、**調達カテゴリ階層** ページまたは **品目の詳細** ページで追加する必要があります。  
  - **既定** の更新タイプは、調達カテゴリ階層に追加された新しい製品をすぐにカタログに表示するかどうかを決定します。 更新タイプが **動的** に設定されている場合、変更はすぐに表示されます。 更新タイプが **静的** の場合、新しい製品は、カタログが再公開された後にカタログを使用している従業員にのみ表示されます。 **公開** アクションはページ上部のアクション ウィンドウで使用できます。 製品が調達カテゴリ階層から削除されると、**既定** の更新タイプ フィールドの値に関係なく、変更はすぐに表示されます。  

8. アクション ウィンドウで、**カテゴリ ナビゲーション** を選択し、**有効化** が選択されていることを確認します。
9. **カタログの有効化** を選択します。
10. ページを閉じます。

## <a name="make-the-catalog-visible"></a>カタログを表示します
1. **ナビゲーション ウィンドウ > モジュール > 調達 > 設定 > ポリシー > 購買ポリシー** の順に移動します。
2. **調達ポリシー USMF** を選択します。 作業者がユーザー プロファイルに接続して製品を注文することができるよう、法人の購入ポリシーを選択する必要があります。 USMF のデモ データでは、管理者ユーザーは **ジュリア ファンダーバーク** と呼ばれる作業者に接続され、既定の USMF で製品を注文します。  
3. 作成したばかりのカタログを選択します。
4. **OK** を選択します。

## <a name="use-the-catalog"></a>カタログを使用します
1. **ナビゲーション ウィンドウ > モジュール > 調達 > 購買要求 > すべての購買要求** の順に移動します。
2. **新規** を選択します。
3. **名前** フィールドに値を入力します。
4. **OK** を選択します。
5. **製品の追加** を選択します。
6. 一覧で、目的のレコードを見つけ、選択します。 左のカテゴリ階層またはリストの先頭にあるフィルターを使用して、製品をフィルター処理できます。  
7. **明細行に追加** を選択します。
8. **OK** を選択します。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]