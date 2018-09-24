---
title: "オンプレミス配置でのドキュメントの生成、発行、および印刷"
description: "このトピックでは、オンプレミス展開でのドキュメントの生成、公開、印刷の機能について説明します。"
author: TJVass
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysCorpNetPrinterList
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 99b2caa8d0aeee8d09a29c50cbe3ad335367adce
ms.contentlocale: ja-jp
ms.lasthandoff: 08/13/2018

---

# <a name="document-generation-publishing-and-printing-in-on-premises-deployments"></a>オンプレミス配置でのドキュメントの生成、発行、および印刷

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations のオンプレミス展開におけるドキュメントの生成、発行、印刷の機能について説明します。 Finance and Operations は、Microsoft SQL Server Reporting Services (SSRS) によるエンタープライズ ドキュメントの生成に対する、完全に統合された経験を提供します。 任意のサポートされているデバイスからは、ユーザーは、業務プロセスにリンクされている業界標準のドキュメントを生成できます。 これらのドキュメントには、請求書、小切手、梱包明細が含まれています。 ユーザーがネットワーク プリンターに安全に接続できるように、管理者は組み込みのツールを使用してサービスを構成します。

Microsoft Dynamics AX 2012 SQL Reporting Services フレームワーク上で構築されたソリューションをアップグレード、または [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com) で利用可能なモダン ソリューションを活用することができます。

## <a name="document-publishing-services-secure-reliable-and-convenient"></a>ドキュメント公開サービス: セキュリティ、信頼性、便利
従業員は、移動に多くの時間を費やします。 したがって、従業員がリモートで作業している間、企業は作業員の生産性を維持する能力に依存します。 ただし、現在でも、ドキュメントは業務トランザクションおよび記録管理のために不可欠です。

モバイル デバイスから、ネットワーク プリンターでドキュメントを印刷できます。 また、ビジネス ドキュメントの作成を自動化したり、組み込みツールを使用してドキュメントを複数の受信者に送信するように指定することもできます。

次のオプションがドキュメントの公開で使用できます。

- **電子メール** - サーバー経由でメールを配布し、レポートを添付ファイルとしてリンクします。
- **アーカイブ** - 将来の参照および規制順守のためにレポートを保管します。
- **ファイル** – ローカル印刷用にブラウザに直接ダウンロードされる PDF ファイルを作成します。
- **印刷** – サポートされているすべてのプラットフォームからネットワーク プリンターに直接ドキュメントを送信します。 これらのプラットフォームにはモバイル デバイスが含まれています。

![ドキュメント公開サービス](media/document-publishing-services.png)

クラウド ホスト環境ソリューションで使用できる情報アクセスのオプションの高レベルの概要については、[Finance and Operations アプリケーションで印刷](print-documents.md) を参照してください。

## <a name="comparing-the-cloud-hosted-and-on-premises-services"></a>クラウド ホスト サービスとオンプレミス サービスの比較
クラウド ホスト サービスとは異なり、オンプレミス パブリッシング サービスではドキュメントは PDF ファイルとして生成され、自動的にブラウザにダウンロードされます。 したがって、ローカル接続デバイスを使用してドキュメントを保存したり、ハード コピーを印刷することができます。 管理者は、組み込み管理ページを使用して、アプリケーションから直接ネットワーク プリンターへのアクセスを管理できます。 必要に応じてレポートを操作したり、定期的にドキュメントを安全に生成して配布するための自動ジョブをスケジュールできます。

次の図は、ドキュメントの印刷に関係するコンポーネントを示しています。

![ドキュメント印刷](media/Cloud-vs-on-premises.png)

拡張機能を使用して、アプリケーション レポートで埋め込みドリルスルー リンクの可用性を管理する方法の詳細については、付録を参照してください。

## <a name="managing-access-to-network-printers"></a>ネットワーク プリンターへのアクセスの管理
管理者は、組み込みの管理ページを使用して、ネットワーク プリンターへのアクセスを管理できます。 ネットワーク プリンターは会社ごとにセキュリティで保護され、アプリケーションのユーザーによって共有されます。 ユーザーが提供した設定に基づき、権限を持つドメイン アカウントを使用してドキュメントが出力されます。 オンプレミス配置では、プリンターや FAX などのドメイン リソースに接続するアダプターをインストールする必要はありません。

次の図は、ネットワーク プリンターの管理に使用されるページを示しています。

![ネットワーク プリンターのページの管理](media/manage-network-printers.png)

## <a name="appendix"></a>付録

### <a name="turning-on-embedded-links-in-business-documents"></a>ビジネス ドキュメントでのリンクの埋め込みを有効にする
PDF ドキュメントで埋め込みドリルスルー リンクの使用を可能にするコードを次に示します。 

```
class Controller extends SrsReportRunController
{
    protected void preRunModifyContract()
    {
        this.parmReportContract().parmRdlContract().parmEnableFileDrillThrough(true);
        super();
    }
    static void main(Args _args)
    {
        ...
    }
}
```

