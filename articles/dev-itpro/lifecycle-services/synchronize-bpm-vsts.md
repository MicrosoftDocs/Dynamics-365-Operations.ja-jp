---
title: BPM ライブラリと Azure DevOps の同期
description: このトピックでは、LCS の BPM ライブラリを Azure DevOps と同期させる方法について説明します。
author: amarshall
manager: AnnBe
ms.date: 05/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012, Operations
ms.custom: 13301
ms.assetid: ''
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 911a8983baa8df0fd3e21c86abb527e93b9c4978
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595457"
---
# <a name="synchronize-bpm-libraries-with-azure-devops"></a>BPM ライブラリと Azure DevOps の同期

[!include [banner](../includes/banner.md)]

プロジェクトの実装のステージを開始するには、Microsoft Azure DevOps で、ビジネス プロセス モデラー (BPM) とお客様のプロジェクトを同期します。 この方法で、プロセスを確認し、要件を業務プロセスと関連付けることができます。 BPM ライブラリを Azure DevOps プロジェクトと同期させることにより、Azure DevOps での実装プロジェクトの進捗状況を追跡したり、さまざまな作業項目を要件や業務プロセスに関連付けることができます。 これらの作業項目には、バグ、タスク、バックログ項目、テスト、ドキュメントが含まれます。

現在、BPM Azure DevOps 同期では、カスタム作業項目または業務プロセスとの同期をサポートしていません。 これらのいずれかを試みると、警告が表示されます。 警告を無視して、カスタム テンプレートとの Azure DevOps 同期を試みる場合は、テンプレートの次の内容を確認することで同期の問題を回避できます。
- 作業品目タイプの状態を削除しないでください。
- 作業品目タイプの状態を削除しないでください。
- 必須フィールドを作業項目の種類に追加しない

