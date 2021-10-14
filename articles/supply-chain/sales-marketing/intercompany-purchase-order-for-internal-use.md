---
title: 内部で使用する会社間発注書の作成および請求
description: このトピックでは、内部使用の会社間発注書を作成および請求する方法について説明します
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 88a14ff962c5cf0cd1cff24b16cc7a62e9e1c8ce
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548377"
---
# <a name="create-and-invoice-an-intercompany-purchase-order-for-internal-use"></a>内部で使用する会社間発注書の作成および請求

[!include [banner](../../includes/banner.md)]

会社間仕入先の会社間発注書を作成できます。 これにより、会社間仕入先で会社間販売注文書が自動的に作成されます。

![会社間内部購入プロセス](media/intercompanypurchaseprocess.png)

## <a name="create-an-intercompany-purchase-order-and-a-corresponding-intercompany-sales-order"></a>会社間発注書と対応する会社間販売注文書の作成

図に示すように、法人 AAA でこれらの手順を実行します。

1. **買掛金勘定** \> **発注書** \> **すべての発注書** を選択します。
1. **すべての発注書** リスト ページで、会社間仕入先の発注書を作成します。 フィールド値が仕入先勘定から発注書にコピーされます。

    会社間仕入先を使用しているため、会社間販売注文書が仕入先に相当する法人で作成されます。 会社間販売注文書の番号は、会社間発注書の番号と同じにすることができ、法人の ID を含めることができます。 使用される番号構造は、**会社間** ページにある **販売注文の番号付け** フィールドの選択内容によって異なります。 たとえば、法人 AAA で販売注文 00029\_064 を作成すると、法人 BBB の販売注文番号は AAA00029\_64 になります。

    情報メッセージは、会社間発注書と会社間販売注文が作成されたことを示します。 メッセージには、会社間販売注文番号が参考までに含まれます。

1. 発注書に明細行品目を追加します。 対応する明細行品目が会社間販売注文書に自動的に追加されます。 品目が他方の法人にない場合は、メッセージが表示され、発注書に品目を追加することはできません。 この問題を解決するには、他方の法人に切り替え、その法人に製品をリリースします。 品目が、その法人の販売注文に追加できるようになります。 その後、発注書の法人に戻り、明細行品目の追加を続行します。
1. 発注書の情報の入力が完了したら、確認します。

## <a name="process-the-intercompany-packing-slip-and-customer-invoice"></a>会社間梱包明細と顧客請求書の処理

図に示すように、法人 BBB でこれらの手順を実行します。

1. **売掛金勘定 \> 販売注文 \> すべての販売注文** に移動します。
1. **すべての販売注文** リスト ページで、会社間販売注文を選択します。
1. アクション ペインで **ピッキングと梱包** タブ を選択 し、**梱包明細** を選択します。
1. **転記** チェック ボックスを選択します。
1. **OK** を選択します。 梱包明細が法人 BBB に転記されます。
1. **すべての販売注文** リスト ページで、会社間販売注文を選択します。
1. アクション ペインで **請求書** タブを選択し、**請求書** を選択します。
1. **転記** チェック ボックスを選択します。
1. **OK** を選択します。

    会社間販売注文書の顧客請求書が法人 BBB に転記されます。

## <a name="process-the-intercompany-product-receipt-and-vendor-invoice"></a>会社間製品受領書と仕入先請求書の処理

図に示すように、法人 AAA でこれらの手順を実行します。

1. **買掛金勘定 \> 発注書 \> すべての発注書** に移動します。
1. **すべての発注書** リスト ページで、会社間発注書を選択します。
1. アクション ペインで **入庫** を選択し、**製品受領書** を選択します。 製品受領書が作成されます。 製品受領書番号は、会社間梱包明細番号と同じです。
1. **転記** チェック ボックスを選択します。
1. **OK** を選択します。
1. **すべての発注書** リスト ページで、会社間発注書を選択します。
1. アクション ペインで **請求書** を選択し、**請求書** を選択します。 仕入先請求書が作成されます。 仕入先請求書番号は、会社間顧客請求書番号と同じです。
1. 仕入先請求書の入力を終了し、転記します。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
