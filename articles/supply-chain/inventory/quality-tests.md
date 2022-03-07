---
title: 品質管理テスト
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management の品質指示に使用できるテストを作成する方法について説明します。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62e5aca8c41aa324802e83e53f52ea39b623a65882962413e743e6dd2671a901
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781041"
---
# <a name="quality-management-tests"></a>品質管理テスト

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management の品質指示に使用できるテストを作成する方法について説明します。

**テスト** ページを使用して、製品が品質仕様を満たすかどうかを決定する個別のテストを定義して表示できます。 テスト グループに 1 つ以上の個別のテストを割り当てることができます。 この場合、許容測定値などのテスト固有の情報も指定します。 測定値は、定量試験に使用されます。 定性試験では、テスト変数が使用されます。

- 定量試験の場合は、**タイプ** フィールドは、*整数* または *分数* に設定されます。 測定単位も指定されます。 品質仕様とテスト結果が数字で示されます。
- 定性試験では、**タイプ** フィールドは、*オプション* に設定されます。 定性試験では、測定されるテスト変数と列挙されたオプションに関する追加情報が必要です。 品質仕様とテスト結果が結果に応じて示されます。

必要に応じて、テスト機器にテストを割り当てることができます。 ただし、品質指示のテストを作成して使用するために、テスト機器は必要ありません。 詳細については、[品質管理テスト機器](quality-test-instruments.md) を参照してください。

必要に応じて、テストの単位を指定して、テスト結果が記録される測定単位を示すこともできます。 たとえば、温度のテストには、華氏または摂氏のいずれかの単位が含まれる場合があります。

## <a name="example-of-a-test"></a>テストの例

ある製造会社では、購入した材料に対して 2 種類のテストを行います。材料品質に関する定量試験と、梱包破損に関する定性試験です。 定性試験に関して、テスト変数 (たとえば、破損した梱包) とその結果を定義する追加情報を指定します。 **テスト グループ** ページを使用して、これら 2 つのテストを 1 つのテスト グループに割り当て、テスト固有の情報を指定します。 2 つのテストの結果をレポートできるよう、テスト グループを品質指示に割り当てます。

## <a name="create-a-test"></a>テストの作成

次の手順に従って、テストを作成します。

1. **在庫管理 \> 設定 \> 品質管理 \> テスト** の順に移動します。
1. アクション ウィンドウで **新規** を選択して、行をグリッドに追加します。 続いて、新しい行に次のフィールドを設定します:

    - **テスト** – テストの固有の ID または名前を入力します。
    - **説明** – テストの詳細説明を入力します。
    - **タイプ** – テストで生成される結果のタイプを選択します。 定量試験では、*分数* または *整数* を選択します。 定性試験では、*オプション* を選択します。
    - **テスト機器** – テストに使用する[テスト機器](quality-test-instruments.md) を選択します。
    - **単位** – **タイプ** フィールドで *分数* または *整数* を選択した場合 (テストが定量試験の場合)、テスト結果を記録する測定単位を選択します。

1. ページを閉じます。

> [!NOTE]
> テストを保存した後は、グリッドの **タイプ** フィールドを編集することはできなくなります。 テストについて記録されるテスト結果のタイプを変更する必要がある場合は、アクション ウィンドウで **品質テスト タイプの変更** を選択します。 **品質テスト タイプの変更** ダイアログ ボックスで、**新しいタイプ** フィールドを目的のタイプに設定し、**OK** を選択してダイアログ ボックスを閉じます。

## <a name="additional-resources"></a>追加リソース

- [品質管理テスト機器](quality-test-instruments.md)
- [品質管理テスト グループ](quality-test-groups.md)
- [品質管理テスト変数](quality-test-variables.md)
- [品質関連](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
