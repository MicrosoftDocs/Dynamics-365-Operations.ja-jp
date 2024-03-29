---
title: アクティベーション アカウントの管理とデバイスの検証
description: この記事では、作業者が Modern POS デバイスまたはクラウド POS デバイスを有効にするためにコマース アクティベーション アカウントを IT Pro で設定する方法について説明します。
author: josaw1
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 20471
ms.assetid: 5394e10c-539c-4e26-a097-504c6950cd56
ms.search.industry: Retail
ms.search.form: HcmWorker, RetailDeviceActivationValidation, RetailPositionPosPermission
ms.openlocfilehash: 7668bcbdb7f33767d1290e11e6c346d0330bb936
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286768"
---
# <a name="manage-activation-accounts-and-validate-devices"></a>アクティベーション アカウントの管理とデバイスの検証

[!include [banner](includes/banner.md)]

この記事では、作業者が Modern POS デバイスまたはクラウド POS デバイスを有効にするためにコマース アクティベーション アカウントを IT Pro で設定する方法について説明します。

## <a name="setting-up-a-device-activation-account-for-a-single-worker"></a>1 人の作業者のデバイス有効化アカウントの設定

この手順は、クラウド POS を有効化する前に完了する必要があります。

1. コマースで、**作業者** ページから、作業者の **作業者の詳細** ページを開き、AAD 有効化権限を割り当てます。 **編集** をクリックします。
2. **コマース** タブで、**POS アクセス許可** リンクをクリックします。 作業者がマネージャー アクセス許可グループにあるか、**デバイスの管理** が作業者に対して **はい** に設定されていることを確認します。
3. **コマース** タブの、**外部 ID** で、次のフィールドの値を更新します。

    - エイリアス
    - UPN
    - 外部識別子

4. 既存の AAD アカウントを使用するか、または新しい AAD アカウントを作成して、**外部 ID** フィールドを更新することができます。 フィールドを更新するには、**コマース** メイン メニュー (**コマース**&gt;**既存の ID の関連付け** または **コマース**&gt;**新しい ID の作成**) から **外部 ID** オプションにアクセスします。
5. 既存の AAD アカウントを使用するには、**コマース**&gt;**既存の ID の関連付け** を選択します。 スライダーで、正確な名前を持つ AAD アカウントをクリックしてから **OK** をクリックします。 その名前とエイリアスに関連付けられている AAD アカウントは、Modern POS のユーザーの有効化アカウントです。
6. 完了し、変更を **作業者** ページに保存し、ページを更新します。 外部 ID 情報を含むセクションは、新しい情報で更新する必要があります。 マッピングされた AAD アカウントは、Cloud POS と Modern POS のユーザーの有効化アカウントになりました。 このアカウントは、POS アクセス許可が必要な作業者にマップされます。 Modern POS または POS の有効化に、この AAD アカウントを使用できます。
7. 外部 ID 作成機能は、入力したエイリアスを使用することにより新しい AAD アカウントを作成します。 フィールドを更新するには、**コマース** メイン メニュー (**コマース** &gt; **新しい ID の作成**) から **外部 ID** オプションにアクセスします。
8. 生成するエイリアスを手動で入力するか、**既定値にリセット** ボタンを使用することができます。 その後強力なパスワードを手動で入力し、**OK** をクリックします。
9. 作業者が正常に作成された場合、**作業者** ページにメッセージが表示されます。 マッピングされた AAD アカウントは、Cloud POS と Modern POS のユーザーの有効化アカウントになりました。 このアカウントは、POS アクセス許可が必要な作業者にマップされます。 Modern POS または POS の有効化に、この AAD アカウントを使用できます。

## <a name="setting-up-device-activation-accounts-for-multiple-workers"></a>複数の作業者のデバイス有効化アカウントの設定

複数の作業者のアクティベーション アカウントをバルクで設定することができます。 ただし、この機能は ID を関連付けるのでなく、新しい外部 ID を作成する場合にのみサポートされます。

1. 作業者フォームで、有効化アカウントを設定する作業者の一覧を選択します。
2. フィールドを更新するには、**コマース** &gt; **外部 ID を作成** の順にクリックします。 作業者に関連付けられているすべての AAD アカウントはこのウィンドウに表示されます。

    > [!NOTE]
    > これらのアカウントは、外部 ID フロー オプションを使用してマップするまで、デバイスのアクティベーション アカウントではありません。

3. 既存の AAD アカウントを有効化アカウントとして使用する場合は、バルクでマップできません。 これらの作業者の選択をキャンセルし、**既存の外部 ID の使用** を使用して個別にマップします。
4. 新しい AAD アカウントを作成し、作業者に関連付けてアクティベーション アカウントとして使用できるようにするには、**エイリアス** と **パスワード** フィールドを更新し、**OK** をクリックします。 メイン作業者フォームでは、アクティベーション アカウントが作業者ごとに作成されるとメッセージを受け取ります。

## <a name="run-the-validate-devices-for-activation-check-at-headquarters"></a>本社で有効化チェックのためにデバイス検証を実行

有効化アカウントを作業者に手渡す前に、IT プロフェッショナルは作業者に割り当てられたデバイスのためにデバイスを検証チェックを実行する必要があります。 これは、事前にデバイス動作の潜在的な障害を特定し、それを作業者に通知する前に修正するのに役立ちます。

1. **デバイス** ページを HQ (**小売りとコマース** &gt; **チャンネル設定** &gt; **POS 設定** &gt; **デバイス**)で開きます。
2. デバイスの有効化を検証するデバイスを選択し、**デバイスで有効化を検証する** をクリックします。 たとえば、デバイスの **HOUSTON-2** を選択します。
3. 表示されるダイアログ ボックスで、デバイスを検証する作業者 (前の手順で AAD アカウントにマップされた作業者) を選択します。 たとえば、作業者の **000160** を選択します。
4. **OK** をクリックし、次のようなメッセージが表示されることを確認します。「デバイス HOUSTON-2 とスタッフ 000160 の有効化前の検証が完了しました。 検証: 成功

## <a name="checklist-to-follow-before-activation"></a>起動前のチェックリスト

1. HQ で **有効化のためにデバイスを検証** チェックを完了し、デバイスが検証をパスしたことを確認します。
2. デバイスを有効化しているクライアント マシンで、Commerce Scale Unit URL 正常性チェックにアクセスし、正常性チェックが承認されていることを確認します。 次の形式を使用します: `https://clxtestax404ret.cloud.test.dynamics.com/en/healthcheck?testname=ping`
3. 作業者は、AAD アカウント (**外部 ID** 下) にマップする必要があります。
4. マッピングする AAD アカウントは、同じテナントに属している必要があります。
5. 作業者を AAD アカウントにマップするには、Microsoft Dynamics Lifecycle Services (LCS) の管理者アカウントを使用して HQ に サインインします。
6. 作業者がマネージャー ロール内のコマース ユーザーとして設定されていることを確認します (検証でチェックされます)。
7. チャネル データがチャネル データベースに存在することを確認します。
8. **登録** &gt; **登録** (検証によって確認) でハードウェア プロファイルを設定します。
9. レジスターおよび店舗に画面レイアウトがあることを確認します (検証でチェックされます)。
10. 基本住所が法人に対して設定されていることを確認します。
11. 電子決済 (EFT) のコンフィギュレーションの値があることを確認します。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
