---
title: Azure Resource Manager (ARM) の研修プロセスを完了します。
description: このトピックでは、コネクタの Azure Resource Manager (ARM) 登録プロセスを完了する方法について説明します。
author: sarvanisathish
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.custom: 141093
ms.assetid: dcd23629-246d-4fbc-adf5-7245bb2121e4
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: af1114de08b0ea93bb1df70a27132efa3c5ccce2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681630"
---
# <a name="complete-the-azure-resource-manager-arm-onboarding-process"></a>Azure Resource Manager (ARM) の研修プロセスを完了します。

[!include [banner](../includes/banner.md)]

このトピックでは、コネクタの Azure Resource Manager (ARM) 登録プロセスを完了する方法について説明します。 

Microsoft Azure Resource Manager (ARM) トポロジを配置するには、コネクタに対して ARN 研修プロセスを完了する必要があります。 オンボード プロセスを開始するには、次の項目が必要です。

-   展開する Azure サブスクリプション ID
-   Azure サブスクリプションの所有権、またはサブスクリプション所有者へのアクセス。共同作成者ワークフロー、およびアップロード管理証明書を追加できるようにします。
-   テナント管理者が管理者同意ワークフローを実行する

## <a name="arm-onboarding-process"></a>ARM 研修プロセス
ARM オンボードは、各ステップに独自のサブ手順がある、2 ステップ手順とみなすことできます。 Microsoft Dynamics Lifecycle Services (LCS) プロジェクトに追加するすべてのサブスクリプションに対してこれらすべてのを完了する必要があります。

1.  Azure サブスクリプションで作業を行う LCS 配置サービス (DSU) を承認します。
    1.  ワークフローを認証します。
    2.  投稿者ワークフローを設定します。

2.  ARM リソースを配置する Azure サブスクリプションを有効にします。
    1.  Azure コネクタを有効にし、LCS ユーザーを追加にします。
    2.  オプション: 管理証明書をアップロードします。
    3.  配置設定をコンフィギュレーションします。

### <a name="authorize-the-lcs-dsu-to-work-on-the-azure-subscription"></a>Azure サブスクリプションで作業を行う LCS DSU を承認する

Azure サブスクリプションで動作するよう LCS DSU を承認するには、次の手順を実行します。

#### <a name="authorize-the-workflow"></a>ワークフローを認証する

テナントの管理者は、次の手順を完了する必要があります。

1.  LCS で、**プロジェクト** ページの **環境** セクションにある **Microsoft Azure 設定** をクリックします。
2.  **プロジェクト設定** ページでは、**Azure コネクタ** タブの、**組織リスト** グループで、**承認** をクリックして ARM 貢献者ワークフローを開始します。 このワークフローでは、DSU のアクセス許可が設定されるため、DSU を自分の代わりにサブスクリプションに展開できます。
3.  **管理者の同意の付与** ページで、**承認** をクリックします。 次に、接続する Azure サブスクリプションの管理者アカウントを使用してサインインし、**承諾** をクリックします。 これで、承認が完了として表示されます。

#### <a name="set-the-contributor-workflow"></a>投稿者ワークフローを設定

**寄稿者** ロールを **Dynamics 配置サービス \[wsfed 有効 \]** アプリケーションに割り当てるため、これらの手順に従います。

