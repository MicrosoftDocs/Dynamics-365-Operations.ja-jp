---
title: ER プリンター送信先のタイプ
description: このトピックでは、PDF または Microsoft Office 形式 (Excel\Word) で送信ドキュメントを生成するようにコンフィギュレーションされている電子申告 (ER) 形式の各フォルダーまたはファイル コンポーネントに対して、プリンター送信先をコンフィギュレーションする方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 01/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 58e067baa130458e3a8e788d978604f208140a03
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019867"
---
# <a name="PrinterDestinationType"></a>プリンター出力先

[!include [banner](../includes/banner.md)]

直接印刷のために生成されたドキュメントをネットワーク プリンターに直接送信できます。

## <a name="prerequisites"></a>必要条件

開始する前に、ドキュメント回覧エージェントのインストールおよびコンフィギュレーションを行い、ネットワーク プリンターを登録する必要があります。 詳細については、 [ドキュメント ルーティング エージェントをインストールしてネットワーク印刷を有効にする](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent) を参照してください。

## <a name="make-the-printer-destination-available"></a>プリンター送信先を利用可能にする

Microsoft Dynamics 365 Finance の現在のインスタンスで**プリンター**送信先を利用可能にするには、**機能管理**ワークスペースに移動して、順序どおりに次の機能を有効にします。

1. Microsoft Office 形式から PDF に電子申告送信ドキュメントを変換する
2. 送信ドキュメントの電子申告の送信先としてのドキュメント回覧エージェント

[![機能管理で ER プリンター送信先機能を有効にする](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>適合性

**プリンター**送信先は、印刷可能な PDF 形式 (PDF 合併または PDF ファイル形式の要素) または Microsoft Office Excel/Word 形式 (Excel ファイル) のいずれかで出力を生成するために使用されるファイル コンポーネントに対してのみコンフィギュレーションできます。 出力が PDF 形式で生成された場合、プリンターに送信されます。 出力が Microsoft Office 形式で生成された場合、自動的に PDF 形式に変換され、プリンターに送信されます。

### <a name="limitations"></a>制限

この機能はプレビュー機能で、[Microsoft Dynamics 365 プレビューの追加使用条件](https://go.microsoft.com/fwlink/?linkid=2105274) で説明されている使用条件に従います。

**印刷**送信先は、クラウド配置に対してのみ実装されます。

### <a name="use-the-printer-destination"></a>印刷送信先の使用

1. 生成されたドキュメントをプリンターに送信するには、**有効**オプションを **Yes** に設定します。
2. **プリンター名**フィールドで、必要なネットワーク プリンターを選択します。
3. **印刷アーカイブに保存しますか?** オプションを**はい**に設定して生成された出力を印刷アーカイブに保存することにより、さらに印刷できるようになります。 後でアーカイブ出力にアクセスするには、**組織管理** \> **照会およびレポート** \> **レポート アーカイブ**に移動します。

[![プリンター送信先の使用](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> **プリンター**送信先をコンフィギュレーションする場合、**PDF への変換**オプションを有効にする必要はありません。 印刷目的のための PDF 変換は、オプションが無効になっていても実行されます。

## <a name="additional-resources"></a>追加リソース

- [電子申告 (ER) の概要](general-electronic-reporting.md)
- [電子申告 (ER) の送信先](electronic-reporting-destinations.md)
