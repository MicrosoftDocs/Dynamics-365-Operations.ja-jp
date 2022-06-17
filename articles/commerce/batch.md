---
title: バッチ追跡品目の処理の改善
description: この記事では、Microsoft Dynamics 365 Commerce の明細転記プロセスで使用するバッチ追跡項目の改善された処理について説明します。
author: josaw1
ms.date: 09/09/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 736ab8dd21f04d7119cca6d53bfeb5e408b8cbd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881881"
---
# <a name="improved-handling-of-batch-tracked-items"></a>バッチ追跡品目の処理の改善

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce の明細転記プロセスで使用するバッチ追跡項目の改善された処理について説明します。

Dynamics 365 Commerce 販売時点管理 (POS) では、バッチ追跡品目のバッチ番号を販売時に取得することはできません。 ただし、特定の構成では、顧客の注文または明細書の転記を通じて販売が Commerce 本社に転記されるとき、Commerce は、バッチ追跡品目に対して有効なバッチ番号が存在することと、請求プロセスで有効なバッチ番号が使用されることを想定しています。

製品に対して有効なバッチ番号が存在する場合は、顧客注文の請求プロセスと、明細書の転記からの販売注文請求プロセスの両方で、そのバッチ番号を使用します。 製品に対する有効なバッチ番号が存在しない場合は、顧客の注文請求プロセスを転記できず、POS ユーザーにエラー メッセージが表示されます。 その後、製品に対してマイナス在庫を有効化している場合でも、明細書の転記がエラー状態になります。

Commerce の改善によって、バッチ追跡品目に対してマイナス在庫が有効になっているとき、在庫が 0 (ゼロ) であるか、またはバッチ番号が使用できない場合、明細書の転記を通じた顧客注文の請求と販売注文の請求がブロックされないことが保証されます。 この改善された機能では、バッチ番号を使用できないときに、販売明細行の既定バッチ ID を使用します。

## <a name="define-the-default-batch-id-that-is-used-for-customer-orders"></a>顧客注文に対して使用する既定バッチ ID を定義する

顧客注文に対して使用する既定バッチ ID を定義する際は、次の手順に従います。

1. Commerce 本社で、**Retail と Commerce \> 本社の設定 \> パラメーター \> Commerce パラメーター** に移動します。
1. **顧客注文** タブの **注文** クイック タブで、**既定バッチ ID** フィールドに値を入力します。

## <a name="define-the-default-batch-id-that-is-used-for-sales-order-invoicing-through-statement-posting"></a>明細書の転記で販売注文の請求に使用する既定バッチ ID を定義する

明細書の転記で販売注文の請求に使用する既定バッチ ID を定義する際は、次の手順に従います。

1. Commerce 本社で、**Retail と Commerce \> 本社の設定 \> パラメーター \> Commerce パラメーター** に移動します。
1. **転記** タブの **在庫の更新** クイック タブで、**既定バッチ ID** フィールドに値を入力します。

> [!NOTE]
> - 既定バッチ ID の機能は、特定の店舗倉庫および品目に対して高度な倉庫管理が有効になっている場合にのみ使用できます。 今後のリリースでは、高度な倉庫管理が有効になっていない場合にも、既定バッチ ID の機能をサポートします。
> - 倉庫管理が複雑でない場合に、明細書の転記でバッチ追跡項目の処理を改善するサポートが Commerce バージョン 10.0.5 リリースに導入されました。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
