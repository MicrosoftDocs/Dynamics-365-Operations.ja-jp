---
title: 税内訳情報を注文集計で非表示にする
description: このトピックでは、Microsoft Dynamics 365 Commerce のカートの注文集計、チェックアウト、注文確認、および注文の詳細ページで税内訳情報を非表示にする方法について説明します。
author: gvrmohanreddy
ms.date: 04/21/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-03-28
ms.openlocfilehash: 9890b5cd92f8c07e6feabb26f4fdd076cb7a02bc
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645220"
---
# <a name="hide-tax-breakup-information-in-order-summaries"></a>税内訳情報を注文集計で非表示にする

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce のカートの注文集計、チェックアウト、注文確認、および注文の詳細ページで税内訳情報を非表示にする方法について説明します。

既定では、Dynamics 365 Commerce は税内訳情報を、カートの注文集計、チェックアウト、注文確認、および注文の詳細ページで表示します。 Commerce バージョン 10.0.27 リリースでは、Commerce サイト ビルダーに、注文集計の税内訳情報を非表示にできるオプションが用意されています。

次の図は、注文集計の 2 つの例を示しています。 1 つは税内訳情報を表示し、もう 1 つの方は非表示にします。

![税内訳情報が表示および非表示にされるカートの例。](media/prices-include-sales-tax-e-Commerce.png)

> [!NOTE]
> - 注文集計で税内訳情報を非表示にするオプションは、**小売とコマース \> チャネル \> 店舗 \> すべての店舗** において、コマース本部で e コマースチャネルの **税込価格** オプションが **はい** に設定されている場合のみ使用できます。 
> - 既定では、サイト ビルダーでは **税内訳を注文集計で表示** オプションが有効になっています。

## <a name="hide-tax-breakup-information-in-order-summaries"></a>税内訳情報を注文集計で非表示にする

税内訳情報を注文集計で非表示にするには、以下の手順を実行します。

1. Commerce サイト ビルダーで、更新するサイトに移動します。
1. **サイト 設定 \> 拡張** に移動します。
1. **税内訳を注文集計で表示** チェックボックスをオフにします。

税内訳情報を注文集計で表示するには、**税内訳を注文集計で表示** チェックボックスをオンにします。  

次の図は、サイト ビルダーで強調表示および選択された **税内訳を注文集計で表示** のチェックボックスを示しています。

![税内訳を注文集計で表示するオプションを、サイト ビルダーに表示します。](media/prices-include-sales-tax-e-Commerce-site-settings.png)

## <a name="additional-resources"></a>追加リソース

[消費税の概要](/finance/general-ledger/indirect-taxes-overview)

[オンライン注文用の消費税のコンフィギュレーション](sales-tax-config.md)

[トラブルシューティング: オンライン注文の税金が間違って計算される](troubleshoot/tax-miscalculated-online-order.md)
