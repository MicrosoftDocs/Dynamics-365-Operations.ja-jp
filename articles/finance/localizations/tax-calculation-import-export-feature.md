---
title: 税計算のインポートとエクスポート
description: このトピックでは、税計算サービスのインポートおよびエクスポート機能に関する情報を提供します。
author: Kai-Cloud
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-11-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 02ad47b5f350969b4935a8f383ddf26a7ce7a46a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690893"
---
# <a name="import-and-export-tax-calculations"></a>税計算のインポートとエクスポート

このトピックでは、税計算サービスのインポートおよびエクスポート機能に関する情報を提供します。 この機能により、柔軟で効率的なコンフィギュレーション エクスペリエンスを実現できます。

## <a name="import-and-export-tax-codes"></a>税コードのインポートとエクスポート

### <a name="export-templates"></a>テンプレートのエクスポート

1. [Regulatory Configuration Service (RCS)](https://marketing.configure.global.dynamics.com/) にサインインします。
2. **グローバリゼーション機能** ワークスペースで **機能** を選択し、**税計算** タイルを選択します。
3. 既存の機能を選択するか、[新しい計画を作成](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs) します。
4. **バージョン** グリッドで **編集** を選択します。
5. **税計算** 機能ページで [コンフィギュレーション バージョン](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs) を設定します。
6. **税コード** タブで **インポート** を選択します。
7. **税コード テンプレートのエクスポート** を選択し、**TaxCodesTemplate.zip** ファイルをダウンロードします。
8. **TaxCodesTemplate.zip** を解凍します。 税コード テンプレートは、**計算基準** の値に従って個別に圧縮されます。
9. **By Net Amount.zip** を解凍して、次のコンマ区切り値 (CSV) ファイルを取得します:

    - **TaxCode.csv** – 税コードを入力します。
    - **TaxLimit.csv** – 各税コードの税の上限を入力します。
    - **TaxRate.csv** – 各税コードの税率を入力します。

> [!NOTE]
> 既定では、**サンプル** 税コードの項目がテンプレートで使用可能です。 **サンプル** 税コードが CSV ファイルから削除されていない場合、その機能にインポートされます。

### <a name="import-tax-codes"></a>税コードのインポート

次の手順に従って、テンプレートの **サンプル** 税コードを税計算機能にインポートします。

1. RCS にある **税計算** 機能ページの **税コード** タブで **インポート** を選択します。
2. **参照** を選択し、**TaxCode.csv** ファイルを検索して選択し、**ターゲット テーブル** フィールドで **税コード** を選択します。
3. **OK** を選択し、税コードをインポートします。
4. **TaxRate.csv** ファイルを検索して選択し、**ターゲット テーブル** フィールドで **税率** を選択します。
5. **OK** を選択し、税率をインポートします。
6. **TaxLimit.csv** ファイルを検索して選択し、**ターゲット テーブル** フィールドで **税の上限** を選択します。
7. **OK** を選択し、税の上限をインポートします。

3 つの CSV ファイルすべてが含まれる zip ファイルを直接インポートすることもできます。 これにより、インポートをすばやく簡単に完了できます。

1. RCS にある **税計算** 機能ページの **税コード** タブで **インポート** を選択します。
2. **参照** を選択して、**By Net Amount.zip** ファイルを検索して選択し、次に **OK** を選択します。

### <a name="export-tax-codes"></a>税コードのエクスポート

1. RCS にある **税計算** 機能ページの **税コード** タブで **エクスポート** を選択します。

    **エクスポート** ボタンは、**税コード** グリッドに少なくとも 1 つの税コードがある場合に使用できます。

2. **OK** を選択して、その機能のすべての税コードを ZIP ファイルにエクスポートします。

> [!NOTE]
> エクスポート ファイルをテンプレートとして使用して、税コードを対応する機能にインポートします。

## <a name="import-and-export-applicability-rules"></a>適用ルールのインポートとエクスポート

### <a name="export-applicability-rules"></a>適用ルールのエクスポート

1. [RCS](https://marketing.configure.global.dynamics.com/) にサインインします。
2. **グローバリゼーション機能** ワークスペースで **機能** を選択し、**税計算** タイルを選択します。
3. 既存の機能を選択するか、[新しい計画を作成](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs) します。
4. **バージョン** グリッドで **編集** を選択します。
5. **税計算** 機能ページで [コンフィギュレーション バージョン](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs) を設定します。
6. **税グループの適用** タブで、**税グループ適用の設定** グリッドにある行を選択します。
7. **Microsoft Office で開く** ボタンを選択し、**税サービスの動的適用性マトリックス** を選択します。

    [![税計算機能ページでの Microsoft Excel への適用ルールのエクスポート。](./media/tax-cal-import-export-1.png)](./media/tax-cal-import-export-1.png)

8. **ダウンロード** を選択し、選択した行を Microsoft Excel ワークシートにエクスポートします。

### <a name="import-applicability-rules"></a>適用ルールのインポート

ダウンロードした Excel ワークシートには、**税グループ適用の設定** グリッドの構造が含まれています。 新しいルールをワークシートに直接追加できます。 完了したら、次の手順に従って、新しいルールを **税グループ適用の設定** グリッドにインポートし直します。

1. Excel ワークシートで、インポートする行を選択してコピーします。
2. RCS にある **税計算** 機能ページの **税グループの適用** タブで、**追加** を選択して、**税グループ適用の設定** グリッドの下部に空のレコードを挿入します。
3. **Ctrl + V** を選択して、コピーした行をグリッドに貼り付けます。
4. **保存** を選択します。
