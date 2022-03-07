---
title: 製品モデルのルートの管理
description: この手順を実行するには、既存の製品コンフィギュレーション モデルが必要です。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 704a6b72c9eb8dc49ba9410ccd3689ba5ccfdd1f03e538b95ad174f6c1ee9796
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746139"
---
# <a name="maintain-route-for-a-product-model"></a>製品モデルのルートの管理

[!include [banner](../../includes/banner.md)]

この手順を実行するには、既存の製品コンフィギュレーション モデルが必要です。 この手順は、このプロセスを説明するために、デモ会社 USMF の [ハイエンド スピーカー] モデルを使用します。

## <a name="add-a-route-operation"></a>工順工程の追加

1. **製品情報管理\>製品\>製品コンフィギュレーション モデル** の順にクリックします。
1. 一覧で、目的のレコードを見つけ、選択します。
    * この練習の [ハイエンド スピーカー] モデルを選択します。  
1. 一覧で、選択した行のリンクを選択します。
1. **工順工程** セクションを展開します。
1. **追加** を選択します。
1. **名前** フィールドに値を入力します。
1. **説明** フィールドで、値を入力します。
1. **保存** を選択します。

## <a name="enter-route-operation-details"></a>工順工程の詳細の入力

1. **工順工程の詳細** を選択します。
1. **工程** フィールドで、値を入力または選択します。
1. **工程番号** フィールドで番号を入力します。
    * 工程番号が工順を決定します。  
    * 工順工程の各プロパティは、静的値を取得するか、または属性にマップすることができます。 属性へのマッピングは、コンフィギュレーションの一部として設定された値になります。  
1. **工順グループ** フィールドで、値を入力または選択します。
    * 工順グループは、原価計算、消費、設定の重要な動作を決定します。  
1. **設定** タブを選択します。
1. **時間** タブを選択します。
1. **処理数量** フィールドで、数値を入力します。
    * 一つの工程間で処理される数量を決定します。  
1. **時間変換係数** フィールドで、数値を入力します。
    * 時間の比率を入力します。  
1. **設定** チェック ボックスを選択します。
1. **実行時間** フィールドで、数値を入力します。
    * 指定した数量に対する処理時間を決定します。  
1. **リソース要件** タブを選択します。
1. **追加** を選択します。
1. 一覧で、選択された行をマークします。
1. **要件のタイプ** フィールドでオプションを選択します。
    * 保有している特定のリソースまたは機能を指定するかどうかを決定します。  
1. **要件** フィールドで、値を入力または選択します。
1. **OK** を選択します。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]