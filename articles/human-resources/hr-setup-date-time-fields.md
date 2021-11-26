---
title: 日付と時刻のフィールドの理解
description: このトピックでは、Microsoft Dynamics 365 Human Resources で日付と時刻フィールドを使用する際の予想事項を把握します。
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 06c783c1e4a2961f1445909ea03d557c0985064e
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2021
ms.locfileid: "7728592"
---
# <a name="understand-date-and-time-fields"></a>日付と時刻のフィールドの理解

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**日付と時刻** フィールドは、Microsoft Dynamics 365 Human Resources の基本的な概念です。 ページ、Dataverse、外部ソースにおいて **日付と時刻** データを操作する方法を理解しておくことが重要です。

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>日付フィールドと日付と時刻フィールドのデータ型の違いを理解する

**日付と時刻** フィールドにはタイム ゾーン情報が含まれますが、**日付** フィールドには含まれません。 **日付** フィールドには、どの場所でも同じ情報が表示されます。 日付を **日付** フィールドに入力すると、同じ日付がデータベースに書き込まれます。

**日付と時刻** フィールドにデータを表示する場合、**ユーザー オプション** ページで選択されたユーザーのタイム ゾーンに基づいて、日付と時刻が調整されます (**共通 \> 設定 \> ユーザー オプション**)。 フィールドに入力した日付と時刻の情報は、データベースに書き込まれた情報とは異なる場合があります。

[![ユーザー オプション ページ。](./media/Useroptionsform.png)](./media/Useroptionsform.png)

## <a name="understanding-date-and-time-fields-on-pages"></a>ページの日付と時刻のフィールドを理解する 

ユーザーのタイムゾーンが協定世界時 (UTC) に設定されていない場合、画面に表示される **日付と時刻** データはデータベースに保存されているデータとは異なります。 **日付と時刻** フィールドのデータは、常に UTC として保存されます。

[![作業者ページ UTC。](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>データベースの日付と時刻のフィールドを理解する 

**日付と時刻** の値がデータベースに書き込まれる際、データは UTC で保存されます。 そのため、ユーザーは、ユーザー オプションで定義されたタイムゾーンに関連する **日付と時刻** のデータを参照できます。
 
上記の例では、開始時刻は特定の日付ではなく特定時点の時刻です。 ログインしているユーザーのタイム ゾーンを [GMT +12:00] から [GMT UTC] に変更すると、作成されたレコードが [05/01/2019 12:00:00] ではなく [04/30/2019 12:00:00] と表示されます。

次の例では、従業員 000724 の雇用が、タイム ゾーンに関係なく同時に有効になります。 従業員は GMT タイム ゾーンの 04/30/2019 で有効になり、GMT + 12:00 タイムゾーンの 05/01/2019 と同じになります。 どちらも、特定の日付ではなく、同じ特定時点を参照します。 

[![作業者ページ GMT。](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a>データ管理フレームワーク、Excel、Dataverse、および Power BI における日付と時刻のデータ 

データ管理フレームワーク (DMF)、Excel アドイン、Dataverse、および Power BI レポートは、データベース レベルでデータを直接操作できるように設計されています。 **日付と時刻** のデータをユーザーのタイム ゾーンに調整するクライアントは存在しないため、**日付と時刻** の値はすべて UTC となり、データの入力や表示の際に誤った認識につながる可能性があります。
 
**日付と時刻** データが DMF、Excel、または Dataverse を介して送信されると、データベースによって UTC と見なされます。 ただし、データを表示するユーザーのタイム ゾーンが UTC に設定されていない場合、送信された **日時** の値は正常に表示されず、ユーザーが混乱する可能性があります。 
 
データがエクスポートされると、同じことが逆に発生する可能性があります。 エクスポートされた DMF エンティティの **日付と時刻** データは、Dynamics クライアントに表示されるものとは異なる場合があります。 
 
DMF などの外部ソースを使用してデータを表示または作成する場合、ユーザーのコンピューターのタイム ゾーンや現在のユーザーのタイム ゾーンの設定に関係なく、**日付と時刻** の値は既定で UTC であると見なされる点にご注意ください。 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>同じレコードが異なる製品領域に表示されている例 

**UTC に設定されているユーザー タイム ゾーンのある Human Resources**

[![作業者ページを UTC に設定。](./media/worker-form3.png)](./media/worker-form3.png)

**GMT +12:00 に設定されているユーザー タイム ゾーンのある Human Resources** 

[![作業者ページを GMT に設定。](./media/worker-form4.png)](./media/worker-form4.png)

**OData を介した Excel**

[![OData を介した Excel。](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMF ステージング**

[![DMF ステージング。](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMF エクスポート**

[![DMF エクスポート。](./media/DMFExport.png)](./media/DMFExport.png)

**Dataverse を介した Excel**

[![Dataverse を介した Excel。](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>参照

[日付と時刻データ](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[ユーザーの優先タイム ゾーン](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
