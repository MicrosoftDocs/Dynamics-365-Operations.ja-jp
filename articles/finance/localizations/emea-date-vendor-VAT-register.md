---
title: 仕入先 VAT 登録日
description: この記事では、仕入先 VAT 登録の日付を有効化する機能について説明します
author: AdamTrukawka
ms.date: 01/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: global
ms.author: atrukawk
ms.search.validFrom: 2022-01-15
ms.dyn365.ops.version: AX 10.0.24
ms.custom: intro-internal
ms.openlocfilehash: 4af770427f5b19eaf2a129b26d54aeacc6c2f148
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278281"
---
# <a name="date-of-vendor-vat-register"></a>仕入先 VAT 登録日

Microsoft Dynamics 365 Finance バージョン 10.0.24 では、新しい **仕入先 VAT 登録日** フィールドを仕入先請求書に使用できます。 このフィールドは、購入に対する課税対象供給の日付を指定します。

新しいフィールドを有効化する場合は、**機能管理** ワークスペースに移動し、**仕入先請求書の仕入先 VAT 登録日を有効化する** 機能を見つけて選択して、次に **今すぐ有効化** を選択します。

仕入先から受け取る請求書には日付が 2 つあります: 仕入先が請求書を発行した日付と、課税対象供給の日付 (つまり、支払うべき付加価値税 [VAT] を仕入先が請求した日付)。 シナリオによっては、これら 2 つの日付が異なる場合があります。

先に述べた両方の日付とは異なる日付に、購入請求書の受け取り VAT 金額を控除して、その請求書を VAT レポートに含めることができます。 この日付は一部のシナリオで、受領 VAT 控除の延期に関する地域の法的規則に従って制御されます。 これは国や地域によって異なります。

チェコ共和国の [VAT 管理明細書レポート](emea-cze-vat-declaration-tax-declaration-model.md#vat-control-statement) など、一部の VAT レポートでは購入ドキュメントで課税対象供給日の報告が必須です。 この日付は、税務署が取引先間の VAT 申告を照合するために報告する必要があります。

Finance では、次のフィールドで日付を定義できます。

- **請求日** – 外注業者が請求書を発行した日付。
- **VAT 登録日** – 購入請求書の VAT 金額を控除した日付。
- **仕入先 VAT 登録日** – 仕入先の課税対象供給日。
- **ドキュメント受領日** – 請求書を受け取った日付。

これらのフィールドは次のページに表示されます。

- 仕入先請求書
- 仕入先仕入帳
- 仕入先請求書の承認
- 仕入先の請求仕訳帳

仕入先請求書を転記すると、**請求仕訳帳** と **仕入先トランザクション** のページで日付を確認できます。