Azure DevOps の詳細については、[www.visualstudio.com/team-services](https://www.visualstudio.com/team-services) をご覧ください。

## <a name="lcs-project-settings-set-up-azure-devops"></a>LCS プロジェクト設定: Azure DevOps の設定

既に Microsoft Dynamics Lifecycle Services (LCS) から Azure DevOps を設定している場合、このセクションの手順を省略できます。

### <a name="create-a-personal-access-token"></a>個人用アクセス トークンを作成する

Azure DevOps プロジェクトに接続するために、LCS は個人用アクセス トークンを使用して認証されます。 Azure DevOps で個人用アクセス トークンを作成するには、これらの手順に従います。

1. <https://www.visualstudio.com> に移動し、サインイン、および Azure DevOps プロジェクトを検索します。
2. 右上隅で、自分の名前にポインターを置き、表示されるメニューで**セキュリティ**を選択します。
3. **追加** を選択し、新しい個人用アクセス トークンを作成します。
4. トークン名を入力し、トークンの持続時間を指定します。
5. **トークンの作成** を選択します。
6. トークンをクリップボードにコピーします。

    > [!NOTE]
    > このステップを完了してこのページから移動すると、トークンの詳細を再度検索することはできません。 したがって、ページから移動する前にトークンをコピーしたことを確認してください。

### <a name="configure-your-lcs-project-to-connect-to-azure-devops"></a>LCS プロジェクトをコンフィギュレーションして Azure DevOps に接続する

1. LCS プロジェクトで、**プロジェクト設定**タイルを選択します。
2. **Azure DevOps** を選択し、**Azure DevOps の設定** を選択します。 この構成は多くの LCS ツールで必要です。 既に LCS を構成して Azure DevOps プロジェクトに接続している場合、この手順を省略するか、**変更**を選択して既存のコンフィギュレーションを変更できます。
3. Azure DevOps アカウントのルート URL および以前に作成した個人用アクセス トークンを入力し、**続行**を選択します。
4. Azure DevOps プロジェクトを選択します。
5. LCS/BPM 項目と関連付けられている Azure DevOps 作業項目の種類の間のマッピングを指定します。

    ![作業項目タイプ マッピング](./media/newbpm_BlogPost24.png)

6. **続行** を選択して変更内容を確認し、**保存** を選択します。

## <a name="synchronize-a-bpm-library-with-a-azure-devops-project"></a>Azure DevOps プロジェクトと BPM ライブラリの同期

LCS プロジェクトおよび Azure DevOps プロジェクト間の接続を設定した後は、Azure DevOps プロジェクトに BPM ライブラリを同期することができます。 BPM ライブラリを Azure DevOps プロジェクトと同期させると、BPM ライブラリ内の各業務プロセスの明細行に対して Azure DevOps 作業項目が作成されます。 さらに、BPM の業務プロセスの階層は、Azure DevOps の作業項目の階層に反映されます。 Azure DevOps で作成される作業項目のタイプは、LCS プロジェクトの設定によって異なります。

この同期は一方向の同期です。 LCS の変更は Azure DevOps に反映されますが、Azure DevOps の変更は LCS に反映されません。

次の情報が同期されます。

- 業務プロセスの名前
- 業務プロセスの説明
- キーワード (タグとして)
- 国または地域 (タグとして)
- 業界 (タグとして)

BPM ライブラリを Azure DevOps プロジェクトと同期させるには、**業務プロセス ライブラリ**ページで、同期するライブラリのタイルの省略記号ボタン (...) を選択し、**Azure DevOps 同期**を選択します。

![ライブラリのタイルから Azure DevOps 同期を開始](./media/newbpm_BlogPost25.png)

また、BPM ライブラリ内のツールバーから Azure DevOps 同期を開始することができます。 省略記号ボタン (...) を選択し、**Azure DevOps の同期** を選択します。

![ライブラリのツール バーから Azure DevOps 同期を開始](./media/newbpm_BlogPost26.png)

> [!NOTE]
> BPM ローカライズはサポートされません。 EN-US 以外の言語で新しい BPM クライアントを編集すると、変更が加えられた言語で BPM を表示したときのみ変更が表示されます。 EN-US で行われた変更を表示するには、変更が表示される前に、Visual Studio Team Server と同期する必要があります。

## <a name="turn-off-synchronization-of-bpm-with-azure-devops"></a>BPM と Azure DevOps の同期の停止

同期をオフにするには、**業務プロセス ライブラリ** ページで同期を停止するライブラリを選択し、省略記号ボタン (...) を選択してから **Azure DevOps 同期** を選択解除します。

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

Azure DevOps に接続されている業務プロセスを確認するとき、Azure DevOps プロジェクトに要求を直接追加することができます。

1. ビジネス プロセスを選択します。
2. 右ウィンドウの**要件**タブで、**要件を追加**を選択します。
3. 名前、説明、およびタイプを入力し、次に**作成**を選択します。

    Azure DevOps では、現在の業務プロセスに関連付けられている要求作業項目が作成されます。

現在の業務プロセスに関連付けられている Azure DevOps 作業項目に移動するには、**要件** タブで適切なリンクを選択します。

## <a name="common-syncing-errors"></a>一般的な同期エラー

BPM から Azure DevOps への同期が失敗した場合、失敗したプロセス名、作業項目の種類、およびエラー メッセージが表示されます。 

![BPM 同期エラー](./media/BPMsyncError.jpg)

ここでいくつか一般的な原因と、エラーを解決するために推奨するアクションを示します。

| **考えられる原因** | **エラー メッセージ** | **推奨される解決策** | 
|---------|--------|--------|
| 必須フィールドが追加されました | 作業項目の作成に失敗しました。 必須フィールドがこの作業項目の種類に追加されましたが、サポートされていません。 この要件を削除するか、プロセス テンプレートで既定値を提供して、操作をブロック解除します。 | 必須フィールドを削除するか、既定値を提供します。 | 
| 作業項目の種類が無効です | 作業項目の作成に失敗しました。 作業項目の種類がプロセス テンプレートで無効になっています。 作業項目の種類を有効にして、操作をブロック解除します。 | 作業項目の種類をプロセス テンプレートで有効にします。 |  
| 更新する作業項目が見つかりませんでした | 作業項目の更新に失敗しました。 作業項目が存在しないか、読み取るためのアクセス許可がありません。 プロジェクト設定で PAT コンフィギュレーションを確認するか、作業項目が DevOps プロジェクトから直接削除されている場合は作業項目を復元します。 | 削除された場合はごみ箱から作業項目を復元するか、新しい個人用アクセス トークン (PAT) を作成して完全なアクセス許可があることを確認します。 |  
| 個人用アクセス トークンの期限が切れています | Visual Studio Team Services との同期に失敗しました。 要求応答は次のとおりです: 無許可。 PAT が正しく設定されていてまだ有効なことを確認し、エラーが引き続き発生する場合は再試行してサポートに連絡してください。 | Azure DevOps から新しい個人用アクセス トークン (PAT) を作成し、LCS プロジェクト設定で PAT 値を更新します。 | 
| 一般的なエラー | Visual Studio Team Services との同期に失敗しました。 要求応答は次のとおりです: {0}。 PAT が正しく設定されていてまだ有効なことを確認し、エラーが引き続き発生する場合は再試行してサポートに連絡してください。 | 同期エラーの原因となった要求応答で、顧客サポートに問い合わせてください。 | 
