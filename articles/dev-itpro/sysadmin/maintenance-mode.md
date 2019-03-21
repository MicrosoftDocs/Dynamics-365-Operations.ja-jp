---
title: メンテナンス モード
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のメンテナンス モードに関する情報を提供します。 メンテナンス モードは、システム機能に影響を与える可能性のあるシステム変更を、システム管理者が安全に実行できるシステム全体に適用される設定です。
author: manalidongre
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysConfiguration
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 70292
ms.assetid: c11a35e8-40bb-4005-adf3-cfd998a418fc
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b1ced105f238b6cd97d17c114478128cc9ea6b1
ms.sourcegitcommit: 980cf8280538f37d64c477576a67f66bb00252d3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2019
ms.locfileid: "776910"
---
# <a name="maintenance-mode"></a>メンテナンス モード

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/limited-availability.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations のメンテナンス モードに関する情報を提供します。 メンテナンス モードを有効にすると、システム機能に影響を与える可能性のあるシステム変更を、システム管理者が安全に実行する方法が提供されます。 たとえば、コンフィギュレーション キーは、有効または無効にすることができます。 メンテナンス モードがオンのとき、システム管理者および **メンテナンス モード ユーザー** ロールを持つユーザーのみがシステムにサインインすることができます。 既定では、メンテナンス モードがオフになっています。 メンテナンス モードがオフのとき、**ライセンス コンフィギュレーション** ページを編集することはできません。

## <a name="turn-maintenance-mode-on-and-off-on-sandbox-and-production-environments-through-lifecycle-services"></a>Lifecycle Services を通じてサンドボックスおよび運用環境でメンテナンス モードを有効または無効にする 
サンドボックスおよび運用環境で、Lifecycle Services (LCS) を通じて直接メンテナンス モードを有効または無効にできます。 これを行うには、次の手順を参照してください。

1. 環境の詳細ページに移動し、**メンテナンス** メニューで **メンテナンス モードの構成** をクリックします。 プレビューに追加された顧客に対してこのメニュー項目が表示されます。
2. スライダーで、環境の **メンテナンス モードを有効にする** を設定し、**確認** を選択します。
3. サービス工程が開始され、システムがメンテナンス モードになります。
4. 完了時、環境の状態が **メンテナンス中** になります。 この時点では、システム管理者だけが環境にアクセスできます。
5. システム全体にわたる変更を完了した後、環境更新セクションで **メンテナンス モードの無効化** をクリックすることで、メンテナンス モードをオフにすることができます。
6. これにより、環境のメンテナンス モードを終了するサービス操作が開始されます。 環境の詳細ページで、工程の進捗状況を確認できます。
7. これが完了すると、環境が **配置中** 状態に戻ります。 すべてのユーザーが環境にログオンできるようになりました。
8. メンテナンス モードが有効または無効かを環境の履歴ページで確認することができます。 環境履歴ページに移動するには環境の詳細ページで **履歴** および **環境の変更** を選択します。

サンドボックスおよび運用環境のメンテナンス モードをオン/オフにする操作と、サービス操作にとても似ています。 メンテナンス モードのオンまたはオフに失敗した場合は、**再開**、**ロールバック**、および **中止** などのオプションが表示されます。 操作に失敗した理由をトラブルシューティングするために**ログをダウンロード**するオプションもあります。

## <a name="turn-maintenance-mode-on-and-off-in-devtestdemo-environments-and-vhd-based-hosted-environments"></a>DevTest/デモ環境およびVHD ベースのホストされている環境でメンテナンス モードのオンとオフを切り替える

次のコマンドを実行して、メンテナンス モードをローカルでオンにすることができます。 

> [!Note]
> 一部の仮想マシン (VM) では、Deployment.Setup.exe ツールの正確な場所が異なる場合があります。 AosServiceWebRootbin を確認してください。

    J:\AosService\PackagesLocalDirectory\Bin\Microsoft.Dynamics.AX.Deployment.Setup.exe --metadatadir J:\AosService\PackagesLocalDirectory --bindir J:\AosService\PackagesLocalDirectory\Bin --sqlserver . --sqldatabase axdb --sqluser axdbadmin --sqlpwd ********* --setupmode maintenancemode --isinmaintenancemode true

次のテーブルに、このコマンドで使用されるパラメーターを示します。

| パラメーター名              | 説明  |
|-----------------------------|------|
| --setupmode maintenancemode | システムをメンテナンス モードにするかメンテナンス モードを解除するかをセットアップ ツールに通知するには、このパラメーターを使用します。    |
| --metadatadir               | メタデータ ディレクトリ を指定するには、このパラメーターを使用します。 既定のパッケージ ディレクトリを使用する必要があります。              |
| --bindir                    | バイナリ ディレクトリ を指定するには、このパラメーターを使用します。 既定のパッケージ ディレクトリを使用する必要があります。              |
| --sqlserver                 | このパラメーターを使用して Microsoft SQL Server を指定します。 1 ボックス環境では、ピリオド (**.**) を使用します。           |
| --sqluser                   | SQL Server のユーザーを指定するには、このパラメーターを使用します。 **AOSUser** を使用する必要があります。                                    |
| --sqlpwd                    | SQL Server のパスワードを指定するには、このパラメーターを使用します。                                                            |
| --isinmaintenancemode       | 構成モードを有効または無効にするには、このパラメーターを使用します。 オンにするには **true** とし、オフにするには **false** にします。 |

Finance and Operations の Application Object Server (AOS) のインスタンスを再起動すると、システムはメンテナンス モードになります。 次のスクリーンショットに示すように、構成キーを有効にすることができます。 

[![license-configuration-page-when-not-in-maintenance-mode](./media/license-configuration-page-when-not-in-maintenance-mode.png)](./media/license-configuration-page-when-not-in-maintenance-mode.png) 

システムがメンテナンス モードになっているときに、システム管理者または**メンテナンス モード ユーザー** ロールを持つユーザーではない人が、Finance and Operations にアクセスしようとすると、エラー メッセージが表示されることがあります。 

次のコマンドを実行して、メンテナンス モードをオフにすることができます。

    J:\AosService\PackagesLocalDirectory\Bin\Microsoft.Dynamics.AX.Deployment.Setup.exe --metadatadir J:\AosService\PackagesLocalDirectory --bindir J:\AosService\PackagesLocalDirectory\Bin --sqlserver . --sqldatabase axdb --sqluser axdbadmin --sqlpwd ********* --setupmode maintenancemode --isinmaintenancemode false

