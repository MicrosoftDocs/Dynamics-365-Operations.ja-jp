---
title: プレビュー サブスクリプションのサインアップ
description: このトピックでは、プレビュー/パートナー オファーをサブスクライブして環境を配置する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 05/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: 13211
ms.assetid: bd976311-f6e3-418b-a6c6-49bb568de130
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 218e46d6cc90d24d9481d2eb741f9bb7c6e6c4b2
ms.sourcegitcommit: 69e41165cd07434ab0d1a35f749018b5659b063e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/11/2020
ms.locfileid: "3037196"
---
# <a name="sign-up-for-preview-subscriptions"></a>プレビュー サブスクリプションのサインアップ

[!include [banner](../includes/banner.md)]

このトピックでは、プレビュー/パートナー オファーをサブスクライブして環境を配置する方法について説明します。 サブスクリプションを作成すると、Microsoft Online Services のテストテナントと、環境を展開できる Microsoft Dynamics Lifecycle Services (LCS) プロジェクトが提供されます。 このトピックでは、Microsoft Online Services テナントに追加ユーザーを設定し、サービス管理機能の経験を積むのにも役立ちます。 学ぶスキルを次に示します。

- 新しい Microsoft オンライン テスト テナントを購読して作成します。
- LCS プロジェクトに移動します。
- LCS の各種機能を使用します。
- Microsoft Azure Active Directory (Azure AD) とクライアントにユーザーを追加します。
- サブスクリプション電子メールのリソースを表示します。

## <a name="key-terms"></a>重要な用語
- **Microsoft Online Services テナント** – テナントは、組織のすべての定期売買とユーザーのグループです。 テナントは、Microsoft Online Services の最初のサブスクリプションと同時に作成されます。
- **定期売買** – 定期売買により、オンライン クラウドの環境と経験が得られます。 また、これにより、作成したカスタマイズをクラウドに配置する方法も確認できます。
- **Microsoft Azure Active Directory** – クラウド環境には、Azure AD が含まれます。 オンプレミス環境の管理と同様、Azure AD はオンライン アプリケーションのユーザー、グループ、セキュリティ ロール、およびライセンスを管理するのに役立ちます。
- **ユーザー** – 組織がサブスクリプションしているサービスのユーザーは Azure AD で管理されます。 テナント内のすべてのユーザーを追加して、セキュリティ ロールに割り当てることができます。
- **開発者と管理者** - 開発者と管理者は、プロジェクトや環境を管理できる LCS にもアクセスできるユーザーです。 これらのユーザーは、エンド ユーザーでもあります。
- **組織アカウント** – ユーザーは Azure AD 資格情報を取得します。 これらの資格情報は、他のデスクトップまたは企業の資格情報とは異なります。 Azure AD 資格情報は、Microsoft Office 365 およびその他の Microsoft クラウド サービスへのサインインに使用されます。 ユーザーは組織のアカウントを使用してサインインします。

    > [!IMPORTANT]
    > 今回のリリースでは、Office 365 または Microsoft Dynamics CRM Online などの他のオンライン サービスに関連付けられている、既存の資格情報を使用しないようお勧めします。

- **Microsoft アカウント** – Microsoft アカウントは、以前は Passport アカウントまたは Windows Live ID アカウントと呼ばれていました。 現在、Finance and Operations アプリケーション、Microsoft Dynamics 365 Commerce、またはその他の Microsoft オンライン サービスで Microsoft アカウントを使用することはできません。 ただし、Microsoft アカウントは、CustomerSource、PartnerSource、ソース情報、および Microsoft Dynamics コミュニティなどの Microsoft Connect および他の Microsoft Business Solutions サイトに対して必要です。 これらのサービスにアクセスするには、Microsoft アカウントを引き続き使用します。
- **Microsoft Office 365 管理者センター** – Office 365 管理者センターは、Office 365 が管理者に提供する定期売買管理ポータルです。 Office 365 管理者センターは、ユーザーおよびサブスクリプションの管理機能を提供するために使用されます。
- **環境** - 必要に応じて、仮想マシン (VM) の単一インスタンスをいくつでも配置できます。 これらのインスタンスを *環境* と呼び出ます。

