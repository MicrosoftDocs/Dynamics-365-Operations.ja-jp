---
title: 発注書フォームと販売注文フォームを使用した TDS 請求書の計算
description: このトピックでは、様々なタイプの請求書のソース (TDS) で税控除を計算する手順を示します。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: e7925206f3c060c6332de9d4972c8a7fb0066be2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023378"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a>発注書フォームと販売注文フォームを使用した TDS 請求書の計算

[!include [banner](../includes/banner.md)]

このトピックでは、**発注書**、**購買仕訳帳**、**一括発注**、**販売注文** の各ページをを使ってさまざまな種類の請求書の源泉徴収税 (TDS) を計算する手順を紹介します。

1. 一覧表示されたページを使用して、発注書、購買仕訳帳、購買一括注文、または販売注文を作成します。 必要な詳細情報を入力します。

2. **設定** タブを選択して、仕入先または顧客の被査定者の性質を表示します。 この情報は、**源泉徴収税グループ** フィールド グループの **被査定者の性質** フィールド に一覧表示されます。

3. **TDS グループ** フィールドで、仕入先や顧客に対して定義されている既定の TDS グループを確認または変更します。

   > [!NOTE]
   > **TDS グループ** フィールドで TDS グループを選択すると、**TCS グループ** フィールドは使用できなくなります。 TDS は、**すべての仕入先** または **すべての顧客** ページで、仕入先または顧客の **源泉徴収税を計算する** チェックボックスが選択されている場合にのみ計算されます。  

4. **明細行** タブで品目を作成し、必要な詳細情報を入力します。

5. ヘッダー レベルで定義されたTDSグループを表示または変更するには、**設定** タブ (行レベル) を選択します。 TDS グループは、**TDS グループ** フィールド、**源泉徴収税グループ** のフィールド グループの下に表示されます。

6. **税金情報** タブを選択し、このフィールドに表示されている会社名に設定されている代替アドレスを選択します。 **名前** フィールドの **会社情報** フィールドグループの下に会社名が表示されます。 

   選択された会社名の TAN は、**源泉徴収税フィールド** グループの下の **税口座番号** (**TAN**) フィールドに表示されます。 

7. **源泉徴収税** を選択し、**一時源泉徴収税トランザクション** ページを開きます。 **一時源泉徴収票** ページの上部ペインで、以下のフィールドで確認できます。

   - **合計源泉徴収税額** – TDS グループのトランザクションに対して計算された TDS の合計です。

   - **値** – トランザクションの TDS の計算に使用された合計割合です。 合計割合は、TDS 税コードに対して定義され、TDS グループに関連付けられた式に基づきます。

   - **合計調整済源泉徴収税額** – TDS グループのすべての税コードに対する調整済 TDS 金額の合計です。

   - **TDS** - これが選択されている場合、TDS グループはトランザクションに関連付けされます。

**一時源泉徴収票トランザクション** ページの **概要**、**一般**、 **調整** タブのフィールドには、TDS グループに属する各 TDS 税コードの計算された TDS 金額と調整された TDS 金額の詳細が表示されます。

8. **しきい値** を選択すると、**しきい値** ページが開きます。 このページでは、特定の TDS 税コードに関連付けられた TDS 税コンポーネントに定義されたしきい値を確認できます。

9. **式デザイナー** を選択して **式デザイナー** ページを開きます。 このページでは、特定の TDS 税コードに定義された計算式が表示されます。 

10. 請求書を転記します。 購買請求書で計算された TDS 金額が買掛金勘定に転記され、売上請求書で計算された TDS 金額が TDS グループの各 TDS 税コードに対して定義されている売掛金勘定に転記されます。 TDS 税コードの買掛金勘定や売掛金勘定は、**源泉徴収税コード** ページで定義されます。

11. **照会** ボタン **> 請求書 > 転記済み源泉徴収税** ボタンを選択し、**源泉徴収税トランザクション** ページを開きます。 **値** フィールドには、当該取引の TDS 計算に使用された合計パーセンテージを確認できます。

**源泉徴収税トランザクション** ページの **概要** タブ、**一般** タブ、および **金額** タブの各フィールドには、トランザクションに対して計算された TDS の情報が表示されます。 TDS グループに関連付けられた各 TDS 税コードの TDS 計算情報が表示されます。