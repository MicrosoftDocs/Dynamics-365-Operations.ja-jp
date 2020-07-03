---
title: システム要件
description: この記事では、Microsoft Dynamics 365 Human Resources の要件について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f68b8f642ada1345e7097b5e7220e222b132b1dd
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431156"
---
# <a name="system-requirements"></a>システム要件

この記事では、Microsoft Dynamics 365 Human Resources の要件について説明します。 また、人事管理が利用可能な国および地域、および人事管理データの言語とローカライズの概要について説明します。

## <a name="supported-web-browsers"></a>サポートされている Web ブラウザー

人事管理は、指定されたオペレーティング システムで実行される次のすべての Web ブラウザで実行できます。 

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
> * 人事管理は、待機時間が 250 ～ 300 ミリ秒 (ms) 以下のネットワーク用に設計されています。 これは、ブラウザー クライアントから人事管理をホストする Microsoft Azure データ センターまでの待機時間のことです。 [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test") にてネットワークの待機時間をテストすることをお勧めします。
> * 人事管理に対する帯域幅の要件は、シナリオによって異なります。 最も一般的なシナリオでは、毎秒 50 キロバイト (KBps) 以上の帯域幅が必要です。
> 
> [!WARNING]
> ユーザー数に帯域幅要件の最小値を掛けてクライアントの場所からの帯域幅要件を計算しないでください。 特定の場所の同時使用は非常に計算が困難です。 帯域幅の要件について懸念する顧客には、人事管理のトライアル バージョンを使用します。

## <a name="supported-microsoft-office-applications"></a>サポートされる Microsoft Office アプリケーション

* Microsoft Excel と Word のアドインを実行するには、Windows または Mac 用の Microsoft Office 2016 をインストールしておく必要があります。 バージョン要件の詳細については、[Office 統合トラブルシューティング](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office 統合のトラブルシューティング") を参照してください。
* Excel にエクスポートまたはWord にエクスポート機能によって生成されたドキュメントを表示するには、Microsoft Office 2007 以降をインストールしておく必要があります。

## <a name="regional-availability-languages-and-localization"></a>地域の使用可用性、言語、およびローカライズ

人事管理がサポートする国、地域、および言語に関する PDF ファイルを [Microsoft Dynamics 365 の国際可用性ガイド](https://docs.microsoft.com/dynamics365/get-started/availability) からダウンロードすることができます。 

> [!NOTE]
> ユーザー インターフェイスは他の言語にローカライズされますが、ユーザーデータすべては入力された言語で保存されます。 電子メールおよびテンプレートは他の言語で作成できますが、スケジューリング情報などのデータは、現時点では英語でのみ使用可能です。

国や地域固有のカスタマイズの作成、または現在 Microsoft にサポートされていない国や地域用のソリューションの作成に関心のある開発者は、[グローバリゼーション](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region) を参照してください。