## <a name="prerequisites"></a>前提条件
1. プレビューへの参加を招待する電子メールを受信しました。
2. 会社に Microsoft Online Services 付きの組織アカウントがあり、サインインしている場合、続行する前にサインアウトする必要があります。 または、**InPrivate ブラウズ**モードを使用することができます。
3. ログオンしているかどうか分からない場合は、ブラウザーのクッキーを削除し、続行する前にブラウザーを閉じます。

## <a name="subscribe"></a>サブスクライブ
> [!IMPORTANT]
> 組織内で 1 人 (テナント管理者) だけ、このタスクを実行する必要があります。 このリリースをサブスクライブしていない場合は、組織がサインアップし、ユーザーの資格情報を受信するまで待機します。 その後、手順を続行します。

1. Finance and Operations アプリケーションおよび Retail は、既存の Microsoft Dynamics 365 のチャネル パートナーおよび Business Ready 拡張プラン (BREP) サービス プランに現在登録されている顧客にのみ使用できます。 既存の顧客は、[CustomerSource](https://mbs.microsoft.com/customersource/Global/365Enterprise/news-events/news/md365financeoperationsenterprisecusttrial) の試用版にアクセスする詳細方法を検索できます。 パートナーは、[PartnerSource](https://mbs.microsoft.com/partnersource/global/news-events/news/Microsoft_Dynamics_AX_Public_Preview) で詳細を参照できます。
2. **アカウント設定**ページの、**国または地域**フィールドで、国または地域の選択をします。
3. 最後のステップに到達するまで、サインアップを完了するウィザードおよびプロンプトに従います。

    [![準備ができました](./media/wizardprompt.png)](./media/wizardprompt.png)

## <a name="start-a-new-project-in-lcs"></a>LCS で新しいプロジェクトを開始
LCS を使用して環境を管理するには、新しいプロジェクトを作成する必要があります。

1. <https://lcs.dynamics.com/Logon/Index> に移動します。
2. **サインイン** を選択します。
3. サブスクライブするために使用したアカウントを使用してサインインします。
4. プラス記号 (**+**) を選択して新しいプロジェクトを作成します。

    [![プロジェクトの作成](./media/11.jpg)](./media/11.jpg)

5. プロジェクト タイプを選択します。
6. プロジェクト情報を入力し、**作成**を選択します。

    コマースを評価する予定がある場合は、**製品名**フィールドで **Microsoft Dynamics 365 Commerce** を必ず選択します。

    インスタンスを管理するための新しいプロジェクトが作成されます。

    ![新規プロジェクト](./media/projectworkspace.jpg)

## <a name="add-users-to-lcs"></a>LCS へのユーザーの追加
LCS プロジェクトのユーザーとして既に設定しています。 他の Office 365 ユーザーも追加した場合、このプロジェクトに追加する必要があります。 他の管理者や開発者は、独自の環境の配置できるようになります。 これらの LCS ユーザーは、実装に積極的に取り組むチーム メンバーです。 エンド ユーザーと混同しないでください。 LCS でプロジェクト ページを開始します。

1. 右にスクロールし、**追加ツール** セクションで、**プロジェクト ユーザー** タイルを選択します。
2. 左上で、プラス記号 (**+**) を選択して新しいユーザーを追加します。
3. **電子メール** フィールドに、追加するユーザーの電子メール アドレスを入力します。 この電子メール アドレスは、以前作成した Office 365 組織の電子メール アドレスである必要があります。
4. **プロジェクトのロール** フィールドで、**プロジェクト所有者**を選択します。
5. **招待** を選択します。
6. 組織内のすべてのユーザーに対して手順 2 ～ 5 を繰り返します。

## <a name="deploy-environments"></a>環境の配置
環境では、既存の Azure サブスクリプションを配置する必要があります。

> [!NOTE]
> それぞれの環境開発者は、Azure に自身のシステムを導入する必要があります。 ただし、最初のプロジェクト ユーザーのみが配置の Azure サブスクリプションを設定する必要があります。

2 種類の方法で環境を作成することができます。

- Microsoft クラウド サービス (Azure) に配置します。
- ローケル仮想ハード ディスク (VHD) をダウンロードします。

LCS でプロジェクト ページを開始します。

1. **環境**セクションで、プラス記号 (**+**) を選択します。 **Microsoft Azure 設定**ダイアログ ボックスが表示されます。
2. Azure サブスクリプション ID を入力します。 Azure サブスクリプション ID は Azure Portal (<https://ms.portal.azure.com/>) の、左下の **設定** で見つけることができます。
3. **次へ** を選択します。
4. Azure Management Certificate をコンピューターのローカル フォルダーにダウンロードし、**設定** &gt; **管理証明書**にアクセスして Azure Management Portal を更新します。 この証明書は、自分の代わりに LCS が Azure と通信できるようにします。
5. LCS に戻り、**次へ** を選択します。
6. 配置する Azure リージョンを選択します。 **米国西部** 地域は展開が最も速くなっていますが、このシステムを使用する場所に近いデータ センターを選択することが重要です。
7. **接続** を選択します。
8. 使用可能なトポロジの一覧で、配置するトポロジを選択します。 VHD をダウンロードする **ダウンロード** リンク、または Azure 上に展開する **次へ** のいずれかを選択することができます。 Azure は優先されるパスです。
9. 環境名を入力します。
10. 価格決定およびライセンス条件を読み、チェック ボックスをオンにして理解したことを示します。
11. **次へ** を選択します。
12. 詳細を確認し、**配置**を選択します。

    > [!NOTE]
    > 独自の環境を使用する開発者および管理者は、サインインしてこれらの手順を繰り返す必要があります。
    
    環境を配置した後、**環境**セクションは使用可能です。

    [![環境セクションにある新規環境](./media/pic7.jpg)](./media/pic7.jpg)

13. 配置のステータスに関する詳細を表示するための環境を選択します。 最初の配置には数時間かかりますが、その後の配置はずっと高速になります。
14. 配置状態が **配置済み** に変わったときに、**ログイン** を選択してクライアントに接続するか、または VM の名前を選択して、リモート デスクトップを使用して開発マシンに接続します。 配置が完了した後、リモート デスクトップ経由で環境に接続するために必要な基本 URL と情報を見つけることができます。

## <a name="use-the-features-of-lcs"></a>LCS 機能の使用
LCS は、オンライン管理アクティビティを実行するための出発点です。 これらの活動例を次に示します。

- Azure に VM を配置します。
- アクセスの材料。
- ツールとリソースのダウンロードにアクセス。

### <a name="explore-the-lcs-project"></a>LCS プロジェクトを検証
1. 方法を確認し、ライフ サイクルを通過するときにタスクとフェーズを完了します。

    [![フェーズおよびタスク](./media/pic8.jpg)](./media/pic8.jpg)[](./media/methodologyreview.png)
    
    フェーズとタスクの情報により、エンタープライズ リソース プランニング (ERP) エクスペリエンスの全体を通して使用できるツールとリソースを表示できます。

2. 右にスクロールし、タイルを確認します。

    [![タイル](./media/pic9.jpg)](./media/pic9.jpg)

    使用可能なタイルには、LCS のさまざまなツールとサービスがあります。 次の追加のタイトルも含まれます。

    - **自分の定期売買** – Office 365 定期売買の管理ポータルでは、オンライン定期売買を表示して操作できます。 ページの左側のナビゲーション セクションで**ユーザーとグループ**を選択することにより、オンライン ユーザーを管理することもできます。

        > [!NOTE]
        > このページにアクセスするには、組織の Microsoft Online Services テナントにおいて**グローバル管理者** ロールのメンバーである必要があります。

    - **フィードバックとバグ** – このタイルは Microsoft Connect の**全般フィードバック**ページを開きます。 バグの記録や、設計変更要求、機能要求、提案を行うには、このページを使用します。
    - **Office 365 ユーザー** – このタイルは Office 365 管理者センターの**ユーザーおよびグループ**ページを開きます。 他のサービスのためにユーザーを追加、更新、および削除し、パスワードをリセットし、ライセンスを割り当てることができます。

        > [!NOTE]
        > このページにアクセスするには、組織の Microsoft Online Services テナントにおいて**グローバル管理者** ロールのメンバーである必要があります。 インストール ユーザーは常にグローバル管理者ですが、他のユーザーをこのロールに追加する必要があります。

        [![Office 365 管理者センターの有効なユーザー](./media/activeusersadmin.png)](./media/activeusersadmin.png)
