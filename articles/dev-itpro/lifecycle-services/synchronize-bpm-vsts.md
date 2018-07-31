---
title: "BPM ライブラリと Visual Studio Team Services の同期"
description: "このトピックでは、LCS の BPM ライブラリを Visual Studio Team Services (VSTS) と同期させる方法について説明します。"
author: kfend
manager: AnnBe
ms.date: 11/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012, Operations
ms.custom: 13301
ms.assetid: 
ms.search.region: Global
ms.author: ntecklu
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: d3fc1e8ea856b6c7c6daffd8f46f2e5e4fb12710
ms.openlocfilehash: 4383825c37d7aed6de60e8da392a1d5b0c5c713a
ms.contentlocale: ja-jp
ms.lasthandoff: 06/04/2018

---

# <a name="synchronize-a-bpm-library-with-visual-studio-team-services"></a>BPM ライブラリと Visual Studio Team Services の同期

[!include [banner](../includes/banner.md)]

プロジェクトの実装のステージを開始するには、Microsoft Visual Studio Team Services (VSTS) で、ビジネス プロセス モデラー (BPM) とお客様のプロジェクトを同期します。 この方法で、プロセスを確認し、要件を業務プロセスと関連付けることができます。 BPM ライブラリを VSTS プロジェクトと同期させることにより、VSTS での実装プロジェクトの進捗状況を追跡したり、さまざまな作業項目を要件や業務プロセスに関連付けることができます。 これらの作業項目には、バグ、タスク、バックログ項目、テスト、ドキュメントが含まれます。

現在、BPM VSTS 同期では、カスタム作業項目または業務プロセスとの同期をサポートしていません。 これらのいずれかを試みると、警告が表示されます。 警告を無視して、カスタム テンプレートとの VSTS 同期を試みる場合は、テンプレートの次の内容を確認することで同期の問題を回避できます。
- 作業品目タイプの状態を削除しないでください。
- 作業品目タイプの状態を削除しないでください。
- 必須フィールドを作業項目の種類に追加しない

