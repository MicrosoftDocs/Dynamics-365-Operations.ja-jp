---
title: Dynamics 365 Human Resources の新機能または変更された機能 (2021 年 7 月 26 日)
description: この記事では、2021 年 7 月 26 日に更新された Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: marcelbf
ms.date: 07/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-26
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6c7211135733f45a9841ae5a80607b01999d7c69
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870932"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-26-2021"></a>Dynamics 365 Human Resources の新機能または変更された機能 (2021 年 7 月 26 日)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、Dynamics 365 Human Resources の新機能、変更された機能または間もなく近日公開される機能について説明します。

更新プロセスとスケジュールの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

新機能と予想される一般提供日の詳細については、[Dynamics 365 Human Resources 2021 リリース ウェーブ 2 の概要](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="in-this-release"></a>今回のリリース

今回のリリースには、次の新機能とバグ修正が含まれています。 変更は、ビルド番号 8.1.4384 に適用されます。

### <a name="new-features"></a>新機能

このリリースでは、次の機能が一般に使用可能です。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| プラットフォーム update 10.0.20 | -- | [財務と運用アプリのバージョン 10.0.20 (2021 年 8 月) のプラットフォーム更新プログラム](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20) |

### <a name="bug-fixes"></a>バグ修正

このリリースには、次のバグ修正が含まれています。

> [!NOTE]
> 私たちの目標は、この情報をできるだけ早くお客様にお届けすることです。 この記事が最初に公開された後に、ビルドに加えたバグ修正を含めるために、この記事を更新する可能性があります。

| 問題の番号 | 問題 |  Description |
| --- | --- | --- |
| 600422 | 支払準備完了の給与住所の検証に失敗しました。 | 検証が更新され、「給与居住の場所」タイプのアドレスが 1 つだけ、「給与作業の場所」タイプのアドレスが 1 つだけ必要になるようになりました。 |
| 601226 | データ統合の問題 : 給与統合エクスポート プロジェクトには、フルプッシュするオプションがありません | Ceridian DayForce への給与統合は、フル プッシュではなく増分プッシュを実行しました。 Ceridian は常に完全に更新する必要があります。 この問題は修正され、データ エクスポート プロジェクトのエンティティは増分プッシュに切り替わりません。 |
| 602272 | 従業員セルフ サービ スワークスペースに追加されたタイルが失われ、タイルを追加できなくなりました | 従業員セルフ サービスの個人用設定の問題が修正されました。 新しいタイルをビューに追加でき、既存のパーソナライズがユーザーに表示されます |
| 600711 | 半日の定義選択フィールドが終日の休暇申請に対して有効になっている | この問題は修正され、従業員が半日の定義を有効にした休暇タイプを選択し、半日を金額として選択した場合にのみ、半日の定義フィールドが有効になります |
| 602208 | 日ではなく時間を表示する発生率の単位 | この問題は修正されました。 **休暇** フォームでは、**見越計上率** 欄に正しい休暇単位 (時間または日数) が表示されます。 |

## <a name="in-preview"></a>プレビュー

次の新機能はプレビュー中です。 機能をオンまたはオフにする方法については、[機能の管理](hr-admin-manage-features.md) を参照してください。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| 給付金管理ワークスペース | [給付金管理ワークスペース (プレビュー)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [給付金管理ワークスペース](hr-benefits-management-workspace.md) |
| 簡素化された給与統合 (給与統合 API) を有効にする | [簡素化された給与プロバイダーとの統合を有効にする](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [給与統合 API](hr-admin-integration-payroll-api-introduction.md)|
|  休暇マネージャの休暇管理の有効化 | [休暇マネージャの休暇管理の有効化](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | このリリースでは、休暇マネージャーのワークスペース ビューを更新しています。 詳細については、[休暇マネージャー ロールのコンフィギュレーション](https://go.microsoft.com/fwlink/?linkid=2168107)を参照してください。|
|  休暇タイプごとに添付ファイル要件を構成する | [休暇タイプごとに添付ファイル要件を構成する](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[休暇および欠勤タイプのコンフィギュレーション](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  休暇タイプごとに休暇単位を構成する | [休暇タイプごとに休暇単位を構成する](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[休暇および欠勤タイプのコンフィギュレーション](https://go.microsoft.com/fwlink/?linkid=2168215)|
| 従業員の支払準備完了のマークの有効化 | [従業員の支払準備完了のマークの有効化](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [支払準備完了](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>間もなく公開

予定されている機能とリリースの完全な一覧については、[Dynamics 365 Human Resources 2021 のリリース ウェーブ 2 の概要](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 のリリース ウェーブ 2 の概要](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
