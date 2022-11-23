---
title: Dynamics 365 Commerce での前払い
description: この記事では、Microsoft Dynamics 365 Commerce における前払いトランザクションの処理の概要を示します。
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-06-28
ms.openlocfilehash: 8262470f83481ef8840857a52948c0833d8b278e
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780362"
---
# <a name="prepayments-in-dynamics-365-commerce"></a>Dynamics 365 Commerce での前払い

[!include[banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce における前払いトランザクションの処理の概要を示します。

Dynamics 365 Commerce は、売掛金勘定または Commerce で使用される次の支払タイプの前払トランザクションを処理します。

- **顧客勘定預金の支払** – 顧客が販売時点管理 (POS) で前金を支払います。 Commerce は、前金支払を前払いトランザクションとして処理します。 トランザクションを転記すると、支払仕訳帳が作成され、Commerce Headquarters の **仕訳伝票** ページに転記されます。 支払仕訳帳では、**支払** タブの **前払仕訳伝票** チェック ボックスが自動的に選択されます。 ターゲット地域に関連する前払いや税固有の情報などの詳細については、[グローバリゼーション リソース - 国/地域固有のヘルプ コンテンツ](/dynamics365/fin-ops-core/dev-itpro/lcs-solutions/country-region?context=%2Fdynamics365%2Fcontext%2Ffinance#countryregion-specific-help-content)を参照してください。
- **前金がある顧客注文** – 顧客は POS で顧客注文を作成します。 顧客は、Commerce Headquarters の **顧客注文** ページで構成されている既定の前金率に基づいて注文の預金を支払います (**Commerce パラメーター \> 顧客注文**)。 Commerce は、顧客注文の前金支払を前払いトランザクションとして処理します。 トランザクションを転記すると、支払仕訳帳が作成され、**仕訳伝票** ページに転記されます。 支払仕訳帳では、**支払** タブの **前払仕訳伝票** チェック ボックスが自動的に選択されます。 支払が決済され、注文が受け取られたか配送された際に顧客請求書が自動的に発行されます。
- **コール センター販売注文** - コール センターのカスタマー サービス担当者が顧客に代わって販売注文を作成し、支払のキャプチャ時に **前払** 属性が **はい** に設定されます。

Commerce では、前払を処理するために次の作業を実行します。

- **顧客勘定預金の支払の処理** – 顧客が行う前金支払は、データを同期するサービスを使用して Commerce に転送されます。 Commerce によって、支払の小売支払トランザクションが作成されます。 小売トランザクションを転記すると、現金仕訳帳または顧客支払仕訳帳が転記されます。 支払仕訳帳に対して、Commerce Headquarters の **仕訳伝票** ページの **支払** タブにある **前払仕訳伝票** のチェック ボックスが自動的に選択されます。 支払金額が負の場合、前払は処理されません。
- **前金がある顧客注文または販売注文を処理する** – Commerce Data Exchange: リアルタイム サービスを使用して、顧客が顧客注文に対して要求された前金を支払います。 Commerce では、顧客が使用する支払方法に応じて、顧客支払仕訳帳または現金仕訳帳が作成されます。 仕訳帳に対して、Commerce Headquarters の **仕訳伝票** ページの **支払** タブにある **前払仕訳伝票** のチェック ボックスが自動選択されます。 顧客が複数の支払方法を使用して部分支払を行う場合、Commerce は使用された支払方法に基づいてそれぞれの部分支払を処理します。

クレジット カードおよびクレジット カードの支払方法が基になるデジタル サービスの場合、Commerce は認証が成功した後に "キャプチャ" 要求を送信します。 (販売注文の請求を行う前に、資金がキャプチャされます。)

顧客注文をキャンセルすると、前払金額が払戻され、前金に対して払戻支払仕訳帳が転記されます。 払戻金額は、払戻しの支払を転記するときに指定した支払方法に基づいて計算および転記されます。 Commerce では、Commerce Headquarters の **Commerce パラメーター** ページで設定したパーセントに基づいてキャンセル料を適用する場合があります。

顧客注文を返品すると、返品注文および払戻支払仕訳帳が作成されます。 返品注文を転記すると、元のトランザクションに対して顧客が使用した支払方法に応じて、顧客支払仕訳帳または現金仕訳帳が作成されます。
