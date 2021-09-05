---
title: Dynamics 365 Human Resources (2021 年 8 月 9 日) の新機能または変更された機能
description: このトピックでは、2021 年 8 月 9 日に更新された、Microsoft Dynamics 365 Human Resources の新機能または変更された機能について説明します。
author: marcelbf
ms.date: 08/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-08-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0f515b614aedce3d58994bf21104ada25702a71e
ms.sourcegitcommit: fc19ee0aba2a6174fef305d151f1eb23ca6c0346
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2021
ms.locfileid: "7385703"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-9-2021"></a>Dynamics 365 Human Resources (2021 年 8 月 9 日) の新機能または変更された機能

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Microsoft Dynamics 365 Human Resources の新機能、変更された機能または間もなく公開される機能について説明します。

更新プロセスとスケジュールの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

新機能と予想される一般提供日の詳細については、[Dynamics 365 Human Resources 2021 リリース ウェーブ 2 の概要](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="in-this-release"></a>今回のリリース

今回のリリースには、次の新機能とバグ修正が含まれています。 変更は、ビルド番号 8.1.4393 に適用されます。

### <a name="bug-fixes"></a>バグ修正

このリリースには、次のバグ修正が含まれています。

> [!NOTE]
> 私たちの目標は、この情報をできるだけ早くお客様にお届けすることです。 このトピックが最初に公開された後に、ビルドに加えたバグ修正を含めるために、このトピックを更新する可能性があります:

| 問題の番号 | 問題 | 説明 |
| --- | --- | --- |
| 558385 | 既定の被指名人に対して **被指名人の自動選択** オプションが有効になっている場合は、既定の被指名人は選択されません。 | この問題は修正されました。 **被指名人の自動選択** オプションが **Human Resources の共有パラメーター** ページで有効の場合は、複数の既定の被指名人が適用できるプランで自動選択されます。 |
| 589617 | 特定の会社にアクセスが制限されている場合、**休暇** ページでは、**購入可能** と **販売可能** の残高が空白になります。 | この問題は修正されました。 特定の会社にユーザーが制限されている場合、**休暇** ページでは、正しい **購入可能** と **販売可能** の残高が表示されます。 |

## <a name="in-preview"></a>プレビュー

次の新機能はプレビュー中です。 機能をオン/オフにする方法の詳細については、[機能の管理](hr-admin-manage-features.md) を参照してください。

| フィーチャー | リリース計画 | ドキュメント |
| --- | --- | --- |
| 給付金管理ワークスペース | [給付金管理ワークスペース (プレビュー)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [給付金管理ワークスペース](hr-benefits-management-workspace.md) |
| 簡素化された給与統合 (給与統合 API) を有効にする | [簡素化された給与プロバイダーとの統合を有効にする](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [給与統合 API](hr-admin-integration-payroll-api-introduction.md)|
| 休暇マネージャの休暇管理の有効化 | [休暇マネージャの休暇管理の有効化](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | このリリースでは、休暇マネージャーのワークスペース ビューを更新しています。 詳細については、[休暇マネージャー ロールのコンフィギュレーション](https://go.microsoft.com/fwlink/?linkid=2168107)を参照してください。 |
| 休暇タイプごとに添付ファイル要件を構成する | [休暇タイプごとに添付ファイル要件を構成する](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[休暇および欠勤タイプのコンフィギュレーション](https://go.microsoft.com/fwlink/?linkid=2168108)|
| 休暇タイプごとに休暇単位を構成する | [休暇タイプごとに休暇単位を構成する](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[休暇および欠勤タイプのコンフィギュレーション](https://go.microsoft.com/fwlink/?linkid=2168215)|
| 従業員の支払準備完了のマークの有効化 | [従業員の支払準備完了のマークの有効化](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [支払準備完了](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>間もなく公開

予定されている機能とリリースの完全な一覧については、[Dynamics 365 Human Resources 2021 のリリース ウェーブ 2 の概要](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) を参照してください。

| フィーチャー | 細目 |
| --- | --- |
| プラットフォーム 更新プログラム 10.0.21 (45) | プラットフォーム更新プログラム 10.0.21 のロールアウトは、2021 年 10 月 4 日のサービス リリースで開始する予定です。 詳細については、[Finance and Operations アプリのバージョン 10.0.21 のプラットフォーム更新プログラム (2021 年 10 月)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21) を参照してください。 |

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 のリリース ウェーブ 2 の概要](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
