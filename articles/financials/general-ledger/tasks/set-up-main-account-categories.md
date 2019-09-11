---
title: 主勘定カテゴリの設定
description: このトピックでは、Dynamics 365 for Finance and Operations で主勘定カテゴリを設定する方法について説明します。
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d37deb0bda225abb111375d8a00ae22d9e0c4fe
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916071"
---
# <a name="set-up-main-account-categories"></a>主勘定カテゴリの設定

[!include [task guide banner](../../includes/task-guide-banner.md)]

このトピックでは、Dynamics 365 for Finance and Operations で主勘定カテゴリを設定する方法について説明します。 主勘定カテゴリは、財務報告と Power BI の既定のレポートに使用されます。 既定で作成される主勘定カテゴリの名前は変更できますが、削除はできません。 追加の勘定カテゴリを作成しレポートおよび分析に使用できます。 このトピックでは、USMF というデモ会社を使用します。

## <a name="create-a-main-account-category"></a>主勘定カテゴリの作成
1. ナビゲーション ウィンドウで、**モジュール > 総勘定元帳 > 勘定科目表 > 勘定 > 主勘定カテゴリ**の順に移動します。
2. **新規** を選択します。
3. **主勘定カテゴリ** フィールドに一意の名前を入力します。
4. **説明フィールド**に、主勘定カテゴリの説明を入力します。
5. **主勘定タイプ** フィールドで、カテゴリにリンクされる主勘定タイプを選択します。

## <a name="link-main-accounts-to-account-category"></a>主勘定の勘定カテゴリへのリンク
1. **主勘定をリンク**をクリックします。
2. 一覧で、主勘定カテゴリに割り当てる主勘定を選択するには、**リンク**された列のチェックボックスをオンにします。 主勘定を主勘定カテゴリに割り当てると、そのカテゴリが財務報告と分析に使用された際に勘定の残高を集計します。  
3. **リンク済**オプションを選択またはクリアして主勘定を選択します。
4. **OK** を選択します。
5. **はい**を選択します。
