---
title: 仕入先勘定の作成
description: この手順では、仕入先勘定の作成方法と住所および連絡先情報の追加方法を示します。
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22c7a1a2b7468f00aa25a67a2c5f62b088e2fe7c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546182"
---
# <a name="create-a-vendor-account"></a>仕入先勘定の作成

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、仕入先勘定の作成方法と住所および連絡先情報の追加方法を示します。 この手順では、購買目的および財務目的のためのすべてのフィールドを設定する方法は表示されません。 これらのフィールドについての詳細は、フィールドの説明を参照してください。 デモ データの会社 USMF のこの手順を使うか、または独自のデータを使うことができます。 通常、仕入先勘定は、調達担当者または売掛金勘定担当者によって作成されます。


## <a name="create-a-vendor-account"></a>仕入先勘定の作成
1. [調達] > [仕入先] > [すべての仕入先] の順に移動します。
2. [新規] をクリックします。
3. [仕入先] フィールドに値を入力します。
    * フィールドには自動的に値を入力できる場合があります。 その場合、この手順を省略できます。  
    * 個人または組織の仕入先勘定を作成できます。 この操作は、フィールドが使用可能になるときに影響します。 この例では、組織の仕入先勘定を作成します。   
4. [名前] フィールドで値を入力または選択します。
    * 仕入先が既にシステムに登録されている当事者である場合、このフィールドでドロップダウンを使用し、仕入先を選択できます。また、新しい仕入先勘定では、既に登録されている住所と連絡先情報を継承します。  
5. [グループ] フィールドで、値を入力または選択します。
    * 仕入先グループは、次の共通のパラメータを持つ仕入先をグループ化するために使用されます。支払条件、決済期間、売上税グループを含む在庫転記の勘定科目、既定の勘定科目、製品のフィルター コードおよび供給予測コンフィギュレーション。  
6. [従業員数] フィールドに数値を入力します。
7. [組織番号] フィールドに値を入力します。

## <a name="add-an-address"></a>住所の追加
1. [住所] セクションを展開します。
2. [追加] をクリックします。
3. [目的] フィールドで、値を入力または選択します。
    * 1 つ以上の目的を選択できます。 これらは該当する目的に正しい住所を選択するために使用されます。 たとえば、目的が「請求書」であれば、請求書を送付するときに住所が使用されます。  
4. [名前または説明] フィールドに値を入力します。
5. [国/地域] フィールドで、値を入力または選択します。
    * 住所の詳細を入力します。 選択した国/地域により、国/地域の住所の形式に対応して、表示されるフィールドが決まります。   
6. [OK] をクリックします。

## <a name="add-contact-information"></a>連絡先情報の追加
1. [追加] をクリックします。
2. [説明] フィールドに値を入力します。
3. [タイプ] フィールドで、オプションを選択します。
4. [連絡先の電話番号/住所] フィールドに値を入力します。
    * これが基本連絡先である場合は、この [主要] チェック ボックスを選択できます。  
5. [保存] をクリックします。
6. ページを閉じます。
7. ページを閉じます。

