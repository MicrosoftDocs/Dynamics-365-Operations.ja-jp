---
title: トランザクションと領収書メールに QR コードまたはバーコードを追加
description: このトピックでは、注文 ID を Microsoft Dynamics 365 Commerce のトランザクションと領収書メールに表す QR コードおよびバーコードの入力方法を説明します。
author: bicyclingfool
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 791b244c867ea4263f08250abf220a1b75784cad
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907866"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a>トランザクションと領収書メールに QR コードまたはバーコードを追加

[!include [banner](includes/banner.md)]

このトピックでは、注文 ID を Microsoft Dynamics 365 Commerce のトランザクションと領収書メールに表す QR コードおよびバーコードの入力方法を説明します。

小売環境での注文ルックアップ プロセスを速くするために、トランザクションの電子メールに簡単に QR コードとバーコードを含めることができます。 電子メールに QR コードとバーコードを挿入するには、生成および表示サービスから QR コードとバーコード イメージを要求する HTM **\<img\>** タグを使用します。 Microsoft は、このサービスを提供しません。 ただし、クエリ文字列に渡された値に基づき、動的に生成される QR コードまたはバーコードを出すたくさんの無料または安いサービスがあります。

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a>トランザクション電子メールに QR コードまたはバーコードを追加

E コマース購買の一部として送信されるトランザクション電子メールに、QR コードまたはバーコードを挿入するには、次の手順に従います。

1. トランザクション電子メール テンプレートのソース HTML を開き、QR コードまたはバーコード サービスにポイントする HTML **\<img\>** タグを追加します。 次に例を示します。

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    前例の内容について説明します:

    - **YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** は、QR コードまたはコード サービスのドメインを表します。
    - **データ** は、QR コードまたはバーコード サービスが、QR コードまたはバーコードとしてレンダリングする必要があるコンテンツを受け取るために使用するパラメータをー表します。

        その値 **%salesid%** は、パラメーターに割り当てる必要があります。 この例では、値がイメージの代替テキストとしても使用されます。

    - **param1** および **param2** は、追加のオプション パラメーターを表します。

1. **小売とコマース \> 本社の設定 \> パラメーター \> 組織の電子メール テンプレート** に移動し、更新済の HTML を適切なトランザクション電子メール テンプレートにアップロードします。

> [!NOTE]
> パラメーターは、QR コードとコード サービス プロバイダ間で異なる場合があります。 したがって、値を割り当てる必要があるパラメータを確認するために、サービス プロバイダーに問い合わせしてください。

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a>領収書メールに QR コードまたはバーコードを追加 

販売時点設定 (POS) で購買が行われた後に送信するレシートの電子メールに、QR バーコードまたはバーコードを挿入するには、次の手順に従います。

1. 領収書メール テンプレートのソース HTML を開き、QR コードまたはバーコード サービスにポイントする HTML **\<img\>** タグを追加します。 次に例を示します。

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    前例の内容について説明します:

    - **YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** は、QR コードまたはコード サービスのドメインを表します。
    - **データ** は、QR コードまたはバーコード サービスが、QR コードまたはバーコードとしてレンダリングする必要があるコンテンツを受け取るために使用するパラメータをー表します。

        その値 **%receiptid%** は、パラメーターに割り当てる必要があります。 この例では、値がイメージの代替テキストとしても使用されます。

    - **param1** および **param2** は、追加のオプション パラメーターを表します。

1. **小売とコマース \> 本社設定 \> パラメーター \> 組織の電子メール テンプレート** に移動し、更新済の HTML を電子メール ID **emailrecpt** を持つ電子メール テンプレートにアップロードします。

> [!NOTE]
> パラメーターは、QR コードとコード サービス プロバイダ間で異なる場合があります。 したがって、値を割り当てる必要があるパラメータを確認するために、サービス プロバイダーに問い合わせしてください。

## <a name="additional-resources"></a>追加リソース

[Modern POS (MPOS) からの電子メール レシートの送信](email-receipts.md)

[トランザクション イベント用の電子メール テンプレートの作成](email-templates-transactions.md)
