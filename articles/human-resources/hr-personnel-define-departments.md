---
title: 新しい部門の定義
description: 部門は、販売または会計など、事業の機能領域を表す作業単位です。
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMOperatingUnit, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 06b93e9b7bd4d68aa5d6f6c377991963e37579ae
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464407"
---
# <a name="define-new-departments"></a>新しい部門の定義

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



部門は、販売または会計など、事業の機能領域を表す作業単位です。 多くの会社には、事業内のさまざまな部門を表示する組織階層があります。 この手順では、部門を作成し、作成した部門を組織内の部門階層に追加するプロセスを説明します。 この手順の作成に使用するデモ データの会社は USMF です。

1. [人事管理] > [部門] > [部門] の順に移動します。
2. [新規] をクリックすると、ドロップ ダイアログが開きます。
3. [名前] フィールドに値を入力します。
    * 例: プロジェクトの請求書作成  
4. [メモ] フィールドに値を入力します。
    * 例: プロジェクトの請求書作成  
5. [マネージャー] フィールドで、値を入力または選択します。
    * 例: Jodi Christiansen  
6. [保存] をクリックします。
7. ページを閉じます。
8. [人事管理] > [部門] > [部門階層] の順に移動します。
9. [編集] をクリックします。
10. [挿入] をクリックします。
11. [部門] をクリックします。
12. 一覧で、目的のレコードを見つけ、選択します。
    * 例: プロジェクトの請求書作成  
13. [OK] をクリックします。
14. [発行] をクリックして、ドロップ ダイアログを開きます。
15. [有効日] フィールドに日時を入力します。
    * 部門の階層を公開する際、変更をいつ有効にするかを選択できます。 変更を将来の日付にすることもできます。 たとえば、次の会計年度の期首に追加の部門を追加することがわかっている場合があります。 会計年度の期首に有効日を設定すれば、階層の変更はその日付に有効になります。  
16. [変更の説明] フィールドで、値を入力します。
17. [発行] をクリックします。



[!INCLUDE[footer-include](../includes/footer-banner.md)]