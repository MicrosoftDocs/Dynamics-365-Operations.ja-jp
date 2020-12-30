---
title: Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 3 月 19 日)
description: この記事では、2020 年 3 月 19 日に更新された Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 03/19/2020
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
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 902539a5abecba6ad99718afbb37613838450032
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526868"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-19-2020"></a>Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 3 月 19 日)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。 変更は、ビルド番号 8.1.3014 に適用されます。 一部のヘッダーにあるかっこ内の数字は、参照用に Lifecycle Services (LCS) のサポート番号を参照しています。

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>人事管理環境の制限は、現在、更新されたライセンスに基づいている (394595)

Lifecycle Services (LCS) のプロジェクトあたりの環境数の制限が変更されました。 以前の制限は 2 つの環境でした。 LCS で人事管理用に作成できる運用環境とサンドボックス環境の数の制限は、更新されたライセンスに基づいています。 購入したライセンスの数に応じて、LCS プロジェクトごとに必要な数の環境を作成できるようになりました。 2020 年 2 月 1 日に更新された新しいライセンスでは、顧客は追加の環境を購入できます。 追加の環境のライセンス要件の詳細については、[Dynamics 365 ライセンスガイド](https://dynamics.microsoft.com/pricing/#HumanResources) を参照してください。

## <a name="provide-cross-company-viewing-of-compensation-data-for-employees-and-managers-403904"></a>従業員とマネージャーの報酬データを会社表示する (403904)

**機能の管理** ワークスペースで、この機能を有効にします。 詳細は、[プレビュー機能を有効または無効にする](hr-admin-manage-features.md#enable-or-disable-preview-features) を参照してください。

この機能を有効にすると、マネージャーは雇用のある会社にログインすることなく、直属の部下および拡張レポートの報酬を表示することができます。 完全な報酬履歴は、マネージャーがアクセスできるログインしている会社から入手できます。 詳細については、[従業員およびマネージャー セルフサービスの概要](hr-employee-manager-self-service-overview.md) を参照してください。

## <a name="enable-global-address-book-merge-functionality-427189"></a>グローバル アドレス帳のマージ機能を有効にする (427189)

重複するアドレス帳エントリをマージするには、重複するレコードを選択して、**グローバル アドレス帳** ページから選択し、**マージ** を選択します。

## <a name="unable-to-adjust-leave-balance-for-a-plan-with-no-accruals-that-was-created-with-the-multiple-leave-type-feature-on-419635"></a>複数の休暇タイプ機能を使用して作成された、見越計上のない計画の休暇残高を調整できない (419635)

ここで、機能管理で **複数の休暇タイプ** プレビュー機能を有効にして作成した休暇計画の残高を調整できます。

## <a name="primary-position-field-in-the-workerpositionassignmententity-when-an-employee-is-terminated-420774"></a>従業員が退職したときの WorkerPositionAssignmentEntity の基本職位フィールド (420774)

雇用が終了した従業員については、退職時にアクティブだった基本職位がエンティティに表示されます。 統合の場合は、その従業員の作業者の職位割り当てに対して重複するレコードが作成されなくなります。 

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
| 新しい **肩書** エンティティ | <ul><li>追加された **タイトル**</li></ul>新しい **タイトル** エンティティは Common Data Service に含まれますが、この時点では **職位** または **職務** エンティティから参照されません。 |

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

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>一部の環境で、SharePoint プレビューが機能しない

SharePoint で保存されているドキュメントのドキュメント プレビューが機能しない場合は、次の手順を実行します。

1. 管理者のユーザー アカウントにユーザー レコードに関連付けられたメールがあることを確認します。 この情報は、**ユーザー** ページで確認できます。 メールが設定されていない場合は、OData Excel アドインを使用してメールとプロバイダーを追加する必要があります。 既定では、Excel デザインにメール アドレスは表示されません。 Excel デザインを編集し、すべてのフィールドを追加し、適用して更新する必要があります。 これらのステップを完了すると、管理者アカウントを更新できます。

2. 管理者アカウントにメール アカウントが関連付けられたら、人事管理に管理者としてサインインします。

3. SharePoint で添付ファイルにアクセスして、ドキュメントのプレビューを開始します。

4. 添付ファイルにアクセスできる他のユーザー アカウントでサインインし、適切にプレビューが機能することを確認します。

## <a name="coming-soon"></a>間もなく公開

### <a name="platform-update-33"></a>プラットフォーム update 33

- フル ページ アプリ (プレビュー) - このプレビュー機能は、保存されたビュー機能を有効にする必要があり、ダッシュボードから Power Apps とサード パーティー アプリをフルページ エクスペリエンスとして追加できます。

- 保存されているビュー (プレビュー) - このプレビュー機能はパーソナル化 サブシステムの大幅な拡張を提供する、保存されているビューを有効にします。 この機能により、ユーザーはページごとに複数の名前を付けた個人用設定を使用できます。 セキュリティ ロールにビューを公開することもできます。

- 「次の値のいずれか」のフィルタリング結果を最適化 - この機能により、最適化された「いずれか」のフィルタリング結果が可能になり、複数のフィルター値の入力を容易にして、個々またはすべてのフィルター値を削除する簡単なメカニズムを備え、またフィルター値のよりコンパクトで直感的な視覚化を実現します。

- 推奨されるフィールド - ユーザーは、多くの場合、グリッドまたはページにフィールドを追加する必要があります。 多数の使用可能なフィールドでは、これは困難になることがあります。 この機能により、大きなリストを通じて検索する代わりに、システムは類似のシナリオでほかのユーザーが最も頻繁に追加する内容に基づいて、一連の推奨されるフィールドを表示することが有効になります。

- グリッド内の既定の付箋アクション - この機能により、グリッド内の既定のアクションは、その列が移動または非表示のどちらであるかに関係なく、グリッド内の特定の列にリンクされます。

## <a name="new-production-release-cadence"></a>新しい生産リリース リズム

4 月から、人事管理のリリース リズムは、毎週更新から隔週の更新に移行します。 これにより、安全な展開プラクティスでアラインメントを行い、サービスの安定性と信頼性の高い基準を維持することができます。 プロセスの各ステージで成功した展開を確認するために、テストとモニターを追加で実行しています。 リリース リズムの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

## <a name="in-preview"></a>プレビュー

2020 年 2 月 3 日に次のプレビュー機能が利用可能になります。

- **休暇および欠勤のプレビュー機能** - 詳細については、[休暇および欠勤のプレビュー機能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features) を参照してください。

- **福利厚生管理プレビュー機能** - 既知の問題など、詳細については[福利厚生管理の概要](hr-benefits-management-overview.md)を参照してください。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)