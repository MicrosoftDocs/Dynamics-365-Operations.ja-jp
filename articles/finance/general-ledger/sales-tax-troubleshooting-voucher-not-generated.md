---
title: 伝票が生成されない
description: この記事では、伝票を生成する必要があるが、生成しない場合に役立つトラブルシューティング情報を提供します。
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 1200fe50bf9be4c6d1ca809ad9a86da2ff3e0ced
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909014"
---
# <a name="voucher-isnt-generated"></a>伝票が生成されない

[!include [banner](../includes/banner.md)]

伝票を生成する必要があるのに、**伝票トランザクション** ページに伝票が表示されない場合、この問題のトラブルシューティングを行うには、必要に応じて次のセクションの手順に従ってください。

[![伝票がない伝票トランザクション ページ。](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)

## <a name="check-the-tax-applicability"></a>税の適用性の確認

1. **税金** \> **定期処理のタスク** \> **まだ転送されていない補助元帳仕訳エントリ** の順に移動します。
2. 仕訳帳レコードがある場合は、それを選択して、**今すぐ転送** を選択します。

    [![まだ転送されていない補助元帳仕訳エントリ ページの今すぐ転送ボタン。](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)

3. **伝票トランザクション** ページを再度開き、伝票が生成されたかどうかを確認します。

## <a name="determine-whether-customization-exists"></a>カスタマイズが存在するかどうかの確認

前のセクションの手順を完了し、問題が見つからなかった場合は、カスタマイズが存在するかどうかを確認します。 カスタマイズが存在しない場合、さらにサポートを受けるために Microsoft サービス要求を作成します。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
