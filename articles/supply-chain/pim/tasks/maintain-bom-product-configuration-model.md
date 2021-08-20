---
title: 製品コンフィギュレーション モデルの BOM の管理
description: この手順を実行するには、既存の製品コンフィギュレーション モデルが必要です。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 173022d40a5c1354cbe05c171a8921e733d908d065b10889f9cbe0e87f3e98fa
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781468"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>製品コンフィギュレーション モデルの BOM の管理

[!include [banner](../../includes/banner.md)]

この手順を実行するには、既存の製品コンフィギュレーション モデルが必要です。 この手順を作成するのに、デモ会社 USMF の [ハイエンド スピーカー] モデルが使用されています。

## <a name="add-a-bom-line"></a>BOM 明細行の追加

1. **製品情報管理\>製品\>製品コンフィギュレーション モデル** の順にクリックします。
1. 一覧で、目的のレコードを見つけ、選択します。
    * この手順で [ハイエンド スピーカー] を選択します。  
1. 一覧で、選択した行のリンクを選択します。
1. **BOM 明細行** セクションを展開します。
1. **追加** を選択します。
1. **名前** フィールドに値を入力します。
1. **説明** フィールドで、値を入力します。
1. **保存** を選択します。

## <a name="add-bom-line-details"></a>BOM 明細行の詳細の追加

1. **BOM 明細行の詳細** を選択します。
2. **品目番号グループ** フィールドで、値を入力または選択します。
    * たとえば、品目 M0055 を選択できます。  
    * 各 BOM 明細行プロパティに、固定値をとるか、属性にマップさせるかを選択できます。  
3. **設定** チェック ボックスを選択します。
4. **計算** フィールドで、*はい* を選択します。
    * **計算** プロパティを *はい* にを設定すると、原価計算に BOM 明細行 が含まれるようになります。  
5. **設定** タブを選択します。
6. **設定** チェック ボックスを選択します。
7. **数量** フィールドに、数値を入力します。
    * 数量フィールドは、BOM に含まれる品目の数量を決定します。 これは、属性のマッピングの明確な候補になる場合があります。  
8. **分析コード** タブを選択します。
    * 製品分析コードのいずれかが有効であるかどうかを確認します。したがって、値または属性が割り当て済である必要があります。  
9. **OK** を選択します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]