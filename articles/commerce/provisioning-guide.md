---
title: Dynamics 365 Commerce 評価環境のプロビジョニング
description: このトピックでは、Microsoft Dynamics 365 Commerce の評価環境をプロビジョニングする方法について説明します。
author: psimolin
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c8241c31e82d124398189666c3a1709d25884b8acd9c8f3b1068529cbd216684
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777503"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a>Dynamics 365 Commerce 評価環境のプロビジョニング

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce の評価環境をプロビジョニングする方法について説明します。

開始する前に、このトピックにざっと目を通して、プロセスに必要な内容を把握することをお勧めします。

> [!NOTE]
> コマースの評価環境は一般的には提供されておらず、パートナーや顧客からのリクエストに応じて付与されます。 ライセンスの詳細については、Microsoft パートナーにお問い合わせください。

Commerce 評価環境を正常にプロビジョニングするには、特定の製品名とタイプを持つプロジェクトを作成する必要があります。 この環境と Commerce Scale Unit (CSU) には、後から E コマースをプロビジョニングする場合に使用する必要がある特定のパラメーターもいくつかあります。 このトピックの手順では、プロビジョニングを完了するために必要なすべての手順と、使用する必要があるパラメーターについて説明します。

Commerce 評価環境のプロビジョニングが正常に完了した後、いくつかのプロビジョニング後の手順を完了して、使用のために準備する必要があります。 一部の手順は、システムのどの側面を評価するかに応じて使用するオプションです。 オプションの手順は、後からいつでも完了できます。

プロビジョニング後に Commerce 評価環境を構成する方法については、[Commerce 評価環境のコンフィギュレーション](cpe-post-provisioning.md) を参照してください。 Commerce 評価環境のオプション機能を構成する方法については、[Commerce 評価環境のオプション機能のコンフィギュレーション](cpe-optional-features.md) を参照してください。

## <a name="prerequisites"></a>必要条件

Commerce 評価環境をプロビジョニングする前に、次の前提条件が整っている必要があります。

- あなたは評価プログラムに参加し、評価環境の能力を付与されました。
- Microsoft Dynamics Lifecycle Services (LCS) ポータルへのアクセス許可があります。
- 既存の Microsoft Dynamics 365 のパートナーまたは顧客は、Dynamics 365 Commerce プロジェクトを作成できます。
- Microsoft Azure サブスクリプションへの管理者アクセスがあるか、必要に応じてサポートできるサブスクリプション管理者に連絡しています。
- Azure Active Directory (Azure AD) テナント ID が使用可能です。
- E コマース システムの管理者グループとして使用される  Azure AD セキュリティ グループが作成され、その ID が使用可能になりました。
- 評価とレビューのモデレーター グループとして使用される  Azure AD セキュリティ グループが作成され、その ID が使用可能になりました。 (このセキュリティ グループは、E コマースのシステム管理グループと同じにすることができます。)

このリストは包括的なものではないことに注意してください。 問題が発生した場合は、Microsoft パートナーの連絡先に問い合わせてください。

## <a name="provision-your-commerce-evaluation-environment"></a>Commerce 評価環境のプロビジョニング

これらの手順は、Commerce 評価環境をプロビジョニングする方法を説明しています。 それらを正常に完了すると、Commerce 評価環境を構成する準備が整います。 ここで説明するすべての活動は、LCS ポータルで発生します。

### <a name="create-a-new-project"></a>新しいプロジェクトの作成

LCS に新しいプロジェクトを作成するには、次の手順を実行します。

1. LCS のホーム ページで、プラス記号 (**+**) を選択してプロジェクトを作成します。
1. 右側のウィンドウで、次のいずれかのステップを実行します。

    - パートナーである場合、**移行、ソリューションの作成、および学習** を選択します。
    - 顧客の場合、**見込みプリセールス** を選択します。

1. 名前と説明、および業種を入力します。
1. **製品名** フィールドで、**Dynamics 365 Commerce** を選択します。
1. **製品バージョン** フィールドで、**Dynamics 365 Commerce** を選択します。
1. **方法** フィールドで、**Dynamics Retail の実装方法** を選択します。
1. オプション: ロールとユーザーを既存のプロジェクトからインポートできます。
1. **作成** を選択します。 プロジェクト ビューが表示されます。

### <a name="add-the-azure-connector"></a>Azure コネクタの追加

Azure コネクタ を LCS プロジェクトに追加するには、[Azure Resource Manager (ARM) 研修プロセス](../fin-ops-core/dev-itpro/deployment/arm-onboarding.md) の手順に従ってください。

### <a name="deploy-the-environment"></a>環境の配置

環境を配置するには、次の手順に従います。

> [!NOTE]
> オプションが 1 つしかないページはスキップされるため、手順 6、7、または 8 を完了する必要はありません。 **環境パラメーター** ビューで、**Dynamics 365 Commerce - デモ (10.0.* x* プラットフォーム更新プログラム *xx*)** が **環境名** フィールドのすぐ上に表示されていることを確認します。 詳細については、手順 8 の後に表示されているイラストを参照してください。

1. トップ メニューで、**クラウド ホスト環境** を選択します。
1. 環境を追加するために **追加** を選択します。
1. **アプリケーション バージョン** フィールドで、最新のバージョンを選択します。 最新バージョン以外のアプリケーション バージョンを特定する必要がある場合は、**10.0.14** より前のバージョンを選択しないでください。
1. **プラットフォーム バージョン** フィールドで、選択したアプリケーション バージョンに対して自動的に選択されたプラットフォーム バージョンを使用します。 

    ![アプリケーションとプラットフォーム バージョンを選択する。](./media/project1.png)

