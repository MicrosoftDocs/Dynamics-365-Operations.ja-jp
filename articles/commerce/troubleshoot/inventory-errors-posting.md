---
title: 利用できない在庫または更新の競合による明細書転記エラー
description: この記事では、Microsoft Dynamics 365 Commerce の明細書の転記時に在庫関連の問題に対して適用される可能性があります。
author: Shajain
ms.date: 12/19/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: cebb890b42def6e9b002b01be63266b88bfc35a4
ms.sourcegitcommit: 4ad87483ba0bfea3e04fdb7e578d8abc34e607a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2022
ms.locfileid: "9887630"
---
# <a name="statement-posting-errors-due-to-unavailable-inventory-or-update-conflicts"></a>利用できない在庫または更新の競合による明細書転記エラー

[!include [banner](../../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce の明細書の転記時に在庫関連の問題に対して適用される可能性があります。

## <a name="description"></a>Description

Commerce トランザクションの転記時に、在庫の問題または更新の競合に関連するエラー メッセージが表示される場合があります。

### <a name="inventory-issues-error-message"></a>在庫品目の問題エラー メッセージ

在庫の問題が発生した場合は、次のようなエラー メッセージが表示されます。

> 在庫から yy しか利用できないため、xx はピッキングできません

### <a name="update-conflict-error-messages"></a>競合エラー メッセージの更新

在庫評価方法が *標準原価* または *移動平均* である場合に更新の競合問題が発生する可能性があります。 これらの方法はどちらも費用方法を変更しないので、最終的な原価は転記時に決定されます。

*移動平均* メソッドを使用している場合、受け取る更新競合エラー メッセージは次のような例と類似しています。

> 比例経費計算後の在庫値 xx.xx が予期されません

*標準コスト* メソッドを使用している場合、受け取る更新競合エラー メッセージは次のような例と類似しています。

> 更新後の標準原価が資産在庫金額と一致しません。 値 = xx.xx, Qty = yy.yy、標準コスト = zz.zz

## <a name="resolutions"></a>解決策

### <a name="workaround-for-the-inventory-error"></a>在庫エラーの回避策

品目の在庫を手動で更新するか、Commerce Headquarters の品目に関連付けられている品目モデル グループのマイナスの現物在庫を有効にすることで、在庫エラーを軽減できます。

一貫した転記エクスペリエンスを得るためには、Microsoft では品目モデル グループに対して物理的なマイナス在庫を有効にすることをお勧めします。 一部のシナリオでは、マイナスの現物在庫が有効化されていない限り、ステートメントは転記できない可能性があります。

たとえば、品目に使用できる在庫がない場合、レジ係は品目を返品し、その品目を割引価格で同じトランザクションに追加して価格の一致を適用します。 この場合、返品トランザクションと販売トランザクションの両方が、単一の顧客注文の同じ明細書に引き出されます。 ただし、販売行 (在庫を減少) が転記される前に返品行 (在庫の増加) が転記される保証はないので、在庫エラーが発生する可能性があります。 このシナリオでマイナスの現物在庫が有効化されている場合、トランザクション転記は悪影響を受けず、システムは在庫を正しく反映します。

#### <a name="enable-negative-physical-inventory-for-an-item-model-group"></a>品目モデル グループに対するマイナスの物理在庫の有効化

Commerce Headquarters の品目モデル グループでマイナスの在庫を有効にするには、次の手順に従います。

1. **在庫管理 \> 設定 \> 在庫** の順に移動します。
1. 左のナビゲーション ウィンドウで、品目モデル グループを選択します。
1. **在庫ポリシー** セクションの **マイナス在庫** で、**マイナスの現物在庫** チェック ボックスをオンにします。

![マイナス現物在庫が有効化されています。](./media/Physical_Negative_Inventory.png)

### <a name="workaround-for-the-update-conflict-error"></a>更新の競合エラーの回避策

更新の競合エラーの回避策の可能性については、[在庫評価方法が標準原価または移動平均の場合に更新の競合が発生する](/troubleshoot/dynamics-365/supply-chain/costing/update-conflict-standard-cost-moving-average-inventory-valuation) をご覧ください。

> [!NOTE]
> 更新の競合エラーの場合は、転記の集計手順を使用して生成された顧客注文を削除する必要があります。 推奨される修正プログラムを実装した後に、ステートメントの転記を再び実行する場合は、明細書を転記する必要があります。
