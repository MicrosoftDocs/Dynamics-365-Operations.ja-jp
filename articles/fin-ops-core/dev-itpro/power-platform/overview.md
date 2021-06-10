---
title: Finance and Operations アプリと Microsoft Power Platform の統合
description: このトピックでは Microsoft Dataverse および Finance and Operations アプリ の Microsoft Dynamics Lifecycle Services を介して Microsoft Power Platform の統合の概要を提供します。
author: Sunil-Garg
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 1c98ec12ade16e4850b624fdec69681b16b357c9
ms.sourcegitcommit: 6884d9c845a8d16e7a18d5a3880606e3cbe78b95
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/27/2021
ms.locfileid: "6111368"
---
# <a name="microsoft-power-platform-integration-with-finance-and-operations-apps"></a>Finance and Operations アプリと Microsoft Power Platform の統合

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Power Platform は、Power Platform 管理者センターを介した Dynamics 365 アプリケーションの一連の機能を提供します。 今日、Finance and Operations アプリは Power Platform 管理者センターで管理されていません。 ただし、時間の経過とともに、Microsoft Dynamics Lifecycle Services (LCS) から管理センターに移行される管理機能がますます増えています。 暫定的に、顧客は、LCS の Microsoft Power Platform 統合機能を介して、二重書き込み機能、仮想エンティティ、アドインなどの機能のロックを解除できるようになります。

## <a name="prerequisite-reading"></a>前提条件の参照先

Microsoft Power Platform、Dataverse、二重書き込み、および Finance and Operations アプリの仮想エンティティのアーキテクチャを理解するには、それらのしくみを理解しておく必要があります。 したがって、次のドキュメントが前提条件になります。

- [Power Platform の管理](/power-platform/admin/admin-documentation)
- [Dataverse とは](/powerapps/maker/common-data-service/data-platform-intro)
- [Dataverse のテーブル](/powerapps/maker/common-data-service/entity-overview)
- [エンティティの関連付けの概要](/powerapps/maker/common-data-service/relationships-overview)
- [外部データ ソースのデータを含む仮想テーブルの作成と編集](/powerapps/maker/common-data-service/create-edit-virtual-entities)
- [Power Apps ポータルについて](/powerapps/maker/portals/overview)
- [Power Apps でのアプリの作成の概要](/powerapps/maker/)

## <a name="tools-and-services-unlocked-with-microsoft-power-platform-integration"></a>Microsoft Power Platform 統合によってロックが解除されたツールとサービス

同時に、仮想エンティティ、二重書き込み、およびビジネス イベントは、Finance and Operations アプリと Dataverse プラットフォームの収束性に対する共有データ レイヤーを構成しています。 これらは、一緒に仕様することを目的とした補完的なテクノロジです。 

**仮想エンティティ** により、Microsoft Power Platform または Dataverse ネイティブ アプリから Finance and Operations データへのアクセスが必要になるシナリオが有効になります。 そのデータをクエリしてフォームをバインドし、一般的には、Finance and Operations アプリの全機能に対して Microsoft Power Platform の完全な機能を使用することができます。 システム間でデータはコピーされません。 代わりに、Microsoft Power Platform テクノロジが既にバインドすることができる標準の仮想エンティティ インフラストラクチャを通して直接アクセスします。 詳細については、[仮想エンティティの概要](virtual-entities-overview.md)を参照してください。 

**ビジネス イベント** により、Microsoft Power Platform を使用して Finance and Operations アプリで発生するイベントに応答できます。 ビジネス イベントは、Finance and Operations アプリを含め、任意のアプリから発生させることができ、Microsoft Power Platform ビジネス ロジックによって処理することができます。 多くの場合、この処理には、ネイティブ エンティティまたは仮想エンティティを通じた追加データのクエリや操作が含まれます。 

シナリオのサブセットについては、Finance and Operations アプリと Dataverse ネイティブ エンティティの間でデータを物理的にコピーする必要があります。 これらのシナリオは、Dataverse ネイティブ アプリと Finance and Operations アプリの両方でバインドされた大量のロジックを持つ重複するエンティティを対象としているので、データを各タイプのアプリのローカル データベースに配置する必要があります。 これらのエンティティの数は比較的少ないがが、アカウント/顧客、会社、製品、および販売注文などの最も重要なエンティティの一部が含まれます。 これらのシナリオでは、**二重書き込み** により、ほぼリアルタイムの同期コピーが可能になります。 この機能により、既存のアプリはローカル データに対する操作を設計通りに継続することができ、また対応する重複エンティティが同期されていることを確認することができます。詳細については、[二重書き込みのホームページ](../data-entities/dual-write/dual-write-home-page.md)を参照してください。 

