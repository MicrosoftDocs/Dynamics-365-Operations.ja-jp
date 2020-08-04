---
title: Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 4 月 3 日)
description: この記事では、Microsoft Dynamics 365 Human Resources の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 04/03/2020
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
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 02243b2c75a4f50683a51c1d9d811f2e2a2d413f
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555054"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-3-2020"></a>Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 4 月 3 日)

この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。 変更は、ビルド番号 8.1.3111 に適用されます。 一部のヘッダーにあるかっこ内の数字は、参照用に Lifecycle Services (LCS) のサポート番号を参照しています。

## <a name="features-that-are-generally-available-the-week-of-april-6"></a>4 月 6 日の週に一般公開される機能

- **休暇と欠勤の機能** - 詳細については、[休暇と欠勤の概要](hr-leave-and-absence-overview.md) を参照してください。

- **福利厚生管理の機能** - 詳細については、[福利厚生管理の概要](hr-benefits-management-overview.md) を参照してください。

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>人事管理環境の制限は、現在、更新されたライセンスに基づいている (394595)

LCS のプロジェクトあたりの環境数の制限が変更されました。 以前の制限は 2 つの環境でした。 LCS で人事管理用に作成できる運用環境とサンドボックス環境の数の制限は、更新されたライセンスに基づいています。 購入したライセンスの数に応じて、LCS プロジェクトごとに必要な数の環境を作成できるようになりました。 2020 年 2 月 1 日に更新された新しいライセンスでは、顧客は追加の環境を購入できます。 追加の環境のライセンス要件の詳細については、[Dynamics 365 ライセンスガイド](https://dynamics.microsoft.com/pricing/#HumanResources) を参照してください。
 
## <a name="error-when-trying-to-delete-a-questionnaire-428603"></a>アンケートを削除しようとするとエラーが発生しました (428603)

今週の更新プログラムでは、アンケートを削除しようとすると次のエラーが表示される問題が修正されました:

アンバランスな X++ TTSBEGIN/TTSCOMMIT ペアが検出されました。

## <a name="performance-journal-and-professional-certificates-security-issue-428499"></a>業績仕訳と専門的な証明書のセキュリティ問題 (428499)

この変更により、アクセスできる企業に基づいて、業績仕訳と専門的な証明書の両方の表示が制限されます。 

## <a name="the-abbreviation-for-quebec-and-manitoba-387510"></a>ケベック州とマニトバ州の略語 (387510)

開始データは、マニトバ州とケベック州の正しい略語を反映するように更新されました。

## <a name="new-entities-available-in-data-management-framework"></a>データ管理フレームワークで使用できる新しいエンティティ

次のエンティティが利用可能になりました。 エンティティ リストにこれらのエンティティが表示されない場合は、**フレームワーク パラメーター > エンティティ設定 > エンティティ リストの更新** の **エンティティの更新** オプションを使用します。

 - 休暇の銀行トランザクション V2
 - 休暇の登録 V2
 - 休暇計画層 V2
 - 休暇計画 V2

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Common Data Service ソリューションが、次の変更で利用可能になりました。

| 説明 | 計上額 |
| --- | --- |
| **職務/職位**エンティティの変更 | <ul><li>追加された**報酬地域**</li>|
| 追加された**職務職位分析**エンティティ | <ul><li>追加された**財務分析コード**</li>
| **作業者**エンティティの変更 | <ul><li>追加された**名前の順序**</li><li>追加された**自宅から作業**</li><li>追加された**言語**</li><li>追加された**勤続日数**</li><li>追加された**記念日**</li><li>追加された**元の採用日付**</li></ul> |
| **雇用**エンティティの変更 | <ul><li>追加された**財務分析コード**</li><li>追加された**退職理由**</li><li>**移行日**から名前変更された**退職日**</li><li>追加された**猶予期間**</li></ul> |
| **作業者住所**エンティティの変更 | <ul><li>追加された**番地**</li><li>廃止としてマークされた**住所行 1**、**住所行 2**、および**住所行 3**</li></ul> |
| 新しい変動報酬の設定エンティティ | <ul><li>**変動報酬プラン タイプ**</li><li>**変動報酬プラン**</li><li>**給付ルール**</li><li>**変動報酬プラン レベル**</li></ul> |
| 新しい**作業者カレンダー雇用**エンティティ | <ul><li>追加された**作業カレンダー エンティティ**</li></ul> |
| 新しい**給与職位詳細**エンティティ | <ul><li>追加された**給与職位詳細**</li></ul> |
| 新しい**肩書**エンティティ | <ul><li>追加された**タイトル**</li></ul>新しい**タイトル** エンティティは Common Data Service に含まれますが、この時点では**職位**または**職務**エンティティから参照されません。 |

> [!NOTE]
> 職位と雇用どちらの財務分析コードは、Human Resources から Common Data Service への更新の一方向の統合を提供します。 財務分析コードの更新は、現在 Common Data Service から Human Resources へは同期されません。

今後数週間のうちに、これらのエンティティの変更がすべての環境で使用できるようになります。 Human Resources の最新 Common Data Service ソリューションを手動でインストールするには、次の操作を行います。

1.  [Power Platform 管理センター](https://admin.powerplatform.microsoft.com) に移動します。

2.  **環境**を選択します。

3.  アップグレードする環境を検索します。 環境は、Human Resources の**バージョン情報**フォームで、**Common Data Service 情報**セクションの**環境名**に対応している必要があります。

4.  環境の詳細を表示するための環境を選択します。

5.  上部の操作バーで、**ソリューションの管理**を選択します。 新しいブラウザー ウィンドウが開き、環境のコンテキストで**Dynamics 365 管理センター**に移動します。

6.  **ソリューション** リストで、**Dynamics 365 Human Resources アンカー**を選択します。

7.  最新のソリューションを適用するには、**アップグレード**を選択します。

## <a name="in-preview"></a>プレビュー

## <a name="leave-suspension"></a>休暇の停止

従業員に対し Human Resources で休暇および欠勤を中断できます。 休暇を中断すると、選択した休暇タイプの休暇の発生が停止します。 一時停止が見越計上プロセス後に発生した場合、休暇の一時停止により、従業員の休暇残日数が比例配分調整されます。 詳細については、[休暇の中断](hr-leave-and-absence-suspend-leave.md) を参照してください。

## <a name="carry-forward-rules"></a>繰越ルール

繰越調整を転送する繰越残日数に対して、繰越休暇タイプを指定できます。 たとえば、従業員が 10 日間繰り越す場合、その 10 日間に別の休暇タイプを選択できます。 詳細については、[休暇および欠勤タイプのコンフィギュレーション](hr-leave-and-absence-types.md) を参照してください。

## <a name="coming-soon"></a>間もなく公開

## <a name="new-production-release-cadence"></a>新しい生産リリース リズム

4 月から、Human Resources のリリース頻度は、毎週更新から隔週更新に移行します。 安全な展開プラクティスとの整合性を確保し、サービスの安定性と信頼性の高い標準を維持するために、すべての地域にサービス更新を展開するプロセスは 2 週間で展開されます。 プロセスの各ステージで展開が成功したことを確認するために、追加のテストとモニターが実行されます。 リリース頻度の詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

## <a name="known-issues"></a>既知の問題

## <a name="employment-detail-entity"></a>雇用の詳細エンティティ

**雇用の詳細** エンティティが、次のフィールドで更新されました: **PayFrequency**、**雇用カテゴリ ID**、**雇用タイプ**、**EmploymentType ID**、**福利厚生の雇用状況**。 これらのフィールドの設定データは、機能管理で有効になっている福利厚生の管理に依存します。 これらのフィールドは、インポート中にエラーが発生するため、**雇用の詳細** エンティティで入力または更新しないでください。

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>一部の環境で、SharePoint プレビューが機能しない

SharePoint で保存されているドキュメントのドキュメント プレビューが機能しない場合は、次の手順を実行します。

1. 管理者のユーザー アカウントにユーザー レコードに関連付けられたメールがあることを確認します。 この情報は、**ユーザー** ページで確認できます。 メールが設定されていない場合は、OData Excel アドインを使用してメールとプロバイダーを追加する必要があります。 既定では、Excel デザインにメール アドレスは表示されません。 Excel デザインを編集し、すべてのフィールドを追加し、適用して更新する必要があります。 これらのステップを完了すると、管理者アカウントを更新できます。

2. 管理者アカウントにメール アカウントが関連付けられたら、人事管理に管理者としてサインインします。

3. SharePoint で添付ファイルにアクセスして、ドキュメントのプレビューを開始します。

4. 添付ファイルにアクセスできる他のユーザー アカウントでサインインし、適切にプレビューが機能することを確認します。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)