---
title: Azure Active Directory からユーザーをインポートする
description: システム管理者はこの手順を使用して、選択したユーザーを手動でインポートするか、Azure Active Directory から多数のユーザーをインポートすることができます。
author: peakerbl
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56b6666310309817ff30ccb3902721880b829ee0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679817"
---
# <a name="import-users-from-azure-active-directory"></a>Azure Active Directory からユーザーをインポートする

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a>選択したユーザーのインポート

システム管理者はこの手順を使用して、Azure Active Directory (Azure AD) から選択したユーザーをインポートすることができます。

1. ユーザーは、既定の会社として現在のセッション会社と共にインポートされます。 ユーザーをインポートする前に、現在の会社を変更します。
2. **システム管理 > ユーザー > ユーザー** の順に移動します。
3. **ユーザーのインポート** をクリックします。
4. インポートするユーザーを選択し、**ユーザーのインポート** を選択します。

インポートが完了したら、ユーザーにロールを割り当てるために必要になります。

## <a name="import-users-in-bulk"></a>ユーザーの一括インポート

システム管理者はこの手順を使用して、Azure Active Directory から多数のユーザーをインポートすることができます。
バッチ インポート オプションを使用する場合は、ユーザーを選択できないことに注意してください。

## <a name="run-the-import-as-a-batch-job"></a>バッチ ジョブとしてインポート処理を実行する
1. ユーザーは、既定の会社として現在のセッション会社と共にインポートされます。 ユーザーをインポートする前に、現在の会社を変更します。
2. **システム管理 > ユーザー > ユーザー** の順に移動します。
3. **バッチ インポート** をクリックします。
4. **バックグラウンドで実行** セクションを展開します。
4. **バッチ処理** フィールドで **はい を選択します。
6. **バッチ グループ** フィールドで、値を入力または選択します。 これは、オプションのステップです。  
7. **個人** フィールドでは、**はい** を選択します。 これは、オプションのステップです。  
8. **重要なジョブ** フィールドでは、**はい** を選択します。 これは、オプションのステップです。  
9. **監視カテゴリ** フィールドでは、オプションを選択します。
10. **OK** をクリックします。

インポートが完了したら、ユーザーにロールを割り当てるために必要になります。

## <a name="run-in-a-sandbox-environment"></a>サンドボックス環境で実行
1. **バッチインポート** を選択します。
2. **OK** を選択します。
