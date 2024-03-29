---
title: Dynamics 365 財務と運用、Enterprise edition 7.2 およびプラットフォーム更新プログラム 12 (2018 年 3 月) のオンプレミスの展開での新機能および変更された機能
description: この記事では、プラットフォーム更新プログラム 12 による Microsoft Dynamics 365 財務と運用、Enterprise Edition 7.2 のオンプレミスの展開での新機能または変更された機能について説明します。 この展開オプションは、2018 年 3 月に使用できるようになりました。
author: sericks007
ms.date: 03/14/2018
ms.topic: article
ms.prod: dynamics-365
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2017-11-30
ms.dyn365.ops.version: Platform update 12
ms.custom: ''
ms.service: ''
ms.openlocfilehash: e19683676e0f0d54855f3376a62c9cac2241ef9b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292320"
---
# <a name="whats-new-or-changed-in-on-premises-deployments-of-dynamics-365-finance-and-operations-enterprise-edition-72-with-platform-update-12-march-2018"></a>Dynamics 365 財務と運用、Enterprise edition 7.2 およびプラットフォーム更新プログラム 12 (2018 年 3 月) のオンプレミスの展開での新機能および変更された機能

[!include [banner](../includes/banner.md)]

この記事では、プラットフォーム更新プログラム 12 による Microsoft Dynamics 365 財務と運用、Enterprise Edition 7.2 のオンプレミスの展開での新機能または変更された機能について説明します。 この展開オプションは、2018 年 3 月に使用できるようになりました。

プラットフォーム更新プログラム 12 の詳細については、[Dynamics 365 財務と運用、Enterprise edition プラットフォーム更新プログラム 12 の新機能または変更された機能について (2017 年 11 月)](whats-new-platform-update-12.md) を参照してください。

オンプレミス配置のリソースについては、[オンプレミス配置のホーム ページ](../../dev-itpro/deployment/on-premises-deployment-landing-page.md) を参照してください。

## <a name="setup-and-deployment"></a>設定と配置

セットアップおよび配置プロセスが強化されました。 これらの改良により、展開に必要な時間が大幅に短縮されます。 信頼性を向上させるために、自動処理の強化および複数の前提条件の検証も追加されました。 詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../../dev-itpro/deployment/setup-deploy-on-premises-pu12.md) を参照してください。

## <a name="servicing"></a>サービス

オンプレミス環境が配置されると、Microsoft Dynamics Lifecycle Services (LCS) を使用して Microsoft からリリースされたプラットフォームおよびアプリケーションの更新プログラムを適用できます。 また、コードのカスタマイズを適用することもできます。 したがって、顧客は最新の修正プログラムを最新の状態に保ち、既存の環境を再構成したり、オンプレミス環境を再配置することなく、新しいカスタマイズを行うことができます。 また、パッケージが正常に適用されなかった場合に、コード変更をロール バックできるようになりました。 詳細については、[オンプレミス配置への更新プログラムの適用](../../dev-itpro/deployment/apply-updates-on-premises.md)を参照してください。

[新しいプラットフォームまたはトポロジを使用するために環境を再構成](../../dev-itpro/lifecycle-services/reconfigure-environment.md)は、プラットフォーム更新プログラム 12 以前のバージョンで配置された環境でも使用可能であることに注意してください。

## <a name="hotfixes"></a>修正プログラム

LCS からダウンロードできる修正プログラムは、プラットフォーム更新プログラム 12 のオンプレミス配置に関する追加の機能を提供します。 次の修正プログラムを適用する必要があります。

- **[KB 4091763 - 管理者がクライアントの接続と Skype プレゼンスを切り替える](https://fix.lcs.dynamics.com/Issue/Details?kb=4091763&bugId=3934773&qc=fd949f8a204ceeedaa0a586ca8a1bfdbd6535b35225da98506d688e093d086f6):** この修正プログラムにより、管理者はクライアント マシンのインターネット接続に依存するエクスペリエンスを無効にできます。 詳細については、[クライアント インターネット接続](../../dev-itpro/user-interface/client-disconnected.md)を参照してください。
- **[KB 4093454 - オンプレミスの ISV ライセンス サポート](https://fix.lcs.dynamics.com/Issue/Details?kb=4093454&bugId=3936799&qc=766427475435463a174e287b531401ab8cc8f1aeedf12bf2c2d4f8d1a1774592):** プラットフォーム更新プログラム 12 から開始するオンプレミス環境を配置する場合、テナント GUID は LCS からオンプレミス環境に自動的に入力されます。 ライセンス供与の検証では次の値を読み取り、正常にライセンスを検証できます。 詳細については、[独立系ソフトウェア ベンダー (ISV) ライセンス (オンプレミス)](../../dev-itpro/dev-tools/isv-licensing-on-prem.md)を参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

