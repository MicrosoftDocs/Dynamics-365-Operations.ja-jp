---
title: 組み込みのマスター プラン エンジンを実行するとエラーが表示されます
description: 非推奨の組み込みのマスター プラン エンジンを実行するとエラー メッセージが表示されます。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c950292a4f43319d21a7deafdfb341b7bef15d8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294120"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a>組み込みのマスター プラン エンジンを実行するとエラーが表示されます

エラー コード: ReqCalcScheduleItemTablePlanningOptimizationFitError

## <a name="symptoms"></a>現象

非推奨の組み込みを使用してマスター プランを実行すると次のエラー メッセージが表示されます。

> このエラー メッセージが表示されるのは、組み込みマスター プラン エンジンが、計画の最適化によってサポートされているシナリオに使用されたためです。 現在の組み込みのマスター プランは非推奨であるため、今すぐ計画の最適化に移行する必要があります。 このマスター プランの実行が正常に完了したことを確認します。 移行が保留中の機能に強い依存関係がある場合は、組み込みのマスター プラン エンジンの使用を継続することはできません。 次のアンケートに記入して開始し、必要に応じて、計画の最適化への移行に関連する例外を要求してください。 [計画の最適化の移行と例外に関するアンケート](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a>原因

計画を実行し、製造制御機能を使用しない場合は、計画の最適化への移行を考慮する必要があります。 組み込みのマスター プラン エンジンは非推奨になります。 したがって、エラー メッセージを受け取ることなしに引き続き使用するには、Microsoft からの例外を適用する必要があります。

## <a name="resolution"></a>解決策

計画の最適化に移行する方法の詳細、または例外を適用して非推奨の組み込みのプラン エンジンを引き続き使用できるようにする方法についての詳細については、[マスター プランの計画の最適化への移行](/dynamics365/supply-chain/master-planning/new-master-planning-engine) を参照してください。
