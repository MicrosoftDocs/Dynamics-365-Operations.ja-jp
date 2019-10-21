---
title: Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 27 (2019 年 6 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 27 (2019 年 6 月) でプレビューされる機能について説明します。
author: tonyafehr
manager: AnnBe
ms.date: 04/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2019-06-30
ms.dyn365.ops.version: Platform 27
ms.openlocfilehash: 096a46ae1a0d9380d876c43179702eb9e03f7d6f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180491"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-platform-update-27-june-2019"></a>Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 27 (2019 年 6 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 27 の新機能または変更された機能について説明します。 このバージョンのビルド番号は 7.0.5286 です。 プラットフォーム更新プログラム 27 の詳細については [追加リソース](whats-new-platform-update-27.md#additional-resources) を参照してください。

## <a name="feature-management"></a>機能管理
**機能管理** エクスペリエンスは、各リリースで提供されている機能を表示、有効化、無効化、およびスケジュールできるワークスペースを提供します。 既定では、新機能が無効になっています。 ワークスペースを使用してそれらを有効にし、それらのドキュメントを参照できます。 

機能管理の詳細については [機能管理の概要](feature-management/feature-management-overview.md) を参照してください。

## <a name="dedicated-capacity-to-process-business-events"></a>ビジネス イベントを処理する専用キャパシティ 
ビジネス イベント処理バッチ ジョブをスケジュールして、ビジネス イベントを処理する必要はもうなくなります。 専用スレッドがシステムによってビジネス イベントを処理するために割り当てられ、これによりビジネス イベントの処理が高速化します。 既存のバッチ ジョブをまだ使用できます (ただし、専用キャパシティに問題がある場合を除き、実行する必要はありません)。 このプラットフォーム更新の前にバッチ ジョブが既にスケジュールされていた場合は、バッチが無効になり、更新後に専用スレッドに引き継がれます。

詳細については[ビジネス イベント](../../dev-itpro/business-events/home-page.md)を参照してください。

## <a name="cancel-a-running-batch-job"></a>実行中のバッチ ジョブをキャンセルします。
ジョブに現在実行中のタスクが含まれている場合、バッチ ジョブのキャンセルに長い時間がかかることがあります。 中止オプションを使用すると、システム管理者やバッチ ジョブ マネージャーは、ジョブがキャンセルされた場合にジョブに対してすでに実行中のタスクをキャンセルすることができます。 これは他の場所でシステムの使用に影響を与える可能性がある長時間実行中のジョブをキャンセルする、はるかに高速なメカニズムを提供します。 詳細については [実行中のバッチ ジョブの中止](../../dev-itpro/sysadmin/batch-abort.md) を参照してください。

## <a name="extensibility-enhancements"></a>拡張性の強化
プラットフォーム更新プログラム 27 に含まれる [プラットフォーム拡張機能の 4 番目の波](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-finance-operations/platform-extensibility4) は、2019 年 4 月リリース ノートにドキュメントされています。 2 つの機能強化の詳細が記載されており、そのハイライトは表示拡張がラベルとヘルプ テキストの値を変更できるようになったことです。

## <a name="additional-resources"></a>追加リソース

### <a name="platform-update-27-bug-fixes"></a>プラットフォーム アップデート 27 のバグ修正プログラム
プラットフォーム更新 27 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、この [KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=320391&dbType=3&qc=d5539716f56ccea45e2187c269570772af20e1f10a78371811220da6315a3c34)を参照してください。

### <a name="dynamics-365-april-19-release-notes"></a>Dynamics 365 2019 年 4 月 リリース ノート
当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[2019 年 4 月リリース ノートをご覧ください](https://docs.microsoft.com/business-applications-release-notes/April19/index)。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能
[削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックは Dynamics 365 for Finance and Operations の削除済みまたは非推奨の機能について説明します。

- *削除された*機能は製品では使用できません。
- *削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。
