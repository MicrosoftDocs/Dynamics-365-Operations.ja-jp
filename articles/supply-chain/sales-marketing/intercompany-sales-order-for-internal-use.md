---
title: 内部使用の会社間販売注文書の作成
description: このトピックでは、内部使用の会社間販売注文書を作成する方法について説明します
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0718a1560ec42df2a0a12e8b81484aa3be46d2d8
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548374"
---
# <a name="create-an-intercompany-sales-order-for-internal-use"></a>内部使用の会社間販売注文書の作成

[!include [banner](../../includes/banner.md)]

通常、会社間販売注文書は、会社間発注書に基づいて自動的に作成されます。 また、会社間販売注文書を手動で作成し、会社間顧客の法人で会社間発注書を生成することもできます。

![会社間の内部販売プロセス](media/intercompanyinternalsalesprocess.png)

## <a name="create-an-intercompany-sales-order-manually"></a>会社間販売注文書の手動作成

図に示すように、法人 B でこれらの手順を実行します。

1. **売掛金勘定 \> 販売注文 \> すべての販売注文** に移動します。
1. アクション ペインで **販売注文** を選択して、販売注文を作成します。
1. **販売注文の作成** ページで顧客アカウントを選択します。 **全般** クイック タブで **会社間** チェック ボックスが選択されていることを確認します。 これは、選択した顧客が会社間顧客であることを示します。
1. 情報を入力または修正し、**OK** を選択して注文明細行を通常どおり完了します。

    **配送先住所** フィールド値が、会社間販売注文書ヘッダーから会社間発注書ヘッダーにコピーされます。 製品分析コードを含む **品目番号** フィールド値と、**配送日** と **通貨コード** のフィールド値が、会社間販売注文明細行から会社間発注書明細行にコピーされます。

1. 注文ヘッダーで **会社間** を選択して、関連する会社間発注書を確認します。
1. 注文明細行で **会社間** を選択して、会社間取引の手持在庫に関する情報を確認します。

> [!TIP]
> 会社間販売注文書は **会社間注文** ページで確認できます。

> [!NOTE]
> 会社間を使用する場合は、**売掛金勘定パラメーター** ページの **請求後の注文の削除** チェック ボックスを解除することをお勧めします。 それ以外の場合、関連する発注書は削除されます。 また、**買掛金勘定パラメーター** ページの **請求後に発注書を削除** チェック ボックスを解除することをお勧めします。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
