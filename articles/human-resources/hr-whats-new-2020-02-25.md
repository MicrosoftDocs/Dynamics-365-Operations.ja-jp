---
title: Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 2 月 25 日)
description: この記事では、2020 年 2 月 25 日に更新された Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: andreabichsel
manager: tfehr
ms.date: 02/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4faecb83518f3ef8af825872abc2a6ffb94162fc
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5128025"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a>Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 2 月 25 日)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。 変更は、ビルド番号 8.1.2927 に適用されます。 ヘッダーにあるかっこ内の数字は、参照用の LCS のサポート番号を参照していることがあります。

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a>ケース管理ナビゲーションおよびデータ管理フレームワーク (DMF) エンティティを有効にする (414754)

このプレビュー機能を使用すると、ケース管理ケースへの追加ナビゲーションができます。 このプレビュー機能は、**機能管理** ワークスペースで有効にすることができます。 これらのメニュー項目は、Dynamics 365 Human Resources の **コンプライアンス** ワークスペースに表示されます。 この変更により、Human Resources は次のような情報にアクセスできます。

- すべてのケース
- 自分のケース
- 自分のオープンなケース
- 自分の期限を過ぎたケース
- ワークフローを使用して自分に割り当てられたケース

これらの新しいビューと共に、**ケースの詳細** DMF エンティティも使用できます。

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a>グローバル アドレス帳でのリレーションシップの定義を有効にする (414762)

グローバル アドレス帳でリレーションシップが有効になりました。 今週のリリース前までは、**リレーションシップ** 情報ボックスはすべてのシステム定義されたリレーションシップを表示していました。 これで、グローバル アドレス帳ページでこれらのリレーションシップを定義することができます。

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a>職位に有効な報酬レコードが存在する場合、その職位を削除できます (414568)

この変更により、職位を削除しようと試みるとき作業者が同じ職位の有効な報酬レコードを持っている場合、警告が表示されます。 この場合、職位を削除する前に、従業員の固定報酬レコードを更新する必要があります。

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a>業績の確認ワークフローでは、プロセスの一部でない人物からのサイン オフが時折追加されます (414171)

この変更により、追加のサイン オフ参加者がパフォーマンス レビューに追加される場合に発生する問題を修正します。

## <a name="worker-position-assignment-not-created-in-dataverse-when-selected-on-the-new-worker-dialog-413479"></a>新しい作業者ダイアログで選択した場合、Dataverse で作業者の職位割り当てが作成されません (413479)

この変更により、新しい作業員を採用して **新しい作業者** ダイアログから新しい採用を職務に割り当てる場合に発生する問題を修正します。 これで、職位の割り当てが Dataverse に反映されるようになります。

## <a name="coming-soon"></a>間もなく公開

### <a name="updated-dataverse-solution"></a>更新された Dataverse ソリューション

次の変更により、新しい Dataverse ソリューションがまもなく利用可能になります。

| 説明 | 計上額 |
| ----------------------------------------- | --- |
| **職務/職位** エンティティの変更 | 追加された **報酬地域**</br>追加された **財務分析コード** |
| **作業者** エンティティの変更 | 追加された **名前の順序**</br>追加された **自宅から作業**</br>追加された **言語**</br>追加された **勤続日数**</br>追加された **記念日**</br>追加された **元の採用日付** |
| **雇用** エンティティの変更 | 追加された **財務分析コード**</br>追加された **退職理由**</br>**移行日** から名前変更された **退職日**</br>追加された **猶予期間** |
| **作業者住所** エンティティの変更 | 追加された **番地**</br>廃止としてマークされた **住所行 1**、**住所行 2**、および **住所行 3** |
| 新しい変動報酬の設定エンティティ | **変動報酬プラン タイプ**</br>**変動報酬プラン**</br>**給付ルール**</br>**変動報酬プラン レベル** |
| 新しい **作業者カレンダー雇用** エンティティ | 追加された **作業カレンダー エンティティ** |
| 新しい **給与職位詳細** エンティティ | 追加された **給与職位詳細** |
| 新しい **肩書** エンティティ | 追加済み **タイトル**。 新しい **タイトル** エンティティが、Human Resources と Dataverse の間の同期プロセスに含まれます。 **職位** または **ジョブ** エンティティから最初に参照されることはありません。 |

今後数週間のうちに、これらのエンティティの変更がすべての環境で使用できるようになります。 Human Resources の最新 Dataverse ソリューションを手動でインストールするには、次の操作を行います。

1.  [Power Platform 管理センター](https://admin.powerplatform.microsoft.com) に移動します。

2.  **環境** を選択します。

3.  アップグレードする環境を検索します。 これは、Human Resources の **バージョン情報** フォームで、**Common Data Service 情報** セクションの **環境名** に対応している必要があります。

4.  環境の詳細を表示するための環境を選択します。

5.  上部の操作バーで、**ソリューションの管理** を選択します。 新しいブラウザー ウィンドウが開き、環境のコンテキストで **Dynamics 365 管理センター** に移動します。

6.  **ソリューション** リストで、**Dynamics 365 Human Resources アンカー** を選択します。

7.  最新のソリューションを適用するには、**アップグレード** を選択します。

## <a name="in-preview"></a>プレビュー

次のプレビュー機能が 2020 年 2 月 3 日に利用可能になります。

- **休暇および欠勤のプレビュー機能** - 詳細については、[休暇および欠勤のプレビュー機能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features) を参照してください。

- **福利厚生管理プレビュー機能** - 既知の問題など、詳細については[福利厚生管理の概要](hr-benefits-management-overview.md)を参照してください。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]