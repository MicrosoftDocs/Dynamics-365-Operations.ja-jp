---
title: ER アーカイブ送信先のタイプ
description: このトピックでは、電子申告 (ER) 形式の各フォルダーまたはファイル コンポーネントに対してアーカイブ送信先を構成する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 11/30/2020
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
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 72b896ca692a54200ff79b14d0b5dc6ab4b0fe27
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562049"
---
# <a name="archive-er-destination-type"></a>ER アーカイブ送信先のタイプ

[!include [banner](../includes/banner.md)]

送信ドキュメントを生成するようにコンフィギュレーションされている電子申告 (ER) 形式の各 **フォルダー** または **ファイル** コンポーネントに対して、アーカイブ送信先をコンフィギュレーションできます。 送信先の設定に基づいて、生成されたドキュメントは ER ジョブ リストのレコードの添付ファイルとして保存されます。 結果を表示するには、**組織管理** \> **電子申告** \> **電子申告ジョブ** に移動します。

このオプションを使用して、生成したドキュメントを Microsoft SharePoint フォルダーまたは Microsoft Azure ストレージに送信することができます。 **有効** を **はい** に設定し、選択したドキュメント タイプで定義されている変換先に出力を送信します。 グループが **ファイル** に設定されているドキュメントタイプのみ選択できます。 **組織管理** \> **ドキュメント管理** \> **ドキュメント タイプ** で、ドキュメント [タイプ](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) を定義します。 電子申告の送信先への構成は、ドキュメント管理システムの構成と同じです。

[![ドキュメント タイプ ページ](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

場所は、ファイルの保存場所を決定します。 **アーカイブ** 先を有効にすると、結果をジョブ アーカイブに保存できます。 結果は、**組織管理** \> **電子申告** \> **電子申告アーカイブ済ジョブ** で表示できます。

> [!NOTE]
> ジョブ アーカイブのドキュメント タイプは、**組織管理** \> **ワークスペース** \> **電子申告** \> **電子申告のパラメーター** に移動して選択します。 詳細については、[電子申告 (ER) フレームワークのコンフィギュレーション](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup) を参照してください。

## <a name="sharepoint"></a>SharePoint

指定された SharePoint フォルダーにファイルを保存することができます。 既定の SharePoint サーバーを定義するには、**組織管理** \> **ドキュメント管理** \> **ドキュメント管理パラメーター** に移動します。 **SharePoint** タブで、SharePoint フォルダーをコンフィギュレーションします。 ER 出力を保存するフォルダーとして選択できます。 **SharePoint** の場所は、このドキュメント タイプで選択する必要があります。

[![SharePoint フォルダーの選択](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>Azure ストレージ

ドキュメント タイプの場所を **Azure ストレージ** に設定すると、Azure ストレージにファイルを保存することができます。

> [!NOTE] 
> ER フレームワークは、処理する必要があるドキュメントに対して、7 日間の保持ポリシーを適用するデータ管理フレームワークとは異なり、Azure Blob Storage にファイルを永久に保存します。 詳細については、[メッセージ状態を取得中の API](../data-entities/recurring-integrations.md#api-for-getting-message-status) および [ステータス チェック API](../data-entities/data-management-api.md#status-check-api) を参照してください。 ER 関連のファイルは、必要な限り、アプリケーション テーブル レコードの添付ファイルとし、Azure Blob Storage に保存されます。 1 つのファイルが、このファイルが関連付けられているアプリケーション テーブル レコードと共に、Azure Blob Storage から削除されます。

## <a name="additional-resources"></a>追加リソース

- [電子申告 (ER) の概要](general-electronic-reporting.md)
- [電子申告 (ER) の送信先](electronic-reporting-destinations.md)
- [ドキュメント管理のコンフィギュレーション](../../fin-ops/organization-administration/configure-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]