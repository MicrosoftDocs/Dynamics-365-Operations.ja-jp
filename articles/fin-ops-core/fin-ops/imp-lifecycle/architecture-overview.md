---
title: 財務と運用アプリケーションのアーキテクチャ
description: このトピックでは、財務と運用アプリケーション アーキテクチャの概要を示します。
author: ClaudiaBetz-Haubold
ms.date: 04/24/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.custom:
- "56551"
- intro-internal
ms.assetid: d876e8de-d547-43e5-9259-f095821dc758
ms.search.region: Global
ms.author: chaubold
ms.search.validFrom: 2018-05-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c93538cfa0644c2f4dbef70a25921a7bfd199835
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984419"
---
# <a name="finance-and-operations-application-architecture"></a>財務と運用アプリケーションのアーキテクチャ

[!include [banner](../includes/banner.md)]

財務と運用アプリケーション クラウド アーキテクチャには、[Microsoft のクラウドが提供するサブスクリプション、ライセンス、アカウントおよびテナント](/office365/enterprise/subscriptions-licenses-accounts-and-tenants-for-microsoft-cloud-offerings) に説明されているように、すべての Microsoft クラウドの提供内容に共通する全ての要素が含まれています。 さらに、ソフトウェアの展開とプロビジョニング、運用の監視とレポート、およびシームレスなアプリケーション ライフサイクル管理を自動化するサービスが含まれます。

![クラウド アーキテクチャ。](./media/cloud-architecture.png)

クラウド アーキテクチャは、これらの概念領域で構成されています。

- **サブスクリプション** – 財務と運用アプリに対するサブスクリプションは、オンライン クラウド環境 (または複数の環境) およびエクスペリエンスを提供します。
- **ライセンス** – 顧客は、組織または関連会社の従業員のために、およびオンサイト エージェント、仕入先、直接または間接的に財務と運用アプリにアクセスする契約社員のサブスクリプション ライセンス (SL) を購買する必要があります。 これらのアプリは、Microsoft ボリューム ライセンスおよび Microsoft クラウド ソリューション プロバイダー (CSP) プログラムを通じてライセンスされています。 詳細については、最新の [Dynamics 365 の価格設定からの Microsoft Dynamics 365 ライセンス ガイド](https://dynamics.microsoft.com/pricing/)をダウンロードしてください。
- **テナント** – Microsoft Azure Active Directory (AAD) で、テナントは組織を表示します。 Microsoft との関係を作成するとき (たとえば、Azure、Microsoft Intune または Microsoft 365 など Microsoft クラウド サービスにサインアップすることにより)、組織が受け取り所有する AAD サービスの専用インスタンスです。 すべての AAD テナントは特徴的で、他の AAD テナントとは区別されます。 AAD テナントの詳細については、[Azure Active Directory テナントを取得する方法](/azure/active-directory/develop/active-directory-howto-tenant)を参照してください。

    テナントには、会社のユーザー情報が格納されています。 この情報には、パスワード、ユーザー プロファイル データ、アクセス許可、および関連情報が含まれます。 テナントには、組織やそのセキュリティに関するグループ、アプリケーション、およびその他の情報も含まれています。

    顧客が、Microsoft 365、Microsoft Dynamics 365、Azure などの Microsoft Online Service に、最初のサブスクリプションのサインアップをした際にテナントが作成されます。 同じオンライン サービスまたは他のオンライン サービスのすべての後のサブスクリプションを同じテナント内でグループ化することができます。

    組織では、複数の AAD テナントを持つことができます。 複数のテナントがある場合は、財務と運用アプリのすべてのサブスクリプションが正しいテナントに関連付けられていることを確認してください。

- **Azure Active Directory (AAD)** – AAD は、マルチ テナントで Microsoft のコア ディレクトリ サービス、アプリケーション アクセス管理、および単一ソリューションの ID 保護を組み合わせたクラウドベース ディレクトリと管理サービス ID です。 詳細については、[Azure Active Directory](/azure/active-directory/) を参照してください。 財務と運用アプリは、店舗の ID として AAD を使用します。 AAD へのアクセスは、財務と運用アプリへのサブスクリプションの一部として提供されます。
- **Microsoft 365 管理者センター** – Microsoft 365 管理者センターは、Microsoft 365 が管理者に提供するサブスクリプション管理ポータルです。 ユーザー (AAD) およびサブスクリプションの管理機能を提供するのに使用されます。 これらの管理機能の一部として、サービスの正常性に関する情報を提供します。 詳細については、[Microsoft 365 管理センターについて](https://support.office.com/article/about-the-office-365-admin-center-758befc4-0888-4009-9f14-0d147402fd23)を参照してください。

    > [!NOTE]
    > 財務と運用アプリを配置するために Microsoft 365 ライセンスを取得する必要はありません。 ただし、特定の Office 統合シナリオのライセンスが必要な場合があります。 詳細については、 [Office 統合の概要](../../dev-itpro/office-integration/office-integration.md)を参照してください。

- **Microsoft Dynamics Lifecycle Services (LCS)** - LCS は、実装のアプリケーション ライフサイクルの管理に役立つ環境と定期的に更新される一連のサービスを提供するコラボレーション ポータルです。 詳細については、 [Lifecycle Services のリソース](../../dev-itpro/lifecycle-services/lcs.md) を参照してください。 財務と運用アプリを購入してサブスクリプションを有効化した後、**実装プロジェクト** ワークスペースでテナント管理者が初めてサインインすると、LCS にプロビジョニングされます。

    > [!NOTE]
    > 実装プロジェクトは、クラウド サービスの LCS プロジェクトです。 Microsoft パートナーとして、目的に合わせて非実装 LCS プロジェクトを準備することもできます。 詳細については、 [Lifecycle Services (LCS) for Finance and Operations アプリのパートナー](../../dev-itpro/lifecycle-services/getting-started-lcs.md) を参照してください。

- **財務と運用アプリ** – 財務と運用アプリは、LCS を通じて展開されます。 開発/テスト/ビルド、受入れテスト、パフォーマンス テスト、高可用性生産など、さまざまなトポロジが利用できます。 さまざまなトポロジの詳細については、 [Dynamics 365 の価格設定からの最新の Microsoft Dynamics 365 ライセンス ガイド](https://dynamics.microsoft.com/pricing/)をダウンロードしてください。
- **Microsoft Azure DevOps** – Azure DevOps は、主にコードのバージョン管理、開発、ビルド環境を配置に使用されます。 Azure DevOps は、クラウドを利用したサポートを通じて Microsoft に送信される Azure DevOps の作業項目などのサポート インシデントの追跡や、ビジネス プロセス モデラー (BPM) ライブラリ階層を作業項目の階層として Azure DevOps プロジェクトに統合するのにも使用されます。 Azure DevOps はコードのアップグレード時にも使用されます。

財務と運用アプリでは、Azure ストレージ、ネットワーク、監視、Azure SQL データベースなど、Azure プラットフォームの多くの機能を使用しています。 共有サービスが工程に移り、参加者の環境のアプリケーション ライフサイクルが調整されます。 Azure の機能と LCS があいまって、堅牢なクラウド サービスを提供します。

> [!NOTE]
> Azure プラットフォームのさまざまな機能を使用しても、Microsoft の管理されたクラウドで財務と運用アプリを配置する Azure サブスクリプションは必要ありません。 Azure サブスクリプションには、財務と運用アプリのクラウド ホスト環境を自分の Azure サブスクリプションに導入する場合にのみ、Azure サブスクリプションが必要です。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
