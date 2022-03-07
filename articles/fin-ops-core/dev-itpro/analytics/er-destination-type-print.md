---
title: ER プリンター送信先のタイプ
description: このトピックでは、電子申告 (ER) 形式の各フォルダーまたはファイル コンポーネントに対してプリンター出力先を構成する方法について説明します。
author: NickSelin
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 7749a458020de664d00e81ccf0e480ae459da617
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894007"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>プリンター出力先

[!include [banner](../includes/banner.md)]

直接印刷のために生成されたドキュメントをネットワーク プリンターに直接送信できます。

## <a name="prerequisites"></a>必要条件

開始する前に、ドキュメント回覧エージェントのインストールおよびコンフィギュレーションを行い、ネットワーク プリンターを登録する必要があります。 詳細については、 [ドキュメント ルーティング エージェントをインストールしてネットワーク印刷を有効にする](./install-document-routing-agent.md) を参照してください。

## <a name="make-the-printer-destination-available"></a>プリンター送信先を利用可能にする

Microsoft Dynamics 365 Finance の現在のインスタンスで **プリンター** 送信先を利用可能にするには、**機能管理** ワークスペースに移動して、順序どおりに次の機能を有効にします。

1. Microsoft Office 形式から PDF に電子申告送信ドキュメントを変換する
2. 送信ドキュメントの電子申告の送信先としてのドキュメント回覧エージェント

[![機能管理で ER プリンター送信先機能を有効にする](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>適合性

**プリンター** 送信先は、印刷可能な PDF 形式 (PDF 合併または PDF ファイル形式の要素) または Microsoft Office Excel/Word 形式 (Excel ファイル) のいずれかで出力を生成するために使用されるファイル コンポーネントに対してのみコンフィギュレーションできます。 出力が PDF 形式で生成された場合、プリンターに送信されます。 出力が Microsoft Office 形式で生成された場合、自動的に PDF 形式に変換され、プリンターに送信されます。

### <a name="limitations"></a>制限

**印刷** 送信先は、クラウド配置に対してのみ実装されます。

### <a name="use-the-printer-destination"></a>印刷送信先の使用

1. 生成されたドキュメントをプリンターに送信するには、**有効** オプションを **Yes** に設定します。
2. **プリンター名** フィールドで、必要なネットワーク プリンターを選択します。
3. **印刷アーカイブに保存しますか?** オプションを **はい** に設定して生成された出力を印刷アーカイブに保存することにより、さらに印刷できるようになります。 後でアーカイブ出力にアクセスするには、**組織管理** \> **照会およびレポート** \> **レポート アーカイブ** に移動します。

[![プリンター送信先の使用](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> **プリンター** 送信先をコンフィギュレーションする場合、**PDF への変換** オプションを有効にする必要はありません。 印刷目的のための PDF 変換は、オプションが無効になっていても実行されます。

送信ドキュメントを Excel 形式で印刷する際に特定の [ページの向き](electronic-reporting-destinations.md#SelectPdfPageOrientation) を使用するには、**PDF に変換する** オプションを有効にする必要があります。 **PDF に変換する** オプションを **はい** に設定すると、**ページの向き** フィールドが使用できるようになります。 **ページの方向** フィールドで、ページの向きを選択することができます。

## <a name="additional-resources"></a>追加リソース

- [電子申告 (ER) の概要](general-electronic-reporting.md)
- [電子申告 (ER) の送信先](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]