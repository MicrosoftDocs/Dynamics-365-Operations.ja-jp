---
title: 新しい部門の定義
description: 部門は、販売または会計など、事業の機能領域を表す作業単位です。
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMOperatingUnit, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e8b109a16aa96f0d87776d6965c20808ee6f6fce
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009652"
---
# <a name="define-new-departments"></a>新しい部門の定義



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

