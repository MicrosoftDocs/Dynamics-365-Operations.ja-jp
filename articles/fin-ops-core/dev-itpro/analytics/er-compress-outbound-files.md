---
title: 電子申告で生成される大きなドキュメントを圧縮する
description: このトピックでは、電子申告 (ER) 形式で生成される大きなドキュメントを圧縮する方法について説明します。
author: NickSelin
manager: kfend
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner, ERFormatDestinationTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 30de55f9e55911290750c148621fd3d4531686c2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680857"
---
# <a name="compress-large-documents-that-are-generated-in-electronic-reporting"></a>電子申告で生成される大きなドキュメントを圧縮する 

[!include [banner](../includes/banner.md)]

[電子報告 (ER) フレームワーク](general-electronic-reporting.md) を使用すると、トランザクション データをフェッチして、送信ドキュメントを生成するソリューションを構成できます。 この生成されたドキュメントは非常に大きい場合があります。 このタイプのドキュメントが生成されると、[Application Object Server (AOS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/access-instances#location-of-packages-source-code-and-other-aos-configurations) メモリを使用して保持されます。 ある時点で、ドキュメントを Microsoft Dynamics 365 Finance アプリケーションからダウンロードする必要があります。 現在、ER で生成される 1 つのドキュメントの最大サイズは 2 ギガバイト (GB) に制限されています。 また、Finance では現在、ダウンロード ファイルのサイズを 1 GB に [制限](https://fix.lcs.dynamics.com/Issue/Details?bugId=489291) しています。 したがって、これらの制限を超えて、**ストリームが長すぎる** または **算術演算におけるオーバーフローまたはアンダーフロー** 例外を受け取る可能性を低くする、ER ソリューションを構成する必要があります。

ソリューションを構成するときに、**フォルダー** タイプのルート要素を追加して、入れ子になった要素によって生成されるコンテンツを圧縮することによって、オペレーション デザイナーで ER 形式を調整できます。 圧縮は、"ジャスト イン タイム" で機能するため、ピーク時のメモリ使用量とダウンロードされるファイルのサイズを減らすことができます。

> [!NOTE]
> ファイルの圧縮には、CPU 使用率の追加割合がかかります。

このアプローチの詳細については、このトピックの例を完了してください。

## <a name="example-compress-an-outbound-document"></a>例: 送信ドキュメントの圧縮

この例では、**システム管理者** または **電子申告機能コンサルタント** のロールに割り当てられたユーザーが、ER 形式を構成して、生成されたドキュメントを圧縮できるようにする方法を示します。

### <a name="prerequisites"></a>必要条件

このトピックの手順を完了する前に、次の手順を完了する必要があります。

1. [構成プロバイダーをアクティブにします](er-defer-xml-element.md#activate-a-configuration-provider)。
2. [サンプル ER のコンフィギュレーションのインポート](er-defer-xml-element.md#import-the-sample-er-configurations)。
3. [インポートされた形式を確認する](er-defer-xml-element.md#review-the-imported-format)。

> [!NOTE]
> 現在、形式構造は、**ファイル** タイプの **レポート** 要素から始まり、XML 要素を含んでいます。 したがって、送信ドキュメントは XML 形式で生成され、圧縮は使用されません。

### <a name="generate-an-er-format-to-get-an-uncompressed-document"></a>非圧縮ドキュメントを取得するための ER 形式の生成

1. [インポートされた形式の実行](er-defer-xml-element.md#run-the-imported-format)。
2. XML 形式で生成されたドキュメントのサイズが 3 キロバイト (KB) であることに注意してください。

    ![非圧縮送信ドキュメントのプレビュー](./media/er-compress-outbound-files1.png)

### <a name="modify-the-format-to-compress-the-generated-output"></a>生成された出力を圧縮するように形式を変更する

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **コンフィギュレーション** ページのコンフィギュレーション ツリーで、**遅延要素を知るためのモデル** を展開します。
3. **遅延 XML 要素を知るための形式** コンフィギュレーションを選択します。
4. **デザイナー** を選択して、形式構造を変更します。
5. **形式デザイナー** ページの **形式** タブで **ルートの追加** を選択し、ルート形式要素を追加します。
6. **追加** ダイアログ ボックスで、**Common\\Folder** を選択します。
7. **OK** を選択して、新しいルート要素の追加を確認します。
8. **保存** を選択します。

> [!NOTE]
> 形式構造は、**フォルダー** タイプの要素から始まります。 この要素は、出力を圧縮 (zip) ファイルとして生成します。 **レポート** 要素によって生成されたドキュメントが送信 ZIP ファイルに配置されると、送信ファイルのサイズを縮小するためにそのコンテンツが圧縮されます。

### <a name="generate-an-er-format-to-get-a-compressed-document"></a>圧縮ドキュメントを取得するための ER 形式の生成

1. **フォーマット デザイナー** ページで、**実行** を選択します。
2. Web ブラウザーが提供する ZIP ファイルをダウンロードし、レビュー用に開きます。
3. ZIP 形式で生成されたドキュメントのサイズが 1 KB であることに注意してください。

    > [!NOTE] 
    > この ZIP ファイルが保持する XML ファイルの圧縮率は 87% です。 圧縮率は、圧縮するデータによって異なります。

    ![圧縮送信ドキュメントのプレビュー](./media/er-compress-outbound-files2.png)

> [!NOTE]
> 出力を生成する形式要素 (この例では **レポート** 要素) に ER [出力先](electronic-reporting-destinations.md) が構成されている場合、出力の圧縮がバイパスされます。

## <a name="additional-resources"></a>追加リソース

[電子申告 (ER) の概要](general-electronic-reporting.md)

[電子申告 (ER) の送信先](electronic-reporting-destinations.md)

[電子申告形式における XML 要素の実行の延期](er-defer-xml-element.md)
