---
title: Finance and Operations のアーキテクチャ
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のアーキテクチャの概要を提供します。
author: ClaudiaBetz-Haubold
manager: AnnBe
ms.date: 06/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 56551
ms.assetid: d876e8de-d547-43e5-9259-f095821dc758
ms.search.region: Global
ms.author: chaubold
ms.search.validFrom: 2018-05-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca848cc0849bd65019ed02c58c52bab87a4322bc
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1507997"
---
# <a name="finance-and-operations-architecture"></a>Finance and Operations のアーキテクチャ

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations クラウド アーキテクチャには、[定期売買、ライセンス、アカウントおよび Microsoft のクラウド提供のテナント](https://docs.microsoft.com/office365/enterprise/subscriptions-licenses-accounts-and-tenants-for-microsoft-cloud-offerings)に説明されているように、すべての Microsoft クラウド提供に共通する全ての要素が含まれています。 さらに、ソフトウェアの展開とプロビジョニング、運用の監視とレポート、およびシームレスなアプリケーション ライフサイクル管理を自動化するサービスが含まれます。

![クラウド アーキテクチャ](./media/cloud-architecture.png)

Finance and Operations のクラウド アーキテクチャは、これらの概念領域で構成されています。

- **サブスクリプション** – Microsoft Dynamics 365 for Finance and Operations (クラウド) に対するサブスクリプションは、オンライン クラウド環境 (または複数の環境) およびエクスペリエンスを提供します。
- **ライセンス** – 顧客は、組織または関連会社の従業員のために、およびオンサイト エージェント、仕入先、直接または間接的に Finance and Operations にアクセスする契約社員のサブスクリプション ライセンス (SL) を購買する必要があります。 Finance and Operations は、Microsoft ボリューム ライセンスおよび Microsoft クラウド ソリューション プロバイダー (CSP) プログラムを通じてライセンスされています。 詳細については、最新の [Dynamics 365 の価格設定からの Microsoft Dynamics 365 ライセンス ガイド](https://dynamics.microsoft.com/pricing/)をダウンロードしてください。
- **テナント** – Microsoft Azure Active Directory (AAD) で、テナントは組織を表示します。 Microsoft との関係を作成するとき (たとえば、Azure、Microsoft Intune または Microsoft Office 365 など Microsoft クラウド サービスにサインアップすることにより)、組織が受け取り所有する AAD サービスの専用インスタンスです。 すべての AAD テナントは特徴的で、他の AAD テナントとは区別されます。 AAD テナントの詳細については、[Azure Active Directory テナントを取得する方法](https://docs.microsoft.com//azure/active-directory/develop/active-directory-howto-tenant)を参照してください。

    テナントには、会社のユーザー情報が格納されています。 この情報には、パスワード、ユーザー プロファイル データ、アクセス許可、および関連情報が含まれます。 テナントには、組織やそのセキュリティに関するグループ、アプリケーション、およびその他の情報も含まれています。

    顧客が、Office 365、Microsoft Dynamics 365、Azure などの Microsoft Online Service に、最初のサブスクリプションのサインアップをした際にテナントが作成されます。 同じオンライン サービスまたは他のオンライン サービスのすべての後のサブスクリプションを同じテナント内でグループ化することができます。

    組織では、複数の AAD テナントを持つことができます。 複数のテナントがある場合は、Finance and Operations のサブスクリプションが正しいテナントに関連付けられていることを確認してください。

- **Azure Active Directory (AAD)** – AAD は、マルチ テナントで Microsoft のコア ディレクトリ サービス、アプリケーション アクセス管理、および単一ソリューションの ID 保護を組み合わせたクラウドベース ディレクトリと管理サービス ID です。 詳細については、「[Azure Active Directory](https://docs.microsoft.com/azure/active-directory/)」を参照してください。 Finance and Operations は、店舗の ID として AAD を使用します。 AAD へのアクセスは、Finance and Operations へのサブスクリプションの一部として提供されます。
- **Office 365 管理者センター** – Office 365 管理者センターは、Office 365 が管理者に提供する定期売買管理ポータルです。 ユーザー (AAD) および定期売買の管理機能を提供するのに使用されます。 これらの管理機能の一部として、サービスの正常性に関する情報を提供します。 詳細については、[Office 365 管理センターについて](https://support.office.com/article/about-the-office-365-admin-center-758befc4-0888-4009-9f14-0d147402fd23)を参照してください。

    > [!NOTE]
    > Finance and Operations を配置するために Office 365 ライセンスを取得する必要はありません。 ただし、特定の Office 統合シナリオのライセンスが必要な場合があります。 詳細については、[Office 統合](../../dev-itpro/office-integration/office-integration.md)を参照してください。

- **Microsoft Dynamics Lifecycle Services (LCS)** - LCS は、Finance and Operations 実装のアプリケーション ライフサイクルの管理に役立つ環境と定期的に更新される一連のサービスを提供するコラボレーション ポータルです。 詳細については、[Lifecycle Services for Finance and Operations](../../dev-itpro/lifecycle-services/lcs.md) を参照してください。 Finance and Operations を購入してサブスクリプションを有効化した後、**実装プロジェクト**ワークスペースでテナント管理者が初めてサインインすると、LCS にプロビジョニングされます。

    > [!NOTE]
    > 実装プロジェクトは、Microsoft-managed Finance and Operations クラウド サービスの LCS プロジェクトです。 Microsoft パートナーとして、目的に合わせて非実装 LCS プロジェクトを準備することもできます。 詳細については、[Lifecycle Services for Finance and Operations のパートナー](../../dev-itpro/lifecycle-services/getting-started-lcs.md)を参照してください。

- **Finance and Operations** – Finance and Operations は、LCS を通じて展開されます。 開発/テスト/ビルド、受入れテスト、パフォーマンス テスト、高可用性生産など、さまざまなトポロジが利用できます。 さまざまなトポロジの詳細については、 [Dynamics 365 の価格設定からの最新の Microsoft Dynamics 365 ライセンス ガイド](https://dynamics.microsoft.com/pricing/)をダウンロードしてください。
- **Microsoft Azure DevOps** – Azure DevOps は、主にコードのバージョン管理に使用され、ビルド環境を配置します。 Azure DevOps は、クラウドを利用したサポートを通じて Microsoft に送信される Azure DevOps の作業項目などのサポート インシデントの追跡や、ビジネス プロセス モデラー (BPM) ライブラリ階層を作業項目の階層として Azure DevOps プロジェクトに統合するのにも使用されます。 Azure DevOps はコードのアップグレード時にも使用されます。

Finance and Operations では、Azure ストレージ、ネットワーク、監視、Azure SQL データベースなど、Azure プラットフォームの多くの機能を使用しています。 共有サービスが工程に移り、参加者の環境のアプリケーション ライフサイクルが調整されます。 Azure の機能と LCS があいまって、堅牢なクラウド サービスを提供します。

> [!NOTE]
> Azure プラットフォームのさまざまな機能を使用しても、Microsoft の管理されたクラウドで Finance and Operations を配置する Azure サブスクリプションは必要ありません。 Azure サブスクリプションには、 Finance and Operations のクラウド ホスト環境を自分の Azure サブスクリプションに導入する場合にのみ、Azure サブスクリプションが必要です。