VSTS の詳細については、[[www.visualstudio.com/team-services](http://www.visualstudio.com/team-services)] をご覧ください。

## <a name="lcs-project-settings-set-up-vsts"></a>LCS プロジェクト設定: VSTS の設定

既に Microsoft Dynamics Lifecycle Services (LCS) から VSTS を設定している場合、このセクションの手順を省略できます。

### <a name="create-a-personal-access-token"></a>個人用アクセス トークンを作成する

VSTS プロジェクトに接続するために、LCS は個人用アクセス トークンを使用して認証されます。 VSTS で個人用アクセス トークンを作成するには、これらの手順に従います。

1. <https://www.visualstudio.com> に移動し、サインイン、および VSTS プロジェクトを検索します。
2. 右上隅で、自分の名前にポインターを置き、表示されるメニューで**セキュリティ**を選択します。
3. **追加** を選択し、新しい個人用アクセス トークンを作成します。
4. トークン名を入力し、トークンの持続時間を指定します。
5. **トークンの作成** を選択します。
6. トークンをクリップボードにコピーします。

    > [!NOTE]
    > このステップを完了してこのページから移動すると、トークンの詳細を再度検索することはできません。 したがって、ページから移動する前にトークンをコピーしたことを確認してください。

### <a name="configure-your-lcs-project-to-connect-to-vsts"></a>LCS プロジェクト コンフィギュレーションして VSTS に接続する

1. LCS プロジェクトで、**プロジェクト設定**タイルを選択します。
2. **Visual Studio Team Services** を選択し、**Visual Studio Team Services の設定** を選択します。 この構成は多くの LCS ツールで必要です。 既に LCS を構成して VSTS プロジェクトに接続している場合、この手順を省略するか、**変更**を選択して既存のコンフィギュレーションを変更できます。
3. VSTS アカウントのルート URL および以前に作成した個人用アクセス トークンを入力し、**続行**を選択します。
4. VSTS プロジェクトを選択します。
5. LCS/BPM 項目と関連付けられている VSTS 作業項目の種類の間のマッピングを指定します。

    ![作業項目タイプ マッピング](./media/newbpm_BlogPost24.png)

6. **続行** を選択して変更内容を確認し、**保存** を選択します。

## <a name="synchronize-a-bpm-library-with-a-vsts-project"></a>VSTS プロジェクトと BPM ライブラリを同期

LCS プロジェクトおよび VSTS プロジェクト間の接続を設定した後は、VSTS プロジェクトにBPM ライブラリを同期することができます。 BPM ライブラリを VSTS プロジェクトと同期させると、BPM ライブラリ内の各業務プロセスの明細行に対して VSTS 作業項目が作成されます。 さらに、BPM の業務プロセスの階層は、VSTS の作業項目の階層に反映されます。 VSTS で作成される作業項目のタイプは、LCS プロジェクトの設定によって異なります。

この同期は一方向の同期です。 LCS の変更は VSTS に反映されますが、VSTS の変更は LCS に反映されません。

次の情報が同期されます。

- 業務プロセスの名前
- 業務プロセスの説明
- キーワード (タグとして)
- 国または地域 (タグとして)
- 業界 (タグとして)

BPM ライブラリを VSTS プロジェクトと同期させるには、**業務プロセス ライブラリ**ページで、同期するライブラリのタイルの省略記号ボタン (...) を選択し、**VSTS同期**を選択します。

![ライブラリのタイルから VSTS 同期を開始](./media/newbpm_BlogPost25.png)

また、BPM ライブラリ内のツールバーから VSTS 同期を開始することができます。 省略記号ボタン (...) を選択し、**VSTS の同期** を選択します。

![ライブラリのツール バーから VSTS 同期を開始](./media/newbpm_BlogPost26.png)

>[!NOTE]
> BPM ローカライズはサポートされません。 EN-US 以外の言語で新しい BPM クライアントを編集すると、変更が加えられた言語で BPM を表示したときのみ変更が表示されます。 EN-US で行われた変更を表示するには、変更が表示される前に、Visual Studio Team Server と同期する必要があります。

## <a name="turn-off-synchronization-of-bpm-with-vsts"></a>VSTS と BPM の同期をオフにする

同期をオフにするには、**業務プロセス ライブラリ** ページで同期を停止するライブラリを選択し、省略記号ボタン (...) を選択してから **VSTS 同期** を選択解除します。

## <a name="review-processes-and-add-requirements"></a>プロセスを確認し、要件を追加

要件を収集しているプロジェクトのフェーズ中に、BPM ライブラリを使用して、ビジネス プロセスおよびタスクをレビューし、要件を特定することができます。 BPM で、業務プロセスを確認済みとマークして、確認プロセスを追跡することができます。

プロセスまたはその子プロセスの 1 つをレビューとしてマークするには、BPMでプロセスを選択し、右ウィンドウの **概要** タブで **レビューとしてマーク** を選択します。

業務プロセスを確認済みとしてマークすると、**確認済** 列が更新されます。 この列には、次の情報が表示されます。

- 分数では、直接の子プロセスの確認された数を示します。
- 記号は、プロセスとその子プロセスがどれだけ完全にレビューされたかを示します。

   - **緑のチェック マーク** – プロセスとそのすべての子プロセスは完全に確認済です。
   - **黄色の円** – プロセスおよびその子プロセスは部分的に確認されています。
   - **赤いダッシュ** – プロセスとその子プロセスは確認されていません。

![レビュー列の例](./media/newbpm_BlogPost28.png)

BPM ライブラリが VSTS プロジェクトと同期され、プロセスを BPM でレビュー済みとマークすると、そのステータスは VSTS の **Active** に変更されます。

VSTS に接続されている業務プロセスを確認するとき、VSTS プロジェクトに要求を直接追加することができます。

1. ビジネス プロセスを選択します。
2. 右ウィンドウの**要件**タブで、**要件を追加**を選択します。
3. 名前、説明、およびタイプを入力し、次に**作成**を選択します。

    ![要件を作成しています](./media/newbpm_BlogPost29.png)

    VSTS では、現在の業務プロセスに関連付けられている要求作業項目が作成されます。

現在の業務プロセスに関連付けられている VSTS 作業項目に移動するには、**要件** タブで適切なリンクを選択します。

