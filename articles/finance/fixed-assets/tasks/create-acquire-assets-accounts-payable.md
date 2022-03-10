---
title: 買掛金勘定からの資産の作成と取得
description: この手順では、購買プロセスで固定資産の作成と取得について説明します。
author: saraschi2
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dbac069362a15b5ab1d2dbf88a732a14a3cf709d
ms.sourcegitcommit: 03f53980a4bc67b73ac2be76a3b3e7331d0db705
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/18/2021
ms.locfileid: "7394661"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>買掛金勘定からの資産の作成と取得

[!include [banner](../../includes/banner.md)]

この手順では、購買プロセスで固定資産の作成と取得について説明します。  ここでは、経理担当者、買掛金勘定係、デモ会社 USMF を使用します。


## <a name="set-fixed-assets-parameters"></a>固定資産パラメーターの設定
1. **ナビゲーション ウィンドウ** で、**モジュール > 固定資産 > 設定 > 固定資産パラメーター** の順に移動します。
2. **発注書** クイック タブを展開します。
3. **購買からの資産の取得を許可する** チェック ボックスをオンにします。
4. **製品受領書または請求書の転記時に資産を作成する** チェック ボックスをオンにします。

## <a name="create-a-new-vendor-invoice"></a>新しい仕入先請求書の作成
1. **ナビゲーション ウィンドウ** で、**モジュール > 買掛金勘定 > ワークスペース > 仕入先請求書入力** の順に移動します。
2. **新しい仕入先請求書** をクリックします。
3. **請求元仕入先** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. 一覧で、選択された行のリンクをクリックします。
5. **数** フィールドに値を入力します。
6. **転記日付** フィールドに日付を入力します。
7. **行の追加** をクリックします。
8. **品目番号** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。 在庫のない品目または調達カテゴリが、固定資産の取得に使用できます。  
9. 一覧で、選択された行のリンクをクリックします。
10. **数量** フィールドに、数値を入力します。 数量に関係なく、1 つの請求明細行が作成する固定資産は 1 つのみです。 請求書の数量フィールドの値は、固定資産の数量に転送されます。  
11. **単価** フィールドに数値を入力します。
12. **行の詳細** クイック タブを展開します。
13. **固定資産タ** タブをクリックします。
14. **新しい固定資産の作成** チェック ボックスをオンにします。
15. **固定資産グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
16. 新しい固定資産を作成するときに使用する固定資産グループを一覧で選択します。
17. 一覧で、選択された行のリンクをクリックします。
18. **転記** をクリックします。 固定資産は、請求書の転記時に作成および取得されます。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