同時に、仮想エンティティ、二重書き込み、およびビジネス イベントにより、Finance and Operations アプリと Dataverse ネイティブ アプリ間の境界をまたぐアプリと業務プロセスをビルドすることができます。 ほとんどのアプリと業務プロセスでは、これら共有データ レイヤーの 3 つの部分の組み合わせかすべてのいずれかが使用されます。 同様に、拡張機能およびカスタマイズにおいて、データベース間でコピーされるデータ量を可能な限り減少させる必要があり、これらのツールを使用する際に、最も有利なユーザー エクスペリエンス用に最適化する必要もあります。 

### <a name="add-ins-functionality"></a>アドイン機能

アドインを使用すると、Finance and Operations アプリの機能を拡張できます。 すべてのアドインは、サンドボックスおよび実稼働タイプの環境の環境詳細ページの Lifecycle Services を介してインストールされ、管理されます。 インストールされているアドインと各アドインの構成オプションに関するメタデータは、Microsoft Power Platform 統合の一部としてプロビジョニングされている Microsoft Dataverse データベースに格納されます。 一部のアドインは、Dataverse データベースにビジネス データも格納します。 使用可能なアドインの詳細については、[アドインの概要](add-ins-overview.md) を参照してください。

## <a name="typical-scenarios-and-patterns-that-use-dual-write"></a>二重書き込みを使用する一般的なシナリオとパターン

二重書き込みを使用する一般的なシナリオを次に示します。

### <a name="customer-service-representatives-can-facilitate-a-change-of-address-for-finance-and-operations-customers"></a>顧客サービス担当者が Finance and Operations の顧客の住所変更を容易にできるようにする

顧客が移転し、請求先住所と送付先住所の情報を変更したいとします。 この顧客は、顧客サービス担当者に連絡して、住所の変更を依頼します。 顧客サービス担当者が電話を受け、顧客の請求先住所と送付先住所を変更します。

| 意思決定 | 情報 | 
|----------|-------------|
| リアルタイムな日付が必要ですか。 | あり |
| ピーク データ量 | 適用できません |
| 頻度 | アドホック |

#### <a name="recommended-solution"></a>推奨される解決策

ほぼリアルタイムのデータ同期が関係するシナリオでは、二重書き込みで実装するのが最適です。

1. 顧客情報は、Finance and Operations アプリから取得されます。
2. 顧客が顧客サービスに電話し、請求先住所と送付先住所の情報を変更するよう依頼します。
3. 顧客サービス担当者は、Dynamics 365 Customer Service の顧客レコードを取得します。
4. 顧客サービス担当者は、請求先住所と送付先住所を更新してデータを保存します。
5. 新しい請求先住所と送付先住所は、リアルタイムで Finance and Operations アプリに同期されます。

### <a name="sales-representatives-can-change-customer-credit-limits-without-signing-in-to-a-finance-and-operations-app"></a>販売担当者は、Finance and Operations アプリにサインインすることなく、顧客の与信限度額を変更できます

顧客には $2,000 の与信限度額があり、$5,000 に引き上げたいと考えています。 この顧客が電話をかけて、増額を要求します。 チケットが、販売部門に割り当てられます。 販売責任者は依頼を検討し、顧客の支払履歴を確認し、顧客が与信限度額の増加の資格があると判断します。 販売責任者は依頼を承認し、チケットに応答します。 顧客は与信限度額 $5,000 の承認に関する電子メールを受け取ります。

| 意思決定 | 情報 | 
|---------|--------------|
| リアルタイムな日付が必要ですか。 | あり |
| ピーク データ量 | 適用できません |
| 頻度 | アドホック |

#### <a name="recommended-solution"></a>推奨される解決策

このシナリオでは、二重書き込みを使用して実装するのが最適です。

