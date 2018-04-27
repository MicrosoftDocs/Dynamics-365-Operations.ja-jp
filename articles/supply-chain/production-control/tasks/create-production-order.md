---
title: "製造オーダーの作成"
description: "この手順では、製造オーダーを作成する方法を示します。"
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: 4db56f76c7f8ce0cccf85ab04024d9a1e88a8822
ms.contentlocale: ja-jp
ms.lasthandoff: 02/06/2018

---
# <a name="create-a-production-order"></a>製造オーダーの作成

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

この手順では、製造オーダーを作成する方法を示します。 この手順の作成に使用するデモ データの会社は USMF です。 これは、製造オーダーのライフ サイクルを説明する 7 個の手順の 1 番目です。


## <a name="create-a-production-order"></a>製造オーダーの作成
1. [生産管理] > [製造オーダー] > [すべての製造オーダー] の順に移動します。
2. [新しい製造オーダー] をクリックします。
3. [品目番号] フィールドに、'D0001' を入力します。
4. [出荷] フィールドで、日付を入力します。
    * 出荷日は、期日通りに配送できるように製造オーダーを終了させる必要のある日を示します。 この日付は、スケジューリング プロセスで使用できます。 たとえば、出荷日から逆算して注文のスケジュールを決めることができます。  
5. 数量を '20' に設定します。
    * 注記: BOM 番号フィールドには自動的に現在の品目について有効な BOM 番号が表示されますが、承認済 BOM バージョンの一覧から有効な BOM を選択することによって、製造オーダーの BOM を変更できます。    注記: 工順番号フィールドには自動的に現在の品目について有効な工順番号が表示されますが、承認済の工順バージョンの一覧から有効な工順を選択することによって、製造オーダーの工順を変更できます。  
6. [作成] をクリックします。

## <a name="validate-the-production-order"></a>製造オーダーの検証
1. 一覧で、選択された行のリンクをクリックします。
    * 作成した製造オーダー番号のリンクをクリックします。 これにより、注文の詳細ページが開きます。  
2. [編集] をクリックします。
3. [出荷] フィールドで、日付を入力します。
    * たとえば、製品オーダーの出荷日を変更することができます。  
4. [保存] をクリックします。
5. ページを閉じます。

## <a name="update-the-bom"></a>BOM の更新
1. アクション ウィンドウで、[製造オーダー] をクリックします。
2. BOM をクリックします。
    * BOM のページを開き、製造オーダーの作成時に既定のデータからコピーされたBOMのデータを検証します。 この手順では、BOM の数量を更新する必要があります。  
3. [編集] をクリックします。
4. [数量] フィールドに数値を入力します。
    * BOM 明細行の数量を変更すると、製造オーダーの材料消費の原価見積に影響します。  
5. [保存] をクリックします。
6. ページを閉じます。

## <a name="update-the-production-route"></a>生産工順の更新
1. アクション ウィンドウで、[製造オーダー] をクリックします。
2. [工順] をクリックします。
    * [工順] のページを開き、注文の作成時に既定のデータからコピーされた製造工順のデータを検証します。 この手順では、生産工順内の作業の数量を更新する必要があります。  
3. 一覧で、目的のレコードを見つけ、選択します。
4. [編集] をクリックします。
5. 処理数量 フィールドで、数値を入力します。
    * 処理時間を変更すると、製造オーダーの見積工順消費と原価に影響します。  
6. [保存] をクリックします。
7. ページを閉じます。

