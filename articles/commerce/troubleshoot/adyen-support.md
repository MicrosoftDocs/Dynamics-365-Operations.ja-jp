---
title: Adyen 向け Dynamics 365 Payment Connector に関する問題のトラブルシューティング
description: この記事では、Adyen 向け Microsoft Dynamics 365 Payment Connector に関する問題が発生した場合のサポートに役立つトラブルシューティング ガイドを提供します。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 687f2fdff5e29cc25fae911b015164f0d90aee88
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268868"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a>Adyen 向け Dynamics 365 Payment Connector に関する問題のトラブルシューティング

[!include [banner](../../includes/banner.md)]

この記事では、Adyen 向け Microsoft Dynamics 365 Payment Connector に関する問題が発生した場合のサポートに役立つトラブルシューティング ガイドを提供します。

## <a name="description"></a>説明

次の領域の Adyen 向け Dynamics 365 Payment Connector に問題があり、Adyen チームのサポートが必要です。

- 販売時点管理 (POS) の構成、Modern 販売時点管理 (MPOS)、コール センター、および Dynamics 365 Commerce
- Adyen 支払サービス プロバイダ (PSP) 参照番号 (たとえば、手動キー入力 \[MKE\] 拒否を含む、拒否について質問がある場合)
- テスト環境またはライブ マーチャント環境で機能していないもの

## <a name="resolution"></a>解像度

Adyen チームでプロセスをサポート開始するには、次の電子メール テンプレートを使用します。 トラブルシューティングを迅速化するには、電子メールに必要なすべての詳細が含まれている必要があります。

| フィールド        | 先頭値 |
|--------------|-------|
| 宛先           | `support@adyen.com` |
| cc           | |
| 件名 | Microsoft Dynamics サポート リクエスト |
| 本文         | <p>こんにちは サポート、</p><p>以下の問題についてサポートを提供してください:</p><ul><li>マーチャント口座</li><li>環境 (Test/Prod)</li><li>チャンネル (POS/ コール センター / コマース電子商取引)</li><li>PSP 参照番号、問題が特定のトランザクションに関係している場合 (Adyen Customer Area、または POS ターミナルのトランザクション メニューにある PSP 参照番号を参照できます。)</li><li>該当する場合、エラー メッセージのスクリーンショットまたは写真</li><li>イベント ビューアー ログ (.txt 形式)</li><li>問題と試したトラブルシューティングの手順</li></ul> |

## <a name="additional-resources"></a>追加リソース

[Dynamics 365 Commerce の Adyen コネクタで支払を受取る](https://www.adyen.com/partners/dynamics-365-commerce)

[Adyen 向け Dynamics 365 Payment Connector](../dev-itpro/adyen-connector.md)

[Dynamics 365 の Adyen 支払コネクタを設定](https://docs.adyen.com/plugins/microsoft-dynamics)
