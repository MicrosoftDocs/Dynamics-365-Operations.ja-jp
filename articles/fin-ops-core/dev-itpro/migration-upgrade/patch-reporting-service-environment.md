---
title: 1 ボックス環境で SQL Server Reporting Services (SSRS) への修正プログラムの適用
description: SSRS 修正プログラムをワンボックス開発環境に適用します。
author: RobinARH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 23661
ms.assetid: 744bd1dc-d109-40df-a5dd-9db8982523a6
ms.search.region: Global
ms.author: shailesn
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f9165a52ec1f0dc0ca0e96a401ca2b7f7c445bdfa10133715e2f4e236bf7d74
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764448"
---
# <a name="patch-sql-server-reporting-services-ssrs-in-one-box-environments"></a>1 ボックス環境で SQL Server Reporting Services (SSRS) への修正プログラムの適用

[!include [banner](../includes/banner.md)]

次の手順は、1 ボックス開発環境のみを対象としています。

## <a name="patch-the-reporting-service"></a>Reporting Service のパッチ適用

次の手順は、1 ボックス開発環境のみを対象としています。

-   パッチ .zip file を Lifecycle Services (LCS) からダウンロードします。
-   レポート サービスの修正プログラムのデータのフォルダーにフォント ファイルがある場合は、SQL Server Reporting Services (SSRS) が実行されているコンピューターにこれらをインストールします。 Windows にフォントをインストールする方法の詳細については、 [windowsにフォントをインストールまたは削除する方法](https://support.microsoft.com/help/314960/how-to-install-or-remove-a-font-in-windows)を参照してください。  既にインストールされているフォントは再度インストールする必要はありません。
-   Reporting Services のパッチ スクリプト フォルダーのファイルを C:\\Packages\\Plugins\\AxReportVmRoleStartupTask の下にあるレポート プラグイン フォルダーにコピーします。
-   ディレクトリを、スクリプト ファイルを格納したレポート プラグイン フォルダに変更します。
-   以下に示すメソッドのいずれかを使用して、レポート拡張機能の古いインスタンスを置き換えます。
    -   レポート拡張機能を削除/再インストールします。 削除/再インストール オプションでは、インストールが完了した後にすべてのレポートを再配置する必要があります。
    -   SQL Server バイナリ フォルダーに手動でバイナリをコピーします。 手動でファイルをコピーする場合は、レポートを再展開する必要はありません。

### <a name="removereinstall-the-reporting-extension"></a>レポート拡張機能を削除/再インストール
SSRS が実行されているマシンの管理者グループのユーザーとして、以下の手順を実行します。

-   Windows PowerShell を使用して、次のスクリプトを実行することで、Dynamics SSRS 拡張機能を削除します。
    -   PowerShell .\\DeploySsrsExtension.ps1 –UninstallOnly
-   PowerShell では、次のスクリプトを実行することで Dynamics SSRS 拡張機能を再インストールします。
    -   PowerShell .\\DeploySsrsExtension.ps1
-   レポートの拡張機能を削除すると、すべてのレポートが削除されます。 レポート拡張機能を削除してから再インストールした場合は、次のスクリプトを実行してレポートを再展開する必要があります。
    -   Powershell .\\DeployAllReportsToSsrs.ps1
-   このタスクは、完了までに 20 ~ 30 分かかります。

### <a name="manually-copy-binaries-to-the-sql-server-binary-folder"></a>SQL Server バイナリ フォルダーへの手動でのバイナリのコピー
1.  SQL Server Reporting Services を停止します。 これは、**サービス管理コンソール** または **Reporting Services 構成マネージャー** から実行できます。 [![Configuration\_RSHotfix.](./media/configuration_rshotfix.png)](./media/configuration_rshotfix.png)
2.  SQL Server Reporting Services バイナリ フォルダーを検索します。 このフォルダーは、通常、C:\\Program Files\\Microsoft SQL Server\\MSRS11.MSSQLSERVER\\Reporting Services\\ReportServer\\bin にあります。
3.  次のファイルのいずれかがパッチにある場合は、それらのファイルを SQL Server Reporting Services Bin フォルダーにコピーします。* *

> [!NOTE]
> パッチは、サービスによって使用されるすべてのファイルを含む完全なパッチ、または変更されたファイルのみを含む増分パッチのいずれかです。 差分の修正プログラムを使用する場合は、一部のファイルが含まれない可能性があります。 パッチに含まれていないファイルは、置き換える必要はありません。

-   Microsoft.Dynamics.AX.Framework.Services.Platform.Client.dll
-   Microsoft.Dynamics.Framework.ReportsExtensions.dll
-   Microsoft.Dynamics.Framework.Reports.dll
-   Microsoft.Dynamics.ApplicationPlatform.SSRSReportRuntime.Instrumentation.dll
-   Microsoft.Dynamics.ApplicationPlatform.SSRSReportRuntime.man
-   Microsoft.Dynamics.Platform.Integration.ClientSdk.Abstraction.dll
-   Microsoft.Dynamics.AX.Framework.Reports.Shared.dll
-   Microsoft.Dynamics.AX.Framework.EncryptionEngine.dll
-   Microsoft.Dynamics.AX.Framework.Utilities.dll
-   Microsoft.Dynamics.ApplicationSuite.Reporting.BusinessLogic.dll
-   Microsoft.Dynamics.ApplicationPlatform.Environment.dll
-   Microsoft.Dynamics.AX.ReportConfiguration.axc
-   Microsoft.WindowsAzure.ServiceRuntime.dll
-   Microsoft.IdentityModel.dll
-   msshrtmi.dll

SQL Server Reporting Services を再起動します。

### <a name="reporting-service-installation"></a>Reporting Services インストール
レポート サービスのインストールでは、以下の変更が行われます。以下のファイルは、レポート サービスの bin フォルダー (C:\\Program Files\\Microsoft SQL Server\\MSRS11.MSSQLSERVER\\Reporting Services\\ReportServer\\bin) にコピーされ、対応する SSRS 設定ファイルが更新され、SSRS は拡張機能を認識します。

-   Dynamics.AX.Framework.Services.Platform.Client.dll
-   Dynamics.Framework.ReportsExtensions.dll
-   Dynamics.Framework.Reports.dll
-   Dynamics.ApplicationPlatform.SSRSReportRuntime.Instrumentation.dll
-   Dynamics.ApplicationPlatform.SSRSReportRuntime.man
-   Dynamics.Platform.Integration.ClientSdk.Abstraction.dll
-   Dynamics.AX.Framework.Reports.Shared.dll
-   Dynamics.AX.Framework.EncryptionEngine.dll
-   Dynamics.AX.Framework.Utilities.dll
-   Dynamics.ApplicationSuite.Reporting.BusinessLogic.dll
-   Dynamics.ApplicationPlatform.Environment.dll
-   Dynamics.AX.ReportConfiguration.axc
-   WindowsAzure.ServiceRuntime.dll
-   IdentityModel.dll
-   msshrtmi.dll

SSRS サービス アカウントはローカル システムを使用して更新されます。 新しい SSRS カタログ データベースの DynamicsAxReportServer と、一時データベースの DynamicsAxReportServerTempDB データベースが作成され、SSRS は、これら 2 つのデータベースを使用するように構成されます。 既定のカタログ データベース ReportServer と ReportServerTempDBstill は存在しますが、レポート サービスでは使用されないように設定されています。 SSRS サービスは、Windows 認証を使用するために更新されます。 xml 構成ファイル ReportPVMConfiguration.xml はレポート実行時間の SSRS bin フォルダー内に作成されます。 **Dynamics** という名前のレポート ルート フォルダーと **DynamicsBrowser** という名前のセキュリティ ロールが作成されます。 このカスタム ロールには AOS Web アプリケーションの AppPool ID とバッチ サービス アカウントの両方が追加されます。 配置中、レポート フォルダーは削除されてから再作成されることに注意してください。 したがって、以前に展開されたレポートはすべて SSRS サーバーから削除されます。  レポート拡張機能を再インストールした後は、レポートを再配置する必要があります。  





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]