---
title: 時刻と出勤の給与プロセスの有効化
description: この手順は、時刻と出勤の給与プロセスを有効にする方法を示します。
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72b925feb8f784c257656dd93b48c9c0cc66da5e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214917"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a>時刻と出勤の給与プロセスの有効化

[!include [banner](../../includes/banner.md)]

この手順は、時刻と出勤の給与プロセスを有効にする方法を示します。 この手順の作成に使用するデモ データの会社は USMF です。


## <a name="create-a-pay-type-with-a-related-pay-rate"></a>関連する支払レートを使用して新しい支払タイプを作成する
1. [時刻と出勤] > [設定] > [給与] > [支払タイプ]
2. [新規] をクリックします。
3. [支払タイプ] フィールドに値を入力します。
4. [説明] フィールドに値を入力します。
5. [保存] をクリックします。
6. [レート] をクリックします。
    * 支払タイプのレートは、特定の時間間隔に対して設定され、個々のレートを従業員に対して指定できます。 時間と出勤の支払タイプのレートを必ず作成する必要はありません。 この情報は、すでに従業員の給与を生成するときに使用される給与システムに存在する場合があります。  
7. [新規] をクリックします。
8. 一覧で、選択された行をマークします。
9. [レート] フィールドに数値を入力します。
10. [保存] をクリックします。

## <a name="create-a-pay-agreement"></a>支払協定の作成
1. ページを閉じます。
2. ページを閉じます。
3. [支払協定] に移動します。
    * [時刻と出勤] > [設定] > [支払協定]  
4. [新規] をクリックします。
5. [支払協定] フィールドに値を入力します。
6. [説明] フィールドに値を入力します。
7. [保存] をクリックします。
8. [契約明細行] をクリックします。
9. [新規] をクリックします。
10. 一覧で、選択された行をマークします。
11. [プロファイル タイプ] フィールドで、値を入力または選択します。
12. [支払タイプ] フィールドで値を入力または選択します。

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a>時間登録作業者の支払協定を設定する
1. ページを閉じます。
2. ページを閉じます。
3. [時間登録作業者] に移動します。
    * [時刻と出勤] > [設定] > [時間登録作業者]  
4. 一覧で、選択された行のリンクをクリックします。
5. [雇用] タブをクリックします。
6. [時間登録] セクションを展開します。
7. [編集] をクリックします。
8. [支払協定] フィールドで値を入力または選択します。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]