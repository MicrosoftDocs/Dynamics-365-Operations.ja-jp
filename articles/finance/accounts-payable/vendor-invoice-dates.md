---
title: 仕入先請求書の日付
description: このトピックでは、仕入先請求書に表示される日付について説明します。 また、転記日付を自動的に調整するためにシステムを設定する方法も説明します。
author: sunfzam
ms.date: 2/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 064a125d448ebb3511db2d9b1f4228380805dc44
ms.sourcegitcommit: f2a78e0d7d461ca843ac2f9abff7690275db9196
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/09/2022
ms.locfileid: "8105467"
---
# <a name="vendor-invoice-dates"></a>仕入先請求書の日付

[!include [banner](../includes/banner.md)]

このトピックでは、仕入先請求書に表示される日付について説明します。 また、転記日付を自動的に調整するためにシステムを設定する方法も説明します。

**保留中の仕入先請求書の詳細** ページでは、請求書ヘッダーに 4 つの日付 (請求受信日、請求日、転記日付、および期日) が表示されます。 仕入先請求書が作成されると、次の日付が既定で入力されます。

- **請求書受領日** - このフィールドは、現在のシステム日付に設定されます。
- **転記日** - このフィールドは、現在のシステム日付に設定されます。 
- **期日** - このフィールドの日付は、転記日と支払条件に基づいて計算されます。
- **請求日** - 既定では、このフィールドは空白になります。 必要に応じて値を入力することもできます。 その場合、**期日** フィールドの日付は、請求書の日付と支払条件に基づいて再度計算されます。

時々、仕入先請求書が、期間の決済後に長い間保留中の状態になる場合があります。 転記の準備が整った場合でも、過去の転記期間の古い転記日付が使用されます。 ただし、この期間はクローズされています。 したがって、買掛金勘定 (AP) の事務員は、以前に作成された保留中のすべての請求書について、すべての転記日付を新しい転記期間に手動で変更する必要があります。

このトピックで説明する機能を使用すると、業務要件に応じて転記日付を自動的に調整するようにシステムを設定できます。

## <a name="parameter-for-automatically-adjusting-the-vendor-invoice-posting-date"></a>仕入先請求書転記日を自動的に調整するパラメータ

次の手順に従って、システムによって仕入先請求書の転記日付が自動的に調整されます。

1.  **買掛金勘定 \> 設定 \> 買掛金勘定パラメーター** の順に移動します。
2.  **元帳と売上税** タブで、**転記日付の調整自動調整** フィールドで、次のいずれかの値を選択します。

    - **変更なし** - 転記の際に転記日付は自動的に変更されません。 この値は規定で選択されています。
    - **転記日付は常にシステム日付に変更する** - 転記中は、システムによって転記日付が自動的に変更されます。
    - **転記日付期間が終了または保留状態のときに転記日付をシステム日付に変更する** - システムは、転記時に転記日付をシステム日付に変更します。ただし、転記日付の対応する期間に **終了した** または **保留中** のステータスが設定されている場合にだけ変更されます。
    - **転記日付期間が終了済みまたは保留中のときに転記日を新しい期間の最初の日に変更する** - システムは、転記日を新しくオープンした期間の最初の日に変更しますが、転記日の対応する期間に **終了した** または **保留中** のステータスが設定されている場合にだけ変更されます。

> [!NOTE]
> 自動的に調整された新しい転記日付が新しい会計年度の場合、請求書の転記日付は更新されません。 "会計年度が変更されました。 転記日付を確認し、再入力してください。" というエラーが表示されます。 請求書の転記日付は、転記する新しい会計年度日付に更新する必要があります。

## <a name="impact-of-posting-date-changes"></a>転記日の変更の影響

保留中の仕入先請求書の転記日が変更された場合、その変更によって次の影響を受します。

- **期日**

    - **請求書の日付** フィールドが空欄の場合、期限は新しい転記日と支払条件に基づいて再度計算されます。
    - **請求日** フィールドが以前に設定されている場合、転記日付の変更は 期日に影響を及ぼしません。

- **現金割引日**

    - **請求日** フィールドが空白の場合は、新しい転記日付を使用して現金割引が計算されます。
    - **請求日** フィールドが以前に設定されている場合、現金割引は変更されません。

- **為替レート** - 為替レートの日付は、**買掛金勘定パラメータ** ページ (**買掛金勘定 \> 設定 \>買掛金勘定パラメータ**) の **請求書** タブの **請求日オプションを使用して、仕入先会計の更新** の設定によって決まります。

    - このオプションが **はい** に設定されている場合は請求日が使用され、転記日付 の変更が為替レートに影響を与える影響はありません。
    - このオプションが **いいえ** に 設定 されている場合は、転記日付を使用して為替レートが計算されます。 転記日付が更新された場合、会計およびレポートの金額が再計算されます。 したがって、マッチング検証を再度実行する必要があります。

## <a name="validation"></a>検証

**買掛金勘定パラメータ** ページの **請求** タブにある他の 2 つのフィールド (**買掛金勘定 \> 設定 \> 買掛金勘定パラメータ**) は、請求書処理に影響します。

- **使用された請求書番号の確認** フィールドが **会計年度内の重複を否認** に設定されている場合は、転記日付を使用して、請求書の転記中に重複する請求書がチェックされます。
- **仕入先請求書の文書日付を要求** フィールドが **エラー オプション** に設定されている場合は、**保留中の請求書ヘッダー** フィールドの請求日が必要です。 請求日が転記日付より後の場合は、エラー メッセージが表示されます。