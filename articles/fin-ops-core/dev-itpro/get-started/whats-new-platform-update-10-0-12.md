---
title: Finance and Operations アプリ バージョン 10.0.12 のプラットフォーム更新プログラム（2020 年 8 月）
description: このトピックでは、Finance and Operations アプリ バージョン 10.0.12 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。
author: sericks007
ms.date: 07/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-05-31
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 55343ad454462c60e0d0e2a706f973714e9e0712
ms.sourcegitcommit: 2f766e5bb8574d250f19180ff2e101e895097713
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923526"
---
# <a name="platform-updates-for-version-10012-of-finance-and-operations-apps-august-2020"></a>Finance and Operations アプリ バージョン 10.0.12 のプラットフォーム更新プログラム（2020 年 8 月）

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Finance and Operations アプリ バージョン 10.0.12 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。 (この更新プログラムは、*プラットフォーム更新プログラム 36* と呼ばれていました)。このバージョンには、ビルド番号 7.0.5688 が付与されており、次のスケジュールで利用できます:

- **プレビュー リリース :** 2020 年 5 月
- **一般提供 (自己更新) :**  2020 年 7 月
- **自動更新:** 2020 年 8 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

-  [パーソナル化ツールバーを使用してフィールドを必須として指定する](/dynamics365-release-plan/2020wave1/finance-operations-crossapp-capabilities/usability-improvements-filtering-personalization) – 詳細については、[ユーザー エクスペリエンスのカスタマイズ](../../fin-ops/get-started/personalize-user-experience.md) を参照してください。 
-  [タスク記録の基本制御値の編集](/dynamics365-release-plan/2020wave1/finance-operations-crossapp-capabilities/new-task-recorder-capabilities-rsat) – 詳細については、[タスク レコーダー リソース](../user-interface/task-recorder.md)を参照してください。
-  [ファイルと添付ファイルでの悪意のあるコードのスキャン](/dynamics365-release-plan/2020wave1/finance-operations-crossapp-capabilities/scanning-files-attachments-malicious-code) – 詳細については、[ファイル アップロード コントロール](../user-interface/file-upload-control.md)および[ドキュメント管理のコンフィギュレーション](../../fin-ops/organization-administration/configure-document-management.md)を参照してください。
-  [関連するドキュメントの添付ファイルの表示](/dynamics365-release-plan/2020wave1/finance-operations-crossapp-capabilities/show-related-document-attachments) – 詳細については、[ドキュメント管理の構成](../../fin-ops/organization-administration/configure-document-management.md)を参照してください。
- [仮想エンティティとしての Dataverse の Finance and Operations エンティティ](/dynamics365-release-plan/2020wave1/finance-operations-crossapp-capabilities/finance-operations-entities-common-data-service-as-virtual-entities) – 詳細については、[Finance and Operations との Microsoft Power Platform 統合](../power-platform/overview.md)を参照してください。
- 顧客および仕入先のマスター データは、機能管理を使用して有効にすることができます。詳細については、[顧客および仕入先のマスター データ共有](../sysadmin/cross-company-data-sharing.md#customer-and-vendor-master-data-sharing)を参照してください。
- [Finance and Operations のライセンス](/dynamics365-release-plan/2020wave1/finance-operations-crossapp-capabilities/finance-operations-licensing) – Dynamics 365 Finance、Dynamics 365 Supply Chain Management、Dynamics 365 Commerce などの製品名がナビゲーション バーに表示され、現在のユーザーに関連付けられている基本ライセンスが反映されます。

## <a name="additional-resources"></a>追加リソース

### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics の Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=453382&dbType=3&qc=a68cf77635c0ab926e7b1b75c6925c82a23058c524c4d728ba8b30fedaf41746) を参照してください。

### <a name="dynamics-365-2020-release-wave-1-plan"></a>Dynamics 365: 2020 リリースのウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2020 リリース ウェーブ 1 プラン](/dynamics365-release-plan/2020wave1/index) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-platform-features"></a>削除済みおよび非推奨のプラットフォーム機能

[削除済みまたは非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) のトピックでは、削除された機能、または Finance and Operations アプリのプラットフォーム更新プログラムで削除予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *非推奨* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能を削除する 12 か月前に、[削除または非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) のトピックに廃止通知が追加されます。

互換性を破る変更で、それがコンパイル時間にのみ影響を与えるが、サンドボックスと運用環境に対するバイナリ互換である場合、廃止期間は 12 ヶ月未満になります。 通常、これらの変更は、コンパイラに対して行う必要がある機能更新です。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]