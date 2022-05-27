---
title: 新しい部門の定義
description: 部門は、販売または会計など、事業の機能領域を表す作業単位です。
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OMOperatingUnit, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c90628b6a1aa4c1ff899b9caaa804af6e02b7afb
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693699"
---
# <a name="define-new-departments"></a>新しい部門の定義


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



部門は、販売または会計など、事業の機能領域を表す作業単位です。 多くの会社には、事業内のさまざまな部門を表示する組織階層があります。 この手順では、部門を作成し、作成した部門を組織内の部門階層に追加するプロセスを説明します。 この手順の作成に使用するデモ データの会社は USMF です。

1. **人事管理** > **部門** > **部門** の順に移動します。
2. **新規** をクリックすると、ドロップ ダイアログが開きます。
3. **名前** フィールドに値を入力します。
    * 例: プロジェクトの請求書作成  
4. **メモ** フィールドに値を入力します。
    * 例: プロジェクトの請求書作成  
5. **マネージャー** フィールドで、値を入力または選択します。
    * 例: Ana Bowman  
6. **保存** をクリックします。
7. ページを閉じます。
8. **人事管理** > **部門** > **部門階層** の順に移動します。
9. **編集** をクリックします。
10. **挿入** をクリックします。
11. **部門** をクリックします。
12. 一覧で、目的のレコードを見つけ、選択します。
    * 例: プロジェクトの請求書作成  
13. **OK** をクリックします。
14. **発行** をクリックして、ドロップ ダイアログを開きます。
15. **有効日** フィールドに日時を入力します。
    * 部門の階層を公開する際、変更をいつ有効にするかを選択できます。 変更を将来の日付にすることもできます。 たとえば、次の会計年度の期首に追加の部門を追加することがわかっている場合があります。 会計年度の期首に有効日を設定すれば、階層の変更はその日付に有効になります。  
16. **変更の説明** フィールドで、値を入力します。
17. **発行** をクリックします。



[!INCLUDE[footer-include](../includes/footer-banner.md)]
