---
title: Finance and Operations アプリ バージョン 10.0.15 のプラットフォーム更新プログラム (2021 年 1 月)
description: このトピックでは、Finance and Operations アプリ バージョン 10.0.15 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。
author: sericks007
ms.date: 12/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f41cbcd71456c124a9b294f1533a34fcd830327b7e568bc2b5914815246b080c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730559"
---
# <a name="platform-updates-for-version-10015-of-finance-and-operations-apps-january-2021"></a>Finance and Operations アプリ バージョン 10.0.15 のプラットフォーム更新プログラム (2021 年 1 月)

[!include [banner](../includes/banner.md)]

このトピックでは、Finance and Operations アプリ バージョン 10.0.15 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。 このバージョンのビルド番号は 7.0.5816 で、次のスケジュールで使用できます。

- **プレビュー リリース:** 2020 年 10 月
- **一般提供 (自己更新):** 2020 年 11 月
- **自動更新:** 2021 年 1 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

-  資産の配置の Azure Pipelines タスクは、セルフサービス環境をサポートする<br>- このサポートを有効にする方法の詳細については、「[Azure Pipelines を使用した資産の配置](../dev-tools/pipeline-deploy-asset.md)」を参照してください。
- セキュリティを構成したり、ユーザーにロールを割り当てたりする際に、特定のユーザー フル ライセンス情報が使用できるようになりました。<br>- 詳細については、「[ユーザー ライセンス要件への準拠の維持](../sysadmin/stay-compliant-user-license-requirement.md)」を参照してください。
- Regression Suite Automation Tool (RSAT) 2.0<br>- RSAT ユーザーの場合、バージョン 10.0.15 では既知の問題に対処するために最新バージョンの RSAT が必要です。 RSAT 2.0.7031.98 以降は、2020 年 10 月 12 日の月曜日に https://www.microsoft.com/en-us/download/details.aspx?id=57357 からダウンロードできるようになります。

## <a name="additional-resources"></a>追加リソース

### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics の Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=514518&dbType=3&qc=8fbe12733a7e1aa197e91fb11530f69fa89b9b39c08d89a19873f755c9430988) を参照してください。

### <a name="dynamics-365-2020-release-wave-2-plan"></a>Dynamics 365: 2020 リリースのウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2020 リリース ウェーブ 2 プラン](/dynamics365-release-plan/2020wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-platform-features"></a>削除済みおよび非推奨のプラットフォーム機能

[削除済みまたは非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) のトピックでは、削除された機能、または Finance and Operations アプリのプラットフォーム更新プログラムで削除予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *非推奨* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能を削除する 12 か月前に、[削除または非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) のトピックに廃止通知が追加されます。

互換性を破る変更で、それがコンパイル時間にのみ影響を与えるが、サンドボックスと運用環境に対するバイナリ互換である場合、廃止期間は 12 ヶ月未満になります。 通常、これらの変更は、コンパイラに対して行う必要がある機能更新です。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]