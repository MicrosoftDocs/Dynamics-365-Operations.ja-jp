---
title: "メンテナンス モード"
description: "この記事では、Microsoft Dynamics 365 for Finance and Operations のメンテナンス モードについて説明します。 メンテナンス モードは、システム機能に影響を与える可能性のあるシステム変更を、システム管理者が安全に実行できる新しいシステム全体に適用される設定です。"
author: manalidongre
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SysConfiguration
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 70292
ms.assetid: c11a35e8-40bb-4005-adf3-cfd998a418fc
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 94b59eac447f3a5b4f0bd5660baae1a175de9627
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="maintenance-mode"></a>メンテナンス モード

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 for Finance and Operations のメンテナンス モードについて説明します。 メンテナンス モードは、システム機能に影響を与える可能性のあるシステム変更を、システム管理者が安全に実行できる新しいシステム全体に適用される設定です。

Microsoft Dynamics 365 for Finance and Operations には、メンテナンス モードという名前の新しいシステム全体に適用される設定が含まれています。 メンテナンス モードを有効にすると、システム機能に影響を与える可能性のあるシステム変更を、システム管理者が安全に実行する方法が提供されます。 たとえば、コンフィギュレーション キーは、有効または無効にすることができます。 メンテナンス モードがオンのとき、システム管理者および **メンテナンス モード ユーザー** ロールを持つユーザーのみがシステムにサインインすることができます。 既定では、メンテナンス モードがオフになっています。

## <a name="turning-maintenance-mode-on-and-off"></a>メンテナンス モードのオン/オフを切り替え
メンテナンス モードがオフのとき、**ライセンス コンフィギュレーション** ページを編集することはできません。
次のコマンドを実行して、メンテナンス モードをローカルでオンにすることができます。 

**注記:** 一部の仮想マシン (VM) では、Deployment.Setup.exe ツールの正確な場所が異なる場合があります。 AosServiceWebRootbin を確認してください。

    J:\AosService\PackagesLocalDirectory\Bin\Microsoft.Dynamics.AX.Deployment.Setup.exe --metadatadir J:\AosService\PackagesLocalDirectory --bindir J:\AosService\PackagesLocalDirectory\Bin --sqlserver . --sqldatabase axdb --sqluser axdbadmin --sqlpwd ********* --setupmode maintenancemode --isinmaintenancemode true

次のテーブルに、このコマンドで使用されるパラメーターを示します。

| パラメーター名              | 説明                                                                                                       |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------|
| --setupmode maintenancemode | システムをメンテナンス モードにするかメンテナンス モードを解除するかをセットアップ ツールに通知するには、このパラメーターを使用します。    |
| --metadatadir               | メタデータ ディレクトリ を指定するには、このパラメーターを使用します。 既定のパッケージ ディレクトリを使用する必要があります。              |
| --bindir                    | バイナリ ディレクトリ を指定するには、このパラメーターを使用します。 既定のパッケージ ディレクトリを使用する必要があります。              |
| --sqlserver                 | Microsoft SQL Server を指定するには、このパラメーターを使用します。 1 ボックス環境では、ピリオド (**.**) を使用します。           |
| --sqluser                   | SQL Server のユーザーを指定するには、このパラメーターを使用します。 **AOSUser** を使用する必要があります。                                    |
| --sqlpwd                    | SQL Server のパスワードを指定するには、このパラメーターを使用します。                                                            |
| --isinmaintenancemode       | 構成モードを有効または無効にするには、このパラメーターを使用します。 オンにするには **true** とし、オフにするには **false** にします。 |

Microsoft Dynamics 365 for Finance and Operations の Application Object Server (AOS)のインスタンスを再起動すると、システムはメンテナンス モードになります。 次のスクリーン ショットに示すように、構成キーを有効にすることができます。 

[![license-configuration-page-when-not-in-maintenance-mode](./media/license-configuration-page-when-not-in-maintenance-mode.png)](./media/license-configuration-page-when-not-in-maintenance-mode.png) 

システムがメンテナンス モードになっているときに、システム管理者または**メンテナンス モード ユーザー** ロールを持つユーザーではない人が、Finance and Operations にアクセスしようとすると、エラー メッセージが表示されます。 

次のコマンドを実行して、メンテナンス モードをオフにすることができます。

    J:\AosService\PackagesLocalDirectory\Bin\Microsoft.Dynamics.AX.Deployment.Setup.exe --metadatadir J:\AosService\PackagesLocalDirectory --bindir J:\AosService\PackagesLocalDirectory\Bin --sqlserver . --sqldatabase axdb --sqluser axdbadmin --sqlpwd ********* --setupmode maintenancemode --isinmaintenancemode false

## <a name="maintenance-mode-in-production-environments"></a>実稼動環境でのメンテナンス モード
実稼動環境でメンテナンス モードを有効にするには、**サービス要求** ページで LCS の **その他の要求** フォームを使用して、Dynamics サービス エンジニアリング (DSE) チームに要求を送信する必要があります。 LCS を通しての要求の送信の詳細については、[Dynamics サービス エンジニア リング チームへの要求の送信](../lifecycle-services/submit-request-dynamics-service-engineering-team.md) を参照してください。 

Dynamics サービス エンジニアリング チームは、システムをメンテナンス モードにし、お客様と連携してコンフィギュレーションの更新を完了します。 更新が完了したという確認をチームが受け取った後、メンテナンス モードからシステムが削除されます。

## <a name="troubleshooting"></a>トラブルシューティング
イベント ビューアーにエラーが検出できます。




