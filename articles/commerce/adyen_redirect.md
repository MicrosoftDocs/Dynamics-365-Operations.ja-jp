---
title: 'Adyen コネクタを使用した強力な顧客認証 (Strong Customer Authentication: SCA)'
description: このトピックでは、店舗内チェックアウトにおける強力な顧客認証 (SCA) について説明します。
author: rubendel
manager: annbe
ms.date: 05/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 1388ae62001f423474f677b71704b0d7924f3cdd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980069"
---
# <a name="strong-customer-authentication-sca-using-the-adyen-connector"></a>Adyen コネクタを使用した強力な顧客認証 (Strong Customer Authentication: SCA)


[!include [banner](../includes/banner.md)]

このトピックでは、Adyen コネクタに組み込まれている強力な顧客認証 (SCA) サポートについて説明します。

## <a name="key-terms"></a>重要な用語

| 期間 | 説明 |
|---|---|
| リダイレクト | オンラインの買い物客の閲覧セッションを、販売者の店舗外に移動するアクション。 |
| SCA | 強力な顧客認証。 電子決済方法で決済する場合、オンラインで買い物をする人は、オンライン ショッピング以外で認証を受けることを義務付ける EU 決済サービス指令 2.0 (Payment Services Directive 2.0: PSD 2.0) の一部。 |
| 発行銀行 | 顧客に支払手段を発行する金融機関。 |

## <a name="overview"></a>概要

PSD 2.0 では、オンライン ショッピングのチェックアウト時に SCA がサポートされ、支払方法を発行した銀行が顧客を認証できるようにする必要があります。 認証は、通常、買い物客がオンライン注文のためにチェックアウト中で、支払詳細を提供した後に行われます。 これらの詳細は評価され、PSD2.0 の条件に基づいて顧客が銀行にリダイレクトされる場合があります。 銀行にリダイレクトされた後、顧客は支払方法に対して認証されたユーザーであることを確定するために、何らかの形式の認証を提供する必要があります。 ユーザーがカード所有者であることが確認されると、支払が既に送信された店舗にリダイレクトされ、その後、チェックアウトの続行が許可されます。 SCA が失敗した場合、そのトランザクションに対してプロセスは続行できません。

## <a name="prerequisites-for-sca-support"></a>SCA サポートの前提条件

SCA のサポートは、直ぐに使える [Adyen 向け Dynamics 365 Payment Connector](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3) によって提供されます。 これは、支払 SDK を使用するサード パーティ コネクタによって実装できます。

## <a name="setup"></a>セットアップ

設定の詳細は、支払コネクタによって異なります。 標準の Adyen コネクタに関連する設定の詳細については、Adyen コネクタ トピックの [E コマース セクション](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3#e-commerce) を参照してください。 

## <a name="functional-experience"></a>機能のエクスペリエンス

顧客が SCA にリダイレクトされると、通常、新しいブラウザ ウィンドウまたは iFrame 内で、銀行から課題が提出されます。 認証されると、チェックアウト セッションにリダイレクトされます。 検証に失敗すると、チェックアウトを続行することはできません。 

## <a name="additional-resources"></a>追加リソース

- [支払に関するよく寄せられる質問](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/payments-retail)
- [Adyen 向け Dynamics 365 Payment Connector](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)
- [チェックアウト モジュール](https://docs.microsoft.com/dynamics365/commerce/add-checkout-module)
