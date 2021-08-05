---
title: Finance and Operations アプリケーション アーキテクチャ
description: このトピックでは、Finance and Operations アプリケーションのアーキテクチャの概要を説明します。
author: ClaudiaBetz-Haubold
ms.date: 04/24/2020
ms.topic: article
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
ms.openlocfilehash: ab6b73df11d43f1e6abbdad2c4832dbfdc98c410
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348569"
---
# <a name="finance-and-operations-application-architecture"></a>Finance and Operations アプリケーション アーキテクチャ

[!include [banner](../includes/banner.md)]

Finance and Operations アプリケーション クラウド アーキテクチャには、[Microsoft クラウド製品のサブスクリプション、ライセンス、アカウント、テナント](/office365/enterprise/subscriptions-licenses-accounts-and-tenants-for-microsoft-cloud-offerings) で説明されているように、すべての Microsoft クラウド製品に共通する全ての要素が含まれています。 さらに、ソフトウェアの展開とプロビジョニング、運用の監視とレポート、およびシームレスなアプリケーション ライフサイクル管理を自動化するサービスが含まれます。

![クラウド アーキテクチャ。](./media/cloud-architecture.png)

クラウド アーキテクチャは、これらの概念領域で構成されています。

- **サブスクリプション** – Finance and Operations アプリに対するサブスクリプションは、オンライン クラウド環境 (または複数の環境) とエクスペリエンスを提供します。
- **ライセンス** – お客様は、組織、または関連会社の従業員、オンサイト エージェント、仕入先、または Finance and Operations アプリに直接または間接的にアクセスする契約社員のためにサブスクリプション ライセンス (SL) を購買する必要があります。 これらのアプリは、Microsoft ボリューム ライセンスおよび Microsoft クラウド ソリューション プロバイダー (CSP) プログラムを通じてライセンスされています。 詳細については、最新の [Dynamics 365 の価格設定からの Microsoft Dynamics 365 ライセンス ガイド](https://dynamics.microsoft.com/pricing/)をダウンロードしてください。
- **テナント** – Microsoft Azure Active Directory (AAD) で、テナントは組織を表示します。 Microsoft との関係を作成するとき (たとえば、Azure、Microsoft Intune または Microsoft 365 などの Microsoft Cloud Service にサインアップすることにより)、組織が受け取り所有する AAD サービスの専用インスタンスです。 すべての AAD テナントは特徴的で、他の AAD テナントとは区別されます。 AAD テナントの詳細については、[Azure Active Directory テナントを取得する方法](/azure/active-directory/develop/active-directory-howto-tenant)を参照してください。

    テナントには、会社のユーザー情報が格納されています。 この情報には、パスワード、ユーザー プロファイル データ、アクセス許可、および関連情報が含まれます。 テナントには、組織やそのセキュリティに関するグループ、アプリケーション、およびその他の情報も含まれています。

    お客様が、Microsoft 365、Microsoft Dynamics 365、Azure などの Microsoft Online Service に、最初のサブスクリプションのサインアップをした際にテナントが作成されます。 同じオンライン サービスまたは他のオンライン サービスのすべての後のサブスクリプションを同じテナント内でグループ化することができます。

    組織では、複数の AAD テナントを持つことができます。 複数のテナントがある場合は、Finance and Operations アプリのサブスクリプションが正しいテナントに関連付けられていることを確認してください。

- **Azure Active Directory (AAD)** – AAD は、マルチ テナントで Microsoft のコア ディレクトリ サービス、アプリケーション アクセス管理、および単一ソリューションの ID 保護を組み合わせたクラウドベース ディレクトリと管理サービス ID です。 詳細については、[Azure Active Directory](/azure/active-directory/) を参照してください。 Finance and Operations アプリは、ID のストアとして AAD を使用します。 AAD へのアクセスは、Finance and Operations アプリへのサブスクリプションの一部として提供されます。
- **Microsoft 365 管理センター** – Microsoft 365 管理センターは、Microsoft 365 が管理者に提供するサブスクリプション管理ポータルです。 ユーザー (AAD) および定期売買の管理機能を提供するのに使用されます。 これらの管理機能の一部として、サービスの正常性に関する情報を提供します。 詳細については、[Microsoft 365 管理センターについて](https://support.office.com/article/about-the-office-365-admin-center-758befc4-0888-4009-9f14-0d147402fd23) を参照してください。

    > [!NOTE]
    > Finance and Operations アプリを配置するために Microsoft 365 ライセンスを取得する必要はありません。 ただし、特定の Office 統合シナリオのライセンスが必要な場合があります。 詳細については、 [Office 統合の概要](../../dev-itpro/office-integration/office-integration.md)を参照してください。

- **Microsoft Dynamics Lifecycle Services (LCS)** - LCS は、実装のアプリケーション ライフサイクルの管理に役立つ環境と定期的に更新される一連のサービスを提供するコラボレーション ポータルです。 詳細については、 [Lifecycle Services のリソース](../../dev-itpro/lifecycle-services/lcs.md) を参照してください。 Finance and Operations アプリのサブスクリプションを購入して有効化すると、**実装プロジェクト** ワークスペースが、テナント管理者が初めてサインインしたときに、LCS でプロビジョニングされます。

    > [!NOTE]
    > 実装プロジェクトは、クラウド サービスの LCS プロジェクトです。 Microsoft パートナーとして、目的に合わせて非実装 LCS プロジェクトを準備することもできます。 詳細については、[Finance and Operations アプリ パートナー向け Lifecycle Services (LCS)](../../dev-itpro/lifecycle-services/getting-started-lcs.md) を参照してください。

- **Finance and Operations アプリ** – Finance and Operations アプリは LCS を介して展開されます。 開発/テスト/ビルド、受入れテスト、パフォーマンス テスト、高可用性生産など、さまざまなトポロジが利用できます。 さまざまなトポロジの詳細については、 [Dynamics 365 の価格設定からの最新の Microsoft Dynamics 365 ライセンス ガイド](https://dynamics.microsoft.com/pricing/)をダウンロードしてください。
- **Microsoft Azure DevOps** – Azure DevOps は、主にコードのバージョン管理、開発、ビルド環境を配置に使用されます。 Azure DevOps は、クラウドを利用したサポートを通じて Microsoft に送信される Azure DevOps の作業項目などのサポート インシデントの追跡や、ビジネス プロセス モデラー (BPM) ライブラリ階層を作業項目の階層として Azure DevOps プロジェクトに統合するのにも使用されます。 Azure DevOps はコードのアップグレード時にも使用されます。

"内部," Finance and Operations アプリでは、Azure Storage、ネットワーク、監視、Azure SQL データベースなど、Azure プラットフォームの多くの機能を使用しています。 共有サービスが工程に移り、参加者の環境のアプリケーション ライフサイクルが調整されます。 Azure の機能と LCS があいまって、堅牢なクラウド サービスを提供します。

> [!NOTE]
> Azure プラットフォームの多くの機能が使用されますが、Microsoft の管理されたクラウドに Finance and Operations アプリを配置するために Azure サブスクリプションは必要ありません。 Finance and Operations アプリのクラウド ホスト環境を自分の Azure サブスクリプションに配置する場合にのみ、Azure サブスクリプションが必要です。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
