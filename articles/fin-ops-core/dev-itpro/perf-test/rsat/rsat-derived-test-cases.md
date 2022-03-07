---
title: 派生テスト ケース
description: このトピックでは、Regression Suite Automation Tool を使用して、複数のコンフィギュレーションで同じテスト ケースを実行する方法について説明します。
author: FrankDahl
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.custom: 21631
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86fc39387bb36803f85c1633d973ebd2231c6b4d
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782447"
---
# <a name="derived-test-cases"></a>派生テスト ケース

[!include [banner](../../includes/banner.md)]

Regression Suite Automation Tool (RSAT) を使用すると、複数のテスト ケースを使用して同じタスク記録を使用できるので、異なるデータ構成を使用してタスクを実行できます。 Regression Suite Automation Tool でテストケースを選択し、**新規 > 派生テスト ケースの作成** を選択します。 これにより、 Azure DevOps に子テスト ケースが作成されます。 結果として派生したテスト ケースは、 Azure DevOps の親テスト ケースにリンクされます。 Excel パラメーター ファイルが添付されていますが、記録ファイルはありません。 派生したテスト ケースは、選択した **派生** 列と同じテスト スイートの下の Regression Suite Automation Tool グリッドに表示されます。 既定では、派生したテスト ケースに、親テスト ケースと数値の接尾語に基づいた名前が付けられます。

次の図では、**販売注文の作成と検証 - v2** という名前のテスト ケースからの派生テスト ケースが作成されています。 (Azure DevOps の) 派生テスト ケースに **販売注文の作成と検証 - v2 (検証に失敗)** という名前が付けられています。

![派生テスト ケースの例。](media/derived-test-case.png)

Azure DevOps において、派生テスト ケースは **販売注文の作成と検証 - v2** テスト ケースの子項目であり、特別なキーワード **RSAT:DerivedTestSteps** でタグ付けされています。

![自動的に作成された派生テスト ケースの例。](media/derived-1.png)

派生テスト ケースを実行すると、親テスト ケースの記録と Excel パラメーター ファイルのコピーが使用されます。 これにより、複数の記録を維持することなく、異なるパラメーターで同じテストを実行できます。

派生テスト ケースは、親テスト ケースと同じテスト スイートの一部である必要はなく、他のスイートで使用することができます。 派生テスト ケースの名前を変更することもできます。 派生テスト ケースの Excel パラメーター ファイルを編集して、親テスト ケースとは異なるユーザー、会社、または異なる入力や検証パラメーターで実行することができます。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]