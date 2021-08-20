---
title: POS アクセス許可グループの作成
description: このトピックでは、POS アクセス許可グループの作成方法を説明します。
author: scott-tucker
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 362fbfb5f0cae7cc8583754b53a198eae90bc67f24a871523374c4b7997826eb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762299"
---
# <a name="create-pos-permission-groups"></a>POS アクセス許可グループの作成

[!include [banner](../includes/banner.md)]

このトピックでは、POS アクセス許可グループの作成方法を説明します。 このタスクの作成に使用するデモ データの会社は USRT です。 このタスクは、Commerce 工程マネージャー ロールを対象としています。

1. ナビゲーション ウィンドウで、**モジュール > Retail と Commerce > 従業員 > アクセス許可グループ** の順に移動します。
2. **新規** を選択します。
3. **POS アクセス許可グループ ID** フィールドに、値を入力します。
4. **説明** フィールドで、値を入力します。
5. **タイム レコーダー エントリの表示** フィールドで **はい** を選択します。 これで、POS アクセス許可グループのさまざまなアクセス許可を有効、または無効にすることができます。 複数のアクセス許可に対して、POS ユーザーが操作を実行することができるかどうか評価するために使用する値を設定することができます。 このタスク ガイドは、レジ担当者に支給される可能性があるいくつかのアクセス許可を有効にします。  
6. **注文の作成を許可** フィールドで **はい** を選択します。
7. **注文の編集を許可** フィールドで **はい** を選択します。
8. **注文の取得を許可** フィールドで **はい** を選択します。
9. **パスワードの変更を許可** フィールドで **はい** を選択します。
10. **ブラインド クローズを許可** フィールドで **はい** を選択します。
11. **保存** を選択します。 変更が保存された後、Commerce チャネルへ変更をプッシュするために、スタッフ配送スケジュールを実行する必要があります。 
12. ナビゲーション ウィンドウで、**モジュール > 人事部 > ジョブ > ジョブ** の順に移動します。
13. 次に、ジョブに対して POS アクセス許可グループを割り当てます。 一覧で、目的のレコードを見つけ、選択します。
14. **編集** を選択します。
15. **ジョブ分類** セクションを展開します。
16. [POS アクセス許可グループ] フィールドで、値を入力または選択します。 作業者の POS アクセス許可が職位のレベルで上書きされない場合、このジョブの職位のすべての作業者は、この POS アクセス許可グループの設定を使用します。  
17. **保存** を選択します。 変更が保存された後、チャネルへ変更をプッシュするために、スタッフ配送スケジュールを実行する必要があります。  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]