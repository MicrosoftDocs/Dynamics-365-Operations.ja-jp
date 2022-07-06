---
title: Azure Resource Manager (ARM) のオンボード プロセスの実施
description: この記事では、コネクタの Azure Resource Manager オンボード プロセスを実施する方法について説明します。
author: saurabhsurana
ms.date: 03/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.custom: 141093
ms.assetid: dcd23629-246d-4fbc-adf5-7245bb2121e4
ms.search.region: Global
ms.author: sasurana
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: 95b3b862109cc5cf7ff3adb96a4dda47830a841e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867480"
---
# <a name="complete-the-azure-resource-manager-onboarding-process"></a>Azure Resource Manager (ARM) のオンボード プロセスの実施

[!include [banner](../includes/banner.md)]

この記事では、コネクタの Microsoft Azure Resource Manager オンボード プロセスを実施する方法について説明します。 

Azure Resource Manager トポロジを配置するには、コネクタのオンボード プロセスを実施する必要があります。 オンボード プロセスを開始するには、次の項目が必要です。

-   展開する Azure サブスクリプション ID
-   Azure サブスクリプションの所有権、またはサブスクリプション所有者へのアクセス。共同作成者ワークフロー、およびアップロード管理証明書を追加できるようにします。
-   テナント管理者が管理者同意ワークフローを実行する

## <a name="azure-resource-manager-onboarding-process"></a>Azure Resource Manager オンボード プロセス
Azure Resource Manager オンボードは、各ステップに独自のサブ手順がある、2 ステップ手順とみなすことができます。 Microsoft Dynamics Lifecycle Services (LCS) プロジェクトに追加するすべてのサブスクリプションに対してこれらすべてのを完了する必要があります。

1.  Azure サブスクリプションで作業を行う LCS 配置サービスを承認します。
    1.  ワークフローを認証します。
    2.  投稿者ワークフローを設定します。

2.  Azure Resource Manager リソースをデプロイする Azure サブスクリプションを有効にします。
    1.  Azure コネクタを有効にし、LCS ユーザーを追加にします。
    2.  オプション: 管理証明書をアップロードします。
    3.  配置設定をコンフィギュレーションします。

### <a name="authorize-the-lcs-deployment-service-to-work-on-the-azure-subscription"></a>Azure サブスクリプションで作業を行う LCS 配置サービスを承認する

Azure サブスクリプションで動作するよう LCS 配置サービスを承認するには、次の手順を実行します。

#### <a name="authorize-the-workflow"></a>ワークフローを認証する

テナントの管理者は、次の手順を完了する必要があります。

1.  LCS で、**プロジェクト** ページの **環境** セクションにある、**Microsoft Azure 設定** を選択します。
2.  **プロジェクト設定** ページでは、**Azure コネクタ** タブの、**組織リスト** グループで、**承認** を選択して Azure Resource Manager 共同作成者ワークフローを開始します。 このワークフローでは、配置サービスのアクセス許可が設定されるため、配置サービスを自分の代わりにサブスクリプションに展開できます。
3.  **管理者の同意の付与** ページで、**承認** を選択します。 次に、接続する Azure サブスクリプションの管理者アカウントを使用してサインインし、**承諾** を選択します。 これで、承認が完了として表示されます。

#### <a name="set-the-contributor-workflow"></a>投稿者ワークフローを設定

**寄稿者** ロールを **Dynamics 配置サービス \[wsfed 有効 \]** アプリケーションに割り当てるため、これらの手順に従います。

