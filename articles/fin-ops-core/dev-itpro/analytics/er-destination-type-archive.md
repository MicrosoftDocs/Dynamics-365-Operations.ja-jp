---
title: ER アーカイブ送信先のタイプ
description: このトピックでは、送信ドキュメントを生成するようにコンフィギュレーションされている電子申告 (ER) 形式の各フォルダーまたはファイル コンポーネントに対して、アーカイブ送信先をコンフィギュレーションする方法に関する情報を提供します。
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
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
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8797a68507a5116c6adbf1f2d805838fa507958c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745588"
---
# <a name="archive-destination"></a>アーカイブ先

[!include [banner](../includes/banner.md)]

送信ドキュメントを生成するようにコンフィギュレーションされている電子申告 (ER) 形式の各フォルダーまたはファイル コンポーネントに対して、アーカイブ送信先をコンフィギュレーションできます。 送信先の設定に基づいて、生成されたドキュメントは ER ジョブ リストのレコードの添付ファイルとして保存されます。

このオプションを使用して、生成したドキュメントを Microsoft SharePoint フォルダーまたは Microsoft Azure ストレージに送信することができます。 **有効** を **はい** に設定し、選択したドキュメント タイプで定義されている変換先に出力を送信します。 グループが**ファイル**に設定されているドキュメントタイプのみ選択できます。 **組織管理** \> **ドキュメント管理** \> **ドキュメント タイプ**で、ドキュメント [タイプ](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) を定義します。 電子申告の送信先への構成は、ドキュメント管理システムの構成と同じです。

[![ドキュメント タイプ ページ](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

場所は、ファイルの保存場所を決定します。 **アーカイブ**先を有効にすると、結果をジョブ アーカイブに保存できます。 結果は、**組織管理** \> **電子申告** \> **電子申告アーカイブ済ジョブ** で表示できます。

> [!NOTE]
> ジョブ アーカイブのドキュメント タイプは、**組織管理** \> **ワークスペース** \> **電子申告** \> **電子申告のパラメーター**に移動して選択します。 詳細については、[電子申告 (ER) フレームワークのコンフィギュレーション](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup) を参照してください。

## <a name="sharepoint"></a>SharePoint

指定された SharePoint フォルダーにファイルを保存することができます。 既定の SharePoint サーバーを定義するには、**組織管理** \> **ドキュメント管理** \> **ドキュメント管理パラメーター**に移動します。 **SharePoint** タブで、SharePoint フォルダーをコンフィギュレーションします。 ER 出力を保存するフォルダーとして選択できます。 **SharePoint** の場所は、このドキュメント タイプで選択する必要があります。

[![SharePoint フォルダーの選択](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>Azure ストレージ

ドキュメント タイプの場所を **Azure ストレージ**に設定すると、Azure ストレージにファイルを保存することができます。

## <a name="additional-resources"></a>追加リソース

- [電子申告 (ER) の概要](general-electronic-reporting.md)
- [電子申告 (ER) の送信先](electronic-reporting-destinations.md)
- [ドキュメント管理のコンフィギュレーション](../../fin-ops/organization-administration/configure-document-management.md)
