---
title: Dynamics 365 Talent (2019 年 12 月 10 日) の新機能および変更された機能
description: この記事では、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 12/10/2019
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
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 18f86f5d87b780d5d4ffc83330d389077987dda6
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528174"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-10-2019"></a>Dynamics 365 Talent (2019 年 12 月 10 日) の新機能および変更された機能

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Dynamics 365 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。

## <a name="changes-in-onboard"></a>Onboard の変更

今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更

このセクションに記載された変更は、ビルド番号 8.1.2660 に適用されます。 ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。

### <a name="feature-management-workspace"></a>機能管理ワークスペース

**機能管理** ワークスペースでは、各リリースで可能になる機能の一覧を表示できます。 既定では、新機能が無効になっています。 ワークスペースを使用してそれらを有効にし、それらのドキュメントを参照できます。 機能管理の詳細については [機能管理の概要](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) を参照してください。

すべての新機能は少なくとも 30 日間、通常は 30-60 日間、プレビューのままになります。 主な機能は、通常、プレビュー期間に従って毎年 10 月と 4 月に使用可能です。 **機能管理** ワークスペースに新しい機能が表示されたら、すぐにそれらをオンにすることができます。 一部の機能は既定でオンになっている場合があります。
 
場合によっては、通常は整数機能が有効になりますが、オフにすることはできません (**機能管理** ワークスペースなど)。
 
機能が一般に使用可能になったら、運用環境でオンまたはオフにすることができます。 **機能管理** ワークスペースは、プレビュー機能が必須になるタイミングを示します。 この日付は、通常、半年のリリース計画に沿って 10 月 1 日または 4 月 1 日になっています。 必須機能を無効にすることはできません。 必須になるまでは、すべての環境で機能を有効または無効にすることができます。

### <a name="streamlined-worker-form-has-moved-to-the-feature-management-workspace-390583"></a>合理化された作業者のフォームが機能管理ワークスペースに移動された (390583)

この変更により、合理化された作業者のフォームを **機能管理** ワークスペースで有効にすることができるようになりました。 この機能は、**システム管理** の **システム パラメーター** フォームから移動されました。

### <a name="prevent-hcmworkerpayrollinfo-records-from-being-written-without-a-worker-value-394526"></a>HcmWorkerPayrollInfo レコードが、作業者の値がなくても書き込まれるのを防止する (394526)

今回のリリースにより、このシナリオで作業者の参照がない場合、**HcmWorkerPayrollInfo** レコードは作成されなくなりました。 

### <a name="message-log-associated-to-the-action-isnt-populated-when-the-action-fails-to-complete-374007"></a>アクションの完了に失敗した場合、アクションに関連付けられているメッセージ ログが設定されない (374007)

このリリースには、特定のシナリオでアクションが失敗した場合にアクション メッセージ ログを設定するための変更が含まれています。 

### <a name="common-data-service-integration-batch-job-creation-388030"></a>Common Data Service 統合バッチ ジョブの作成 (388030)

この変更により、サービスを有効にした時に Common Data Service 統合のためのバッチ ジョブが作成されます。

### <a name="additional-pick-list-values-to-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>カスタム フィールド フォームで適用をクリックしても、カスタム フィールドの追加のピッキング リスト値が Common Data Service に反映されない (379599)

この変更により、Talent で入力された新しいピッキング リスト値が、変更を適用する時に Common Data Service と同期されるようになりました。

### <a name="update-to-common-data-service-for-then-leave-bank-transaction-entity-turns-into-an-insert-on-talent-side-352938"></a>休暇バンク トランザクション エンティティに関する Common Data Service への更新が、Talent 側への挿入に変わる (352938)

この変更により、休暇バンク トランザクションに対する更新で、Talent に新しいレコードが作成される問題が修正されます。

## <a name="in-preview"></a>プレビュー

プレビュー機能は **サンドボックス** 環境でのみ有効になります。

### <a name="print-performance-reviews"></a>業績の確認の印刷

詳細については、Dynamics 365: 2019 リリース ウェーブ 2 プランにある[業績の確認の印刷](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews)を参照してください。

