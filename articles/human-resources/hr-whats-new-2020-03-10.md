---
title: Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 3 月 10 日)
description: この記事では、2020 年 3 月 10 日に更新された Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 03/10/2020
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
ms.author: dkrame
ms.search.validFrom: 2020-03-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 944481727f3222a10f128ac3078c117f5ae7d193
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526921"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-10-2020"></a>Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 3 月 10 日)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。 変更は、ビルド番号 8.1.2985 に適用されます。 ヘッダーにあるかっこ内の数字は、参照用の LCS のサポート番号を参照していることがあります。

## <a name="cant-access-skill-gap-analysis-report-394460"></a>スキル ギャップ分析レポートにアクセスできません (394460)

このレポートは Dynamics 365 Human Resources ではサポートされていません。 SSRS レポートを印刷するためのメニュー項目が削除されます。

## <a name="incorrect-message-accessing-the-getting-started-page-417950"></a>はじめにページにアクセスするメッセージが正しくありません (417950)

この変更により、フォームへのアクセス許可がない場合は、セキュリティによってこのメニュー項目が非表示になります。

## <a name="streamlined-task-maintenance-for-employees-380538"></a>従業員のタスク メンテナンスの合理化 (380538)

作業者タスク メンテナンス フォームには、オンボード、オフボード、移動、および業務プロセスのすべてのタスクが表示されます。 タスクの状態を削除、再割り当て、または更新できるようになりました。

例: ベンジャミン マーティンは福利厚生管理者です。 従業員のオンボードでは、ベンジャミンに対してタスクが作成され、新しい従業員の給付金の選択が確認されます。 ベンジャミンには、完了した過去のタスクと、完了する必要がある将来のタスクがあります。 ベンジャミンが会社を退職することを決定したので、タスクを再割り当てまたは削除する必要があります。 タスクのメンテナンス フォーム (**作業者** フォームのアクション ウィンドウ) では、ベンジャミンのすべてのタスクが別の作業者に再割り当てされるかまたは削除されます。  

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Common Data Service ソリューションが、次の変更で利用可能になりました。

| 説明 | 計上額 |
| --- | --- |
| **職務/職位** エンティティの変更 | <ul><li>追加された **報酬地域**</li>|
| 追加された **職務職位分析** エンティティ | <ul><li>追加された **財務分析コード**</li>
| **作業者** エンティティの変更 | <ul><li>追加された **名前の順序**</li><li>追加された **自宅から作業**</li><li>追加された **言語**</li><li>追加された **勤続日数**</li><li>追加された **記念日**</li><li>追加された **元の採用日付**</li></ul> |
| **雇用** エンティティの変更 | <ul><li>追加された **財務分析コード**</li><li>追加された **退職理由**</li><li>**移行日** から名前変更された **退職日**</li><li>追加された **猶予期間**</li></ul> |
| **作業者住所** エンティティの変更 | <ul><li>追加された **番地**</li><li>廃止としてマークされた **住所行 1**、**住所行 2**、および **住所行 3**</li></ul> |
| 新しい変動報酬の設定エンティティ | <ul><li>**変動報酬プラン タイプ**</li><li>**変動報酬プラン**</li><li>**給付ルール**</li><li>**変動報酬プラン レベル**</li></ul> |
| 新しい **作業者カレンダー雇用** エンティティ | <ul><li>追加された **作業カレンダー エンティティ**</li></ul> |
| 新しい **給与職位詳細** エンティティ | <ul><li>追加された **給与職位詳細**</li></ul> |
| 新しい **肩書** エンティティ | <ul><li>追加された **タイトル**</li></ul> 新しい **タイトル** エンティティは Common Data Service に含まれますが、この時点では **職位** または **職務** エンティティから参照されません。 |

> [!NOTE]
> 職位と雇用どちらの財務分析コードは、Human Resources から Common Data Service への更新の一方向の統合を提供します。 財務分析コードの更新は、現在 Common Data Service から Human Resources へは同期されません。

今後数週間のうちに、これらのエンティティの変更がすべての環境で使用できるようになります。 Human Resources の最新 Common Data Service ソリューションを手動でインストールするには、次の操作を行います。

1.  [Power Platform 管理センター](https://admin.powerplatform.microsoft.com) に移動します。

2.  **環境** を選択します。

3.  アップグレードする環境を検索します。 環境は、Human Resources の **バージョン情報** フォームで、**Common Data Service 情報** セクションの **環境名** に対応している必要があります。

4.  環境の詳細を表示するための環境を選択します。

5.  上部の操作バーで、**ソリューションの管理** を選択します。 新しいブラウザー ウィンドウが開き、環境のコンテキストで **Dynamics 365 管理センター** に移動します。

6.  **ソリューション** リストで、**Dynamics 365 Human Resources アンカー** を選択します。

7.  最新のソリューションを適用するには、**アップグレード** を選択します。

## <a name="in-preview"></a>プレビュー

2020 年 2 月 3 日に次のプレビュー機能が利用可能になります。

- **休暇および欠勤のプレビュー機能** - 詳細については、[休暇および欠勤のプレビュー機能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features) を参照してください。

- **福利厚生管理プレビュー機能** - 既知の問題など、詳細については[福利厚生管理の概要](hr-benefits-management-overview.md)を参照してください。

## <a name="coming-soon"></a>間もなく公開

### <a name="platform-update-33"></a>プラットフォーム update 33

- フル ページ アプリ (プレビュー) - このプレビュー機能は、保存されたビュー機能を有効にする必要があり、ダッシュボードから Power Apps とサード パーティー アプリをフルページ エクスペリエンスとして追加できます。

- 保存されているビュー (プレビュー) - このプレビュー機能は個人用設定サブシステムの大幅な拡張で、保存されているビューを有効にします。 この機能により、ユーザーはページごとに複数の名前を付けた個人用設定を使用できます。 セキュリティ ロールにビューを公開することもできます。

- 「次の値のいずれか」のフィルタリング結果を最適化 - この機能により、最適化された「いずれか」のフィルタリング結果が可能になり、複数のフィルター値の入力を容易にして、個々またはすべてのフィルター値を削除する簡単なメカニズムを備え、またフィルター値のよりコンパクトで直感的な視覚化を実現します。

- 推奨されるフィールド - ユーザーは、多くの場合、グリッドまたはページにフィールドを追加する必要があります。 多数の使用可能なフィールドでは、これは困難になることがあります。 この機能により、大きなリストを通じて検索する代わりに、システムは類似のシナリオでほかのユーザーが最も頻繁に追加する内容に基づいて、一連の推奨されるフィールドを表示することが有効になります。

- グリッド内の既定の付箋アクション - この機能により、グリッド内の既定のアクションは、その列が移動または非表示のどちらであるかに関係なく、グリッド内の特定の列にリンクされます。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)