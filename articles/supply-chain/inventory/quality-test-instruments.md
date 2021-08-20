---
title: 品質管理テスト機器
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management の品質指示のテストに使用できるテスト機器を作成する方法について説明します。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 39624a9f00829e551fe3790a024155b6104318ef5cc1c582ab263c3868462063
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774105"
---
# <a name="quality-management-test-instruments"></a>品質管理テスト機器

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management の品質指示のテストに使用できるテスト機器を作成する方法について説明します。

**テスト機器** ページを使用して、品質指示のテストを実行するために使用するデバイスに関する詳細を定義および表示します。 テスト機器はオプションです。 ただし、品質作業員が、特定のテストの実行にどのデバイスまたはツールを使用する必要があるのかを知るのに役立ちます。

## <a name="test-instrument-example"></a>テスト機器の例

電気コンポーネントに対してさまざまなテストを実行しています。 一部のテストは、コンポーネントの電圧出力用で、1 つのテストはコンポーネントの温度用であり、もう 1つのテストはコンポーネントの重量用です。 各テストの実行には、さまざまなツール、デバイス、または設備が使用されます。 たとえば、電圧計は電圧を測定するために使用され、温度計は温度を測定するために使用され、スケールは重量を測定するために使用されます。 これらの各デバイスをテスト機器として構成し、テスト結果を記録する必要がある測定単位を指定できます。 たとえば、電圧計の結果はボルトで記録され、温度計の結果は華氏または摂氏で記録され、スケールの結果はポンドまたはキログラムで記録されます。

## <a name="create-a-test-instrument"></a>テスト機器の作成

1. **在庫管理 \> 設定 \> 品質管理 \> テスト機器** の順に移動します。
1. アクション ウィンドウで **新規** を選択して、行をグリッドに追加します。 続いて、新しい行に次のフィールドを設定します:

    - **テスト機器** – テスト機器の固有の ID または名前を入力します。
    - **説明** – テスト機器の詳細説明を入力します。
    - **単位** – 機器が測定する結果の単位を選択します。 **精度** フィールドは、選択した単位に基づいて自動的に設定されます。

1. ページを閉じます。

## <a name="additional-resources"></a>追加リソース

- [品質管理テスト](quality-tests.md)
- [品質管理テスト グループ](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