1. 顧客は電話し、与信限度額を $2,000 から $5,000 に引き上げたいと考えています。
2. 顧客サポート担当者が Dynamics 365 Customer Service でチケットを作成します。
3. チケットが、販売部門に割り当てられます。
4. 販売部門の販売担当者が依頼を確認して、承認します。
5. Dynamics 365 Sales で顧客の与信限度額が $5,000 に増額されます。
6. Finance and Operations アプリの与信限度額が $5,000 に更新されます。
7. 販売担当者は、チケットに応答して解決します。
8. 顧客は、与信限度額の引き上げに関する電子メールを受け取ります。

## <a name="prerequisites-for-setting-up-the-microsoft-power-platform-integration"></a>Microsoft Power Platform 統合を設定するための前提条件

次の一覧は、Microsoft Power Platform 統合を設定するための前提条件に関する詳細を提供します。

- テナントで少なくとも 1 ギガバイト (GB) の Microsoft Power Platform データベース ストレージ容量スペースが使用可能であることを確認してください。 それ以外の場合、設定は失敗です。 [Power Platform管理センター](https://admin.powerplatform.microsoft.com/resources/capacity) にて、容量を表示できます。 

- Finance and Operations 環境管理者を識別します。 **環境の詳細** セクションにて、情報を確認できます。

    ![環境の詳細タブ](media/EnvironmentDetails.png)

- Microsoft Power Platform 環境ガバナンス ポリシーを検証します。 検証するには、**グローバル管理者** または **Power Platform 管理者** である必要があります。

    1. [Power Platform 管理センター](https://admin.powerplatform.microsoft.com) にサイン インします。
    2. ページの右上隅にある **設定** ボタン (ギヤ記号) を選択して、**Power Platform 設定** ウィンドウを開きます。

        ![Power Platform 設定ウィンドウ](media/PowerPlatformSettings.png)

- 全員に Microsoft Power Platform 実稼働環境の作成を **許可しない** 組織のために、Finance and Operations 環境管理者のアカウントを次の Microsoft Power Platform 管理ロールの 1 つを追加する必要があります。 この変更を行うには、**グローバル管理者** が必要です。

    - Global 管理者
    - Dynamics 365 管理者
    - Power Platform 管理者

    > [!NOTE]
    > 上記のロールは、Finance and Operations 管理者アカウントに必要なアクセス許可よりも多くのアクセス許可を提供することがあります。 したがって、この統合にさらに制限されたロールが最終的に Azure Active Directory (Azure AD) に追加されます。 新しいロールに上記のロールは必要ではありません。 最小限の特権の管理者を維持する場合、一時的に上記のロールの 1 つを付与できます。 Microsoft Power Platform 統合が設定された後、そのロールを削除します。

- Microsoft Power Platform 環境を作成するすべてのユーザーはライセンスが必要です。 **Dynamics 365 Unified Operations プラン** または **AX エンタープライズ** ライセンス、または **Dynamics 365 Finance** などのアプリケーション固有のライセンスを Finance and Operations 環境の管理者アカウントに適用するには、Microsoft 365 管理センターを使用する必要があります。

## <a name="enabling-the-microsoft-power-platform-integration"></a>Microsoft Power Platform 統合の有効化

Microsoft Power Platform 統合は、LCS で新しい Finance and Operations 環境を作成するときに有効にすることができます。 また、既存の Finance and Operations 環境で有効にできます。

### <a name="enable-during-environment-deployment"></a>環境の配置中に有効にする

LCS に新しい Finance and Operations 環境を設定する場合、配置ウィザードには値を設定することができる複数のセクションが含まれています。 それらセクションの 1 つが **Power Platform 統合** という名前です 。

![配置ウィザードの Power Platform 統合セクション](media/powerplat_integration_step0.png)

**Power Platform 統合** セクションを構成するには、次の手順に従います。

1. **Power Platform 環境の構成** オプションを **はい** に設定します。 複数の追加設定が使用可能になります。
2. **Power Platform テンプレート** フィールドで、次のいずれかの値を選択します。

    - **Dynamics 365 標準** – この基本テンプレートは、すべての Finance and Operations 環境に適用できます。 特定のテンプレートが必要ない場合、この値を選択します。
    - **Project Operations** – このテンプレートは、プロジェクト操作のシナリオに固有のものです。 この値は、テナントに Dynamics 365 Project Operations のライセンスと資格が付与されている場合にのみ使用できます。

3. DevTest またはクラウド ホスト環境を配置する場合、**環境の種類** フィールドが使用可能です。 そこで、作成しリンクする Dataverse 環境の種類を選択できます。 それ以外の場合、既定では、環境の種類はレベル 2 から 5 の承認テスト環境の場合は **サンドボックス** に、運用環境の場合は **運用** に設定されます。
4. **同意** チェック ボックスをオンにして、統合の使用条件に同意することを示します。

> [!IMPORTANT]
> Finance and Operations 環境に作成およびリンクされる Dataverse 環境の **言語** および **通貨** の値は、Azure AD テナントの物理的なアドレスに基づいて自動的に決定されます。 たとえば、住所が米国ワシントン州 Redmond である場合、既定では言語は英語で、通貨は米ドル (USD) になります。
>
> 既定値とは異なる値が必要な場合、Microsoft サポートに問い合わせください。 Finance and Operations 環境に手動でプロビジョニングする既存の Dataverse 環境をリンクすることができます。 最終的には、設定オプションとして言語と通貨のフィールドが追加され、顧客は手動で設定したり、既定値を受け入れることができます。

### <a name="set-up-after-environment-deployment"></a>環境を配置後に設定
Finance and Operations 環境が配置された後に設定するには、次の手順に従います。

1. Finance and Operations 環境が LCS を通じて展開された後、LCS の **環境詳細** ページが開きます。
2. **Power Platform 統合** セクションで、**設定** を選択します。

    ![Power Platform 統合セクションの設定ボタン](media/powerplat_integration_step1.png) 

3. **Power Platform 環境の設定** ダイアログ ボックスで契約条件に同意し、ダイアログ ボックスの下部にある **設定** を選択します。

    > [!NOTE]
    > これにより、Power Platform 管理センターで Microsoft Dataverse ベースの環境がプロビジョニングされ、通常は 1GB のデータベース ストレージ容量が必要になります。 使用する Finance and Operations 環境と同じ名前が必要です。 二重書き込みプラットフォーム レベルのコンポーネントはインストールされますが、二重書き込みアプリケーション コンポーネントは設定または有効化されません。 これは別のアクションです。

4. Microsoft Power Platform 環境が準備されているというメッセージが表示された場合は、**OK** を選択します。

    **環境詳細** ページの **Power Platform 統合** セクションに、Microsoft Power Platform 環境が準備されているというメッセージが表示されます。

5. 数分後、**環境の詳細** ページが更新されます。
6. **Power Platform 統合** セクションにおいて、**ステータス** フィールドの値が **環境設定が進行中** であることに注意してください。

    通常、設定は 60分 から 90分かかります。

    Dataverse 環境がプロビジョニングされた後、**新しいアドインのインストール** と **二重書き込みアプリケーション** ボタンが **Power Platform 統合** セクションで利用できます。

    ![新しいアドイン ボタンのインストール](media/InstallANewAddIn.png)

    ![二重書き込みアプリケーション ボタン](media/powerplat_integration_dwApp_button.png)

> [!IMPORTANT]
> Finance and Operations 環境に作成およびリンクされる Dataverse 環境の **言語** および **通貨** の値は、Azure AD テナントの物理的なアドレスに基づいて自動的に決定されます。 たとえば、住所が米国ワシントン州 Redmond である場合、既定では言語は英語で、通貨は米ドル (USD) になります。
>
> 既定値とは異なる値が必要な場合、Microsoft サポートに問い合わせください。 Finance and Operations 環境に手動でプロビジョニングする既存の Dataverse 環境をリンクすることができます。 最終的には、設定オプションとして言語と通貨のフィールドが追加され、顧客は手動で設定したり、既定値を受け入れることができます。


### <a name="troubleshooting-the-setup"></a>設定のトラブルシューティング

設定は、Dataverse ベースの環境を配置するさまざまなステージで失敗する可能性があります。 

![デュアル書き込みの失敗](media/Error.png)

- 設定が失敗すると、エラー メッセージが表示されます。 エラー メッセージに基づいて、ライセンスや容量の問題に対処する必要がある場合があります。 これらが解決されたら、LCS の **環境の詳細** ページの **Power Platform 統合** セクションにある **再開** ボタンを使用して設定を完了することができます。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
