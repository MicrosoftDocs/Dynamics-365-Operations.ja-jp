---
title: Talent システム要件と更新ポリシー
description: このトピックは、Dynamics 365 for Talent の要件を一覧表示します。 同様に、その更新ポリシーについても説明します。
author: andreabichsel
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 2389f00b22ec3b5284eeffb2c015533b7a3d13e0
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/19/2019
ms.locfileid: "856304"
---
# <a name="talent-system-requirements-and-update-policy"></a>Talent システム要件と更新ポリシー

[!include [banner](includes/banner.md)]

このトピックは、Microsoft Dynamics 365 for Talent の要件を一覧表示します。 同様に、その更新ポリシーについても説明します。

## <a name="supported-web-browsers"></a>サポートされている Web ブラウザー

Microsoft Dynamics 365 for Talent Web アプリケーションは、指定されたオペレーティング システムで実行される次のすべての Web ブラウザで実行できます。 

*   Windows 10 の Microsoft Edge (公開されている最新のバージョン)
*   Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11
*   Google Chrome (公開されている最新バージョン)
*   Apple Safari (公開されている最新バージョン)

各 Web ブラウザの最新版を検索するには、ソフトウェア メーカーの Web サイトに移動します。 

> [!NOTE]
> * タスク レコーダーから生成される画像をキャプチャして Microsoft Word ドキュメントに含めるには、Chrome 拡張機能をインストールする必要があります。 
> * ワークフロー エディターは ClickOnce アプリケーションとして起動されます。 Microsoft Edge と Internet Explorer (Microsoft Windows のサポートされているバージョン) のみが、ClickOnce アプリケーションをサポートします。 ワークフロー エディタ ClickOnce アプリケーションには、64 ビットの互換性のあるオペレーティング システムが必要です。
> * PDF ファイルをプレビューするには、Windows 10 の Microsoft Edge (公開されている最新のバージョン)、もしくは Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン) などの最新のブラウザを使用することをお勧めします。
>   ネットワーク要件
> * Dynamics 365 for Talent は、待機時間が 250 ～ 300 ミリ秒 (ms) 以下のネットワーク用に設計されています。 これは、ブラウザー クライアントから Dynamics 365 for Talent をホストする Microsoft Azure データ センターまでの待機時間のことです。 [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test") でネットワーク待機時間をテストすることをお勧めします。
> * Dynamics 365 for Talent に対する帯域幅の要件は、シナリオによって異なります。 最も一般的なシナリオでは、毎秒 50 キロバイト (KBps) 以上の帯域幅が必要です。
> 
> [!WARNING]
> ユーザー数に帯域幅要件の最小値を掛けてクライアントの場所からの帯域幅要件を計算しないでください。 特定の場所の同時使用は非常に計算が困難です。 帯域幅の要件について懸念する顧客には、Dynamics 365 for Talent のトライアル バージョンを使用します。

## <a name="supported-microsoft-office-applications"></a>サポートされる Microsoft Office アプリケーション

* Microsoft Excel と Word のアドインを実行するには、Windows または Mac 用の Microsoft Office 2016 をインストールしておく必要があります。 バージョン要件の詳細については、[Office 統合トラブルシューティング](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office 統合トラブルシューティング") を参照してください。
* Excel にエクスポートまたはWord にエクスポート機能によって生成されたドキュメントを表示するには、Microsoft Office 2007 以降をインストールしておく必要があります。

## <a name="update-policy"></a>更新ポリシー

Microsoft Dynamics 365 for Talent はクラウドの提供としてサービスされます。 Dynamics 365 for Talent の更新は、Microsoft によって連続的かつ自動的に適用されます。

更新プログラムは一定の調子でリリースされ、すべての環境で行われます。  Dynamics 365 for Talent は、[Microsoft Support Lifecycle ポリシー](https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle") に従ってサポートされています。ここでは、製品サポートの使用可能性における一貫した予測可能なガイドラインを提供します。
