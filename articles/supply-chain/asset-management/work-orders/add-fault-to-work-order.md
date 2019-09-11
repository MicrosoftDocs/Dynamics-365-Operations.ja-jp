---
title: 作業指示書へのエラーの追加
description: このトピックでは、資産管理における作業指示書へのエラー登録を追加する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875761"
---
# <a name="add-fault-to-work-order"></a>作業指示書へのエラーの追加

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


エラー デザイナーで設定されたエラーを作業指示書に追加できます。 作業指示書で選択された資産には、1 つ以上のエラー レコードが接続されている資産タイプが含まれている必要があります。 設定の詳細については、[エラー管理](../setup-for-work-orders/fault-management.md) セクションを参照してください。

1. **資産管理** > **共通** > **作業指示書** > **すべての作業指示書**または**有効な作業指示書**の順にクリックします。

2. 一覧で、エラー登録を行う作業指示書を選択し、**資産エラー**をクリックします。

3. **現象**クイック タブの、**明細行の追加**をクリックします。 **エラー** フィールドには、エラー番号が連番で自動的に挿入されます。

4. **エラー現象**フィールドで該当する現象を選択します。

5. **エラー領域**と**エラー タイプ**を選択します。

6. **エラー日付**フィールドには、現在の日付が自動的に挿入されます。 必要に応じて、別の日付を選択できます。

7. **選択した現象の原因**クイック タブで、問題の原因を説明する明細行を追加します。

8. **選択した現象の救済**クイック タブで、問題の実行可能なソリューションを説明する明細行を追加します。

9. **保存**をクリックします。

![図 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a>資産エラーの表示

**資産エラー**の一覧では、資産に登録されているすべてのエラーの概要を取得できます。

**資産管理** > **照会** > **資産エラー** > **資産エラー**の順にクリックして、一覧を開きます。


## <a name="print-asset-fault-report"></a>資産エラー レポートの印刷

**すべての資産**リスト ページから、すべてのエラー登録を表示する資産エラー レポートおよびエラー統計のグラフィックな概要を印刷できます。

1. **資産管理**  >  **共通**  >  **資産**  >  **全資産**をクリックします。

2. **資産**リストで、印刷するエラー レポートの資産を選択します。

3. **一般**タブ > **レポート セクション**で、**資産エラー**をクリックします。

4. 特定の期間を挿入するか、エラー タイプを選択します。

5. **OK** をクリックしてレポートを印刷します。

>[!NOTE]
>**資産管理** > **レポート** > **資産** > **資産エラー**の順にクリックして、複数の資産または資産タイプに対するエラー レポートを印刷することもできます。

