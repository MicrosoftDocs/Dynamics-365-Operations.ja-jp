---
title: Excel テンプレートを再適用して電子申告形式を変更する
description: このトピックでは、変更後の Excel テンプレートを再適用することによって、ビジネス ドキュメントを生成するために使用される電子レポート (ER) 形式を変更する方法に関する情報を提供します。
author: NickSelin
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 626450b05789c93f63675a55e050649c862c86f6
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811395"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a>Excel テンプレートの再適用による電子申告形式の変更

[!include [banner](../includes/banner.md)]

電子申告 (ER) ツールを使用して、電子的な形式でビジネス ドキュメントを生成します。 ビジネス ドキュメントを生成するには、ER 形式を作成し、ER デザイナーを使用してビジネス ドキュメントのレイアウトを定義し、それに含まれるように、データを指定する必要があります。 ビジネス ドキュメントを生成するために ER 形式を実行できます。

Microsoft Excel ファイルとしてのビジネス ドキュメントを生成するために、ER ツールを使用することができます。 Excel ドキュメントは、これらのドキュメントをテンプレートとして使用できます。 ER デザイナーでのドキュメント レイアウトを定義するには、定義済みの ER 形式をテンプレートとして使用する Excel ドキュメントの内容をインポートできます。 このシナリオ実行の詳細については、**ER は、OPENXML 形式でレポートを生成するコンフィギュレーションを設計する** タスク ガイド (7.5.4.3 IT サービス / ソリューション コンポーネントの取得 / 開発 (10677) ビジネス プロセスの一部) を再生します。 Excel テンプレートをインポートするタスク ガイドの手順では、支払レポート Excel ファイルの初期テンプレート [SampleVendPaymWsReport](https://download.microsoft.com/download/e/6/b/e6bb79f0-cc08-44af-96fa-49c7929d4fb8/SampleVendPaymWsReport.xlsx) を使用します。

ビジネス ドキュメントのテンプレートとして使用される Excel ドキュメントを編集する場合は、新しい ER 機能では、ER 形式に更新されたテンプレートを適用することができます。 更新されたテンプレートに準拠できるように、ER 形式が更新されます。 この機能の詳細については、**ER は Excel テンプレートの更新を反映して形式を変更する** (7.5.5.3取得/作成ITサービス/ソリューション コンポーネント (10683) 業務プロセスの一部) タスクガイドを再生してください。 更新されたテンプレートをインポートするタスク ガイドの手順では、支払レポート Excel ファイルの変更されたテンプレート [SampleVendPaymWsReport2](https://download.microsoft.com/download/3/1/0/3104d397-c9c5-4227-b68e-f98625313801/SampleVendPaymWsReport2.xlsx) を使用します。

## <a name="additional-resources"></a>追加リソース

[テンプレートの更新](er-fillable-excel.md#update-a-template)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
