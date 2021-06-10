---
title: Dynamics 365 Human Resources（2020 年 5 月 1 日）の新機能と変更された機能
description: この記事では、2020 年 5 月 1 日に更新された Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: andreabichsel
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e8ceea10b3157fee410e5db6e1d8c9a0366e30e2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6050972"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-1-2020"></a>Dynamics 365 Human Resources（2020 年 5 月 1 日）の新機能と変更された機能

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。 変更は、ビルド番号 8.1.3196 に適用されます。 ヘッダーにあるかっこ内の数字は、参照用の LCS のサポート番号を参照していることがあります。

## <a name="new-performance-management-entities-available-in-data-management-framework-dmf"></a>データ管理フレームワーク (DMF) で使用できる新しいパフォーマンス管理エンティティ

次のエンティティが利用可能になりました。 エンティティ リストにこれらのエンティティが表示されない場合は、**フレームワーク パラメーター > エンティティ設定 > エンティティ リストの更新** の **エンティティの更新** オプションを使用します。

- **ディスカッションのコンピテンシー**
- **ディスカッションの目標**
- **ディスカッションの測定**
- **ディスカッションのトピック**
- **業績履歴**
- **測定**
- **目標の測定**

さらに、**合計スコア** と **平均スコア** が **ディスカッション** エンティティに追加されました。

## <a name="increase-length-of-leave-request-comments-275641"></a>休暇要求のコメントの文字数の増加 (275641)

休暇に対するコメントで、100 文字を超えた入力が許可されます。

## <a name="final-comments-on-reviews-dont-appear-when-the-manager-or-employee-is-signed-into-a-different-company-431688"></a>マネージャーや従業員が別の会社にサイン インしている場合、レビューの最終コメントは表示されません (431688)

レビューを表示すると、すべてのコメントが表示されるようになります。

## <a name="user-defined-links-arent-supported-on-new-worker-form-390374"></a>新しい作業者フォームでユーザー定義のリンクに対応していない (390374)

合理化された **作業者** フォームで、ユーザー定義のリンクを有効にすることができます。

## <a name="hcmratinglevelentity-causes-odata-api-crash-439476"></a>HcmRatingLevelEntity により、OData API がクラッシュする (439476)

この変更により、API のクラッシュが修正されます。 重複した名称がこのエラーの原因となりました。

## <a name="in-preview"></a>プレビュー

## <a name="leave-suspension"></a>休暇の停止

従業員に対し Human Resources で休暇および欠勤を中断できます。 休暇を中断すると、選択した休暇タイプの休暇の発生が停止します。 一時停止が見越計上プロセス後に発生した場合、休暇の一時停止により、従業員の休暇残日数が比例配分調整されます。 詳細については、[休暇の中断](hr-leave-and-absence-suspend-leave.md) を参照してください。

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>ユーザー エクスペリエンスを更新し、見越計上の中断が表示されるようになりました (429550)

ユーザー エクスペリエンスは、計画に対して見越計上が中断されたことを示します。

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a>指定した休暇タイプの休暇取得を一時停止する (272447)

今回のリリースでは、人事部は無給休暇の休暇申請を入力した従業員に対して、休暇の発生を停止するルールを作成することができます。 無給休暇のタイプを指定できますが、必須ではあります。 他の休暇種類に基づいて、任意の休暇を停止することができます。

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a>DMF エンティティが見越し計上の停止に使用可能 (429549)

DMF エンティティが見越し計上の停止に使用できるようになりました 。

## <a name="add-reason-code-to-accrual-suspensions-429547"></a>見越計上の停止に理由コードが追加されました (429547)

見越計上の中断に理由コードが追加されました。

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a>人事パラメータから休職,、欠勤パラメータへの移行を開始

このリリースでは、人事管理パラメータと休暇・欠勤のパラメータの組み合わせに対応しています。

## <a name="carry-forward-rules"></a>繰越ルール

繰越調整を転送する繰越残日数に対して、繰越休暇タイプを指定できます。 たとえば、従業員が 10 日間繰り越す場合、その 10 日間に別の休暇タイプを選択できます。 詳細については、[休暇および欠勤タイプのコンフィギュレーション](hr-leave-and-absence-types.md) を参照してください。

## <a name="known-issues"></a>既知の問題

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>一部の環境で、SharePoint プレビューが機能しない

SharePoint で保存されているドキュメントのドキュメント プレビューが機能しない場合は、次の手順を実行します。

1. 管理者のユーザー アカウントにユーザー レコードに関連付けられたメールがあることを確認します。 この情報は、**ユーザー** ページで確認できます。 メールが設定されていない場合は、OData Excel アドインを使用してメールとプロバイダーを追加する必要があります。 既定では、Excel デザインにメール アドレスは表示されません。 Excel デザインを編集し、すべてのフィールドを追加し、適用して更新する必要があります。 これらのステップを完了すると、管理者アカウントを更新できます。

2. 管理者アカウントにメール アカウントが関連付けられたら、人事管理に管理者としてサインインします。

3. SharePoint で添付ファイルにアクセスして、ドキュメントのプレビューを開始します。

4. 添付ファイルにアクセスできる他のユーザー アカウントでサインインし、適切にプレビューが機能することを確認します。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]