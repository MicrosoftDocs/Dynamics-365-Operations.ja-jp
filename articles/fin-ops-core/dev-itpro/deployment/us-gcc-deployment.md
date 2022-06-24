---
title: US Government Community Cloud (GCC) の Dynamics 365 Finance、Supply Chain Management、Commerce
description: この記事では、資格のある政府機関や民間企業が利用できる Microsoft Dynamics 365 US Government 製品についての情報を提供します。
author: hasaid
ms.date: 11/12/2021
ms.topic: article
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2021-11-09
ms.openlocfilehash: 90e64fec512307af209ace128d5897475de7aee5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867276"
---
# <a name="dynamics-365-finance-supply-chain-management-and-commerce-in-us-government-community-cloud-gcc"></a>US Government Community Cloud (GCC) の Dynamics 365 Finance、Supply Chain Management、Commerce

[!include [banner](../includes/banner.md)]



Microsoft Dynamics 365 米国 (US) 政府機関製品は、資格のある政府機関や民間企業が利用できます。 それらのエンティティは、以下の種類に限られます:

- 米国の連邦、州、地方、部族、領土の政府機関
- Dynamics 365 US Government を使用して、政府機関またはクラウド コミュニティの適格なメンバーにソリューションを提供する民間企業
- 政府の規制対象となる顧客データを持つ民間企業で、Dynamics 365 US Government は規制要件を満たす適切なサービスです

詳細については、 [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government) を参照してください。

## <a name="onboarding"></a>オンボーディング

Microsoft Dynamics Lifecycle Services (LCS) の実装プロジェクトの初期オンボーディングを完了するには、[実装プロジェクトのオンボーディング](../../../fin-ops-core/fin-ops/imp-lifecycle/onboard.md)に記載の手順に従ってください。 ただし、この説明に記載されている公開 LCS へのリンクは使用しないでください。 代わりに、次の URL を使用して、US Government Community Cloud (GCC) の LCS を開きます: <https://gov.lcs.microsoftdynamics.us>。

最初のオンボーディングが完了した後、[プロジェクトのオンボーディング](../lifecycle-services/project-onboarding.md)に記載のの指示に従ってください。 もう一度、パブリック LCSではなく、[GCC 用 の LCS](https://gov.lcs.microsoftdynamics.us) を使用してください。

## <a name="environment-deployment"></a>環境配置

プロジェクトのオンボーディングの完了後は、[財務と運用アプリの顧客向け Lifecycle Services (LCS)](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md) に記載されている LCS の追加機能を確認することができます。 続いて環境の展開に移ります。

- LCS を使用してマイクロソフトが管理する環境を展開するには、[財務と運用アプリの顧客用 Lifecycle Services (LCS)](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md#new-deployment-experience) に記載の手順に従ってください。
- クラウド ホスト環境については、[開発環境の導入とアクセス](../../../fin-ops-core/dev-itpro/dev-tools/access-instances.md) を参照してください。 また、[米国政府の Lifecycle Services プロジェクトに対する Azure Resource Manager のオンボーディングプロセスの完了](arm-onbarding-us-goverment.md)に記載されているように、ご利用コネクタに対する Resource Manager のオンボーディングプロセスを完了する必要があります。

> [!NOTE]
> 米国政府機関向け LCS プロジェクトでは、政府機関用の Azure サブスクリプションのみがサポートされます。

## <a name="features-that-arent-available"></a>利用できない機能

一部の機能は GCC では展開できないか、あるいは GCC で Dynamics 365 を使用することはできません。 たとえば、GCC では Azure DevOps サービスは利用できません。 ただし、オンプレミスの Azure DevOps やパブリックの Azure DevOps のサービスを利用できます。 機能の提供についての詳細は、[Business Applications の米国政府機関向けの機能](https://aka.ms/BAPFunctionalParity)を参照してください。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="are-dynamics-365-finance-and-dynamics-365-supply-chain-management-supported-in-gcc-high"></a>Dynamics 365 Finance と Dynamics 365 Supply Chain Management は GCC-High に対応していますか。

いいえ。 Dynamics 365 Finance と Dynamics 365 Supply Chain Management は GCC にのみ対応しています。

### <a name="can-i-use-public-azure-devops-with-finance-and-supply-chain-management-in-gcc"></a>GCC で Finance と Supply Chain Management で公共の Azure DevOps を使うことはできますか？

はい、FEDRAMP (Federal Risk and Authorization Management Program) で認証されたソリューションの要件を満たしていない場合は、公共の Azure DevOps サービスを利用することができます。 代わりに、Azure DevOps サーバーを使用できます。

### <a name="can-i-deploy-a-cloud-hosted-environment-tier-1-development-environment-on-an-azure-commercial-subscription"></a>Azure Commercial のサブスクリプションにクラウド　ホスティング環境の Tier-1 開発環境を導入できますか？

いいえ。 [GCC 用 LCS](https://gov.lcs.microsoftdynamics.us)では、Azure Government のサブスクリプションを使用して、クラウド ホスティング環境を展開する必要があります。

### <a name="what-can-i-do-if-i-need-a-package-from-the-shared-asset-library-but-it-isnt-available-in-lcs-for-gcc"></a>共用資産ライブラリのパッケージが必要な状況であっても、GCC 用 LCS では利用できない場合はどうすればいいですか？

同じパッケージを [公共 LCS](https://lcs.dynamics.com) の共用資産ライブラリからダウンロードすることができます。 または、パートナーがパッケージのダウンロードをお手伝いします。

### <a name="is-the-code-upgrade-tool-available-in-gcc"></a>GCC にコードのアップグレード ツールはありますか？

いいえ、コードのアップグレード ツールは、現在 GCC では利用できません。 ただし、[公共 LCS](https://lcs.dynamics.com) でプロスペクト プロジェクトを作成し、コードのアップグレード ツールを使用できます。 なお、プロスペクト プロジェクトでは環境を展開することはできません。

### <a name="can-my-partner-open-a-support-ticket-on-my-behalf"></a>パートナーが自分に代わってサポート チケットを開くことはできますか？

はい。 ただし、パートナーが GCC 以外の ID を使用している場合は、サポート チケットは公開サポート キューに送られます。 サポートチケットの発行には、LCS の顧客 GCC エンタイトルメントを使用することをお勧めします。

## <a name="see-also"></a>参照

- [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government)
- [Business Applications 米国政府 機能一覧](https://aka.ms/BAPFunctionalParity)。
- [Lifecycle Services (LCS) ユーザー ガイド](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [クラウド配置の概要](../../../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
