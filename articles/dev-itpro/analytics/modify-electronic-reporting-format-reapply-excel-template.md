---
title: "Excel テンプレートの再適用による電子申告形式の変更"
description: "このトピックでは、変更後の Excel テンプレートを再適用することによって、ビジネス ドキュメントを生成するために使用される電子レポート (ER) 形式を変更する方法に関する情報を提供します。"
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8707f7b184bb66648edd0e48672c5514a0a5caf1
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a>Excel テンプレートの再適用による電子申告形式の変更

[!include [banner](../includes/banner.md)]

電子申告 (ER) ツールを使用して、電子的な形式でビジネス ドキュメントを生成します。 ビジネス ドキュメントを生成するには、ER 形式を作成し、ER デザイナーを使用してビジネス ドキュメントのレイアウトを定義し、それに含まれるように、データを指定する必要があります。 ビジネス ドキュメントを生成するために ER 形式を実行できます。

Microsoft Excel ファイルとしてのビジネス ドキュメントを生成するために、ER ツールを使用することができます。 Excel ドキュメントは、これらのドキュメントをテンプレートとして使用できます。 ER デザイナーでのドキュメント レイアウトを定義するには、定義済みの ER 形式をテンプレートとして使用する Excel ドキュメントの内容をインポートできます。 このシナリオ実行の詳細については、**ER は、OPENXML 形式でレポートを生成するコンフィギュレーションを設計する** タスク ガイド (7.5.4.3 IT サービス / ソリューション コンポーネントの取得 / 開発 (10677) ビジネス プロセスの一部) を再生します。

ビジネス ドキュメントのテンプレートとして使用される Excel ドキュメントを編集する場合は、新しい ER 機能では、ER 形式に更新されたテンプレートを適用することができます。 更新されたテンプレートに準拠できるように、ER 形式が更新されます。 この機能の詳細については、**ER は Excel テンプレートの更新を反映して形式を変更する** (7.5.5.3取得/作成ITサービス/ソリューション コンポーネント (10683) 業務プロセスの一部) タスクガイドを再生してください。 更新されたテンプレートをインポートするタスクガイド ステップでは、支払レポート Excel ファイルの変更されたテンプレートである SampleVendPaymWsReport2 をテンプレートとして使用します。

