---
title: Dynamics 365 Talent (2019 年 10 月 1 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 69c0a805027f215b2a2a42d826ee7a346cfdd511
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529663"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-1-2019"></a>Dynamics 365 Talent (2019 年 10 月 1 日) の新機能および変更された機能

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Dynamics 365 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。

## <a name="changes-in-onboard"></a>Onboard の変更

今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更

このセクションに記載された変更は、ビルド番号 8.1.2509 に適用されます。 ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。

### <a name="streamlined-employee-entry-and-navigation"></a>合理化された従業員の入力とナビゲーション

この機能は、すべての環境で使用可能になりました。 この機能を有効にするには、**システム管理 > リンク > 設定 > システム パラメーター > プレビュー機能** に移動します。 **拡張された作業者フォームおよびナビゲーション** を選択します。 これにより、これらの変更がすべてのユーザーに対して有効になります。 このオプションはいつでもオフにすることができます。

詳細については、[合理化された従業員の入力とナビゲーション](./streamlined-employee-entry.md) を参照してください。 これらの変更のビデオを視聴するには、[Dynamics 365 for Talent 2019 リリース ウェーブ 2 の概要](https://aka.ms/ROGT19RW2ROV) を参照してください。

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a>サンドボックス環境および試用環境で、プレビュー機能を有効にできます

Talent の新しいインスタンスをプロビジョニングする時に、インスタンス タイプを実稼働またはサンドボックスのどちらかに指定することができます。 サンドボックス タイプのインスタンスにより、新機能を事前に試用できるようになります。 既存のインスタンスのいずれかをサンドボックス インスタンス タイプに更新する場合は、変更要求を開始するよう サポート に連絡してください。

変更を公開する方法の詳細については、[Talent のプロビジョニング](./provisioning-talent.md) を参照してください。

### <a name="compensation-date-defaults-to-a-different-date-than-the-position-assignment-337694"></a>報酬日付は、既定で職位の割り当てと異なる日付になります (337694)

この変更により、報酬開始日の既定値は、職位の割り当ての開始日になります。

### <a name="not-able-to-end-compensation-along-with-its-position-assignment-328993"></a>その職位の割り当てと共に報酬を終了することはできません (328993)

この変更により、個人のアクションが有効になっている **作業者職位の割り当て** ページで **割り当ての終了** を使用して、職位の割り当てを終了する際に報酬を終了できます。

### <a name="bank-account-validation-requires-routing-and-account-numbers-in-all-locations-340403"></a>銀行口座の検証には、すべての場所における処理番号、口座番号が必要になります (340403)

今週の変更により、検証の必要な **処理番号** および **口座番号** が無効にする新しいコンフィギュレーション オプションが追加されます。 

### <a name="attachments-are-not-enabled-in-mss-performance-journals-for-performance-feedback-341794"></a>パフォーマンス フィードバックの MSS 業績仕訳帳で添付ファイルが有効になりません (341794)

今週のリリースでは、業績仕訳帳ページのフィードバック項目に対して添付ファイルが有効になっています。

### <a name="leave-request-details-dont-sync-from-common-data-service-to-talent-369608"></a>休暇申請詳細情報は Common Data Service から Talent に同期しません (369608)

これらの変更により、Common Data Service で更新された休暇申請詳細情報は、Talent に逆同期されます。

### <a name="job-description-doesnt-display-for-the-job-in-the-skill-gap-analysis-page-369398"></a>職務明細書がスキル ギャップ分析ページに表示されません (369398)

今週のビルドでは、**スキル ギャップ分析** ページでジョブを選択する際に詳細が表示されます。

## <a name="coming-soon"></a>間もなく公開

### <a name="print-performance-reviews"></a>業績の確認の印刷

従業員、マネージャー、および人事担当者は、従業員の業績の確認を印刷できるようになります。
