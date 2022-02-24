---
title: 派生テスト ケース
description: このトピックでは、Regression Suite Automation Tool を使用して、複数のコンフィギュレーションで同じテスト ケースを実行する方法について説明します。
author: robadawy
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 21631
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a840091a62af1e64f8a71a250b62d05e1738ef7e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683366"
---
# <a name="derived-test-cases"></a>派生テスト ケース

[!include [banner](../../includes/banner.md)]

Regression Suite Automation Tool (RSAT) を使用すると、複数のテスト ケースを使用して同じタスク記録を使用できるので、異なるデータの構成を使用してタスクを実行できます。 これを行うには、Regression Suite Automation Tool でテストケースを選択し、 **新規 > 派生テストケースの作成** を選択します。 これにより、 Azure DevOps に子テスト ケースが作成されます。 結果として派生したテスト ケースは、 Azure DevOps の親テスト ケースにリンクされます。 Excel パラメーター ファイルが添付されていますが、記録ファイルはありません。 派生したテスト ケースは、選択した **派生** 列と同じテスト スイートの下の Regression Suite Automation Tool グリッドに表示されます。 派生したテスト ケースには、親テスト ケースに数字の接尾語が付いた名前が付けられます。

次の図では、 **仕入先の作成** というテスト ケースから派生テスト ケースが作成されています。

![仕入先の作成という名前のテスト ケースから作成された派生テスト ケースの例](media/derived-test-case.png)
 
派生テスト ケースは、 Azure DevOps で自動的に作成されます。 これは、 **仕入先の作成 テスト** ケースの子品目であり、特別なキーワード **RSAT: DerivedTestSteps** でタグ付けされています。

![自動的に作成された派生テスト ケースの例](media/derived-1.png)
 
派生テスト ケースを実行 (再生) すると、親テスト ケースの記録と Excel パラメーター ファイルのコピーが使用されます。 これにより、複数の記録を維持することなく、異なるパラメーターで同じテストを実行できます。

派生テスト ケースは、親テスト ケースと同じテスト スイートの一部である必要はありません。 他のスイートに移動できます。

派生テストケースの Excel パラメータ ファイルを編集して、親テスト ケースとは異なるユーザー、異なる会社、および・または異なる入力と検証パラメータで実行することができます。