1.  [Azure ポータル](https://portal.azure.com)の **サブスクリプション** タブで、Azure サブスクリプションを選択してから、**アクセス制御 (IAM)** 行項目を選択します。
2.  **追加** を選択し、**ロール割り当ての追加** を選択します。 ダイアログ ボックスで、**ロール** を **貢献者** に、**アクセス権の割り当て先** を **Azure AD ユーザー、グループ、サービス プリンシパル** に設定します。 **選択** フィールドで **Dynamics 配置サービス \[wsfed 有効\]** を検索して選択します。 **保存** を選択します。 

    > [!NOTE]
    > 一部の Azure サブスクリプションには **アクセス制御 (IAM)** セクションではなく **ユーザー** セクションがあります。 この場合、**ユーザーの追加** ダイアログ ボックスの **選択** フィールドに、**Dynamics 配置サービス \[wsfed 有効\]** と入力して **選択** を選択します。
    
[![Dynamics 配置サービス \[wsfed 有効\.\]](./media/arm_redo_02.png)](./media/arm_redo_02.png)

3.  **ロールの割り当て** タブで、アプリは **貢献者** として割り当てられます。 

    > [!NOTE]
    > Dynamics 配置サービス \[wsfed 有効\] が表示されない場合、承認プロセスは完了していないか、別の Azure サブスクリプションで完了しています。 

### <a name="enable-the-azure-subscription-to-deploy-azure-resource-manager-resources"></a>Azure Resource Manager リソースをデプロイする Azure サブスクリプションを有効にする

Azure サブスクリプションを有効にして Azure Resource Manager リソースをデプロイできるようにするには、次の手順を実行します。

#### <a name="enable-the-azure-connector-and-add-an-lcs-user"></a>Azure コネクタを有効、および LCS ユーザーを追加

Azure コネクタを有効にし、必要に応じて LCS ユーザーを追加するには、これらの手順に従います。

1.  LCS で、**プロジェクト** ページの **環境** セクションにある、**Microsoft Azure 設定** を選択します。
2.  **プロジェクト設定** ページでは、**Azure コネクタ** タブの、**Azure コネクタ** の下で **追加** を選択します。 

    > [!NOTE]
    > 既存のコネクタで Azure Resource Manager を有効にしている場合は、**編集** を選択します。

3.  コネクタ名および配置する Azure サブスクリプション ID を入力し、**Azure Resource Manager を使用するコンフィギュレーション** オプションを **はい** に設定します。
4.  **Azure サブスクリプション AAD テナント ドメイン** フィールドで、Azure サブスクリプション アカウント管理者のドメイン名を入力し、**次へ** を選択します。
5.  Azure サブスクリプションに LCS ユーザーを追加するか管理証明書を使用して、サブスクリプションへのアクセスを認証します。 

    > [!重要] LCS ユーザーを追加する場合は、手順 6 に進みます。 管理証明書をアップロードする必要がある場合は、この手順のステップ 6 から 8 を実行しないようにします。 代わりに、[管理証明書のアップロード](#upload-the-management-certificate)という次の手順を完了します。 

6.  [Azure ポータル](https://portal.azure.com)の **サブスクリプション** タブで、Azure サブスクリプションを選択してから、**アクセス制御 (IAM)** 行項目を選択します。
7.  **アクセス制御 (IAM)** ダイアログ ボックスで、**追加** を選択し、**寄稿者** を選択してから、**OK** を選択します。
8.  **ユーザーの追加** ダイアログ ボックスの **選択** フィールドで、LCS ユーザーを入力してから Enter キーを押します。 

    > [!NOTE]
    > ユーザーを明確に入力する必要があります。 ユーザーがメンバーであるグループを追加することはできません。 **ユーザー** ページが開いたとき、ユーザーが **寄稿者** として割り当てられていることを確認できます。

#### <a name="upload-the-management-certificate"></a>管理証明書のアップロード

前の手順「Azure コネクタを有効にし LCS ユーザーを追加する」の手順 6 から 8 を完了していない場合にのみ、この手順を実行します。 

1.  LCS では、**Microsoft Azure 設定** ページで、**ダウンロード** を選択します。 証明書ファイルをダウンロードした場所をメモしておきます。 この情報を使用して、証明書を Azure サブスクリプションにアップロードします。
2.  [Azure クラシック ポータル](https://ms.portal.azure.com)の左ウィンドウで、**設定** を選択します。
3.  使用する Azure サブスクリプションへフィルター処理をし、次に、**管理証明書** タブで、**アップロード** を選択します。
4.  手順 1 でダウンロードした管理証明書を選択してから、**OK** を選択します。

#### <a name="configure-deployment-settings"></a>配置設定のコンフィギュレーション

1.  LCS で、**プロジェクト** ページの **環境** セクションにある、**Microsoft Azure 設定** を選択します。
2.  **Microsoft Azure 設定** ページで、デプロイする地域を選択し、**接続** を選択します。 これで Azure Resource Manager オンボード フローは完了です。 **Azure コネクタ** リストにサブスクリプションが追加されたのが確認できるはずです。 また、チェック マークは **ARM 有効** で表示されます。

## <a name="expired-connectors"></a>期限切れコネクタ

管理証明書を使用して作成された Azure コネクタには有効期限があります。 有効期限が過ぎると、証明書は無効になります。 したがって、Azure コネクタを使用したり、LCS からそのコネクタを介して展開された任意のリソースを管理したりすることはできません。 コネクタを更新して有効期限をリセットするには、[Azure コネクタを有効にし LCS ユーザーを追加する](./arm-onboarding.md#enable-the-azure-connector-and-add-an-lcs-user)の手順に従い、コネクタを編集することをお勧めします。  これにより、新しいダウンロード用の証明書が生成され、有効期限がリセットされます。

有効期限は、管理証明書を使用するコネクタに対してのみ表示されます。 LCS ユーザーを介してコネクタを作成した場合は、この記事で前述したように、有効期限は表示されません。 代わりに、LCS ユーザーがサブスクリプションにアクセスできる限り、Azure コネクタは有効です。

## <a name="known-limitations"></a>既知の制限

LCS で Azure コネクタを設定または管理する際には、いくつかの既知の制限があります:

- 見込顧客の組織は、財務と運用アプリのライセンスを購入していないため、ソフトウェアを展開できず、これらの組織は Azure コネクタを設定することができません。 組織タイプを確認するには、LCS へのサインイン中にページの右上隅で自分の名前を選択します。
- Azure コネクタは、LCS プロジェクト ID、Azure サブスクリプション ID、および Azure リージョンの一意の組み合わせに対してのみ作成できます。 同じサブスクリプションおよびリージョンに対して複数のコネクタを作成することはできません。 サブスクリプションとリージョンの特定の組み合わせに対して Azure コネクタを削除する必要がある場合は、まずそのコネクタにより作成されたすべての環境を削除する必要があります。
- 管理証明書は、リージョンに関係なく、同じ Azure サブスクリプション ID に対して同じプロジェクトで再利用することはできません。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
