---
title: 会社間注文の諸費用を設定する
description: このトピックでは、会社間注文の諸費用を設定する方法について説明します
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 3786df5ce185fa8433d7c69bed5bef09b4983b8b
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548383"
---
# <a name="set-up-charges-on-intercompany-orders"></a>会社間注文の諸費用を設定する

[!include [banner](../../includes/banner.md)]

会社間注文に追加する諸費用を設定できます。 会社間販売注文書に諸費用を追加すると、その諸費用は会社間発注書に自動的に同期されます。 これは、会社間の販売注文書から発注書まで、またその逆の両方で機能します。

また、諸費用を会社間の割合として定義することで、諸費用を使用して会社間販売注文書に利益を追加することもできます。

会社間注文に適用される諸費用を設定すると、元の販売注文書の正味金額から会社間販売注文の内部利益を計算できます。 これは、会社間仕入先が原価価格で販売している場合に行うことができます。 以下の手順では、会社間顧客に対してこれを行う方法について説明します。 同じ手順を仕入先に対しても使用できます。

1. **売掛金勘定 \> 設定 \> 諸費用 \> 顧客請求金額グループ** に移動します。
1. 請求金額グループを作成します。
1. **売掛金勘定 \> 顧客 \> すべての顧客** の順に移動します。 顧客アカウント リンクを選択します。 アクション ペインで **顧客** タブを選択し、**販売注文** クイック タブを選択します。
1. アクション ペインの **編集** を選択して、フィールドに対する編集を有効にします。 **請求金額グループ** フィールドで、手順 2 で設定した会社間請求金額グループを選択します。
1. **売掛金勘定 \> 設定 \> 諸費用 \> 自動請求** に移動します。
1. 関連するフィールドにデータを入力することで諸費用を設定します。
1. **顧客関係** フィールドで、手順 2 で設定した会社間請求金額グループを選択します。
1. **明細行** クイック タブの **カテゴリ** フィールドで **会社間の割合** を選択します。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