1. **次へ** を選択します。
1. 環境のトポロジとして **デモ** を選択します。

    ![環境トポロジ 1 を選択する。](./media/project2.png)

1. **環境の配置** のページで、環境名を入力します。 詳細設定はそのままにしておきます。

    ![環境の配置のページ。](./media/project4.png)

1. VM サイズを必要に応じて調整します。 (VM 最小在庫管理単位をお勧めします \[SKU\] **D13 v2**。)
1. 価格決定およびライセンス条件を確認、チェック ボックスをオンにして同意したことを示します。
1. **次へ** を選択します。
1. 配置の確認ページで、詳細が正しいことを確認した後、**配置** を選択します。 **クラウド ホスト環境** ビューに戻り、環境がリストに表示されます。

    要求した環境はキューに格納され、その後配置されます。 環境ワークフローは完了までに少し時間がかかることがあります。 そのため、約 6 ~ 9 時間後に再度確認してください。

1. 続行する前に、環境の状態が **配置済み** になっていることを確認してください。

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Commerce Scale Unit (CSU) を初期化する (クラウド)

CSU を初期化するには、次の手順に従います。

1. **クラウド ホスト環境** ビュー内で、リストから環境を選択します。
1. 右側の環境ビューで、**完全な詳細** を選択します。 環境の詳細のビューが表示されます。
1. **環境機能** の下で、**管理** を選択します。
1. **コマース** タブで、**初期化** を選択します。 CSU 初期化パラメーター ビューが表示されます。
1. **地域** フィールドで、環境を配置したのと同じか、またはそれに近い地域を選択します。
1. **バージョン** フィールドはそのままにしておきます。
1. **初期化** を選択します。
1. 配置の確認ページで、詳細が正しいことを確認した後、**はい** を選択します。 **コマース** タブが選択されているところでは、**コマースの管理** ビューが再度表示されます。 CSU がプロビジョニング用にキューに格納されました。
1. 続行する前に、CSU の状態が **成功** となっていることを確認します。 初期化には約 2 ~ 5 時間かかります。

環境の詳細ビューに **管理** リンクが見つからない場合は 、Microsoft の連絡先に問い合わせてください。

デプロイのプロセスでは、次のエラー メッセージが表示される場合があります。

> 評価 (デモ/テスト) 環境では、スケール ユニット コネクタ アプリケーションを本部の \<application ID\> に登録する必要があります。

CSU の初期化が失敗してこのエラー メッセージが表示された場合は、アプリケーション ID (グローバル一意識別子 : GUID) をメモし、次のセクションの手順に従って CSU デプロイ アプリケーションをCommerce 本部に登録します。

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a>Commerce 本部に CSU デプロイ アプリケーションを登録します (必要に応じて)

Commerce 本部に CSU デプロイ アプリケーションを登録するには、次の手順に従います。

1. Commerce 本部で、**システム管理 \> 設定 \> Azure Active Directory アプリケーション** に移動します。
1. **クライアント ID** 列に、受信した CSU 初期化エラー メッセージのアプリケーション ID を入力します。
1. **名前** 列に、説明用テキスト (例 : **CSU Eval**) を入力します 。
1. **ユーザー ID** 列に、**RetailServiceAccount** と入力します。
1. LCS から CSU の初期化とデプロイを再試行します。

### <a name="initialize-e-commerce"></a>E コマースの初期化

E コマースを初期化するためには、次の手順に従います。

1. **E コマース** タブで、評価の同意を確認し、**設定** を選択します。
1. **E コマース環境名** フィールドに名前を入力します。 この名前は E コマース インスタンスを指す URL の一部に表示されることに注意してください。
1. **Commerce Scale Unit の名前** フィールドで、リストから CSU を選択します。 (リストには 1 つのオプションのみが必要です。)

    **E コマースの地域** フィールドは自動的に設定されます。

1. **次へ** を選択して続行します。
1. **サポートされているホスト名** フィールドに、`www.fabrikam.com` などの有効なドメインを入力します。
1. **システム管理者の AAD セキュリティ グループ** フィールドに、使用するセキュリティ グループの名前の最初の数文字を入力し、虫眼鏡記号を選択して検索結果を表示します。 リストで正しいセキュリティ グループを選択します。
1.  **評価とレビュー モデレーター用 AAD セキュリティ グループ** フィールドに、使用するセキュリティ グループの名前の最初の数文字を入力し、虫眼鏡記号を選択して検索結果を表示します。 リストで正しいセキュリティ グループを選択します。
1. **評価とレビュー サービスを有効にする** オプションを、**はい** のままにします。
1. **初期化** を選択します。 **E コマース** タブが選択されているところでは、**コマースの管理** ビューが再度表示されます。 E コマースの初期化を開始しました。
1. 続行する前に、E コマースの初期化状態が **初期化成功** になるまでお待ちください。
1. 右下の **リンク** で、次のリンクの URL をメモします。

    * **E コマース サイト** – E コマース サイトのルートへのリンク。
    * **Commerce サイト ビルダー** – サイト管理ツールへのリンク。

## <a name="next-steps"></a>次のステップ

Commerce 評価環境のプロビジョニングと構成のプロセスを続行するには、[Commerce 評価環境のコンフィギュレーション](cpe-post-provisioning.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[Dynamics 365 Commerce 評価環境の概要](cpe-overview.md)

[Dynamics 365 Commerce の評価環境を構成する](cpe-post-provisioning.md)

[Dynamics 365 Commerce 評価環境で BOPIS を構成する](cpe-bopis.md)

[Dynamics 365 Commerce 評価環境のオプション機能を構成する](cpe-optional-features.md)

[Dynamics 365 Commerce 評価環境に関するよく寄せられる質問](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit (クラウド)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure ポータル](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce Web サイト](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]