1.  [Azure ポータル](https://portal.azure.com)の **サブスクリプション** タブで、Azure サブスクリプションを選択してから **アクセス制御 (IAM)** 行項目をクリックします。
2.  **Add** をクリックして **ロール割り当ての追加** を選択します。 ダイアログ ボックスで、**ロール** を **貢献者** に、**アクセス権の割り当て先** を **Azure AD ユーザー、グループ、サービス プリンシパル** に設定します。 **選択** フィールドで **Dynamics 配置サービス \[wsfed 有効\]** を検索して選択します。 **保存** を選択します。 
    > [!NOTE]
    > 一部の Azure サブスクリプションには **アクセス制御 (IAM)** セクションではなく **ユーザー** セクションがあります。 この場合、**ユーザーの追加** ダイアログ ボックスの **選択** フィールドに、**Dynamics 配置サービス \[wsfed 有効\]** と入力して **選択** を選択します。
    
[![Dynamics 配置サービス \[wsfed 有効\]](./media/arm_redo_02.png)](./media/arm_redo_02.png)

3.  **ロールの割り当て** タブで、アプリは **貢献者** として割り当てられます。 
    > [!NOTE]
    > Dynamics 配置サービス \[wsfed 有効\] が表示されない場合、承認プロセスは完了していないか、別の Azure サブスクリプションで完了しています。 

### <a name="enable-the-azure-subscription-to-deploy-arm-resources"></a>ARM リソースを配置する Azure サブスクリプションの有効化

Azure サブスクリプションを有効にして ARM リソースを展開できるようにするには、次の手順を実行します。

#### <a name="enable-the-azure-connector-and-add-an-lcs-user"></a>Azure コネクタを有効、および LCS ユーザーを追加

Azure コネクタを有効にし、必要に応じて LCS ユーザーを追加するには、これらの手順に従います。

1.  LCS で、**プロジェクト** ページの **環境** セクションにある **Microsoft Azure 設定** をクリックします。
2.  **プロジェクト設定** ページでは、**Azure コネクタ** タブで、**Azure コネクタ** の **追加** をクリックします。 
    > [!NOTE]
    > 既存のコネクタで ARM を有効にしている場合は、**編集** をクリックします。
3.  コネクタ名および配置する Azure サブスクリプション ID を入力し、**Azure Resource Manager を使用するコンフィギュレーション** オプションを **はい** に設定します。
4.  **Azure サブスクリプション AAD テナント ドメイン** フィールドで、Azure サブスクリプション アカウント管理者のドメイン名を入力してから **次へ** をクリックします。
5.  Azure サブスクリプションに LCS ユーザーを追加するか管理証明書を使用して、サブスクリプションへのアクセスを認証します。 **重要:** LCS ユーザーを追加する場合は、手順 6 に進みます。 管理証明書をアップロードする必要がある場合は、この手順のステップ 6 から 8 を実行しないようにします。 代わりに、「管理証明書のアップロード」という次の手順を完了します。
6.  [Azure ポータル](https://portal.azure.com)の **サブスクリプション** タブで、Azure サブスクリプションを選択してから **アクセス制御 (IAM)** 行項目をクリックします。
7.  **アクセス制御 (IAM)** ダイアログ ボックスで、**追加** をクリックし、**寄稿者** を選択してから、**OK** をクリックします。
8.  **ユーザーの追加** ダイアログ ボックスの **選択** フィールドで、LCS ユーザーを入力してから Enter キーを押します。 
    > [!NOTE]
    > ユーザーを明確に入力する必要があります。 ユーザーがメンバーであるグループを追加することはできません。 **ユーザー** ページが開いたとき、ユーザーが **寄稿者** として割り当てられていることを確認できます。

#### <a name="upload-the-management-certificate"></a>管理証明書のアップロード

前の手順「Azure コネクタを有効にし LCS ユーザーを追加する」の手順 6 から 8 を完了していない場合にのみ、この手順を実行します。

1.  LCS で、**Microsoft Azure 設定** ページの **ダウンロード** をクリックします。 証明書ファイルをダウンロードした場所をメモしておきます。 この情報を使用して、証明書を Azure サブスクリプションにアップロードします。
2.  [Azure クラシック ポータル](https://manage.windowsazure.com/)の左ウィンドウで **設定** をクリックします。
3.  使用する Azure サブスクリプションへフィルター処理をし、次に、**管理証明書** タブで、**アップロード** をクリックします。
4.  手順 1 でダウンロードした管理証明書を選択し、**OK** をクリックします。

#### <a name="configure-deployment-settings"></a>配置設定のコンフィギュレーション

1.  LCS で、**プロジェクト** ページの **環境** セクションにある **Microsoft Azure 設定** をクリックします。
2.  **Microsoft Azure 設定** ページで、配置する地域を選択してから、**接続** をクリックします。 ARM オンボーディング フローが完了しました。 **Azure コネクタ** リストにサブスクリプションが追加されたのが確認できるはずです。 また、チェック マークは **ARM 有効** で表示されます。




