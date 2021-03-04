---
title: 作業指示書へのエラーの追加
description: このトピックでは、資産管理における作業指示書へのエラー登録を追加する方法について説明します。
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e82026f1d73e7368d93109bc0b895b7368ac84d4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431992"
---
# <a name="add-fault-to-work-order"></a>作業指示書へのエラーの追加

[!include [banner](../../includes/banner.md)]



エラー デザイナーで設定されたエラーを作業指示書に追加できます。 1 つ以上のエラー レコードを、作業指示書で選択された資産に使用される資産タイプに接続する必要があります。 設定の詳細については、[エラー管理](../setup-for-work-orders/fault-management.md) を参照してください。

1. **資産管理** > **共通** > **作業指示書** > **すべての作業指示書** または **有効な作業指示書** の順に選択します。

2. エラー登録を行う作業指示書を選択し、アクション ウィンドウの **作業指示書** タブの、**資産** グループで **資産エラー** を選択します。

3. **現象** クイック タブの、**明細行の追加** を選択します。 **エラー** フィールドには、エラー番号が連番で自動的に入力されます。

4. **エラー現象** フィールドで、該当する現象を選択します。

5. **エラー領域** フィールドおよび **エラー タイプ** フィールドで、適切な値を選択します。

6. **エラー日付** フィールドには、現在の日付が自動的に挿入されます。 必要に応じて別の日付を選択できます。

7. **選択した現象の原因** クイック タブで、問題の原因を説明する明細行を追加します。

8. **選択した現象の救済** クイック タブで、問題の実行可能なソリューションを説明する明細行を追加します。

9. **保存** を選択します。

下の図は、エラー登録の例を示します。

![図 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a>資産エラーの表示

**資産エラー** の一覧では、資産に登録されているすべてのエラーの概要を取得できます。

**資産エラー** リスト ページでは、資産に登録されているすべてのエラーの概要を取得できます。 ページを開くには、**資産管理** > **照会** > **資産エラー** > **資産エラー** の順に選択します。


## <a name="print-asset-fault-report"></a>資産エラー レポートの印刷

**すべての資産** リスト ページから、すべてのエラー登録を表示する資産エラー レポートおよびエラー統計のグラフィカルな概要を印刷できます。

1. **資産管理** >  **共通** >  **資産** > **全資産** の順に選択します。

2. エラー レポートを印刷する資産を選択します。

3. アクション ウィンドウで、**一般** タブの **レポート** グループで、**資産エラー** を選択します。

4. 特定の期間を入力するか、エラー タイプを選択します。

5. **OK** を選択してレポートを印刷します。

>[!NOTE]
>**資産管理** > **レポート** > **資産** > **資産エラー** の順に選択して、複数の資産または資産タイプに対するエラー レポートを印刷できます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]