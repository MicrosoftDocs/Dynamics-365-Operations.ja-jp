---
title: B2B e コマース Webサイトの請求書管理
description: このトピックでは、Microsoft Dynamics 365 Commerce 企業間 (B2B) の e コマース Web サイトの請求書管理機能について説明します。
author: shajain
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 60cb0c8aaede4a0eaeed80cf5ebe41068da57836
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686303"
---
# <a name="invoice-management-for-b2b-e-commerce-websites"></a>B2B e コマース Webサイトの請求書管理

[!include [banner](../../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce 企業間 (B2B) の e コマース Web サイトの請求書管理機能について説明します。

顧客貸方での注文を受け入れる B2B トランザクションをおこなう会社では、注文を処理した後に顧客に請求書を送るのが一般的です。 支払条件は顧客に対して定義され、時間や時間の前に支払を行う顧客を動機付けるいくつかの割引がある場合があります。 支払いを期日までに受け取る確立を上げるのに役立てるために、B2B e コマースの Web サイトでは、顧客が自分たちのすべての請求書を閲覧できるようにします。 顧客は簡単に請求書をフィルター処理して、支払済、未払、部分的に支払済の請求書を期日と共に表示できます。

![B2B Web サイトの請求書ページ。](../media/ViewInvoices.png)

> [!NOTE]
> サインインしたユーザーは、自分の請求書のみを表示して支払を行うことができます。 Commerce 本部の顧客レコードの **請求書と納品** クイック タブ上にある **請求先アカウント** ドロップダウン メニューに組織 ID が構成されている場合は、ユーザーは組織アカウントの請求書を表示して支払を行うことができます。

B2B Web サイトの **請求書** ページで、ユーザーは未払または部分的に支払われた請求書を選択し、**請求書を支払う** を選択できます。 選択した請求書がカートに追加され、ユーザーは支払を続行できます。 その後、ユーザーは、請求書の全額または一部を支払うかどうかを選択できます。 ユーザーはアカウント上の支払い方法を使って請求書を支払うことはできません。

> [!NOTE]
> 請求書は、現在カートに品目が入っていない場合にのみ、カートに追加できます。 逆に、品目は、現在請求書がカートにない場合のみカートに追加できます。 Microsoft は、Commerce の今後のリリースでこの制限を削除する予定です。

![B2B の Web サイト上のカート ページ。](../media/PayInvoice.png)

**請求書** ページ では、ユーザーが請求書 の横にある **請求書の要求** を選択することもできます。 これにより、請求書の詳細を登録済の電子メール アドレスに送信できます。

![請求書のダイアログ ボックスを要求します。](../media/RequestInvoice2.png)

ユーザーが請求書を要求すると、その要求は **マイ アカウント** ページの **B2B 要求** セクションに移動されます。 その後、**P-0001** および Commerce 本部で **注文およびチャンネル要求の同期** ジョブを実行した後、請求書の電子メールがトリガーされ、B2B 要求のステータスが完了とマークされます。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
