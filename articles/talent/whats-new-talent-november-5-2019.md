---
title: Dynamics 365 Talent (2019 年 11 月 5 日) の新機能または変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 11/05/2019
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
ms.search.validFrom: 2019-11-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c4068cf81782d2f9559179b91da31e049c006059
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527123"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-5-2019"></a>Dynamics 365 Talent (2019 年 11 月 5 日) の新機能または変更された機能

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Dynamics 365 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。

## <a name="changes-in-onboard"></a>Onboard の変更

今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更

このセクションに記載された変更は、ビルド番号 8.1.2598 に適用されます。 ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。

### <a name="copy-a-core-hr-instance"></a>Core HR インスタンスのコピー

今週のリリースでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して、Microsoft Dynamics 365 Talent: Core HR のデータベースをサンドボックス環境にコピーすることができます。 別のサンドボックス環境を使用する場合は、その環境から対象のサンドボックス環境にデータベースをコピーすることもできます。 詳細については、以下を参照してください。

- Dynamics 365: 2019 リリース ウェーブ 2 プランの、[より広範な環境管理](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management)

- Talent のドキュメントに、[Core HR インスタンスをコピー](hr-copy-instance.md)

### <a name="common-data-service-integration-batch-jobs-arent-created-when-common-data-service-integration-is-enabled-388030"></a>Common Data Service 統合が有効になっている場合、Common Data Service統合バッチ ジョブが作成されない (388030)

この変更により、有効になったときに、Common Data Service 統合のバッチ ジョブが作成されます。

### <a name="the-hcmpersonimageentity-doesnt-resize-the-person-image-when-uploaded-369469"></a>HcmPersonImageEntity でアップロード時に従業員の画像サイズが変更されない (369469)

今週のリリースにより、パフォーマンス向上のため、データ管理を使用してインポートした際、画像サイズの変更方法が変わりました。

### <a name="a-positions-available-for-assignment-date-can-be-earlier-than-the-activation-date-340103"></a>職位の割り当て可能日が、有効化した日より以前になることがある (340103)

この変更により、職位が **有効化した日** より以前に **割り当て可能日** を選択した場合に警告が表示されるようになります。

### <a name="cant-create-a-compensation-change-request-in-employee-self-service-for-step-based-plans-376872"></a>ステップベースの計画では従業員セルフサービスで報酬変更要求を作成できない (376872)

このリリースにより、ステップベースの計画で従業員セルフサービスを使用して報酬の変更を要求する場合に発生する問題が修正されます。 

### <a name="reason-code-doesnt-sync-to-common-data-service-if-the-description-is-longer-than-30-characters-core-hr-allows-60-352682"></a>説明が 30 文字 (Core HR では 60 文字) を超えている場合、理由コードが Common Data Service に同期されない (352682)

この変更により、30 文字を超える理由コードが Common Data Service で更新されます。 Common Data Service で行われた変更は、Talent にも反映されます。

### <a name="address-integration-from-talent-to-finance-and-operations-351961"></a>Talent から Finance and Operations に対する住所の統合 (351961)

このリリースにより、Talent で更新された住所が Finance and Operations では更新されないという問題が修正されます。 住所のブロックに対する変更が更新されます。

## <a name="coming-soon"></a>間もなく公開

### <a name="print-performance-reviews"></a>業績の確認の印刷

詳細については、Dynamics 365: 2019 リリース ウェーブ 2 プランにある[業績の確認の印刷](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews)を参照してください。

### <a name="feature-management-workspace"></a>機能管理ワークスペース

機能は、すべてのリリースで追加および更新されます 機能管理エクスペリエンスは、各リリースで提供されている機能のリストを表示できるワークスペースを提供します。 既定では、新機能が無効になっています。 ワークスペースを使用してそれらを有効にし、それらのドキュメントを参照できます。

機能管理に伴う変更の詳細については、[機能管理の概要](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)を参照してください。


[!INCLUDE[footer-include](../includes/footer-banner.md)]