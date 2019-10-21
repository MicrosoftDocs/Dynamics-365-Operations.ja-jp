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
ms.search.scope: Operations
ms.custom: 21631
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 95252fdd36a8ac2b24e5a6d2c757ac7fff416fdb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191808"
---
# <a name="derived-test-cases"></a>派生テスト ケース

[!include [banner](../../includes/banner.md)]

Regression Suite Automation Tool を使用すると、複数のコンフィギュレーションで同じテスト ケースを実行できます。 これを行うには、Regression Suite Automation Tool でテストケースを選択し、 **新規 > 派生テストケースの作成** を選択します。 これにより、 Azure DevOps に子テスト ケースが作成されます。 結果として派生したテスト ケースは、 Azure DevOps の親テスト ケースにリンクされます。 Excel パラメーター ファイルが添付されていますが、記録ファイルはありません。 派生したテスト ケースは、選択した **派生** 列と同じテスト スイートの下の Regression Suite Automation Tool グリッドに表示されます。 派生したテスト ケースには、親テスト ケースに数字の接尾語が付いた名前が付けられます。

次の図では、 **仕入先の作成** というテスト ケースから派生テスト ケースが作成されています。

![](media/derived-test-case.png)
 
派生テスト ケースは、 Azure DevOps で自動的に作成されます。 これは、 **仕入先の作成 テスト** ケースの子品目であり、特別なキーワード **RSAT: DerivedTestSteps** でタグ付けされています。

![](media/derived-1.png)
 
派生テスト ケースを実行 (再生) すると、親テスト ケースの記録と Excel パラメーター ファイルのコピーが使用されます。 これにより、複数の記録を維持することなく、異なるパラメーターで同じテストを実行できます。

派生テスト ケースは、親テスト ケースと同じテスト スイートの一部である必要はありません。 他のスイートに移動できます。
