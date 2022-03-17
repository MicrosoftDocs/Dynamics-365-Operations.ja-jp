---
title: ER プリンター送信先のタイプ
description: このトピックでは、電子申告 (ER) 形式の各フォルダーまたはファイル コンポーネントに対してプリンター出力先を構成する方法について説明します。
author: NickSelin
ms.date: 02/14/2022
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
ms.openlocfilehash: 2513fc4f86519c71602089cd46e9757813b1a708
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388291"
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

[![機能管理で ER プリンター送信先機能を有効にする。](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>適用性

#### <a name="pdf-printing"></a>PDF の印刷

財務のバージョン10.0.18 以前では、**プリンター** 送信先は、印刷可能な PDF 形式 (**PDF 合併** または **PDF ファイル** 形式の要素) または Microsoft Office Excel と Word 形式 (**Excel ファイル**) のいずれかで出力を生成するために使用されるファイル コンポーネントに対してのみ構成できます。 出力が PDF 形式で生成された場合、プリンターに送信されます。 出力が **Excel ファイル** を使用した Office 形式要素で生成された場合、自動的に PDF 形式に変換され、プリンターに送信されます。

ただし、バージョン10.0.18 では、**共通ファイル** 形式要素用に **プリンター** 出力先を構成できます。 ほとんどの場合、この形式要素は、TXT 形式または XML 形式で出力を生成するために使用されます。 ルート形式要素として **共通ファイル** 形式要素を含む ER 形式を、その下に入れ子になった唯一の要素として **バイナリ コンテンツ** 形式要素を構成できます。 この場合、**共通ファイル** のファイル形式の要素により、**バイナリ コンテンツ** 形式要素に対して構成するバインドで指定された形式で出力が生成されます。 たとえば、PDF または Office (Excel または Word) 形式の [ドキュメント管理](../../fin-ops/organization-administration/configure-document-management.md) の添付ファイルの内容をこの要素に [含める](tasks/er-document-management-files-5.md#modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format) 場合、このバインドを構成できます。 出力は、構成されている [プリンタ] 出力先を使用して **出力** できます。 

> [!NOTE]
> **プリンター** の出力先を構成するために **共通\\ファイル** 形式要素を選択した場合、選択した要素によって PDF 形式に変換可能な PDF 形式またはプリンター 出力が生成さることが設計時に保証する方法がありません。 したがって、次の警告メッセージが表示されます: "選択した形式のコンポーネントによって生成された出力が PDF に変換可能であることを確認してください。 オフの場合は、'PDFに変換' オプションをオフにします。 実行時に印刷するために PDF 以外の出力または PDF 以外の出力が提供される場合は、実行時の問題を回避するための対策をとる必要があります。 Office (ExcelまたはWord) 形式の出力を受け取る場合は **PDF に変換** オプションを選択する必要があります。
>
> バージョン 10.0.26 以降で **PDF に変換** オプションを使用するには、構成されている **プリンター** 出力先の **ドキュメント ルート設定タイプ** パラメータに **PDF** を選択する必要があります。

#### <a name="zpl-printing"></a>ZPL の印刷

バージョン 10.0.26 以降では、**ドキュメント ルート設定タイプ** パラメータに **ZPL** を選択することで、**共通\\ファイル** フォーマット要素の **プリンター** 送信先を構成できます。 この場合、**PDF に変換** オプションは実行時に無視され、TXT または XML の出力は、[ドキュメント ルート設定 エージェント (DRA)](install-document-routing-agent.md) の  Zebra プログラム言語 (ZPL) 契約を使用して、選択したプリンタに直接送信されます。 この機能は、ZPL II ラベル レイアウトを表す ER 形式で、さまざまなラベルを印刷するために使用します。

[!["宛先の設定" ダイアログ ボックスでドキュメントのルーティング タイプ のパラメータを設定する。](./media/ER_Destinations-SetDocumentRoutingType.png)](./media/ER_Destinations-SetDocumentRoutingType.png)

この機能の詳細については、[ZPL ラベルを印刷する新しい ER ソリューションのデザイン](er-design-zpl-labels.md) を参照してください。

### <a name="limitations"></a>制限

**印刷** 送信先は、クラウド配置に対してのみ実装されます。

### <a name="use-the-printer-destination"></a>印刷送信先の使用

1. 生成されたドキュメントをプリンターに送信するには、**有効** オプションを **Yes** に設定します。
2. **プリンター名** フィールドで、必要なネットワーク プリンターを選択します。
3. **印刷アーカイブに保存しますか?** オプションを **はい** に設定して生成された出力を印刷アーカイブに保存することにより、さらに印刷できるようになります。 後でアーカイブ出力にアクセスするには、**組織管理** \> **照会およびレポート** \> **レポート アーカイブ** に移動します。

[![プリンター送信先の使用。](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> **プリンター** 送信先をコンフィギュレーションする場合、**PDF への変換** オプションを有効にする必要はありません。 印刷目的のための PDF 変換は、オプションが無効になっていても実行されます。

送信ドキュメントを Excel 形式で印刷する際に特定の [ページの向き](electronic-reporting-destinations.md#SelectPdfPageOrientation) を使用するには、**PDF に変換する** オプションを有効にする必要があります。 **PDF に変換する** オプションを **はい** に設定すると、**ページの向き** フィールドが使用できるようになります。 **ページの方向** フィールドで、ページの向きを選択することができます。

## <a name="additional-resources"></a>追加リソース

- [電子申告 (ER) の概要](general-electronic-reporting.md)
- [電子申告 (ER) の送信先](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
