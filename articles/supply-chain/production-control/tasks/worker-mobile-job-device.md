---
title: モバイル ジョブ デバイスを使用した作業者のコンフィギュレーション
description: このトピックでは、作業者のユーザー アカウントに適切なロールを割り当てる方法を表示します。それによって、作業者が作業現場の登録を行う方法を説明します。
author: ShylaThompson
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6210cdeed99f26a6b58b75d9f5405c0e1ee5aef1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213333"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>モバイル ジョブ デバイスを使用した作業者のコンフィギュレーション

[!include [banner](../../includes/banner.md)]

このトピックでは、作業者のユーザー アカウントに適切なロールを割り当てる方法を表示します。それによって、作業者が作業現場の登録を行う方法を説明します。

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a>作業者に特定のロールが割り当てられていることを確認する

この例では、作業者アカウントを構成する前に、ユーザー "SHANNON" に機械オペレータのロールが割り当てられていることを確認します。

1. **ナビゲーション ウィンドウ > モジュール > システム管理 > ユーザー > ユーザー** の順に移動します。
2. クイック フィルターでユーザーを検索します。 この例では、`shannon` を入力します。
3. 表示されるユーザー アカウントの **ユーザー ID** 列のリンクを選択します。
4. **ユーザーのロール** ツリーで、**ロール > 機械オペレーター** を選択します。
5. **ユーザーの詳細** ページと **ユーザー** ページを閉じて、ホーム ページに戻ります。

## <a name="configure-worker-account"></a>作業者のアカウンの構成
1. **ナビゲーション ウィンドウ > モジュール > 人事部 > 作業者 > 作業者** の順に移動します。
2. クイック フィルターでユーザーを検索します。 この例では、`shannon` を入力します。
3. 表示されるユーザー アカウントの **名前** 列のリンクを選択します。
4. **時間登録** タブを選択します。
5. **登録ターミナルで有効化** を選択します。
6. 次のフィールドで値を入力または選択します。  

    - **計算グループ**  
    - **既定の計算グループ**  
    - **承認グループ**  
    - **標準プロファイル**  
    - **プロファイル グループ**  

7. **OK** を選択します。
8. **編集** を選択して、新しい時間登録作業者のバッジ番号を入力します。 **バッジ ID** フィールドで値を入力します。
9. **保存** を選択します。
10. **作業者の詳細** と **作業者** のページを閉じます。

## <a name="assign-worker-to-device-group"></a>デバイス グループに作業者を割り当てる
1. **生産産管理 > 設定 > 製造実行 > デバイスのジョブ カードのコンフィギュレーション** の順に移動します。
2. **追加** を選択します。
3. 一覧で、目的の作業者を選択します。 この例では、**SHANNON** を選択します。
4. **OK** を選択します。
5. **編集** を選択します。
6. **生産単位** フィールドで、作業者の既定のフィルターを設定できます。 これにより作業者がデバイスにログオンするときに、選択した生産単位の生産ジョブのみが表示されます。 目的の値の入力します。
7. ページを閉じます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]