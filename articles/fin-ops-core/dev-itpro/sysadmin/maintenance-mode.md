---
title: メンテナンス モード
description: この記事では、メンテナンス モードについて説明します。メンテナンス モードは、システム管理者がシステム機能に影響を与える可能性のあるシステム変更を行うための、システム全体に適用される設定です。
author: laneswenka
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysConfiguration
audience: IT Pro
ms.reviewer: sericks
ms.custom: 70292
ms.assetid: c11a35e8-40bb-4005-adf3-cfd998a418fc
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a6fe67861829bf874512b20e21715a5608252d5
ms.sourcegitcommit: e4b6521337dfff3515f70086b0125d4c23308c71
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262346"
---
# <a name="maintenance-mode"></a>メンテナンス モード

[!include [banner](../includes/banner.md)]

この記事では、財務と運用アプリのメンテナンス モードについて説明します。 メンテナンス モードを有効にすると、システム機能に影響を与える可能性のあるシステム変更を、システム管理者が安全に実行する方法が提供されます。 たとえば、コンフィギュレーション キーは、有効または無効にすることができます。 メンテナンス モードがオンのとき、システム管理者および **メンテナンス モード ユーザー** ロールを持つユーザーのみがシステムにサインインすることができます。 既定では、メンテナンス モードがオフになっています。 メンテナンス モードがオフのとき、**ライセンス コンフィギュレーション** ページを編集することはできません。

> [!Note]
> 環境でメンテナンス モードを有効にした後は、対話型の AOS と非対話型 AOS (バッチ AOS) を 1 つしか使用できません。

## <a name="turn-maintenance-mode-on-and-off-on-sandbox-and-production-environments-through-lifecycle-services"></a>Lifecycle Services を通じてサンドボックスおよび運用環境でメンテナンス モードを有効または無効にする 
サンドボックスおよび運用環境で、Lifecycle Services (LCS) を通じて直接メンテナンス モードを有効または無効にできます。 これを行うには、次の手順を参照してください。

1. 環境の詳細ページに移動し、 **メンテナンス** メニューで **メンテナンス モードの有効化** をクリックします。 
2. スライダーで、環境の **メンテナンス モードを有効にする** を設定し、**確認** を選択します。
3. サービス工程が開始され、システムがメンテナンス モードになります。
4. 完了時、環境の状態が **メンテナンス中** になります。 この時点では、システム管理者だけが環境にアクセスできます。
5. システム全体の変更を完了後、 **メンテナンス** メニューの **メンテナンスモードの無効化** をクリックすることで、メンテナンス モードをオフにすることができます。
6. これにより、環境のメンテナンス モードを終了するサービス操作が開始されます。 環境の詳細ページで、工程の進捗状況を確認できます。
7. これが完了すると、環境が **配置中** 状態に戻ります。 すべてのユーザーが環境にログオンできるようになりました。
8. メンテナンス モードが有効または無効かを環境の履歴ページで確認することができます。 環境履歴ページに移動するには環境の詳細ページで **履歴** および **環境の変更** を選択します。

サンドボックスおよび運用環境のメンテナンス モードをオン/オフにする操作と、サービス操作にとても似ています。 メンテナンス モードのオンまたはオフに失敗した場合は、**再開**、**ロールバック**、および **中止** などのオプションが表示されます。 操作に失敗した理由をトラブルシューティングするために **ログをダウンロード** するオプションもあります。

## <a name="turn-maintenance-mode-on-and-off-in-devtestdemo-environments-hosted-in-customers-subscription"></a>顧客のサブスクリプションで動作している開発テスト環境またはデモ環境にてメンテナンス モードをオンにする/オフにする
1. 開発者のマシンに RDP の接続を確立します。
2. 開発者のマシンで、LCS から axdbadmin ユーザーの資格情報を使用して SQL Server にサインインします。 次に、AXDB データベースに切り替えて、次のコマンドを実行します。

    ```Console
    update SQLSYSTEMVARIABLES SET VALUE = 1 where PARM = 'CONFIGURATIONMODE'
    ```

3. **World Wide Web 公開サービス** を再起動して IIS をリセットします。
4. サービスが再起動されると、システムはメンテナンス モードになります。
5. メンテナンス モードの活動を完了したら、ステップ 2 および 3 を繰り返しますが、値はステップ 2 で 0 に設定します。

## <a name="turn-maintenance-mode-on-and-off-for-vhd-based-environments-hosted-by-customers"></a>顧客がホストする VHD ベース環境でメンテナンス モードのオン/オフを切り替える

次のコマンドを実行して、メンテナンス モードをローカルでオンにすることができます。 

> [!Note]
> 一部の仮想マシン (VM) では、Deployment.Setup.exe ツールの正確な場所が異なる場合があります。 AosServiceWebRootbin を確認してください。

```Console
J:\AosService\PackagesLocalDirectory\Bin\Microsoft.Dynamics.AX.Deployment.Setup.exe --metadatadir J:\AosService\PackagesLocalDirectory --bindir J:\AosService\PackagesLocalDirectory\Bin --sqlserver . --sqldatabase axdb --sqluser axdbadmin --sqlpwd ********* --setupmode maintenancemode --isinmaintenancemode true
```
コマンドを実行した後、**World Wide Web 公開サービス** を再起動して、IIS をリセットします。 その後、システムはメンテナンス モードになります。  

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

## <a name="enable-or-disable-configuration-keys"></a>コンフィギュレーション キーの有効化 (または無効化)

Application Object Server (AOS) のインスタンスを再起動すると、システムはメンテナンス モードになります。 次のスクリーンショットに示すように、構成キーを有効にすることができます。 

[![メンテナンス モード以外のライセンス コンフィギュレーション ページ。](./media/license-configuration-page-when-not-in-maintenance-mode.png)](./media/license-configuration-page-when-not-in-maintenance-mode.png) 

メンテナンス モードになっている際にシステムへアクセスしようとすると、システム管理者または **メンテナンス モード ユーザー** ロールを持つユーザーではない人が、Finance and Operations にアクセスしようとすると、エラー メッセージが表示されることがあります。 

次のコマンドを実行して、メンテナンス モードをオフにすることができます。

```Console
J:\AosService\PackagesLocalDirectory\Bin\Microsoft.Dynamics.AX.Deployment.Setup.exe --metadatadir J:\AosService\PackagesLocalDirectory --bindir J:\AosService\PackagesLocalDirectory\Bin --sqlserver . --sqldatabase axdb --sqluser axdbadmin --sqlpwd ********* --setupmode maintenancemode --isinmaintenancemode false
```
コマンドを実行した後、**World Wide Web 公開サービス** を再起動して、IIS をリセットします。 その後、システムはメンテナンス モードではなくなります。  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

