---
title: Dynamics 365 for Talent の新機能および変更された機能 (2019 年 8 月 27 日)
description: このトピックでは、Microsoft Dynamics 365 for Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 8/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: andreabichsel
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-08-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8965636e539345be5ef0ad591f7017938efd322d
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529807"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-august-27-2019"></a>Dynamics 365 for Talent の新機能および変更された機能 (2019 年 8 月 27 日)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Dynamics 365 for Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。

## <a name="changes-in-onboard"></a>Onboard の変更

今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更

このセクションに記載された変更は、ビルド番号 8.1.2447 に適用されます。 ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>プレビュー機能は、サンドボックス インスタンスでのみ有効です。

Talent の新しいインスタンスをプロビジョニングする時に、インスタンス タイプを実稼働またはサンドボックスのどちらかに指定することができます。 サンドボックス タイプのインスタンスにより、新機能を事前にテストできるようになります。 既存の Talent のインスタンスすべては、実稼働インスタンス タイプに更新されます。 既存のインスタンスのいずれかをサンドボックス インスタンス タイプに更新する場合は、変更要求を開始するよう サポート に連絡してください。

変更を公開する方法の詳細については、[Talent のプロビジョニング](./provisioning-talent.md) を参照してください。

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>マネージャー セルフサービスの業績に関する追加情報の確認

新しいオプションにより、マネージャーは自分の直接レポートと拡張レポートの両方の業績を確認できるようになります。 現在、ライン マネージャーは業績目標の割り当てと更新、また新しい確認の発行をすることができます。 また、直属のマネージャーと従業員は業績仕訳の管理および更新を行うことにより、業績確認プロセスを確実に、スムーズに行うことができます。 この変更が実装されると、マネージャーは直接レポートに加えて、拡張レポートの業績関連情報の確認および管理ができるようになります。

### <a name="deleting-legal-entities-isnt-allowed-if-employees-exist-within-the-company-339849"></a>従業員が会社に存在する場合、法人を削除することは許可されていません (339849)

この変更により、法人に従業員および他の関連データが存在する場合、会社を削除することはできません。

### <a name="compensation-management-business-intelligence-analytics-dont-match-on-the-compensation-workspace-322493"></a>報酬管理ビジネス インテリジェンス分析が報酬ワークスペースと一致しません (322493)

このリリースで、報酬分析は、従業員に割り当てられたプランを正確に反映するように調整されました。

### <a name="workflow-placeholder-company-displays-dat-when-hiring-employees-through-workflow-343905"></a>ワークフロー プレースホルダー %company% は、ワークフローを通じて従業員を雇用する時に DAT を表示します (343905)

このリリースにより、会社のプレースホルダーは、新しい従業員の雇用に関連付けられている法人を表示することができます。

### <a name="the-cdsjobposition-entity-displays-an-error-when-valid-to-date-is-set-349387"></a>失効日が設定されている場合、CDSJobPosition エンティティはエラーを表示します (349387)

このリリースで、**CDSJobPosition** エンティティ上の **職位の詳細** および **職位の期間** データ ソースについて、Common Data Service から **有効日** フィールドに編集することが許可されています。 

### <a name="for-employee-termination-the-last-day-worked-is-populated-on-assignment-end-date-332496"></a>従業員の退職について、最終勤務日が割り当て終了日に設定されます (332496)

この変更により、職位の **割り当て終了日** が **雇用終了日** に既定で設定されるようになりました。 これらの既定値は、データの入力時に変更できます。

### <a name="legal-entities-arent-limited-with-hire-338871"></a>法人は雇用に関して制限されていません (338871)
 
この変更により雇用プロセスが制限され、ユーザーがアクセスできる法人のみが表示されるようになります。  

## <a name="in-preview"></a>プレビュー

### <a name="streamlined-employee-entry-and-navigation"></a>合理化された従業員の入力とナビゲーション

この機能は、サンドボックスおよび試用環境で使用可能になりました。 この機能を有効にするには、**システム管理 > リンク > 設定 > システム パラメーター > プレビュー機能** に移動します。 **拡張された作業者フォームおよびナビゲーション** を選択します。 これにより、これらの変更がすべてのユーザーに対して有効になります。 このオプションはいつでもオフにすることができます。

詳細については、[合理化された従業員の入力とナビゲーション](./streamlined-employee-entry.md) を参照してください。

## <a name="coming-soon"></a>間もなく公開

### <a name="platform-update-29"></a>プラットフォーム update 29

プラットフォーム更新プログラム 29 に関する詳細については [Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 29 (2019 年 10 月) のプレビュー機能](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29) を参照してください。


[!INCLUDE[footer-include](../includes/footer-banner.md)]