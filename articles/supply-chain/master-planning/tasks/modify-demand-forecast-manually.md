---
title: 'ガイド: 需要予測の手動変更'
description: この記事では、品目の予測を変更する方法を説明します
author: t-benebo
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6275749f85c9b9d5a8b89da6340beeafbe22c2d4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859259"
---
# <a name="guide-modify-a-demand-forecast-manually"></a>ガイド: 需要予測の手動変更

[!include [banner](../../includes/banner.md)]

この手順では、品目の予測を変更する方法を示します。 この手順は、生産の計画者を対象としています。

## <a name="modify-the-forecast-for-a-selected-item"></a>選択された品目の予測の変更

選択された品目の予測を変更するには:

1. **モジュール \> 生産情報管理 \> 製品 \> リリース済製品** の順に移動します。
1. 一覧で、目的のレコードを見つけ、選択します。 予測を変更する品目を選択します。
1. アクション ペインで、**計画** タブを開き、**需要予測** を選択します。
1. 一覧で行を選択します。 予測明細行がない場合は、アクション ペインで **新規** を選択して、新しい行を作成します。  
1. **販売数量** フィールドに正の数を入力します。 この数値は、品目の予測数量を表わします。 負の数を入力するとエラーが表示されます。
1. 必要に応じて、その他のフィールドに入力します。
1. アクション ウィンドウで、 **保存** を選択します。

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a>Microsoft Excel を使って、1 つ以上のアイテムの予測を変更する

Microsoft Excel を使って、1 つ以上のアイテムの予測を変更するには:

1. 次のどちらかを実行します。
    - 前のセクションで説明したように、任意の品目 (どちらでも構いません) の **需要予測** ページを開きます。
    - **マスター プラン \> 予測 \> 手動予測入力エントリ \> 需要予測明細行** の順に移動します。
1. アクション ペインで、**Microsoft Office で開く \> 需要予測エントリ** を選択します。
1. ダウンロード場所を選択し、保存してから、ダウンロードしたファイルを Excel で開きます。
1. 警告が表示された場合は、**編集を有効にする** を選択 します。
1. Excel で、Microsoft Dynamics 作業ウィンドウを使用して Supply Chain Management にサインインします。 **サインインしたままにする** オプションを有効にしてサインインする必要があり、データ接続アプリを信頼する必要があります。
1. Excel スプレッドシートに、会社の現在の需要予測明細行がすべて表示されます。  必要に応じて、需要予測明細行を追加、削除、および編集できます。
1. Microsoft Dynamics 作業ウィンドウで **発行** を選択 して、変更を Supply Chain Management にアップロードします。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
