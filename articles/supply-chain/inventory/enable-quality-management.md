---
title: 品質および不適合管理の有効化
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management の品質および不適合管理機能を設定および構成するプロセスの概要を説明します。
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c2c8b7e9a1a8d7692e1d2215e38de1b0f4d2d82
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567418"
---
# <a name="enable-quality-and-nonconformance-management"></a>品質および不適合管理の有効化

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management の品質および不適合管理機能を設定および構成するプロセスの概要を説明します。

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a>品質および不適合管理の有効化

次の手順に従って、システムの品質管理を有効にします。

1. **在庫管理 \> 設定 \> 在庫および倉庫管理パラメーター** の順に移動します。
1. **品質管理** タブで、**品質管理の使用** オプションを *はい* に設定します。
1. **時間レート** フィールドに、国内通貨で時給レートを入力します。 時給レートは、不適合に関連する工程の原価計算に使用されます。 時間あたりのレートと算出原価は、不適合の参照情報を提供するものです。 これらは、他の機能に作用することはありません。
1. **レポート設定** を選択します。
1. さまざまなレポート タイプの新しい行を追加し、各レポートで使用するドキュメントのタイプを選択します。
1. ページを閉じます。
1. ページを閉じます。

## <a name="quality-management-configuration-process"></a>品質管理の構成プロセス

品質管理機能を使用し、品質指示を生成する前に、システムおよび前提条件を構成する必要があります。 ここでは、品質管理を構成するために必要な手順の一覧を示します。

1. [品質および不適合管理を有効にします](#enable-qm)。
1. オプション : [テスト機器を構成します](quality-test-instruments.md)。
1. [テストを構成します](quality-tests.md)。
1. [テスト変数と結果を構成します](quality-test-variables.md)。
1. [テスト グループを構成します](quality-test-groups.md)。
1. オプション : [品質グループを構成し、製品にリンクします](quality-groups.md)。
1. オプション : [品質アソシエーションを構成します](quality-associations.md)。

構成が完了したら、品質指示の作成と処理を開始できます。 品質指示の作成および使用方法の詳細については、[品質指示](quality-orders.md) を参照してください。

## <a name="nonconformance-management-configuration-process"></a>不適合管理の構成プロセス

不適合管理機能を使用し、不適合を生成する前に、システムおよび前提条件を構成する必要があります。 ここでは、不適合管理を構成するために必要な手順の一覧を示します。

1. [品質および不適合管理を有効にします](#enable-qm)。
1. [不適合の承認を担当する作業者を構成します](quality-responsible-workers.md)。
1. [問題タイプを構成します](quality-problem-types.md)。
1. [検査ゾーンを構成します](quality-quarantine-zones.md)。
1. [診断タイプを構成します](quality-diagnostic-types.md)。
1. [操作を構成します](quality-operations.md)。
1. オプション : [品質諸費用を構成します](quality-charges.md)。

構成が完了したら、不適合の作成と処理を開始できます。 不適合を作成し使用する方法の詳細については、「[不適合の作成および処理](tasks/create-process-non-conformance.md)」を参照してください。

## <a name="additional-resources"></a>追加リソース

- [品質管理の概要](quality-management-processes.md)
- [品質および不適合管理の有効化](enable-quality-management.md)
- [倉庫プロセスに対する品質管理](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
