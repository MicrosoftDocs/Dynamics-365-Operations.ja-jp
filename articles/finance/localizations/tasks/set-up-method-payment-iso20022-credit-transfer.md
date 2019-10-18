---
title: ISO20022 口座振替用の支払方法の設定
description: この手順では、ISO20022 口座振替の仕入先の支払方法や電子レポートを使用してファイルを生成するその他の支払タイプを設定する方法を示します。
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8bb54864c8d0a57510b4d47b00aed60c5be95512
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174939"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a>ISO20022 口座振替用の支払方法の設定

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、ISO20022 口座振替の仕入先の支払方法や電子レポートを使用してファイルを生成するその他の支払タイプを設定する方法を示します。 

このタスクを完了する前に、書式設定のコンフィギュレーションをエクスポートして支払口座を設定する必要があります。

このタスクは、デモデータ会社 DEMF を使用して作成されました。

これは、5 つのうち 3 つ目の手順で、電子レポートのコンフィギュレーションを使用する仕入先支払処理を説明しています。 この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。

1. [買掛金勘定] > [支払設定] > [支払方法] の順に移動します。
2. クイック フィルターを使用して、レコードを見つけます。 たとえば、値「SEPA CT」で [支払い方法] フィールドにフィルターを適用します。
3. [編集] をクリックします。
4. [期間] フィールドで、「合計」を選択します。
5. [支払タイプ] フィールドで、「電子支払」を選択します。
6. [ファイル形式] セクションを展開します。
7. [一般的な電子申告] フィールドで [はい] を選択します。
8. [エクスポート形式のコンフィギュレーション] フィールドで、値を入力または選択します。
    * 一覧で値「ISO20022 口座振替 (DE)」を選択します。 一覧が空の場合、仕入先支払エクスポート形式のコンフィギュレーションはインポートされず有効になりません。  
9. [勘定タイプ] フィールドで、「銀行」を選択します。
10. [支払勘定] フィールドで、値「DEMF OPER」を指定します。
11. [保存] をクリックします。

