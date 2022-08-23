---
title: Power BI ER 送信先タイプ
description: この記事では、送信ドキュメントに対して Power BI ER 送信先タイプを構成する方法について説明します。
author: kfend
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 10.0.09
ms.custom: 97423
ms.assetid: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: 8d167d6749e2f05f1e263839260dfdb563d2bbea
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285368"
---
# <a name="power-bi-destination"></a>Power BI 出力先

[!include [banner](../includes/banner.md)]

送信ドキュメントを生成するようにコンフィギュレーションされている電子申告 (ER) 形式の各フォルダーまたはファイル コンポーネントに対して、Microsoft Power BI 送信先をコンフィギュレーションできます。 送信先の設定に基づいて、生成されたドキュメントは以前にコンフィギュレーションされた SharePoint フォルダーに保存されます。

**有効** を **はい** に設定し、ER 構成を使用して Dynamics 365 Finance インスタンスから Microsoft Power BI サービスへのデータ転送を調整します。 転送されたファイルは、その目的にコンフィギュレーションされている Microsoft SharePoint Server インスタンスに保存されます。 詳細については、[データを Power BI にプルする電子申告 (ER) の構成](general-electronic-reporting-report-configuration-get-data-powerbi.md)を参照してください。

[![送信先の設定ページ。](./media/ER_Destinations-EnablePowerBIDestination.png)](./media/ER_Destinations-EnablePowerBIDestination.png)

## <a name="additional-resources"></a>追加リソース

- [電子申告 (ER) の概要](general-electronic-reporting.md)
- [電子申告 (ER) の送信先](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
